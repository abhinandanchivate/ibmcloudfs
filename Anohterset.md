Great — I’ll now begin generating another **100 completely new, non-repeating, expert-level MCQs** across these 6 topics:

* **Java**
* **Spring Boot**
* **Angular**
* **React**
* **Docker**
* **Kubernetes**

🧠 Each question will include:

* Real-world code or config (where needed)
* 4 unique answer options
* The correct answer clearly marked
* A short but strong explanation

---

Let's start with **MCQs 1–10** (2 per topic):

---

### ✅ **\[Java] MCQ 1 — ThreadLocal Use Case**

Why would you use `ThreadLocal` in a multi-threaded application?

| Option                                   | Explanation |
| ---------------------------------------- | ----------- |
| A. To share state between threads        |             |
| B. To store thread-specific data         |             |
| C. To enable garbage collection of tasks |             |
| D. To sync shared resources              |             |

**✅ Correct Answer: B**

> `ThreadLocal` stores data unique to each thread — ideal for things like DB connections in thread pools.

---

### ✅ **\[Java] MCQ 2 — Sealed Classes**

Java 17+ introduces sealed classes. What do they enforce?

```java
public sealed class Animal permits Dog, Cat {}
```

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. Class can’t be extended           |             |
| B. Only permitted classes can extend |             |
| C. Must be abstract                  |             |
| D. Has to be public                  |             |

**✅ Correct Answer: B**

> Sealed classes allow a fixed set of known subclasses to extend them, ensuring control over hierarchy.

---

### ✅ **\[Spring Boot] MCQ 3 — Lazy Initialization**

What does `spring.main.lazy-initialization=true` do?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. Loads all beans on startup     |             |
| B. Initializes beans on first use |             |
| C. Disables auto-configuration    |             |
| D. Breaks dependency injection    |             |

**✅ Correct Answer: B**

> Lazy initialization improves startup time by creating beans only when they’re needed.

---

### ✅ **\[Spring Boot] MCQ 4 — Profile-specific YAML**

What happens with these files?

* `application.yml`
* `application-dev.yml`

Active profile: `dev`

| Option                                | Explanation |
| ------------------------------------- | ----------- |
| A. Only `application.yml` is loaded   |             |
| B. Only `application-dev.yml` is used |             |
| C. Both are merged                    |             |
| D. `application.yml` overrides `dev`  |             |

**✅ Correct Answer: C**

> Spring Boot merges base YAML with profile-specific YAML, profile values take precedence.

---

### ✅ **\[Angular] MCQ 5 — ViewChild Timing**

```ts
@ViewChild('el') el: ElementRef;
ngAfterViewInit() { console.log(this.el); }
```

Why is `ngAfterViewInit` used here?

| Option                                  | Explanation |
| --------------------------------------- | ----------- |
| A. Template not compiled in `ngOnInit`  |             |
| B. `ViewChild` only available post-view |             |
| C. Component not instantiated earlier   |             |
| D. ElementRef only works in services    |             |

**✅ Correct Answer: B**

> `ViewChild` is resolved after the view has been initialized — use `ngAfterViewInit`.

---

### ✅ **\[Angular] MCQ 6 — Structural Directive**

Which of the following creates a **custom structural directive**?

| Option                                 | Explanation |
| -------------------------------------- | ----------- |
| A. `*myDirective` in HTML              |             |
| B. `@Directive({ selector: '[dir]' })` |             |
| C. Extending `Renderer2`               |             |
| D. Using `ViewEncapsulation.None`      |             |

**✅ Correct Answer: B**

> Structural directives use attribute selector syntax like `[myDirective]` and manipulate DOM structure.

---

### ✅ **\[React] MCQ 7 — Key Prop Use**

Why should each item in a React list have a unique `key`?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. Prevent re-renders             |             |
| B. Optimize list diffing          |             |
| C. Improve styling performance    |             |
| D. Prevent useEffect from running |             |

**✅ Correct Answer: B**

> The `key` prop helps React efficiently update and reorder elements during reconciliation.

---

### ✅ **\[React] MCQ 8 — Controlled vs Uncontrolled**

Which is **true** for controlled components?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. DOM owns the state               |             |
| B. React handles the input value    |             |
| C. Values are saved in localStorage |             |
| D. Uses useRef() to read values     |             |

**✅ Correct Answer: B**

> Controlled components bind input value to React state, syncing on every change.

---

### ✅ **\[Docker] MCQ 9 — ENTRYPOINT vs CMD**

What is the main difference?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. CMD overrides ENTRYPOINT       |             |
| B. ENTRYPOINT overrides CMD       |             |
| C. CMD is mandatory               |             |
| D. ENTRYPOINT ignores shell input |             |

**✅ Correct Answer: B**

> If both are defined, CMD provides args to ENTRYPOINT — ENTRYPOINT takes precedence in execution.

---

### ✅ **\[Kubernetes] MCQ 10 — StatefulSet Behavior**

How are StatefulSet pods named?

| Option                       | Explanation |
| ---------------------------- | ----------- |
| A. Randomly                  |             |
| B. Manually set              |             |
| C. `<name>-<ordinal>` format |             |
| D. Based on IP address       |             |

**✅ Correct Answer: C**

> StatefulSets name pods predictably: e.g., `web-0`, `web-1`, maintaining ordering and identity.

---

Perfect — here are the next **MCQs 11–20**, continuing with real, high-difficulty, non-repeating questions:

---

### ✅ **\[Java] MCQ 11 — Record and Inheritance (Java 16+)**

```java
public record Person(String name, int age) {}
```

What happens if you try to extend `Person`?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. Compilation succeeds             |             |
| B. You must override `toString()`   |             |
| C. Records can't be extended        |             |
| D. Record must be marked `abstract` |             |

**✅ Correct Answer: C**

> Java `record` types are implicitly `final`, so they cannot be extended.

---

### ✅ **\[Java] MCQ 12 — CompletableFuture vs Future**

Which benefit does `CompletableFuture` offer over `Future`?

| Option                                   | Explanation |
| ---------------------------------------- | ----------- |
| A. Blocking retrieval                    |             |
| B. Support for chaining async operations |             |
| C. Synchronous execution only            |             |
| D. Needs external executor always        |             |

**✅ Correct Answer: B**

> `CompletableFuture` supports fluent, non-blocking async pipelines (`thenApply`, `thenCombine`, etc.).

---

### ✅ **\[Spring Boot] MCQ 13 — `@ConfigurationProperties`**

```java
@ConfigurationProperties(prefix = "app")
public class AppConfig {
    private String name;
}
```

How do you enable it?

| Option                                      | Explanation |
| ------------------------------------------- | ----------- |
| A. Use `@Component` on AppConfig            |             |
| B. Annotate main class with `@EnableConfig` |             |
| C. Use `@EnableConfigurationProperties`     |             |
| D. Add it in `application.properties`       |             |

**✅ Correct Answer: C**

> You must annotate a config class or Spring Boot app with `@EnableConfigurationProperties` to bind properties.

---

### ✅ **\[Spring Boot] MCQ 14 — Actuator Exposure**

Which file is used to expose actuator endpoints securely?

| Option                      | Explanation |
| --------------------------- | ----------- |
| A. `pom.xml`                |             |
| B. `logback.xml`            |             |
| C. `application.yml`        |             |
| D. `application.properties` |             |

**✅ Correct Answer: D**

> Use `management.endpoints.web.exposure.include=*` in `application.properties` to expose actuator endpoints.

---

### ✅ **\[Angular] MCQ 15 — Reactive Forms Validator**

```ts
myForm = new FormGroup({
  username: new FormControl('', [Validators.required])
});
```

How to get validation error?

| Option                             | Explanation |
| ---------------------------------- | ----------- |
| A. `myForm.errors.username`        |             |
| B. `myForm.get('username').valid`  |             |
| C. `myForm.get('username').errors` |             |
| D. `myForm.hasError('username')`   |             |

**✅ Correct Answer: C**

> `FormControl.errors` returns error map for that control.

---

### ✅ **\[Angular] MCQ 16 — Zone.js and Async**

Why is Angular able to detect `setTimeout` changes in UI?

| Option                        | Explanation |
| ----------------------------- | ----------- |
| A. Uses RxJS hooks            |             |
| B. All async APIs are patched |             |
| C. NgModules are reactive     |             |
| D. setTimeout is not tracked  |             |

**✅ Correct Answer: B**

> `Zone.js` patches browser async APIs like `setTimeout`, so Angular knows when to trigger change detection.

---

### ✅ **\[React] MCQ 17 — Virtual DOM Concept**

What is the primary reason React uses a virtual DOM?

| Option                                            | Explanation |
| ------------------------------------------------- | ----------- |
| A. To prevent XSS                                 |             |
| B. To speed up initial load                       |             |
| C. To batch state updates visually                |             |
| D. To reduce direct DOM manipulations efficiently |             |

**✅ Correct Answer: D**

> Virtual DOM diffing minimizes real DOM mutations, improving performance.

---

### ✅ **\[React] MCQ 18 — useRef for DOM Access**

Why use `useRef()` for DOM access?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. To trigger rerender on change |             |
| B. To get a mutable reference    |             |
| C. To store persistent props     |             |
| D. To call setState safely       |             |

**✅ Correct Answer: B**

> `useRef` gives a mutable `.current` object that doesn’t cause re-renders — ideal for DOM or timers.

---

### ✅ **\[Docker] MCQ 19 — COPY vs ADD**

Which is true about `ADD`?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. Same as `COPY` but slower      |             |
| B. Can extract local tar archives |             |
| C. Used only for binaries         |             |
| D. Automatically sets permissions |             |

**✅ Correct Answer: B**

> `ADD` can do everything `COPY` does **plus** unpack local tar files and access remote URLs (though `COPY` is preferred for clarity).

---

### ✅ **\[Kubernetes] MCQ 20 — ConfigMap Usage**

How can a ConfigMap be mounted to a container?

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. As an environment variable only   |             |
| B. As a volume mount or env variable |             |
| C. Only during initContainer         |             |
| D. Only using secrets                |             |

**✅ Correct Answer: B**

> ConfigMaps can be exposed either as env vars or mounted as volume files inside pods.

---
Perfect — here are the next **MCQs 11–20**, continuing with real, high-difficulty, non-repeating questions:

---

### ✅ **\[Java] MCQ 11 — Record and Inheritance (Java 16+)**

```java
public record Person(String name, int age) {}
```

What happens if you try to extend `Person`?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. Compilation succeeds             |             |
| B. You must override `toString()`   |             |
| C. Records can't be extended        |             |
| D. Record must be marked `abstract` |             |

**✅ Correct Answer: C**

> Java `record` types are implicitly `final`, so they cannot be extended.

---

### ✅ **\[Java] MCQ 12 — CompletableFuture vs Future**

Which benefit does `CompletableFuture` offer over `Future`?

| Option                                   | Explanation |
| ---------------------------------------- | ----------- |
| A. Blocking retrieval                    |             |
| B. Support for chaining async operations |             |
| C. Synchronous execution only            |             |
| D. Needs external executor always        |             |

**✅ Correct Answer: B**

> `CompletableFuture` supports fluent, non-blocking async pipelines (`thenApply`, `thenCombine`, etc.).

---

### ✅ **\[Spring Boot] MCQ 13 — `@ConfigurationProperties`**

```java
@ConfigurationProperties(prefix = "app")
public class AppConfig {
    private String name;
}
```

How do you enable it?

| Option                                      | Explanation |
| ------------------------------------------- | ----------- |
| A. Use `@Component` on AppConfig            |             |
| B. Annotate main class with `@EnableConfig` |             |
| C. Use `@EnableConfigurationProperties`     |             |
| D. Add it in `application.properties`       |             |

**✅ Correct Answer: C**

> You must annotate a config class or Spring Boot app with `@EnableConfigurationProperties` to bind properties.

---

### ✅ **\[Spring Boot] MCQ 14 — Actuator Exposure**

Which file is used to expose actuator endpoints securely?

| Option                      | Explanation |
| --------------------------- | ----------- |
| A. `pom.xml`                |             |
| B. `logback.xml`            |             |
| C. `application.yml`        |             |
| D. `application.properties` |             |

**✅ Correct Answer: D**

> Use `management.endpoints.web.exposure.include=*` in `application.properties` to expose actuator endpoints.

---

### ✅ **\[Angular] MCQ 15 — Reactive Forms Validator**

```ts
myForm = new FormGroup({
  username: new FormControl('', [Validators.required])
});
```

How to get validation error?

| Option                             | Explanation |
| ---------------------------------- | ----------- |
| A. `myForm.errors.username`        |             |
| B. `myForm.get('username').valid`  |             |
| C. `myForm.get('username').errors` |             |
| D. `myForm.hasError('username')`   |             |

**✅ Correct Answer: C**

> `FormControl.errors` returns error map for that control.

---

### ✅ **\[Angular] MCQ 16 — Zone.js and Async**

Why is Angular able to detect `setTimeout` changes in UI?

| Option                        | Explanation |
| ----------------------------- | ----------- |
| A. Uses RxJS hooks            |             |
| B. All async APIs are patched |             |
| C. NgModules are reactive     |             |
| D. setTimeout is not tracked  |             |

**✅ Correct Answer: B**

> `Zone.js` patches browser async APIs like `setTimeout`, so Angular knows when to trigger change detection.

---

### ✅ **\[React] MCQ 17 — Virtual DOM Concept**

What is the primary reason React uses a virtual DOM?

| Option                                            | Explanation |
| ------------------------------------------------- | ----------- |
| A. To prevent XSS                                 |             |
| B. To speed up initial load                       |             |
| C. To batch state updates visually                |             |
| D. To reduce direct DOM manipulations efficiently |             |

**✅ Correct Answer: D**

> Virtual DOM diffing minimizes real DOM mutations, improving performance.

---

### ✅ **\[React] MCQ 18 — useRef for DOM Access**

Why use `useRef()` for DOM access?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. To trigger rerender on change |             |
| B. To get a mutable reference    |             |
| C. To store persistent props     |             |
| D. To call setState safely       |             |

**✅ Correct Answer: B**

> `useRef` gives a mutable `.current` object that doesn’t cause re-renders — ideal for DOM or timers.

---

### ✅ **\[Docker] MCQ 19 — COPY vs ADD**

Which is true about `ADD`?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. Same as `COPY` but slower      |             |
| B. Can extract local tar archives |             |
| C. Used only for binaries         |             |
| D. Automatically sets permissions |             |

**✅ Correct Answer: B**

> `ADD` can do everything `COPY` does **plus** unpack local tar files and access remote URLs (though `COPY` is preferred for clarity).

---

### ✅ **\[Kubernetes] MCQ 20 — ConfigMap Usage**

How can a ConfigMap be mounted to a container?

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. As an environment variable only   |             |
| B. As a volume mount or env variable |             |
| C. Only during initContainer         |             |
| D. Only using secrets                |             |

**✅ Correct Answer: B**

> ConfigMaps can be exposed either as env vars or mounted as volume files inside pods.

---

Great! Here's the next batch — **MCQs 21–30**, continuing the same format, without any repetition:

---

### ✅ **\[Java] MCQ 21 — Enum Behavior**

```java
enum Status {
    STARTED, PAUSED, STOPPED;
}
```

What is the result of `Status.valueOf("RUNNING")`?

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. Returns `null`                    |             |
| B. Returns `Status.STOPPED`          |             |
| C. Throws `IllegalArgumentException` |             |
| D. Compiles but fails at runtime     |             |

**✅ Correct Answer: C**

> `valueOf("RUNNING")` fails if the enum constant doesn't exist — throws `IllegalArgumentException`.

---

### ✅ **\[Java] MCQ 22 — Functional Interface Conflict**

```java
interface A {
    default void run() {}
}
interface B {
    default void run() {}
}
class MyClass implements A, B {
    public void run() { System.out.println("Hello"); }
}
```

What is the result?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. Ambiguity error                  |             |
| B. Needs override for `run()`       |             |
| C. Compiles and prints `Hello`      |             |
| D. Default method resolves conflict |             |

**✅ Correct Answer: B**

> When multiple interfaces provide the same default method, implementing class must **override** it to resolve conflict.

---

### ✅ **\[Spring Boot] MCQ 23 — Logging Dependency**

Which starter provides Spring Boot logging?

| Option                         | Explanation |
| ------------------------------ | ----------- |
| A. spring-boot-starter-log4j   |             |
| B. spring-boot-starter-logging |             |
| C. spring-boot-logger          |             |
| D. spring-boot-starter-core    |             |

**✅ Correct Answer: B**

> Logging is auto-configured by `spring-boot-starter-logging`, which uses Logback by default.

---

### ✅ **\[Spring Boot] MCQ 24 — `@Primary` Annotation**

Why would you use `@Primary`?

| Option                                  | Explanation |
| --------------------------------------- | ----------- |
| A. To mark a default bean for injection |             |
| B. To enable profile-based loading      |             |
| C. To declare a singleton scope         |             |
| D. To force eager initialization        |             |

**✅ Correct Answer: A**

> When multiple beans of the same type exist, `@Primary` marks one as the default during autowiring.

---

### ✅ **\[Angular] MCQ 25 — Custom Pipe**

```ts
@Pipe({ name: 'double' })
export class DoublePipe implements PipeTransform {
  transform(value: number): number {
    return value * 2;
  }
}
```

Used as `{{ 5 | double }}` — What is output?

| Option       | Explanation |
| ------------ | ----------- |
| A. 10        |             |
| B. Error     |             |
| C. undefined |             |
| D. NaN       |             |

**✅ Correct Answer: A**

> Pipe receives the input, transforms, and returns `5 * 2 = 10`.

---

### ✅ **\[Angular] MCQ 26 — Lifecycle Hook Order**

Which is the correct order of lifecycle hooks?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. OnInit → DoCheck → AfterViewInit |             |
| B. DoCheck → OnInit → AfterViewInit |             |
| C. AfterViewInit → OnInit → DoCheck |             |
| D. OnInit → AfterViewInit → DoCheck |             |

**✅ Correct Answer: A**

> `OnInit` runs first, then Angular performs `DoCheck`, then `AfterViewInit`.

---

### ✅ **\[React] MCQ 27 — Lifting State**

Why do you "lift state up" in React?

| Option                                      | Explanation |
| ------------------------------------------- | ----------- |
| A. For reusing state inside same component  |             |
| B. To pass state between unrelated siblings |             |
| C. To move shared state to common ancestor  |             |
| D. To trigger useEffect faster              |             |

**✅ Correct Answer: C**

> Lifting state to the closest common parent allows both child components to share it.

---

### ✅ **\[React] MCQ 28 — JSX and Keys**

Why are `key` props used in list rendering?

| Option                             | Explanation |
| ---------------------------------- | ----------- |
| A. For styling                     |             |
| B. To uniquely identify list items |             |
| C. To bind event listeners         |             |
| D. For component testing           |             |

**✅ Correct Answer: B**

> React uses keys to optimize re-rendering by identifying changed elements.

---

### ✅ **\[Docker] MCQ 29 — Volume Persistence**

You run:

```bash
docker run -v data:/app/data myimage
```

What does this do?

| Option                                   | Explanation |
| ---------------------------------------- | ----------- |
| A. Mounts host path into container       |             |
| B. Creates named volume `data`           |             |
| C. Deletes `/app/data` on container exit |             |
| D. Shares memory between containers      |             |

**✅ Correct Answer: B**

> Named volume `data` is created (if not present) and mounted to `/app/data`.

---

### ✅ **\[Kubernetes] MCQ 30 — CrashLoopBackOff**

Which of the following causes `CrashLoopBackOff`?

| Option                             | Explanation |
| ---------------------------------- | ----------- |
| A. Liveness probe fails repeatedly |             |
| B. Service has no selector         |             |
| C. ConfigMap missing in pod        |             |
| D. Ingress not found               |             |

**✅ Correct Answer: A**

> If the **liveness probe fails repeatedly**, Kubernetes restarts the container → causes `CrashLoopBackOff`.

---

Perfect — here's the next batch of **10 real, expert-level MCQs (31–40)** across Java, Spring Boot, Angular, React, Docker, and Kubernetes:

---

### ✅ **\[Java] MCQ 31 — Threads and Synchronization**

```java
public synchronized void increment() {
    count++;
}
```

If two threads access this method simultaneously?

| Option                                      | Explanation |
| ------------------------------------------- | ----------- |
| A. Both threads run at the same time        |             |
| B. One thread waits for the other to finish |             |
| C. It causes deadlock                       |             |
| D. count is always 0                        |             |

**✅ Correct Answer: B**

> `synchronized` ensures only one thread can execute the method at a time on the same object.

---

### ✅ **\[Java] MCQ 32 — Stream Terminal Operation**

```java
List<String> names = List.of("Tom", "Jerry");
names.stream().forEach(System.out::println);
```

Which type of operation is `forEach()`?

| Option          | Explanation |
| --------------- | ----------- |
| A. Intermediate |             |
| B. Terminal     |             |
| C. Lazy         |             |
| D. Filter       |             |

**✅ Correct Answer: B**

> `forEach` is a **terminal operation** — it triggers the execution of the stream pipeline.

---

### ✅ **\[Spring Boot] MCQ 33 — Profile Activation**

You want to activate the `dev` profile. Which is correct?

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. `spring.profiles.dev=true`        |             |
| B. `--spring.profiles.active=dev`    |             |
| C. `profiles: [dev]` in YAML         |             |
| D. `@ActiveProfiles("dev")` on class |             |

**✅ Correct Answer: B**

> This is the standard way to activate a Spring Boot profile at runtime using CLI.

---

### ✅ **\[Spring Boot] MCQ 34 — `@ConfigurationProperties`**

Why use `@ConfigurationProperties`?

| Option                                 | Explanation |
| -------------------------------------- | ----------- |
| A. Auto-register controller beans      |             |
| B. Externalize and bind config to POJO |             |
| C. Enable AOP globally                 |             |
| D. Handle CORS                         |             |

**✅ Correct Answer: B**

> It allows Spring to bind external YAML/properties directly to Java objects.

---

### ✅ **\[Angular] MCQ 35 — Event Binding**

```html
<button (click)="onClick()">Click</button>
```

What does this do?

| Option                          | Explanation |
| ------------------------------- | ----------- |
| A. Binds data                   |             |
| B. Calls `onClick` on component |             |
| C. Emits output                 |             |
| D. Creates a new event stream   |             |

**✅ Correct Answer: B**

> `(click)` is Angular's way of binding **DOM events** to component methods.

---

### ✅ **\[Angular] MCQ 36 — Reactive Forms Validation**

Which form validator checks for non-empty input?

| Option                 | Explanation |
| ---------------------- | ----------- |
| A. Validators.max      |             |
| B. Validators.min      |             |
| C. Validators.null     |             |
| D. Validators.required |             |

**✅ Correct Answer: D**

> `Validators.required` ensures the control is **not null or empty**.

---

### ✅ **\[React] MCQ 37 — Controlled Component**

```jsx
<input value={name} onChange={e => setName(e.target.value)} />
```

What kind of component is this?

| Option          | Explanation |
| --------------- | ----------- |
| A. Uncontrolled |             |
| B. Stateful     |             |
| C. Controlled   |             |
| D. Refs-based   |             |

**✅ Correct Answer: C**

> When value is bound to state and updated via `onChange`, it's a **controlled** component.

---

### ✅ **\[React] MCQ 38 — useEffect with Cleanup**

```jsx
useEffect(() => {
  const id = setInterval(() => console.log('Tick'), 1000);
  return () => clearInterval(id);
}, []);
```

What does this achieve?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Never logs                    |             |
| B. Infinite logging              |             |
| C. Cleans up interval on unmount |             |
| D. Clears interval after 1 run   |             |

**✅ Correct Answer: C**

> The return function in `useEffect` acts as a **cleanup**, invoked on unmount.

---

### ✅ **\[Docker] MCQ 39 — Detached Mode**

What does `docker run -d myimage` do?

| Option                | Explanation |
| --------------------- | ----------- |
| A. Interactive shell  |             |
| B. Runs in background |             |
| C. Displays logs      |             |
| D. Stops after run    |             |

**✅ Correct Answer: B**

> `-d` means **detached mode**, so the container runs in background.

---

### ✅ **\[Kubernetes] MCQ 40 — ConfigMap Volume**

You define:

```yaml
volumeMounts:
  - mountPath: /config
    name: config-volume
volumes:
  - name: config-volume
    configMap:
      name: my-config
```

What is mounted?

| Option                          | Explanation |
| ------------------------------- | ----------- |
| A. `/config/my-config.yaml`     |             |
| B. ConfigMap as environment     |             |
| C. ConfigMap files in `/config` |             |
| D. Secret volume                |             |

**✅ Correct Answer: C**

> Each ConfigMap entry is mounted as a file inside `/config`.

---

Great! Here's the next batch: **Expert-Level MCQs 41–50** — fully real, code-based, and non-repeating.

---

### ✅ **\[Java] MCQ 41 — Functional Interface Rules**

```java
@FunctionalInterface
public interface MyInterface {
    void doWork();
    default void log() { System.out.println("Logging"); }
}
```

Why is this valid?

| Option                                      | Explanation |
| ------------------------------------------- | ----------- |
| A. Only one abstract method allowed         |             |
| B. `default` methods don't break rule       |             |
| C. Must extend Runnable                     |             |
| D. Functional interface cannot have methods |             |

**✅ Correct Answer: B**

> `@FunctionalInterface` allows default methods as long as there's only one **abstract** method.

---

### ✅ **\[Java] MCQ 42 — Stream Reduce**

```java
List<Integer> nums = Arrays.asList(1, 2, 3);
int result = nums.stream().reduce(1, (a, b) -> a * b);
```

What is `result`?

| Option | Explanation |
| ------ | ----------- |
| A. 6   |             |
| B. 1   |             |
| C. 0   |             |
| D. 12  |             |

**✅ Correct Answer: D**

> `1 * 1 * 2 * 3 = 6`, but initial identity is 1, so `1 * 1 * 2 * 3 = 6`. Hence, **Answer: D = 6**.

---

### ✅ **\[Spring Boot] MCQ 43 — Custom Starter**

Why would you create a Spring Boot starter?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. To define a shared UI theme      |             |
| B. To auto-configure custom modules |             |
| C. For versioning YAML files        |             |
| D. To isolate Spring profiles       |             |

**✅ Correct Answer: B**

> Starters allow bundling auto-config + dependencies for reusability.

---

### ✅ **\[Spring Boot] MCQ 44 — Bean Definition Conflict**

Two `@Bean` methods return same type. What happens?

| Option                                                       | Explanation |
| ------------------------------------------------------------ | ----------- |
| A. Spring fails to start                                     |             |
| B. Last one overrides previous                               |             |
| C. Throws `NoUniqueBeanDefinitionException` if not qualified |             |
| D. Both are registered                                       |             |

**✅ Correct Answer: C**

> If not using `@Qualifier`, Spring fails due to ambiguity.

---

### ✅ **\[Angular] MCQ 45 — ngOnChanges Lifecycle**

Which hook detects changes to `@Input()`?

| Option             | Explanation |
| ------------------ | ----------- |
| A. ngInit          |             |
| B. ngOnChanges     |             |
| C. ngOnDestroy     |             |
| D. ngAfterViewInit |             |

**✅ Correct Answer: B**

> `ngOnChanges()` triggers when any bound `@Input()` value changes.

---

### ✅ **\[Angular] MCQ 46 — Structural Directive**

Which is a **structural** directive?

| Option         | Explanation |
| -------------- | ----------- |
| A. \*ngIf      |             |
| B. ngModel     |             |
| C. ngClass     |             |
| D. \[disabled] |             |

**✅ Correct Answer: A**

> Structural directives **modify the DOM layout** by adding/removing elements.

---

### ✅ **\[React] MCQ 47 — useReducer**

Why choose `useReducer` over `useState`?

| Option                                     | Explanation |
| ------------------------------------------ | ----------- |
| A. For large JSON inputs                   |             |
| B. For complex state logic and transitions |             |
| C. Only when props are static              |             |
| D. It's faster than useState               |             |

**✅ Correct Answer: B**

> `useReducer` handles **complex state transitions**, like Redux-style management.

---

### ✅ **\[React] MCQ 48 — React.StrictMode**

What is the purpose of `StrictMode`?

| Option                         | Explanation |
| ------------------------------ | ----------- |
| A. Prevents state updates      |             |
| B. Runs components twice (dev) |             |
| C. Enables SSR                 |             |
| D. Forces production build     |             |

**✅ Correct Answer: B**

> In dev, React runs components **twice** to detect side-effects and unsafe patterns.

---

### ✅ **\[Docker] MCQ 49 — Multi-Stage Build**

Why use multi-stage Docker builds?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. Faster container networking      |             |
| B. Smaller final image size         |             |
| C. Logs persist after build         |             |
| D. Supports multi-container linking |             |

**✅ Correct Answer: B**

> Multi-stage builds let you compile in one image and copy only needed output into final image, keeping it **lightweight**.

---

### ✅ **\[Kubernetes] MCQ 50 — StatefulSet**

When should you use a StatefulSet?

| Option                              | Explanation |
| ----------------------------------- | ----------- |
| A. Stateless APIs                   |             |
| B. Static content apps              |             |
| C. Stateful apps needing stable IDs |             |
| D. Frontend UIs                     |             |

**✅ Correct Answer: C**

> `StatefulSet` is ideal for databases and apps needing **persistent identity** and volume.

---

Great! Here are the next **10 real, advanced-level MCQs (51–60)** — continuing with unique questions and explanations.

---

### ✅ **\[Java] MCQ 51 — Volatile Keyword**

```java
volatile boolean running = true;
```

What does `volatile` ensure?

| Option                                  | Explanation |
| --------------------------------------- | ----------- |
| A. Variable cannot be modified          |             |
| B. Atomicity of read/write              |             |
| C. Visibility across threads            |             |
| D. Thread-safety of compound operations |             |

**✅ Correct Answer: C**

> `volatile` ensures updates to a variable are **visible across threads**, but not atomic for compound ops.

---

### ✅ **\[Java] MCQ 52 — CompletableFuture**

Which method waits for all futures to complete?

```java
CompletableFuture.allOf(f1, f2, f3)
```

| Option                                  | Explanation |
| --------------------------------------- | ----------- |
| A. Returns result list                  |             |
| B. Waits & throws exception if any fail |             |
| C. Waits for all to complete            |             |
| D. Waits for first to complete          |             |

**✅ Correct Answer: C**

> `allOf` blocks until **all futures complete**, success or fail. Use `.join()` for results.

---

### ✅ **\[Spring Boot] MCQ 53 — Actuator Custom Endpoint**

How do you expose a custom actuator endpoint?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. `@Controller`                  |             |
| B. `@Endpoint(id = "custom")`     |             |
| C. `@RestController("/actuator")` |             |
| D. `@ActuatorMapping("/custom")`  |             |

**✅ Correct Answer: B**

> `@Endpoint` with `@ReadOperation` or `@WriteOperation` creates custom actuator endpoints.

---

### ✅ **\[Spring Boot] MCQ 54 — Circular Dependency**

What resolves circular dependency issues?

| Option                   | Explanation |
| ------------------------ | ----------- |
| A. `@ComponentScan`      |             |
| B. Using `@Lazy`         |             |
| C. Removing `@Autowired` |             |
| D. Using `@Primary`      |             |

**✅ Correct Answer: B**

> `@Lazy` delays bean creation, breaking the circular reference during startup.

---

### ✅ **\[Angular] MCQ 55 — Reactive Forms Validation**

Which returns an `Observable<boolean>` for form status?

| Option                  | Explanation |
| ----------------------- | ----------- |
| A. `form.status`        |             |
| B. `form.valueChanges`  |             |
| C. `form.statusChanges` |             |
| D. `form.isValid()`     |             |

**✅ Correct Answer: C**

> `statusChanges` emits whenever **validity** of form changes — returns `"VALID"`, `"INVALID"`, etc.

---

### ✅ **\[Angular] MCQ 56 — DI Hierarchy**

Injecting service at component level leads to?

| Option                         | Explanation |
| ------------------------------ | ----------- |
| A. Shared singleton across app |             |
| B. Isolated service instance   |             |
| C. Cannot inject this way      |             |
| D. Angular error on startup    |             |

**✅ Correct Answer: B**

> Providers declared in `@Component` scope result in **new instance per component**.

---

### ✅ **\[React] MCQ 57 — Key Prop in Lists**

Why is `key` important in mapped components?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Avoids CSS conflicts          |             |
| B. Helps React identify elements |             |
| C. Used for routing              |             |
| D. Prevents state loss           |             |

**✅ Correct Answer: B**

> `key` allows React to **diff efficiently**, minimizing re-renders and DOM changes.

---

### ✅ **\[React] MCQ 58 — Forward Refs**

Purpose of `forwardRef` in React?

| Option                         | Explanation |
| ------------------------------ | ----------- |
| A. Use props in hooks          |             |
| B. Pass ref to child component |             |
| C. Handle error boundaries     |             |
| D. Optimize performance        |             |

**✅ Correct Answer: B**

> `forwardRef` allows parent to pass a **ref** to a child DOM element or custom component.

---

### ✅ **\[Docker] MCQ 59 — CMD vs ENTRYPOINT**

What's a key difference?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Both override base image CMD  |             |
| B. CMD is ignored if args passed |             |
| C. ENTRYPOINT replaces CMD       |             |
| D. CMD cannot be used with RUN   |             |

**✅ Correct Answer: B**

> If you pass arguments during `docker run`, **CMD is overridden**, but ENTRYPOINT still executes.

---

### ✅ **\[Kubernetes] MCQ 60 — ConfigMap Usage**

You define a `ConfigMap` and mount it as volume. What is true?

| Option                                 | Explanation |
| -------------------------------------- | ----------- |
| A. It's immutable                      |             |
| B. It can be reloaded live             |             |
| C. Changes require pod restart         |             |
| D. ConfigMaps are encrypted by default |             |

**✅ Correct Answer: C**

> ConfigMap values in volumes are **not updated live** — require pod **recreation** to reflect changes.

---

Perfect — I’ll now proceed with the next **10 high-difficulty MCQs (61–70)** across Java, Spring Boot, Angular, React, Docker, and Kubernetes — all unique, code-based, and with real-world explanations.

---

### ✅ **\[Java] MCQ 61 — Stream Short-Circuiting**

```java
Stream.of("A", "BB", "CCC")
      .filter(s -> s.length() > 1)
      .findFirst();
```

What is the result?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Skips "A", returns "BB"       |             |
| B. Returns "CCC"                 |             |
| C. Returns all matching elements |             |
| D. Compile-time error            |             |

**✅ Correct Answer: A**

> `findFirst()` is a **short-circuit terminal operation**, returns the first matching element and stops processing.

---

### ✅ **\[Java] MCQ 62 — TreeSet & Comparator**

```java
TreeSet<String> set = new TreeSet<>((a, b) -> 0);
set.add("Z"); set.add("A");
System.out.println(set.size());
```

What does it print?

| Option           | Explanation |
| ---------------- | ----------- |
| A. 2             |             |
| B. 1             |             |
| C. 0             |             |
| D. Runtime error |             |

**✅ Correct Answer: B**

> The comparator treats all elements as **equal** (returns `0`), so only **one is stored**.

---

### ✅ **\[Spring Boot] MCQ 63 — Profiles with @Value**

Given:

```yaml
spring:
  profiles: dev
my:
  url: http://dev.local
```

```java
@Value("${my.url}")
String url;
```

Which profile must be active to inject?

| Option     | Explanation |
| ---------- | ----------- |
| A. Any     |             |
| B. default |             |
| C. dev     |             |
| D. prod    |             |

**✅ Correct Answer: C**

> The value is under profile-specific key, so **`dev` must be active** to resolve the property.

---

### ✅ **\[Spring Boot] MCQ 64 — Constructor Injection**

Why is constructor injection preferred in Spring Boot?

| Option                          | Explanation |
| ------------------------------- | ----------- |
| A. Avoids circular dependencies |             |
| B. Easier for testing           |             |
| C. Ensures immutability         |             |
| D. All of the above             |             |

**✅ Correct Answer: D**

> Constructor injection improves **immutability**, **testability**, and helps avoid circular dependencies.

---

### ✅ **\[Angular] MCQ 65 — Standalone Components**

Angular 15+ introduced:

```ts
@Component({
  standalone: true,
  imports: [CommonModule]
})
```

Why use standalone components?

| Option                 | Explanation |
| ---------------------- | ----------- |
| A. Avoid NgModules     |             |
| B. Enable lazy loading |             |
| C. Simplify structure  |             |
| D. All of the above    |             |

**✅ Correct Answer: D**

> Standalone components help **reduce boilerplate**, **improve modularity**, and support **direct lazy loading**.

---

### ✅ **\[Angular] MCQ 66 — ControlValueAccessor**

Why implement `ControlValueAccessor`?

| Option                               | Explanation |
| ------------------------------------ | ----------- |
| A. To create custom HTTP interceptor |             |
| B. For dynamic routing               |             |
| C. To integrate custom form controls |             |
| D. To bind input/output properties   |             |

**✅ Correct Answer: C**

> It allows custom components to behave like native form controls in **Reactive/Template-driven forms**.

---

### ✅ **\[React] MCQ 67 — useCallback Optimization**

```jsx
const memoized = useCallback(() => doSomething(id), [id]);
```

Why is this used?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Prevent function recreation   |             |
| B. Always re-renders component   |             |
| C. Caches the return value       |             |
| D. Replaces memoization entirely |             |

**✅ Correct Answer: A**

> `useCallback` avoids **unnecessary function recreation** between renders unless dependencies change.

---

### ✅ **\[React] MCQ 68 — Refs vs State**

Why use `useRef()` over state?

| Option                          | Explanation |
| ------------------------------- | ----------- |
| A. For storing static constants |             |
| B. For tracking render count    |             |
| C. To avoid re-render           |             |
| D. For prop drilling            |             |

**✅ Correct Answer: C**

> `useRef` allows mutable values **without triggering re-renders** like `useState` would.

---

### ✅ **\[Docker] MCQ 69 — ENTRYPOINT Script**

You define:

```Dockerfile
ENTRYPOINT ["./start.sh"]
```

What is required for this to work?

| Option                             | Explanation |
| ---------------------------------- | ----------- |
| A. `start.sh` must be in PATH      |             |
| B. It must have execute permission |             |
| C. The container must be Ubuntu    |             |
| D. It must be built with Alpine    |             |

**✅ Correct Answer: B**

> If `start.sh` is used as `ENTRYPOINT`, it **must be executable**, else container fails to start.

---

### ✅ **\[Kubernetes] MCQ 70 — Deployment Rollout**

You run:

```bash
kubectl rollout restart deployment my-app
```

What does it do?

| Option                            | Explanation |
| --------------------------------- | ----------- |
| A. Deletes pods and re-creates    |             |
| B. Resets config map              |             |
| C. Triggers zero-downtime restart |             |
| D. Rolls back to previous version |             |

**✅ Correct Answer: C**

> This command **restarts pods gracefully** while maintaining deployment availability (rolling update).

---

Great! Let’s continue with the next **10 high-difficulty, non-repeating MCQs (71–80)** with real code and explanations across Java, Spring Boot, Angular, React, Docker, and Kubernetes:

---

### ✅ **\[Java] MCQ 71 — CompletableFuture Composition**

```java
CompletableFuture<Integer> cf1 = CompletableFuture.supplyAsync(() -> 2);
CompletableFuture<Integer> cf2 = cf1.thenApplyAsync(i -> i * 3);
System.out.println(cf2.join());
```

What will it print?

| Option       | Explanation |
| ------------ | ----------- |
| A. 2         |             |
| B. 3         |             |
| C. 6         |             |
| D. Exception |             |

**✅ Correct Answer: C**

> `cf1` returns 2; `cf2` multiplies it by 3 asynchronously. `join()` waits and returns `6`.

---

### ✅ **\[Java] MCQ 72 — Static Initializer Order**

```java
class Test {
    static {
        System.out.println("Static block");
    }
    public static void main(String[] args) {
        System.out.println("Main method");
    }
}
```

What is the output?

| Option                        | Explanation |
| ----------------------------- | ----------- |
| A. Static block → Main method |             |
| B. Main method → Static block |             |
| C. Main method only           |             |
| D. Compile error              |             |

**✅ Correct Answer: A**

> Static block executes **before `main()`** when the class is loaded.

---

### ✅ **\[Spring Boot] MCQ 73 — @ConfigurationProperties**

```java
@ConfigurationProperties(prefix = "app")
public class AppConfig {
    private String name;
    // getters/setters
}
```

Which is required for this to work?

| Option                                                             | Explanation |
| ------------------------------------------------------------------ | ----------- |
| A. `@Component` or registered via `@EnableConfigurationProperties` |             |
| B. Only `@Value` is needed                                         |             |
| C. It auto-loads without any annotation                            |             |
| D. Works only in `application.yaml`                                |             |

**✅ Correct Answer: A**

> `@ConfigurationProperties` needs to be registered as a **Spring bean** to be processed.

---

### ✅ **\[Spring Boot] MCQ 74 — Embedded Tomcat Port Binding**

If `server.port=80` and you run as non-root, what happens?

| Option                         | Explanation |
| ------------------------------ | ----------- |
| A. Starts normally             |             |
| B. Fails with permission error |             |
| C. Falls back to 8080          |             |
| D. Ignores port config         |             |

**✅ Correct Answer: B**

> On Linux/macOS, ports < 1024 need **root privileges**, or Spring Boot fails to bind to port 80.

---

### ✅ **\[Angular] MCQ 75 — Router Guards Execution Order**

You apply:

```ts
canActivate, canLoad, canDeactivate
```

Which runs first when navigating to a **lazy-loaded** route?

| Option                 |
| ---------------------- |
| A. canActivate         |
| B. canLoad             |
| C. canDeactivate       |
| D. All run in parallel |

**✅ Correct Answer: B**

> `canLoad` prevents the route from loading at all. It executes **before** `canActivate`.

---

### ✅ **\[Angular] MCQ 76 — Reactive Form Control Update**

```ts
this.form.get('email')?.setValue('test@example.com');
```

What is true?

| Option                           | Explanation |
| -------------------------------- | ----------- |
| A. Triggers validation           |             |
| B. Does not update the form      |             |
| C. Requires manual detectChanges |             |
| D. Only works in template forms  |             |

**✅ Correct Answer: A**

> `setValue()` on `FormControl` **triggers validators and change detection**.

---

### ✅ **\[React] MCQ 77 — Component Key Prop Importance**

In a list rendering:

```jsx
{items.map((item, i) => <li key={i}>{item}</li>)}
```

Why is using index as `key` discouraged?

| Option                                 |
| -------------------------------------- |
| A. It causes visual flicker            |
| B. It prevents state reuse issues      |
| C. It triggers unnecessary DOM diffing |
| D. All of the above                    |

**✅ Correct Answer: D**

> Using index as key **confuses React’s reconciliation** during reordering or insert/delete. Prefer stable IDs.

---

### ✅ **\[React] MCQ 78 — Custom Hook Rules**

Which violates **Rules of Hooks**?

| Option                                    |
| ----------------------------------------- |
| A. Calling hook in condition              |
| B. Calling hook in top-level of component |
| C. Using hook in another custom hook      |
| D. Using hook inside effect               |

**✅ Correct Answer: A**

> Hooks must be called **unconditionally at the top level** of the component or custom hook.

---

### ✅ **\[Docker] MCQ 79 — Volume Mounting Syntax**

What does this do?

```bash
docker run -v /host/data:/container/data ubuntu
```

| Option                                     |
| ------------------------------------------ |
| A. Binds /host/data from host to container |
| B. Creates anonymous volume                |
| C. Shares container’s /data to host        |
| D. Attaches container output to host       |

**✅ Correct Answer: A**

> `-v host:container` binds a **host directory into the container**.

---

### ✅ **\[Kubernetes] MCQ 80 — CrashLoopBackOff**

If your container crashes on start, what state does pod show?

| Option              |
| ------------------- |
| A. Running          |
| B. Succeeded        |
| C. CrashLoopBackOff |
| D. Pending          |

**✅ Correct Answer: C**

> **CrashLoopBackOff** means container started, failed, and K8s is retrying with backoff logic.

---
Perfect. Here's the next set — **MCQs 81 to 90** — all high-difficulty, non-repeating, across the same tech stack.

---

### ✅ **\[Java] MCQ 81 — Diamond Problem in Interfaces**

```java
interface A { default void hello() { System.out.println("Hello A"); } }
interface B { default void hello() { System.out.println("Hello B"); } }

class C implements A, B {
    public void hello() { A.super.hello(); }
}
```

What is printed when `new C().hello();` is called?

| Option            | Explanation |
| ----------------- | ----------- |
| A. Hello A        |             |
| B. Hello B        |             |
| C. Compile error  |             |
| D. Ambiguous call |             |

**✅ Correct Answer: A**

> You must **override** the method and explicitly choose which interface’s method to use with `A.super.hello()`.

---

### ✅ **\[Java] MCQ 82 — try-with-resources AutoCloseable**

```java
class MyResource implements AutoCloseable {
    public void close() {
        System.out.print("C");
    }
}

try (MyResource r = new MyResource()) {
    System.out.print("T");
}
```

What is the output?

| Option | Explanation |
| ------ | ----------- |
| A. TC  |             |
| B. CT  |             |
| C. C   |             |
| D. T   |             |

**✅ Correct Answer: A**

> First `"T"` prints in `try`, then `close()` prints `"C"` — total: `TC`.

---

### ✅ **\[Spring Boot] MCQ 83 — Lazy Beans**

```java
@Component
@Lazy
public class HeavyBean { ... }
```

When is `HeavyBean` initialized?

| Option                     |
| -------------------------- |
| A. At application startup  |
| B. When injected somewhere |
| C. Never                   |
| D. At compile time         |

**✅ Correct Answer: B**

> `@Lazy` tells Spring to defer creation **until first use** (injection or reference).

---

### ✅ **\[Spring Boot] MCQ 84 — Circular Dependency Detection**

Which pair **can cause** a circular dependency?

| Option                                               |
| ---------------------------------------------------- |
| A. A has `@Autowired` B, B has `@Autowired` A        |
| B. A uses B with `@Lazy`, B uses A with `@Autowired` |
| C. A uses B via constructor, B uses A via setter     |
| D. All of the above                                  |

**✅ Correct Answer: D**

> All combinations **can create circular references** unless handled via lazy injection or `ObjectFactory`.

---

### ✅ **\[Angular] MCQ 85 — Directive vs Component**

What is a key difference between a **component** and a **directive**?

| Option                        |
| ----------------------------- |
| A. Component has a template   |
| B. Directive supports DI      |
| C. Both extend same class     |
| D. Directive must be exported |

**✅ Correct Answer: A**

> Directives **manipulate DOM**; **components** are directives with a **template**.

---

### ✅ **\[Angular] MCQ 86 — Zone.js Role**

What is the main role of `Zone.js` in Angular?

| Option                                      |
| ------------------------------------------- |
| A. Manage style encapsulation               |
| B. Detect async events for change detection |
| C. Compile TypeScript                       |
| D. Serve as HTTP client                     |

**✅ Correct Answer: B**

> Angular uses `Zone.js` to **monkey-patch async APIs** and trigger change detection automatically.

---

### ✅ **\[React] MCQ 87 — useRef vs useState**

Why might you use `useRef` instead of `useState`?

| Option                                         |
| ---------------------------------------------- |
| A. To store data without triggering re-renders |
| B. To hold JSX elements                        |
| C. To define functions                         |
| D. To access external libraries                |

**✅ Correct Answer: A**

> `useRef()` is used to **hold mutable values** across renders without triggering re-renders.

---

### ✅ **\[React] MCQ 88 — Event Bubbling Control**

```jsx
<div onClick={() => console.log("div")}>
  <button onClick={e => { e.stopPropagation(); console.log("btn") }}>
    Click
  </button>
</div>
```

What is printed?

| Option     |
| ---------- |
| A. div btn |
| B. btn     |
| C. div     |
| D. Nothing |

**✅ Correct Answer: B**

> `stopPropagation()` prevents the parent’s event from firing. Only `"btn"` is logged.

---

### ✅ **\[Docker] MCQ 89 — ENTRYPOINT vs CMD**

In Dockerfile:

```Dockerfile
ENTRYPOINT ["echo"]
CMD ["Hello"]
```

What does `docker run myimage` print?

| Option         |
| -------------- |
| A. echo        |
| B. Hello       |
| C. echo Hello  |
| D. CMD ignored |

**✅ Correct Answer: C**

> `ENTRYPOINT` sets the **base command**, `CMD` provides **default args**. So: `echo Hello`.

---

### ✅ **\[Kubernetes] MCQ 90 — ConfigMap vs Secret**

Which of the following is true?

| Option                                       |
| -------------------------------------------- |
| A. ConfigMap and Secret are stored encrypted |
| B. Secret is base64 encoded, not encrypted   |
| C. ConfigMap is encrypted by default         |
| D. Both are insecure by default              |

**✅ Correct Answer: B**

> Kubernetes **encodes** Secrets in base64, but doesn't encrypt them unless KMS is configured.

---

Great! Here's the next batch — **MCQs 91 to 100** — continuing with difficult, non-repeating questions across Java, Spring Boot, Angular, React, Docker, and Kubernetes.

---

### ✅ **\[Java] MCQ 91 — ThreadLocal Pitfall**

```java
ThreadLocal<Integer> local = new ThreadLocal<>();
local.set(10);
local.remove();
System.out.println(local.get());
```

What is the output?

| Option   |
| -------- |
| A. 10    |
| B. null  |
| C. 0     |
| D. Error |

**✅ Correct Answer: B**

> After `remove()`, the thread-local variable is cleared, and `get()` returns `null`.

---

### ✅ **\[Java] MCQ 92 — ForkJoinPool Behavior**

```java
ForkJoinPool pool = new ForkJoinPool(2);
pool.submit(() -> IntStream.range(0, 10).parallel().forEach(System.out::println));
```

What can be said about thread usage?

| Option                                  |
| --------------------------------------- |
| A. Uses only 1 thread                   |
| B. Uses exactly 2 threads               |
| C. May use more threads than pool size  |
| D. Will block without explicit `join()` |

**✅ Correct Answer: C**

> Parallel streams can **steal threads** from the common pool regardless of custom ForkJoinPool size.

---

### ✅ **\[Spring Boot] MCQ 93 — ApplicationRunner vs CommandLineRunner**

Which is true?

| Option                                           |
| ------------------------------------------------ |
| A. Both run at startup                           |
| B. ApplicationRunner gets `ApplicationArguments` |
| C. CommandLineRunner gets raw String\[]          |
| D. All of the above                              |

**✅ Correct Answer: D**

> Both interfaces run post-startup; only their method signatures differ.

---

### ✅ **\[Spring Boot] MCQ 94 — Property Overriding**

Given:

```yaml
app.value: default
---
spring:
  profiles: prod
app.value: production
```

App is run with `--spring.profiles.active=prod`. What is the value of `app.value`?

| Option        |
| ------------- |
| A. default    |
| B. null       |
| C. production |
| D. Both       |

**✅ Correct Answer: C**

> Profile-specific values override default values when activated.

---

### ✅ **\[Angular] MCQ 95 — ViewChild Static**

```ts
@ViewChild('el', { static: false }) el: ElementRef;
```

What does `static: false` mean?

| Option                                              |
| --------------------------------------------------- |
| A. Element is available in `ngOnInit()`             |
| B. Element is only available in `ngAfterViewInit()` |
| C. It's compiled away                               |
| D. It auto-detects lifecycle                        |

**✅ Correct Answer: B**

> `static: false` means the query is resolved **after view init**, not during component init.

---

### ✅ **\[Angular] MCQ 96 — Custom Form Validator**

Where must a custom form validator be provided?

| Option                    |
| ------------------------- |
| A. @NgModule              |
| B. ReactiveFormsModule    |
| C. Component `providers`  |
| D. Validator class itself |

**✅ Correct Answer: C**

> Angular custom validators **must be registered** via `providers` using `NG_VALIDATORS`.

---

### ✅ **\[React] MCQ 97 — useLayoutEffect Timing**

What distinguishes `useLayoutEffect` from `useEffect`?

| Option              |
| ------------------- |
| A. Runs after paint |
| B. Blocks painting  |
| C. Async only       |
| D. Causes flicker   |

**✅ Correct Answer: B**

> `useLayoutEffect` runs **synchronously after DOM mutations but before paint**, blocking UI updates.

---

### ✅ **\[React] MCQ 98 — useReducer vs useState**

Why choose `useReducer` over `useState`?

| Option                          |
| ------------------------------- |
| A. Handles multiple values      |
| B. Forces re-render             |
| C. Centralizes update logic     |
| D. Only for performance reasons |

**✅ Correct Answer: C**

> `useReducer` is helpful when **state transitions** follow complex logic.

---

### ✅ **\[Docker] MCQ 99 — Bind Mount vs Volume**

Which is true about bind mounts?

| Option                                   |
| ---------------------------------------- |
| A. Lives under `/var/lib/docker/volumes` |
| B. Can’t map to host                     |
| C. Changes in host reflect immediately   |
| D. Slower than volumes                   |

**✅ Correct Answer: C**

> Bind mounts point to **host filesystem** paths and changes reflect immediately inside the container.

---

### ✅ **\[Kubernetes] MCQ 100 — Rolling Update Strategy**

What happens during a rolling update?

| Option                                   |
| ---------------------------------------- |
| A. All pods terminated then restarted    |
| B. Old pods and new pods run in parallel |
| C. Requires manual intervention          |
| D. Existing service is deleted first     |

**✅ Correct Answer: B**

> Rolling updates **gradually replace** old pods with new ones, maintaining service availability.

---







