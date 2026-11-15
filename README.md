# Senior Full-Stack Developer → Architect: The Complete Path

A structured learning path for JavaScript/TypeScript full-stack engineers moving from **mid-level → senior → staff/architect**.

- **15 parts, 158 chapters**, each with a checklist of what you must know
- Stack: TypeScript, React, Next.js, Node.js, NestJS, PostgreSQL, Redis, cloud
- Every part ends with a project and exit criteria, so progress is measurable
- **Every checklist item links to one free resource** to learn it from

> **Version baseline:** late 2026: React 19.x with React Compiler, Next.js 16 App Router with Cache Components and `proxy.ts`, current Node.js LTS, Express 5, NestJS 12 (Standard Schema validation), PostgreSQL 17/18. API names in the checklists were checked against the official documentation sources in November 2026.

### How the resources work

Each checklist item ends with `· [resource](link)`: one **free** resource chosen for that exact item.

- **Official documentation first** (MDN, react.dev, nextjs.org, nodejs.org, docs.nestjs.com, postgresql.org, redis.io, RFCs, OWASP Cheat Sheets).
- **Recognised free references** where no official doc exists (Google SRE books, Azure Architecture Center patterns, Martin Fowler, AWS Builders' Library, StaffEng).
- Links to documentation sites were checked against each project's published source in November 2026. Docs move, so if a link breaks, search the page title on the same site.

---

## Level legend

| Tag | Meaning | You should be able to |
|-----|---------|-----------------------|
| 🟢 | **Senior core** (mid → senior) | Explain it, use it daily, debug it without help |
| 🔵 | **Senior deep** (strong senior) | Predict behavior from internals, teach it, review others' use of it |
| 🟣 | **Architect** (staff / architect) | Decide when *not* to use it, defend the trade-off, set the standard for a team |

---

## Table of contents

| # | Part | Chapters | Focus |
|---|------|----------|-------|
| 01 | [JavaScript & TypeScript](#part-01) | 13 | Language mastery |
| 02 | [The Web Platform](#part-02) | 7 | Browser, network, CSS |
| 03 | [React](#part-03) | 11 | UI engineering |
| 04 | [Next.js](#part-04) | 11 | Full-stack framework |
| 05 | [Node.js](#part-05) | 11 | Runtime internals |
| 06 | [Express & NestJS](#part-06) | 10 | Backend frameworks |
| 07 | [Databases, Caching & Data Modeling](#part-07) | 14 | Data layer |
| 08 | [API Design & Messaging](#part-08) | 12 | Contracts and async communication |
| 09 | [Security & Authentication](#part-09) | 13 | Defense and identity |
| 10 | [Testing & Code Quality](#part-10) | 9 | Confidence and maintainability |
| 11 | [Cloud, DevOps & Delivery](#part-11) | 10 | Shipping and operating |
| 12 | [System Design](#part-12) | 12 | Designing at scale |
| 13 | [Software Architecture](#part-13) | 9 | Structure and trade-offs |
| 14 | [AI Engineering for Full-Stack](#part-14) | 8 | LLM-powered products |
| 15 | [Technical Leadership & the Architect Role](#part-15) | 8 | Influence and strategy |

Also: [Review of the original path](#review) · [How to use this path](#how-to) · [Suggested timeline](#timeline) · [Capstone project thread](#capstone)

---

<a id="review"></a>
## Review of the original path: what changed and why

The original 10-part outline was a strong **senior** curriculum. Its gaps were almost all at the **architect** end and in the layers around the code (browser, infrastructure, people).

### What was already good (kept)

- Logical order: language → UI → framework → runtime → backend → data → APIs → security → design
- Depth in the right places: event loop, MVCC, isolation levels, backpressure, idempotency
- Multi-tenancy as a recurring thread (routing, request context, row-level security)
- Up-to-date topics: React Compiler, Cache Components, passkeys, Standard Schema

### Gaps found and fixes applied

| # | Gap in the original | Fix |
|---|---------------------|-----|
| 1 | No browser or network fundamentals. React started without the rendering pipeline, HTTP, TLS, or CSS. | New **Part 02: The Web Platform** |
| 2 | Infrastructure squeezed into two chapters (containers in Node, deployment in system design). No Kubernetes, IaC, serverless, incident response, or cost. | New **Part 11: Cloud, DevOps & Delivery** |
| 3 | Nothing on architecture as a discipline: quality attributes, DDD, hexagonal, modular monolith, ADRs, legacy migration. "Clean Architecture" was one third of a testing chapter. | New **Part 13: Software Architecture** |
| 4 | No leadership content. The jump from senior to architect is mostly about decisions, writing, and influence. | New **Part 15: Technical Leadership & the Architect Role** |
| 5 | No AI engineering. In 2026, LLM features, RAG, agents, and MCP are standard full-stack work. | New **Part 14: AI Engineering for Full-Stack** |
| 6 | CI/CD lived inside the testing part. | Moved to Part 11 |
| 7 | Observability and deployment were in System Design as tools, mixing "how to operate" with "how to design". | Hands-on versions moved to Part 11. System Design gained **Multi-Region & Disaster Recovery** and a second case-study chapter. |
| 8 | No file uploads / object storage, a part of almost every real product. | New chapter 8.8 |
| 9 | No data lifecycle topics: CDC, analytics, zero-downtime data migration. | New chapter 7.14 |
| 10 | Supply chain, audit logging, and compliance were merged; privacy was missing. | Split into 9.12 and 9.13 |
| 11 | No data structures and complexity, needed for interviews and for performance reasoning. | New chapter 1.13 |
| 12 | No level markers; a mid-level reader could not tell core from advanced. | 🟢 🔵 🟣 tags on every chapter |
| 13 | No way to verify learning. | Project and exit criteria for every part, plus one capstone thread |

### Chapter number mapping (old → new)

| Original part | New part |
|---------------|----------|
| 01 JavaScript & TypeScript | 01 (plus 1.13) |
| — | 02 The Web Platform (new) |
| 02 React | 03 |
| 03 Next.js | 04 |
| 04 Node.js | 05 |
| 05 Express & NestJS | 06 |
| 06 Databases | 07 (plus 7.14) |
| 07 API Design & Messaging | 08 (plus 8.8) |
| 08 Security | 09 (8.12 split into 9.12 and 9.13) |
| 10 Testing & Code Quality | 10 (10.10 CI/CD → 11.6) |
| — | 11 Cloud, DevOps & Delivery (new; absorbs old 9.7, 9.8) |
| 09 System Design | 12 |
| — | 13 Software Architecture (new) |
| — | 14 AI Engineering (new) |
| — | 15 Technical Leadership (new) |

---

<a id="how-to"></a>
## How to use this path

1. **Self-assess first.** Read each chapter checklist. If you can explain every bullet out loud with an example, skip it.
2. **Follow the level tags.** Mid-level engineers: do all 🟢 first across Parts 01–10, then return for 🔵. Seniors aiming at architect: skim 🟢, do 🔵, then spend most time on 🟣 and Parts 11–15.
3. **Build, do not only read.** Each part has a project. All projects extend one product (see [capstone thread](#capstone)).
4. **Write as you learn.** For each part, write one short design note or ADR. Writing is the main skill of an architect.
5. **Teach it.** A topic is finished when you can explain it to a mid-level developer in five minutes.

<a id="timeline"></a>
### Suggested timeline (8–10 hours per week)

| Phase | Parts | Duration | Outcome |
|-------|-------|----------|---------|
| 1. Language and platform | 01, 02 | 6–8 weeks | You reason from first principles |
| 2. Frontend | 03, 04 | 7–9 weeks | You own a production Next.js app |
| 3. Backend | 05, 06 | 6–8 weeks | You own a production Node service |
| 4. Data and APIs | 07, 08 | 8–10 weeks | You design schemas and contracts |
| 5. Hardening | 09, 10, 11 | 9–11 weeks | You secure, test, ship, and operate |
| 6. Architect track | 12, 13, 14, 15 | 10–12 weeks | You design systems and lead decisions |

Total: roughly 11–14 months. A working senior can compress phases 1–3 heavily.

<a id="capstone"></a>
### Capstone project thread: "Acme Orders"

One multi-tenant B2B order-management SaaS, built up part by part:

- Tenants (companies), users with roles, products, orders, payments, notifications
- Next.js frontend, NestJS API, PostgreSQL, Redis, a queue, object storage
- Each part's project adds a layer; Part 12 ends with the full design at scale

---

<a id="part-01"></a>
## Part 01 — JavaScript & TypeScript

**Goal:** predict what any piece of JS/TS does and why, without running it.

#### 1.1 Values, Scope & Closures 🟢
- Primitives vs objects; copy by value vs sharing by reference; `structuredClone` · [MDN: Data types and data structures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Data_structures)
- `var` / `let` / `const`, hoisting, the temporal dead zone · [MDN: let and the temporal dead zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
- Lexical scope, the scope chain, block vs function vs module scope · [YDKJS: Scope & Closures (free book)](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/scope-closures/README.md)
- Closures: what is captured (bindings, not values), the loop-closure bug, stale closures · [MDN: Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures)
- Closure use cases: private state, factories, memoization; closures and memory retention · [javascript.info: Variable scope, closure](https://javascript.info/closure)

#### 1.2 Functions, "this" & Functional Techniques 🟢
- The four `this` binding rules (default, implicit, explicit, `new`) and arrow-function lexical `this` · [MDN: this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- `call`, `apply`, `bind`; losing `this` in callbacks and how to fix it · [MDN: Function.prototype.bind()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind)
- Higher-order functions, pure functions, immutability, referential transparency · [Eloquent JavaScript: Higher-order functions](https://eloquentjavascript.net/05_higher_order.html)
- Composition, currying, partial application; when functional style hurts readability · [javascript.info: Currying](https://javascript.info/currying-partials)
- Default, rest, and spread parameters; `arguments` and why to avoid it · [MDN: Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)

#### 1.3 Objects, Prototypes, Classes & Proxies 🔵
- Property descriptors, getters/setters, `Object.freeze` / `seal`, enumerable vs own properties · [MDN: Object.defineProperty()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)
- The prototype chain, `Object.create`, how `new` works step by step · [MDN: Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain)
- Classes as syntax over prototypes: fields, `#private`, `static`, accessors, `super` · [MDN: Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- Inheritance vs composition; mixins; why deep class trees fail · [javascript.info: Mixins](https://javascript.info/mixins)
- `Proxy` and `Reflect`: traps, use in reactivity and validation, performance cost · [MDN: Meta programming (Proxy and Reflect)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Meta_programming)
- `Symbol`, well-known symbols (`Symbol.iterator`, `Symbol.dispose`, `Symbol.toPrimitive`) · [MDN: Symbol](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)

#### 1.4 Types, Coercion, Numbers, Strings & Dates 🟢
- `==` vs `===` vs `Object.is`; the abstract coercion rules (`ToPrimitive`, `ToNumber`) · [MDN: Equality comparisons and sameness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness)
- Truthy/falsy, `??` vs `||`, optional chaining · [MDN: Nullish coalescing operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- IEEE-754 doubles: `0.1 + 0.2`, safe integer limits, `BigInt`, never floats for money · [MDN: Number (encoding and safe integers)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
- Strings: UTF-16, code points vs code units, graphemes, `Intl.Segmenter`, normalization · [MDN: String (UTF-16, code points, graphemes)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
- `Date` pitfalls, time zones, UTC storage, the `Temporal` API, `Intl` formatting · [MDN: Temporal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Temporal)

#### 1.5 Collections, Iterators & Generators 🟢
- `Array` methods and their complexity; mutating vs copying methods (`toSorted`, `toSpliced`, `with`) · [MDN: Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- `Map` vs object, `Set` and set methods, `WeakMap` / `WeakSet` / `WeakRef` use cases · [MDN: Keyed collections](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Keyed_collections)
- The iterable and iterator protocols; `for...of`; spread and destructuring over iterables · [MDN: Iteration protocols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols)
- Generators: lazy sequences, `yield*`, two-way communication · [MDN: Iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_generators)
- Iterator helpers (`map`, `filter`, `take` on iterators); async iterators and `for await` · [MDN: Iterator (helpers)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator)
- Typed arrays and `ArrayBuffer` basics · [MDN: Typed arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Typed_arrays)

#### 1.6 Asynchronous JavaScript: Event Loop, Promises & Async/Await 🔵
- Call stack, task queue, microtask queue; ordering of `setTimeout`, promises, `queueMicrotask` · [javascript.info: Event loop, microtasks and macrotasks](https://javascript.info/event-loop)
- Promise states, chaining, error propagation, unhandled rejections · [MDN: Using promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
- `Promise.all`, `allSettled`, `race`, `any`, `withResolvers`: when to use each · [MDN: Promise (concurrency methods)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- `async`/`await` desugaring; sequential vs parallel awaits; the `await`-in-loop trap · [MDN: async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
- Concurrency limiting (pools, semaphores), batching, debounce and throttle · [Node.js Learn: Asynchronous flow control](https://nodejs.org/learn/asynchronous-work/asynchronous-flow-control)
- Race conditions in async code: stale responses, check-then-act, re-entrancy · [React docs: Fetching data and race conditions](https://react.dev/learn/you-might-not-need-an-effect#fetching-data)

#### 1.7 Error Handling, Cancellation & Resource Management 🔵
- `Error` subclasses, `cause`, `AggregateError`; operational vs programmer errors · [MDN: Error cause](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error/cause)
- Throw vs return a result type; where to catch (boundaries, not everywhere) · [Node.js Best Practices: Error handling](https://github.com/goldbergyoni/nodebestpractices#2-error-handling-practices)
- `AbortController` / `AbortSignal`: timeouts, `AbortSignal.any`, propagating cancellation through layers · [MDN: AbortSignal](https://developer.mozilla.org/en-US/docs/Web/API/AbortSignal)
- `try/finally`, `using` and `await using` (explicit resource management), `DisposableStack` · [MDN: Resource management (using)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Resource_management)
- Retry with backoff and jitter; which errors are retryable · [AWS Architecture Blog: Exponential backoff and jitter](https://aws.amazon.com/blogs/architecture/exponential-backoff-and-jitter/)

#### 1.8 Modules: ESM, CommonJS & Bundling 🔵
- ESM semantics: static structure, live bindings, top-level `await`, cyclic imports · [MDN: JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
- CommonJS semantics; ESM/CJS interop, `require(esm)`, dual-package hazard · [Node.js docs: ESM and CommonJS interoperability](https://nodejs.org/api/esm.html#interoperability-with-commonjs)
- `package.json`: `exports`, `imports`, `type`, conditions, `sideEffects` · [Node.js docs: Package entry points](https://nodejs.org/api/packages.html#package-entry-points)
- Bundlers (Vite/Rolldown, Turbopack, esbuild): tree shaking, code splitting, dynamic `import()` · [Vite docs: Why Vite](https://vite.dev/guide/why)
- Source maps, transpilation targets, polyfills, browserslist · [web.dev: What are source maps?](https://web.dev/articles/source-maps)

#### 1.9 Memory, Garbage Collection & Runtime Performance 🔵
- Stack vs heap; reachability; generational GC (young/old space, scavenge, mark-sweep-compact) · [V8 blog: Trash talk (the Orinoco garbage collector)](https://v8.dev/blog/trash-talk)
- Common leaks: globals, forgotten timers and listeners, closures, unbounded caches, detached DOM · [Chrome DevTools: Fix memory problems](https://developer.chrome.com/docs/devtools/memory-problems)
- V8 internals that matter: hidden classes, inline caches, deoptimization, monomorphic vs polymorphic code · [V8 blog: Fast properties (hidden classes)](https://v8.dev/blog/fast-properties)
- Measuring: `performance.now`, `performance.mark`, DevTools Performance and Memory panels · [MDN: Performance APIs](https://developer.mozilla.org/en-US/docs/Web/API/Performance_API)
- Rule: measure first; algorithmic wins beat micro-optimizations · [Chrome DevTools: Analyze runtime performance](https://developer.chrome.com/docs/devtools/performance)

#### 1.10 TypeScript Foundations: Structural Typing, Inference & Narrowing 🟢
- Structural vs nominal typing; excess property checks; branded types for nominal behavior · [TS Handbook: Type compatibility](https://www.typescriptlang.org/docs/handbook/type-compatibility.html)
- Inference, widening, `as const`, `satisfies`; when to annotate · [TS Handbook: Type inference](https://www.typescriptlang.org/docs/handbook/type-inference.html)
- Unions, intersections, literal types, discriminated unions, exhaustiveness with `never` · [TS Handbook: Discriminated unions](https://www.typescriptlang.org/docs/handbook/2/narrowing.html#discriminated-unions)
- Narrowing: `typeof`, `in`, `instanceof`, type predicates, assertion functions · [TS Handbook: Narrowing](https://www.typescriptlang.org/docs/handbook/2/narrowing.html)
- `any` vs `unknown` vs `never`; `strict` flags and what each one catches · [TSConfig reference: strict](https://www.typescriptlang.org/tsconfig/#strict)

#### 1.11 Generics & Type-Level Programming 🔵
- Generic functions, constraints, defaults, `const` type parameters, `NoInfer` · [TS Handbook: Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html)
- `keyof`, indexed access, mapped types, key remapping, template literal types · [TS Handbook: Mapped types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)
- Conditional types, `infer`, distributive behavior · [TS Handbook: Conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
- Built-in utilities and how to write them: `Partial`, `Pick`, `Omit`, `ReturnType`, `Awaited` · [TS Handbook: Utility types](https://www.typescriptlang.org/docs/handbook/utility-types.html)
- Variance; function overloads vs unions · [TS Handbook: Function overloads](https://www.typescriptlang.org/docs/handbook/2/functions.html#function-overloads)
- 🟣 Limits: type complexity vs compile time and readability; when a simpler type is the better design · [TypeScript wiki: Performance](https://github.com/microsoft/TypeScript/wiki/Performance)

#### 1.12 TypeScript in Practice: tsconfig, Declaration Files & Runtime Validation 🔵
- Key `tsconfig` options: `strict`, `module`, `moduleResolution`, `target`, `verbatimModuleSyntax`, `isolatedModules`, `erasableSyntaxOnly` · [TSConfig reference](https://www.typescriptlang.org/tsconfig/)
- Project references, incremental builds, monorepo setups; running TS directly in Node (type stripping) · [TS Handbook: Project references](https://www.typescriptlang.org/docs/handbook/project-references.html)
- `.d.ts` files, `declare module`, module augmentation, typing third-party code · [TS Handbook: Declaration files](https://www.typescriptlang.org/docs/handbook/declaration-files/introduction.html)
- Types disappear at runtime: validate at boundaries with Zod / Valibot / ArkType; Standard Schema as the shared interface · [Standard Schema specification](https://standardschema.dev/)
- Derive types from schemas (one source of truth); typing environment variables and API responses · [Zod docs](https://zod.dev/)

#### 1.13 Data Structures, Algorithms & Complexity in Practice 🟢 *(new)*
- Big-O for time and space; amortized cost; recognizing accidental O(n²) · [Big-O Cheat Sheet](https://www.bigocheatsheet.com/)
- Arrays, hash maps, sets, stacks, queues, heaps, trees, tries, graphs: when each fits · [JavaScript Algorithms and Data Structures (repo)](https://github.com/trekhleb/javascript-algorithms)
- Core techniques: two pointers, sliding window, binary search, BFS/DFS, recursion vs iteration, dynamic programming basics · [NeetCode roadmap (free problems by pattern)](https://neetcode.io/roadmap)
- Real uses: LRU cache, debouncing queues, topological sort for dependency graphs, tree diffing · [JavaScript Algorithms: LRU cache](https://github.com/trekhleb/javascript-algorithms/tree/master/src/data-structures/lru-cache)
- Interview practice: explain the approach before coding; state complexity; test edge cases · [Tech Interview Handbook: Coding interview techniques](https://www.techinterviewhandbook.org/coding-interview-techniques/)

**Part project:** build a typed utility library: `retry` with backoff and abort support, a concurrency-limited `pMap`, an LRU cache, and a small event emitter. Full strict types, tests, dual ESM/CJS publish.

**Exit criteria:** you can predict output ordering of mixed timers/promises, explain a memory leak from a heap snapshot, and write a conditional type with `infer` unaided.

---

<a id="part-02"></a>
## Part 02 — The Web Platform *(new)*

**Goal:** understand what the browser and the network do, so framework behavior stops being magic.

#### 2.1 How Browsers Work: Parsing, Rendering & the Main Thread 🟢
- Navigation to pixels: HTML parsing, DOM, CSSOM, style, layout, paint, composite · [MDN: How browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/How_browsers_work)
- Render-blocking CSS, parser-blocking scripts, `async` / `defer` / `type="module"` · [MDN: The script element (async, defer, module)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/script)
- The main thread, long tasks, frames and the 16 ms budget, `requestAnimationFrame`, `scheduler.yield` · [web.dev: Optimize long tasks](https://web.dev/articles/optimize-long-tasks)
- Reflow vs repaint; layout thrashing; compositor-only properties (`transform`, `opacity`) · [web.dev: Avoid large, complex layouts and layout thrashing](https://web.dev/articles/avoid-large-complex-layouts-and-layout-thrashing)
- Process model: site isolation, renderer vs browser process · [Chrome blog: Inside look at modern web browser (part 1)](https://developer.chrome.com/blog/inside-browser-part1)

#### 2.2 DOM, Events & Core Web APIs 🟢
- DOM traversal and mutation; event capture, bubbling, delegation; passive listeners · [MDN: Event bubbling](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Event_bubbling)
- Observers: `IntersectionObserver`, `ResizeObserver`, `MutationObserver` · [MDN: Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
- `fetch`, `Request` / `Response`, streams, `URL`, `URLSearchParams`, `FormData` · [MDN: Using the Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
- History and Navigation APIs; View Transitions API · [MDN: Navigation API](https://developer.mozilla.org/en-US/docs/Web/API/Navigation_API)
- Web Workers, `postMessage`, transferable objects; Web Components basics · [MDN: Using Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers)

#### 2.3 Networking: DNS, TCP, TLS & HTTP/1.1 → HTTP/3 🔵
- What happens on a request: DNS resolution, TCP handshake, TLS handshake, request, response · [What happens when... (repo)](https://github.com/alex/what-happens-when)
- TLS 1.3 basics: certificates, chain of trust, SNI, HSTS · [High Performance Browser Networking: TLS (free online)](https://hpbn.co/transport-layer-security-tls/)
- HTTP/1.1 limits (head-of-line blocking), HTTP/2 multiplexing, HTTP/3 over QUIC · [MDN: Evolution of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Evolution_of_HTTP)
- Connection reuse, keep-alive, resource hints (`preconnect`, `preload`, `fetchpriority`) · [web.dev: Preconnect and dns-prefetch](https://web.dev/articles/preconnect-and-dns-prefetch)
- Compression (gzip, Brotli, zstd); reading a waterfall in DevTools · [MDN: Compression in HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Compression)

#### 2.4 HTTP Caching 🔵
- `Cache-Control` directives: `max-age`, `s-maxage`, `no-cache`, `no-store`, `private`, `immutable` · [MDN: HTTP caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Caching)
- Validation: `ETag`, `Last-Modified`, conditional requests, `304` · [MDN: HTTP conditional requests](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Conditional_requests)
- `stale-while-revalidate`, `stale-if-error`, `Vary` · [web.dev: Keeping things fresh with stale-while-revalidate](https://web.dev/articles/stale-while-revalidate)
- Browser cache vs shared cache (CDN); cache keys; content-hashed filenames · [RFC 9111: HTTP Caching](https://www.rfc-editor.org/rfc/rfc9111)
- Back/forward cache (bfcache) and what breaks it · [web.dev: Back/forward cache](https://web.dev/articles/bfcache)

#### 2.5 Storage, Service Workers & Offline 🔵
- Cookies vs `localStorage` vs `sessionStorage` vs IndexedDB vs Cache API: capacity, sync/async, security · [web.dev: Storage for the web](https://web.dev/articles/storage-for-the-web)
- Storage partitioning and third-party cookie restrictions · [MDN: State partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/Guides/State_Partitioning)
- Service worker lifecycle; caching strategies (cache-first, network-first, stale-while-revalidate) · [MDN: Using Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers)
- PWA basics: manifest, installability, background sync, push · [MDN: Progressive web apps](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
- Offline-first and local-first trade-offs; conflict resolution overview (CRDT idea) · [Ink & Switch: Local-first software](https://www.inkandswitch.com/local-first/)

#### 2.6 Modern CSS & Layout 🟢
- Cascade, specificity, inheritance, cascade layers (`@layer`), `@scope` · [MDN: Introduction to the CSS cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Introduction)
- Box model, formatting contexts, stacking contexts, positioning · [MDN: Stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Positioned_layout/Stacking_context)
- Flexbox and Grid (including subgrid); intrinsic sizing; logical properties · [web.dev Learn CSS: Grid](https://web.dev/learn/css/grid)
- Container queries, `:has()`, native nesting, custom properties, `clamp()`, `color-mix()` · [MDN: CSS container queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Containment/Container_queries)
- Responsive strategy, fluid type, dark mode, `prefers-reduced-motion` · [web.dev: Learn Responsive Design](https://web.dev/learn/design/)

#### 2.7 Web Performance Fundamentals 🔵
- Core Web Vitals: LCP, INP, CLS: what each measures and typical causes · [web.dev: Web Vitals](https://web.dev/articles/vitals)
- Lab data vs field data (RUM); Lighthouse vs CrUX; percentiles (p75) · [web.dev: Why lab and field data can be different](https://web.dev/articles/lab-and-field-data-differences)
- Critical rendering path optimization; image formats and responsive images; font loading · [web.dev: Learn Performance (course)](https://web.dev/learn/performance/)
- JavaScript cost: download, parse, execute; code splitting; third-party script control · [V8 blog: The cost of JavaScript](https://v8.dev/blog/cost-of-javascript-2019)
- Performance budgets and how to enforce them in CI · [web.dev: Performance budgets 101](https://web.dev/articles/performance-budgets-101)

**Part project:** build a small app with **no framework**: client-side routing with the Navigation API, a service worker with offline support, and a Lighthouse score above 95. Write down every optimization and its measured effect.

**Exit criteria:** you can narrate everything that happens between typing a URL and first paint, and diagnose a slow page from a DevTools trace.

---

<a id="part-03"></a>
## Part 03 — React

**Goal:** understand React's model well enough to design component systems and fix any rendering bug.

#### 3.1 React's Mental Model: Components, JSX & Rendering 🟢
- UI as a function of state; declarative vs imperative · [React docs: Thinking in React](https://react.dev/learn/thinking-in-react)
- JSX compiles to element objects; elements vs components vs instances · [React docs: Writing markup with JSX](https://react.dev/learn/writing-markup-with-jsx)
- Render phase vs commit phase; rendering must be pure · [React docs: Keeping components pure](https://react.dev/learn/keeping-components-pure)
- What triggers a render: state change, parent render, context change · [React docs: Render and commit](https://react.dev/learn/render-and-commit)
- Strict Mode double invocation and what it reveals · [React docs: StrictMode](https://react.dev/reference/react/StrictMode)

#### 3.2 Reconciliation, Keys & Component Identity 🔵
- The diffing heuristics: same type at same position preserves state · [React docs: Preserving and resetting state](https://react.dev/learn/preserving-and-resetting-state)
- Keys: identity across renders; why index keys break; using `key` to reset state · [React docs: Rendering lists (keys)](https://react.dev/learn/rendering-lists)
- Fiber architecture overview: units of work, priority lanes, interruptible rendering · [React Fiber Architecture (acdlite)](https://github.com/acdlite/react-fiber-architecture)
- Defining components inside components (identity reset bug) · [React docs: static-components lint rule](https://react.dev/reference/eslint-plugin-react-hooks/lints/static-components)
- `<Activity>` for hiding UI while preserving state · [React docs: Activity](https://react.dev/reference/react/Activity)

#### 3.3 State: useState, useReducer & State Design 🟢
- State as a snapshot; batching; updater functions · [React docs: State as a snapshot](https://react.dev/learn/state-as-a-snapshot)
- Immutable updates for objects and arrays · [React docs: Updating objects in state](https://react.dev/learn/updating-objects-in-state)
- `useReducer` for complex transitions; reducers as state machines · [React docs: Extracting state logic into a reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)
- State design rules: minimal state, derive do not store, no duplicated or contradictory state · [React docs: Choosing the state structure](https://react.dev/learn/choosing-the-state-structure)
- Lifting state up vs colocating; controlled vs uncontrolled components; URL as state · [React docs: Sharing state between components](https://react.dev/learn/sharing-state-between-components)

#### 3.4 Effects, Refs & Synchronizing with External Systems 🔵
- Effects synchronize with external systems; they are not lifecycle hooks · [React docs: Synchronizing with effects](https://react.dev/learn/synchronizing-with-effects)
- Dependency arrays, cleanup, race conditions in fetching effects · [React docs: Lifecycle of reactive effects](https://react.dev/learn/lifecycle-of-reactive-effects)
- "You might not need an effect": derived values, event handlers, `key` resets · [React docs: You might not need an effect](https://react.dev/learn/you-might-not-need-an-effect)
- `useEffectEvent` for non-reactive logic inside effects · [React docs: useEffectEvent](https://react.dev/reference/react/useEffectEvent)
- Refs: mutable values, DOM access, `ref` as a prop, ref cleanup functions, `useImperativeHandle` · [React docs: Manipulating the DOM with refs](https://react.dev/learn/manipulating-the-dom-with-refs)
- `useLayoutEffect`, `useSyncExternalStore` for external stores · [React docs: useSyncExternalStore](https://react.dev/reference/react/useSyncExternalStore)

#### 3.5 Context, Composition & Component Patterns 🔵
- Context: what it solves (prop drilling) and its cost (every consumer re-renders) · [React docs: Passing data deeply with context](https://react.dev/learn/passing-data-deeply-with-context)
- Splitting contexts, memoizing values, state/dispatch separation · [React docs: Scaling up with reducer and context](https://react.dev/learn/scaling-up-with-reducer-and-context)
- Composition: `children`, slots, render props, compound components · [patterns.dev: Compound pattern](https://www.patterns.dev/react/compound-pattern/)
- Custom hooks as the unit of logic reuse; headless components · [React docs: Reusing logic with custom hooks](https://react.dev/learn/reusing-logic-with-custom-hooks)
- Polymorphic components, controlled/uncontrolled dual APIs, inversion of control · [Kent C. Dodds: Inversion of control](https://kentcdodds.com/blog/inversion-of-control)
- 🟣 Designing component APIs for a team: what to expose, what to hide · [Radix Primitives: Composition guide](https://www.radix-ui.com/primitives/docs/guides/composition)

#### 3.6 Server State & Data Fetching 🟢
- Server state vs client state: caching, staleness, ownership · [TanStack Query: Overview](https://tanstack.com/query/latest/docs/framework/react/overview)
- TanStack Query model: query keys, `staleTime` vs `gcTime`, background refetch, invalidation · [TanStack Query: Important defaults](https://tanstack.com/query/latest/docs/framework/react/guides/important-defaults)
- Mutations, optimistic updates, rollback; pagination and infinite queries · [TanStack Query: Optimistic updates](https://tanstack.com/query/latest/docs/framework/react/guides/optimistic-updates)
- Request waterfalls vs parallel fetching; prefetching; render-as-you-fetch · [TanStack Query: Request waterfalls](https://tanstack.com/query/latest/docs/framework/react/guides/request-waterfalls)
- The `use` hook with promises; when a framework data layer replaces a client cache · [React docs: use](https://react.dev/reference/react/use)

#### 3.7 Suspense, Transitions & Concurrent Rendering 🔵
- Suspense boundaries: fallbacks, nesting, placement strategy, avoiding layout shift · [React docs: Suspense](https://react.dev/reference/react/Suspense)
- `useTransition`, `startTransition`: urgent vs non-urgent updates, async transitions · [React docs: useTransition](https://react.dev/reference/react/useTransition)
- `useDeferredValue` for keeping input responsive · [React docs: useDeferredValue](https://react.dev/reference/react/useDeferredValue)
- Streaming SSR and selective hydration · [React Working Group: New Suspense SSR architecture](https://github.com/reactwg/react-18/discussions/37)
- Error boundaries with Suspense; reset and retry patterns · [React docs: Catching rendering errors with an error boundary](https://react.dev/reference/react/Component#catching-rendering-errors-with-an-error-boundary)

#### 3.8 Forms & Actions: useActionState, useOptimistic & Validation 🟢
- `<form action>` with functions; progressive enhancement · [React docs: form](https://react.dev/reference/react-dom/components/form)
- `useActionState` for pending state and results; `useFormStatus` · [React docs: useActionState](https://react.dev/reference/react/useActionState)
- `useOptimistic` for instant feedback and automatic revert · [React docs: useOptimistic](https://react.dev/reference/react/useOptimistic)
- Validation: shared schema on client and server; field vs form errors; accessible error display · [Next.js docs: Forms guide (validation)](https://nextjs.org/docs/app/guides/forms)
- When to use React Hook Form or TanStack Form; complex forms (wizards, dynamic arrays) · [React Hook Form: Get started](https://react-hook-form.com/get-started)

#### 3.9 Client State Management at Scale 🔵
- Classify state first: server, URL, form, local UI, global UI · [React docs: Managing state](https://react.dev/learn/managing-state)
- Stores: Zustand, Redux Toolkit, Jotai; selectors and subscription granularity · [Zustand docs](https://zustand.docs.pmnd.rs/)
- State machines and statecharts (XState) for complex flows · [XState docs](https://stately.ai/docs/xstate)
- Signals: the idea and how it differs from React's model · [TC39 Signals proposal](https://github.com/tc39/proposal-signals)
- 🟣 Choosing for a team: boring defaults, migration cost, avoiding one global store for everything · [Redux FAQ: When should I use Redux?](https://redux.js.org/faq/general#when-should-i-use-redux)

#### 3.10 Performance: React Compiler, Memoization & Profiling 🔵
- Why components re-render; when re-renders are actually a problem · [Josh Comeau: Why React re-renders](https://www.joshwcomeau.com/react/why-react-re-renders/)
- React Compiler: automatic memoization, the Rules of React it depends on, opting out · [React docs: React Compiler introduction](https://react.dev/learn/react-compiler/introduction)
- Manual `memo`, `useMemo`, `useCallback`: when still needed · [React docs: useMemo](https://react.dev/reference/react/useMemo)
- React DevTools Profiler, Performance tracks; finding the slow component · [React docs: React Performance tracks](https://react.dev/reference/dev-tools/react-performance-tracks)
- List virtualization, code splitting with `lazy`, moving state down, passing children · [Dan Abramov: Before you memo()](https://overreacted.io/before-you-memo/)
- Measuring INP for interactions · [web.dev: Interaction to Next Paint (INP)](https://web.dev/articles/inp)

#### 3.11 Accessibility, Styling & Design Systems 🔵
- Semantic HTML first; ARIA roles, states, and when not to use ARIA · [W3C: ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/)
- Keyboard navigation, focus management, focus traps, live regions; WCAG 2.2 AA · [W3C: WCAG 2.2 quick reference](https://www.w3.org/WAI/WCAG22/quickref/)
- Accessible primitives (React Aria, Radix, Base UI); testing with axe and a screen reader · [React Aria docs](https://react-spectrum.adobe.com/react-aria/)
- Styling options: CSS Modules, Tailwind, zero-runtime CSS-in-JS; trade-offs with Server Components · [Next.js docs: CSS](https://nextjs.org/docs/app/getting-started/css)
- Design tokens, theming, variants · [W3C Design Tokens Community Group](https://www.w3.org/community/design-tokens/)
- 🟣 Design system governance: versioning, contribution model, documentation, adoption · [Brad Frost: A design system governance process](https://bradfrost.com/blog/post/a-design-system-governance-process/)

**Part project:** Acme Orders admin UI: order table with filtering, sorting, and virtualization; an optimistic order-status update; a multi-step order form; fully keyboard accessible.

**Exit criteria:** you can explain any re-render from the Profiler, remove unnecessary effects from a codebase, and design a compound component API.

---

<a id="part-04"></a>
## Part 04 — Next.js

**Goal:** own a production Next.js application, including rendering, caching, and deployment decisions.

#### 4.1 App Router Architecture & Routing 🟢
- File conventions: `page`, `layout`, `template`, `loading`, `error`, `not-found`, `route`, `default` · [Next.js docs: Project structure](https://nextjs.org/docs/app/getting-started/project-structure)
- Dynamic, catch-all, and optional segments; route groups; private folders · [Next.js docs: Dynamic routes](https://nextjs.org/docs/app/api-reference/file-conventions/dynamic-routes)
- Parallel routes and intercepting routes (modals, dashboards) · [Next.js docs: Parallel routes](https://nextjs.org/docs/app/api-reference/file-conventions/parallel-routes)
- Navigation: `<Link>`, prefetching, `useRouter`, `redirect`, soft vs hard navigation · [Next.js docs: Linking and navigating](https://nextjs.org/docs/app/getting-started/linking-and-navigating)
- Async `params` and `searchParams`; typed routes · [Next.js docs: page.js (params, searchParams)](https://nextjs.org/docs/app/api-reference/file-conventions/page)

#### 4.2 Server Components, Client Components & Boundaries 🔵
- What Server Components are: run only on the server, zero client JS, can be async · [React docs: Server Components](https://react.dev/reference/rsc/server-components)
- `"use client"` marks a boundary, not a component type; everything imported below is client code · [Next.js docs: use client](https://nextjs.org/docs/app/api-reference/directives/use-client)
- The RSC payload and serialization rules for props · [Next.js docs: Server and Client Components](https://nextjs.org/docs/app/getting-started/server-and-client-components)
- Composition: passing Server Components as `children` to Client Components · [Next.js docs: Server and client boundary](https://nextjs.org/docs/app/guides/server-and-client-boundary)
- `server-only` / `client-only`; keeping secrets out of the bundle; context providers placement · [Next.js docs: Data security](https://nextjs.org/docs/app/guides/data-security)
- 🟣 Deciding the boundary: push `"use client"` to the leaves; measuring bundle impact · [Next.js docs: Package bundling](https://nextjs.org/docs/app/guides/package-bundling)

#### 4.3 Layouts, Loading, Error & Not-Found UI 🟢
- Nested layouts and partial rendering; layouts do not re-render on navigation · [Next.js docs: Layouts and pages](https://nextjs.org/docs/app/getting-started/layouts-and-pages)
- `loading.tsx` as a Suspense boundary; granular `<Suspense>` for streaming · [Next.js docs: loading.js](https://nextjs.org/docs/app/api-reference/file-conventions/loading)
- `error.tsx`, `global-error.tsx`, recovery; `notFound()`, `forbidden()`, `unauthorized()` · [Next.js docs: Error handling](https://nextjs.org/docs/app/getting-started/error-handling)
- Skeleton design that avoids layout shift · [Next.js docs: Streaming](https://nextjs.org/docs/app/guides/streaming)

#### 4.4 Data Fetching & Rendering Strategies 🔵
- Fetch in Server Components close to where data is used; request deduplication with `cache()` · [Next.js docs: Fetching data](https://nextjs.org/docs/app/getting-started/fetching-data)
- Parallel vs sequential fetching; avoiding waterfalls; preloading · [React docs: cache](https://react.dev/reference/react/cache)
- Static vs dynamic rendering; what makes a route dynamic (`cookies`, `headers`, `searchParams`) · [Next.js docs: Rendering philosophy](https://nextjs.org/docs/app/guides/rendering-philosophy)
- Streaming; Partial Prerendering: static shell plus dynamic holes · [Next.js docs: Optimizing the static shell](https://nextjs.org/docs/app/guides/optimizing-the-static-shell)
- `generateStaticParams`; the data access layer pattern and DTOs · [Next.js docs: generateStaticParams](https://nextjs.org/docs/app/api-reference/functions/generate-static-params)

#### 4.5 Caching: Cache Components, "use cache" & Revalidation 🔵
- The Cache Components model: dynamic by default, cache by opting in · [Next.js docs: Caching](https://nextjs.org/docs/app/getting-started/caching)
- `"use cache"` on files, components, and functions; how cache keys are derived from arguments · [Next.js docs: use cache](https://nextjs.org/docs/app/api-reference/directives/use-cache)
- `cacheLife` profiles and `cacheTag` · [Next.js docs: cacheLife](https://nextjs.org/docs/app/api-reference/functions/cacheLife)
- Invalidation: `revalidateTag`, `updateTag` (read-your-writes), `revalidatePath`, `refresh` · [Next.js docs: Revalidating](https://nextjs.org/docs/app/getting-started/revalidating)
- Client router cache behavior; runtime vs build-time caching · [Next.js docs: Instant navigation](https://nextjs.org/docs/app/guides/instant-navigation)
- 🟣 Designing a tagging scheme per entity and tenant; debugging stale data; cache stampede risks · [Next.js docs: How revalidation works](https://nextjs.org/docs/app/guides/how-revalidation-works)

#### 4.6 Server Actions & Mutations 🟢
- `"use server"`: actions are public HTTP endpoints, so authenticate, authorize, and validate in each · [Next.js docs: use server](https://nextjs.org/docs/app/api-reference/directives/use-server)
- Calling from forms and event handlers; pending and optimistic UI · [Next.js docs: Mutating data](https://nextjs.org/docs/app/getting-started/mutating-data)
- Returning errors vs throwing; revalidation and redirect after mutation · [Next.js docs: Interactive apps (pending and optimistic UI)](https://nextjs.org/docs/app/guides/interactive-apps)
- Security: closures and encrypted bound values, CSRF protections, rate limiting · [Next.js docs: Server Actions deep dive](https://nextjs.org/docs/app/guides/server-actions)
- When to use a Route Handler instead · [Next.js docs: Route Handlers](https://nextjs.org/docs/app/getting-started/route-handlers)

#### 4.7 Route Handlers & Backend-for-Frontend Patterns 🔵
- `route.ts`: HTTP methods, Web `Request` / `Response`, streaming responses · [Next.js docs: route.js](https://nextjs.org/docs/app/api-reference/file-conventions/route)
- Webhook endpoints: raw body, signature verification · [Stripe docs: Receive webhooks](https://docs.stripe.com/webhooks)
- BFF pattern: aggregation, token handling, hiding internal services · [Next.js docs: Backend for Frontend](https://nextjs.org/docs/app/guides/backend-for-frontend)
- 🟣 Next.js as full backend vs Next.js in front of a separate API: decision criteria · [Sam Newman: Backends For Frontends](https://samnewman.io/patterns/architectural/bff/)

#### 4.8 Proxy (Middleware), Authentication & Multi-Tenant Routing 🔵
- `proxy.ts` (formerly middleware): what belongs there (redirects, rewrites, headers) and what does not (heavy logic, full auth) · [Next.js docs: proxy.js](https://nextjs.org/docs/app/api-reference/file-conventions/proxy)
- Auth architecture: session cookie, optimistic check in proxy, real check in the data access layer · [Next.js docs: Authentication](https://nextjs.org/docs/app/guides/authentication)
- Auth libraries (Auth.js, Better Auth) and hosted providers; protecting pages, actions, and handlers · [Auth.js: Getting started](https://authjs.dev/getting-started)
- Multi-tenancy: subdomain and custom-domain routing via rewrites; tenant resolution; tenant-scoped caching · [Next.js docs: Multi-tenant](https://nextjs.org/docs/app/guides/multi-tenant)

#### 4.9 Metadata, SEO, Internationalization, Images & Fonts 🟢
- Metadata API, `generateMetadata`, Open Graph images, `sitemap`, `robots`, structured data · [Next.js docs: Metadata and OG images](https://nextjs.org/docs/app/getting-started/metadata-and-og-images)
- i18n: locale routing, message loading, formatting with `Intl`, RTL support · [Next.js docs: Internationalization](https://nextjs.org/docs/app/guides/internationalization)
- `next/image`: sizing, `sizes`, priority, formats, remote patterns · [Next.js docs: Image component](https://nextjs.org/docs/app/api-reference/components/image)
- `next/font`: self-hosting, subsetting, avoiding layout shift; `next/script` strategies · [Next.js docs: Font module](https://nextjs.org/docs/app/api-reference/components/font)

#### 4.10 Performance & Core Web Vitals 🔵
- Bundle analysis; `dynamic()` imports; reducing client JS · [Next.js docs: Lazy loading](https://nextjs.org/docs/app/guides/lazy-loading)
- Improving LCP (priority images, streaming), INP (less hydration, transitions), CLS (reserved space) · [Next.js docs: Production checklist](https://nextjs.org/docs/app/guides/production-checklist)
- Turbopack; build performance in large apps · [Next.js docs: Turbopack](https://nextjs.org/docs/app/api-reference/turbopack)
- Field monitoring: `useReportWebVitals`, RUM, OpenTelemetry instrumentation · [Next.js docs: OpenTelemetry](https://nextjs.org/docs/app/guides/open-telemetry)

#### 4.11 Deployment, Self-Hosting & Production Security 🔵
- Deployment targets: managed platform, Node server, Docker `standalone` output, static export, adapters · [Next.js docs: Deploying](https://nextjs.org/docs/app/getting-started/deploying)
- Self-hosting concerns: shared cache handler across instances, image optimization, streaming through proxies · [Next.js docs: Self-hosting](https://nextjs.org/docs/app/guides/self-hosting)
- Environment variables: build-time vs runtime, `NEXT_PUBLIC_` exposure · [Next.js docs: Environment variables](https://nextjs.org/docs/app/guides/environment-variables)
- Security headers, CSP with nonces, Server Action allowed origins, data tainting · [Next.js docs: Content Security Policy](https://nextjs.org/docs/app/guides/content-security-policy)
- 🟣 Cost and lock-in analysis of platform choice; multi-region considerations · [Next.js docs: Deploying to platforms](https://nextjs.org/docs/app/guides/deploying-to-platforms)

**Part project:** Acme Orders storefront and dashboard on Next.js: tenant subdomains, cached catalog with tag invalidation, Server Action mutations, auth, i18n in two languages, deployed with Docker.

**Exit criteria:** for any route you can state what is static, cached, or dynamic and why, and you can explain exactly what invalidates each cached piece.

---

<a id="part-05"></a>
## Part 05 — Node.js

**Goal:** understand the runtime well enough to diagnose production problems from first principles.

#### 5.1 Node Architecture: V8, libuv & Event Loop Phases 🔵
- Components: V8, libuv, C++ bindings, core JS modules · [libuv docs: Design overview](https://docs.libuv.org/en/v1.x/design.html)
- Event loop phases: timers, pending callbacks, poll, check, close · [Node.js Learn: The event loop, timers and nextTick](https://nodejs.org/learn/asynchronous-work/event-loop-timers-and-nexttick)
- `process.nextTick` vs promise microtasks vs `setImmediate` vs `setTimeout(0)` · [Node.js Learn: Understanding setImmediate()](https://nodejs.org/learn/asynchronous-work/understanding-setimmediate)
- What is truly async in the kernel (network) vs the thread pool (fs, DNS lookup, crypto, zlib) · [libuv docs: Thread pool](https://docs.libuv.org/en/v1.x/threadpool.html)
- Differences from the browser event loop · [Node.js Learn: Differences between Node.js and the browser](https://nodejs.org/learn/getting-started/differences-between-nodejs-and-the-browser)

#### 5.2 Blocking Code, the Thread Pool & Worker Threads 🔵
- How one CPU-heavy request stalls all others; measuring event-loop delay and utilization · [Node.js Learn: Don't block the event loop](https://nodejs.org/learn/asynchronous-work/dont-block-the-event-loop)
- Typical blockers: large `JSON.parse`, sync APIs, catastrophic regex (ReDoS), big loops · [OWASP: Regular expression denial of service (ReDoS)](https://owasp.org/www-community/attacks/Regular_expression_Denial_of_Service_-_ReDoS)
- Thread pool size (`UV_THREADPOOL_SIZE`) and saturation · [Node.js docs: UV_THREADPOOL_SIZE](https://nodejs.org/api/cli.html#uv_threadpool_sizesize)
- Worker threads: `MessageChannel`, transferables, `SharedArrayBuffer`, `Atomics`, worker pools (Piscina) · [Node.js docs: Worker threads](https://nodejs.org/api/worker_threads.html)
- Partitioning work vs offloading to a queue · [Node.js Learn: Comparing Node.js concurrency models](https://nodejs.org/learn/concurrency/comparing-nodejs-concurrency-models)

#### 5.3 Buffers, Encodings & Binary Data 🟢
- `Buffer` and `Uint8Array`; allocation (`alloc` vs `allocUnsafe`) · [Node.js docs: Buffer](https://nodejs.org/api/buffer.html)
- Encodings: UTF-8, base64, base64url, hex; multi-byte characters split across chunks · [Node.js docs: Buffers and character encodings](https://nodejs.org/api/buffer.html#buffers-and-character-encodings)
- Endianness; parsing binary protocols; `TextEncoder` / `TextDecoder` · [MDN: Endianness](https://developer.mozilla.org/en-US/docs/Glossary/Endianness)
- `Blob`, `File`, and `ArrayBuffer` interop · [MDN: Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob)

#### 5.4 Streams & Backpressure 🔵
- Readable, Writable, Duplex, Transform; flowing vs paused; object mode · [Node.js Learn: How to use streams](https://nodejs.org/learn/modules/how-to-use-streams)
- Backpressure: `highWaterMark`, `write()` return value, `drain` · [Node.js Learn: Backpressuring in streams](https://nodejs.org/learn/modules/backpressuring-in-streams)
- `pipeline()` and `stream/promises` over `.pipe()` for error handling and cleanup · [Node.js docs: stream.pipeline()](https://nodejs.org/api/stream.html#streampipelinesource-transforms-destination-options)
- Async iteration over streams; Web Streams interop · [Node.js docs: Web Streams API](https://nodejs.org/api/webstreams.html)
- Use cases: large file processing, CSV/JSON streaming, proxying, compression · [Node.js docs: zlib (streaming compression)](https://nodejs.org/api/zlib.html)

#### 5.5 File System & Process I/O 🟢
- `fs/promises`, file handles, atomic writes (write temp then rename), file watching · [Node.js docs: fs promises API](https://nodejs.org/api/fs.html#promises-api)
- Path handling, `import.meta.dirname`, path traversal prevention · [Node.js docs: path](https://nodejs.org/api/path.html)
- `process`: `argv`, `env`, `stdin` / `stdout` / `stderr`, exit codes, signals · [Node.js docs: process](https://nodejs.org/api/process.html)
- Built-ins worth knowing: `--env-file`, `--watch`, `node:test`, `parseArgs`, the permission model · [Node.js docs: Command-line options](https://nodejs.org/api/cli.html)

#### 5.6 EventEmitter, Async Hooks & AsyncLocalStorage 🔵
- `EventEmitter`: synchronous emit, the special `error` event, listener leaks, `once`, `on` as async iterator · [Node.js docs: Events](https://nodejs.org/api/events.html)
- `EventTarget` in Node · [Node.js docs: EventTarget and Event API](https://nodejs.org/api/events.html#eventtarget-and-event-api)
- `AsyncLocalStorage`: request-scoped context (request ID, tenant, user) without passing parameters · [Node.js docs: Asynchronous context tracking](https://nodejs.org/api/async_context.html)
- Context loss pitfalls; performance cost; `diagnostics_channel` · [Node.js docs: Diagnostics channel](https://nodejs.org/api/diagnostics_channel.html)

#### 5.7 HTTP, Networking & the Fetch API 🔵
- `node:http` server internals: keep-alive, `headersTimeout`, `requestTimeout`, slow-client attacks · [Node.js Learn: Anatomy of an HTTP transaction](https://nodejs.org/learn/http/anatomy-of-an-http-transaction)
- Built-in `fetch` (undici): connection pooling, agents/dispatchers, timeouts, retries · [Node.js Learn: Fetch with Undici](https://nodejs.org/learn/getting-started/fetch)
- Sockets with `net` and `tls`; HTTP/2 basics · [Node.js docs: net](https://nodejs.org/api/net.html)
- DNS: `lookup` vs `resolve`, caching · [Node.js docs: DNS implementation considerations](https://nodejs.org/api/dns.html#implementation-considerations)
- Running behind a proxy: `X-Forwarded-*` headers, trust settings · [Express docs: Behind proxies](https://expressjs.com/en/guide/behind-proxies.html)

#### 5.8 Configuration, Logging & Error Strategy 🟢
- Twelve-factor config; validate env at startup and fail fast; separating secrets · [The Twelve-Factor App: Config](https://12factor.net/config)
- Structured JSON logging (Pino): levels, correlation IDs, redaction, child loggers · [Pino docs](https://getpino.io/)
- Error taxonomy: operational vs programmer; a central error handler · [Node.js Best Practices: Error handling](https://github.com/goldbergyoni/nodebestpractices#2-error-handling-practices)
- `uncaughtException` and `unhandledRejection`: log, then crash and restart · [Node.js docs: uncaughtException event](https://nodejs.org/api/process.html#event-uncaughtexception)

#### 5.9 Child Processes, Clustering & Scaling a Node Process 🔵
- `spawn`, `exec`, `execFile`, `fork`; stdio, IPC, shell-injection risk · [Node.js docs: Child process](https://nodejs.org/api/child_process.html)
- The `cluster` module vs multiple containers behind a load balancer · [Node.js docs: Cluster](https://nodejs.org/api/cluster.html)
- Statelessness requirements: externalized sessions, sticky sessions for WebSockets · [The Twelve-Factor App: Processes](https://12factor.net/processes)
- 🟣 Vertical vs horizontal scaling; sizing memory and CPU limits per instance · [Kubernetes docs: Resource management for containers](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/)

#### 5.10 Diagnostics: Profiling, Heap Snapshots & Memory Leaks 🔵
- `--inspect`, CPU profiles, flame graphs; finding hot paths · [Node.js Learn: Flame graphs](https://nodejs.org/learn/diagnostics/flame-graphs)
- Heap snapshots: the three-snapshot technique, retainers, allocation timelines · [Node.js Learn: Using heap snapshot](https://nodejs.org/learn/diagnostics/memory/using-heap-snapshot)
- `perf_hooks`: event-loop delay histogram, `PerformanceObserver` · [Node.js docs: Performance measurement APIs](https://nodejs.org/api/perf_hooks.html)
- Heap limits (`--max-old-space-size`), OOM kills in containers, diagnostic reports · [Node.js Learn: Understanding and tuning memory](https://nodejs.org/learn/diagnostics/memory/understanding-and-tuning-memory)
- Safe production profiling · [Node.js Learn: Profiling Node.js applications](https://nodejs.org/learn/getting-started/profiling)

#### 5.11 Graceful Shutdown, Health Checks & Running in Containers 🟢
- Handling `SIGTERM`: stop accepting, drain in-flight requests, close DB and queue connections, exit · [Express docs: Health checks and graceful shutdown](https://expressjs.com/en/advanced/healthcheck-graceful-shutdown.html)
- Liveness vs readiness vs startup probes; what each should check · [Kubernetes docs: Liveness, readiness and startup probes](https://kubernetes.io/docs/concepts/workloads/pods/probes/)
- Docker: multi-stage builds, slim or distroless images, non-root user, PID 1 and signal forwarding · [OWASP: Node.js Docker cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/NodeJS_Docker_Cheat_Sheet.html)
- Memory and CPU limits vs Node's view of resources; using the lockfile for reproducible installs · [Node.js Docker image: Best practices](https://github.com/nodejs/docker-node/blob/main/docs/BestPractices.md)

**Part project:** a streaming CSV order-import service: handles files larger than memory, applies backpressure, offloads validation to a worker pool, carries a request ID through `AsyncLocalStorage`, and shuts down gracefully.

**Exit criteria:** you can find a memory leak and an event-loop block in a running service using only profiling tools.

---

<a id="part-06"></a>
## Part 06 — Express & NestJS

**Goal:** build and structure backend services that a team can maintain for years.

#### 6.1 Express Internals: Middleware, Routing & the Request Lifecycle 🟢
- The middleware chain: `(req, res, next)`, ordering, short-circuiting · [Express docs: Using middleware](https://expressjs.com/en/guide/using-middleware.html)
- Router, mounting, path matching in Express 5 · [Express docs: Routing](https://expressjs.com/en/guide/routing.html)
- Body parsing, static files, common middleware (helmet, cors, compression) · [Express docs: Middleware modules](https://expressjs.com/en/resources/middleware.html)
- Express 5 changes: rejected promises forwarded to the error handler · [Express docs: Migrating to Express 5](https://expressjs.com/en/guide/migrating-5.html)
- Landscape awareness: Fastify (schemas, speed), Hono (Web standards, edge); when each fits · [NestJS docs: Nest vs Fastify, Express and Hono](https://docs.nestjs.com/faq/nest-vs-fastify-express-hono)

#### 6.2 Express Error Handling, Validation & Project Structure 🟢
- Error middleware (four arguments); mapping domain errors to HTTP responses · [Express docs: Error handling](https://expressjs.com/en/guide/error-handling.html)
- Request validation with a schema library; typed request handlers · [Zod docs](https://zod.dev/)
- Layering: routes → controllers → services → repositories · [Node.js Best Practices: Layer your components](https://github.com/goldbergyoni/nodebestpractices/blob/master/sections/projectstructre/createlayers.md)
- Dependency injection without a framework; testability; app vs server separation · [Martin Fowler: Inversion of control containers and dependency injection](https://martinfowler.com/articles/injection.html)

#### 6.3 NestJS Architecture: Modules, Providers & Dependency Injection 🔵
- Modules: `imports`, `providers`, `exports`; feature, shared, global, and dynamic modules · [NestJS docs: Modules](https://docs.nestjs.com/modules)
- The DI container: tokens, `useClass` / `useValue` / `useFactory`, custom providers · [NestJS docs: Custom providers](https://docs.nestjs.com/fundamentals/dependency-injection)
- Injection scopes: singleton, request, transient, and the cost of request scope · [NestJS docs: Injection scopes](https://docs.nestjs.com/fundamentals/provider-scopes)
- Circular dependencies: causes, `forwardRef`, and the real fix (restructure) · [NestJS docs: Circular dependency](https://docs.nestjs.com/fundamentals/circular-dependency)
- Lifecycle hooks; `ModuleRef`; lazy-loaded modules · [NestJS docs: Lifecycle events](https://docs.nestjs.com/fundamentals/lifecycle-events)
- 🟣 Module boundaries as architecture: mapping modules to business capabilities · [Martin Fowler: Bounded Context](https://martinfowler.com/bliki/BoundedContext.html)

#### 6.4 Controllers, DTOs & Validation with Standard Schema 🟢
- Controllers, route decorators, parameter decorators, custom decorators · [NestJS docs: Controllers](https://docs.nestjs.com/controllers)
- DTOs as the API boundary; never expose entities directly · [NestJS docs: Serialization](https://docs.nestjs.com/application/serialization)
- Validation approaches: `class-validator` + `ValidationPipe` vs schema-first (Zod, Valibot) through Standard Schema · [NestJS docs: Validation (class-validator and Standard Schema)](https://docs.nestjs.com/application/validation)
- Transformation, whitelisting unknown fields, response serialization · [NestJS docs: Pipes](https://docs.nestjs.com/pipes)
- OpenAPI generation from DTOs or schemas · [NestJS docs: OpenAPI introduction](https://docs.nestjs.com/openapi/introduction)

#### 6.5 The Request Pipeline: Middleware, Guards, Interceptors, Pipes & Filters 🔵
- Exact order: middleware → guards → interceptors (before) → pipes → handler → interceptors (after) → exception filters · [NestJS docs: Request lifecycle](https://docs.nestjs.com/faq/request-lifecycle)
- Guards for authentication and authorization; `ExecutionContext`, `Reflector`, metadata · [NestJS docs: Guards](https://docs.nestjs.com/guards)
- Interceptors: logging, timeouts, caching, response mapping (RxJS basics) · [NestJS docs: Interceptors](https://docs.nestjs.com/interceptors)
- Pipes for validation and transformation; exception filters for consistent error shapes · [NestJS docs: Exception filters](https://docs.nestjs.com/exception-filters)
- Binding levels: global, controller, method · [NestJS docs: Middleware](https://docs.nestjs.com/middlewares)

#### 6.6 Configuration, Request Context & Multi-Tenancy in NestJS 🔵
- `ConfigModule`, validated config, typed namespaces · [NestJS docs: Configuration](https://docs.nestjs.com/application/configuration)
- Request context with `AsyncLocalStorage` (for example `nestjs-cls`) instead of request-scoped providers · [NestJS docs: Async Local Storage](https://docs.nestjs.com/recipes/async-local-storage)
- Tenant resolution: subdomain, header, or token claim · [OWASP: Multi-tenant security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Multi_Tenant_Security_Cheat_Sheet.html)
- Tenant-aware data access; durable providers; preventing cross-tenant leaks in caches and logs · [NestJS docs: Durable providers](https://docs.nestjs.com/fundamentals/provider-scopes#durable-providers)

#### 6.7 Data Access in NestJS 🔵
- Choosing Prisma, Drizzle, TypeORM, or MikroORM: trade-offs · [NestJS docs: Data overview](https://docs.nestjs.com/data/overview)
- Repository pattern; keeping persistence out of domain logic · [Martin Fowler: Repository](https://martinfowler.com/eaaCatalog/repository.html)
- Transactions across services: unit of work, transactional context via ALS · [Prisma docs: Transactions](https://www.prisma.io/docs/orm/fundamentals/transactions)
- Migrations in deployment; connection pool lifecycle; testing against a real database · [The Twelve-Factor App: Admin processes (run migrations as one-off tasks)](https://12factor.net/admin-processes)

#### 6.8 Background Jobs, Scheduling & Queues 🔵
- BullMQ: queues, workers, concurrency, retries with backoff, delayed and repeatable jobs · [NestJS docs: Queues](https://docs.nestjs.com/application/queues)
- Idempotent job handlers; dead-letter handling; poison messages · [BullMQ docs: Idempotent jobs](https://docs.bullmq.io/patterns/idempotent-jobs)
- Cron scheduling and distributed locking so a job runs once across instances · [NestJS docs: Task scheduling](https://docs.nestjs.com/application/task-scheduling)
- Flows and job dependencies; running workers as separate processes; queue monitoring · [BullMQ docs: Flows](https://docs.bullmq.io/guide/flows)

#### 6.9 Microservices & Transports 🔵
- Nest microservice transports: TCP, Redis, NATS, RabbitMQ, Kafka, gRPC · [NestJS docs: Microservices overview](https://docs.nestjs.com/microservices/basics)
- Request-response vs event patterns; hybrid applications · [NestJS docs: Hybrid application](https://docs.nestjs.com/faq/hybrid-application)
- Serialization, timeouts, retries, error propagation across services · [NestJS docs: Resilience](https://docs.nestjs.com/reliability/resilience)
- 🟣 Start with a modular monolith; extraction criteria; the distributed monolith failure mode · [Martin Fowler: Monolith First](https://martinfowler.com/bliki/MonolithFirst.html)

#### 6.10 NestJS in Production: Observability, Performance & Upgrades 🔵
- OpenTelemetry tracing, metrics, health checks (Terminus), structured logs · [NestJS docs: OpenTelemetry](https://docs.nestjs.com/observability/opentelemetry)
- Fastify adapter; caching; compression; rate limiting (`@nestjs/throttler`) · [NestJS docs: Performance (Fastify)](https://docs.nestjs.com/http/performance)
- Graceful shutdown hooks; startup time; memory profile · [NestJS docs: Health checks (Terminus)](https://docs.nestjs.com/reliability/terminus)
- API versioning; planning major-version upgrades; dependency hygiene · [NestJS docs: Versioning](https://docs.nestjs.com/http/versioning)

**Part project:** the Acme Orders API in NestJS: tenant-aware modules for orders, products, and users; validated DTOs; a guard-based permission system; BullMQ jobs for emails; OpenAPI docs.

**Exit criteria:** you can draw the Nest request pipeline from memory and justify every module boundary in your project.

---

<a id="part-07"></a>
## Part 07 — Databases, Caching & Data Modeling

**Goal:** design schemas that survive growth, and explain any slow query or concurrency bug.

#### 7.1 Relational Fundamentals & Data Modeling 🟢
- Relations, primary and foreign keys, cardinality (1:1, 1:N, M:N) · [PostgreSQL docs: Constraints (primary and foreign keys)](https://www.postgresql.org/docs/current/ddl-constraints.html)
- Normalization (1NF–3NF) and deliberate denormalization · [Wikipedia: Database normalization](https://en.wikipedia.org/wiki/Database_normalization)
- Entity modeling from requirements; ER diagrams · [CMU 15-445: Database Systems (free course)](https://15445.courses.cs.cmu.edu/)
- Key choice: serial vs UUIDv4 vs UUIDv7 / ULID, natural vs surrogate keys · [RFC 9562: UUIDs (including UUIDv7)](https://www.rfc-editor.org/rfc/rfc9562)
- Modeling patterns: soft delete, audit columns, temporal data, polymorphic associations, trees · [PostgreSQL wiki: Don't Do This](https://wiki.postgresql.org/wiki/Don%27t_Do_This)

#### 7.2 SQL Mastery: Joins, CTEs, Window Functions & Aggregation 🟢
- Join types, including anti-join, semi-join, and `LATERAL` · [PostgreSQL docs: Table expressions (joins, LATERAL)](https://www.postgresql.org/docs/current/queries-table-expressions.html)
- `GROUP BY`, `HAVING`, `FILTER`, grouping sets · [PostgreSQL docs: Aggregate functions tutorial](https://www.postgresql.org/docs/current/tutorial-agg.html)
- CTEs and recursive CTEs (hierarchies, graphs) · [PostgreSQL docs: WITH queries (CTEs)](https://www.postgresql.org/docs/current/queries-with.html)
- Window functions: `ROW_NUMBER`, `RANK`, `LAG` / `LEAD`, frames, running totals · [PostgreSQL docs: Window functions tutorial](https://www.postgresql.org/docs/current/tutorial-window.html)
- `INSERT ... ON CONFLICT` (upsert), `RETURNING`, `MERGE`; NULL semantics and three-valued logic · [PostgreSQL docs: INSERT (ON CONFLICT, RETURNING)](https://www.postgresql.org/docs/current/sql-insert.html)

#### 7.3 Schema Design, Constraints & Migrations 🔵
- Data types: `numeric` for money, `timestamptz`, `jsonb`, arrays, enums vs lookup tables · [PostgreSQL docs: Data types](https://www.postgresql.org/docs/current/datatype.html)
- Constraints: `NOT NULL`, `UNIQUE`, `CHECK`, foreign keys, exclusion constraints · [PostgreSQL docs: Constraints](https://www.postgresql.org/docs/current/ddl-constraints.html)
- Zero-downtime migrations: the expand → migrate → contract pattern · [Martin Fowler: Parallel Change (expand and contract)](https://martinfowler.com/bliki/ParallelChange.html)
- Dangerous operations: table rewrites, long locks, `CREATE INDEX CONCURRENTLY`, `NOT VALID` constraints, `lock_timeout` · [PostgreSQL docs: CREATE INDEX (CONCURRENTLY)](https://www.postgresql.org/docs/current/sql-createindex.html)
- Batched backfills; migration tooling; rollback strategy · [strong_migrations: Catalog of dangerous migrations](https://github.com/ankane/strong_migrations)

#### 7.4 Indexes: How They Work & How to Choose Them 🔵
- B-tree structure; why column order matters in composite indexes; leftmost prefix · [Use The Index, Luke: Anatomy of an index](https://use-the-index-luke.com/sql/anatomy)
- Covering indexes (`INCLUDE`), index-only scans, partial indexes, expression indexes · [PostgreSQL docs: Index-only scans and covering indexes](https://www.postgresql.org/docs/current/indexes-index-only-scans.html)
- Other types: GIN (jsonb, full-text, arrays), GiST, BRIN, hash · [PostgreSQL docs: Index types](https://www.postgresql.org/docs/current/indexes-types.html)
- Selectivity and cardinality; when the planner ignores an index · [Use The Index, Luke: Concatenated keys](https://use-the-index-luke.com/sql/where-clause/the-equals-operator/concatenated-keys)
- Index cost: write overhead, bloat, unused index detection · [PostgreSQL wiki: Index maintenance](https://wiki.postgresql.org/wiki/Index_Maintenance)

#### 7.5 Query Planning & Performance Tuning 🔵
- Reading `EXPLAIN (ANALYZE, BUFFERS)`: scan types, join algorithms, estimated vs actual rows · [PostgreSQL docs: Using EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html)
- Statistics, `ANALYZE`, misestimates · [PostgreSQL docs: Statistics used by the planner](https://www.postgresql.org/docs/current/planner-stats.html)
- Finding slow queries with `pg_stat_statements`; the N+1 problem · [PostgreSQL docs: pg_stat_statements](https://www.postgresql.org/docs/current/pgstatstatements.html)
- Keyset pagination vs `OFFSET`; rewriting queries; materialized views · [Use The Index, Luke: No offset (keyset pagination)](https://use-the-index-luke.com/no-offset)
- Vacuum, autovacuum, bloat; key configuration (`work_mem`, `shared_buffers`) · [PostgreSQL docs: Routine vacuuming](https://www.postgresql.org/docs/current/routine-vacuuming.html)

#### 7.6 Transactions, Isolation Levels & MVCC 🔵
- ACID, precisely · [PostgreSQL docs: Transactions tutorial](https://www.postgresql.org/docs/current/tutorial-transactions.html)
- Anomalies: dirty read, non-repeatable read, phantom, lost update, write skew · [Jepsen: Consistency models and anomalies](https://jepsen.io/consistency)
- Isolation levels in PostgreSQL: Read Committed, Repeatable Read (snapshot), Serializable (SSI) · [PostgreSQL docs: Transaction isolation](https://www.postgresql.org/docs/current/transaction-iso.html)
- MVCC: row versions, snapshots, dead tuples, why long transactions hurt · [PostgreSQL docs: Introduction to MVCC](https://www.postgresql.org/docs/current/mvcc-intro.html)
- Serialization failures and retry loops; savepoints · [PostgreSQL docs: Serialization failure handling](https://www.postgresql.org/docs/current/mvcc-serialization-failure-handling.html)

#### 7.7 Locking, Concurrency Control & Idempotency 🔵
- Row locks: `SELECT ... FOR UPDATE`, `SKIP LOCKED` (job queues), `NOWAIT` · [PostgreSQL docs: SELECT (the locking clause)](https://www.postgresql.org/docs/current/sql-select.html)
- Table lock modes; deadlocks: detection and prevention by consistent ordering · [PostgreSQL docs: Explicit locking](https://www.postgresql.org/docs/current/explicit-locking.html)
- Optimistic concurrency with a version column vs pessimistic locking · [Martin Fowler: Optimistic Offline Lock](https://martinfowler.com/eaaCatalog/optimisticOfflineLock.html)
- Advisory locks; distributed locks and their limits (fencing tokens) · [Martin Kleppmann: How to do distributed locking](https://martin.kleppmann.com/2016/02/08/how-to-do-distributed-locking.html)
- Idempotency keys, unique constraints as guards, exactly-once *effects* · [Stripe blog: Designing robust APIs with idempotency](https://stripe.com/blog/idempotency)

#### 7.8 Multi-Tenancy Strategies & Row-Level Security 🟣
- Models: shared schema with `tenant_id`, schema per tenant, database per tenant: isolation, cost, operations · [Azure Architecture Center: Tenancy models](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/considerations/tenancy-models)
- PostgreSQL RLS: policies, setting tenant context per transaction, behavior with connection pooling · [PostgreSQL docs: Row security policies](https://www.postgresql.org/docs/current/ddl-rowsecurity.html)
- Tenant-leading indexes and unique constraints · [PostgreSQL docs: Multicolumn indexes](https://www.postgresql.org/docs/current/indexes-multicolumn.html)
- Noisy neighbors, per-tenant limits, tenant migration, sharding by tenant · [Azure Architecture Center: Noisy neighbor antipattern](https://learn.microsoft.com/en-us/azure/architecture/antipatterns/noisy-neighbor/noisy-neighbor)
- Per-tenant backup, export, and deletion · [Azure Architecture Center: Multitenant architecture overview](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/overview)

#### 7.9 ORMs, Query Builders & Connection Pooling 🔵
- ORM vs query builder vs raw SQL: Prisma, Drizzle, Kysely trade-offs · [Prisma Data Guide: SQL, query builders and ORMs compared](https://www.prisma.io/dataguide/types/relational/comparing-sql-query-builders-and-orms)
- Avoiding N+1; relation loading strategies; knowing the SQL your ORM emits · [Prisma docs: Relations and joins (loading strategies)](https://www.prisma.io/docs/orm/fundamentals/relations-and-joins)
- Pool sizing: why bigger is not better; `max_connections` · [HikariCP wiki: About pool sizing](https://github.com/brettwooldridge/HikariCP/wiki/About-Pool-Sizing)
- PgBouncer modes (session vs transaction) and their limits; pooling in serverless · [PgBouncer: Features (pooling modes)](https://www.pgbouncer.org/features.html)
- Timeouts at every level: statement, lock, idle-in-transaction · [PostgreSQL docs: Client connection defaults (timeouts)](https://www.postgresql.org/docs/current/runtime-config-client.html)

#### 7.10 Replication, Partitioning & Backups 🔵
- Streaming replication, sync vs async, replication lag, read-your-writes problems · [PostgreSQL docs: Log-shipping standby servers](https://www.postgresql.org/docs/current/warm-standby.html)
- Logical replication and its uses · [PostgreSQL docs: Logical replication](https://www.postgresql.org/docs/current/logical-replication.html)
- Failover and high availability; managed-service behavior · [PostgreSQL docs: High availability, load balancing and replication](https://www.postgresql.org/docs/current/high-availability.html)
- Table partitioning (range, list, hash), partition pruning, retention by dropping partitions · [PostgreSQL docs: Table partitioning](https://www.postgresql.org/docs/current/ddl-partitioning.html)
- Backups: base backups plus WAL, point-in-time recovery, RPO/RTO, restore drills · [PostgreSQL docs: Continuous archiving and PITR](https://www.postgresql.org/docs/current/continuous-archiving.html)

#### 7.11 Caching Patterns & Invalidation 🔵
- Patterns: cache-aside, read-through, write-through, write-behind · [Azure Architecture Center: Cache-Aside pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/cache-aside)
- TTL design, jitter, negative caching · [Redis docs: Key expiration](https://redis.io/docs/latest/develop/using-commands/keyspace/)
- Invalidation strategies: on write, event-driven, versioned keys · [Azure Architecture Center: Caching guidance](https://learn.microsoft.com/en-us/azure/architecture/best-practices/caching)
- Stampede protection: locking, request coalescing, stale-while-revalidate, probabilistic early expiry · [Wikipedia: Cache stampede](https://en.wikipedia.org/wiki/Cache_stampede)
- Cache layers (in-process, distributed, CDN) and consistency between them · [Redis docs: Client-side caching](https://redis.io/docs/latest/develop/reference/client-side-caching/)
- 🟣 Deciding what *not* to cache; cache as a liability when it hides a slow system · [Amazon Builders' Library: Caching challenges and strategies](https://aws.amazon.com/builders-library/caching-challenges-and-strategies/)

#### 7.12 Redis in Depth 🔵
- Data structures and their use cases: strings, hashes, lists, sets, sorted sets, streams, HyperLogLog · [Redis docs: Data types](https://redis.io/docs/latest/develop/data-types/)
- Single-threaded execution model; pipelining; transactions; Lua scripts and functions for atomicity · [Redis docs: Pipelining](https://redis.io/docs/latest/develop/using-commands/pipelining/)
- Expiry, eviction policies, memory analysis · [Redis docs: Key eviction](https://redis.io/docs/latest/develop/reference/eviction/)
- Persistence (RDB, AOF); replication, Sentinel, Cluster and hash slots · [Redis docs: Persistence](https://redis.io/docs/latest/operate/oss_and_stack/management/persistence/)
- Recipes: rate limiter, distributed lock (and its caveats), leaderboard, session store, pub/sub vs streams · [Redis docs: Distributed locks](https://redis.io/docs/latest/develop/clients/patterns/distributed-locks/)
- Ecosystem awareness: Valkey and managed alternatives · [Valkey documentation](https://valkey.io/topics/)

#### 7.13 NoSQL & Search: Document Stores, Key-Value & Full-Text Search 🔵
- Document databases (MongoDB): modeling by access pattern, embedding vs referencing · [MongoDB docs: Data modeling](https://www.mongodb.com/docs/manual/data-modeling/)
- Wide-column and key-value stores (DynamoDB): partition and sort keys, single-table design · [AWS docs: DynamoDB best practices](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html)
- Full-text search: PostgreSQL `tsvector` vs Elasticsearch / OpenSearch / Typesense; inverted index, analyzers, relevance (BM25) · [PostgreSQL docs: Full text search](https://www.postgresql.org/docs/current/textsearch.html)
- Vector search: `pgvector`, HNSW indexes, hybrid search · [pgvector (README)](https://github.com/pgvector/pgvector)
- Keeping a search index in sync with the source of truth · [Martin Kleppmann: Why dual writes are a bad idea](https://www.confluent.io/blog/using-logs-to-build-a-solid-data-infrastructure-or-why-dual-writes-are-a-bad-idea/)
- 🟣 Polyglot persistence: the operational cost of each extra datastore · [Martin Fowler: Polyglot Persistence](https://martinfowler.com/bliki/PolyglotPersistence.html)

#### 7.14 Data Lifecycle: CDC, Analytics & Zero-Downtime Data Migrations 🟣 *(new)*
- OLTP vs OLAP; columnar stores (ClickHouse, BigQuery, DuckDB); why not to run analytics on the primary · [DuckDB: Why DuckDB (OLAP vs OLTP)](https://duckdb.org/why_duckdb)
- Change data capture (Debezium, logical decoding); ETL vs ELT · [Debezium documentation](https://debezium.io/documentation/reference/stable/index.html)
- Migrating between databases or schemas live: dual writes, backfill, verification, cutover · [Stripe blog: Online migrations at scale](https://stripe.com/blog/online-migrations)
- Data retention, archiving, and deletion policies · [PostgreSQL docs: Table partitioning (retention by dropping partitions)](https://www.postgresql.org/docs/current/ddl-partitioning.html)
- Time-series data handling · [PostgreSQL docs: BRIN indexes (time-ordered data)](https://www.postgresql.org/docs/current/brin.html)

**Part project:** the Acme Orders schema: multi-tenant with RLS, an inventory reservation flow that is correct under concurrency (prove it with a test that runs 100 parallel orders), keyset pagination, a Redis cache with stampede protection, and one zero-downtime column migration.

**Exit criteria:** you can read any `EXPLAIN` plan, name the anomaly behind a concurrency bug, and choose the isolation level or lock that fixes it.

---

<a id="part-08"></a>
## Part 08 — API Design & Messaging

**Goal:** design contracts that are easy to use, hard to misuse, and safe to evolve.

#### 8.1 HTTP Semantics for API Designers 🟢
- Methods: safe, idempotent, cacheable; correct use of `PUT` vs `PATCH` vs `POST` · [RFC 9110: HTTP Semantics](https://www.rfc-editor.org/rfc/rfc9110)
- Status codes used precisely (`201`, `202`, `204`, `409`, `412`, `422`, `429`) · [MDN: HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status)
- Content negotiation; conditional requests with `ETag` / `If-Match` for optimistic concurrency · [MDN: HTTP conditional requests](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Conditional_requests)
- Caching headers for APIs; `Location`, `Retry-After`, `Link` · [MDN: Retry-After header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Retry-After)

#### 8.2 REST Resource Design, Pagination & Filtering 🟢
- Resource modeling, naming, nesting depth; actions that are not CRUD · [Azure Architecture Center: Web API design best practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- Pagination: offset vs cursor/keyset; stable ordering; response shape · [Stripe API: Pagination](https://docs.stripe.com/api/pagination)
- Filtering, sorting, field selection, expansion of related resources · [Google AIP-160: Filtering](https://google.aip.dev/160)
- Bulk operations; long-running operations (`202` plus a status resource) · [Google AIP-151: Long-running operations](https://google.aip.dev/151)
- Consistent conventions for dates, money, enums, and IDs · [Zalando RESTful API guidelines](https://opensource.zalando.com/restful-api-guidelines/)

#### 8.3 Errors, Versioning, Idempotency & API Evolution 🔵
- Problem Details (RFC 9457): machine-readable error codes, validation error format · [RFC 9457: Problem Details for HTTP APIs](https://www.rfc-editor.org/rfc/rfc9457)
- Versioning strategies: URL, header, date-based; the cost of each · [Stripe API: Versioning](https://docs.stripe.com/api/versioning)
- Backward-compatible changes vs breaking changes; tolerant readers · [Google AIP-180: Backwards compatibility](https://google.aip.dev/180)
- `Idempotency-Key` implementation: storage, request fingerprint, replaying responses · [Stripe API: Idempotent requests](https://docs.stripe.com/api/idempotent_requests)
- Deprecation and sunset policy; communicating change to consumers · [RFC 8594: The Sunset HTTP header](https://www.rfc-editor.org/rfc/rfc8594)

#### 8.4 OpenAPI, Contracts & Documentation 🔵
- OpenAPI 3.1 structure; design-first vs code-first · [OpenAPI Initiative: Learn the specification](https://learn.openapis.org/)
- Generating typed clients and server stubs; contract linting (Spectral) · [openapi-typescript docs](https://openapi-ts.dev/)
- Breaking-change detection in CI · [oasdiff: OpenAPI breaking-change detection](https://github.com/oasdiff/oasdiff)
- Documentation that works: quick start, examples, error catalog, changelog · [Diátaxis documentation framework](https://diataxis.fr/)
- 🟣 API governance: style guide, review process, treating the API as a product · [Microsoft REST API guidelines](https://github.com/microsoft/api-guidelines)

#### 8.5 GraphQL: Schema Design, Resolvers & Performance 🔵
- Schema design: types, nullability, connections for pagination, mutation payloads, error modeling · [GraphQL docs: Schemas and types](https://graphql.org/learn/schema/)
- Resolvers and the N+1 problem; DataLoader batching · [DataLoader (README)](https://github.com/graphql/dataloader)
- Security and cost: depth and complexity limits, persisted queries · [OWASP: GraphQL cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html)
- Caching challenges; federation overview; subscriptions · [GraphQL docs: Caching](https://graphql.org/learn/caching/)
- 🟣 When GraphQL is the right choice (many clients, varied data needs) and when it is overhead · [GraphQL docs: Best practices](https://graphql.org/learn/best-practices/)

#### 8.6 RPC Styles: tRPC & gRPC 🔵
- tRPC: end-to-end types without code generation; best inside a TypeScript monorepo · [tRPC docs](https://trpc.io/docs)
- gRPC: Protocol Buffers, schema evolution rules, four streaming modes, deadlines, status codes · [gRPC docs: Core concepts](https://grpc.io/docs/what-is-grpc/core-concepts/)
- gRPC-Web and Connect; internal vs public API suitability · [Connect docs: Introduction](https://connectrpc.com/docs/introduction)
- 🟣 Choosing REST vs GraphQL vs RPC per boundary (public, BFF, service-to-service) · [Google Cloud blog: gRPC vs OpenAPI vs REST](https://cloud.google.com/blog/products/api-management/understanding-grpc-openapi-and-rest-and-when-to-use-them)

#### 8.7 Real-Time: Polling, SSE & WebSockets 🔵
- Short polling, long polling, Server-Sent Events, WebSockets, WebTransport: trade-offs · [javascript.info: Long polling](https://javascript.info/long-polling)
- SSE: reconnection, `Last-Event-ID`, proxy buffering issues · [MDN: Using server-sent events](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events)
- WebSockets: handshake, heartbeats, reconnection with backoff, authentication, backpressure · [MDN: Writing WebSocket client applications](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_client_applications)
- Scaling connections: sticky sessions, pub/sub backplane, connection limits · [Socket.IO docs: Using multiple nodes](https://socket.io/docs/v4/using-multiple-nodes/)
- Presence, ordering, and delivery guarantees; managed real-time services · [Socket.IO docs: Delivery guarantees](https://socket.io/docs/v4/delivery-guarantees)

#### 8.8 File Uploads, Object Storage & Media 🟢 *(new)*
- Object storage model (S3-compatible): buckets, keys, storage classes, lifecycle rules · [AWS docs: What is Amazon S3?](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
- Direct-to-storage uploads with presigned URLs; multipart and resumable uploads · [AWS docs: Uploading objects with presigned URLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/PresignedUrlUploadObject.html)
- Validation: size, type sniffing, malware scanning; never trust the client filename · [OWASP: File upload cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html)
- Serving: CDN, signed URLs for private content, range requests · [Azure Architecture Center: Valet Key pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/valet-key)
- Image and video processing pipelines; storing metadata in the database · [sharp: High-performance image processing](https://sharp.pixelplumbing.com/)

#### 8.9 Webhooks & Third-Party Integrations 🔵
- Receiving: signature verification (HMAC), replay protection, respond fast then process async, deduplicate · [OWASP: Webhook security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Webhook_Security_Cheat_Sheet.html)
- Sending: retries with backoff, signing, delivery logs, endpoint management, SSRF protection · [Standard Webhooks specification](https://www.standardwebhooks.com/)
- Integration resilience: timeouts, circuit breakers, vendor rate limits, sandbox testing · [Azure Architecture Center: Transient fault handling](https://learn.microsoft.com/en-us/azure/architecture/best-practices/transient-faults)
- Anti-corruption layer around third-party models; payment provider integration patterns · [Azure Architecture Center: Anti-corruption Layer pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/anti-corruption-layer)

#### 8.10 Messaging Fundamentals: Queues, Logs & Delivery Guarantees 🔵
- Queue (RabbitMQ, SQS) vs log (Kafka) semantics: consumption, retention, replay · [Jay Kreps: The Log](https://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying)
- At-most-once, at-least-once, and why exactly-once delivery is really idempotent processing · [RabbitMQ docs: Reliability guide](https://www.rabbitmq.com/docs/reliability)
- Ordering, partitions, consumer groups, rebalancing · [Apache Kafka docs: Introduction (topics, partitions, consumer groups)](https://kafka.apache.org/documentation/#intro_concepts_and_terms)
- Acknowledgements, visibility timeouts, dead-letter queues, poison messages · [AWS docs: SQS dead-letter queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html)
- Backpressure and consumer lag; message schema evolution · [Confluent docs: Schema evolution and compatibility](https://docs.confluent.io/platform/current/schema-registry/fundamentals/schema-evolution.html)

#### 8.11 Event-Driven Architecture: Outbox, Sagas & Event Sourcing 🟣
- The dual-write problem; transactional outbox; inbox for deduplication; CDC as an alternative · [microservices.io: Transactional outbox](https://microservices.io/patterns/data/transactional-outbox.html)
- Event types: notification, event-carried state transfer, domain vs integration events · [Martin Fowler: What do you mean by "Event-Driven"?](https://martinfowler.com/articles/201701-event-driven.html)
- Sagas: choreography vs orchestration, compensating actions; workflow engines (Temporal) · [Azure Architecture Center: Saga pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/saga)
- Event sourcing and CQRS: projections, snapshots, when the complexity is justified · [Azure Architecture Center: Event Sourcing pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing)
- Living with eventual consistency in the UI and in support processes · [Werner Vogels: Eventually consistent](https://www.allthingsdistributed.com/2008/12/eventually_consistent.html)

#### 8.12 Rate Limiting, Throttling & API Gateways 🔵
- Algorithms: fixed window, sliding window, token bucket, leaky bucket · [Cloudflare blog: How we built rate limiting (sliding window)](https://blog.cloudflare.com/counting-things-a-lot-of-different-things/)
- Distributed rate limiting with Redis; limit keys (user, tenant, IP, API key) · [Stripe blog: Scaling your API with rate limiters](https://stripe.com/blog/rate-limiters)
- Response contract: `429`, `Retry-After`, rate-limit headers · [MDN: 429 Too Many Requests](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/429)
- Quotas and plans; load shedding · [Amazon Builders' Library: Using load shedding to avoid overload](https://aws.amazon.com/builders-library/using-load-shedding-to-avoid-overload/)
- API gateway responsibilities: auth, routing, limits, transformation; gateway vs BFF vs service mesh · [microservices.io: API gateway pattern](https://microservices.io/patterns/apigateway.html)

**Part project:** a public Acme Orders API: OpenAPI-first, cursor pagination, idempotent order creation, Problem Details errors, signed outgoing webhooks with retries, an outbox publishing order events, presigned invoice uploads, per-tenant rate limits.

**Exit criteria:** you can review an API design and list its evolution risks, and you can explain why your order flow never loses or duplicates an event.

---

<a id="part-09"></a>
## Part 09 — Security & Authentication

**Goal:** think like an attacker, build like a defender, and make the secure path the default path.

#### 9.1 Threat Modeling & Security Principles 🔵
- Principles: least privilege, defense in depth, secure defaults, fail closed, zero trust · [OWASP: Secure product design cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Secure_Product_Design_Cheat_Sheet.html)
- Threat modeling with STRIDE; data-flow diagrams; trust boundaries · [OWASP: Threat modeling cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)
- OWASP Top 10 and API Security Top 10 as checklists · [OWASP Top 10](https://owasp.org/Top10/)
- Risk rating: likelihood × impact; accepting vs mitigating risk · [OWASP: Risk rating methodology](https://owasp.org/www-community/OWASP_Risk_Rating_Methodology)
- 🟣 Running a threat-modeling session for a new design · [Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/)

#### 9.2 Injection & Input Handling 🟢
- SQL injection and parameterized queries; ORM raw-query pitfalls · [OWASP: SQL injection prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
- NoSQL injection, command injection, path traversal, template injection · [OWASP: Injection prevention](https://cheatsheetseries.owasp.org/cheatsheets/Injection_Prevention_Cheat_Sheet.html)
- Validation (allow-list) vs sanitization vs output encoding: each has a different job · [OWASP: Input validation](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html)
- Prototype pollution, mass assignment, ReDoS · [OWASP: Prototype pollution prevention](https://cheatsheetseries.owasp.org/cheatsheets/Prototype_Pollution_Prevention_Cheat_Sheet.html)

#### 9.3 XSS, CSP & Browser Security 🔵
- Stored, reflected, and DOM-based XSS; what React escapes and what it does not (`dangerouslySetInnerHTML`, `href` URLs) · [OWASP: Cross-site scripting prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
- Sanitizing HTML (DOMPurify); Trusted Types · [MDN: Trusted Types API](https://developer.mozilla.org/en-US/docs/Web/API/Trusted_Types_API)
- Content Security Policy: nonces, hashes, `strict-dynamic`, report-only rollout · [MDN: Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP)
- Security headers: HSTS, `X-Content-Type-Options`, `frame-ancestors`, Referrer-Policy, Permissions-Policy · [OWASP: HTTP security response headers](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html)
- Subresource Integrity; third-party script risk · [MDN: Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Defenses/Subresource_Integrity)

#### 9.4 CSRF, CORS, Cookies & the Same-Origin Policy 🔵
- Origin vs site; what the same-origin policy actually blocks · [MDN: Same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Defenses/Same-origin_policy)
- CORS: simple vs preflighted requests, credentials, common misconfigurations · [MDN: Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS)
- Cookie attributes: `HttpOnly`, `Secure`, `SameSite`, `__Host-` prefix, partitioned cookies · [MDN: Using HTTP cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cookies)
- CSRF defenses: SameSite, tokens, Origin checks, Fetch Metadata · [OWASP: CSRF prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)
- Clickjacking; cross-origin isolation headers (COOP, COEP, CORP) · [OWASP: Clickjacking defense](https://cheatsheetseries.owasp.org/cheatsheets/Clickjacking_Defense_Cheat_Sheet.html)

#### 9.5 SSRF, Deserialization & Server-Side Attacks 🔵
- SSRF: cloud metadata endpoints, DNS rebinding, allow-lists, egress controls · [OWASP: SSRF prevention](https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html)
- Insecure deserialization; XXE; unsafe YAML · [OWASP: Deserialization](https://cheatsheetseries.owasp.org/cheatsheets/Deserialization_Cheat_Sheet.html)
- File upload attacks; zip bombs; open redirects · [OWASP: Unvalidated redirects and forwards](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html)
- HTTP request smuggling; cache poisoning; host header attacks · [PortSwigger Web Security Academy: HTTP request smuggling](https://portswigger.net/web-security/request-smuggling)

#### 9.6 Password Storage, Sessions & Session Security 🟢
- Hashing with Argon2id (or bcrypt/scrypt); salts, peppers, parameter tuning · [OWASP: Password storage](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html)
- Password policy per NIST: length over complexity, breached-password checks · [NIST SP 800-63B: Digital identity guidelines](https://pages.nist.gov/800-63-4/sp800-63b.html)
- Server-side sessions: ID entropy, storage, rotation on login, idle and absolute timeouts, revocation · [OWASP: Session management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html)
- Account-flow security: enumeration, reset tokens, email change, brute-force and credential-stuffing defenses · [OWASP: Forgot password](https://cheatsheetseries.owasp.org/cheatsheets/Forgot_Password_Cheat_Sheet.html)

#### 9.7 Tokens & JWT: Design and Pitfalls 🔵
- JWT structure; JWS vs JWE; signature algorithms (HS256, RS256, ES256, EdDSA) · [jwt.io: Introduction to JSON Web Tokens](https://jwt.io/introduction)
- Mandatory validation: `alg`, `iss`, `aud`, `exp`; key rotation via JWKS · [RFC 8725: JWT Best Current Practices](https://www.rfc-editor.org/rfc/rfc8725)
- Classic attacks: `alg: none`, algorithm confusion, weak secrets, `kid` injection · [PortSwigger Web Security Academy: JWT attacks](https://portswigger.net/web-security/jwt)
- Revocation problem: short-lived access tokens, refresh-token rotation with reuse detection · [Auth0 docs: Refresh token rotation](https://auth0.com/docs/secure/tokens/refresh-tokens/refresh-token-rotation)
- Token storage in browsers; the BFF pattern; when plain sessions are the better choice · [IETF draft: OAuth 2.0 for browser-based applications](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-browser-based-apps)

#### 9.8 OAuth 2 & OpenID Connect 🔵
- Roles and grants: Authorization Code with PKCE, Client Credentials, Device Code; why Implicit and Password grants are gone · [OAuth 2.0 Simplified (free online book)](https://www.oauth.com/)
- OAuth 2.1 direction and security best practices · [oauth.net: OAuth 2.1](https://oauth.net/2.1/)
- OIDC: ID token vs access token, UserInfo, discovery · [OpenID Foundation: How OpenID Connect works](https://openid.net/developers/how-connect-works/)
- `state`, `nonce`, exact redirect-URI matching · [RFC 9700: OAuth 2.0 Security Best Current Practice](https://www.rfc-editor.org/rfc/rfc9700)
- Enterprise SSO: SAML basics, SCIM provisioning · [OWASP: SAML security](https://cheatsheetseries.owasp.org/cheatsheets/SAML_Security_Cheat_Sheet.html)
- 🟣 Build vs buy identity (Keycloak, Auth0, Clerk, WorkOS): criteria and exit costs · [Keycloak documentation (open-source option to evaluate)](https://www.keycloak.org/documentation)

#### 9.9 MFA, Passkeys & WebAuthn 🔵
- Factors: TOTP, SMS weaknesses, push, hardware keys · [OWASP: Multifactor authentication](https://cheatsheetseries.owasp.org/cheatsheets/Multifactor_Authentication_Cheat_Sheet.html)
- WebAuthn: registration and authentication ceremonies, challenge, origin binding, attestation · [WebAuthn Guide](https://webauthn.guide/)
- Passkeys: synced vs device-bound, conditional UI (autofill), phishing resistance · [passkeys.dev: What are passkeys?](https://passkeys.dev/docs/intro/what-are-passkeys/)
- Recovery flows as the weakest link; step-up authentication for sensitive actions · [OWASP: Transaction authorization (step-up)](https://cheatsheetseries.owasp.org/cheatsheets/Transaction_Authorization_Cheat_Sheet.html)

#### 9.10 Authorization Models: RBAC, ABAC & ReBAC 🟣
- Authentication vs authorization; broken access control (IDOR/BOLA) as the top API risk · [OWASP API Security: Broken object level authorization](https://owasp.org/API-Security/editions/2023/en/0xa1-broken-object-level-authorization/)
- RBAC: roles, permissions, hierarchies, role explosion · [OWASP: Authorization cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html)
- ABAC and policy engines (OPA, Cedar); ReBAC and Zanzibar-style systems (OpenFGA, SpiceDB) · [Google Research: Zanzibar paper](https://research.google/pubs/zanzibar-googles-consistent-global-authorization-system/)
- Enforcement points: gateway, service, data layer (RLS); centralized policy vs scattered checks · [OWASP: Authorization patterns](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Patterns_Cheat_Sheet.html)
- Tenant isolation in authorization; testing permission matrices · [OWASP: Authorization testing automation](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Testing_Automation_Cheat_Sheet.html)

#### 9.11 Secrets, Cryptography Basics & Data Protection 🔵
- Secrets management: vaults, cloud secret managers, rotation, no secrets in git or images · [OWASP: Secrets management](https://cheatsheetseries.owasp.org/cheatsheets/Secrets_Management_Cheat_Sheet.html)
- Symmetric (AES-GCM) vs asymmetric (RSA, ECC) encryption; hashing vs MAC vs signature · [OWASP: Cryptographic storage](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html)
- Never invent crypto; use vetted libraries; secure randomness · [Node.js docs: Crypto](https://nodejs.org/api/crypto.html)
- Encryption in transit and at rest; envelope encryption with a KMS; field-level encryption · [Google Cloud KMS docs: Envelope encryption](https://cloud.google.com/kms/docs/envelope-encryption)
- Key rotation; constant-time comparison · [OWASP: Key management](https://cheatsheetseries.owasp.org/cheatsheets/Key_Management_Cheat_Sheet.html)

#### 9.12 Supply-Chain Security 🔵
- npm risks: typosquatting, malicious install scripts, compromised maintainers, dependency confusion · [OWASP: npm security](https://cheatsheetseries.owasp.org/cheatsheets/NPM_Security_Cheat_Sheet.html)
- Lockfiles, `npm ci`, pinning, minimum release age, auditing (`npm audit`, Socket, Snyk) · [npm docs: npm ci](https://docs.npmjs.com/cli/commands/npm-ci)
- SBOMs, provenance and signing (Sigstore, SLSA levels) · [SLSA: Security levels](https://slsa.dev/spec/v1.0/levels)
- CI/CD hardening: least-privilege tokens, OIDC to cloud, pinned actions, protected branches · [OWASP: GitHub Actions security](https://cheatsheetseries.owasp.org/cheatsheets/GitHub_Actions_Security_Cheat_Sheet.html)
- Container image scanning; automated updates (Renovate, Dependabot) · [OWASP: Vulnerable dependency management](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerable_Dependency_Management_Cheat_Sheet.html)

#### 9.13 Audit Logging, Privacy & Compliance 🟣
- Audit logs: who, what, when, where; immutability; tenant-visible audit trails · [OWASP: Logging cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html)
- Security monitoring and alerting on suspicious patterns · [OWASP: Logging vocabulary](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Vocabulary_Cheat_Sheet.html)
- Privacy: PII classification, data minimization, GDPR rights (access, deletion, portability), retention, residency · [GDPR full text (gdpr-info.eu)](https://gdpr-info.eu/)
- Compliance overview: SOC 2, ISO 27001, PCI DSS scope reduction, HIPAA awareness · [ISO/IEC 27001 overview](https://www.iso.org/standard/27001)
- Security incident response; secure SDLC and security champions · [NIST SP 800-61: Incident response](https://csrc.nist.gov/pubs/sp/800/61/r3/final)

**Part project:** harden Acme Orders: write a STRIDE threat model, add passkey login plus an OIDC provider, implement RBAC with tenant isolation tested by a permission matrix, add a strict CSP, and produce an audit log.

**Exit criteria:** you can attack your own application across the OWASP Top 10 and explain each defense in depth.

---

<a id="part-10"></a>
## Part 10 — Testing & Code Quality

**Goal:** a codebase the team can change quickly without fear.

#### 10.1 Testing Strategy & Philosophy 🔵
- What tests are for: confidence, design feedback, documentation · [Martin Fowler: The Practical Test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)
- Pyramid vs trophy vs honeycomb; choosing a shape for your architecture · [Kent C. Dodds: The Testing Trophy](https://kentcdodds.com/blog/the-testing-trophy-and-testing-classifications)
- Test behavior, not implementation; cost vs value of each test type · [Testing Library: Guiding principles](https://testing-library.com/docs/guiding-principles)
- Coverage as a signal, not a target; mutation testing · [Stryker Mutator docs](https://stryker-mutator.io/docs/)
- Flaky tests: causes, quarantine, zero-tolerance policy · [Google Testing Blog: Flaky tests at Google](https://testing.googleblog.com/2016/05/flaky-tests-at-google-and-how-we.html)
- 🟣 Defining a test strategy for a team and a risk-based test plan · [Martin Fowler: Testing strategies in a microservice architecture](https://martinfowler.com/articles/microservice-testing/)

#### 10.2 Unit Testing & Test Doubles 🟢
- Vitest / Jest / `node:test`; arrange-act-assert; naming; one reason to fail · [Vitest: Getting started](https://vitest.dev/guide/)
- Doubles: dummy, stub, spy, mock, fake, and the cost of over-mocking · [Martin Fowler: Mocks Aren't Stubs](https://martinfowler.com/articles/mocksArentStubs.html)
- Controlling time, randomness, and the network · [Vitest: Mocking](https://vitest.dev/guide/mocking)
- Design for testability: pure core, dependency injection · [Martin Fowler: Humble Object](https://martinfowler.com/bliki/HumbleObject.html)
- Property-based testing (fast-check); snapshot tests and their misuse · [fast-check docs](https://fast-check.dev/docs/introduction/)

#### 10.3 Integration Testing with Real Dependencies 🔵
- Testcontainers for PostgreSQL, Redis, and brokers · [Testcontainers for Node.js](https://node.testcontainers.org/)
- Isolation strategies: transaction rollback, truncate, schema or database per worker · [PostgreSQL docs: CREATE DATABASE (template databases for per-worker isolation)](https://www.postgresql.org/docs/current/sql-createdatabase.html)
- Test data: factories and builders over shared fixtures · [Node.js testing best practices (repo)](https://github.com/goldbergyoni/nodejs-testing-best-practices)
- Testing migrations, queue consumers, and transactional behavior · [Testcontainers: PostgreSQL module](https://node.testcontainers.org/modules/postgresql/)
- Keeping the integration suite fast and parallel · [Vitest: Improving performance](https://vitest.dev/guide/improving-performance)

#### 10.4 Testing APIs & Contracts 🔵
- HTTP-level tests with Supertest or framework injection; testing auth and error paths · [NestJS docs: Testing (unit and end-to-end)](https://docs.nestjs.com/fundamentals/unit-testing)
- Mocking outbound HTTP with MSW or nock · [Mock Service Worker docs](https://mswjs.io/docs/)
- Consumer-driven contract testing (Pact); provider verification · [Pact docs: Contract testing](https://docs.pact.io/)
- Schema-based testing against the OpenAPI document; backward-compatibility checks · [Schemathesis docs](https://schemathesis.readthedocs.io/)

#### 10.5 Testing React Components 🟢
- Testing Library principles: query by role and label, act like a user · [Testing Library: About queries](https://testing-library.com/docs/queries/about)
- `user-event`, async utilities, avoiding `act` warnings · [Testing Library: user-event](https://testing-library.com/docs/user-event/intro)
- MSW for network; testing hooks; testing forms and error states · [Kent C. Dodds: Stop mocking fetch](https://kentcdodds.com/blog/stop-mocking-fetch)
- Vitest browser mode vs jsdom; what to do about Server Components (test via E2E or as functions) · [Vitest: Browser mode](https://vitest.dev/guide/browser/)
- Accessibility assertions; visual regression testing (Storybook, Chromatic) · [Storybook docs: Writing tests](https://storybook.js.org/docs/writing-tests)

#### 10.6 End-to-End Testing with Playwright 🔵
- Locators, auto-waiting, web-first assertions · [Playwright docs: Locators](https://playwright.dev/docs/locators)
- Fixtures, authentication state reuse, API-seeded test data · [Playwright docs: Authentication](https://playwright.dev/docs/auth)
- Parallelism, sharding, retries, trace viewer · [Playwright docs: Parallelism](https://playwright.dev/docs/test-parallel)
- Network interception; visual comparisons; mobile emulation · [Playwright docs: Network](https://playwright.dev/docs/network)
- Scope: critical user journeys only; smoke tests against production · [Playwright docs: Best practices](https://playwright.dev/docs/best-practices)

#### 10.7 Performance, Load & Security Testing 🔵
- Load test types: smoke, load, stress, spike, soak; tools (k6, Artillery) · [Grafana k6 docs: Load test types](https://grafana.com/docs/k6/latest/testing-guides/test-types/)
- Realistic workload models; reading percentiles (p95, p99); coordinated omission · [Grafana k6 docs: Thresholds](https://grafana.com/docs/k6/latest/using-k6/thresholds/)
- Frontend performance testing with Lighthouse CI and budgets · [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci)
- SAST, DAST, dependency and secret scanning in the pipeline · [OWASP: CI/CD security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/CI_CD_Security_Cheat_Sheet.html)
- Chaos experiments and game days · [Principles of Chaos Engineering](https://principlesofchaos.org/)

#### 10.8 Code Quality: Linting, Formatting, Types & Code Review 🟢
- ESLint with typescript-eslint (type-aware rules), Biome / Oxlint, Prettier · [typescript-eslint: Linting with type information](https://typescript-eslint.io/getting-started/typed-linting/)
- Git hooks, conventional commits, strictness ratchets · [Conventional Commits](https://www.conventionalcommits.org/)
- Code review: what to look for, small PRs, tone, turnaround time, automation of the trivial · [Google Engineering Practices: Code review](https://google.github.io/eng-practices/review/)
- Complexity metrics and their limits; documentation standards · [Wikipedia: Cyclomatic complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity)
- 🟣 Setting engineering standards that teams actually follow · [Google TypeScript style guide](https://google.github.io/styleguide/tsguide.html)

#### 10.9 Refactoring & Technical Debt 🔵
- Code smells and the core refactorings; refactor in small, safe, tested steps · [Refactoring.Guru: Refactoring](https://refactoring.guru/refactoring)
- Characterization tests and seams for legacy code · [Understand Legacy Code](https://understandlegacycode.com/)
- Branch by abstraction; parallel change · [Martin Fowler: Branch By Abstraction](https://martinfowler.com/bliki/BranchByAbstraction.html)
- Classifying debt (deliberate vs accidental); a debt register · [Martin Fowler: Technical Debt Quadrant](https://martinfowler.com/bliki/TechnicalDebtQuadrant.html)
- 🟣 Making the business case for paying debt; refactor vs rewrite decision · [Joel Spolsky: Things you should never do (rewrites)](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/)

**Part project:** bring Acme Orders to a full test strategy: unit tests on domain logic, Testcontainers integration tests, a contract test between frontend and API, five Playwright journeys, and a k6 load test with a written report.

**Exit criteria:** you can defend where every type of test sits and why, and your CI suite is fast and not flaky.

---

<a id="part-11"></a>
## Part 11 — Cloud, DevOps & Delivery *(new)*

**Goal:** ship safely many times a day and operate what you ship.

#### 11.1 Linux, Networking & Cloud Primitives 🟢
- Linux essentials: processes, signals, file descriptors, permissions, `systemd`, basic debugging tools (`top`, `ss`, `curl`, `dig`, `strace`) · [MIT: The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)
- Networking: IP, CIDR, subnets, NAT, ports, firewalls, DNS record types · [Cloudflare Learning Center: What is DNS?](https://www.cloudflare.com/learning/dns/what-is-dns/)
- Cloud building blocks: compute, object storage, managed databases, queues, VPC, security groups · [AWS whitepaper: Overview of Amazon Web Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/introduction.html)
- IAM: principals, roles, policies, least privilege · [AWS docs: IAM security best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- Regions and availability zones; the shared responsibility model · [AWS: Shared responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/)

#### 11.2 Containers & Docker 🟢
- Images vs containers; layers and build cache; namespaces and cgroups in brief · [Docker docs: What is Docker?](https://docs.docker.com/get-started/docker-overview/)
- Dockerfile best practices: multi-stage, small base, non-root, `.dockerignore`, reproducible installs · [Docker docs: Building best practices](https://docs.docker.com/build/building/best-practices/)
- Networking, volumes, health checks; Docker Compose for local environments · [Docker docs: Docker Compose](https://docs.docker.com/compose/)
- Image tagging, registries, scanning, signing · [OWASP: Docker security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html)

#### 11.3 Kubernetes & Orchestration Essentials 🔵
- Core objects: Pod, Deployment, Service, Ingress / Gateway API, ConfigMap, Secret, Job, CronJob · [Kubernetes docs: Workloads](https://kubernetes.io/docs/concepts/workloads/)
- Requests and limits; probes; rolling updates; pod disruption budgets · [Kubernetes docs: Resource management for containers](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/)
- Autoscaling: HPA, KEDA (queue-based), cluster autoscaling · [Kubernetes docs: Autoscaling workloads](https://kubernetes.io/docs/concepts/workloads/autoscaling/)
- Helm or Kustomize; GitOps (Argo CD, Flux) · [Argo CD docs](https://argo-cd.readthedocs.io/en/stable/)
- 🟣 When Kubernetes is overkill: managed container platforms (ECS/Fargate, Cloud Run, Fly, Render) · [Google Cloud docs: What is Cloud Run?](https://cloud.google.com/run/docs/overview/what-is-cloud-run)

#### 11.4 Serverless, Edge & Managed Platforms 🔵
- Functions as a service: cold starts, concurrency model, limits, pricing · [AWS docs: Lambda execution environment lifecycle](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html)
- Edge runtimes: Web-standard APIs, constraints, good use cases · [Cloudflare docs: How Workers works](https://developers.cloudflare.com/workers/reference/how-workers-works/)
- Database access from serverless: pooling, HTTP drivers, serverless databases · [AWS docs: Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html)
- Event-driven patterns with managed queues, schedulers, and workflows · [AWS docs: What is Step Functions?](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html)
- 🟣 Serverless vs containers vs PaaS: cost curve, lock-in, operations burden · [Azure Architecture Center: Choose a compute service](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree)

#### 11.5 Infrastructure as Code & Environments 🔵
- Terraform / OpenTofu: providers, state, modules, plan and apply, drift · [Terraform docs: What is Terraform?](https://developer.hashicorp.com/terraform/intro)
- Alternatives: Pulumi, CDK, SST · [Pulumi docs: Concepts](https://www.pulumi.com/docs/iac/concepts/)
- Environment strategy: dev, preview per PR, staging, production; environment parity · [The Twelve-Factor App: Dev/prod parity](https://12factor.net/dev-prod-parity)
- Secrets and config per environment; policy as code · [Open Policy Agent docs](https://www.openpolicyagent.org/docs)

#### 11.6 CI/CD, Quality Gates & Release Engineering 🔵
- Pipeline design: fast feedback first, caching, parallelism, affected-only builds in monorepos · [GitHub docs: GitHub Actions](https://docs.github.com/en/actions)
- Quality gates: types, lint, tests, security scans, bundle and performance budgets · [GitHub docs: Code security](https://docs.github.com/en/code-security)
- Trunk-based development vs long-lived branches; merge queues · [Trunk Based Development](https://trunkbaseddevelopment.com/)
- Build once, promote the same artifact; database migrations in the pipeline · [The Twelve-Factor App: Build, release, run](https://12factor.net/build-release-run)
- Versioning, changelogs, release automation · [Semantic Versioning](https://semver.org/)
- DORA metrics: deployment frequency, lead time, change failure rate, time to restore · [DORA: Software delivery performance metrics](https://dora.dev/guides/dora-metrics-four-keys/)

#### 11.7 Deployment Strategies, Feature Flags & Progressive Delivery 🔵
- Rolling, blue-green, canary; automated rollback on SLO breach · [Martin Fowler: Canary Release](https://martinfowler.com/bliki/CanaryRelease.html)
- Feature flags: release, experiment, ops, and permission toggles; flag lifecycle and cleanup · [Martin Fowler: Feature Toggles](https://martinfowler.com/articles/feature-toggles.html)
- Separating deploy from release; dark launches; shadow traffic · [Martin Fowler: Dark Launching](https://martinfowler.com/bliki/DarkLaunching.html)
- Backward-compatible deploys: API and schema compatibility across versions (N and N-1) · [Martin Fowler: Parallel Change](https://martinfowler.com/bliki/ParallelChange.html)

#### 11.8 Observability in Practice: Logs, Metrics, Traces & SLOs 🔵
- Three pillars plus profiling; structured logs with correlation IDs · [OpenTelemetry docs: Observability primer](https://opentelemetry.io/docs/concepts/observability-primer/)
- Metrics: counters, gauges, histograms; RED and USE methods; cardinality control · [Grafana blog: The RED method](https://grafana.com/blog/2018/08/02/the-red-method-how-to-instrument-your-services/)
- Distributed tracing with OpenTelemetry: spans, context propagation, sampling · [OpenTelemetry docs: Traces](https://opentelemetry.io/docs/concepts/signals/traces/)
- SLI, SLO, error budgets; burn-rate alerting; alert on symptoms, not causes · [Google SRE Workbook: Alerting on SLOs](https://sre.google/workbook/alerting-on-slos/)
- Dashboards that answer questions; frontend observability (RUM, error tracking) · [Google SRE Book: Monitoring distributed systems](https://sre.google/sre-book/monitoring-distributed-systems/)

#### 11.9 Incident Response, On-Call & Postmortems 🟣
- Incident lifecycle: detect, triage, mitigate, resolve, learn · [Google SRE Book: Managing incidents](https://sre.google/sre-book/managing-incidents/)
- Roles: incident commander, communications, scribe; severity levels · [PagerDuty Incident Response documentation](https://response.pagerduty.com/)
- Mitigate first, diagnose second; rollback as the default move · [Google SRE Book: Emergency response](https://sre.google/sre-book/emergency-response/)
- Runbooks; on-call health and sustainable rotations · [Google SRE Book: Being on-call](https://sre.google/sre-book/being-on-call/)
- Blameless postmortems; contributing factors over "root cause"; tracking action items · [Google SRE Book: Postmortem culture](https://sre.google/sre-book/postmortem-culture/)

#### 11.10 Cost Engineering (FinOps) 🟣
- Cloud pricing models: compute, storage, data transfer (egress), managed-service premiums · [FinOps Foundation: What is FinOps?](https://www.finops.org/introduction/what-is-finops/)
- Unit economics: cost per tenant, per request, per order · [FinOps Framework: Unit economics](https://www.finops.org/framework/capabilities/unit-economics/)
- Right-sizing, autoscaling, reserved or committed use, spot instances · [AWS Well-Architected: Cost optimization pillar](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/welcome.html)
- Tagging, budgets, anomaly alerts · [FinOps Framework: Allocation](https://www.finops.org/framework/capabilities/allocation/)
- Cost as an architecture quality attribute in every design review · [Azure Well-Architected: Cost optimization](https://learn.microsoft.com/en-us/azure/well-architected/cost-optimization/)

**Part project:** take Acme Orders to production: Docker images, Terraform-managed infrastructure, a CI/CD pipeline with gates and preview environments, canary deploys behind a feature flag, OpenTelemetry tracing, two SLOs with alerts, and one simulated incident with a written postmortem.

**Exit criteria:** you can deploy on a Friday afternoon without stress, and you can answer "what does one order cost us?"

---

<a id="part-12"></a>
## Part 12 — System Design (Backend + Frontend)

**Goal:** design systems that meet stated requirements, and communicate the design clearly under time pressure.

#### 12.1 The System Design Method & Interview Framework 🔵
- A repeatable flow: clarify requirements → estimate → API → data model → high-level design → deep dives → bottlenecks and trade-offs · [System Design Primer: How to approach a system design question](https://github.com/donnemartin/system-design-primer#how-to-approach-a-system-design-interview-question)
- Functional vs non-functional requirements; turning vague goals into numbers · [Azure Well-Architected Framework: Pillars](https://learn.microsoft.com/en-us/azure/well-architected/pillars)
- Driving the conversation; managing time; drawing clear diagrams · [Hello Interview: System design delivery framework](https://www.hellointerview.com/learn/system-design/in-a-hurry/delivery)
- Stating trade-offs explicitly: "I choose X over Y because Z, at the cost of W" · [System Design Primer: Performance vs scalability and other trade-offs](https://github.com/donnemartin/system-design-primer#performance-vs-scalability)
- Common mistakes: jumping to a solution, over-engineering, ignoring data · [ByteByteGo: System Design 101 (repo)](https://github.com/ByteByteGoHq/system-design-101)

#### 12.2 Estimation & Capacity Planning 🔵
- Back-of-envelope math: QPS, storage, bandwidth, memory · [System Design Primer: Back-of-the-envelope calculations](https://github.com/donnemartin/system-design-primer#appendix)
- Numbers to memorize: latency of memory, SSD, network; powers of two; seconds per day · [Latency numbers every programmer should know](https://gist.github.com/jboner/2841832)
- Average vs peak load; read/write ratio; growth projection · [Google SRE Workbook: Managing load](https://sre.google/workbook/managing-load/)
- Latency budgets across a request path; headroom · [Google Research: The Tail at Scale](https://research.google/pubs/the-tail-at-scale/)
- Load testing to validate the estimate · [Grafana k6 docs: Load test types](https://grafana.com/docs/k6/latest/testing-guides/test-types/)

#### 12.3 Load Balancing, Reverse Proxies & CDNs 🔵
- Layer 4 vs layer 7 balancing; algorithms (round robin, least connections, consistent hashing) · [Google SRE Book: Load balancing at the frontend](https://sre.google/sre-book/load-balancing-frontend/)
- Health checks, connection draining, TLS termination · [Google SRE Book: Load balancing in the datacenter](https://sre.google/sre-book/load-balancing-datacenter/)
- Reverse proxy duties: routing, compression, buffering, caching · [nginx: Beginner's guide (reverse proxy)](https://nginx.org/en/docs/beginners_guide.html)
- CDN: edge caching, cache keys, purging, origin shielding, edge compute · [Cloudflare Learning Center: What is a CDN?](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/)
- Global traffic management: GeoDNS, anycast · [Cloudflare Learning Center: Anycast network](https://www.cloudflare.com/learning/cdn/glossary/anycast-network/)

#### 12.4 Scaling Data: Replication, Sharding & Consistency 🟣
- Read replicas and replication lag handling · [System Design Primer: Database (replication, federation, sharding)](https://github.com/donnemartin/system-design-primer#database)
- Sharding: key choice, hash vs range, hot partitions, resharding, cross-shard queries · [Azure Architecture Center: Sharding pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/sharding)
- Consistent hashing with virtual nodes · [Werner Vogels: Amazon's Dynamo (consistent hashing)](https://www.allthingsdistributed.com/2007/10/amazons_dynamo.html)
- Consistency models: strong, eventual, causal, read-your-writes, monotonic reads · [Jepsen: Consistency models](https://jepsen.io/consistency)
- Leader-follower, multi-leader, and leaderless replication; quorums; conflict resolution · [Distributed Systems for Fun and Profit: Replication](https://book.mixu.net/distsys/replication.html)

#### 12.5 Distributed Systems Fundamentals: CAP, PACELC, Consensus & Clocks 🟣
- The fallacies of distributed computing; partial failure · [Wikipedia: Fallacies of distributed computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)
- CAP in practice (the choice is made during a partition); PACELC (latency vs consistency otherwise) · [Martin Kleppmann: Please stop calling databases CP or AP](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html)
- Consensus: what Raft provides (leader election, replicated log) and where you rely on it (etcd, ZooKeeper) · [The Raft consensus algorithm](https://raft.github.io/)
- Time: clock skew, logical clocks, vector clocks, hybrid logical clocks · [Distributed Systems for Fun and Profit: Time and order](https://book.mixu.net/distsys/time.html)
- Why two-phase commit is avoided; split brain and fencing · [Cambridge: Distributed Systems lecture notes (Kleppmann)](https://www.cl.cam.ac.uk/teaching/2122/ConcDisSys/dist-sys-notes.pdf)

#### 12.6 Reliability Patterns: Timeouts, Retries, Circuit Breakers & Bulkheads 🔵
- Timeouts everywhere; deadline propagation · [Amazon Builders' Library: Timeouts, retries and backoff with jitter](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/)
- Retries with exponential backoff and jitter; retry budgets; retry storms · [Azure Architecture Center: Retry pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/retry)
- Circuit breakers; bulkheads; rate limiting and load shedding · [Azure Architecture Center: Circuit Breaker pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/circuit-breaker)
- Graceful degradation and fallbacks; idempotency as the enabler of retries · [Amazon Builders' Library: Avoiding fallback in distributed systems](https://aws.amazon.com/builders-library/avoiding-fallback-in-distributed-systems/)
- Backpressure across services; queues as buffers; failure-mode analysis · [Google SRE Book: Addressing cascading failures](https://sre.google/sre-book/addressing-cascading-failures/)

#### 12.7 Multi-Region, Availability & Disaster Recovery 🟣 *(new)*
- Availability math: nines, serial vs parallel dependencies · [Google SRE Book: Availability table](https://sre.google/sre-book/availability-table/)
- Single points of failure; redundancy across zones and regions · [Amazon Builders' Library: Static stability using Availability Zones](https://aws.amazon.com/builders-library/static-stability-using-availability-zones/)
- Active-passive vs active-active; data replication across regions; conflict handling · [AWS whitepaper: Disaster recovery options in the cloud](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)
- RPO and RTO; backup, pilot light, warm standby, hot standby · [AWS Well-Architected: Plan for disaster recovery](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/plan-for-disaster-recovery-dr.html)
- Data residency constraints; cell-based architecture; DR drills · [AWS Well-Architected: Cell-based architecture](https://docs.aws.amazon.com/wellarchitected/latest/reducing-scope-of-impact-with-cell-based-architecture/what-is-a-cell-based-architecture.html)

#### 12.8 Frontend Architecture: Rendering Strategies & Performance Budgets 🔵
- CSR, SSR, SSG, ISR, streaming, partial prerendering, islands, resumability: trade-off matrix · [web.dev: Rendering on the web](https://web.dev/articles/rendering-on-the-web)
- Choosing per page type (marketing, dashboard, feed, editor) · [patterns.dev: Rendering patterns](https://www.patterns.dev/)
- State and data architecture for large apps; API layer design; error and loading strategy · [Bulletproof React (architecture reference repo)](https://github.com/alan2207/bulletproof-react)
- Performance budgets tied to business metrics · [web.dev: Your first performance budget](https://web.dev/articles/your-first-performance-budget)
- Frontend system design interview format: requirements, component tree, data model, API, optimizations · [GreatFrontEnd: Front end system design playbook](https://www.greatfrontend.com/front-end-system-design-playbook)

#### 12.9 Frontend at Scale: Micro-Frontends, Monorepos & Design Systems 🟣
- Monorepos: Turborepo / Nx, task graph, remote cache, package boundaries, ownership · [monorepo.tools](https://monorepo.tools/)
- Micro-frontends: Module Federation, route-level composition; the costs (duplication, UX drift, coordination) · [Martin Fowler: Micro Frontends](https://martinfowler.com/articles/micro-frontends.html)
- Design system as a platform: tokens, components, versioning, adoption metrics · [Brad Frost: Atomic Design (free online book)](https://atomicdesign.bradfrost.com/table-of-contents/)
- Shared code strategy; dependency version policy · [pnpm docs: Catalogs (shared dependency versions)](https://pnpm.io/catalogs)
- Organizational fit: team autonomy vs consistency · [Martin Fowler: Conway's Law](https://martinfowler.com/bliki/ConwaysLaw.html)

#### 12.10 Case Studies I: Rate Limiter, Notification System, News Feed & Search 🔵
- Rate limiter: algorithm choice, distributed counters, failure behavior · [Stripe blog: Scaling your API with rate limiters](https://stripe.com/blog/rate-limiters)
- Notification system: channels, templates, preferences, retries, deduplication, priority · [Novu (open-source notification infrastructure): docs](https://docs.novu.co/)
- News feed: fan-out on write vs read, ranking, pagination, the celebrity problem · [System Design Primer: Design the Twitter timeline and search](https://github.com/donnemartin/system-design-primer/blob/master/solutions/system_design/twitter/README.md)
- Search and autocomplete: indexing pipeline, relevance, typeahead with tries or prefix indexes · [System Design Primer: Design a web crawler and search index](https://github.com/donnemartin/system-design-primer/blob/master/solutions/system_design/web_crawler/README.md)

#### 12.11 Case Studies II: Payments, Chat, File Storage & Multi-Tenant SaaS 🟣 *(new)*
- Payments and ledger: double-entry bookkeeping, idempotency, reconciliation, provider webhooks · [Modern Treasury: Accounting for developers](https://www.moderntreasury.com/journal/accounting-for-developers-part-i)
- Real-time chat and collaboration: connection gateway, ordering, presence, offline sync · [System Design (Karan Pratap Singh): WhatsApp case study](https://github.com/karanpratapsingh/system-design#whatsapp)
- File storage and sharing: chunking, deduplication, metadata service, permissions · [Dropbox Tech blog: Rewriting the heart of our sync engine](https://dropbox.tech/infrastructure/rewriting-the-heart-of-our-sync-engine)
- Multi-tenant SaaS platform: isolation tiers, tenant routing, per-tenant limits, billing metering · [Azure Architecture Center: SaaS and multitenant solution architecture](https://learn.microsoft.com/en-us/azure/architecture/guide/saas-multitenant-solution-architecture/)

#### 12.12 Capstone: Designing Acme Orders at Scale 🟣
- Requirements: 10,000 tenants, 50 million orders per month, 99.95% availability, EU and US data residency · [Azure Architecture Center: Multitenancy checklist](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/checklist)
- Full design: API, data model, service boundaries, sync and async flows · [The C4 model](https://c4model.com/)
- Scaling plan from 10 to 10,000 tenants: what changes at each stage · [System Design Primer: Scaling to millions of users on AWS](https://github.com/donnemartin/system-design-primer/blob/master/solutions/system_design/scaling_aws/README.md)
- Failure analysis, SLOs, security model, cost estimate · [AWS Well-Architected: Reliability pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)
- Deliverable: a design document with C4 diagrams and ADRs, presented in 45 minutes · [Malte Ubl: Design docs at Google](https://www.industrialempathy.com/posts/design-docs-at-google/)

**Part project:** the 12.12 capstone design document, reviewed by a peer or mentor.

**Exit criteria:** given any product prompt, you can produce a defensible design in 45 minutes and adapt it when requirements change.

---

<a id="part-13"></a>
## Part 13 — Software Architecture *(new)*

**Goal:** structure software so it stays cheap to change, and make trade-offs explicit.

#### 13.1 Architectural Thinking: Quality Attributes & Trade-Offs 🟣
- Architecture as the set of decisions that are expensive to change · [Martin Fowler: Software Architecture Guide](https://martinfowler.com/architecture/)
- Quality attributes: performance, scalability, availability, security, modifiability, testability, operability, cost · [ISO/IEC 25010 quality model](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)
- Quality attribute scenarios (stimulus, response, measure); architecturally significant requirements · [arc42 Quality Model (scenarios and examples)](https://quality.arc42.org/)
- Every decision is a trade-off; "it depends" must be followed by "on what" · [Azure Architecture Center: Design principles](https://learn.microsoft.com/en-us/azure/architecture/guide/design-principles/)
- Reversible vs irreversible decisions; deferring to the last responsible moment · [Amazon 2015 shareholder letter (one-way and two-way doors)](https://www.sec.gov/Archives/edgar/data/1018724/000119312516530910/d168744dex991.htm)

#### 13.2 Design Principles: Coupling, Cohesion & SOLID 🔵
- Coupling and cohesion as the core measures; connascence · [connascence.io](https://connascence.io/)
- SOLID applied pragmatically in TypeScript; dependency inversion in practice · [Wikipedia: SOLID](https://en.wikipedia.org/wiki/SOLID)
- Information hiding; deep vs shallow modules · [John Ousterhout: A Philosophy of Software Design (Talks at Google)](https://www.youtube.com/watch?v=bmSAYlu0NcY)
- DRY vs the wrong abstraction; YAGNI; rule of three · [Sandi Metz: The wrong abstraction](https://sandimetz.com/blog/2016/1/20/the-wrong-abstraction)
- The design patterns that still matter: strategy, adapter, decorator, observer, factory, repository · [Refactoring.Guru: Design patterns in TypeScript](https://refactoring.guru/design-patterns/typescript)

#### 13.3 Architecture Styles: Layered, Hexagonal, Clean & Vertical Slice 🔵
- Layered architecture and its failure modes · [Azure Architecture Center: N-tier architecture style](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier)
- Hexagonal (ports and adapters), onion, and clean architecture: the dependency rule · [Alistair Cockburn: Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture/)
- Vertical slice / feature-based structure · [Jimmy Bogard: Vertical slice architecture](https://www.jimmybogard.com/vertical-slice-architecture/)
- Applying each in NestJS and Next.js; folder structure follows architecture · [Domain-Driven Hexagon (NestJS reference repo)](https://github.com/Sairyss/domain-driven-hexagon)
- 🟣 Choosing by complexity: avoid heavy architecture for CRUD · [Martin Fowler: Yagni](https://martinfowler.com/bliki/Yagni.html)

#### 13.4 Domain-Driven Design: Strategic 🟣
- Ubiquitous language; subdomains (core, supporting, generic) and where to invest · [Eric Evans: DDD Reference (free PDF)](https://www.domainlanguage.com/ddd/reference/)
- Bounded contexts; context mapping (customer-supplier, conformist, anti-corruption layer, shared kernel) · [DDD Crew: Context mapping](https://github.com/ddd-crew/context-mapping)
- Discovery techniques: event storming, domain storytelling · [EventStorming](https://www.eventstorming.com/)
- Aligning contexts with teams · [DDD Crew: Starter modelling process](https://github.com/ddd-crew/ddd-starter-modelling-process)

#### 13.5 Domain-Driven Design: Tactical 🔵
- Entities, value objects, aggregates and invariants, aggregate sizing · [Martin Fowler: DDD Aggregate](https://martinfowler.com/bliki/DDD_Aggregate.html)
- Domain services, application services, repositories, factories · [Martin Fowler: Service Layer](https://martinfowler.com/eaaCatalog/serviceLayer.html)
- Domain events; the rich vs anemic model debate · [Martin Fowler: Anemic Domain Model](https://martinfowler.com/bliki/AnemicDomainModel.html)
- Making illegal states unrepresentable with TypeScript types · [F# for Fun and Profit: Making illegal states unrepresentable](https://fsharpforfunandprofit.com/posts/designing-with-types-making-illegal-states-unrepresentable/)

#### 13.6 Modular Monolith to Microservices 🟣
- Modular monolith: enforced boundaries, module APIs, separate schemas · [Kamil Grzybek: Modular monolith primer](https://www.kamilgrzybek.com/blog/posts/modular-monolith-primer)
- Reasons to split that are valid (independent scaling, team autonomy, fault isolation) and reasons that are not · [Martin Fowler: Microservices](https://martinfowler.com/articles/microservices.html)
- Decomposition by bounded context; data ownership; no shared database · [microservices.io: Decompose by subdomain](https://microservices.io/patterns/decomposition/decompose-by-subdomain.html)
- Costs: network, consistency, operations, testing, local development · [Martin Fowler: Microservice Trade-Offs](https://martinfowler.com/articles/microservice-trade-offs.html)
- Service granularity; distributed monolith warning signs · [Martin Fowler: Microservice Premium](https://martinfowler.com/bliki/MicroservicePremium.html)

#### 13.7 Evolutionary Architecture & Legacy Modernization 🟣
- Fitness functions: automated checks on architectural properties (dependency rules, performance budgets) · [Thoughtworks: Fitness function-driven development](https://www.thoughtworks.com/insights/articles/fitness-function-driven-development)
- Strangler fig, branch by abstraction, anti-corruption layers · [Martin Fowler: Strangler Fig](https://martinfowler.com/bliki/StranglerFigApplication.html)
- Incremental migration planning; running old and new in parallel; verification · [Azure Architecture Center: Strangler Fig pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/strangler-fig)
- Why big-bang rewrites fail; managing risk and stakeholder expectations · [Martin Fowler: Sacrificial Architecture](https://martinfowler.com/bliki/SacrificialArchitecture.html)
- Framework and major-version upgrade strategy · [React blog: React 19 upgrade guide (a model upgrade plan)](https://react.dev/blog/2024/04/25/react-19-upgrade-guide)

#### 13.8 Documenting Architecture: C4, ADRs & RFCs 🟣
- C4 model: context, container, component diagrams; diagrams as code (Mermaid, Structurizr) · [The C4 model](https://c4model.com/)
- Architecture Decision Records: context, decision, alternatives, consequences · [Architectural Decision Records (adr.github.io)](https://adr.github.io/)
- RFC / design-doc process: template, review, decision, follow-up · [Malte Ubl: Design docs at Google](https://www.industrialempathy.com/posts/design-docs-at-google/)
- arc42 overview; keeping docs alive next to the code · [arc42 template overview](https://arc42.org/overview)
- Writing for the audience: executive summary vs engineer detail · [Google: Technical writing courses](https://developers.google.com/tech-writing/overview)

#### 13.9 Governance, Platform Engineering & Developer Experience 🟣
- Golden paths and paved roads; internal developer platforms · [Martin Fowler: What I talk about when I talk about platforms](https://martinfowler.com/articles/talk-about-platforms.html)
- Standards vs autonomy; a tech radar (adopt, trial, assess, hold) · [Thoughtworks Technology Radar](https://www.thoughtworks.com/radar)
- Architecture review without becoming a gate; guardrails over approvals · [Martin Fowler: Scaling the practice of architecture, conversationally](https://martinfowler.com/articles/scaling-architecture-conversationally.html)
- Inner source, shared libraries, service templates · [Backstage docs: Software templates](https://backstage.io/docs/features/software-templates/)
- Measuring developer experience (DORA, SPACE) · [ACM Queue: The SPACE of developer productivity](https://queue.acm.org/detail.cfm?id=3454124)

**Part project:** refactor one Acme Orders module to hexagonal architecture with a rich domain model; write five ADRs for the system; draw C4 context and container diagrams; add one fitness function to CI that enforces module boundaries.

**Exit criteria:** you can explain your architecture to a new engineer in ten minutes and to an executive in two.

---

<a id="part-14"></a>
## Part 14 — AI Engineering for Full-Stack *(new)*

**Goal:** build reliable LLM-powered features and judge when AI is the right tool.

#### 14.1 LLM Fundamentals for Engineers 🟢
- Tokens, context windows, sampling parameters, non-determinism · [Claude docs: Context windows](https://docs.claude.com/en/docs/build-with-claude/context-windows)
- Model families and selection: capability vs latency vs cost; hosted vs open-weight · [Claude docs: Choosing a model](https://docs.claude.com/en/docs/about-claude/models/choosing-a-model)
- Hallucination and its causes; knowledge cutoff · [Claude docs: Reduce hallucinations](https://docs.claude.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations)
- API basics: messages, system prompts, streaming, rate limits, pricing per token · [AI SDK docs: Foundations overview](https://ai-sdk.dev/docs/foundations/overview)
- Prompt caching and batch processing · [Claude docs: Prompt caching](https://docs.claude.com/en/docs/build-with-claude/prompt-caching)

#### 14.2 Prompting, Structured Output & Tool Calling 🔵
- Prompt design: clear instructions, examples, role, constraints, output format · [Claude docs: Prompt engineering overview](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview)
- Structured output with JSON Schema; validate everything with your schema library · [AI SDK docs: Generating structured data](https://ai-sdk.dev/docs/ai-sdk-core/generating-structured-data)
- Tool (function) calling: defining tools, the call loop, error handling · [AI SDK docs: Tools and tool calling](https://ai-sdk.dev/docs/ai-sdk-core/tools-and-tool-calling)
- Prompt versioning and management as code · [Prompt Engineering Guide](https://www.promptingguide.ai/)
- Multimodal inputs: images, documents, audio · [Claude docs: Vision](https://docs.claude.com/en/docs/build-with-claude/vision)

#### 14.3 Streaming AI UX in React & Next.js 🔵
- Streaming over SSE; rendering partial output; cancellation · [AI SDK docs: Streaming](https://ai-sdk.dev/docs/foundations/streaming)
- AI SDK patterns: chat state, tool results as UI, generative UI · [AI SDK docs: Chatbot (AI SDK UI)](https://ai-sdk.dev/docs/ai-sdk-ui/chatbot)
- UX for uncertainty: citations, edit and retry, confidence cues, human confirmation · [Google PAIR: People + AI Guidebook](https://pair.withgoogle.com/guidebook/)
- Latency perception; optimistic interaction; long-running tasks in the background · [Next.js docs: after (work after the response)](https://nextjs.org/docs/app/api-reference/functions/after)

#### 14.4 Embeddings, Vector Search & RAG 🔵
- Embeddings and similarity; chunking strategies · [AI SDK docs: Embeddings](https://ai-sdk.dev/docs/ai-sdk-core/embeddings)
- Vector storage: `pgvector` vs dedicated vector databases · [pgvector (README)](https://github.com/pgvector/pgvector)
- Retrieval quality: hybrid search, reranking, metadata filtering, query rewriting · [AI SDK docs: Reranking](https://ai-sdk.dev/docs/ai-sdk-core/reranking)
- RAG pipeline: ingest, retrieve, augment, generate, cite · [AI SDK cookbook: RAG chatbot guide](https://ai-sdk.dev/cookbook/guides/rag-chatbot)
- Tenant isolation and permission-aware retrieval; keeping the index fresh · [OWASP: RAG security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/RAG_Security_Cheat_Sheet.html)

#### 14.5 Agents, Workflows & MCP 🟣
- Workflows (fixed steps) vs agents (model decides); start with the simplest that works · [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
- Agent loop: plan, act, observe; memory; context management · [AI SDK docs: Building agents](https://ai-sdk.dev/docs/agents/building-agents)
- Model Context Protocol: servers, tools, resources; exposing your product through MCP · [Model Context Protocol: Introduction](https://modelcontextprotocol.io/docs/getting-started/intro)
- Durable execution for long tasks; human-in-the-loop approval · [NestJS docs: Workflows (durable execution)](https://docs.nestjs.com/reliability/workflows)
- Multi-agent patterns and their costs · [AI SDK docs: Subagents](https://ai-sdk.dev/docs/agents/subagents)

#### 14.6 Evals, Observability & Cost 🟣
- Evaluation sets: golden data, code-based checks, LLM-as-judge, human review · [Hamel Husain: Your AI product needs evals](https://hamel.dev/blog/posts/evals/)
- Regression testing prompts and models in CI · [promptfoo docs](https://www.promptfoo.dev/docs/intro/)
- Tracing LLM calls; tracking quality, latency, and token cost per feature and tenant · [OpenTelemetry: Semantic conventions for generative AI](https://opentelemetry.io/docs/specs/semconv/gen-ai/)
- Cost controls: model routing, caching, context trimming, budgets · [AI SDK docs: Batch processing](https://ai-sdk.dev/docs/ai-sdk-core/batch)
- Online feedback loops · [Eugene Yan: Patterns for building LLM-based systems](https://eugeneyan.com/writing/llm-patterns/)

#### 14.7 AI Security & Governance 🟣
- Prompt injection (direct and indirect) and why it is not fully solved; limiting blast radius · [Simon Willison: Prompt injection series](https://simonwillison.net/series/prompt-injection/)
- Least-privilege tools; sandboxing; confirming destructive actions · [OWASP: AI agent security cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/AI_Agent_Security_Cheat_Sheet.html)
- Data leakage, PII handling, provider data-retention terms · [OWASP: Secure AI model ops cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Secure_AI_Model_Ops_Cheat_Sheet.html)
- Output handling as untrusted input (XSS, SQL, command execution) · [OWASP: LLM prompt injection prevention cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html)
- OWASP Top 10 for LLM applications; regulatory awareness (EU AI Act) · [OWASP Top 10 for LLM applications](https://genai.owasp.org/llm-top-10/)

#### 14.8 AI-Assisted Development 🔵
- Working with coding agents: clear specifications, small tasks, context files, verification · [Next.js docs: AI coding agents guide](https://nextjs.org/docs/app/guides/ai-agents)
- Reviewing generated code: correctness, security, maintainability; you own what you merge · [OWASP: Secure coding with AI cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Secure_Coding_with_AI_Cheat_Sheet.html)
- AI in code review, testing, and migration work · [Simon Willison: How I use LLMs to help me write code](https://simonwillison.net/2025/Mar/11/using-llms-for-code/)
- 🟣 Team policy: where AI helps, where it harms, skill development for juniors · [DORA: AI research](https://dora.dev/research/ai/)

**Part project:** add an AI assistant to Acme Orders: natural-language order search over RAG with tenant-safe retrieval, a tool-calling agent that drafts orders with human approval, an eval suite in CI, and an MCP server exposing read-only order data.

**Exit criteria:** you can show measured quality for your AI feature and explain its failure modes and security limits.

---

<a id="part-15"></a>
## Part 15 — Technical Leadership & the Architect Role *(new)*

**Goal:** multiply the output of teams, not only your own.

#### 15.1 The Role: Senior vs Staff vs Architect 🟣
- Scope growth: task → feature → system → organization · [StaffEng: What do Staff engineers actually do?](https://staffeng.com/guides/what-do-staff-engineers-actually-do/)
- Staff archetypes: tech lead, architect, solver, right hand · [StaffEng: Staff archetypes](https://staffeng.com/guides/staff-archetypes/)
- The "architect elevator": moving between executives and engineers · [Gregor Hohpe: The Architect Elevator](https://architectelevator.com/)
- Staying hands-on; avoiding the ivory tower · [Martin Fowler: Who needs an architect? (PDF)](https://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf)
- Finding and choosing high-leverage work · [StaffEng: Work on what matters](https://staffeng.com/guides/work-on-what-matters/)

#### 15.2 Technical Strategy, Vision & Roadmaps 🟣
- Diagnosis → guiding policy → coherent actions · [Will Larson: Writing an engineering strategy](https://lethain.com/eng-strategies/)
- Writing a technical vision and a strategy document · [StaffEng: Writing engineering strategy](https://staffeng.com/guides/engineering-strategy/)
- Aligning technology with business goals and constraints · [Will Larson: Magnitudes of exploration](https://lethain.com/magnitudes-of-exploration/)
- Roadmaps: now / next / later; sequencing by risk and value · [ProdPad: The Now-Next-Later roadmap](https://www.prodpad.com/blog/invented-now-next-later-roadmap/)
- Balancing feature work, platform work, and debt · [Will Larson: How to invest in technical infrastructure](https://lethain.com/how-to-invest-technical-infrastructure/)

#### 15.3 Decision Making: Build vs Buy & Technology Selection 🟣
- Decision frameworks: reversible vs irreversible, weighted criteria, cost of delay · [Untools: Decision matrix](https://untools.co/decision-matrix/)
- Build vs buy vs open source: total cost of ownership, core vs commodity, exit plan · [Martin Fowler: Utility vs Strategic Dichotomy](https://martinfowler.com/bliki/UtilityVsStrategicDichotomy.html)
- Technology evaluation: proof of concept, maturity, community, hiring market, team skills · [Thoughtworks: Build your own Technology Radar](https://www.thoughtworks.com/radar/byor)
- Innovation tokens and boring technology · [Dan McKinley: Choose boring technology](https://boringtechnology.club/)
- Disagree and commit; recording decisions in ADRs · [Michael Nygard: Documenting architecture decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)

#### 15.4 Communication, Writing & Influence 🟣
- Writing as the main tool: design docs, proposals, status updates · [Google: Technical Writing One (free course)](https://developers.google.com/tech-writing/one)
- Structure: conclusion first; one idea per paragraph · [Wikipedia: BLUF (bottom line up front)](https://en.wikipedia.org/wiki/BLUF_%28communication%29)
- Influence without authority: build trust, find sponsors, pre-align before the meeting · [Will Larson: Model, document, share](https://lethain.com/model-document-share/)
- Translating technical risk into business language for product and executives · [StaffEng: Present to executives](https://staffeng.com/guides/present-to-executives/)
- Running effective design reviews; handling disagreement · [Will Larson: Scaling consistency with design reviews](https://lethain.com/scaling-consistency/)

#### 15.5 Estimation, Planning & Delivering Large Projects 🟣
- Estimation under uncertainty: ranges, reference classes, and re-estimation · [Jacob Kaplan-Moss: My estimation technique](https://jacobian.org/2021/may/25/my-estimation-technique/)
- Breaking large work into milestones that each deliver value · [Basecamp: Shape Up (free online book)](https://basecamp.com/shapeup)
- De-risking early: prototypes, spikes, tackling the hardest part first · [C2 wiki: Spike solution](https://wiki.c2.com/?SpikeSolution)
- Managing dependencies across teams; scope negotiation · [The Pragmatic Engineer: Software engineers leading projects](https://blog.pragmaticengineer.com/software-engineers-leading-projects/)
- Tracking and reporting; landing the project (migration finished, old system removed) · [Will Larson: Migrations, the sole scalable fix to tech debt](https://lethain.com/migrations/)

#### 15.6 Mentoring, Hiring & Engineering Culture 🟣
- Mentoring vs coaching vs sponsoring; delegation that develops people · [Lara Hogan: What does sponsorship look like?](https://larahogan.me/blog/what-sponsorship-looks-like/)
- Feedback: specific, timely, kind · [Lara Hogan: The feedback equation](https://larahogan.me/blog/feedback-equation/)
- Code review and design review as teaching tools · [Google Engineering Practices: How to write code review comments](https://google.github.io/eng-practices/review/reviewer/comments.html)
- Interviewing: structured questions, rubrics, reducing bias · [Joel Spolsky: The guerrilla guide to interviewing](https://www.joelonsoftware.com/2006/10/25/the-guerrilla-guide-to-interviewing-version-30/)
- Building culture: psychological safety, blamelessness, quality standards · [Google re:Work: Understand team effectiveness](https://rework.withgoogle.com/en/guides/understanding-team-effectiveness)

#### 15.7 Organization Design: Conway's Law & Team Topologies 🟣
- Conway's law and the inverse Conway maneuver · [Martin Fowler: Conway's Law](https://martinfowler.com/bliki/ConwaysLaw.html)
- Team types: stream-aligned, platform, enabling, complicated-subsystem · [Team Topologies: Key concepts](https://teamtopologies.com/key-concepts)
- Interaction modes; cognitive load as a design constraint · [Martin Fowler: Team Topologies](https://martinfowler.com/bliki/TeamTopologies.html)
- Ownership boundaries matching architecture boundaries · [DDD Crew: Bounded context canvas](https://github.com/ddd-crew/bounded-context-canvas)
- Working with product and design as a triad · [SVPG: Empowered product teams](https://www.svpg.com/empowered-product-teams/)

#### 15.8 Interviews & Career: Senior, Staff & Architect 🔵
- Loop structure: coding, system design, frontend design, architecture deep dive, behavioral · [Tech Interview Handbook: Software engineering interview guide](https://www.techinterviewhandbook.org/software-engineering-interview-guide/)
- Behavioral stories in STAR form: conflict, failure, influence, ambiguity, mentoring · [Tech Interview Handbook: Behavioral interviews](https://www.techinterviewhandbook.org/behavioral-interview/)
- Presenting a past project: context, your decisions, trade-offs, results, what you would change · [StaffEng: Stories from Staff-plus engineers](https://staffeng.com/stories/)
- Building a promotion case: evidence of scope and impact · [StaffEng: Promotion packets](https://staffeng.com/guides/promo-packets/)
- Continuous learning: reading list, public writing, talks, open source · [Professional Programming (curated reading list repo)](https://github.com/charlax/professional-programming)

**Part project:** write a one-page technical strategy for Acme Orders for the next 12 months; write an RFC for one significant change and have it reviewed; mentor one person through a part of this path.

**Exit criteria:** other engineers seek your review on designs, and your written proposals get adopted.

---

## Recommended reading (optional, paid books)

Every checklist above links to free material. These books go deeper if you want them.

| Area | Books |
|------|-------|
| JavaScript / TypeScript | *You Don't Know JS Yet* (Simpson) · *Effective TypeScript* (Vanderkam) |
| Web platform | *High Performance Browser Networking* (Grigorik) · web.dev and MDN |
| Node.js | *Node.js Design Patterns* (Casciaro, Mammino) |
| Databases | *Designing Data-Intensive Applications* (Kleppmann) · *PostgreSQL 14 Internals* (Rogov) |
| APIs and messaging | *Enterprise Integration Patterns* (Hohpe, Woolf) · *Building Microservices* (Newman) |
| Security | *Web Application Security* (Hoffman) · OWASP Cheat Sheet Series |
| Testing and code | *Unit Testing Principles, Practices, and Patterns* (Khorikov) · *Refactoring* (Fowler) |
| Operations | *Site Reliability Engineering* (Google) · *Accelerate* (Forsgren, Humble, Kim) |
| System design | *System Design Interview* vol. 1–2 (Xu) · *Understanding Distributed Systems* (Vitillo) |
| Architecture | *Fundamentals of Software Architecture* (Richards, Ford) · *Learning Domain-Driven Design* (Khononov) · *A Philosophy of Software Design* (Ousterhout) |
| Leadership | *Staff Engineer* (Larson) · *The Staff Engineer's Path* (Reilly) · *The Software Architect Elevator* (Hohpe) · *Team Topologies* (Skelton, Pais) |

---

## Progress tracker

Copy this block into an issue or your own fork and tick parts off as you meet the exit criteria.

- [ ] Part 01 — JavaScript & TypeScript
- [ ] Part 02 — The Web Platform
- [ ] Part 03 — React
- [ ] Part 04 — Next.js
- [ ] Part 05 — Node.js
- [ ] Part 06 — Express & NestJS
- [ ] Part 07 — Databases, Caching & Data Modeling
- [ ] Part 08 — API Design & Messaging
- [ ] Part 09 — Security & Authentication
- [ ] Part 10 — Testing & Code Quality
- [ ] Part 11 — Cloud, DevOps & Delivery
- [ ] Part 12 — System Design
- [ ] Part 13 — Software Architecture
- [ ] Part 14 — AI Engineering for Full-Stack
- [ ] Part 15 — Technical Leadership & the Architect Role
