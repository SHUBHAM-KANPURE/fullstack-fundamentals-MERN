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
  > **Hinglish:** React state/data ke basis par UI describe karne deta hai aur data change hone par DOM update karta hai.
  
- **Component:** A reusable unit of UI, commonly written as a function returning JSX.
  > **Hinglish:** UI ka reusable part, jo commonly function ke form mein JSX return karta hai.
  
- **JSX:** JavaScript syntax extension used to describe UI; build tools transform it into JavaScript calls.
  > **Hinglish:** JavaScript mein UI likhne ka syntax; build tools ise JavaScript calls mein transform karte hain.
  
- **Props:** Read-only inputs passed from a parent component to a child.
  > **Hinglish:** Parent component se child ko milne wale read-only inputs.
  
- **State:** Component-managed data; updating state can trigger a re-render.
  > **Hinglish:** Component ka managed data; state update hone par re-render trigger ho sakta hai.
  
- **Rendering:** React calls components to calculate what the UI should look like.
  > **Hinglish:** React component ko call karke decide karta hai ki UI kaisi honi chahiye.
  
- **Re-rendering:** React recalculates a component's UI after relevant state, props, or context changes.
  > **Hinglish:** State, props ya context change hone par React component ka UI dobara calculate karta hai.
  
- **Virtual DOM:** A common term for React's in-memory representation of UI elements used during rendering and reconciliation.
  > **Hinglish:** UI elements ka in-memory representation, jise React rendering/reconciliation ke dauran use karta hai.
  
- **Reconciliation:** React's process for comparing rendered trees and deciding what updates are needed.
  > **Hinglish:** Purane aur naye rendered tree ko compare karke required UI updates decide karna.
- **Keys:** List items ko renders ke beech identify/match karne mein help karti hain. Items reorder ya delete ho sakte hain to stable unique ID use karein.
  
- **Keys:** Stable identifiers that help React match list items between renders. Prefer unique, stable IDs over array indexes when items can change order.
  > **Hinglish:**
  
- **Hooks:** Functions such as `useState` and `useEffect` that let function components use React features.
  > **Hinglish:** `useState`, `useEffect` jaise functions jo function components mein React features use karne dete hain.
  
- **`useState`:** Stores component state and provides a setter that schedules an update.
  > **Hinglish:** Component state store karta hai aur setter update schedule karta hai.
  
- **`useEffect`:** Synchronizes a component with external systems, such as subscriptions, timers, or network-related effects. It is not needed for every calculation.
  > **Hinglish:** Component ko external systems ke saath synchronize karne ke liye, jaise subscription ya timer. Har calculation ke liye effect ki zaroorat nahi hoti.
  
- **Effect dependencies:** Values that determine when an effect should re-run; include the reactive values used by the effect.
  > **Hinglish:** Ye decide karti hain ki effect kab dobara run hoga; effect mein use hone wali reactive values include karein.
  
- **`useRef`:** Stores a mutable value that persists across renders without triggering a re-render when changed; often used for DOM references.
  > **Hinglish:** Aisi value store karta hai jo renders ke beech persist karti hai; change hone par re-render trigger nahi hota.
  
- **`useMemo`:** Caches a calculated value between renders while dependencies remain unchanged.
  > **Hinglish:** Dependencies same rehne tak calculated value ko cache karta hai.
  
- **`useCallback`:** Caches a function reference between renders while dependencies remain unchanged.
  > **Hinglish:** Dependencies same rehne tak function reference ko cache karta hai.
  
- **`useContext`:** Reads a value provided by a matching React context.
  > **Hinglish:** React context se provided value read karta hai.
  
- **Context API:** Shares values across a component tree without passing props through every intermediate component.
  > **Hinglish:** Har intermediate component se props pass kiye bina component tree mein value share karna.
  
- **Custom Hook:** A reusable function whose name starts with `use` and which can combine React hooks and logic.
  > **Hinglish:** Reusable function jiska naam `use` se start hota hai aur jo React hooks/logic combine karta hai.
  
- **Controlled input:** A form element whose displayed value is driven by React state.
  > **Hinglish:** Input ki value React state control karti hai.
  
- **Uncontrolled input:** A form element that keeps its value in the DOM, commonly accessed using a ref.
  > **Hinglish:** Input apni value DOM mein rakhta hai; aksar ref se read karte hain.
  
- **Lifting state up:** Moving shared state to the closest common parent that needs to coordinate multiple children.
  > **Hinglish:** Shared state ko closest common parent mein move karna.
  
- **Prop drilling:** Passing props through intermediate components that do not themselves need the values.
  > **Hinglish:** Aise intermediate components se props pass karna jinhe khud un values ki zaroorat nahi.
  
- **Conditional rendering:** Showing different UI depending on a condition.
  > **Hinglish:** Condition ke basis par alag UI dikhana.
  
- **React Router:** A routing library commonly used to display different components for different client-side URLs.
  > **Hinglish:** URL ke basis par client-side pages/components show karne ke liye routing library.
  
- **Lazy loading / code splitting:** Loading a component or code chunk only when needed to reduce initial loading work.
  > **Hinglish:** Code ya component ko zaroorat padne par load karna, jisse initial load ka kaam kam ho.
  
- **Performance optimization:** Reduce unnecessary work using suitable component boundaries, stable keys, memoization when measured to help, and code splitting.
  > **Hinglish:** Unnecessary work kam karna; memoization tab use karein jab actual benefit ho.
  
- **`React.memo`:** Skips rendering a component when its props are equal to the previous props, subject to its comparison behavior.
  > **Hinglish:** Props same hone par component render skip kar sakta hai, comparison behavior ke hisaab se.
  
- **State management:** The approach used to store, update, and share application data, using local state, Context, or a library as complexity requires.
  > **Hinglish:** App data ko store/update/share karne ka approach—local state, Context ya library.
  
- **Error boundary:** A React component pattern that catches rendering errors in its descendant tree and displays fallback UI; it does not catch every kind of error, such as ordinary event-handler errors.
  > **Hinglish:** Descendant tree ke rendering errors pakad kar fallback UI dikhata hai; har type ka error catch nahi karta.
  
- **Strict Mode:** A development-only tool that helps reveal unsafe patterns and may intentionally re-run certain logic to expose side effects.
  > **Hinglish:** Development mein unsafe patterns detect karne mein help karta hai; kuch logic ko jaan-bujhkar dobara run karke side effects expose kar sakta hai.

## 3. Node.js

- **Node.js:** A JavaScript runtime that uses the V8 engine and provides APIs for building server-side and other networked applications.
  > **Hinglish:** V8 JavaScript engine aur server-side APIs par based runtime, jisse server/network applications bana sakte hain.
  
- **V8:** The JavaScript engine that parses and executes JavaScript, including JIT compilation.
  > **Hinglish:** JavaScript engine jo code parse aur execute karta hai.
  
- **libuv:** A library used by Node.js for the event loop and asynchronous I/O support, including a worker pool for certain operations.
  > **Hinglish:** Node.js mein event loop aur asynchronous I/O support dene wali library.
  
- **Single-threaded model:** JavaScript callbacks usually run on one main thread per Node.js isolate, while some I/O and worker operations happen elsewhere.
  > **Hinglish:** Ek Node.js isolate mein JavaScript callbacks aam taur par main thread par chalte hain; kuch I/O/worker operations alag resources use karte hain.
  
- **Non-blocking I/O:** Starts I/O work without making the JavaScript thread wait synchronously for completion.
  > **Hinglish:** I/O operation ka wait karne ke liye JavaScript thread ko synchronously rokna nahi padta.
  
- **Event-driven architecture:** The program reacts to events by running registered handlers.
  > **Hinglish:** Events hone par registered handlers execute hote hain.
  
- **Concurrency vs parallelism:** Concurrency manages multiple tasks over overlapping time; parallelism executes tasks at the same time on multiple execution resources.
  > **Hinglish:** Concurrency mein tasks ka progress overlapping time par manage hota hai; parallelism mein tasks same time par execute hote hain.
  
- **`process.nextTick()`:** Schedules a callback in Node's next-tick queue, which is processed before the event loop continues; excessive use can starve I/O.
  > **Hinglish:** Callback ko next-tick queue mein schedule karta hai, jo event loop continue hone se pehle process hoti hai. Bahut zyada use I/O ko starve kar sakta hai.
  
- **`setImmediate()`:** Schedules a callback for the check phase of the event loop.
  > **Hinglish:** Callback ko event loop ke check phase ke liye schedule karta hai.
  
- **Timers:** `setTimeout()` and `setInterval()` schedule callbacks after delays; timing depends on event-loop activity.
  > **Hinglish:** `setTimeout()` aur `setInterval()` delay ke baad callbacks schedule karte hain; exact timing event-loop load par depend karti hai.
  
- **Buffer:** Represents raw binary data, such as file contents or network packets.
  > **Hinglish:** Raw binary data, jaise file content ya network packets, represent karta hai.
  
- **Stream:** Processes data in chunks instead of loading the entire data set into memory.
  > **Hinglish:** Data ko chunks mein process karta hai, poora data memory mein load karna zaroori nahi.
  
- **Readable / Writable / Duplex / Transform streams:** Streams that read data, write data, do both, or transform data while passing it through.
  > **Hinglish:** Data read karna, write karna, dono karna, ya process karke aage pass karna.
  
- **EventEmitter:** A Node.js pattern/API for registering listeners and emitting named events.
  > **Hinglish:** Named events emit karne aur unke listeners register karne ka Node.js API/pattern.
  
- **Worker threads:** Run JavaScript in separate threads and are useful for CPU-intensive work.
  > **Hinglish:** Separate threads mein JavaScript chalate hain; CPU-heavy work ke liye useful.
  
- **Child process:** Starts another process to run a command or program.
  > **Hinglish:** Alag process mein command/program run karta hai.
  
- **Cluster:** Runs multiple Node.js processes that can share a server port, allowing use of multiple CPU cores.
  > **Hinglish:** Multiple Node.js processes run karta hai, jisse multiple CPU cores use kiye ja sakte hain.
  
- **Environment variables:** Configuration values supplied outside source code, often accessed through `process.env`.
  > **Hinglish:** Code ke bahar se configuration dene ka tareeka; Node mein `process.env` se access hoti hain.
  
- **Graceful shutdown:** Stops accepting new work, finishes or safely closes ongoing work, releases resources, and exits.
  > **Hinglish:** New requests rokna, ongoing work ko safely complete/close karna, resources release karna aur exit karna.
  
- **Background job:** Work performed outside the immediate request-response path, often through a queue or worker.
  > **Hinglish:** Aisa work jo immediate HTTP response ke baad worker/queue se process hota hai.
  
- **Node error handling:** Handle expected failures near the operation, propagate errors with context, and avoid leaving rejected promises unhandled.
  > **Hinglish:** Failure ko sahi jagah handle karein, useful context dein aur unhandled promise rejections se bachein.

## 4. Express.js

- **Express.js:** A minimal Node.js web framework for routing HTTP requests and building APIs.
  > **Hinglish:** Node.js ka minimal web framework jo HTTP routes aur APIs banane mein help karta hai.
  
- **Request/response lifecycle:** A request reaches the server, passes through middleware and route handlers, may access services or a database, and ends with a response.
  > **Hinglish:** Request server par aati hai, middleware/routes se pass hoti hai, business logic/database use ho sakta hai, phir response return hota hai.
  
- **Routing:** Maps an HTTP method and URL path to a handler.
  > **Hinglish:** HTTP method aur URL path ko handler ke saath map karna.
  
- **Middleware:** A function that can inspect or modify the request/response, end the response, or pass control to the next middleware.
  > **Hinglish:** Request/response inspect ya modify karta hai, response end karta hai, ya control next middleware ko deta hai.
  
- **Controller:** Handles the HTTP layer, reads input, calls application logic, and returns a response.
  > **Hinglish:** HTTP request ka input handle karta hai, business logic call karta hai aur response bhejta hai.
  
- **Service layer:** Contains reusable business logic separated from HTTP handling.
  > **Hinglish:** Reusable business logic ko HTTP handling se separate rakhti hai.
  
- **Error-handling middleware:** Centralizes errors using the Express error middleware signature `(err, req, res, next)`.
  > **Hinglish:** `(err, req, res, next)` signature se errors ko centrally handle karta hai.
  
- **Authentication middleware:** Verifies who the requester is, for example by validating a token.
  > **Hinglish:** Requester ki identity verify karta hai, jaise token validate karke.
  
- **Validation:** Checks that incoming data has the expected shape, types, and rules before business logic uses it.
  > **Hinglish:** Business logic se pehle request data ka shape, type aur rules check karna.
  
- **REST API:** An HTTP API designed around resources and standard HTTP semantics.
  > **Hinglish:** Resources aur standard HTTP semantics ke around designed API.
  
- **CORS:** A browser security mechanism that controls which origins may read cross-origin responses.
  > **Hinglish:** Browser ko control karta hai ki kaunse origins cross-origin response read kar sakte hain.
  
- **Rate limiting:** Restricts how often a client can make requests within a time window.
  > **Hinglish:** Ek time window mein client ki requests limit karna.
  
- **API structure:** A maintainable separation of routes, controllers, services, models, middleware, and configuration.
  > **Hinglish:** Routes, controllers, services, models, middleware aur config ko logically separate karna.
  
- **Centralized error handling:** Converts errors into consistent responses and avoids repeating error-response logic in every route.
  > **Hinglish:** Har route mein duplicate error response code likhne ke bajay common handler use karna.
  
- **Joi / Zod:** Schema-validation libraries used to validate and sometimes transform request data.
  > **Hinglish:** Schema-validation libraries jo request data validate aur kabhi-kabhi transform karti hain.

## 5. MongoDB and Database Fundamentals

- **MongoDB:** A document-oriented NoSQL database that stores records as BSON documents inside collections.
  > **Hinglish:** Document-oriented NoSQL database jo BSON documents ko collections mein store karta hai.
  
- **Database / collection / document:** A database contains collections; a collection contains documents, broadly comparable to a table and its rows in a relational database.
  > **Hinglish:** Database mein collections hoti hain aur collection mein documents. Roughly relational DB ke table/row se compare kar sakte hain.
  
- **`_id` / ObjectId:** Every MongoDB document has a unique `_id`; ObjectId is a common identifier type, but `_id` can use other supported types.
  > **Hinglish:** Har document ka unique `_id` hota hai. ObjectId common type hai, lekin `_id` doosre supported types ka bhi ho sakta hai.
  
- **CRUD:** Create, Read, Update, and Delete operations on data.
  > **Hinglish:** Create, Read, Update aur Delete operations.
  
- **Schema:** A description of the expected structure and rules for data. MongoDB is flexible, though validation can enforce a schema.
  > **Hinglish:** Data ka expected structure aur rules. MongoDB flexible hai, lekin validation se rules enforce kar sakte hain.
  
- **Index:** A data structure that helps MongoDB find matching records faster, at the cost of storage and write overhead.
  > **Hinglish:** Matching records ko faster find karne mein help karta hai, lekin extra storage aur write overhead hota hai.
  
- **Compound index:** An index containing multiple fields; field order affects which query patterns it supports.
  > **Hinglish:** Multiple fields ka index; field order query support ko affect karta hai.
  
- **Query optimization:** Improving query speed by examining filters, indexes, returned fields, sort operations, and execution plans.
  > **Hinglish:** Filters, indexes, returned fields, sorting aur execution plan improve karke query fast karna.
  
- **`explain()`:** Shows how a database query is planned and executed, helping identify scans and index usage.
  > **Hinglish:** Query ka execution plan dikhata hai, jisse scans aur index usage samajh sakte hain.
  
- **Aggregation pipeline:** A sequence of stages that filters, transforms, groups, joins, or summarizes documents.
  > **Hinglish:** Stages ki series jo documents filter, transform, group, join ya summarize karti hai.
  
- **`$lookup`:** An aggregation stage that joins matching documents from another collection.
  > **Hinglish:** Aggregation stage jo doosri collection se matching documents join karti hai.
  
- **Embedding vs referencing:** Embedding stores related data inside one document; referencing stores links/IDs to separate documents.
  > **Hinglish:** Embedding related data ko same document mein rakhta hai; referencing IDs ke through separate documents ko connect karta hai.
  
- **Transaction:** Groups multiple database operations so they succeed or fail together according to transaction guarantees.
  > **Hinglish:**  Multiple database operations ko ek group ki tarah treat karta hai, taaki transaction guarantees ke mutabik saath succeed/fail ho sakein.
  
- **Atomicity:** An operation is treated as all-or-nothing.
  > **Hinglish:** Operation all-or-nothing hota hai.
  
- **Pagination:** Returns a large result set in smaller portions, using approaches such as skip/limit or cursor-based pagination.
  > **Hinglish:** Large results ko chhote pages mein dena; skip/limit ya cursor-based approach use kar sakte hain.
  
- **MongoDB vs SQL:** MongoDB stores flexible documents; relational databases store data in tables with defined relationships and strong relational query capabilities. Choose based on data shape and requirements.
  > **Hinglish:** MongoDB flexible documents use karta hai; relational DB tables aur defined relationships use karta hai. Choice data aur requirements par depend karti hai.
  
- **Relationship:** A connection between records, such as one-to-one, one-to-many, or many-to-many.
  > **Hinglish:** Records ke beech connection, jaise one-to-one, one-to-many, many-to-many.
  
- **Normalization:** Organizes relational data to reduce duplication and update anomalies.
  > **Hinglish:** Relational data ko organize karna taaki duplication aur update problems kam hon.
  
- **ACID:** Atomicity, Consistency, Isolation, and Durability—properties associated with reliable transactions.
  > **Hinglish:** Atomicity, Consistency, Isolation, Durability—reliable transactions ki properties.
  
- **SQL basics:** Learn `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `WHERE`, `JOIN`, `GROUP BY`, and constraints.
  > **Hinglish:** `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `WHERE`, `JOIN`, `GROUP BY` aur constraints samjhein.

## 6. Mongoose

- **Mongoose:** An ODM library that provides schemas, models, validation, middleware, and convenient MongoDB operations for Node.js.
  > **Hinglish:** Node.js ODM library jo MongoDB ke liye schemas, models, validation, middleware aur convenient queries deti hai.
  
- **Schema:** Defines document paths, types, defaults, validation, and other schema-level behavior.
  > **Hinglish:** Document ke fields, types, defaults aur validation rules define karta hai.
  
- **Model:** A compiled interface based on a schema used to create, query, update, and delete documents.
  > **Hinglish:** Schema se bana interface jisse documents create, query, update aur delete karte hain.
  
- **Validation:** Checks document values against schema rules before saving or validating.
  > **Hinglish:** Save/validate se pehle values ko schema rules ke against check karta hai.
  
- **Middleware/hooks:** Functions that run before or after supported model/document/query operations.
  > **Hinglish:**  Supported document, model ya query operations se pehle/baad functions run karte hain.
  
- **`populate()`:** Replaces referenced IDs with matching documents from another collection.
  > **Hinglish:** Referenced IDs ko related collection ke documents se replace karta hai.
  
- **`lean()`:** Returns plain JavaScript objects instead of full Mongoose documents, often reducing overhead for read-only queries.
  > **Hinglish:** Full Mongoose documents ke bajay plain JavaScript objects return karta hai; read-only queries mein overhead kam ho sakta hai.
  
- **`save()`:** Saves a document and runs applicable document validation and middleware.
  > **Hinglish:** Document save karta hai aur applicable document validation/middleware chalata hai.
  
- **`insertMany()`:** Inserts multiple documents; its validation and middleware behavior differs from saving documents individually.
  > **Hinglish:** Multiple documents insert karta hai; validation aur middleware ka behavior individual `save()` se different hota hai.

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
