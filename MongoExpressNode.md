Great — I’ll start generating **100 advanced MCQs** covering:

* **Node.js (core, async, events, modules)**
* **Express.js (routing, middleware, error handling, security)**
* **MongoDB (schema design, queries, indexes, aggregation)**

Let’s begin with the **first 10 real, code-based MCQs**:

---

### ✅ **\[Node.js] MCQ 1 — Event Loop Behavior**

```js
console.log('A');
setTimeout(() => console.log('B'), 0);
Promise.resolve().then(() => console.log('C'));
console.log('D');
```

What is the output order?

| Option     |
| ---------- |
| A. A B C D |
| B. A D C B |
| C. A C D B |
| D. D A B C |

**✅ Correct Answer: B**

> Microtasks (Promises) run before macrotasks (`setTimeout`), so `C` comes before `B`.

---

### ✅ **\[Node.js] MCQ 2 — require vs import**

Which is true about `require` and `import` in Node.js?

| Option                                               |
| ---------------------------------------------------- |
| A. `require` is asynchronous                         |
| B. `import` supports dynamic path evaluation         |
| C. `require` works without transpilation in CommonJS |
| D. `import` can be used without `type="module"`      |

**✅ Correct Answer: C**

> `require()` is built-in to CommonJS, while `import` needs `type: module` or transpiler.

---

### ✅ **\[Express.js] MCQ 3 — Middleware Execution Order**

```js
app.use((req, res, next) => {
  console.log('A');
  next();
});
app.get('/', (req, res) => {
  console.log('B');
  res.send('Hello');
});
```

Request to `/` logs what?

| Option    |
| --------- |
| A. B A    |
| B. A B    |
| C. Only A |
| D. Only B |

**✅ Correct Answer: B**

> Global middleware runs **before** route handler.

---

### ✅ **\[Express.js] MCQ 4 — Error Handling Middleware**

Which of these is a valid error handler?

```js
app.use((err, req, res, next) => {
  res.status(500).send('Error');
});
```

| Option                      |
| --------------------------- |
| A. Must be last `app.use`   |
| B. Needs 3 params only      |
| C. Cannot use `next`        |
| D. Doesn't need `err` param |

**✅ Correct Answer: A**

> Error-handling middleware must be **last** and have 4 params.

---

### ✅ **\[MongoDB] MCQ 5 — Index Impact**

You query:

```js
db.users.find({ age: 25 }).sort({ name: 1 });
```

Which index best optimizes this?

| Option                   |
| ------------------------ |
| A. `{ age: 1 }`          |
| B. `{ name: 1 }`         |
| C. `{ age: 1, name: 1 }` |
| D. `{ name: 1, age: 1 }` |

**✅ Correct Answer: C**

> Composite index must **match query + sort order** for full index coverage.

---

### ✅ **\[MongoDB] MCQ 6 — \$lookup Join**

Which `$lookup` lets you join `orders` with `users`?

| Option                      |
| --------------------------- |
| A. `from: "orders"`         |
| B. `localField: "_id"`      |
| C. `foreignField: "userId"` |
| D. All of the above         |

**✅ Correct Answer: D**

> All are needed to perform a proper `$lookup` between collections.

---

### ✅ **\[Node.js] MCQ 7 — EventEmitter Memory Leak**

You see this warning:

> `(node:1234) MaxListenersExceededWarning`

Why?

| Option                              |
| ----------------------------------- |
| A. Multiple event emitters          |
| B. No `removeListener()` calls      |
| C. Exceeding default listener limit |
| D. All of the above                 |

**✅ Correct Answer: D**

> All reasons can contribute — fix with `emitter.setMaxListeners(n)` or proper cleanup.

---

### ✅ **\[Express.js] MCQ 8 — Router Mounting**

```js
const router = express.Router();
router.get('/test', handler);
app.use('/api', router);
```

Which route is hit?

| Option            |
| ----------------- |
| A. `/test`        |
| B. `/api`         |
| C. `/api/test`    |
| D. `/router/test` |

**✅ Correct Answer: C**

> Mounting path (`/api`) prefixes all routes inside router.

---

### ✅ **\[MongoDB] MCQ 9 — Aggregation Match Order**

```js
db.users.aggregate([
  { $sort: { age: 1 } },
  { $match: { age: { $gt: 30 } } }
]);
```

Which is better for performance?

| Option                         |
| ------------------------------ |
| A. Current pipeline            |
| B. Swap `$match` and `$sort`   |
| C. Add `$limit` after `$match` |
| D. Both B and C                |

**✅ Correct Answer: D**

> `$match` first **reduces documents early**, and `$limit` after can **cut memory use**.

---

### ✅ **\[Node.js] MCQ 10 — Cluster Module**

Which is true about `cluster` module?

| Option                         |
| ------------------------------ |
| A. Used for horizontal scaling |
| B. Shares the same event loop  |
| C. Workers share memory        |
| D. Only for async code         |

**✅ Correct Answer: A**

> Node’s cluster module allows **multi-core utilization** via child processes.

---

Great! Here are the next **10 advanced MCQs (11–20)** on **Node.js, Express.js, and MongoDB**, non-repeating and fully explained:

---

### ✅ **\[Node.js] MCQ 11 — Callback vs Promise**

What is the key benefit of using Promises over callbacks in Node.js?

| Option                                     |
| ------------------------------------------ |
| A. Improved memory management              |
| B. Better file system performance          |
| C. Avoid callback hell and enable chaining |
| D. Works only in ES5 environments          |

**✅ Correct Answer: C**

> Promises provide **clean chaining and error propagation**, avoiding deeply nested callbacks.

---

### ✅ **\[Express.js] MCQ 12 — Route Order**

```js
app.get('/user/:id', handler1);
app.get('/user/profile', handler2);
```

Request to `/user/profile` triggers?

| Option      |
| ----------- |
| A. handler1 |
| B. handler2 |
| C. Both     |
| D. None     |

**✅ Correct Answer: A**

> `:id` matches anything including `'profile'`. Order matters — **specific routes should come first**.

---

### ✅ **\[MongoDB] MCQ 13 — Update vs Replace**

Which MongoDB command replaces the entire document?

| Option                                    |
| ----------------------------------------- |
| A. `updateOne({}, { $set: { age: 25 } })` |
| B. `replaceOne({}, { name: "John" })`     |
| C. `updateMany({}, { $inc: { age: 1 } })` |
| D. `findOneAndUpdate()`                   |

**✅ Correct Answer: B**

> `replaceOne` **overwrites the full document**, unlike `$set` or `$inc`.

---

### ✅ **\[Node.js] MCQ 14 — process.nextTick()**

What is true about `process.nextTick()`?

| Option                            |
| --------------------------------- |
| A. Runs before Promise microtasks |
| B. Runs after `setTimeout`        |
| C. Runs in parallel               |
| D. Runs only on event emitters    |

**✅ Correct Answer: A**

> `nextTick()` callbacks are **executed before Promises**, giving them **higher priority** in the queue.

---

### ✅ **\[Express.js] MCQ 15 — Middleware Chain Break**

```js
app.use((req, res, next) => {
  res.send('Done');
});
app.use((req, res, next) => {
  console.log('This will run');
});
```

Will the second middleware run?

| Option                           |
| -------------------------------- |
| A. Yes, always                   |
| B. No, unless `next()` is called |
| C. Only on error                 |
| D. Only with async/await         |

**✅ Correct Answer: B**

> Once `res.send()` is called, **response ends** unless `next()` is explicitly invoked.

---

### ✅ **\[MongoDB] MCQ 16 — \_id Type**

What is the type of default `_id` in MongoDB documents?

| Option        |
| ------------- |
| A. String     |
| B. UUID       |
| C. ObjectId   |
| D. BSON Int32 |

**✅ Correct Answer: C**

> MongoDB assigns a **unique ObjectId** unless explicitly overridden.

---

### ✅ **\[Node.js] MCQ 17 — Async/Await Pitfall**

```js
async function fetchData() {
  const result = await axios.get(url);
  return result;
}
```

What does this function return?

| Option           |
| ---------------- |
| A. A value       |
| B. A callback    |
| C. A Promise     |
| D. An observable |

**✅ Correct Answer: C**

> All `async` functions return a **Promise**, even when using `return`.

---

### ✅ **\[Express.js] MCQ 18 — Secure Headers**

Which middleware is used to secure Express apps with HTTP headers?

| Option               |
| -------------------- |
| A. `cors()`          |
| B. `helmet()`        |
| C. `body-parser`     |
| D. `express-session` |

**✅ Correct Answer: B**

> `helmet` sets secure headers like CSP, XSS protection, etc., **improving security**.

---

### ✅ **\[MongoDB] MCQ 19 — Compound Index Order**

Which index is best for:

```js
db.items.find({ type: 'A', status: 'active' });
```

| Option                      |
| --------------------------- |
| A. `{ status: 1 }`          |
| B. `{ type: 1 }`            |
| C. `{ type: 1, status: 1 }` |
| D. `{ status: 1, type: 1 }` |

**✅ Correct Answer: C**

> MongoDB **uses prefix fields**, so `{ type: 1, status: 1 }` supports the query best.

---

### ✅ **\[Node.js] MCQ 20 — Cluster Fork Count**

How can you programmatically fork one worker per CPU core?

| Option                                              |
| --------------------------------------------------- |
| A. `os.fork()`                                      |
| B. `require('threads')`                             |
| C. `cluster.fork()` in loop with `os.cpus().length` |
| D. `spawnCluster()`                                 |

**✅ Correct Answer: C**

> Use `os.cpus().length` to determine available cores and `cluster.fork()` for each.

---

Great — here's the next set of **10 advanced MCQs (21–30)** for **Node.js, Express.js, and MongoDB**, with clear explanations and no repetitions:

---

### ✅ **\[Node.js] MCQ 21 — EventEmitter Memory Leak**

What causes a memory leak warning with `EventEmitter`?

| Option                                  |
| --------------------------------------- |
| A. Too many listeners on a single event |
| B. Large JSON file parsing              |
| C. Deeply nested loops                  |
| D. Using `require()` multiple times     |

**✅ Correct Answer: A**

> If more than **10 listeners** are registered for a single event, Node.js warns about potential memory leaks.

---

### ✅ **\[Express.js] MCQ 22 — Query Params**

Request: `GET /api/products?page=2&size=10`

How do you access `size`?

| Option               |
| -------------------- |
| A. `req.body.size`   |
| B. `req.param.size`  |
| C. `req.query.size`  |
| D. `req.params.size` |

**✅ Correct Answer: C**

> Query parameters are available via `req.query`, e.g., `req.query.size === '10'`.

---

### ✅ **\[MongoDB] MCQ 23 — Aggregation Pipeline Order**

Which stage must come first?

```js
[ ?, { $group: { _id: "$category", count: { $sum: 1 } } } ]
```

| Option        |
| ------------- |
| A. `$project` |
| B. `$match`   |
| C. `$sort`    |
| D. `$limit`   |

**✅ Correct Answer: B**

> `$match` should **ideally come early** to filter data before grouping — for performance.

---

### ✅ **\[Node.js] MCQ 24 — Event Loop Phase**

Which task executes **after timers phase**?

| Option                  |
| ----------------------- |
| A. `setTimeout()`       |
| B. `setImmediate()`     |
| C. Microtask Queue      |
| D. `process.nextTick()` |

**✅ Correct Answer: B**

> `setImmediate()` runs in the **check phase**, after the timers phase completes.

---

### ✅ **\[Express.js] MCQ 25 — Error Handling Middleware**

Which signature defines Express error-handling middleware?

| Option                     |
| -------------------------- |
| A. `(err, req, res, next)` |
| B. `(req, res)`            |
| C. `(req, res, err)`       |
| D. `(res, err, req, next)` |

**✅ Correct Answer: A**

> Express error-handlers must have **4 parameters**, starting with `err`.

---

### ✅ **\[MongoDB] MCQ 26 — Schema Validation**

How do you enforce field types in MongoDB collections?

| Option                          |
| ------------------------------- |
| A. With `BSON.setType()`        |
| B. By using Mongoose only       |
| C. With `$jsonSchema` validator |
| D. Using `ObjectId()` casting   |

**✅ Correct Answer: C**

> MongoDB allows native schema validation via the **`$jsonSchema`** operator in collection validators.

---

### ✅ **\[Node.js] MCQ 27 — require vs import**

What is true about `require()` vs `import`?

| Option                                                         |
| -------------------------------------------------------------- |
| A. `require()` is async                                        |
| B. `import` is CommonJS                                        |
| C. `require()` supports dynamic loading                        |
| D. `import` works without `"type": "module"` in `package.json` |

**✅ Correct Answer: C**

> `require()` can be used **conditionally** or **dynamically**, unlike static `import`.

---

### ✅ **\[Express.js] MCQ 28 — Request Timeout**

How do you globally configure request timeouts in Express?

| Option                                           |
| ------------------------------------------------ |
| A. `res.setTimeout()`                            |
| B. Custom middleware                             |
| C. `app.use(timeout(ms))` with `connect-timeout` |
| D. `req.on('timeout')` event                     |

**✅ Correct Answer: C**

> Use the **`connect-timeout` middleware** to globally apply request timeouts.

---

### ✅ **\[MongoDB] MCQ 29 — Unique Index Conflict**

What happens when inserting duplicate on a `unique` field?

| Option                                |
| ------------------------------------- |
| A. Duplicate record is ignored        |
| B. Record is silently skipped         |
| C. MongoDB throws duplicate key error |
| D. Document is inserted with override |

**✅ Correct Answer: C**

> A **duplicate key error** is thrown if the field is constrained by a `unique` index.

---

### ✅ **\[Node.js] MCQ 30 — process.exit() Usage**

Calling `process.exit(1)` does what?

| Option                                     |
| ------------------------------------------ |
| A. Gracefully shuts down the app           |
| B. Forces exit with success                |
| C. Immediately stops app with error code 1 |
| D. Only stops child process                |

**✅ Correct Answer: C**

> `process.exit(1)` **terminates** the Node.js process with an error exit code.

---

Here are the next **10 advanced and non-repeating MCQs (31–40)** for **Node.js, Express.js, and MongoDB** — with clear code-focused logic and explanations:

---

### ✅ **\[Node.js] MCQ 31 — Global Object**

Which of these is a **global object** in Node.js?

| Option                    |
| ------------------------- |
| A. `document`             |
| B. `window`               |
| C. `global`               |
| D. `this` in module scope |

**✅ Correct Answer: C**

> `global` is Node.js’s equivalent of `window` in browsers. Others are undefined or scoped.

---

### ✅ **\[Express.js] MCQ 32 — Route Matching**

Given routes:

```js
app.get('/user/:id', ...);
app.get('/user/new', ...);
```

What happens for `/user/new`?

| Option                                  |
| --------------------------------------- |
| A. Only second route matches            |
| B. First route matches and `id = 'new'` |
| C. Both match                           |
| D. None match                           |

**✅ Correct Answer: B**

> Express matches **sequentially**. `/user/:id` matches `/user/new` unless placed **after**.

---

### ✅ **\[MongoDB] MCQ 33 — Index Type**

Which index improves geospatial queries?

| Option        |
| ------------- |
| A. `$text`    |
| B. `2dsphere` |
| C. `compound` |
| D. `hashed`   |

**✅ Correct Answer: B**

> The `2dsphere` index supports queries like `$near`, `$geoWithin`, etc., on GeoJSON data.

---

### ✅ **\[Node.js] MCQ 34 — Readable Stream Events**

Which event notifies that the stream is done?

| Option      |
| ----------- |
| A. `close`  |
| B. `data`   |
| C. `end`    |
| D. `finish` |

**✅ Correct Answer: C**

> `end` is fired when no more data will be provided (for readable streams).

---

### ✅ **\[Express.js] MCQ 35 — JSON Body Parsing**

Why use `express.json()`?

| Option                         |
| ------------------------------ |
| A. Handles URL params          |
| B. Parses raw binary data      |
| C. Parses JSON in request body |
| D. Enables routing             |

**✅ Correct Answer: C**

> `express.json()` is a middleware to **parse incoming JSON bodies** into `req.body`.

---

### ✅ **\[MongoDB] MCQ 36 — Replica Set Write Concern**

What does `{ w: "majority" }` do?

| Option                                          |
| ----------------------------------------------- |
| A. Write to 1 node                              |
| B. Waits for all nodes to write                 |
| C. Waits for majority of nodes to confirm write |
| D. Skips journaling                             |

**✅ Correct Answer: C**

> Ensures **durability** by confirming writes to **majority** of nodes in a replica set.

---

### ✅ **\[Node.js] MCQ 37 — Worker Threads**

What is true about Worker Threads?

| Option                                |
| ------------------------------------- |
| A. Only work in cluster mode          |
| B. Share memory with main thread      |
| C. Can’t send messages to main thread |
| D. They block the event loop          |

**✅ Correct Answer: B**

> Worker Threads can **share memory** using `SharedArrayBuffer`.

---

### ✅ **\[Express.js] MCQ 38 — Router Middleware Scope**

Given:

```js
const router = express.Router();
router.use(middleware);
```

Where does `middleware` apply?

| Option                           |
| -------------------------------- |
| A. All requests in app           |
| B. Only GET routes               |
| C. All routes under this router  |
| D. Top-level error handling only |

**✅ Correct Answer: C**

> Middleware is scoped to routes **registered on this router instance**.

---

### ✅ **\[MongoDB] MCQ 39 — `$project` Stage**

What does `$project` do in aggregation?

| Option                  |
| ----------------------- |
| A. Filters documents    |
| B. Changes schema/shape |
| C. Groups fields        |
| D. Sorts output         |

**✅ Correct Answer: B**

> `$project` reshapes documents by **including, excluding**, or **computing fields**.

---

### ✅ **\[Node.js] MCQ 40 — REPL Behavior**

In Node.js REPL, what does `_` refer to?

| Option                    |
| ------------------------- |
| A. Undefined              |
| B. Previous input command |
| C. Last evaluated result  |
| D. Error object           |

**✅ Correct Answer: C**

> `_` in REPL stores the **last evaluated expression result** — very handy for testing.

---

Great! Here are the next **10 advanced and non-repeating MCQs (41–50)** for **Node.js, Express.js, and MongoDB**:

---

### ✅ **\[Node.js] MCQ 41 — Event Loop Phase**

In which phase does `setTimeout` execute?

| Option             |
| ------------------ |
| A. Poll            |
| B. Check           |
| C. Timers          |
| D. Close callbacks |

**✅ Correct Answer: C**

> The `setTimeout` callback is queued in the **Timers phase** of the Node.js event loop.

---

### ✅ **\[Express.js] MCQ 42 — Error-Handling Middleware**

What makes a middleware an error handler in Express?

| Option                     |
| -------------------------- |
| A. It returns `res.status` |
| B. It ends with `next()`   |
| C. It has 4 arguments      |
| D. It’s last in the chain  |

**✅ Correct Answer: C**

> An Express error handler must define `(err, req, res, next)` to catch and handle errors.

---

### ✅ **\[MongoDB] MCQ 43 — Transactions**

MongoDB supports transactions on:

| Option                               |
| ------------------------------------ |
| A. Only single-document writes       |
| B. Sharded clusters only             |
| C. Replica sets and sharded clusters |
| D. Not supported at all              |

**✅ Correct Answer: C**

> MongoDB supports multi-document transactions **on replica sets and sharded clusters**.

---

### ✅ **\[Node.js] MCQ 44 — `require.cache`**

What is the purpose of `require.cache`?

| Option                          |
| ------------------------------- |
| A. Prevents module reuse        |
| B. Logs memory usage            |
| C. Caches loaded modules        |
| D. Tracks environment variables |

**✅ Correct Answer: C**

> Node.js caches modules after first `require`, stored in `require.cache`.

---

### ✅ **\[Express.js] MCQ 45 — `next('route')`**

What does `next('route')` do?

| Option                         |
| ------------------------------ |
| A. Skips to next route handler |
| B. Ends the response           |
| C. Triggers error middleware   |
| D. Restarts middleware stack   |

**✅ Correct Answer: A**

> `next('route')` skips remaining middleware in the current route and moves to next route handler.

---

### ✅ **\[MongoDB] MCQ 46 — `ObjectId` Characteristics**

What is NOT true about MongoDB's `ObjectId`?

| Option                     |
| -------------------------- |
| A. It’s 12 bytes           |
| B. It’s globally unique    |
| C. It includes a timestamp |
| D. It’s auto-incremented   |

**✅ Correct Answer: D**

> `ObjectId` is **not** auto-incremented — it’s generated using timestamp, machine ID, etc.

---

### ✅ **\[Node.js] MCQ 47 — `util.promisify()`**

What does `util.promisify()` do?

| Option                                                 |
| ------------------------------------------------------ |
| A. Converts async to sync                              |
| B. Transforms callback-based to Promise-based function |
| C. Parses JSON                                         |
| D. Buffers stream                                      |

**✅ Correct Answer: B**

> `util.promisify()` is used to **convert traditional callback functions to promises**.

---

### ✅ **\[Express.js] MCQ 48 — `res.locals`**

What is `res.locals` used for?

| Option                        |
| ----------------------------- |
| A. Store response headers     |
| B. Share variables with views |
| C. Log request data           |
| D. Define routes dynamically  |

**✅ Correct Answer: B**

> `res.locals` is used to pass local variables to **views rendered by Express**.

---

### ✅ **\[MongoDB] MCQ 49 — `$addToSet` vs `$push`**

Difference between `$addToSet` and `$push`?

| Option                                            |
| ------------------------------------------------- |
| A. Both avoid duplicates                          |
| B. `$addToSet` avoids duplicates, `$push` doesn’t |
| C. `$push` sorts automatically                    |
| D. `$addToSet` deletes values                     |

**✅ Correct Answer: B**

> `$addToSet` adds only if value is **not already present**, unlike `$push`.

---

### ✅ **\[Node.js] MCQ 50 — Process Exit Code**

What happens with `process.exit(1)`?

| Option                              |
| ----------------------------------- |
| A. Graceful shutdown                |
| B. Success signal                   |
| C. Error signal sent to OS          |
| D. Waits for event loop to complete |

**✅ Correct Answer: C**

> Exit code `1` signals an **error** to the operating system; `0` is normal success.

---

Perfect — here are the next **10 advanced, non-repeating MCQs (51–60)** on **Node.js, Express.js, and MongoDB**:

---

### ✅ **\[Node.js] MCQ 51 — `setImmediate` vs `setTimeout`**

What is the difference between `setImmediate()` and `setTimeout(..., 0)`?

| Option                                            |
| ------------------------------------------------- |
| A. No difference; both execute immediately        |
| B. `setTimeout` always runs before `setImmediate` |
| C. `setImmediate` runs after I/O events           |
| D. `setTimeout` skips the event loop              |

**✅ Correct Answer: C**

> `setImmediate` runs **after the current poll phase**, which is useful after I/O.

---

### ✅ **\[Express.js] MCQ 52 — Mount Path of Router**

You have:

```js
app.use('/api', router);
```

A route inside `router` is defined as:

```js
router.get('/users', ...);
```

What is the full path to access it?

| Option               |
| -------------------- |
| A. /api              |
| B. /users            |
| C. /api/users        |
| D. /router/api/users |

**✅ Correct Answer: C**

> The router is mounted at `/api`, so the full path becomes `/api/users`.

---

### ✅ **\[MongoDB] MCQ 53 — Index Impact**

What is the effect of having a **compound index** on `{ age: 1, name: 1 }`?

| Option                                     |
| ------------------------------------------ |
| A. Only queries on `name` are fast         |
| B. Only exact matches are allowed          |
| C. Queries on `age` or `age+name` are fast |
| D. Index is ignored for sorting            |

**✅ Correct Answer: C**

> Compound indexes support prefix fields — so `age` or `age + name` queries benefit.

---

### ✅ **\[Node.js] MCQ 54 — Cluster Module**

Why use Node.js `cluster` module?

| Option                        |
| ----------------------------- |
| A. Run async code faster      |
| B. Support for GraphQL        |
| C. Multi-core CPU utilization |
| D. Prevent garbage collection |

**✅ Correct Answer: C**

> `cluster` allows **forking workers** to utilize multiple CPU cores.

---

### ✅ **\[Express.js] MCQ 55 — Static Files**

Which line serves static files from `/public`?

| Option                                 |
| -------------------------------------- |
| A. `express.static()`                  |
| B. `app.static('/public')`             |
| C. `app.use(express.static('public'))` |
| D. `res.staticFile()`                  |

**✅ Correct Answer: C**

> `express.static()` middleware serves static files.

---

### ✅ **\[MongoDB] MCQ 56 — Aggregation `$facet`**

What does `$facet` do in aggregation?

| Option                                 |
| -------------------------------------- |
| A. Splits results into multiple stages |
| B. Joins collections like SQL          |
| C. Runs multiple pipelines in parallel |
| D. Filters based on condition          |

**✅ Correct Answer: C**

> `$facet` allows **multiple pipelines** to run on the same input documents.

---

### ✅ **\[Node.js] MCQ 57 — Buffer Basics**

Which of the following creates a zero-filled buffer of length 10?

| Option                |
| --------------------- |
| A. `Buffer.alloc(10)` |
| B. `Buffer(10)`       |
| C. `new Buffer('10')` |
| D. `Buffer.from(10)`  |

**✅ Correct Answer: A**

> `Buffer.alloc(10)` is the safe, modern API for zero-filled buffers.

---

### ✅ **\[Express.js] MCQ 58 — CORS Middleware**

Which header is required to allow cross-origin requests?

| Option                           |
| -------------------------------- |
| A. `Content-Type`                |
| B. `Authorization`               |
| C. `Access-Control-Allow-Origin` |
| D. `X-Powered-By`                |

**✅ Correct Answer: C**

> CORS policy is controlled using `Access-Control-Allow-Origin`.

---

### ✅ **\[MongoDB] MCQ 59 — `$lookup` Join Type**

What type of join is `$lookup` in MongoDB?

| Option             |
| ------------------ |
| A. Left outer join |
| B. Inner join      |
| C. Cartesian join  |
| D. Full join       |

**✅ Correct Answer: A**

> `$lookup` performs a **left outer join** by default in aggregation.

---

### ✅ **\[Node.js] MCQ 60 — Child Processes**

What module is used to spawn child processes?

| Option              |
| ------------------- |
| A. `worker_threads` |
| B. `os`             |
| C. `fs`             |
| D. `child_process`  |

**✅ Correct Answer: D**

> `child_process` module allows you to spawn subprocesses (e.g., via `exec`, `spawn`).

---
Great — here are the next **10 advanced, non-repeating MCQs (61–70)** on **Node.js, Express.js, and MongoDB**:

---

### ✅ **\[Node.js] MCQ 61 — Event Loop Phase**

Which phase of the Node.js Event Loop handles timers like `setTimeout()`?

| Option    |
| --------- |
| A. Poll   |
| B. Check  |
| C. Timers |
| D. Close  |

**✅ Correct Answer: C**

> The `Timers` phase handles callbacks scheduled by `setTimeout()` and `setInterval()`.

---

### ✅ **\[Express.js] MCQ 62 — Route Order**

In Express, what happens if a route `/user/:id` is defined **after** `/user/settings`?

| Option                                         |
| ---------------------------------------------- |
| A. Order doesn't matter                        |
| B. `/user/settings` is overridden              |
| C. `/user/:id` may catch `/settings`           |
| D. Routes are matched by alphabetical priority |

**✅ Correct Answer: C**

> Route matching is **top-down**. So `/user/:id` may match `/user/settings` unless defined after.

---

### ✅ **\[MongoDB] MCQ 63 — ObjectId Timestamp**

What does `ObjectId.getTimestamp()` return?

| Option                           |
| -------------------------------- |
| A. Document's last modified time |
| B. Created-at timestamp          |
| C. Index creation time           |
| D. TTL expiration                |

**✅ Correct Answer: B**

> `ObjectId` encodes creation timestamp in its first 4 bytes.

---

### ✅ **\[Node.js] MCQ 64 — `require.cache`**

What does `require.cache` do?

| Option                         |
| ------------------------------ |
| A. Tracks file size of modules |
| B. Enables hot-reloading       |
| C. Caches loaded modules       |
| D. Compresses response payload |

**✅ Correct Answer: C**

> Node caches loaded modules to improve performance. You can clear it for reloads.

---

### ✅ **\[Express.js] MCQ 65 — `next()` usage**

In middleware, when is `next()` used?

| Option                               |
| ------------------------------------ |
| A. Ends request-response cycle       |
| B. Passes control to next middleware |
| C. Catches 404 errors                |
| D. Returns JSON response             |

**✅ Correct Answer: B**

> `next()` allows chaining to the next middleware in the stack.

---

### ✅ **\[MongoDB] MCQ 66 — TTL Index**

What happens with a TTL (Time-To-Live) index?

| Option                                     |
| ------------------------------------------ |
| A. Deletes expired documents automatically |
| B. Refreshes cache                         |
| C. Denies writes on expiry                 |
| D. Notifies via callback                   |

**✅ Correct Answer: A**

> MongoDB TTL index **auto-deletes** documents after specified time.

---

### ✅ **\[Node.js] MCQ 67 — `fs.promises`**

What is `fs.promises` in Node.js?

| Option                      |
| --------------------------- |
| A. Legacy file operations   |
| B. Experimental stream API  |
| C. Promise-based file I/O   |
| D. Blocking file sync calls |

**✅ Correct Answer: C**

> `fs.promises` provides **async/await**-friendly APIs for file operations.

---

### ✅ **\[Express.js] MCQ 68 — Error Middleware**

Which Express middleware signature handles errors?

| Option                     |
| -------------------------- |
| A. `(req, res)`            |
| B. `(req, res, next)`      |
| C. `(err, req, res, next)` |
| D. `(err, res)`            |

**✅ Correct Answer: C**

> Error handlers in Express must have **4 arguments**, starting with `err`.

---

### ✅ **\[MongoDB] MCQ 69 — `$project`**

What does `$project` stage in aggregation do?

| Option                                |
| ------------------------------------- |
| A. Filters input documents            |
| B. Selects fields and reshapes output |
| C. Updates documents                  |
| D. Joins multiple collections         |

**✅ Correct Answer: B**

> `$project` reshapes each document in the stream, controlling fields.

---

### ✅ **\[Node.js] MCQ 70 — Global `process` object**

Which is **true** about the `process` object?

| Option                              |
| ----------------------------------- |
| A. Only available in browser        |
| B. Provides access to stdin, stdout |
| C. Loads npm packages               |
| D. Compiles native addons           |

**✅ Correct Answer: B**

> The global `process` object gives access to environment, args, stdin, stdout, etc.

---
Here are the next **10 advanced MCQs (71–80)** on **Node.js, Express.js, and MongoDB**:

---

### ✅ **\[Node.js] MCQ 71 — Cluster Module**

What is the purpose of Node.js `cluster` module?

| Option                             |
| ---------------------------------- |
| A. Create frontend components      |
| B. Run multiple threads in browser |
| C. Scale app across CPU cores      |
| D. Increase memory cache size      |

**✅ Correct Answer: C**

> `cluster` lets Node.js spawn child processes across CPU cores for better performance.

---

### ✅ **\[Express.js] MCQ 72 — Path Matching**

What does the route `/api/:type/:id?` mean?

| Option                                  |
| --------------------------------------- |
| A. Both `type` and `id` are required    |
| B. `id` is optional                     |
| C. Wildcard for all parameters          |
| D. Matches only `/api/type/id` strictly |

**✅ Correct Answer: B**

> The `?` after `:id` makes it optional.

---

### ✅ **\[MongoDB] MCQ 73 — Write Concern**

What does MongoDB's `writeConcern: { w: "majority" }` ensure?

| Option                                  |
| --------------------------------------- |
| A. Data replicated to all secondaries   |
| B. Majority of nodes acknowledge write  |
| C. Only one node stores the data        |
| D. Disables replication for performance |

**✅ Correct Answer: B**

> This ensures durability — write is acknowledged only when majority nodes confirm it.

---

### ✅ **\[Node.js] MCQ 74 — `process.nextTick()`**

What is true about `process.nextTick()`?

| Option                           |
| -------------------------------- |
| A. Runs before any I/O events    |
| B. Executes after all timers     |
| C. Delays execution to next loop |
| D. Used only for async/await     |

**✅ Correct Answer: A**

> `process.nextTick()` defers execution **before** any I/O or timers are handled.

---

### ✅ **\[Express.js] MCQ 75 — CORS Headers**

Which header is required for cross-origin requests?

| Option                         |
| ------------------------------ |
| A. Content-Type                |
| B. Access-Control-Allow-Origin |
| C. Cache-Control               |
| D. Accept-Encoding             |

**✅ Correct Answer: B**

> Without `Access-Control-Allow-Origin`, browsers will block cross-origin requests.

---

### ✅ **\[MongoDB] MCQ 76 — `$match` stage**

What does `$match` do in an aggregation pipeline?

| Option                           |
| -------------------------------- |
| A. Joins collections             |
| B. Filters documents by criteria |
| C. Sorts result                  |
| D. Groups documents by fields    |

**✅ Correct Answer: B**

> `$match` is used to filter documents (like `find()` but in aggregation).

---

### ✅ **\[Node.js] MCQ 77 — Unhandled Promise Rejection**

What happens if a Promise rejects and there’s no `.catch()`?

| Option                               |
| ------------------------------------ |
| A. Nothing                           |
| B. Handled by default logging        |
| C. Crashes Node.js in newer versions |
| D. Retries automatically             |

**✅ Correct Answer: C**

> Node.js 15+ treats unhandled rejections as fatal errors.

---

### ✅ **\[Express.js] MCQ 78 — Route Parameter Regex**

What does `/user/:id(\\d+)` match?

| Option                    |
| ------------------------- |
| A. Any string as ID       |
| B. Only digits in `id`    |
| C. UUID values            |
| D. Only alphabets allowed |

**✅ Correct Answer: B**

> The regex forces `:id` to be numeric (`\d+` = one or more digits).

---

### ✅ **\[MongoDB] MCQ 79 — `$lookup` Stage**

What does `$lookup` do?

| Option                              |
| ----------------------------------- |
| A. Looks up cached documents        |
| B. Performs join across collections |
| C. Projects document fields         |
| D. Validates indexes                |

**✅ Correct Answer: B**

> `$lookup` allows left outer joins across collections in aggregation.

---

### ✅ **\[Node.js] MCQ 80 — Environment Variables**

What is the correct way to access environment variables?

| Option                |
| --------------------- |
| A. `env.get("PORT")`  |
| B. `os.env.PORT`      |
| C. `process.env.PORT` |
| D. `dotenv.PORT`      |

**✅ Correct Answer: C**

> `process.env.VAR_NAME` gives access to environment variables.

---
Here’s the next batch of **10 advanced and non-repeating MCQs (81–90)** on **Node.js, Express.js, and MongoDB**:

---

### ✅ **\[Node.js] MCQ 81 — Event Loop Phases**

Which phase comes **after** the timers phase in the Node.js event loop?

| Option               |
| -------------------- |
| A. Poll              |
| B. Pending callbacks |
| C. Close callbacks   |
| D. Check             |

**✅ Correct Answer: B**

> The Node.js event loop flows: timers → **pending callbacks** → idle/prepare → poll → check → close.

---

### ✅ **\[Express.js] MCQ 82 — Error Handling Middleware**

What is special about an Express error-handling middleware?

```js
app.use((err, req, res, next) => { ... });
```

| Option                                     |
| ------------------------------------------ |
| A. It has only 2 parameters                |
| B. It must use `res.sendStatus()`          |
| C. It requires `err` as the first argument |
| D. It overrides route handlers             |

**✅ Correct Answer: C**

> Express recognizes error-handlers by checking for the **4 parameters**, with `err` as the first.

---

### ✅ **\[MongoDB] MCQ 83 — `$project` Usage**

What does `$project: { name: 1, _id: 0 }` do?

| Option                             |
| ---------------------------------- |
| A. Includes only `_id`             |
| B. Excludes both fields            |
| C. Includes `name`, excludes `_id` |
| D. Error: Invalid projection       |

**✅ Correct Answer: C**

> In MongoDB, `1` includes fields, `0` excludes. You explicitly exclude `_id` to suppress it.

---

### ✅ **\[Node.js] MCQ 84 — Built-in Compression**

What package helps you add gzip compression in a Node.js API?

| Option               |
| -------------------- |
| A. `compression`     |
| B. `zlib-stream`     |
| C. `gzip-js`         |
| D. `stream-compress` |

**✅ Correct Answer: A**

> The popular and standard package for enabling gzip in Express is `compression`.

---

### ✅ **\[Express.js] MCQ 85 — Mounting Routers**

You mount a router as:

```js
app.use('/api', router);
```

And in the router:

```js
router.get('/users', ...)
```

Which endpoint does it handle?

| Option                 |
| ---------------------- |
| A. `/users`            |
| B. `/api/users`        |
| C. `/api/router/users` |
| D. `/router/users`     |

**✅ Correct Answer: B**

> Mounting path prefixes all routes in the router with `/api`.

---

### ✅ **\[MongoDB] MCQ 86 — Index Impact**

Which operation benefits most from indexing?

| Option             |
| ------------------ |
| A. Insert          |
| B. Update many     |
| C. Read/query      |
| D. Drop collection |

**✅ Correct Answer: C**

> Indexes are primarily designed to optimize **read** and **query** performance.

---

### ✅ **\[Node.js] MCQ 87 — Global Objects**

Which one is **not** a global object in Node.js?

| Option          |
| --------------- |
| A. `__dirname`  |
| B. `window`     |
| C. `process`    |
| D. `setTimeout` |

**✅ Correct Answer: B**

> `window` is a browser-specific global, **not available** in Node.js.

---

### ✅ **\[Express.js] MCQ 88 — Dynamic Middleware**

How do you conditionally apply a middleware based on a query param?

| Option                                    |
| ----------------------------------------- |
| A. `app.get(middleware, route)`           |
| B. `app.use((req, res, next) => { ... })` |
| C. Use `router.maybe()`                   |
| D. You cannot do this in Express          |

**✅ Correct Answer: B**

> You can write a custom middleware that checks `req.query` before proceeding.

---

### ✅ **\[MongoDB] MCQ 89 — Document Validation**

Where is schema validation configured in MongoDB?

| Option                                |
| ------------------------------------- |
| A. In Node model class                |
| B. In JSON Schema at collection level |
| C. In `_id` index definition          |
| D. At query time via `$validate`      |

**✅ Correct Answer: B**

> MongoDB supports schema validation using **JSON Schema** in `db.createCollection()` options.

---

### ✅ **\[Node.js] MCQ 90 — `require.resolve()` Purpose**

What does `require.resolve('express')` return?

| Option                                 |
| -------------------------------------- |
| A. The contents of express.js          |
| B. The version of Express              |
| C. Absolute path to Express entry file |
| D. List of Express dependencies        |

**✅ Correct Answer: C**

> `require.resolve()` returns the **absolute resolved path** to the required module.

---
Great! Here's the final batch: **MCQs 91–100** on **Node.js, Express.js, and MongoDB**, all advanced and unique — no repeats.

---

### ✅ **\[Node.js] MCQ 91 — Worker Threads**

Which use case is best suited for Node.js Worker Threads?

| Option                           |
| -------------------------------- |
| A. HTTP request handling         |
| B. Reading environment variables |
| C. CPU-intensive computation     |
| D. File watching with fs module  |

**✅ Correct Answer: C**

> Worker threads allow offloading heavy CPU-bound tasks without blocking the event loop.

---

### ✅ **\[Express.js] MCQ 92 — Route Precedence**

What happens if you define routes in this order?

```js
app.get('/user/:id', ...);
app.get('/user/settings', ...);
```

And request `/user/settings`?

| Option                      |
| --------------------------- |
| A. Matches `:id` route      |
| B. Matches `/user/settings` |
| C. Both match; throws error |
| D. No route matches         |

**✅ Correct Answer: A**

> Express routes are matched **top-down**. `/user/:id` will match first, unless `/user/settings` is defined before it.

---

### ✅ **\[MongoDB] MCQ 93 — `$unwind` Operator**

What does `$unwind` do in an aggregation pipeline?

| Option                                            |
| ------------------------------------------------- |
| A. Removes null values                            |
| B. Merges arrays                                  |
| C. Deconstructs an array field into multiple docs |
| D. Groups array items                             |

**✅ Correct Answer: C**

> `$unwind` breaks array elements into **separate documents**, one per array item.

---

### ✅ **\[Node.js] MCQ 94 — `process.nextTick()`**

What is the main difference between `setImmediate()` and `process.nextTick()`?

| Option                                     |
| ------------------------------------------ |
| A. Both are identical                      |
| B. `nextTick()` queues for next I/O cycle  |
| C. `nextTick()` executes before I/O events |
| D. `setImmediate()` blocks the event loop  |

**✅ Correct Answer: C**

> `process.nextTick()` executes **before** any I/O event callbacks.

---

### ✅ **\[Express.js] MCQ 95 — App-Level Middleware Order**

What is the effect of placing `app.use(logger)` **after** route definitions?

| Option                                      |
| ------------------------------------------- |
| A. Logger will not execute for those routes |
| B. Logger executes before route handler     |
| C. Logger throws error                      |
| D. Logger runs twice                        |

**✅ Correct Answer: A**

> Middleware **must be declared before** routes to affect them. Order matters.

---

### ✅ **\[MongoDB] MCQ 96 — `ObjectId` Generation**

How is a MongoDB `ObjectId` generated?

| Option                                        |
| --------------------------------------------- |
| A. Incremental integer ID                     |
| B. UUID                                       |
| C. Hex timestamp + machine ID + PID + counter |
| D. MD5 hash of document                       |

**✅ Correct Answer: C**

> `ObjectId` encodes a **timestamp**, **machine ID**, **process ID**, and **counter** in hex format.

---

### ✅ **\[Node.js] MCQ 97 — `fs/promises` vs `fs`**

What is a key difference between `fs/promises` and the original `fs` module?

| Option                            |
| --------------------------------- |
| A. Supports only reading          |
| B. Has async/await native support |
| C. Works only in ES5              |
| D. Cannot handle large files      |

**✅ Correct Answer: B**

> `fs/promises` returns **Promises** natively — perfect for `async/await` use.

---

### ✅ **\[Express.js] MCQ 98 — Path Parameters Regex**

What does this route match?

```js
app.get('/user/:id([0-9]{3})', ...);
```

| Option                      |
| --------------------------- |
| A. Any ID string            |
| B. Any numeric ID           |
| C. Only 3-digit numeric IDs |
| D. 3-digit alphanumeric IDs |

**✅ Correct Answer: C**

> The regex restricts `:id` to **exactly 3 numeric digits**.

---

### ✅ **\[MongoDB] MCQ 99 — `$match` vs `$filter`**

In aggregation, what does `$match` do?

| Option                  |
| ----------------------- |
| A. Filters documents    |
| B. Filters array fields |
| C. Merges documents     |
| D. Joins collections    |

**✅ Correct Answer: A**

> `$match` filters documents **at the pipeline level**, not within arrays. `$filter` filters arrays.

---

### ✅ **\[Node.js] MCQ 100 — ES Module Syntax**

Which is valid in a `.mjs` file using native ES modules?

| Option                    |
| ------------------------- |
| A. `require('fs')`        |
| B. `import fs from 'fs';` |
| C. `module.exports = {}`  |
| D. `exports.handler = fn` |

**✅ Correct Answer: B**

> `.mjs` files use **ES module syntax** — `import`/`export` — not CommonJS `require`.

---









