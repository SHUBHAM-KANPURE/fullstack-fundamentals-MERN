# Full-Stack Fundamentals — Hinglish Interview Notes

Simple Hinglish explanations for the same topics in `README_ANSWERS_ENGLISH.md`. Technical terms English mein hi rakhe gaye hain.

## 1. JavaScript

### Variables, Scope, and Functions

- **`var`, `let`, `const`:** `var` function-scoped hota hai; `let` aur `const` block-scoped hote hain. `let` ko reassign kar sakte hain, `const` variable binding ko reassign nahi kar sakte. Lekin `const` object ke andar ki values ko automatically freeze nahi karta.
- **Scope:** Scope batata hai ki variable code ke kis area mein access ho sakta hai.
- **Lexical scope:** Variable ka access is baat se decide hota hai ki code kahan likha gaya hai, function kahan call hua isse nahi.
- **Hoisting:** JavaScript code execute karne se pehle declarations ko process karta hai. `var` ki initial value `undefined` hoti hai; `let`/`const` ko declaration se pehle access nahi kar sakte, kyunki TDZ hota hai.
- **Closure:** Jab inner function outer function ke variables ko yaad rakhta hai, outer function finish hone ke baad bhi, use closure kehte hain.
- **`this`:** `this` ki value generally is baat par depend karti hai ki function kaise call hua. Arrow function apne surrounding scope ka `this` use karta hai.
- **Function:** Reusable code block jo input le sakta hai aur result return kar sakta hai.
- **Callback:** Aisa function jo kisi doosre function ko diya jaata hai taaki use baad mein call kiya ja sake.
- **Arrow function:** Function likhne ka short syntax. Iska apna `this` aur `arguments` nahi hota, aur ise constructor ki tarah use nahi kar sakte.
- **Prototype:** Ek object jahan se doosra object prototype chain ke through properties aur methods inherit kar sakta hai.
- **`==` vs `===`:** `==` comparison se pehle type conversion kar sakta hai; `===` type conversion ke bina compare karta hai. Predictable result ke liye `===` prefer karein.
- **`null` vs `undefined`:** `undefined` ka matlab aam taur par value assign nahi hui; `null` ka matlab intentionally empty value.
- **Destructuring:** Array ya object se values nikaal kar variables mein rakhne ka short syntax.
- **Spread (`...`):** Array/object ki values ko expand karke naya array/object ya function arguments banane mein use hota hai.
- **Rest parameters:** `...args` function ke remaining arguments ko ek array mein collect karta hai.
- **Pass by value:** JavaScript values pass karta hai. Object ke case mein copied value same object ka reference hoti hai, isliye object ki mutation caller ko bhi dikh sakti hai.
- **Shallow copy:** Sirf first level copy hota hai; nested objects ke references same reh sakte hain.
- **Deep copy:** Nested data bhi copy karta hai, taaki copy mein changes original ko affect na karein; supported data types copying method par depend karte hain.

### Arrays and Objects

- **`forEach()`:** Har array item par callback chalata hai; result array create nahi karta.
- **`map()`:** Har item ko transform karke same length ka naya array return karta hai.
- **`filter()`:** Condition pass karne wale items ka naya array return karta hai.
- **`reduce()`:** Array ke items ko combine karke ek final result banata hai, jaise sum ya grouped object.
- **`find()`:** Condition match karne wala pehla item deta hai; match na mile to `undefined`.
- **`some()`:** Kam se kam ek item condition pass kare to `true`.
- **`every()`:** Sabhi items condition pass karein tabhi `true`.
- **`slice()` vs `splice()`:** `slice()` original array ko change kiye bina portion return karta hai; `splice()` original array mein items add/remove karta hai.
- **Mutable vs immutable methods:** Mutable method original value change karta hai; non-mutating method original ko badle bina result deta hai.
- **Optional chaining (`?.`):** Agar beech ki value `null` ya `undefined` ho to nested property access se error aane se bachata hai.
- **Nullish coalescing (`??`):** Fallback sirf `null`/`undefined` par deta hai. `||` `0` aur empty string ko bhi false maanta hai.
- **JSON:** Structured data exchange karne ka text format. `JSON.stringify()` supported JS data ko JSON text banata hai; `JSON.parse()` JSON text ko JS value banata hai.

### Asynchronous JavaScript

- **Synchronous code:** Ek step complete hota hai, phir next step execute hota hai.
- **Asynchronous code:** Waiting operation ke complete hone tak program doosra kaam kar sakta hai.
- **Promise:** Future mein complete hone wale async operation ki success ya failure represent karta hai. States: pending, fulfilled, rejected.
- **`async/await`:** Promise-based code ko readable banata hai. `await` async function ko pause karta hai, poore JavaScript thread ko nahi.
- **Event loop:** Call stack aur queued callbacks ko coordinate karta hai, jisse async work handle hota hai.
- **Call stack:** Abhi execute ho rahe functions ka record rakhta hai.
- **Microtask vs macrotask:** Promise callbacks microtask queue mein aate hain; timers aur kai I/O callbacks task queues se run hote hain. Aam taur par next task se pehle microtasks process hote hain.
- **`setTimeout()`:** Diye gaye delay ke baad callback schedule karta hai; exact time par run hone ki guarantee nahi.
- **`Promise.all()`:** Sabhi promises fulfill hon to fulfill hota hai; koi ek reject ho to reject ho jaata hai.
- **`Promise.allSettled()`:** Har promise ka settle hona wait karta hai aur har result ka status deta hai.
- **`Promise.race()`:** Jo promise sabse pehle settle hota hai, uske result se settle hota hai.
- **`Promise.any()`:** Pehle fulfilled promise ka result deta hai; sab reject ho jaayein to `AggregateError`.
- **Error handling:** `async/await` ke saath `try/catch`, promise chain ke saath `.catch()` use karein. Errors ko silently ignore na karein.
- **Debouncing:** Calls rukne ke kuch time baad function run karta hai; search input mein useful hai.
- **Throttling:** Ek time interval mein function kitni baar run ho sakta hai, uski limit lagata hai; scroll/resize mein useful hai.
- **Currying:** Multiple arguments lene wale function ko functions ki chain mein convert karna, jahan har function ek ya kam arguments leta hai.
- **`call`, `apply`, `bind`:** Regular function ka `this` set karte hain. `call` arguments separately leta hai, `apply` array-like input leta hai, `bind` naya bound function return karta hai.
- **Memory leak:** Jab unnecessary data ka reference reh jaata hai aur memory release nahi hoti, jaise forgotten timers, listeners ya unlimited cache.
- **Garbage collection:** JavaScript engine un objects ki memory free karta hai jo ab reachable nahi hain.

### Modules and Runtime

- **CommonJS vs ES Modules:** CommonJS mein `require()`/`module.exports`; ES Modules mein `import`/`export` use hota hai.
- **Strict mode:** JavaScript ke stricter rules enable karta hai aur kuch mistakes pakadta hai. Modules aur class bodies strict mode mein hote hain.
- **Type coercion:** Ek data type ka doosre type mein automatic ya explicit conversion.
- **Event delegation:** Parent par ek event handler laga kar bubbling ki help se child elements ke events handle karna.

## 2. React

- **React kyun?** React state/data ke basis par UI describe karne deta hai aur data change hone par DOM update karta hai.
- **Component:** UI ka reusable part, jo commonly function ke form mein JSX return karta hai.
- **JSX:** JavaScript mein UI likhne ka syntax; build tools ise JavaScript calls mein transform karte hain.
- **Props:** Parent component se child ko milne wale read-only inputs.
- **State:** Component ka managed data; state update hone par re-render trigger ho sakta hai.
- **Rendering:** React component ko call karke decide karta hai ki UI kaisi honi chahiye.
- **Re-rendering:** State, props ya context change hone par React component ka UI dobara calculate karta hai.
- **Virtual DOM:** UI elements ka in-memory representation, jise React rendering/reconciliation ke dauran use karta hai.
- **Reconciliation:** Purane aur naye rendered tree ko compare karke required UI updates decide karna.
- **Keys:** List items ko renders ke beech identify/match karne mein help karti hain. Items reorder ya delete ho sakte hain to stable unique ID use karein.
- **Hooks:** `useState`, `useEffect` jaise functions jo function components mein React features use karne dete hain.
- **`useState`:** Component state store karta hai aur setter update schedule karta hai.
- **`useEffect`:** Component ko external systems ke saath synchronize karne ke liye, jaise subscription ya timer. Har calculation ke liye effect ki zaroorat nahi hoti.
- **Effect dependencies:** Ye decide karti hain ki effect kab dobara run hoga; effect mein use hone wali reactive values include karein.
- **`useRef`:** Aisi value store karta hai jo renders ke beech persist karti hai; change hone par re-render trigger nahi hota.
- **`useMemo`:** Dependencies same rehne tak calculated value ko cache karta hai.
- **`useCallback`:** Dependencies same rehne tak function reference ko cache karta hai.
- **`useContext`:** React context se provided value read karta hai.
- **Context API:** Har intermediate component se props pass kiye bina component tree mein value share karna.
- **Custom Hook:** Reusable function jiska naam `use` se start hota hai aur jo React hooks/logic combine karta hai.
- **Controlled input:** Input ki value React state control karti hai.
- **Uncontrolled input:** Input apni value DOM mein rakhta hai; aksar ref se read karte hain.
- **Lifting state up:** Shared state ko closest common parent mein move karna.
- **Prop drilling:** Aise intermediate components se props pass karna jinhe khud un values ki zaroorat nahi.
- **Conditional rendering:** Condition ke basis par alag UI dikhana.
- **React Router:** URL ke basis par client-side pages/components show karne ke liye routing library.
- **Lazy loading / code splitting:** Code ya component ko zaroorat padne par load karna, jisse initial load ka kaam kam ho.
- **Performance optimization:** Unnecessary work kam karna; memoization tab use karein jab actual benefit ho.
- **`React.memo`:** Props same hone par component render skip kar sakta hai, comparison behavior ke hisaab se.
- **State management:** App data ko store/update/share karne ka approach—local state, Context ya library.
- **Error boundary:** Descendant tree ke rendering errors pakad kar fallback UI dikhata hai; har type ka error catch nahi karta.
- **Strict Mode:** Development mein unsafe patterns detect karne mein help karta hai; kuch logic ko jaan-bujhkar dobara run karke side effects expose kar sakta hai.

## 3. Node.js

- **Node.js:** V8 JavaScript engine aur server-side APIs par based runtime, jisse server/network applications bana sakte hain.
- **V8:** JavaScript engine jo code parse aur execute karta hai.
- **libuv:** Node.js mein event loop aur asynchronous I/O support dene wali library.
- **Single-threaded model:** Ek Node.js isolate mein JavaScript callbacks aam taur par main thread par chalte hain; kuch I/O/worker operations alag resources use karte hain.
- **Non-blocking I/O:** I/O operation ka wait karne ke liye JavaScript thread ko synchronously rokna nahi padta.
- **Event-driven architecture:** Events hone par registered handlers execute hote hain.
- **Concurrency vs parallelism:** Concurrency mein tasks ka progress overlapping time par manage hota hai; parallelism mein tasks same time par execute hote hain.
- **`process.nextTick()`:** Callback ko next-tick queue mein schedule karta hai, jo event loop continue hone se pehle process hoti hai. Bahut zyada use I/O ko starve kar sakta hai.
- **`setImmediate()`:** Callback ko event loop ke check phase ke liye schedule karta hai.
- **Timers:** `setTimeout()` aur `setInterval()` delay ke baad callbacks schedule karte hain; exact timing event-loop load par depend karti hai.
- **Buffer:** Raw binary data, jaise file content ya network packets, represent karta hai.
- **Stream:** Data ko chunks mein process karta hai, poora data memory mein load karna zaroori nahi.
- **Readable/Writable/Duplex/Transform streams:** Data read karna, write karna, dono karna, ya process karke aage pass karna.
- **EventEmitter:** Named events emit karne aur unke listeners register karne ka Node.js API/pattern.
- **Worker threads:** Separate threads mein JavaScript chalate hain; CPU-heavy work ke liye useful.
- **Child process:** Alag process mein command/program run karta hai.
- **Cluster:** Multiple Node.js processes run karta hai, jisse multiple CPU cores use kiye ja sakte hain.
- **Environment variables:** Code ke bahar se configuration dene ka tareeka; Node mein `process.env` se access hoti hain.
- **Graceful shutdown:** New requests rokna, ongoing work ko safely complete/close karna, resources release karna aur exit karna.
- **Background job:** Aisa work jo immediate HTTP response ke baad worker/queue se process hota hai.
- **Node error handling:** Failure ko sahi jagah handle karein, useful context dein aur unhandled promise rejections se bachein.

## 4. Express.js

- **Express.js:** Node.js ka minimal web framework jo HTTP routes aur APIs banane mein help karta hai.
- **Request/response lifecycle:** Request server par aati hai, middleware/routes se pass hoti hai, business logic/database use ho sakta hai, phir response return hota hai.
- **Routing:** HTTP method aur URL path ko handler ke saath map karna.
- **Middleware:** Request/response inspect ya modify karta hai, response end karta hai, ya control next middleware ko deta hai.
- **Controller:** HTTP request ka input handle karta hai, business logic call karta hai aur response bhejta hai.
- **Service layer:** Reusable business logic ko HTTP handling se separate rakhti hai.
- **Error middleware:** `(err, req, res, next)` signature se errors ko centrally handle karta hai.
- **Authentication middleware:** Requester ki identity verify karta hai, jaise token validate karke.
- **Validation:** Business logic se pehle request data ka shape, type aur rules check karna.
- **REST API:** Resources aur standard HTTP semantics ke around designed API.
- **CORS:** Browser ko control karta hai ki kaunse origins cross-origin response read kar sakte hain.
- **Rate limiting:** Ek time window mein client ki requests limit karna.
- **API structure:** Routes, controllers, services, models, middleware aur config ko logically separate karna.
- **Centralized error handling:** Har route mein duplicate error response code likhne ke bajay common handler use karna.
- **Joi / Zod:** Schema-validation libraries jo request data validate aur kabhi-kabhi transform karti hain.

## 5. MongoDB and Database Fundamentals

- **MongoDB:** Document-oriented NoSQL database jo BSON documents ko collections mein store karta hai.
- **Database / collection / document:** Database mein collections hoti hain aur collection mein documents. Roughly relational DB ke table/row se compare kar sakte hain.
- **`_id` / ObjectId:** Har document ka unique `_id` hota hai. ObjectId common type hai, lekin `_id` doosre supported types ka bhi ho sakta hai.
- **CRUD:** Create, Read, Update aur Delete operations.
- **Schema:** Data ka expected structure aur rules. MongoDB flexible hai, lekin validation se rules enforce kar sakte hain.
- **Index:** Matching records ko faster find karne mein help karta hai, lekin extra storage aur write overhead hota hai.
- **Compound index:** Multiple fields ka index; field order query support ko affect karta hai.
- **Query optimization:** Filters, indexes, returned fields, sorting aur execution plan improve karke query fast karna.
- **`explain()`:** Query ka execution plan dikhata hai, jisse scans aur index usage samajh sakte hain.
- **Aggregation pipeline:** Stages ki series jo documents filter, transform, group, join ya summarize karti hai.
- **`$lookup`:** Aggregation stage jo doosri collection se matching documents join karti hai.
- **Embedding vs referencing:** Embedding related data ko same document mein rakhta hai; referencing IDs ke through separate documents ko connect karta hai.
- **Transaction:** Multiple database operations ko ek group ki tarah treat karta hai, taaki transaction guarantees ke mutabik saath succeed/fail ho sakein.
- **Atomicity:** Operation all-or-nothing hota hai.
- **Pagination:** Large results ko chhote pages mein dena; skip/limit ya cursor-based approach use kar sakte hain.
- **MongoDB vs SQL:** MongoDB flexible documents use karta hai; relational DB tables aur defined relationships use karta hai. Choice data aur requirements par depend karti hai.
- **Relationship:** Records ke beech connection, jaise one-to-one, one-to-many, many-to-many.
- **Normalization:** Relational data ko organize karna taaki duplication aur update problems kam hon.
- **ACID:** Atomicity, Consistency, Isolation, Durability—reliable transactions ki properties.
- **SQL basics:** `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `WHERE`, `JOIN`, `GROUP BY` aur constraints samjhein.

## 6. Mongoose

- **Mongoose:** Node.js ODM library jo MongoDB ke liye schemas, models, validation, middleware aur convenient queries deti hai.
- **Schema:** Document ke fields, types, defaults aur validation rules define karta hai.
- **Model:** Schema se bana interface jisse documents create, query, update aur delete karte hain.
- **Validation:** Save/validate se pehle values ko schema rules ke against check karta hai.
- **Middleware/hooks:** Supported document, model ya query operations se pehle/baad functions run karte hain.
- **`populate()`:** Referenced IDs ko related collection ke documents se replace karta hai.
- **`lean()`:** Full Mongoose documents ke bajay plain JavaScript objects return karta hai; read-only queries mein overhead kam ho sakta hai.
- **`save()`:** Document save karta hai aur applicable document validation/middleware chalata hai.
- **`insertMany()`:** Multiple documents insert karta hai; validation aur middleware ka behavior individual `save()` se different hota hai.

## 7. HTTP, REST, APIs, and Web Fundamentals

- **HTTP request/response:** Client method, URL, headers aur optional body bhejta hai; server status code, headers aur optional body return karta hai.
- **HTTP vs HTTPS:** HTTPS, TLS use karke transit mein data protect karta hai aur server authentication provide karta hai.
- **GET:** Data retrieve karne ke liye; state-changing action ke liye use nahi karna chahiye.
- **POST:** Data submit/process karne ke liye, aksar resource create ya operation trigger karta hai.
- **PUT:** Resource representation replace karne ke liye; generally idempotent hota hai.
- **PATCH:** Resource ka partial update karne ke liye.
- **DELETE:** Resource remove karne ki request; HTTP semantics mein idempotent define hai.
- **Status codes:** `2xx` success, `3xx` redirection, `4xx` client/request issue, `5xx` server error.
- **Headers:** Request/response metadata, jaise content type, authorization aur caching rules.
- **Request body:** Request ke saath bheja data, commonly POST/PUT/PATCH mein.
- **Query parameters:** URL mein `?` ke baad key-value data; filtering, sorting, pagination mein useful.
- **Path parameters:** URL path mein resource identify karne wali values, jaise `/tasks/:id`.
- **Cookie:** Browser mein store chhota data jo matching requests ke saath cookie rules ke mutabik bheja jaata hai.
- **Session:** Server-side client state, jise aksar session cookie identify karti hai.
- **Webhook:** Event hone par ek system doosre system ko HTTP request se notify karta hai.
- **JWT:** Claims carry karne wala token format. Signed JWT automatically encrypted nahi hota.
- **Refresh token:** Access token renew karne ka credential; storage, expiry aur revocation carefully handle karna chahiye.
- **Authentication vs authorization:** Authentication identity verify karta hai; authorization permissions decide karta hai.
- **CORS:** Browser ke cross-origin response access ko control karta hai; authentication ka replacement nahi.
- **CSRF:** Attack jahan browser ko user ki authenticated site par unwanted request bhejne ke liye trick kiya jaata hai.
- **XSS:** Unsafe handling ki wajah se malicious script user ke browser mein execute hoti hai.
- **Password hashing:** Password ko one-way verifier mein convert karna, Argon2id/bcrypt jaise algorithm aur suitable salt/cost ke saath.
- **API validation:** Request fields, types, limits aur business rules process se pehle check karna.
- **API versioning:** Existing clients ko break kiye bina API evolve karna.
- **Idempotency:** Same request repeat karne par intended effect ek baar karne jaisa hi rahe. Safe retries mein useful.
- **REST:** Architectural style jo resources, representations, stateless interactions aur standard web semantics par focus karta hai.
- **Create ke liye POST kyun, GET kyun nahi?** GET retrieval ke liye hai aur cache/prefetch ho sakta hai; server state change karne ke liye POST zyada suitable hai.

## 8. Authentication and Security

- **RBAC:** Permissions roles ke basis par dena, jaise admin, manager ya user.
- **Access token:** Protected resources access karne ke liye request ke saath bheja credential.
- **Secure token handling:** Signature, expiry aur relevant issuer/audience verify karein; sirf decoded claims par trust na karein.
- **Least privilege:** User/service ko sirf utni permissions dena jitni kaam ke liye zaroori hain.
- **Input validation / output encoding:** Input rules check karna aur output ko context ke hisaab se safely encode karna.
- **Secrets management:** API keys/passwords source control mein commit na karein; secure configuration/secrets manager use karein aur leaked secrets rotate karein.
- **Security headers:** CSP jaise HTTP headers browser protections enable karte hain.
- **Defense in depth:** Ek security control par depend karne ke bajay multiple layers use karna.

## 9. Git, Deployment, and Engineering

- **Git:** Version-control system jo code changes track karta hai aur branching/collaboration support karta hai.
- **GitHub:** Git repositories host aur collaborate karne ka platform.
- **Branch:** Changes par separately kaam karne ke liye development line.
- **Merge conflict:** Jab Git overlapping changes ko automatically combine nahi kar paata.
- **Environment variables:** Environment-specific configuration; secrets commit nahi karne chahiye.
- **Debugging:** Issue reproduce karke, state inspect karke aur hypotheses test karke root cause find karna.
- **Logging:** Events/errors record karna; passwords, tokens aur sensitive data logs mein nahi rakhna.
- **Testing:** Code expected behavior karta hai ya nahi check karna. Unit small unit, integration collaborating parts, E2E complete flow test karta hai.
- **Docker:** App aur dependencies ko container image mein package karta hai taaki execution environments consistent hon.
- **Nginx:** Web server/reverse proxy, jo TLS termination, static files, routing aur load balancing mein use hota hai.
- **PM2:** Node.js process manager jo app ko running rakhne, restart aur logs manage karne mein help karta hai.
- **Linux basics:** Files, permissions, processes, environment variables, logs aur common shell commands samjhein.
- **Deployment:** App ko aise environment mein release karna jahan users/systems access kar saken.
- **CI/CD:** Build, test aur delivery/release steps automate karta hai.
- **Redis:** In-memory data store, commonly cache, counters, sessions aur queue workloads ke liye.
- **Queue:** Jobs ko store karta hai taaki workers unhe background mein process kar saken.
- **Cron job:** Fixed time ya interval par scheduled task.
- **Third-party API integration:** External service ke API, authentication, request format, errors aur rate limits ke saath connect karna.
- **Retry mechanism:** Defined conditions mein failed operation dobara try karna; bounded retries, backoff aur idempotency use karein.
- **Rate limit handling:** Provider limits respect karein aur retry instructions ke mutabik delay/queue karein.
- **Observability:** Logs, metrics aur traces se system ka behavior samajhna.

## 10. AI and LLM Fundamentals

- **AI:** Aisa broad field jisme systems intelligence-related tasks perform karte hain.
- **LLM:** Large text data par trained model jo token sequences predict/generate karta hai aur language tasks perform kar sakta hai.
- **Prompt engineering:** Instructions aur context ko design karna taaki model useful aur constrained output de.
- **Token:** Text ka piece jise model process karta hai; token hamesha complete word nahi hota.
- **Context window:** Ek interaction mein model jitna input/output token context handle kar sakta hai.
- **Tool/function calling:** Model structured tool request deta hai; application tool execute karke result model ko return karti hai.
- **Embedding:** Data ka numerical vector representation, jo semantic similarity search mein useful hota hai.
- **Vector database:** Vectors store karta hai aur similarity search/metadata filtering support karta hai.
- **RAG:** Relevant external information retrieve karke LLM ko dena, taaki answer source information par grounded ho.
- **RAG flow:** Documents ko chunks mein split karein, embeddings banayein, store karein, query par relevant chunks retrieve karke question ke saath model ko dein.
- **LangChain:** Models, prompts, retrievers, tools aur workflows connect karne ka framework.
- **AI agent:** Aisa system jo goal achieve karne ke liye model se steps/tools select karwata hai, defined permissions aur limits ke andar.
- **Conversation memory:** Relevant past information store karta hai taaki future turns mein use ho sake; privacy aur control important hain.
- **LLM API integration:** Model API ko prompt bhejna, response/errors/timeouts handle karna aur cost/privacy/output validate karna.
- **Hallucination:** Model ka plausible lagne wala lekin unsupported ya incorrect claim.
- **Structured output:** Model response ko defined schema mein constrain karke use karne se pehle validate karna.
- **Temperature:** Generation randomness ko influence karne wala parameter; exact effect model/API par depend karta hai.
- **Evaluation:** AI output ki quality, accuracy, safety, latency aur cost test karna.

## 11. System Design

- **Scalability:** Traffic/data badhne par system ki capacity badhane ya efficiency improve karne ki ability.
- **Vertical scaling:** Ek machine ke resources increase karna.
- **Horizontal scaling:** Multiple machines/instances add karna.
- **Caching:** Frequently used data ko faster layer mein rakhna, jisse latency aur load kam ho.
- **Cache invalidation:** Source data change hone par cached data update/expire karna taaki stale data control ho.
- **Load balancing:** Incoming requests ko multiple servers/instances mein distribute karna.
- **Queue-based processing:** Slow/retryable work ko background workers mein shift karna taaki user response wait na kare.
- **Database scaling:** Indexing, query tuning, replication, sharding ya stronger hardware se capacity improve karna.
- **Replication:** Availability/read scaling ke liye data copies multiple nodes par rakhna.
- **Sharding:** Shard key ke basis par data ko multiple database servers mein divide karna.
- **API design:** Clear routes, methods, request/response formats, validation, errors, security aur compatibility define karna.
- **Reliability:** System ka time ke saath correctly operate karte rehna, failures ke dauran bhi.
- **Availability:** Service kitne time usable rehti hai.
- **Latency vs throughput:** Latency ek operation ka time hai; throughput ek unit time mein complete hone wala work.
- **Rate limiting:** Client/key ke requests limit karke service protect karna.
- **Basic system design approach:** Requirements clear karein, load estimate karein, API/data model banayein, components/data flow sketch karein, bottlenecks aur failure scenarios discuss karein.

## Interview Answer Formula

Har topic ko is order mein prepare karein:

1. **What:** Ek clear sentence.
2. **Why:** Kaunsi problem solve karta hai.
3. **How:** Do ya teen simple steps.
4. **Example:** Project ka practical use.
5. **Trade-off:** Zaroorat ho to limitation ya alternative batayein.
