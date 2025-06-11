

---

### 🔹 **Angular 19 MCQs (1–25)**

---

**1. What is the primary goal of Angular's `Signal` API introduced in Angular 16 and evolved in Angular 19?**
A. To replace RxJS
B. To manage form state
C. To enable fine-grained reactivity
D. To create dynamic routing
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** Signals in Angular allow fine-grained change tracking and reactivity without zone-based detection.

---

**2. What does `@Input({ alias: 'externalName' })` do in Angular 19?**
A. Makes the input required
B. Sets an alias for input binding
C. Tracks output changes
D. Prevents change detection
**Answer:** B
**Difficulty:** Basic
**Explanation:** It lets you use a different name for the input property in the parent component.

---

**3. Which directive is used for rendering items conditionally in Angular?**
A. \*ngSwitch
B. \*ngIf
C. \*ngClass
D. \*ngFor
**Answer:** B
**Difficulty:** Basic
**Explanation:** `*ngIf` is the standard directive for conditional rendering.

---

**4. What lifecycle hook is invoked after Angular checks the content projected into the component?**
A. ngAfterViewInit
B. ngOnChanges
C. ngAfterContentInit
D. ngOnInit
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ngAfterContentInit` is called after Angular projects external content into the component.

---

**5. What’s the main use of `ChangeDetectionStrategy.OnPush`?**
A. Always triggers change detection
B. Disables change detection
C. Optimizes performance by limiting checks
D. Only works with services
**Answer:** C
**Difficulty:** Advanced
**Explanation:** OnPush tells Angular to check for changes only when input references change, reducing overhead.

---

**6. How are standalone components declared?**
A. `@NgModule({ standalone: true })`
B. `@Component({ standalone: true })`
C. `@StandaloneComponent`
D. `@Directive({ standalone: true })`
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** The `standalone: true` flag inside `@Component()` makes a component standalone.

---

**7. What is the default change detection strategy in Angular 19?**
A. OnPush
B. Reactive
C. Default
D. Manual
**Answer:** C
**Difficulty:** Basic
**Explanation:** Angular runs the default change detection strategy unless overridden.

---

**8. What is `inject()` used for in Angular 19?**
A. Creating new components
B. Replacing `constructor` injection
C. Declaring directives
D. Bootstrapping modules
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `inject()` is used to inject dependencies outside the constructor (like in functions).

---

**9. Which Angular directive is used to style elements conditionally?**
A. \*ngIf
B. \*ngSwitch
C. \*ngClass
D. \*ngStyle
**Answer:** C
**Difficulty:** Basic
**Explanation:** `*ngClass` allows applying multiple classes conditionally.

---

**10. What does `RouterModule.forChild()` do?**
A. Registers routes globally
B. Registers routes lazily
C. Configures root routes
D. Enables route guarding
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `forChild()` is used to define child routes typically in feature modules.

---

**11. What is the purpose of `async` pipe in Angular?**
A. Converts a promise to observable
B. Pauses execution
C. Subscribes to observable and updates UI
D. Cancels pending observables
**Answer:** C
**Difficulty:** Basic
**Explanation:** `async` pipe auto-subscribes and handles cleanup.

---

**12. Which CLI flag generates a standalone component in Angular 19?**
A. `--module`
B. `--standalone`
C. `--ngModule=false`
D. `--no-bootstrap`
**Answer:** B
**Difficulty:** Basic
**Explanation:** `--standalone` flag in Angular CLI enables generation of standalone components.

---

**13. What operator is best for switching from one observable to another in Angular services?**
A. mergeMap
B. exhaustMap
C. concatMap
D. switchMap
**Answer:** D
**Difficulty:** Intermediate
**Explanation:** `switchMap` cancels the previous observable and subscribes to the new one.

---

**14. What’s the role of `FormBuilder` in reactive forms?**
A. Builds templates
B. Creates reactive form controls
C. Connects to server
D. Parses form events
**Answer:** B
**Difficulty:** Basic
**Explanation:** `FormBuilder` simplifies the creation of form groups and controls.

---

**15. What is the main benefit of Signals over RxJS for component state?**
A. Zone-free reactivity
B. Two-way binding
C. Class-based design
D. Lazy evaluation
**Answer:** A
**Difficulty:** Advanced
**Explanation:** Signals eliminate reliance on zone.js and support fine-grained updates.

---

**16. What method allows navigation in Angular programmatically?**
A. this.navigation()
B. this.route.push()
C. this.router.navigate()
D. this.route.to()
**Answer:** C
**Difficulty:** Basic
**Explanation:** `this.router.navigate()` is used to move between routes.

---

**17. What hook is used when you need access to ViewChild elements?**
A. ngOnInit
B. ngOnDestroy
C. ngAfterViewInit
D. ngAfterContentChecked
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ngAfterViewInit` ensures the view and its children are fully initialized.

---

**18. What is the main reason for lazy loading modules?**
A. Easier code
B. Performance optimization
C. Simplified routing
D. Better testing
**Answer:** B
**Difficulty:** Basic
**Explanation:** Lazy loading defers loading unused code, reducing initial bundle size.

---

**19. How do you reference a local variable in Angular templates?**
A. with `$var`
B. with `#varName`
C. with `@varName`
D. with `{varName}`
**Answer:** B
**Difficulty:** Basic
**Explanation:** Template reference variables are declared with `#`.

---

**20. What decorator is used for output event binding?**
A. @Input
B. @EventEmitter
C. @Output
D. @Emit
**Answer:** C
**Difficulty:** Basic
**Explanation:** `@Output` is used with `EventEmitter` for emitting custom events.

---
Perfect — here are the remaining **Angular 19 MCQs (21–100)** with correct answers, difficulty, and explanations:

---

### 🔹 **Angular 19 MCQs (21–40)**

---

**21. What’s the Angular service used to retrieve route parameters?**
A. RouteService
B. ActivatedRoute
C. ParamService
D. RouteParams
**Answer:** B
**Difficulty:** Basic
**Explanation:** `ActivatedRoute` provides access to route parameters, query params, and more.

---

**22. What does `Renderer2` in Angular help with?**
A. Interpolating templates
B. DOM manipulation in a safe way
C. Managing zones
D. Updating modules
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `Renderer2` allows safe DOM operations, abstracting away direct access.

---

**23. What is the purpose of `trackBy` in `*ngFor`?**
A. To bind event handlers
B. To reduce memory leaks
C. To optimize rendering
D. To disable animations
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `trackBy` prevents unnecessary DOM manipulations by tracking items by unique keys.

---

**24. Which Angular testing utility is used for creating component instances?**
A. TestModule
B. TestHarness
C. TestBed
D. ComponentFixture
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `TestBed` configures and initializes the environment for unit tests.

---

**25. Which Angular tool performs ahead-of-time (AOT) compilation?**
A. Webpack
B. Babel
C. ngc
D. tsc
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ngc` is Angular's AOT compiler, which compiles HTML and TypeScript before runtime.

---

**26. What does `ngZone.runOutsideAngular()` do?**
A. Prevents event binding
B. Boosts template rendering
C. Runs code outside Angular's change detection
D. Replaces `NgModules`
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Helps exclude performance-sensitive code from triggering Angular change detection.

---

**27. What’s the benefit of `defer` block introduced in Angular 17/19?**
A. Defers HTTP requests
B. Lazy loads child components
C. Adds microtask scheduling
D. Used for lazy template rendering
**Answer:** D
**Difficulty:** Advanced
**Explanation:** `@defer` blocks enable template-level lazy loading using control flow syntax.

---

**28. How is a custom validator created in Angular reactive forms?**
A. Using @Directive
B. Using ValidatorFn
C. With async pipe
D. Using AbstractDirective
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Custom validators implement `ValidatorFn` and return a validation error map.

---

**29. What does `provideRouter()` do in standalone Angular apps?**
A. Defines dependency injection tree
B. Initializes signal store
C. Configures router without NgModule
D. Registers app-level interceptors
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `provideRouter()` replaces `RouterModule.forRoot()` in standalone applications.

---

**30. What’s the purpose of `resolve` in Angular routing?**
A. Defines animations
B. Adds form validation
C. Pre-fetches data before route activation
D. Guards route deactivation
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** Resolvers are used to load data before navigating to a route.

---

**31. Which lifecycle hook is used for cleanup logic in Angular?**
A. ngAfterDestroy
B. ngDestroy
C. ngOnDestroy
D. ngClear
**Answer:** C
**Difficulty:** Basic
**Explanation:** `ngOnDestroy` is called when the component is destroyed.

---

**32. Which of the following best describes Signals in Angular 19?**
A. Observable replacement
B. New HTTP module
C. Fine-grained reactive primitives
D. Router wrapper
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Signals offer an alternative to observables for state changes.

---

**33. What does `environment.ts` manage in Angular CLI apps?**
A. All CSS styles
B. Application constants
C. Environment-specific configurations
D. Deployment pipeline
**Answer:** C
**Difficulty:** Basic
**Explanation:** `environment.ts` holds configurations for dev, prod, and staging environments.

---

**34. What is the function of `ngModel`?**
A. Two-way binding for template-driven forms
B. Registers new modules
C. Imports CSS styles
D. Declares route paths
**Answer:** A
**Difficulty:** Basic
**Explanation:** `ngModel` is used for two-way binding in forms.

---

**35. What does Angular's `Zone.js` do?**
A. Styles DOM
B. Tracks async operations
C. Provides routing
D. Adds HTTP interceptors
**Answer:** B
**Difficulty:** Advanced
**Explanation:** `Zone.js` tracks async operations to know when to trigger change detection.

---

**36. How do you lazy load a component in Angular 19 standalone?**
A. Using ViewChild
B. Using `import()`
C. Using RouterModule
D. With defer block only
**Answer:** B
**Difficulty:** Advanced
**Explanation:** Angular 14+ supports lazy loading using dynamic `import()`.

---

**37. Which module is used to define reactive forms?**
A. FormsModule
B. ReactiveFormsModule
C. HttpClientModule
D. NgZoneModule
**Answer:** B
**Difficulty:** Basic
**Explanation:** Reactive forms require importing `ReactiveFormsModule`.

---

**38. How does Angular detect changes in properties?**
A. Proxy binding
B. Dirty checking
C. Observables
D. Polling loop
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Angular uses dirty checking to detect when component input properties change.

---

**39. What is the `@HostListener` decorator used for?**
A. Emit events
B. Call methods on parent
C. Listen to DOM events on the host element
D. Create observables
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `@HostListener` allows you to bind events to the host element.

---

**40. What is the role of `HttpInterceptor`?**
A. Update styles
B. Modify HTTP requests/responses
C. Render templates
D. Enable animations
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Interceptors can add headers, log responses, and handle errors globally.

---
Continuing with the final set:

### 🔹 **Angular 19 MCQs (41–100)**

---

**41. What is a pure pipe in Angular?**
A. A pipe that updates when the browser refreshes
B. A pipe that runs on each keystroke
C. A pipe that runs only when input values change
D. A pipe that calls API
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** Pure pipes are recalculated only when their inputs change, improving performance.

---

**42. What is the use of `standalone: true` in Angular 19?**
A. Declares lazy routes
B. Avoids importing CommonModule
C. Declares a component without NgModule
D. Forces browser rendering
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** Standalone components remove the need for NgModules and simplify declarations.

---

**43. Which of the following does NOT trigger change detection?**
A. Button click
B. Observable emission
C. setTimeout
D. console.log
**Answer:** D
**Difficulty:** Basic
**Explanation:** `console.log` is synchronous and does not trigger Angular's change detection.

---

**44. How do you bind a property in Angular templates?**
A. {{property}}
B. (property)
C. \[property]
D. #property
**Answer:** C
**Difficulty:** Basic
**Explanation:** `[property]` binds a property to an element.

---

**45. What command runs unit tests in Angular CLI?**
A. ng test
B. ng run
C. ng check
D. ng serve --tests
**Answer:** A
**Difficulty:** Basic
**Explanation:** `ng test` compiles and runs tests using Karma or other test runners.

---

**46. What does `ng-container` do in Angular?**
A. Declares components
B. Acts as invisible wrapper for structural directives
C. Imports modules
D. Provides styling
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `ng-container` groups elements without adding extra DOM nodes.

---

**47. Which decorator is used to define an Angular directive?**
A. @Input
B. @Component
C. @Injectable
D. @Directive
**Answer:** D
**Difficulty:** Basic
**Explanation:** `@Directive` is used to define custom structural or attribute directives.

---

**48. What does `ngSubmit` do?**
A. Binds blur event
B. Submits forms and prevents default behavior
C. Clears forms
D. Triggers on blur
**Answer:** B
**Difficulty:** Basic
**Explanation:** `ngSubmit` is used to handle form submission in Angular.

---

**49. What is the key difference between template-driven and reactive forms?**
A. Reactive forms are in HTML only
B. Template-driven forms use observables
C. Reactive forms offer more control in TS code
D. Template-driven supports FormGroup
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** Reactive forms give programmatic control over validation and updates.

---

**50. What does `ɵɵdefineComponent` indicate in compiled code?**
A. Lazy load component
B. Runtime component definition
C. Angular zone trigger
D. Server-side rendering
**Answer:** B
**Difficulty:** Advanced
**Explanation:** Internal Angular Ivy compiler method for defining components at runtime.

---

**51. How do you bind to an event in Angular?**
A. (event)
B. {event}
C. \*event
D. #event
**Answer:** A
**Difficulty:** Basic
**Explanation:** Event binding uses `(event)` syntax, e.g., `(click)="onClick()"`.

---

**52. Which service is used to detect current URL in Angular?**
A. ActivatedRoute
B. Location
C. Router
D. HttpClient
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `Location` helps access and modify browser URL directly.

---

**53. What is `ComponentFixture` used for?**
A. Building animations
B. Creating service instances
C. Interacting with component in tests
D. Injecting modules
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ComponentFixture` allows test interaction with DOM and component.

---

**54. How does `ngOnChanges` differ from `ngOnInit`?**
A. Called after child view renders
B. Runs before constructor
C. Responds to input property changes
D. Called once only
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ngOnChanges` responds to changes in input-bound properties.

---

**55. What’s the main utility of `APP_INITIALIZER` token?**
A. Trigger bootstrapping
B. Configure form validators
C. Delay app init until async logic runs
D. Start observables
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Used to run logic (like config loading) before Angular starts.

---

**56. Which module must be imported for HTTP requests in Angular?**
A. FormsModule
B. HttpClientModule
C. RouterModule
D. ReactiveFormsModule
**Answer:** B
**Difficulty:** Basic
**Explanation:** `HttpClientModule` must be imported to make HTTP calls.

---

**57. What does `ViewChild()` return?**
A. Data binding
B. DOM reference to element/directive/component
C. Parent component
D. Change detector
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `@ViewChild()` returns a reference to an element or directive in the view.

---

**58. What is the primary function of `RouterOutlet`?**
A. Show errors
B. Trigger events
C. Load route components
D. Fetch data
**Answer:** C
**Difficulty:** Basic
**Explanation:** `RouterOutlet` acts as a placeholder for routed views.

---

**59. What does `zone.js` patch?**
A. CSS rendering
B. DOM queries
C. Async APIs like setTimeout, fetch
D. Local storage
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Zone.js patches async APIs to know when Angular needs to run change detection.

---

**60. What is `HostBinding` used for?**
A. Attach event listeners
B. Bind to host element property
C. Provide services
D. Bind DOM elements
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `@HostBinding` binds class or attribute values to the host element.

---

Awesome! Here's the final batch:

### 🔹 **Angular 19 MCQs (61–100)**

---

**61. What happens when a service is provided in 'root'?**
A. It is instantiated per component
B. It is tree-shakable and singleton
C. It loads lazily
D. It is ignored by DI
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `providedIn: 'root'` registers the service globally and ensures one instance.

---

**62. Which lifecycle hook runs after all content (ng-content) is projected?**
A. ngAfterViewInit
B. ngAfterContentInit
C. ngOnChanges
D. ngBootstrap
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `ngAfterContentInit` is called after the component's projected content is initialized.

---

**63. How do you apply two-way data binding in Angular?**
A. \[()]
B. {{}}
C. \[value]
D. (input)
**Answer:** A
**Difficulty:** Basic
**Explanation:** `[()]` is "banana in a box" syntax for two-way binding, e.g., `[(ngModel)]`.

---

**64. What’s the purpose of `ng add` command?**
A. Add NPM packages manually
B. Add dependencies and run schematics
C. Create routes
D. Format code
**Answer:** B
**Difficulty:** Basic
**Explanation:** `ng add` installs and configures libraries using their schematics.

---

**65. Which directive creates reusable logic for HTML attributes?**
A. Structural directive
B. Attribute directive
C. Async directive
D. Proxy directive
**Answer:** B
**Difficulty:** Basic
**Explanation:** Attribute directives modify the appearance or behavior of DOM elements.

---

**66. What does `ngDoCheck()` do?**
A. Detect changes in projected content
B. Respond to every change detection cycle
C. Validate user input
D. Prevent form submission
**Answer:** B
**Difficulty:** Advanced
**Explanation:** `ngDoCheck()` is called every time Angular’s change detection runs.

---

**67. Which file contains TypeScript entry for bootstrapping the Angular app?**
A. styles.css
B. index.html
C. main.ts
D. polyfills.ts
**Answer:** C
**Difficulty:** Basic
**Explanation:** `main.ts` bootstraps the root module and starts the application.

---

**68. How are template references created?**
A. \*var
B. \$var
C. #var
D. @var
**Answer:** C
**Difficulty:** Basic
**Explanation:** Use `#` to declare local references in templates (e.g., `#inputRef`).

---

**69. Which decorator is used for Angular Pipes?**
A. @Injectable
B. @Pipe
C. @Filter
D. @Service
**Answer:** B
**Difficulty:** Basic
**Explanation:** `@Pipe` is used to create custom pipes for transforming data.

---

**70. What is `title` binding written as in a template?**
A. title\:value
B. {title}
C. \[title]
D. (title)
**Answer:** C
**Difficulty:** Basic
**Explanation:** Property binding in Angular uses square brackets like `[title]="..."`.

---

**71. What happens if a provider is defined at both component and root level?**
A. Component one overrides root
B. Root one overrides component
C. App breaks
D. No service is injected
**Answer:** A
**Difficulty:** Intermediate
**Explanation:** Angular uses the closest provider — the component-level one overrides root.

---

**72. How do you debug change detection cycles?**
A. With console logs
B. With `ng.profiler`
C. By throwing errors
D. Through DOM
**Answer:** B
**Difficulty:** Advanced
**Explanation:** Angular DevTools and `ng.profiler` help debug change detection.

---

**73. What feature of Angular 19 optimizes large lists?**
A. Defer block
B. Virtual Scrolling
C. NgZone
D. Lazy Rendering
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Virtual scrolling renders only visible list items, improving performance.

---

**74. What’s the role of `CommonModule`?**
A. Global CSS
B. Routing
C. Provides ngIf, ngFor
D. Lazy load routes
**Answer:** C
**Difficulty:** Basic
**Explanation:** `CommonModule` includes common directives like `ngIf`, `ngFor`.

---

**75. Which CLI command updates Angular packages?**
A. ng update
B. ng upgrade
C. ng patch
D. ng install
**Answer:** A
**Difficulty:** Basic
**Explanation:** `ng update` updates Angular and dependencies to latest compatible versions.

---

**76. What’s the use of `ng-template`?**
A. Render HTML directly
B. Reusable component
C. Define a template block without rendering
D. Add CSS classes
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `ng-template` defines hidden templates for deferred or conditional rendering.

---

**77. What’s the purpose of `async` pipe in templates?**
A. Cancel subscriptions
B. Load HTML
C. Subscribe to observable and auto-unsubscribe
D. Format string
**Answer:** C
**Difficulty:** Basic
**Explanation:** `async` pipe subscribes to observables/promises and handles unsubscription.

---

**78. What does `HttpParams` help with?**
A. Setting headers
B. Parsing JSON
C. Building query parameters
D. Managing CORS
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `HttpParams` helps append and manage query parameters in HTTP requests.

---

**79. Which guard decides if navigation is allowed?**
A. CanActivate
B. CanLoad
C. CanDeactivate
D. Resolve
**Answer:** A
**Difficulty:** Intermediate
**Explanation:** `CanActivate` controls access to routes before navigation.

---

**80. What happens if a component doesn’t declare `standalone: true` and isn't in a module?**
A. It works fine
B. Angular fails to compile
C. It runs as lazy component
D. It skips change detection
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** If `standalone` is not set and the component isn’t declared in a module, it throws an error.

---

Here are the **real Angular 19 MCQs from 81 to 100**, each crafted with detailed content, correct answer, explanation, and difficulty level:

---

### 🔹 **Angular 19 MCQs (81–100)**

---

**81. What does the `computed()` function in Angular Signals do?**
A. Triggers manual change detection
B. Combines multiple signals into a derived value
C. Resets signals to default state
D. Monitors event emitters
**Answer:** B
**Difficulty:** Advanced
**Explanation:** `computed()` creates a derived signal that updates when its dependencies (other signals) change.

---

**82. Which feature allows conditional lazy loading of components in templates?**
A. @defer
B. @switch
C. LazyComponent
D. viewContainerRef
**Answer:** A
**Difficulty:** Advanced
**Explanation:** `@defer` enables lazy rendering of template blocks using Angular’s control flow syntax.

---

**83. What does the `inject()` function allow in Angular 19?**
A. Import external scripts
B. Inject dependencies outside of constructors
C. Create routes dynamically
D. Debug application state
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `inject()` enables DI in contexts like standalone functions or computed signals.

---

**84. What is the purpose of `effect()` in Angular’s signal API?**
A. Watches signals and triggers side effects
B. Computes derived values
C. Cleans up observables
D. Tracks route changes
**Answer:** A
**Difficulty:** Advanced
**Explanation:** `effect()` watches signals and reacts when they change, running side-effect logic (e.g., logging, API calls).

---

**85. What is functional route guard in Angular 19?**
A. A guard using observable streams
B. A guard written as a pure function using `inject()`
C. A guard based on signal evaluation
D. A deprecated feature
**Answer:** B
**Difficulty:** Advanced
**Explanation:** Functional guards use `inject()` to access services and return boolean/observables directly.

---

**86. How does Angular 19 optimize rendering with `defer` blocks?**
A. Moves rendering to after the user scrolls
B. Replaces `ngIf` completely
C. Loads component templates lazily under conditions
D. Pre-renders HTML on server
**Answer:** C
**Difficulty:** Advanced
**Explanation:** `@defer` allows lazy loading of portions of the UI based on user interaction, visibility, or timer.

---

**87. What are zoneless applications in Angular 19?**
A. Apps that skip event binding
B. Apps that run change detection manually
C. Apps that use signals and skip Zone.js
D. Apps without lifecycle hooks
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Angular 19 supports zoneless apps using signals to track changes without relying on `Zone.js`.

---

**88. What does `provideHttpClient()` do in Angular 19?**
A. Configures fetch API
B. Registers HttpClient in a standalone app
C. Creates a proxy to backend
D. Adds CORS support
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `provideHttpClient()` replaces the need for importing `HttpClientModule` in standalone environments.

---

**89. What’s the role of `RouterOutlet` in a standalone component?**
A. Defines input property
B. Enables form validations
C. Marks where route content is rendered
D. Adds NgModule support
**Answer:** C
**Difficulty:** Basic
**Explanation:** `RouterOutlet` is a directive that acts as a placeholder for components loaded via the router.

---

**90. What feature in Angular 19 enables automatic change tracking?**
A. Signals
B. Interceptors
C. FormsModule
D. Web Workers
**Answer:** A
**Difficulty:** Advanced
**Explanation:** Signals provide automatic and reactive change tracking through primitive state wrappers.

---

**91. What does `Typed Forms` feature offer in Angular 19?**
A. Support for CSS classes
B. Type safety for form controls and groups
C. Server-side validation
D. Automatic UI generation
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Typed Forms help enforce correct types for form values and validations using TypeScript.

---

**92. What is `:host-context()` used for in Angular component styles?**
A. Apply global styles
B. Style content inside ng-content
C. Style component based on ancestor’s class
D. Isolate styles completely
**Answer:** C
**Difficulty:** Advanced
**Explanation:** `:host-context()` allows applying styles based on parent selectors or conditions.

---

**93. What is IntersectionObserver used for in Angular apps?**
A. Form validation
B. Detecting when an element is visible in viewport
C. Triggering HTTP requests
D. Debugging observables
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** `IntersectionObserver` enables lazy loading or animation triggers based on element visibility.

---

**94. What change in Angular 19 supports scoped styling improvements?**
A. Shadow DOM
B. CSS isolation with \:host
C. Tailwind integration
D. Inline style merging
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Angular supports component-level scoped styles using `:host` and `:host-context`.

---

**95. What is differential loading?**
A. Lazy loading based on screen size
B. Serving modern JS to modern browsers and legacy JS to old ones
C. Removing unused modules
D. Module federation
**Answer:** B
**Difficulty:** Intermediate
**Explanation:** Differential loading improves performance by shipping optimized bundles based on browser capabilities.

---

**96. What command builds Angular in production mode?**
A. ng prod
B. ng build
C. ng build --prod
D. ng deploy
**Answer:** C
**Difficulty:** Basic
**Explanation:** `ng build --prod` enables optimizations like AOT, minification, and tree-shaking.

---

**97. How are services injected in functional guards or computed signals?**
A. Using constructor
B. Using @Injectable
C. Using inject()
D. With Injector class
**Answer:** C
**Difficulty:** Advanced
**Explanation:** `inject()` is used to get service instances in non-class contexts like functional guards or computed functions.

---

**98. How does Angular 19 reduce bundle size?**
A. Uses SWC for build
B. Prunes unused styles
C. Tree-shakes unused code and provides standalone APIs
D. Deletes node\_modules
**Answer:** C
**Difficulty:** Advanced
**Explanation:** Angular 19’s standalone APIs, Signals, and tree-shaking reduce bundle size.

---

**99. What’s the purpose of `NgOptimizedImage`?**
A. Optimize API responses
B. Minify CSS
C. Automatically resize and lazy-load images
D. Add animations
**Answer:** C
**Difficulty:** Intermediate
**Explanation:** `NgOptimizedImage` directive provides performance optimizations like lazy-loading and resizing.

---

**100. What are benefits of using standalone APIs in Angular 19?**
A. Simpler module management
B. Easier code splitting
C. Better testability
D. All of the above
**Answer:** D
**Difficulty:** Advanced
**Explanation:** Standalone APIs reduce boilerplate, enable better tree-shaking, and simplify testing and routing.

---






