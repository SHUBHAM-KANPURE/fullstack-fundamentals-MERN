# Full-Stack Fundamentals — MERN

Short, practical definitions for MERN and full-stack interviews. These notes focus on what a concept does and why it matters.

A practical collection of **fundamentals, core concepts, interview questions, and hands-on examples** focused on the MERN stack and related software engineering concepts.

This repository is created to strengthen my understanding of **how things work**, rather than simply memorizing interview answers.

## Goal

The main goal of this repository is to build strong fundamentals and improve my ability to:

* Understand concepts from first principles
* Explain technical concepts clearly in interviews
* Connect theory with real-world projects
* Practice concepts through small examples
* Prepare for Full-Stack / MERN interviews

## 1. JavaScript

### Variables, Scope, and Functions

- **`var`, `let`, `const`:** `var` is function-scoped; `let` and `const` are block-scoped. `let` allows reassignment, while `const` prevents reassignment of the variable binding (but does not freeze an object).
  > **Hinglish:** `var` function-scoped hota hai; `let` aur `const` block-scoped hote hain. `let` ko reassign kar sakte hain, `const` variable binding ko reassign nahi kar sakte. Lekin `const` object ke andar ki values ko automatically freeze nahi karta.

- **Scope:** Scope determines where a variable can be accessed.
  > **Hinglish:** Scope batata hai ki variable code ke kis area mein access ho sakta hai.
  
- **Lexical scope:** JavaScript determines variable access from where functions and blocks are written in the code.
  > **Hinglish:** Variable ka access is baat se decide hota hai ki code kahan likha gaya hai, function kahan call hua isse nahi.
  
- **Hoisting:** JavaScript processes declarations before executing the code. `var` is initialized to `undefined`; `let` and `const` cannot be accessed before their declaration because of the Temporal Dead Zone.
  > **Hinglish:** JavaScript code execute karne se pehle declarations ko process karta hai. `var` ki initial value `undefined` hoti hai; `let`/`const` ko declaration se pehle access nahi kar sakte, kyunki TDZ hota hai.
  
- **Closure:** A closure occurs when a function retains access to variables from its outer scope, even after that outer function has finished.
  > **Hinglish:** Jab inner function outer function ke variables ko yaad rakhta hai, outer function finish hone ke baad bhi, use closure kehte hain.
  
- **`this`:** The value of `this` usually depends on how a function is called. Arrow functions inherit `this` from their surrounding scope.
  > **Hinglish:** `this` ki value generally is baat par depend karti hai ki function kaise call hua. Arrow function apne surrounding scope ka `this` use karta hai.
  
- **Function:** A reusable block of code that can accept inputs and return a result.
  > **Hinglish:** Reusable code block jo input le sakta hai aur result return kar sakta hai.
  
- **Callback:** A function passed to another function to be called later or when an operation completes.
  > **Hinglish:** Aisa function jo kisi doosre function ko diya jaata hai taaki use baad mein call kiya ja sake.
  
- **Arrow function:** A shorter function syntax that does not have its own `this` or `arguments` and cannot be used as a constructor.
  > **Hinglish:** Function likhne ka short syntax. Iska apna `this` aur `arguments` nahi hota, aur ise constructor ki tarah use nahi kar sakte.
  
- **Prototype:** An object from which another object can inherit properties and methods through the prototype chain.
  > **Hinglish:** Ek object jahan se doosra object prototype chain ke through properties aur methods inherit kar sakta hai.
  
- **`==` vs `===`:** `==` may convert types before comparison; `===` compares without type conversion. Prefer `===` for predictable comparisons.
  > **Hinglish:** `==` comparison se pehle type conversion kar sakta hai; `===` type conversion ke bina compare karta hai. Predictable result ke liye `===` prefer karein.
  
- **`null` vs `undefined`:** `undefined` commonly means a value has not been assigned; `null` represents an intentionally empty value.
  > **Hinglish:** `undefined` ka matlab aam taur par value assign nahi hui; `null` ka matlab intentionally empty value.
  
- **Destructuring:** A syntax for extracting values from arrays or properties from objects into variables.
  > **Hinglish:** Array ya object se values nikaal kar variables mein rakhne ka short syntax.
  
- **Spread syntax:** `...` expands iterable items or object properties into a new array/object or function call.
  > **Hinglish:** Array/object ki values ko expand karke naya array/object ya function arguments banane mein use hota hai.
  
- **Rest parameters:** `...args` collects remaining function arguments into an array.
  > **Hinglish:** `...args` function ke remaining arguments ko ek array mein collect karta hai.
  
- **Pass by value:** JavaScript passes values to functions. For objects, the copied value is a reference to the same object, so mutations can be visible to the caller.
  > **Hinglish:** JavaScript values pass karta hai. Object ke case mein copied value same object ka reference hoti hai, isliye object ki mutation caller ko bhi dikh sakti hai.
  
- **Shallow copy:** Copies only the first level; nested objects are still shared references.
  > **Hinglish:** Sirf first level copy hota hai; nested objects ke references same reh sakte hain.
  
- **Deep copy:** Copies nested data too, so changes to the copy do not affect the original, subject to the copying method's supported data types.
  > **Hinglish:** Nested data bhi copy karta hai, taaki copy mein changes original ko affect na karein; supported data types copying method par depend karte hain.

### Arrays and Objects

- **`forEach()`:** Runs a callback for each array item and does not build a result array.
  > **Hinglish:** Har array item par callback chalata hai; result array create nahi karta.
  
- **`map()`:** Transforms each item and returns a new array of the same length.
  > **Hinglish:** Har item ko transform karke same length ka naya array return karta hai.
  
- **`filter()`:** Returns a new array containing items that pass a condition.
  > **Hinglish:** Condition pass karne wale items ka naya array return karta hai.
  
- **`reduce()`:** Combines array items into one accumulated result, such as a sum or grouped object.
  > **Hinglish:** Array ke items ko combine karke ek final result banata hai, jaise sum ya grouped object.
  
- **`find()`:** Returns the first item that matches a condition, or `undefined`.
  > **Hinglish:** Condition match karne wala pehla item deta hai; match na mile to `undefined`.
  
- **`some()`:** Returns `true` if at least one item passes a condition.
  > **Hinglish:** Kam se kam ek item condition pass kare to `true`.
  
- **`every()`:** Returns `true` only if all items pass a condition.
  > **Hinglish:** Sabhi items condition pass karein tabhi `true`.
  
- **`slice()` vs `splice()`:** `slice()` returns a selected portion without changing the original array; `splice()` adds/removes items in the original array.
  > **Hinglish:** `slice()` original array ko change kiye bina portion return karta hai; `splice()` original array mein items add/remove karta hai.
  
- **Mutable vs immutable methods:** Mutating methods change the original value; non-mutating methods return a result without changing it.
  > **Hinglish:** Mutable method original value change karta hai; non-mutating method original ko badle bina result deta hai.
  
- **Optional chaining (`?.`):** Safely accesses a nested property or method when an earlier value may be `null` or `undefined`.
  > **Hinglish:** Agar beech ki value `null` ya `undefined` ho to nested property access se error aane se bachata hai.
  
- **Nullish coalescing (`??`):** Uses a fallback only when the left side is `null` or `undefined`, unlike `||`, which also treats values such as `0` and `''` as false.
  > **Hinglish:** Fallback sirf `null`/`undefined` par deta hai. `||` `0` aur empty string ko bhi false maanta hai.
  
- **JSON:** A text format for exchanging structured data. `JSON.stringify()` converts supported JavaScript data to JSON text; `JSON.parse()` converts JSON text into a JavaScript value.
  > **Hinglish:** Structured data exchange karne ka text format. `JSON.stringify()` supported JS data ko JSON text banata hai; `JSON.parse()` JSON text ko JS value banata hai.

### Asynchronous JavaScript

- **Synchronous code:** Runs one step at a time; the next step waits for the current step to finish.
  > **Hinglish:** Ek step complete hota hai, phir next step execute hota hai.
  
- **Asynchronous code:** Lets an operation complete later so the program can continue other work while waiting. Waiting operation ke complete hone tak program doosra kaam kar sakta hai.
  > **Hinglish:**
  
- **Promise:** An object representing the eventual success or failure of an asynchronous operation. Its states are pending, fulfilled, or rejected.
  > **Hinglish:** Future mein complete hone wale async operation ki success ya failure represent karta hai. States: pending, fulfilled, rejected.
  
- **`async/await`:** Syntax for working with promises in a readable, sequential style. `await` pauses the async function, not the entire JavaScript thread.
  > **Hinglish:** Promise-based code ko readable banata hai. `await` async function ko pause karta hai, poore JavaScript thread ko nahi.
  
- **Event loop:** Coordinates queued callbacks with the call stack so JavaScript can handle asynchronous work.
  > **Hinglish:** Call stack aur queued callbacks ko coordinate karta hai, jisse async work handle hota hai.
  
- **Call stack:** Tracks the functions currently executing.
  > **Hinglish:** Abhi execute ho rahe functions ka record rakhta hai.
  
- **Microtask vs macrotask:** Promise handlers and `queueMicrotask()` use the microtask queue; timers and many I/O callbacks are scheduled through task queues. Microtasks are generally drained before the next task.
  > **Hinglish:** Promise callbacks microtask queue mein aate hain; timers aur kai I/O callbacks task queues se run hote hain. Aam taur par next task se pehle microtasks process hote hain.
  
- **`setTimeout()`:** Schedules a callback to run after at least the specified delay; it does not guarantee an exact execution time.
  > **Hinglish:** Diye gaye delay ke baad callback schedule karta hai; exact time par run hone ki guarantee nahi.
  
- **`Promise.all()`:** Fulfills when all input promises fulfill, and rejects as soon as one rejects.
  > **Hinglish:** Sabhi promises fulfill hon to fulfill hota hai; koi ek reject ho to reject ho jaata hai.
  
- **`Promise.allSettled()`:** Waits for every input promise to settle and reports each outcome.
  > **Hinglish:** Har promise ka settle hona wait karta hai aur har result ka status deta hai.
  
- **`Promise.race()`:** Settles with the first input promise that settles.
  > **Hinglish:** Jo promise sabse pehle settle hota hai, uske result se settle hota hai.
  
- **`Promise.any()`:** Fulfills with the first fulfilled promise; rejects with `AggregateError` if all reject.
  > **Hinglish:** Pehle fulfilled promise ka result deta hai; sab reject ho jaayein to `AggregateError`.
  
- **Error handling:** Use `try/catch` for synchronous errors and awaited promise failures, and `.catch()` for promise chains. Handle errors meaningfully instead of silently ignoring them.
  > **Hinglish:** `async/await` ke saath `try/catch`, promise chain ke saath `.catch()` use karein. Errors ko silently ignore na karein.
  
- **Debouncing:** Delays execution until calls stop for a chosen period; useful for search inputs.
  > **Hinglish:** Calls rukne ke kuch time baad function run karta hai; search input mein useful hai.
  
- **Throttling:** Limits a function to run at most once per time interval; useful for scroll or resize handlers.
  > **Hinglish:** Ek time interval mein function kitni baar run ho sakta hai, uski limit lagata hai; scroll/resize mein useful hai.
  
- **Currying:** Converts a function with multiple arguments into a sequence of functions that each take one or fewer arguments.
  > **Hinglish:** Multiple arguments lene wale function ko functions ki chain mein convert karna, jahan har function ek ya kam arguments leta hai.
  
- **`call`, `apply`, `bind`:** Set a regular function's `this`; `call` passes arguments separately, `apply` passes them as an array-like value, and `bind` returns a new bound function.
  > **Hinglish:** Regular function ka `this` set karte hain. `call` arguments separately leta hai, `apply` array-like input leta hai, `bind` naya bound function return karta hai.
  
- **Memory leak:** Memory remains occupied because something still references data that is no longer needed, such as forgotten timers, event listeners, or unbounded caches.
  > **Hinglish:** Jab unnecessary data ka reference reh jaata hai aur memory release nahi hoti, jaise forgotten timers, listeners ya unlimited cache.
  
- **Garbage collection:** The JavaScript engine reclaims memory used by objects that are no longer reachable.
  > **Hinglish:** JavaScript engine un objects ki memory free karta hai jo ab reachable nahi hain.
  
### Modules and Runtime

- **CommonJS vs ES Modules:** CommonJS uses `require()` and `module.exports`; ES Modules use `import` and `export`.
  > **Hinglish:** CommonJS mein `require()`/`module.exports`; ES Modules mein `import`/`export` use hota hai.
  
- **Strict mode:** Enables stricter JavaScript behavior and catches certain mistakes; class bodies and modules are strict by default.
  > **Hinglish:** JavaScript ke stricter rules enable karta hai aur kuch mistakes pakadta hai. Modules aur class bodies strict mode mein hote hain.
  
- **Type coercion:** Automatic or explicit conversion from one data type to another.
  > **Hinglish:** Ek data type ka doosre type mein automatic ya explicit conversion.
  
- **Event delegation:** Attaches one event handler to a parent and uses event bubbling to handle events from its children.
  > **Hinglish:** Parent par ek event handler laga kar bubbling ki help se child elements ke events handle karna.

## 2. React

- **Why React:** React lets developers describe UI from data/state and updates the DOM when that data changes.
- **Component:** A reusable unit of UI, commonly written as a function returning JSX.
- **JSX:** JavaScript syntax extension used to describe UI; build tools transform it into JavaScript calls.
- **Props:** Read-only inputs passed from a parent component to a child.
- **State:** Component-managed data; updating state can trigger a re-render.
- **Rendering:** React calls components to calculate what the UI should look like.
- **Re-rendering:** React recalculates a component's UI after relevant state, props, or context changes.
- **Virtual DOM:** A common term for React's in-memory representation of UI elements used during rendering and reconciliation.
- **Reconciliation:** React's process for comparing rendered trees and deciding what updates are needed.
- **Keys:** Stable identifiers that help React match list items between renders. Prefer unique, stable IDs over array indexes when items can change order.
- **Hooks:** Functions such as `useState` and `useEffect` that let function components use React features.
- **`useState`:** Stores component state and provides a setter that schedules an update.
- **`useEffect`:** Synchronizes a component with external systems, such as subscriptions, timers, or network-related effects. It is not needed for every calculation.
- **Effect dependencies:** Values that determine when an effect should re-run; include the reactive values used by the effect.
- **`useRef`:** Stores a mutable value that persists across renders without triggering a re-render when changed; often used for DOM references.
- **`useMemo`:** Caches a calculated value between renders while dependencies remain unchanged.
- **`useCallback`:** Caches a function reference between renders while dependencies remain unchanged.
- **`useContext`:** Reads a value provided by a matching React context.
- **Context API:** Shares values across a component tree without passing props through every intermediate component.
- **Custom Hook:** A reusable function whose name starts with `use` and which can combine React hooks and logic.
- **Controlled input:** A form element whose displayed value is driven by React state.
- **Uncontrolled input:** A form element that keeps its value in the DOM, commonly accessed using a ref.
- **Lifting state up:** Moving shared state to the closest common parent that needs to coordinate multiple children.
- **Prop drilling:** Passing props through intermediate components that do not themselves need the values.
- **Conditional rendering:** Showing different UI depending on a condition.
- **React Router:** A routing library commonly used to display different components for different client-side URLs.
- **Lazy loading / code splitting:** Loading a component or code chunk only when needed to reduce initial loading work.
- **Performance optimization:** Reduce unnecessary work using suitable component boundaries, stable keys, memoization when measured to help, and code splitting.
- **`React.memo`:** Skips rendering a component when its props are equal to the previous props, subject to its comparison behavior.
- **State management:** The approach used to store, update, and share application data, using local state, Context, or a library as complexity requires.
- **Error boundary:** A React component pattern that catches rendering errors in its descendant tree and displays fallback UI; it does not catch every kind of error, such as ordinary event-handler errors.
- **Strict Mode:** A development-only tool that helps reveal unsafe patterns and may intentionally re-run certain logic to expose side effects.

## 3. Node.js

- **Node.js:** A JavaScript runtime that uses the V8 engine and provides APIs for building server-side and other networked applications.
- **V8:** The JavaScript engine that parses and executes JavaScript, including JIT compilation.
- **libuv:** A library used by Node.js for the event loop and asynchronous I/O support, including a worker pool for certain operations.
- **Single-threaded model:** JavaScript callbacks usually run on one main thread per Node.js isolate, while some I/O and worker operations happen elsewhere.
- **Non-blocking I/O:** Starts I/O work without making the JavaScript thread wait synchronously for completion.
- **Event-driven architecture:** The program reacts to events by running registered handlers.
- **Concurrency vs parallelism:** Concurrency manages multiple tasks over overlapping time; parallelism executes tasks at the same time on multiple execution resources.
- **`process.nextTick()`:** Schedules a callback in Node's next-tick queue, which is processed before the event loop continues; excessive use can starve I/O.
- **`setImmediate()`:** Schedules a callback for the check phase of the event loop.
- **Timers:** `setTimeout()` and `setInterval()` schedule callbacks after delays; timing depends on event-loop activity.
- **Buffer:** Represents raw binary data, such as file contents or network packets.
- **Stream:** Processes data in chunks instead of loading the entire data set into memory.
- **Readable / Writable / Duplex / Transform streams:** Streams that read data, write data, do both, or transform data while passing it through.
- **EventEmitter:** A Node.js pattern/API for registering listeners and emitting named events.
- **Worker threads:** Run JavaScript in separate threads and are useful for CPU-intensive work.
- **Child process:** Starts another process to run a command or program.
- **Cluster:** Runs multiple Node.js processes that can share a server port, allowing use of multiple CPU cores.
- **Environment variables:** Configuration values supplied outside source code, often accessed through `process.env`.
- **Graceful shutdown:** Stops accepting new work, finishes or safely closes ongoing work, releases resources, and exits.
- **Background job:** Work performed outside the immediate request-response path, often through a queue or worker.
- **Node error handling:** Handle expected failures near the operation, propagate errors with context, and avoid leaving rejected promises unhandled.

## 4. Express.js

- **Express.js:** A minimal Node.js web framework for routing HTTP requests and building APIs.
- **Request/response lifecycle:** A request reaches the server, passes through middleware and route handlers, may access services or a database, and ends with a response.
- **Routing:** Maps an HTTP method and URL path to a handler.
- **Middleware:** A function that can inspect or modify the request/response, end the response, or pass control to the next middleware.
- **Controller:** Handles the HTTP layer, reads input, calls application logic, and returns a response.
- **Service layer:** Contains reusable business logic separated from HTTP handling.
- **Error-handling middleware:** Centralizes errors using the Express error middleware signature `(err, req, res, next)`.
- **Authentication middleware:** Verifies who the requester is, for example by validating a token.
- **Validation:** Checks that incoming data has the expected shape, types, and rules before business logic uses it.
- **REST API:** An HTTP API designed around resources and standard HTTP semantics.
- **CORS:** A browser security mechanism that controls which origins may read cross-origin responses.
- **Rate limiting:** Restricts how often a client can make requests within a time window.
- **API structure:** A maintainable separation of routes, controllers, services, models, middleware, and configuration.
- **Centralized error handling:** Converts errors into consistent responses and avoids repeating error-response logic in every route.
- **Joi / Zod:** Schema-validation libraries used to validate and sometimes transform request data.

## 5. MongoDB and Database Fundamentals

- **MongoDB:** A document-oriented NoSQL database that stores records as BSON documents inside collections.
- **Database / collection / document:** A database contains collections; a collection contains documents, broadly comparable to a table and its rows in a relational database.
- **`_id` / ObjectId:** Every MongoDB document has a unique `_id`; ObjectId is a common identifier type, but `_id` can use other supported types.
- **CRUD:** Create, Read, Update, and Delete operations on data.
- **Schema:** A description of the expected structure and rules for data. MongoDB is flexible, though validation can enforce a schema.
- **Index:** A data structure that helps MongoDB find matching records faster, at the cost of storage and write overhead.
- **Compound index:** An index containing multiple fields; field order affects which query patterns it supports.
- **Query optimization:** Improving query speed by examining filters, indexes, returned fields, sort operations, and execution plans.
- **`explain()`:** Shows how a database query is planned and executed, helping identify scans and index usage.
- **Aggregation pipeline:** A sequence of stages that filters, transforms, groups, joins, or summarizes documents.
- **`$lookup`:** An aggregation stage that joins matching documents from another collection.
- **Embedding vs referencing:** Embedding stores related data inside one document; referencing stores links/IDs to separate documents.
- **Transaction:** Groups multiple database operations so they succeed or fail together according to transaction guarantees.
- **Atomicity:** An operation is treated as all-or-nothing.
- **Pagination:** Returns a large result set in smaller portions, using approaches such as skip/limit or cursor-based pagination.
- **MongoDB vs SQL:** MongoDB stores flexible documents; relational databases store data in tables with defined relationships and strong relational query capabilities. Choose based on data shape and requirements.
- **Relationship:** A connection between records, such as one-to-one, one-to-many, or many-to-many.
- **Normalization:** Organizes relational data to reduce duplication and update anomalies.
- **ACID:** Atomicity, Consistency, Isolation, and Durability—properties associated with reliable transactions.
- **SQL basics:** Learn `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `WHERE`, `JOIN`, `GROUP BY`, and constraints.

## 6. Mongoose

- **Mongoose:** An ODM library that provides schemas, models, validation, middleware, and convenient MongoDB operations for Node.js.
- **Schema:** Defines document paths, types, defaults, validation, and other schema-level behavior.
- **Model:** A compiled interface based on a schema used to create, query, update, and delete documents.
- **Validation:** Checks document values against schema rules before saving or validating.
- **Middleware/hooks:** Functions that run before or after supported model/document/query operations.
- **`populate()`:** Replaces referenced IDs with matching documents from another collection.
- **`lean()`:** Returns plain JavaScript objects instead of full Mongoose documents, often reducing overhead for read-only queries.
- **`save()`:** Saves a document and runs applicable document validation and middleware.
- **`insertMany()`:** Inserts multiple documents; its validation and middleware behavior differs from saving documents individually.

## 7. HTTP, REST, APIs, and Web Fundamentals

- **HTTP request/response:** A client sends a method, URL, headers, and optionally a body; the server responds with a status code, headers, and optionally a body.
- **HTTP vs HTTPS:** HTTPS uses TLS to protect data in transit and authenticate the server.
- **GET:** Retrieves a representation and should not be used to perform a state-changing action.
- **POST:** Submits data for processing, often creating a resource or triggering an operation.
- **PUT:** Replaces a resource representation; it is generally intended to be idempotent.
- **PATCH:** Applies a partial update to a resource.
- **DELETE:** Requests removal of a resource and is defined as idempotent in HTTP semantics.
- **Status codes:** `2xx` indicates success, `3xx` redirection, `4xx` client/request issues, and `5xx` server errors.
- **Headers:** Metadata about a request or response, such as content type, authorization, or caching rules.
- **Request body:** Data sent with a request, commonly used with POST, PUT, or PATCH.
- **Query parameters:** Key-value data in the URL after `?`, often used for filtering, sorting, and pagination.
- **Path parameters:** Values embedded in the URL path that identify a resource, such as `/tasks/:id`.
- **Cookie:** Small data stored by a browser and sent to matching requests according to cookie rules.
- **Session:** Server-managed state associated with a client, often identified by a session cookie.
- **Webhook:** An HTTP request sent by one system to notify another system about an event.
- **JWT:** A token format that carries claims in a signed or otherwise protected structure; a signed JWT is not automatically encrypted.
- **Refresh token:** A longer-lived credential used to obtain new access tokens, with careful storage, expiry, and revocation rules.
- **Authentication vs authorization:** Authentication verifies identity; authorization decides what that identity is allowed to do.
- **CORS:** Controls browser access to cross-origin responses; it is not a replacement for API authentication or authorization.
- **CSRF:** An attack that tricks a browser into sending an unwanted authenticated request to a site.
- **XSS:** An attack where malicious script runs in a user's browser because untrusted content is handled unsafely.
- **Password hashing:** Converts a password into a one-way verifier using a password-hashing algorithm such as Argon2id or bcrypt, with salts and suitable cost settings.
- **API validation:** Verifies request fields, types, limits, and business rules before processing.
- **API versioning:** Allows an API to evolve while managing compatibility for existing clients.
- **Idempotency:** Repeating the same request has the same intended effect as performing it once. It is useful for safe retries.
- **REST:** An architectural style that emphasizes resources, representations, stateless interactions, and standard web semantics.
- **Why POST instead of GET to create data?** GET is intended for retrieval and may be cached or prefetched; POST is more suitable for submitting data that changes server state.

## 8. Authentication and Security

- **Role-Based Access Control (RBAC):** Grants permissions according to roles, such as admin, manager, or user.
- **Access token:** A credential sent with a request to access protected resources; keep its lifetime and storage appropriate to the threat model.
- **Secure token handling:** Validate signature, issuer/audience where applicable, expiry, and allowed algorithms; never trust decoded claims alone.
- **Least privilege:** Give users and services only the permissions they need.
- **Input sanitization / output encoding:** Validate inputs and safely encode output for its context to reduce injection and script risks.
- **Secrets management:** Keep API keys and credentials out of source control; use environment configuration or a secrets manager and rotate exposed secrets.
- **Security headers:** HTTP headers that enable browser protections, such as Content Security Policy and frame restrictions.
- **Defense in depth:** Use multiple complementary security controls rather than relying on one mechanism.

## 9. Git, Deployment, and Engineering

- **Git:** A version-control system that tracks code changes and supports branching and collaboration.
- **GitHub:** A hosting and collaboration platform for Git repositories.
- **Branch:** An independent line of development used to work on changes safely.
- **Merge conflict:** A situation where Git cannot automatically reconcile overlapping changes.
- **Environment variables:** External configuration values for settings that differ between environments; do not commit secrets.
- **Debugging:** Finding the cause of incorrect behavior by reproducing the issue, inspecting state, and testing hypotheses.
- **Logging:** Recording useful events and errors to understand system behavior; avoid logging passwords, tokens, or sensitive data.
- **Testing:** Checking that code behaves as expected; unit tests target small units, integration tests check collaborating parts, and end-to-end tests check complete flows.
- **Docker:** Packages an application and its dependencies into a container image for more consistent execution.
- **Nginx:** A web server and reverse proxy often used for TLS termination, static files, routing, and load balancing.
- **PM2:** A process manager commonly used to keep Node.js applications running and manage restarts/logs.
- **Linux basics:** Understand files, permissions, processes, environment variables, logs, and common shell commands.
- **Deployment:** Releasing an application into an environment where users or systems can access it.
- **CI/CD:** Automates steps such as building, testing, and delivering software changes.
- **Redis:** An in-memory data store commonly used for caching, counters, sessions, and queue-related workloads.
- **Queue:** Holds jobs for workers to process asynchronously, helping separate slow work from user requests.
- **Cron job:** A task scheduled to run at defined times or intervals.
- **Third-party API integration:** Connecting to an external service using its API, authentication, request format, and error/rate-limit rules.
- **Retry mechanism:** Repeats a failed operation under defined conditions; use bounded retries, backoff, and idempotency where appropriate.
- **Rate limit handling:** Respect provider limits, inspect retry instructions, and delay or queue requests when needed.
- **Observability:** Using logs, metrics, and traces to understand a system's internal state from its outputs.

## 10. AI and LLM Fundamentals

- **Artificial Intelligence (AI):** A broad field focused on systems that perform tasks associated with human intelligence.
- **Large Language Model (LLM):** A model trained on large amounts of text that predicts and generates token sequences and can perform many language tasks.
- **Prompt engineering:** Designing instructions and context to guide a model toward useful, constrained outputs.
- **Token:** A piece of text processed by a language model; tokens are not always whole words.
- **Context window:** The amount of input and output token context a model can handle in one interaction.
- **Tool/function calling:** A model emits a structured request for an application to call a tool; the application executes it and returns the result to the model.
- **Embedding:** A numerical vector representing semantic features of data, useful for similarity search and retrieval.
- **Vector database:** Stores vectors and supports similarity search, often with metadata filters.
- **RAG (Retrieval-Augmented Generation):** Retrieves relevant external information and supplies it to an LLM to improve grounded answers.
- **RAG flow:** Split documents into chunks, create embeddings, store them, retrieve relevant chunks for a query, and pass those chunks to the model with the question.
- **LangChain:** A framework with components for connecting models, prompts, retrievers, tools, and workflows.
- **AI agent:** A system that uses a model to select steps or tools toward a goal, usually within defined permissions and limits.
- **Conversation memory:** Stores selected past information so later turns can use it; memory should be relevant, controlled, and privacy-aware.
- **LLM API integration:** Sends structured prompts to a model provider, handles responses/errors/timeouts, and controls cost, privacy, and output validation.
- **Hallucination:** A model-generated claim that sounds plausible but is unsupported or incorrect.
- **Structured output:** Constraining a model response to a defined schema, then validating it before using it.
- **Temperature:** A generation parameter that influences output randomness; its exact effect depends on the model and API.
- **Evaluation:** Tests whether AI outputs meet quality, accuracy, safety, latency, and cost requirements.

## 11. System Design

- **Scalability:** A system's ability to handle increased traffic or data by adding resources or improving efficiency.
- **Vertical scaling:** Increasing the resources of one machine.
- **Horizontal scaling:** Adding more machines or application instances.
- **Caching:** Keeping frequently used data in a faster layer to reduce latency and load.
- **Cache invalidation:** Updating or expiring cached data when the source changes; it is difficult because stale data must be controlled.
- **Load balancing:** Distributes incoming requests across multiple servers or instances.
- **Queue-based processing:** Moves slow or retryable work to background workers instead of making the user wait for it.
- **Database scaling:** Improves database capacity through indexing, query tuning, replication, partitioning/sharding, or stronger hardware as appropriate.
- **Replication:** Maintains copies of data on multiple nodes for availability and read scaling, depending on configuration.
- **Sharding:** Splits data across multiple database servers based on a shard key.
- **API design:** Defines clear resource paths, methods, request/response formats, validation, errors, security, and compatibility.
- **Reliability:** The ability of a system to continue operating correctly over time, including during failures.
- **Availability:** The proportion of time a service is usable.
- **Latency vs throughput:** Latency is the time taken for an operation; throughput is the amount of work completed per unit of time.
- **Rate limiting:** Protects services by limiting request volume per client or key.
- **Basic design approach:** Clarify requirements, estimate load, define APIs and data models, sketch components and data flow, identify bottlenecks, and discuss failures and trade-offs.

## Interview Answer Formula

For any topic, prepare to answer in this order:

1. **What it is:** One clear sentence.
2. **Why it is used:** The problem it solves.
3. **How it works:** Two or three simple steps.
4. **Example:** A practical use from a project.
5. **Trade-off:** Mention a limitation or alternative when relevant.
