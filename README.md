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
