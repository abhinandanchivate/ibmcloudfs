Here is the **complete Express + MongoDB REST API setup** with:



---

### ✅ Final FOLDER STRUCTURE

```
project-root/
├── config/
│   ├── default.json
│   ├── development.json
│   ├── production.json
│   └── test.json
├── controllers/
│   ├── departmentController.js
│   ├── employeeController.js
│   └── userController.js
├── middleware/
│   ├── authMiddleware.js
│   └── logger.js
├── models/
│   ├── Department.js
│   ├── Employee.js
│   └── User.js
├── routes/
│   ├── departmentRoutes.js
│   ├── employeeRoutes.js
│   └── userRoutes.js
├── validators/
│   └── validators.js
├── app.js
├── server.js
├── package.json
└── README.md
```

---

### ✅ CONFIG FILES

#### `config/default.json`

```json
{
  "PORT": 5000,
  "MONGO_URI": "mongodb://localhost:27017/employeesystem",
  "JWT_SECRET": "default_secret"
}
```

#### `config/development.json`

```json
{
  "MONGO_URI": "mongodb://localhost:27017/dev_employeesystem",
  "JWT_SECRET": "dev_secret"
}
```

#### `config/production.json`

```json
{
  "MONGO_URI": "mongodb+srv://your_prod_uri",
  "JWT_SECRET": "prod_secret"
}
```

#### `config/test.json`

```json
{
  "MONGO_URI": "mongodb://localhost:27017/test_employeesystem",
  "JWT_SECRET": "test_secret"
}
```

---

### ✅ DATABASE CONNECTION – `config/db.js`

```js
import mongoose from 'mongoose';
import config from 'config';

const dbURI = config.get('MONGO_URI');

const connectDB = async () => {
  try {
    await mongoose.connect(dbURI, {
      useNewUrlParser: true,
      useUnifiedTopology: true
    });
    console.log('MongoDB Connected');
  } catch (err) {
    console.error('DB connection error:', err.message);
    process.exit(1);
  }
};

export default connectDB;
```

---

### ✅ MODELS

#### `models/User.js`

```js
import mongoose from 'mongoose';

const userSchema = new mongoose.Schema({
  username: { type: String, required: true, unique: true },
  email: { type: String, required: true, unique: true },
  password: { type: String, required: true }
});

export default mongoose.model('User', userSchema);
```

#### `models/Employee.js`

```js
import mongoose from 'mongoose';

const employeeSchema = new mongoose.Schema({
  name: { type: String, required: true },
  role: { type: String, required: true },
  department: { type: mongoose.Schema.Types.ObjectId, ref: 'Department' }
});

export default mongoose.model('Employee', employeeSchema);
```

#### `models/Department.js`

```js
import mongoose from 'mongoose';

const departmentSchema = new mongoose.Schema({
  name: { type: String, required: true },
  location: { type: String, required: true }
});

export default mongoose.model('Department', departmentSchema);
```

---

### ✅ VALIDATORS – `validators/validators.js`

```js
import { body } from 'express-validator';

export const validateUser = [
  body('username').notEmpty(),
  body('email').isEmail(),
  body('password').isLength({ min: 6 })
];

export const validateEmployee = [
  body('name').notEmpty(),
  body('role').notEmpty(),
  body('department').notEmpty()
];

export const validateDepartment = [
  body('name').notEmpty(),
  body('location').notEmpty()
];
```

---

### ✅ MIDDLEWARE

#### `middleware/authMiddleware.js`

```js
import jwt from 'jsonwebtoken';
import config from 'config';

const jwtSecret = config.get('JWT_SECRET');

export const protect = (req, res, next) => {
  const token = req.headers.authorization?.split(' ')[1];
  if (!token) return res.status(401).json({ message: 'Unauthorized: No token' });

  try {
    const decoded = jwt.verify(token, jwtSecret);
    req.user = decoded;
    next();
  } catch (err) {
    res.status(401).json({ message: 'Unauthorized: Invalid token' });
  }
};
```

#### `middleware/logger.js`

```js
import morgan from 'morgan';

const logger = morgan('dev');
export default logger;
```

---

### ✅ CONTROLLERS

#### `controllers/userController.js`

```js
import User from '../models/User.js';
import jwt from 'jsonwebtoken';
import bcrypt from 'bcryptjs';
import config from 'config';

export const register = async (req, res) => {
  const { username, email, password } = req.body;
  const hashed = await bcrypt.hash(password, 10);
  const user = new User({ username, email, password: hashed });
  await user.save();
  res.status(201).json({ message: 'User registered' });
};

export const login = async (req, res) => {
  const { email, password } = req.body;
  const user = await User.findOne({ email });
  if (!user || !(await bcrypt.compare(password, user.password))) {
    return res.status(400).json({ message: 'Invalid credentials' });
  }
  const token = jwt.sign({ id: user._id }, config.get('JWT_SECRET'), { expiresIn: '1d' });
  res.json({ token });
};
```

#### `controllers/employeeController.js`

```js
import Employee from '../models/Employee.js';

export const createEmployee = async (req, res) => {
  const employee = new Employee(req.body);
  await employee.save();
  res.status(201).json(employee);
};

export const getEmployees = async (req, res) => {
  const employees = await Employee.find().populate('department');
  res.json(employees);
};

export const updateEmployee = async (req, res) => {
  const emp = await Employee.findByIdAndUpdate(req.params.id, req.body, { new: true });
  res.json(emp);
};

export const deleteEmployee = async (req, res) => {
  await Employee.findByIdAndDelete(req.params.id);
  res.json({ message: 'Deleted' });
};
```

#### `controllers/departmentController.js`

```js
import Department from '../models/Department.js';

export const createDepartment = async (req, res) => {
  const dept = new Department(req.body);
  await dept.save();
  res.status(201).json(dept);
};

export const getDepartments = async (req, res) => {
  const depts = await Department.find();
  res.json(depts);
};

export const updateDepartment = async (req, res) => {
  const dept = await Department.findByIdAndUpdate(req.params.id, req.body, { new: true });
  res.json(dept);
};

export const deleteDepartment = async (req, res) => {
  await Department.findByIdAndDelete(req.params.id);
  res.json({ message: 'Deleted' });
};
```

---

### ✅ ROUTES

#### `routes/userRoutes.js`

```js
import express from 'express';
import { register, login } from '../controllers/userController.js';
import { validateUser } from '../validators/validators.js';
import { validationResult } from 'express-validator';

const router = express.Router();

const validate = (req, res, next) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) return res.status(400).json({ errors: errors.array() });
  next();
};

router.post('/register', validateUser, validate, register);
router.post('/login', login);

export default router;
```

#### `routes/employeeRoutes.js`

```js
import express from 'express';
import {
  createEmployee,
  getEmployees,
  updateEmployee,
  deleteEmployee
} from '../controllers/employeeController.js';
import { protect } from '../middleware/authMiddleware.js';
import { validateEmployee } from '../validators/validators.js';
import { validationResult } from 'express-validator';

const router = express.Router();

const validate = (req, res, next) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) return res.status(400).json({ errors: errors.array() });
  next();
};

router.route('/')
  .get(protect, getEmployees)
  .post(protect, validateEmployee, validate, createEmployee);

router.route('/:id')
  .put(protect, updateEmployee)
  .delete(protect, deleteEmployee);

export default router;
```

#### `routes/departmentRoutes.js`

```js
import express from 'express';
import {
  createDepartment,
  getDepartments,
  updateDepartment,
  deleteDepartment
} from '../controllers/departmentController.js';
import { protect } from '../middleware/authMiddleware.js';
import { validateDepartment } from '../validators/validators.js';
import { validationResult } from 'express-validator';

const router = express.Router();

const validate = (req, res, next) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) return res.status(400).json({ errors: errors.array() });
  next();
};

router.route('/')
  .get(protect, getDepartments)
  .post(protect, validateDepartment, validate, createDepartment);

router.route('/:id')
  .put(protect, updateDepartment)
  .delete(protect, deleteDepartment);

export default router;
```

---

### ✅ `app.js`

```js
import express from 'express';
import cors from 'cors';
import logger from './middleware/logger.js';
import userRoutes from './routes/userRoutes.js';
import employeeRoutes from './routes/employeeRoutes.js';
import departmentRoutes from './routes/departmentRoutes.js';

const app = express();

app.use(cors());
app.use(logger);
app.use(express.json());

app.use('/api/users', userRoutes);
app.use('/api/employees', employeeRoutes);
app.use('/api/departments', departmentRoutes);

export default app;
```

---

### ✅ `server.js`

```js
import config from 'config';
import connectDB from './config/db.js';
import app from './app.js';

const PORT = config.get('PORT') || 5000;

connectDB();
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
});
```

---


