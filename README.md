# Full-Stack Fundamentals — MERN

A practical collection of **fundamentals, core concepts, interview questions, and hands-on examples** focused on the MERN stack and related software engineering concepts.

This repository is created to strengthen my understanding of **how things work**, rather than simply memorizing interview answers.

## Goal

The main goal of this repository is to build strong fundamentals and improve my ability to:

* Understand concepts from first principles
* Explain technical concepts clearly in interviews
* Connect theory with real-world projects
* Practice concepts through small examples
* Prepare for Full-Stack / MERN interviews

## Tech & Topics

### 1. Start with the foundation: JavaScript

This should be your #1 priority.

Before React or Node, make sure you can comfortably explain:

* `var`, `let`, `const`
* Scope and lexical scope
* Hoisting
* Closures
* this
* Functions and callbacks
* Arrow functions
* Objects and prototypes
* == vs ===
* null vs undefined
* Destructuring
* Spread/rest
* Array methods
* map, filter, reduce
* Promises
* async/await
* Event loop
* Microtask vs macrotask
* setTimeout
* Error handling
* Modules
* Memory and garbage collection

#### Don't just learn definitions.

For example, don't memorize:

“A closure is a function bundled with its lexical environment.”

You should be able to explain:

“A closure happens when an inner function remembers variables from the outer function even after the outer function has finished executing.”

Then give a tiny example.

That's the level interviewers are looking for.

### 2. Then build your React fundamentals

Once JS is strong:

#### React fundamentals → React internals → performance

* Why React exists
* Components
* Props & State
* Rendering & Re-rendering
* Virtual DOM
* Reconciliation
* Keys
* Hooks
* `useState`
* `useEffect`
* `useRef`
* `useMemo`
* `useCallback`
* Context API
* Forms
* Component communication
* API calls
* API Integration
* Error/loading states
* Routing
* Performance Optimization
* State management

The key question for every React topic should be:

#### “What problem does this solve?”

For example:

#### Don't learn:
`useMemo` = memoization.

#### Learn:
“When React renders, some calculations may be expensive. useMemo lets us reuse a previously calculated value until its dependencies change.”

That makes your answer much stronger.

### 3. Node.js

This is another area where interviewers can easily go beyond surface-level questions.

Study in this order:

#### JavaScript async → Node runtime → HTTP → Express → database

* What Node.js actually is
* V8
* libuv
* Event loop
* Non-blocking I/O
* Event-driven Architecture
* Single-threaded model
* Concurrency
* process.nextTick
* setImmediate
* Timers
* Streams & Buffers
* EventEmitter
* Worker threads
* Child processes
* Cluster
* Error handling
* Graceful shutdown
* Background Processing

### 4. Express.js

* Request/response lifecycle
* Routing
* Controllers
* Services
* Middleware
* Error middleware
* Authentication middleware
* Request/Response Lifecycle
* Error Handling
* Validation
* Authentication
* API Structure
* REST APIs
* CORS
* Rate limiting

You should eventually be able to answer:

#### “What happens from the moment a request reaches your Node server until the response is returned?”

That's a very valuable fundamentals question.

### 4. MongoDB & Mongoose + database fundamentals

Don't restrict yourself to:

“MongoDB is a NoSQL database.”

Understand **why and when** things work.

* Schema & Models
* Documents
* Collections
* _id / ObjectId
* CRUD Operations
* Indexes / Indexing
* Compound indexes
* Query optimization
* explain()
* Aggregation
* $lookup
* Embedding vs referencing
* Transactions
* Atomicity
* Pagination
* MongoDB vs SQL
* Basic SQL concepts
* Relationships
* Normalization
* ACID

#### Then connect it to Mongoose:

* Schema
* Model
* Validation
* Middleware
* populate
* lean
* save
* insertMany

### 5. HTTP + REST + security / API & Web Fundamentals

This is an area people often use every day but can't explain properly.

Build strong fundamentals around:

* HTTP request/response
* HTTP vs HTTPS
* HTTP Methods & Status Codes
* Headers
* Body
* Query parameters
* Path parameters
* HTTP methods
* Status codes
* Cookies
* Webhooks
* Sessions
* JWT
* Refresh tokens
* Authentication vs authorization
* CORS
* CSRF
* XSS
* HTTPS
* Password hashing
* API validation
* Rate limiting
* API versioning
* Idempotency

For example, you should be able to explain:

#### Why do we use POST instead of GET for creating data?

rather than simply memorizing:

“POST is used to create.”

### 6. Authentication & Security

* JWT
* Sessions
* Refresh Tokens
* Password Hashing
* Authentication vs Authorization
* RBAC
* XSS
* CSRF
* API Security

### 7. Then your real-world engineering fundamentals

This is where your 3 years of experience should start showing.

* Git & GitHub
* Environment Variables
* Debugging
* Logging
* Testing
* Error handling
* Docker Basics
* Nginx
* PM2
* Linux basics
* Deployment
* CI/CD basics
* Redis
* Queues/background jobs
* Cron jobs
* Webhooks
* Third-party API integration
* Retry mechanisms
* Rate limits

### 8. AI & LLM Fundamentals

* LLM Basics
* Prompt Engineering
* Tokens & Context Windows
* Function / Tool Calling
* Embeddings
* Vector Databases
* RAG
* LangChain
* AI Agents
* Conversation Memory
* LLM API Integration

### 9. System Design

* Scalability
* Caching
* Load Balancing
* Queues
* Database Scaling
* API Design
* Basic System Design Problems

## Learning Approach

For every topic, I aim to understand:

1. **What is it?**
2. **Why do we need it?**
3. **How does it work?**
4. **How can I implement it?**
5. **Where have I used it in a real project?**
6. **What are its alternatives or limitations?**

The focus is on **understanding and explaining**, not memorizing predefined interview answers.

## Interview Preparation

Each concept may contain:

```text
Concept
├── Explanation
├── Why it is needed
├── How it works
├── Example
├── Common interview questions
├── Practical use case
└── Common mistakes / follow-up questions
```

## Repository Structure

```text
fullstack-fundamentals-MERN/
│
├── javascript/
├── react/
├── node/
├── express/
├── mongodb/
├── mongoose/
├── api-rest/
├── authentication-security/
├── git/
├── deployment/
├── redis/
├── system-design/
├── ai-llm/
│
├── interview-questions/
├── coding-practice/
│
└── README.md
```

## Objective

> **Learn the fundamentals. Understand how things work. Practice them. Explain them clearly. Apply them in real projects.**

This repository is a continuous learning and interview-preparation resource for becoming a stronger **Full-Stack MERN Developer**.

---


# `Here are the answers to all the above questions.`

---

## Tech & Topics

### 1. JavaScript

#### Variables, Scope & Functions

* **`var`, `let`, `const`** — `var` is function-scoped and hoisted as `undefined`. `let` and `const` are block-scoped and live in the Temporal Dead Zone until declared. `const` prevents re-assignment, not mutation of objects.
  > **Hinglish:** `var` function-scoped hota hai aur `undefined` ke saath hoist hota hai. `let` aur `const` block-scoped hain aur declare hone se pehle TDZ mein rehte hain. `const` variable ko dobara assign nahi karne deta, lekin object ke andar ki values change ho sakti hain.

* **Scope and lexical scope** — Scope decides where a variable is accessible (global, function, block). Lexical scope means that is decided by where the code is *written*, not where it is called.
  > **Hinglish:** Scope batata hai ki variable kahan-kahan use ho sakta hai (global, function, block). Lexical scope ka matlab hai ki ye code *kahan likha hai* us se decide hota hai, kahan call hua us se nahi.

* **Hoisting** — Declarations are registered before code runs. Function declarations are fully hoisted, `var` is hoisted as `undefined`, and `let`/`const` are hoisted but unusable until declared (TDZ).
  > **Hinglish:** Code run hone se pehle declarations memory mein register ho jaate hain. Function declaration poora hoist hota hai, `var` `undefined` ban ke hoist hota hai, aur `let`/`const` hoist hote hain par declare hone tak use nahi kar sakte (TDZ).

* **Closures** — A closure happens when an inner function remembers variables from the outer function even after the outer function has finished executing.
  ```js
  function counter() {
    let count = 0;
    return () => ++count;
  }
  const inc = counter();
  inc(); // 1
  inc(); // 2
  ```
  > **Hinglish:** Closure tab banta hai jab inner function outer function ke variables ko yaad rakhta hai, bhale hi outer function ka execution khatam ho chuka ho. Upar `count` har call pe yaad rehta hai.

* **`this`** — `this` depends on *how* a function is called: object method → the object, plain call → `undefined` (strict mode) or global, `new` → the new instance, `call/apply/bind` → whatever you pass. Arrow functions don't have their own `this`.
  > **Hinglish:** `this` is baat pe depend karta hai ki function *kaise call hua*: object ka method ho to wo object, normal call ho to `undefined`/global, `new` ho to naya instance, `call/apply/bind` ho to jo aap pass karo. Arrow function ka apna `this` nahi hota.

* **Functions and callbacks** — Functions are first-class values, so they can be passed around. A callback is a function handed to another function to be called later (e.g., after a timer or request).
  > **Hinglish:** JS mein functions ek value ki tarah hote hain, isliye unhe kahin bhi pass kar sakte hain. Callback ek aisa function hai jo kisi dusre function ko diya jaata hai taaki wo baad mein (timer ya request ke baad) call kare.

* **Arrow functions** — Shorter syntax with no own `this`, `arguments`, or `prototype`, so they inherit `this` from the surrounding scope and can't be used as constructors.
  > **Hinglish:** Chhota syntax, aur inka apna `this`, `arguments`, `prototype` nahi hota. Ye `this` apne bahar wale scope se leti hain aur constructor ki tarah use nahi ho sakti.

#### Objects & Types

* **Objects and prototypes** — Every object has a hidden link to a prototype. If a property isn't found on the object, JS walks up the prototype chain. `class` is syntax sugar over this.
  > **Hinglish:** Har object ka ek hidden link hota hai prototype se. Agar property object mein nahi mili to JS prototype chain mein upar dhundhta hai. `class` bas isi ke upar ek aasaan syntax hai.

* **`==` vs `===`** — `==` converts types before comparing (`'1' == 1` is `true`). `===` compares value and type with no conversion. Prefer `===`.
  > **Hinglish:** `==` compare karne se pehle type convert kar deta hai (`'1' == 1` true hota hai). `===` value aur type dono check karta hai, koi conversion nahi. Hamesha `===` use karo.

* **`null` vs `undefined`** — `undefined` means "no value assigned yet". `null` means "intentionally empty".
  > **Hinglish:** `undefined` matlab abhi tak value assign hi nahi hui. `null` matlab hum ne jaan-bujh ke khaali rakha hai.

* **Destructuring** — Unpacks values from arrays/objects into variables: `const { name, age } = user;`
  > **Hinglish:** Array ya object ki values ko seedha alag-alag variables mein nikaal lena: `const { name, age } = user;`

* **Spread/rest** — `...` spreads an iterable/object into individual items (`[...a, ...b]`). In function parameters it *collects* the remaining arguments into an array (rest).
  > **Hinglish:** `...` spread mein array/object ko alag-alag items mein failata hai (`[...a, ...b]`). Function ke parameters mein ye bache hue arguments ko ek array mein *jama* karta hai (rest).

#### Array Methods

* **Array methods** — Built-in helpers like `forEach`, `find`, `some`, `every`, `includes`, `slice`, `splice`. Know which ones mutate (`splice`, `sort`, `push`) and which return new arrays (`map`, `filter`, `slice`).
  > **Hinglish:** `forEach`, `find`, `some`, `every`, `includes`, `slice`, `splice` jaise built-in helpers. Ye yaad rakho kaun original array badalta hai (`splice`, `sort`, `push`) aur kaun naya array deta hai (`map`, `filter`, `slice`).

* **`map`** — Transforms every item and returns a new array of the same length.
  > **Hinglish:** Har item ko badal kar ek naya array deta hai, jiski length same hoti hai.

* **`filter`** — Returns a new array with only items that pass a test.
  > **Hinglish:** Sirf wahi items ka naya array deta hai jo condition pass karte hain.

* **`reduce`** — Folds an array into a single value using an accumulator (sum, object, grouped data, etc.).
  > **Hinglish:** Poore array ko ek single value mein badal deta hai accumulator ki madad se (sum, object, grouping wagairah).

#### Async JavaScript

* **Promises** — An object representing a value that will be available later. It is `pending`, then either `fulfilled` or `rejected`. Handled with `.then()` / `.catch()`.
  > **Hinglish:** Promise ek aisa object hai jo future mein milne wali value ko represent karta hai. Pehle `pending`, phir `fulfilled` ya `rejected`. `.then()` / `.catch()` se handle karte hain.

* **`async/await`** — Syntax over promises that makes async code read like sync code. `await` pauses *that function* (not the thread) until the promise settles.
  > **Hinglish:** Promises ke upar ka syntax jo async code ko sync jaisa dikhata hai. `await` sirf *us function* ko rokta hai, poore thread ko nahi, jab tak promise settle na ho jaye.

* **Event loop** — JS runs on one thread. The event loop continuously checks: if the call stack is empty, take the next queued callback and run it. This is how async works without blocking.
  > **Hinglish:** JS ek hi thread pe chalta hai. Event loop lagatar check karta hai: agar call stack khaali hai to queue se agla callback uthao aur chalao. Isi se bina block kiye async kaam hota hai.

* **Microtask vs macrotask** — Microtasks (promise callbacks, `queueMicrotask`) run right after the current task and *before* the next macrotask. Macrotasks are things like `setTimeout`, I/O, and UI events.
  ```js
  setTimeout(() => console.log('timeout'), 0);
  Promise.resolve().then(() => console.log('promise'));
  // promise, then timeout
  ```
  > **Hinglish:** Microtasks (promise callbacks) current task ke turant baad aur agle macrotask se *pehle* chalte hain. Macrotasks mein `setTimeout`, I/O, UI events aate hain. Isliye upar pehle `promise` print hota hai, phir `timeout`.

* **`setTimeout`** — Schedules a callback after *at least* the given delay. It's a minimum, not a guarantee, because the callback must wait for the call stack to be free.
  > **Hinglish:** Callback ko *kam se kam* diye gaye delay ke baad chalata hai. Ye guarantee nahi hai, kyunki call stack khaali hone ka intezaar karna padta hai.

* **Error handling** — Use `try/catch` (with `async/await`), `.catch()` on promises, and global handlers (`unhandledRejection`) as a safety net. Never swallow errors silently.
  > **Hinglish:** `async/await` ke saath `try/catch`, promises pe `.catch()`, aur safety ke liye global handlers (`unhandledRejection`). Errors ko chup-chap ignore kabhi mat karo.

#### Modules & Memory

* **Modules** — Split code into files with their own scope. CommonJS uses `require/module.exports` (sync, Node default historically); ES Modules use `import/export` (static, standard).
  > **Hinglish:** Code ko alag files mein todna, jinka apna scope hota hai. CommonJS mein `require/module.exports` (sync) use hota hai; ES Modules mein `import/export` (standard, static).

* **Memory and garbage collection** — JS automatically frees memory for objects that are no longer reachable (mark-and-sweep). Memory leaks happen when you keep references alive: forgotten timers, listeners, globals, or large caches.
  > **Hinglish:** Jo objects ab kahin se reachable nahi hain, JS unki memory khud free kar deta hai (mark-and-sweep). Memory leak tab hota hai jab references zinda rehte hain: bhule hue timers, listeners, globals ya bade caches.

#### Don't just learn definitions.

For example, don't memorize:

“A closure is a function bundled with its lexical environment.”

You should be able to explain:

“A closure happens when an inner function remembers variables from the outer function even after the outer function has finished executing.”

Then give a tiny example.

That's the level interviewers are looking for.

---

### 2. Then build your React fundamentals

Once JS is strong:

#### React fundamentals → React internals → performance

* **Why React exists** — To build UIs as a function of state. Instead of manually updating the DOM, you describe what the UI should look like and React updates the DOM efficiently.
  > **Hinglish:** UI ko state ke function ki tarah banane ke liye. DOM ko haath se update karne ke bajay aap batate ho UI kaisa dikhna chahiye, aur React DOM ko efficiently update kar deta hai.

* **Components** — Reusable, independent pieces of UI written as functions that return JSX.
  > **Hinglish:** UI ke reusable, independent tukde, jo functions hote hain aur JSX return karte hain.

* **Props & State** — Props are read-only inputs passed from parent to child. State is data owned by a component that, when changed, triggers a re-render.
  > **Hinglish:** Props parent se child ko diye gaye read-only inputs hain. State component ka apna data hai, jiske badalne par re-render hota hai.

* **Rendering & Re-rendering** — Rendering means React calls your component to figure out the UI. A re-render happens when state/props/context change, and by default re-renders its children too.
  > **Hinglish:** Rendering matlab React aapka component call karke UI nikalta hai. State/props/context badalne par re-render hota hai, aur default mein uske children bhi re-render hote hain.

* **Virtual DOM** — A lightweight JS representation of the UI. React compares the new tree with the old one and only applies the differences to the real DOM.
  > **Hinglish:** UI ki ek halki JS copy. React naye aur purane tree ko compare karta hai aur sirf jo difference hai wahi real DOM mein lagata hai.

* **Reconciliation** — The diffing process React uses to decide what changed. It assumes different element types produce different trees and uses `key`s to match list items.
  > **Hinglish:** Wo diffing process jisse React decide karta hai ki kya badla. Alag element type matlab alag tree, aur list items ko match karne ke liye `key` use hoti hai.

* **Keys** — Stable, unique identifiers for list items so React can track which item changed, moved, or was removed. Avoid using array index when the list can reorder.
  > **Hinglish:** List items ki stable, unique pehchaan, taaki React track kar sake kaun sa item badla, hila ya hata. Agar list reorder ho sakti hai to array index as key mat use karo.

* **Hooks** — Functions (`use...`) that let function components use state, lifecycle, and other React features. Must be called at the top level, not inside conditions or loops.
  > **Hinglish:** `use...` wale functions jo function components ko state, lifecycle jaisi features dete hain. Inhe hamesha top level pe call karo, if/loop ke andar nahi.

* **`useState`** — Adds a piece of state to a component. Calling the setter schedules a re-render with the new value.
  > **Hinglish:** Component mein state add karta hai. Setter call karne par nayi value ke saath re-render schedule hota hai.

* **`useEffect`** — Runs side effects (API calls, subscriptions, timers) *after* render. The dependency array controls when it re-runs, and the cleanup function runs before the next effect/unmount.
  > **Hinglish:** Render ke *baad* side effects chalata hai (API call, subscription, timer). Dependency array decide karta hai ye kab dobara chalega, aur cleanup function agle effect/unmount se pehle chalta hai.

* **`useRef`** — Holds a mutable value that persists across renders without causing a re-render. Also used to access DOM elements.
  > **Hinglish:** Ek aisi value rakhta hai jo renders ke beech bani rehti hai aur badalne par re-render nahi hota. DOM element ko access karne ke liye bhi use hota hai.

* **`useMemo`** — When React renders, some calculations may be expensive. `useMemo` lets us reuse a previously calculated value until its dependencies change.
  > **Hinglish:** Render ke time kuch calculations heavy ho sakti hain. `useMemo` purani calculate ki hui value ko tab tak reuse karta hai jab tak dependencies na badlein.

* **`useCallback`** — Returns the same function reference between renders until dependencies change. Useful when passing callbacks to memoized children (`React.memo`).
  > **Hinglish:** Dependencies na badlein to har render mein same function reference deta hai. `React.memo` wale child components ko callback dete waqt kaam aata hai.

* **Context API** — Lets you share data (theme, user, auth) with deeply nested components without prop drilling. All consumers re-render when the context value changes.
  > **Hinglish:** Data (theme, user, auth) ko gehre nested components tak bina prop drilling ke pahunchata hai. Context value badalne par saare consumers re-render hote hain.

* **Forms** — *Controlled*: React state drives input values (`value` + `onChange`). *Uncontrolled*: the DOM keeps the value and you read it via `ref`.
  > **Hinglish:** *Controlled*: input ki value React state se control hoti hai (`value` + `onChange`). *Uncontrolled*: value DOM ke paas rehti hai aur aap `ref` se padhte ho.

* **Component communication** — Parent → child via props; child → parent via callback props; siblings via lifting state up; distant components via Context or a state library.
  > **Hinglish:** Parent → child props se; child → parent callback props se; siblings ke beech state ko upar le jaake (lifting state up); door ke components ke liye Context ya state library.

* **API calls** — Usually made in `useEffect` (or a data library like React Query) using `fetch`/`axios`, then stored in state.
  > **Hinglish:** Aam taur par `useEffect` (ya React Query jaisi library) mein `fetch`/`axios` se call karte hain aur response state mein rakhte hain.

* **API Integration** — Centralize requests in a service layer, handle auth headers, base URLs, and errors in one place instead of scattering calls in components.
  > **Hinglish:** API calls ko components mein bikherne ke bajay ek service layer mein rakho, jahan auth headers, base URL aur errors ek hi jagah handle hon.

* **Error/loading states** — Every async UI has three states: loading, error, success. Always render something sensible for each. Error Boundaries catch render-time errors.
  > **Hinglish:** Har async UI ke teen states hote hain: loading, error, success. Teeno ke liye kuch sahi dikhana zaroori hai. Error Boundary render ke time hone wale errors pakadta hai.

* **Routing** — Maps URLs to components on the client side (React Router) without full page reloads. Supports nested routes, params, and protected routes.
  > **Hinglish:** Client side pe URL ko components se map karta hai (React Router) bina poora page reload kiye. Nested routes, params aur protected routes support karta hai.

* **Performance Optimization** — Avoid unnecessary re-renders (`React.memo`, `useMemo`, `useCallback`), split code (`lazy`/`Suspense`), virtualize long lists, and keep state as local as possible.
  > **Hinglish:** Faltu re-renders rokna (`React.memo`, `useMemo`, `useCallback`), code splitting (`lazy`/`Suspense`), lambi lists ko virtualize karna, aur state ko jitna ho sake local rakhna.

* **State management** — Local state first. Use Context for light global state, and Redux/Zustand/React Query for complex or server state.
  > **Hinglish:** Pehle local state. Halke global state ke liye Context, aur complex ya server state ke liye Redux/Zustand/React Query.

The key question for every React topic should be:

#### “What problem does this solve?”

For example:

#### Don't learn:
`useMemo` = memoization.

#### Learn:
“When React renders, some calculations may be expensive. useMemo lets us reuse a previously calculated value until its dependencies change.”

That makes your answer much stronger.

---

### 3. Node.js

This is another area where interviewers can easily go beyond surface-level questions.

Study in this order:

#### JavaScript async → Node runtime → HTTP → Express → database

* **What Node.js actually is** — A JavaScript runtime built on V8 that lets JS run outside the browser, with APIs for files, network, and processes.
  > **Hinglish:** V8 pe bana ek JavaScript runtime jo JS ko browser ke bahar chalne deta hai, aur files, network, processes ke APIs deta hai.

* **V8** — Google's JS engine that compiles JavaScript to machine code. It executes your code.
  > **Hinglish:** Google ka JS engine jo JavaScript ko machine code mein compile karke aapka code chalata hai.

* **libuv** — The C library that provides the event loop, thread pool, and async I/O (files, DNS, network) to Node.
  > **Hinglish:** Ek C library jo Node ko event loop, thread pool aur async I/O (files, DNS, network) deti hai.

* **Event loop** — Node's loop with phases (timers → pending callbacks → poll → check → close). It picks up completed async work and runs its callbacks one at a time.
  > **Hinglish:** Node ka loop jo phases mein chalta hai (timers → pending callbacks → poll → check → close). Ye complete ho chuke async kaam ke callbacks ek-ek karke chalata hai.

* **Non-blocking I/O** — Node starts an I/O operation and moves on; a callback/promise is triggered when it finishes, so one thread can serve many requests.
  > **Hinglish:** Node I/O kaam shuru karke aage badh jaata hai; kaam khatam hone par callback/promise chalta hai. Isliye ek thread bahut saari requests serve kar leta hai.

* **Event-driven architecture** — Code reacts to events (request received, file read, timer fired) using listeners/callbacks.
  > **Hinglish:** Code events (request aayi, file padhi gayi, timer baja) pe listeners/callbacks ke through react karta hai.

* **Single-threaded model** — Your JS runs on one main thread. It's great for I/O-heavy work but CPU-heavy tasks will block everything.
  > **Hinglish:** Aapka JS ek main thread pe chalta hai. I/O wale kaam ke liye badhiya hai, lekin CPU-heavy kaam sab kuch block kar dega.

* **Concurrency** — Many tasks are *in progress* at once (waiting on I/O), even though only one JS statement runs at a time. It's not the same as parallelism.
  > **Hinglish:** Kai tasks ek saath *chal rahe* hote hain (I/O ka wait karte hue), bhale hi ek time pe ek hi JS statement chale. Ye parallelism se alag cheez hai.

* **`process.nextTick`** — Queues a callback to run right after the current operation, before promises and before the event loop continues. Overuse can starve I/O.
  > **Hinglish:** Callback ko current operation ke turant baad chalata hai, promises aur event loop ke aage badhne se pehle. Zyada use kiya to I/O ko chalne ka mauka nahi milta.

* **`setImmediate`** — Runs a callback in the "check" phase, right after the poll (I/O) phase. Inside an I/O callback it always runs before `setTimeout(…, 0)`.
  > **Hinglish:** Callback ko "check" phase mein chalata hai, poll (I/O) phase ke theek baad. I/O callback ke andar ye hamesha `setTimeout(…, 0)` se pehle chalta hai.

* **Timers** — `setTimeout`/`setInterval` run in the timers phase; delay is a minimum, not exact.
  > **Hinglish:** `setTimeout`/`setInterval` timers phase mein chalte hain; delay kam se kam hota hai, exact nahi.

* **Streams & Buffers** — A buffer is a chunk of raw binary data. A stream processes data piece by piece (read, write, transform) so large files don't need to fit in memory.
  > **Hinglish:** Buffer raw binary data ka ek tukda hota hai. Stream data ko tukdon mein process karta hai (read, write, transform), isliye bade files poore memory mein load nahi karne padte.

* **EventEmitter** — Core class for the publish/subscribe pattern: `emitter.on('event', fn)` and `emitter.emit('event')`. Many Node APIs (streams, HTTP) are built on it.
  > **Hinglish:** Publish/subscribe pattern ki core class: `emitter.on('event', fn)` se suno aur `emitter.emit('event')` se event bhejo. Streams, HTTP jaise kai Node APIs isi pe bane hain.

* **Worker threads** — Run JS in separate threads with their own V8 instance, for CPU-heavy work (image processing, hashing) without blocking the main thread.
  > **Hinglish:** Alag threads mein JS chalate hain (apne V8 instance ke saath), taaki CPU-heavy kaam (image processing, hashing) main thread ko block na kare.

* **Child processes** — Spawn separate OS processes (`spawn`, `fork`, `exec`) to run other programs or Node scripts, communicating via IPC/streams.
  > **Hinglish:** Alag OS processes banate hain (`spawn`, `fork`, `exec`) dusre programs ya Node scripts chalane ke liye, aur IPC/streams se baat karte hain.

* **Cluster** — Starts multiple Node processes (one per CPU core) sharing the same port so you can use all cores. PM2 does this for you.
  > **Hinglish:** Kai Node processes (har CPU core ke liye ek) shuru karta hai jo same port share karte hain, taaki saare cores use ho sakein. PM2 ye aapke liye kar deta hai.

* **Error handling** — Handle sync errors with `try/catch`, async errors with `.catch`/`try-await`, and listen to `uncaughtException`/`unhandledRejection` only to log and exit cleanly.
  > **Hinglish:** Sync errors ke liye `try/catch`, async errors ke liye `.catch`/`try-await`, aur `uncaughtException`/`unhandledRejection` sirf log karke saaf tareeke se exit karne ke liye.

* **Graceful shutdown** — On `SIGTERM`/`SIGINT`: stop accepting new requests, finish in-flight ones, close DB/queue connections, then exit.
  > **Hinglish:** `SIGTERM`/`SIGINT` aane par: nayi requests lena band karo, chal rahi requests poori karo, DB/queue connections band karo, phir exit karo.

* **Background Processing** — Move slow or non-critical work (emails, reports, image processing) out of the request cycle using queues (BullMQ), workers, or cron jobs.
  > **Hinglish:** Dheere ya kam zaroori kaam (email, reports, image processing) ko request ke bahar queues (BullMQ), workers ya cron jobs se chalao.

---

### 4. Express.js

* **Request/response lifecycle** — Request arrives → passes through middleware in order → matched route handler → response is sent (or an error goes to error middleware).
  > **Hinglish:** Request aati hai → middleware se order mein guzarti hai → matching route handler chalta hai → response bheja jaata hai (ya error, error middleware ke paas jaata hai).

* **Routing** — Matching HTTP method + URL path to a handler: `app.get('/users/:id', handler)`. Use `express.Router()` to group routes.
  > **Hinglish:** HTTP method + URL path ko ek handler se match karna: `app.get('/users/:id', handler)`. Routes ko group karne ke liye `express.Router()` use karo.

* **Controllers** — Functions that handle the request/response: read input, call a service, return a response. They shouldn't contain heavy business logic.
  > **Hinglish:** Ye functions request/response sambhalte hain: input padho, service call karo, response return karo. Inme bhaari business logic nahi hona chahiye.

* **Services** — Hold the business logic and database calls. Keeps controllers thin and logic reusable and testable.
  > **Hinglish:** Business logic aur database calls yahan rehte hain. Isse controllers patle rehte hain aur logic reusable aur testable banta hai.

* **Middleware** — A function `(req, res, next)` that can read/modify the request or response, end the cycle, or call `next()` to continue.
  > **Hinglish:** `(req, res, next)` wala function jo request/response padh ya badal sakta hai, cycle ko khatam kar sakta hai, ya `next()` call karke aage bhej sakta hai.

* **Error middleware** — A middleware with four args `(err, req, res, next)` placed *last*. Centralizes error responses and logging.
  > **Hinglish:** Chaar arguments wala middleware `(err, req, res, next)` jo *sabse last* mein lagta hai. Saare error responses aur logging ek jagah handle karta hai.

* **Authentication middleware** — Verifies the token/session before the route runs, attaches the user to `req.user`, and rejects with `401` if invalid.
  > **Hinglish:** Route chalne se pehle token/session verify karta hai, user ko `req.user` mein daalta hai, aur invalid ho to `401` return karta hai.

* **Error Handling** — Pass errors via `next(err)`, wrap async handlers (Express 5 handles promise rejections automatically), and return consistent error shapes.
  > **Hinglish:** Errors ko `next(err)` se pass karo, async handlers ko wrap karo (Express 5 promise rejections khud handle karta hai), aur error ka format hamesha ek jaisa rakho.

* **Validation** — Never trust client input. Validate body/query/params with libraries like Joi, Zod, or express-validator before using them.
  > **Hinglish:** Client ke input pe kabhi bharosa mat karo. Body/query/params ko Joi, Zod ya express-validator se use karne se pehle validate karo.

* **Authentication** — Confirming who the user is (login via JWT or session) and protecting routes with middleware.
  > **Hinglish:** Ye confirm karna ki user kaun hai (JWT ya session se login) aur middleware se routes ko protect karna.

* **API Structure** — Common layering: `routes → controllers → services → models`, plus `middlewares`, `utils`, and `config`.
  > **Hinglish:** Aam layering: `routes → controllers → services → models`, saath mein `middlewares`, `utils` aur `config`.

* **REST APIs** — Resources are URLs (`/users/1`), actions are HTTP methods (GET/POST/PUT/PATCH/DELETE), stateless, with proper status codes and JSON responses.
  > **Hinglish:** Resources URLs hote hain (`/users/1`), actions HTTP methods (GET/POST/PUT/PATCH/DELETE), server stateless hota hai, aur sahi status codes ke saath JSON response milta hai.

* **CORS** — A browser security rule that blocks cross-origin requests unless the server allows them via headers. Configure it with the `cors` package using specific allowed origins.
  > **Hinglish:** Browser ka security rule jo cross-origin requests ko block karta hai jab tak server headers se allow na kare. `cors` package mein sirf specific origins allow karo.

* **Rate limiting** — Restricts how many requests a client can make in a time window (`express-rate-limit`) to prevent abuse and brute-force attacks.
  > **Hinglish:** Ek time window mein client kitni requests kar sakta hai ye limit karta hai (`express-rate-limit`), taaki abuse aur brute-force attacks rukein.

You should eventually be able to answer:

#### “What happens from the moment a request reaches your Node server until the response is returned?”

**Short answer:** The client sends an HTTP request over TCP (TLS if HTTPS) → Node's `http` server receives it via libuv and creates `req`/`res` objects → Express runs global middleware in order (logging, CORS, body parser, auth) → the router matches the method + path → the controller/service runs (possibly awaiting DB or API calls without blocking the event loop) → the handler sends the response (`res.json`) → if anything throws, `next(err)` goes to the error middleware → the response travels back to the client.

> **Hinglish:** Client TCP pe HTTP request bhejta hai (HTTPS ho to TLS ke saath) → Node ka `http` server libuv ke through use receive karke `req`/`res` objects banata hai → Express global middleware order mein chalata hai (logging, CORS, body parser, auth) → router method + path match karta hai → controller/service chalta hai (DB ya API ka `await` event loop ko block nahi karta) → handler `res.json` se response bhejta hai → agar kuch fail hua to `next(err)` error middleware ke paas jaata hai → response wapas client tak pahunch jaata hai.

That's a very valuable fundamentals question.

---

### 5. MongoDB & Mongoose + database fundamentals

Don't restrict yourself to:

“MongoDB is a NoSQL database.”

Understand **why and when** things work.

#### MongoDB

* **Schema & Models** — A schema defines the shape and rules of a document; a model is the class you use to query a collection. MongoDB itself is flexible, Mongoose adds structure.
  > **Hinglish:** Schema document ka shape aur rules batata hai; model wo class hai jisse collection pe query karte hain. MongoDB khud flexible hai, Mongoose structure add karta hai.

* **Documents** — A record stored as BSON (JSON-like), which can have nested objects and arrays.
  > **Hinglish:** BSON (JSON jaisa) format mein stored ek record, jisme nested objects aur arrays ho sakte hain.

* **Collections** — A group of documents, similar to a table in SQL but without a fixed schema.
  > **Hinglish:** Documents ka group, SQL ke table jaisa, par fixed schema ke bina.

* **`_id` / ObjectId** — Unique identifier automatically added to each document. A 12-byte value containing a timestamp, random value, and counter.
  > **Hinglish:** Har document mein apne aap add hone wali unique ID. 12-byte ki value jisme timestamp, random value aur counter hota hai.

* **CRUD Operations** — Create (`insertOne/insertMany`), Read (`find/findOne`), Update (`updateOne/updateMany`), Delete (`deleteOne/deleteMany`).
  > **Hinglish:** Create (`insertOne/insertMany`), Read (`find/findOne`), Update (`updateOne/updateMany`), Delete (`deleteOne/deleteMany`).

* **Indexes / Indexing** — Data structures (B-trees) that make queries fast by avoiding a full collection scan. They cost extra storage and slow down writes.
  > **Hinglish:** B-tree jaisi data structures jo poore collection ko scan kiye bina query tez karti hain. Inme extra storage lagta hai aur writes thode slow ho jaate hain.

* **Compound indexes** — An index on multiple fields; field order matters (equality first, then sort, then range). It supports queries using a left prefix of the fields.
  > **Hinglish:** Kai fields pe ek index; fields ka order matter karta hai (pehle equality, phir sort, phir range). Ye left prefix wali queries ko support karta hai.

* **Query optimization** — Use indexes, project only needed fields, limit results, avoid unbounded scans, and avoid `$where`/unindexed regex.
  > **Hinglish:** Indexes use karo, sirf zaroori fields mangao (projection), results limit karo, poore collection scan se bacho, aur `$where`/bina index wale regex avoid karo.

* **`explain()`** — Shows how MongoDB executes a query: `COLLSCAN` (bad) vs `IXSCAN` (good), documents examined vs returned, execution time.
  > **Hinglish:** Dikhata hai MongoDB query ko kaise chalata hai: `COLLSCAN` (bura) vs `IXSCAN` (accha), kitne documents dekhe vs kitne return hue, aur execution time.

* **Aggregation** — A pipeline of stages (`$match`, `$group`, `$sort`, `$project`, `$lookup`) that transforms data for reporting and analytics.
  > **Hinglish:** Stages ki ek pipeline (`$match`, `$group`, `$sort`, `$project`, `$lookup`) jo data ko reporting aur analytics ke liye transform karti hai.

* **`$lookup`** — A join-like aggregation stage that pulls matching documents from another collection. Convenient but slower than embedding at scale.
  > **Hinglish:** Join jaisa aggregation stage jo dusre collection se matching documents le aata hai. Aasaan hai, lekin scale pe embedding se slow hota hai.

* **Embedding vs referencing** — Embed when data is read together and bounded (address in user). Reference when data is large, shared, or grows without limit (user → orders).
  > **Hinglish:** Jab data saath padha jaata hai aur limited hai (user ke andar address) to embed karo. Jab data bada, shared ya badhta hi jaane wala ho (user → orders) to reference karo.

* **Transactions** — Multi-document operations that commit or roll back together (requires replica set). Use sparingly; good schema design reduces the need for them.
  > **Hinglish:** Kai documents pe operations jo ya to saath commit hote hain ya saath rollback (replica set chahiye). Kam use karo; achha schema design se inki zaroorat kam padti hai.

* **Atomicity** — A single-document operation is always atomic in MongoDB. That's a major reason to embed related data.
  > **Hinglish:** MongoDB mein ek document pe hone wala operation hamesha atomic hota hai. Isi liye related data ko embed karna faydemand hota hai.

* **Pagination** — `skip/limit` is simple but slow for deep pages. Cursor/range-based pagination (using `_id` or a timestamp) scales better.
  > **Hinglish:** `skip/limit` simple hai par door ke pages pe slow ho jaata hai. Cursor/range-based pagination (`_id` ya timestamp se) better scale karti hai.

* **MongoDB vs SQL** — MongoDB: flexible schema, nested documents, easy horizontal scaling. SQL: strict schema, powerful joins, strong relational integrity. Choose by data shape and access patterns.
  > **Hinglish:** MongoDB: flexible schema, nested documents, aasaan horizontal scaling. SQL: strict schema, powerful joins, strong relational integrity. Data ke shape aur access pattern ke hisaab se chuno.

#### Database fundamentals

* **Basic SQL concepts** — Tables, rows, primary/foreign keys, `SELECT`, `JOIN`, `GROUP BY`, indexes.
  > **Hinglish:** Tables, rows, primary/foreign keys, `SELECT`, `JOIN`, `GROUP BY`, indexes.

* **Relationships** — One-to-one, one-to-many, many-to-many; modeled with foreign keys in SQL and embedding/references in MongoDB.
  > **Hinglish:** One-to-one, one-to-many, many-to-many; SQL mein foreign keys se aur MongoDB mein embedding/references se banaye jaate hain.

* **Normalization** — Organizing data to reduce duplication (store each fact once). MongoDB often *denormalizes* on purpose for faster reads.
  > **Hinglish:** Data ko is tarah organize karna ki duplication kam ho (har baat ek hi baar store ho). MongoDB mein tez reads ke liye aksar jaan-bujh ke *denormalize* karte hain.

* **ACID** — **A**tomicity (all or nothing), **C**onsistency (valid state), **I**solation (concurrent transactions don't interfere), **D**urability (committed data survives crashes).
  > **Hinglish:** **A**tomicity (ya sab ya kuch nahi), **C**onsistency (data hamesha valid state mein), **I**solation (ek saath chalne wali transactions ek dusre ko disturb na karein), **D**urability (commit hua data crash ke baad bhi bacha rahe).

#### Then connect it to Mongoose:

* **Schema** — Defines fields, types, defaults, and rules for a document.
  > **Hinglish:** Document ke fields, types, defaults aur rules define karta hai.

* **Model** — A compiled schema that gives you methods like `find`, `create`, `findByIdAndUpdate`.
  > **Hinglish:** Compile kiya hua schema jo `find`, `create`, `findByIdAndUpdate` jaise methods deta hai.

* **Validation** — Built-in rules (`required`, `min`, `enum`, `match`) and custom validators that run before saving.
  > **Hinglish:** Built-in rules (`required`, `min`, `enum`, `match`) aur custom validators jo save hone se pehle chalte hain.

* **Middleware** — Hooks (`pre`/`post`) that run around operations like `save`, e.g., hashing a password before saving.
  > **Hinglish:** `pre`/`post` hooks jo `save` jaise operations ke aas-paas chalte hain, jaise save se pehle password hash karna.

* **`populate`** — Replaces a referenced `ObjectId` with the actual document from another collection (an app-level "join", runs extra queries).
  > **Hinglish:** Reference wali `ObjectId` ko dusre collection ke asli document se badal deta hai (app-level "join", extra queries chalti hain).

* **`lean`** — Returns plain JS objects instead of full Mongoose documents. Faster and lighter for read-only queries.
  > **Hinglish:** Poore Mongoose document ke bajay simple JS objects return karta hai. Sirf padhne wali queries ke liye tez aur halka.

* **`save`** — Saves a single document and runs validation and middleware.
  > **Hinglish:** Ek document save karta hai aur validation aur middleware bhi chalata hai.

* **`insertMany`** — Inserts many documents in one batch operation. Much faster than looping `save()`, though it skips some document middleware.
  > **Hinglish:** Bahut saare documents ek hi batch mein insert karta hai. Loop mein `save()` se kaafi tez hai, par kuch document middleware skip ho jaate hain.

---

### 6. HTTP + REST + security / API & Web Fundamentals

This is an area people often use every day but can't explain properly.

Build strong fundamentals around:

* **HTTP request/response** — A text-based, stateless protocol. The client sends a request (method, URL, headers, body); the server returns a response (status, headers, body).
  > **Hinglish:** Text-based, stateless protocol. Client request bhejta hai (method, URL, headers, body); server response deta hai (status, headers, body).

* **HTTP vs HTTPS** — HTTPS is HTTP over TLS: data is encrypted, the server is authenticated, and tampering is detected.
  > **Hinglish:** HTTPS matlab HTTP + TLS: data encrypted hota hai, server ki pehchaan verify hoti hai, aur beech mein koi data badle to pata chal jaata hai.

* **HTTP Methods & Status Codes** — Methods describe the action; status codes describe the outcome (see below).
  > **Hinglish:** Methods batate hain kya karna hai; status codes batate hain natija kya raha (neeche dekho).

* **Headers** — Metadata about the request/response (`Content-Type`, `Authorization`, `Cache-Control`, `Set-Cookie`).
  > **Hinglish:** Request/response ke baare mein extra jaankari (`Content-Type`, `Authorization`, `Cache-Control`, `Set-Cookie`).

* **Body** — The payload of a request/response, typically JSON, used with `POST/PUT/PATCH`.
  > **Hinglish:** Request/response ka asli data, aam taur par JSON, jo `POST/PUT/PATCH` ke saath bheja jaata hai.

* **Query parameters** — Optional key-values after `?` used for filtering, sorting, and pagination (`/users?page=2`).
  > **Hinglish:** `?` ke baad aane wale optional key-value pairs, jo filtering, sorting aur pagination ke liye hote hain (`/users?page=2`).

* **Path parameters** — Part of the URL that identifies a resource (`/users/42`).
  > **Hinglish:** URL ka wo hissa jo kisi specific resource ko pehchanta hai (`/users/42`).

* **HTTP methods** — `GET` read (safe, idempotent), `POST` create (not idempotent), `PUT` replace (idempotent), `PATCH` partial update, `DELETE` remove (idempotent).
  > **Hinglish:** `GET` padhne ke liye (safe, idempotent), `POST` banane ke liye (idempotent nahi), `PUT` poora replace (idempotent), `PATCH` thoda sa update, `DELETE` hataane ke liye (idempotent).

* **Status codes** — `2xx` success (200, 201, 204), `3xx` redirect, `4xx` client error (400, 401, 403, 404, 409, 429), `5xx` server error (500, 502, 503).
  > **Hinglish:** `2xx` success (200, 201, 204), `3xx` redirect, `4xx` client ki galti (400, 401, 403, 404, 409, 429), `5xx` server ki galti (500, 502, 503).

* **Cookies** — Small data the server asks the browser to store and send back with each request. Secure ones use `HttpOnly`, `Secure`, and `SameSite`.
  > **Hinglish:** Chhota data jo server browser se store karwata hai aur browser har request ke saath wapas bhejta hai. Secure cookies mein `HttpOnly`, `Secure` aur `SameSite` lagate hain.

* **Webhooks** — The reverse of an API call: a third-party service sends an HTTP POST to *your* URL when an event happens (e.g., payment succeeded). Verify the signature and respond fast.
  > **Hinglish:** API call ka ulta: koi event hone par (jaise payment success) third-party service *aapke* URL pe HTTP POST bhejti hai. Signature verify karo aur jaldi respond karo.

* **Sessions** — The server stores user state and gives the browser a session ID in a cookie. Easy to revoke, but needs server-side storage.
  > **Hinglish:** Server user ki state store karta hai aur browser ko cookie mein session ID deta hai. Revoke karna aasaan hai, par server-side storage chahiye.

* **JWT** — A signed token (header.payload.signature) containing claims. The server verifies the signature without a database lookup. Stateless, but hard to revoke before expiry.
  > **Hinglish:** Signed token (header.payload.signature) jisme claims hote hain. Server bina database dekhe signature verify kar leta hai. Stateless hai, lekin expiry se pehle revoke karna mushkil hai.

* **Refresh tokens** — A long-lived token used to get new short-lived access tokens. Stored securely (HttpOnly cookie) and can be rotated/revoked.
  > **Hinglish:** Lambi life wala token jisse naye short-lived access tokens milte hain. Ise safe tareeke se (HttpOnly cookie) rakho aur rotate/revoke kar sakte hain.

* **Authentication vs authorization** — Authentication = *who are you?* Authorization = *what are you allowed to do?*
  > **Hinglish:** Authentication = *tum kaun ho?* Authorization = *tumhe kya karne ki ijaazat hai?*

* **CORS** — Browser-enforced rule controlling which origins can call your API; the server opts in using `Access-Control-Allow-*` headers. It does not protect the server from non-browser clients.
  > **Hinglish:** Browser ka rule jo decide karta hai kaun se origins aapki API call kar sakte hain; server `Access-Control-Allow-*` headers se allow karta hai. Ye non-browser clients (jaise Postman, curl) se server ko protect nahi karta.

* **CSRF** — An attacker's site tricks the browser into sending an authenticated request using the user's cookies. Prevented with `SameSite` cookies and CSRF tokens.
  > **Hinglish:** Attacker ki site browser ko dhokha deke user ki cookies ke saath authenticated request bhijwa deti hai. `SameSite` cookies aur CSRF tokens se bachav hota hai.

* **XSS** — Attacker injects malicious script into a page that runs in the victim's browser. Prevented with output escaping, sanitization, CSP, and `HttpOnly` cookies.
  > **Hinglish:** Attacker page mein malicious script daal deta hai jo victim ke browser mein chalti hai. Output escape karne, sanitize karne, CSP aur `HttpOnly` cookies se bachav hota hai.

* **HTTPS** — Encrypts traffic between client and server using TLS certificates.
  > **Hinglish:** TLS certificates ke through client aur server ke beech ke traffic ko encrypt karta hai.

* **Password hashing** — Never store plain passwords. Use a slow, salted hash (bcrypt/argon2) so stolen data can't be easily reversed.
  > **Hinglish:** Password kabhi plain text mein store mat karo. Slow, salted hash (bcrypt/argon2) use karo taaki data chori ho bhi jaye to password aasaani se na nikle.

* **API validation** — Validate all input (type, length, format) on the server; client-side validation is only for UX.
  > **Hinglish:** Saara input (type, length, format) server pe validate karo; client-side validation sirf user experience ke liye hai.

* **Rate limiting** — Cap requests per client/IP/time window to stop abuse, brute force, and overload; return `429`.
  > **Hinglish:** Har client/IP ke liye ek time window mein requests ki limit lagao taaki abuse, brute force aur overload rukein; limit cross hone par `429` return karo.

* **API versioning** — Lets you change an API without breaking clients: `/api/v1/users` or a version header.
  > **Hinglish:** API badalte waqt purane clients ko todne se bachata hai: `/api/v1/users` ya version header.

* **Idempotency** — Repeating the same request gives the same result (no extra side effects). Critical for retries; for `POST` payments, use an idempotency key.
  > **Hinglish:** Same request ko dobara bhejne par bhi same result aaye aur extra side effect na ho. Retries ke liye bahut zaroori; `POST` payments mein idempotency key use karte hain.

For example, you should be able to explain:

#### Why do we use POST instead of GET for creating data?

**Short answer:** `GET` is defined as *safe* and *idempotent*: it must not change server state, and browsers, proxies, and CDNs may cache, prefetch, or repeat it freely. Creating data changes state, so using `GET` could create duplicates by accident (a prefetch, a refresh, a crawler). Also, `GET` data goes in the URL (logged, size-limited, visible), while `POST` sends it in the body.

> **Hinglish:** `GET` ko *safe* aur *idempotent* maana jaata hai: wo server ki state nahi badalta, aur browser, proxy, CDN use cache, prefetch ya repeat kar sakte hain. Data banana state badalta hai, to `GET` se banane par galti se duplicates ban sakte hain (prefetch, refresh, crawler ki wajah se). Saath hi `GET` ka data URL mein jaata hai (logs mein dikhta hai, size limited), jabki `POST` data body mein bhejta hai.

rather than simply memorizing:

“POST is used to create.”

---

### 7. Authentication & Security

* **JWT** — Stateless signed token the client sends in each request (usually `Authorization: Bearer <token>`). Keep it short-lived and never put secrets in the payload (it's only encoded, not encrypted).
  > **Hinglish:** Stateless signed token jo client har request ke saath bhejta hai (aam taur par `Authorization: Bearer <token>`). Ise short-lived rakho aur payload mein secrets mat daalo (ye sirf encoded hota hai, encrypted nahi).

* **Sessions** — Server-side state identified by a cookie. Easier to invalidate; needs a store (Redis/DB) to scale.
  > **Hinglish:** Server-side state jo cookie se pehchani jaati hai. Invalidate karna aasaan; scale karne ke liye store (Redis/DB) chahiye.

* **Refresh Tokens** — Used to issue new access tokens without logging in again. Store hashed in DB, rotate on use, and revoke on logout.
  > **Hinglish:** Dobara login kiye bina naye access tokens lene ke liye. DB mein hash karke rakho, use hone par rotate karo, aur logout par revoke karo.

* **Password Hashing** — Use bcrypt/argon2 with salt and a proper cost factor. Hashing is one-way; encryption is two-way.
  > **Hinglish:** Salt aur sahi cost factor ke saath bcrypt/argon2 use karo. Hashing one-way hai (wapas nahi aata); encryption two-way hai (decrypt ho sakta hai).

* **Authentication vs Authorization** — Authentication verifies identity; authorization checks permissions for an action.
  > **Hinglish:** Authentication pehchaan verify karta hai; authorization check karta hai ki us action ki permission hai ya nahi.

* **RBAC** — Role-Based Access Control: permissions are assigned to roles (admin, editor, user) and users get roles. Enforced via middleware.
  > **Hinglish:** Role-Based Access Control: permissions roles ko di jaati hain (admin, editor, user) aur users ko roles milte hain. Middleware se enforce hota hai.

* **XSS** — Malicious scripts running in your page. Escape output, sanitize HTML, use CSP, and avoid `dangerouslySetInnerHTML`.
  > **Hinglish:** Aapke page mein chalne wali malicious scripts. Output escape karo, HTML sanitize karo, CSP lagao, aur `dangerouslySetInnerHTML` se bacho.

* **CSRF** — Forged requests using the victim's cookies. Use `SameSite` cookies and anti-CSRF tokens.
  > **Hinglish:** Victim ki cookies use karke bheji gayi nakli requests. `SameSite` cookies aur anti-CSRF tokens use karo.

* **API Security** — Use HTTPS, validate input, rate limit, set security headers (`helmet`), use least-privilege access, avoid leaking details in errors, and keep dependencies updated.
  > **Hinglish:** HTTPS use karo, input validate karo, rate limit lagao, security headers (`helmet`) set karo, least-privilege access do, errors mein andar ki details leak mat karo, aur dependencies update rakho.

---

### 8. Then your real-world engineering fundamentals

This is where your 3 years of experience should start showing.

* **Git & GitHub** — Git tracks versions locally; GitHub hosts repos and enables collaboration via branches and pull requests. Know `merge` vs `rebase`, `stash`, `cherry-pick`, and resolving conflicts.
  > **Hinglish:** Git local mein versions track karta hai; GitHub repos host karta hai aur branches/pull requests se team collaboration deta hai. `merge` vs `rebase`, `stash`, `cherry-pick` aur conflicts resolve karna aana chahiye.

* **Environment Variables** — Config and secrets kept outside code (`.env`, `process.env`) so the same code runs in dev, staging, and production. Never commit secrets.
  > **Hinglish:** Config aur secrets ko code se bahar rakhna (`.env`, `process.env`) taaki same code dev, staging aur production mein chale. Secrets ko kabhi commit mat karo.

* **Debugging** — Reproduce the issue, read the error/stack trace, isolate the cause, use breakpoints/logs/Node inspector, and fix the root cause.
  > **Hinglish:** Pehle issue reproduce karo, error/stack trace padho, cause ko alag karo, breakpoints/logs/Node inspector use karo, aur asli root cause fix karo.

* **Logging** — Record what the app does, using levels (info/warn/error), structured JSON logs, and request IDs. Tools: Winston, Pino. Never log passwords or tokens.
  > **Hinglish:** App kya kar raha hai ye record karna, levels (info/warn/error), structured JSON logs aur request IDs ke saath. Tools: Winston, Pino. Password ya tokens kabhi log mat karo.

* **Testing** — Unit (single function), integration (modules together, e.g., API + DB), and end-to-end (full flow). Tools: Jest, Supertest, Cypress/Playwright.
  > **Hinglish:** Unit (ek function), integration (modules saath mein, jaise API + DB), aur end-to-end (poora flow). Tools: Jest, Supertest, Cypress/Playwright.

* **Error handling** — Fail gracefully, return clear error responses, log details internally, and don't expose stack traces to users.
  > **Hinglish:** Achhe se fail ho, clear error responses do, andar ki details log karo, aur users ko stack trace mat dikhao.

* **Docker Basics** — Packages your app and its dependencies into an image that runs the same everywhere. Image = blueprint, container = running instance, `Dockerfile` = recipe.
  > **Hinglish:** App aur uski dependencies ko ek image mein pack karta hai jo har jagah same chalti hai. Image = blueprint, container = chalta hua instance, `Dockerfile` = recipe.

* **Nginx** — A web server used as a reverse proxy, load balancer, SSL terminator, and static file server in front of your Node app.
  > **Hinglish:** Ek web server jo Node app ke aage reverse proxy, load balancer, SSL terminator aur static files server ka kaam karta hai.

* **PM2** — A process manager for Node: keeps the app alive, restarts on crash, runs in cluster mode, and manages logs.
  > **Hinglish:** Node ka process manager: app ko zinda rakhta hai, crash par restart karta hai, cluster mode chalata hai aur logs manage karta hai.

* **Linux basics** — Navigating the file system, permissions (`chmod`), processes (`ps`, `top`, `kill`), logs (`tail -f`), and SSH.
  > **Hinglish:** File system mein navigate karna, permissions (`chmod`), processes (`ps`, `top`, `kill`), logs (`tail -f`) aur SSH.

* **Deployment** — Getting code running on a server: build → configure environment → run behind Nginx/PM2 or in containers → monitor.
  > **Hinglish:** Code ko server pe chalana: build → environment configure → Nginx/PM2 ya containers mein run → monitor.

* **CI/CD basics** — CI automatically builds and tests every push; CD automatically deploys passing builds (GitHub Actions, GitLab CI, Jenkins).
  > **Hinglish:** CI har push pe apne aap build aur test karta hai; CD pass hui builds ko apne aap deploy karta hai (GitHub Actions, GitLab CI, Jenkins).

* **Redis** — An in-memory key-value store used for caching, sessions, rate limiting, pub/sub, and job queues.
  > **Hinglish:** Memory mein chalne wala key-value store, jo caching, sessions, rate limiting, pub/sub aur job queues ke liye use hota hai.

* **Queues/background jobs** — Put slow tasks in a queue (BullMQ, RabbitMQ, SQS) and process them with workers so APIs respond quickly and jobs can be retried.
  > **Hinglish:** Dheere kaam ko queue (BullMQ, RabbitMQ, SQS) mein daalo aur workers se process karo, taaki API jaldi respond kare aur fail hone par job retry ho sake.

* **Cron jobs** — Scheduled tasks that run at set times (`node-cron`, system cron) for reports, cleanups, and reminders.
  > **Hinglish:** Tay samay par chalne wale scheduled tasks (`node-cron`, system cron), jaise reports, cleanup aur reminders ke liye.

* **Webhooks** — Receive event notifications from other services; verify signatures, respond `200` quickly, and process asynchronously.
  > **Hinglish:** Dusri services se event notifications receive karna; signature verify karo, jaldi `200` respond karo, aur process baad mein async karo.

* **Third-party API integration** — Handle auth, timeouts, errors, rate limits, retries, and response mapping; wrap each service in its own module.
  > **Hinglish:** Auth, timeouts, errors, rate limits, retries aur response mapping sambhalo; har service ko apne alag module mein wrap karo.

* **Retry mechanisms** — Retry transient failures with exponential backoff + jitter and a max attempts limit; only retry idempotent operations.
  > **Hinglish:** Temporary failures ko exponential backoff + jitter ke saath retry karo, max attempts ki limit ke saath; sirf idempotent operations hi retry karo.

* **Rate limits** — Both ways: limit your own API clients, and respect third-party limits (queue/throttle, honor `429` and `Retry-After`).
  > **Hinglish:** Dono taraf: apne API clients ko limit karo, aur third-party ki limits ka bhi dhyaan rakho (queue/throttle karo, `429` aur `Retry-After` maano).

---

### 9. AI & LLM Fundamentals

* **LLM Basics** — A Large Language Model predicts the next token based on the input, trained on huge text data. It generates plausible text and can hallucinate.
  > **Hinglish:** Large Language Model input ke basis pe agla token predict karta hai, aur bahut bade text data pe train hota hai. Ye sahi dikhne wala text banata hai lekin galat bhi bol sakta hai (hallucination).

* **Prompt Engineering** — Writing clear instructions, context, examples (few-shot), and output format to get reliable results. Use system prompts for role/rules.
  > **Hinglish:** Saaf instructions, context, examples (few-shot) aur output format likhna taaki bharosemand result mile. Role/rules ke liye system prompt use karo.

* **Tokens & Context Windows** — Tokens are chunks of text (~¾ of a word). The context window is the max tokens (input + output) the model can consider at once; cost and latency scale with tokens.
  > **Hinglish:** Tokens text ke tukde hote hain (lagbhag ek shabd ka ¾). Context window wo max tokens (input + output) hai jo model ek baar mein dekh sakta hai; cost aur latency tokens ke saath badhte hain.

* **Function / Tool Calling** — The model returns a structured request to call your function (e.g., `getWeather(city)`); your code runs it and sends the result back so the model can answer.
  > **Hinglish:** Model ek structured request deta hai ki aapka function call karo (jaise `getWeather(city)`); aapka code use chalata hai aur result model ko wapas bhejta hai taaki wo jawab de sake.

* **Embeddings** — Numeric vectors that represent the *meaning* of text, so similar texts are close in vector space. Used for semantic search.
  > **Hinglish:** Text ke *matlab* ko numbers (vectors) mein badalna, taaki milte-julte texts vector space mein paas-paas hon. Semantic search mein use hota hai.

* **Vector Databases** — Databases (Pinecone, Qdrant, pgvector, MongoDB Atlas Vector Search) optimized for storing embeddings and finding nearest neighbors quickly.
  > **Hinglish:** Aise databases (Pinecone, Qdrant, pgvector, MongoDB Atlas Vector Search) jo embeddings store karne aur sabse milte-julte (nearest neighbors) results tezi se dhundhne ke liye bane hain.

* **RAG** — Retrieval-Augmented Generation: embed documents, retrieve the most relevant chunks for a question, and include them in the prompt so the model answers from your data with fewer hallucinations.
  > **Hinglish:** Retrieval-Augmented Generation: documents ko embed karo, sawal ke liye sabse relevant chunks nikaalo, aur unhe prompt mein daalo, taaki model aapke data se jawab de aur hallucination kam ho.

* **LangChain** — A framework that provides building blocks (prompts, chains, retrievers, tools, memory) to build LLM apps faster. Useful, but you should understand the raw API underneath.
  > **Hinglish:** Ek framework jo LLM apps jaldi banane ke liye building blocks deta hai (prompts, chains, retrievers, tools, memory). Kaam ka hai, par neeche ka raw API samajhna bhi zaroori hai.

* **AI Agents** — LLM-driven systems that decide *which steps/tools to use* in a loop (think → act → observe) to reach a goal, rather than following a fixed flow.
  > **Hinglish:** LLM-based systems jo fixed flow follow karne ke bajay loop mein khud decide karte hain *kaun se steps/tools use karne hain* (socho → karo → dekho) taaki goal tak pahunch sakein.

* **Conversation Memory** — LLMs are stateless, so you resend relevant history each time. Manage it by trimming, summarizing, or storing/retrieving important facts.
  > **Hinglish:** LLMs stateless hote hain, isliye har baar relevant history dobara bhejni padti hai. Isse sambhalne ke liye history trim karo, summarize karo, ya zaroori facts store karke retrieve karo.

* **LLM API Integration** — Call the provider's API from your backend (never expose API keys in the frontend), handle streaming, timeouts, retries, rate limits, token costs, and validate outputs.
  > **Hinglish:** Provider ki API ko apne backend se call karo (API key frontend mein kabhi expose mat karo), streaming, timeouts, retries, rate limits, token cost sambhalo, aur output validate karo.

---

### 10. System Design

* **Scalability** — The ability to handle more load. *Vertical* = bigger machine; *horizontal* = more machines (needs stateless services and a load balancer).
  > **Hinglish:** Zyada load sambhalne ki kshamta. *Vertical* = machine ko bada karna; *horizontal* = zyada machines lagana (stateless services aur load balancer chahiye).

* **Caching** — Store frequently-read or expensive results in fast storage (Redis, CDN, browser) to cut latency and DB load. Hardest part: invalidation and stale data.
  > **Hinglish:** Baar-baar padhe jaane wale ya mehenge results ko tez storage (Redis, CDN, browser) mein rakhna, taaki latency aur DB load kam ho. Sabse mushkil hissa: cache invalidation aur purana data.

* **Load Balancing** — Distributes traffic across multiple servers (round robin, least connections) and removes unhealthy ones. Examples: Nginx, AWS ALB.
  > **Hinglish:** Traffic ko kai servers mein baantta hai (round robin, least connections) aur kharab servers ko hata deta hai. Examples: Nginx, AWS ALB.

* **Queues** — Decouple producers from consumers, absorb traffic spikes, and enable async processing and retries.
  > **Hinglish:** Kaam bhejne wale aur kaam karne wale ko alag karti hain, traffic spikes ko sambhalti hain, aur async processing aur retries possible banati hain.

* **Database Scaling** — Indexing and query tuning first, then read replicas, caching, sharding (splitting data across nodes), and partitioning.
  > **Hinglish:** Pehle indexing aur query tuning, phir read replicas, caching, sharding (data ko alag nodes mein baantna) aur partitioning.

* **API Design** — Consistent resource naming, proper methods/status codes, pagination, filtering, versioning, validation, and clear error formats.
  > **Hinglish:** Resource ke naam ek jaise, sahi methods/status codes, pagination, filtering, versioning, validation, aur saaf error format.

* **Basic System Design Problems** — Typical practice: URL shortener, rate limiter, chat app, notification system, news feed. Approach: requirements → estimate scale → high-level design → data model → bottlenecks and trade-offs.
  > **Hinglish:** Aam practice problems: URL shortener, rate limiter, chat app, notification system, news feed. Approach: requirements → scale ka andaza → high-level design → data model → bottlenecks aur trade-offs.

---

## Learning Approach

For every topic, I aim to understand:

1. **What is it?**
2. **Why do we need it?**
3. **How does it work?**
4. **How can I implement it?**
5. **Where have I used it in a real project?**
6. **What are its alternatives or limitations?**

The focus is on **understanding and explaining**, not memorizing predefined interview answers.

## Interview Preparation

Each concept may contain:

```text
Concept
├── Explanation
├── Why it is needed
├── How it works
├── Example
├── Common interview questions
├── Practical use case
└── Common mistakes / follow-up questions
```

## Repository Structure

```text
fullstack-fundamentals-MERN/
│
├── javascript/
├── react/
├── node/
├── express/
├── mongodb/
├── mongoose/
├── api-rest/
├── authentication-security/
├── git/
├── deployment/
├── redis/
├── system-design/
├── ai-llm/
│
├── interview-questions/
├── coding-practice/
│
└── README.md
```

## Objective

> **Learn the fundamentals. Understand how things work. Practice them. Explain them clearly. Apply them in real projects.**

This repository is a continuous learning and interview-preparation resource for becoming a stronger **Full-Stack MERN Developer**.



