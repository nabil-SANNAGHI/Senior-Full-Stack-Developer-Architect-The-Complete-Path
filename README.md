# Senior Full-Stack Developer → Architect: The Complete Path

A structured learning path for JavaScript/TypeScript full-stack engineers moving from **mid-level → senior → staff/architect**.

- **15 parts, 158 chapters**, each with a checklist of what you must know
- Stack: TypeScript, React, Next.js, Node.js, NestJS, PostgreSQL, Redis, cloud
- Every part ends with a project and exit criteria, so progress is measurable

> **Version baseline:** written against the stable releases of late 2026 (React 19.x with React Compiler, Next.js 16 App Router with Cache Components, current Node.js LTS, Express 5, PostgreSQL 17/18). Framework APIs move fast. Treat names of specific APIs as pointers and confirm against the official docs.

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
- Primitives vs objects; copy by value vs sharing by reference; `structuredClone`
- `var` / `let` / `const`, hoisting, the temporal dead zone
- Lexical scope, the scope chain, block vs function vs module scope
- Closures: what is captured (bindings, not values), the loop-closure bug, stale closures
- Closure use cases: private state, factories, memoization; closures and memory retention

#### 1.2 Functions, "this" & Functional Techniques 🟢
- The four `this` binding rules (default, implicit, explicit, `new`) and arrow-function lexical `this`
- `call`, `apply`, `bind`; losing `this` in callbacks and how to fix it
- Higher-order functions, pure functions, immutability, referential transparency
- Composition, currying, partial application; when functional style hurts readability
- Default, rest, and spread parameters; `arguments` and why to avoid it

#### 1.3 Objects, Prototypes, Classes & Proxies 🔵
- Property descriptors, getters/setters, `Object.freeze` / `seal`, enumerable vs own properties
- The prototype chain, `Object.create`, how `new` works step by step
- Classes as syntax over prototypes: fields, `#private`, `static`, accessors, `super`
- Inheritance vs composition; mixins; why deep class trees fail
- `Proxy` and `Reflect`: traps, use in reactivity and validation, performance cost
- `Symbol`, well-known symbols (`Symbol.iterator`, `Symbol.dispose`, `Symbol.toPrimitive`)

#### 1.4 Types, Coercion, Numbers, Strings & Dates 🟢
- `==` vs `===` vs `Object.is`; the abstract coercion rules (`ToPrimitive`, `ToNumber`)
- Truthy/falsy, `??` vs `||`, optional chaining
- IEEE-754 doubles: `0.1 + 0.2`, safe integer limits, `BigInt`, never floats for money
- Strings: UTF-16, code points vs code units, graphemes, `Intl.Segmenter`, normalization
- `Date` pitfalls, time zones, UTC storage, the `Temporal` API, `Intl` formatting

#### 1.5 Collections, Iterators & Generators 🟢
- `Array` methods and their complexity; mutating vs copying methods (`toSorted`, `toSpliced`, `with`)
- `Map` vs object, `Set` and set methods, `WeakMap` / `WeakSet` / `WeakRef` use cases
- The iterable and iterator protocols; `for...of`; spread and destructuring over iterables
- Generators: lazy sequences, `yield*`, two-way communication
- Iterator helpers (`map`, `filter`, `take` on iterators); async iterators and `for await`
- Typed arrays and `ArrayBuffer` basics

#### 1.6 Asynchronous JavaScript: Event Loop, Promises & Async/Await 🔵
- Call stack, task queue, microtask queue; ordering of `setTimeout`, promises, `queueMicrotask`
- Promise states, chaining, error propagation, unhandled rejections
- `Promise.all`, `allSettled`, `race`, `any`, `withResolvers`: when to use each
- `async`/`await` desugaring; sequential vs parallel awaits; the `await`-in-loop trap
- Concurrency limiting (pools, semaphores), batching, debounce and throttle
- Race conditions in async code: stale responses, check-then-act, re-entrancy

#### 1.7 Error Handling, Cancellation & Resource Management 🔵
- `Error` subclasses, `cause`, `AggregateError`; operational vs programmer errors
- Throw vs return a result type; where to catch (boundaries, not everywhere)
- `AbortController` / `AbortSignal`: timeouts, `AbortSignal.any`, propagating cancellation through layers
- `try/finally`, `using` and `await using` (explicit resource management), `DisposableStack`
- Retry with backoff and jitter; which errors are retryable

#### 1.8 Modules: ESM, CommonJS & Bundling 🔵
- ESM semantics: static structure, live bindings, top-level `await`, cyclic imports
- CommonJS semantics; ESM/CJS interop, `require(esm)`, dual-package hazard
- `package.json`: `exports`, `imports`, `type`, conditions, `sideEffects`
- Bundlers (Vite/Rolldown, Turbopack, esbuild): tree shaking, code splitting, dynamic `import()`
- Source maps, transpilation targets, polyfills, browserslist

#### 1.9 Memory, Garbage Collection & Runtime Performance 🔵
- Stack vs heap; reachability; generational GC (young/old space, scavenge, mark-sweep-compact)
- Common leaks: globals, forgotten timers and listeners, closures, unbounded caches, detached DOM
- V8 internals that matter: hidden classes, inline caches, deoptimization, monomorphic vs polymorphic code
- Measuring: `performance.now`, `performance.mark`, DevTools Performance and Memory panels
- Rule: measure first; algorithmic wins beat micro-optimizations

#### 1.10 TypeScript Foundations: Structural Typing, Inference & Narrowing 🟢
- Structural vs nominal typing; excess property checks; branded types for nominal behavior
- Inference, widening, `as const`, `satisfies`; when to annotate
- Unions, intersections, literal types, discriminated unions, exhaustiveness with `never`
- Narrowing: `typeof`, `in`, `instanceof`, type predicates, assertion functions
- `any` vs `unknown` vs `never`; `strict` flags and what each one catches

#### 1.11 Generics & Type-Level Programming 🔵
- Generic functions, constraints, defaults, `const` type parameters, `NoInfer`
- `keyof`, indexed access, mapped types, key remapping, template literal types
- Conditional types, `infer`, distributive behavior
- Built-in utilities and how to write them: `Partial`, `Pick`, `Omit`, `ReturnType`, `Awaited`
- Variance; function overloads vs unions
- 🟣 Limits: type complexity vs compile time and readability; when a simpler type is the better design

#### 1.12 TypeScript in Practice: tsconfig, Declaration Files & Runtime Validation 🔵
- Key `tsconfig` options: `strict`, `module`, `moduleResolution`, `target`, `verbatimModuleSyntax`, `isolatedModules`, `erasableSyntaxOnly`
- Project references, incremental builds, monorepo setups; running TS directly in Node (type stripping)
- `.d.ts` files, `declare module`, module augmentation, typing third-party code
- Types disappear at runtime: validate at boundaries with Zod / Valibot / ArkType; Standard Schema as the shared interface
- Derive types from schemas (one source of truth); typing environment variables and API responses

#### 1.13 Data Structures, Algorithms & Complexity in Practice 🟢 *(new)*
- Big-O for time and space; amortized cost; recognizing accidental O(n²)
- Arrays, hash maps, sets, stacks, queues, heaps, trees, tries, graphs: when each fits
- Core techniques: two pointers, sliding window, binary search, BFS/DFS, recursion vs iteration, dynamic programming basics
- Real uses: LRU cache, debouncing queues, topological sort for dependency graphs, tree diffing
- Interview practice: explain the approach before coding; state complexity; test edge cases

**Part project:** build a typed utility library: `retry` with backoff and abort support, a concurrency-limited `pMap`, an LRU cache, and a small event emitter. Full strict types, tests, dual ESM/CJS publish.

**Exit criteria:** you can predict output ordering of mixed timers/promises, explain a memory leak from a heap snapshot, and write a conditional type with `infer` unaided.

---

<a id="part-02"></a>
## Part 02 — The Web Platform *(new)*

**Goal:** understand what the browser and the network do, so framework behavior stops being magic.

#### 2.1 How Browsers Work: Parsing, Rendering & the Main Thread 🟢
- Navigation to pixels: HTML parsing, DOM, CSSOM, style, layout, paint, composite
- Render-blocking CSS, parser-blocking scripts, `async` / `defer` / `type="module"`
- The main thread, long tasks, frames and the 16 ms budget, `requestAnimationFrame`, `scheduler.yield`
- Reflow vs repaint; layout thrashing; compositor-only properties (`transform`, `opacity`)
- Process model: site isolation, renderer vs browser process

#### 2.2 DOM, Events & Core Web APIs 🟢
- DOM traversal and mutation; event capture, bubbling, delegation; passive listeners
- Observers: `IntersectionObserver`, `ResizeObserver`, `MutationObserver`
- `fetch`, `Request` / `Response`, streams, `URL`, `URLSearchParams`, `FormData`
- History and Navigation APIs; View Transitions API
- Web Workers, `postMessage`, transferable objects; Web Components basics

#### 2.3 Networking: DNS, TCP, TLS & HTTP/1.1 → HTTP/3 🔵
- What happens on a request: DNS resolution, TCP handshake, TLS handshake, request, response
- TLS 1.3 basics: certificates, chain of trust, SNI, HSTS
- HTTP/1.1 limits (head-of-line blocking), HTTP/2 multiplexing, HTTP/3 over QUIC
- Connection reuse, keep-alive, resource hints (`preconnect`, `preload`, `fetchpriority`)
- Compression (gzip, Brotli, zstd); reading a waterfall in DevTools

#### 2.4 HTTP Caching 🔵
- `Cache-Control` directives: `max-age`, `s-maxage`, `no-cache`, `no-store`, `private`, `immutable`
- Validation: `ETag`, `Last-Modified`, conditional requests, `304`
- `stale-while-revalidate`, `stale-if-error`, `Vary`
- Browser cache vs shared cache (CDN); cache keys; content-hashed filenames
- Back/forward cache (bfcache) and what breaks it

#### 2.5 Storage, Service Workers & Offline 🔵
- Cookies vs `localStorage` vs `sessionStorage` vs IndexedDB vs Cache API: capacity, sync/async, security
- Storage partitioning and third-party cookie restrictions
- Service worker lifecycle; caching strategies (cache-first, network-first, stale-while-revalidate)
- PWA basics: manifest, installability, background sync, push
- Offline-first and local-first trade-offs; conflict resolution overview (CRDT idea)

#### 2.6 Modern CSS & Layout 🟢
- Cascade, specificity, inheritance, cascade layers (`@layer`), `@scope`
- Box model, formatting contexts, stacking contexts, positioning
- Flexbox and Grid (including subgrid); intrinsic sizing; logical properties
- Container queries, `:has()`, native nesting, custom properties, `clamp()`, `color-mix()`
- Responsive strategy, fluid type, dark mode, `prefers-reduced-motion`

#### 2.7 Web Performance Fundamentals 🔵
- Core Web Vitals: LCP, INP, CLS: what each measures and typical causes
- Lab data vs field data (RUM); Lighthouse vs CrUX; percentiles (p75)
- Critical rendering path optimization; image formats and responsive images; font loading
- JavaScript cost: download, parse, execute; code splitting; third-party script control
- Performance budgets and how to enforce them in CI

**Part project:** build a small app with **no framework**: client-side routing with the Navigation API, a service worker with offline support, and a Lighthouse score above 95. Write down every optimization and its measured effect.

**Exit criteria:** you can narrate everything that happens between typing a URL and first paint, and diagnose a slow page from a DevTools trace.

---

<a id="part-03"></a>
## Part 03 — React

**Goal:** understand React's model well enough to design component systems and fix any rendering bug.

#### 3.1 React's Mental Model: Components, JSX & Rendering 🟢
- UI as a function of state; declarative vs imperative
- JSX compiles to element objects; elements vs components vs instances
- Render phase vs commit phase; rendering must be pure
- What triggers a render: state change, parent render, context change
- Strict Mode double invocation and what it reveals

#### 3.2 Reconciliation, Keys & Component Identity 🔵
- The diffing heuristics: same type at same position preserves state
- Keys: identity across renders; why index keys break; using `key` to reset state
- Fiber architecture overview: units of work, priority lanes, interruptible rendering
- Defining components inside components (identity reset bug)
- `<Activity>` for hiding UI while preserving state

#### 3.3 State: useState, useReducer & State Design 🟢
- State as a snapshot; batching; updater functions
- Immutable updates for objects and arrays
- `useReducer` for complex transitions; reducers as state machines
- State design rules: minimal state, derive do not store, no duplicated or contradictory state
- Lifting state up vs colocating; controlled vs uncontrolled components; URL as state

#### 3.4 Effects, Refs & Synchronizing with External Systems 🔵
- Effects synchronize with external systems; they are not lifecycle hooks
- Dependency arrays, cleanup, race conditions in fetching effects
- "You might not need an effect": derived values, event handlers, `key` resets
- `useEffectEvent` for non-reactive logic inside effects
- Refs: mutable values, DOM access, `ref` as a prop, ref cleanup functions, `useImperativeHandle`
- `useLayoutEffect`, `useSyncExternalStore` for external stores

#### 3.5 Context, Composition & Component Patterns 🔵
- Context: what it solves (prop drilling) and its cost (every consumer re-renders)
- Splitting contexts, memoizing values, state/dispatch separation
- Composition: `children`, slots, render props, compound components
- Custom hooks as the unit of logic reuse; headless components
- Polymorphic components, controlled/uncontrolled dual APIs, inversion of control
- 🟣 Designing component APIs for a team: what to expose, what to hide

#### 3.6 Server State & Data Fetching 🟢
- Server state vs client state: caching, staleness, ownership
- TanStack Query model: query keys, `staleTime` vs `gcTime`, background refetch, invalidation
- Mutations, optimistic updates, rollback; pagination and infinite queries
- Request waterfalls vs parallel fetching; prefetching; render-as-you-fetch
- The `use` hook with promises; when a framework data layer replaces a client cache

#### 3.7 Suspense, Transitions & Concurrent Rendering 🔵
- Suspense boundaries: fallbacks, nesting, placement strategy, avoiding layout shift
- `useTransition`, `startTransition`: urgent vs non-urgent updates, async transitions
- `useDeferredValue` for keeping input responsive
- Streaming SSR and selective hydration
- Error boundaries with Suspense; reset and retry patterns

#### 3.8 Forms & Actions: useActionState, useOptimistic & Validation 🟢
- `<form action>` with functions; progressive enhancement
- `useActionState` for pending state and results; `useFormStatus`
- `useOptimistic` for instant feedback and automatic revert
- Validation: shared schema on client and server; field vs form errors; accessible error display
- When to use React Hook Form or TanStack Form; complex forms (wizards, dynamic arrays)

#### 3.9 Client State Management at Scale 🔵
- Classify state first: server, URL, form, local UI, global UI
- Stores: Zustand, Redux Toolkit, Jotai; selectors and subscription granularity
- State machines and statecharts (XState) for complex flows
- Signals: the idea and how it differs from React's model
- 🟣 Choosing for a team: boring defaults, migration cost, avoiding one global store for everything

#### 3.10 Performance: React Compiler, Memoization & Profiling 🔵
- Why components re-render; when re-renders are actually a problem
- React Compiler: automatic memoization, the Rules of React it depends on, opting out
- Manual `memo`, `useMemo`, `useCallback`: when still needed
- React DevTools Profiler, Performance tracks; finding the slow component
- List virtualization, code splitting with `lazy`, moving state down, passing children
- Measuring INP for interactions

#### 3.11 Accessibility, Styling & Design Systems 🔵
- Semantic HTML first; ARIA roles, states, and when not to use ARIA
- Keyboard navigation, focus management, focus traps, live regions; WCAG 2.2 AA
- Accessible primitives (React Aria, Radix, Base UI); testing with axe and a screen reader
- Styling options: CSS Modules, Tailwind, zero-runtime CSS-in-JS; trade-offs with Server Components
- Design tokens, theming, variants
- 🟣 Design system governance: versioning, contribution model, documentation, adoption

**Part project:** Acme Orders admin UI: order table with filtering, sorting, and virtualization; an optimistic order-status update; a multi-step order form; fully keyboard accessible.

**Exit criteria:** you can explain any re-render from the Profiler, remove unnecessary effects from a codebase, and design a compound component API.

---

<a id="part-04"></a>
## Part 04 — Next.js

**Goal:** own a production Next.js application, including rendering, caching, and deployment decisions.

#### 4.1 App Router Architecture & Routing 🟢
- File conventions: `page`, `layout`, `template`, `loading`, `error`, `not-found`, `route`, `default`
- Dynamic, catch-all, and optional segments; route groups; private folders
- Parallel routes and intercepting routes (modals, dashboards)
- Navigation: `<Link>`, prefetching, `useRouter`, `redirect`, soft vs hard navigation
- Async `params` and `searchParams`; typed routes

#### 4.2 Server Components, Client Components & Boundaries 🔵
- What Server Components are: run only on the server, zero client JS, can be async
- `"use client"` marks a boundary, not a component type; everything imported below is client code
- The RSC payload and serialization rules for props
- Composition: passing Server Components as `children` to Client Components
- `server-only` / `client-only`; keeping secrets out of the bundle; context providers placement
- 🟣 Deciding the boundary: push `"use client"` to the leaves; measuring bundle impact

#### 4.3 Layouts, Loading, Error & Not-Found UI 🟢
- Nested layouts and partial rendering; layouts do not re-render on navigation
- `loading.tsx` as a Suspense boundary; granular `<Suspense>` for streaming
- `error.tsx`, `global-error.tsx`, recovery; `notFound()`, `forbidden()`, `unauthorized()`
- Skeleton design that avoids layout shift

#### 4.4 Data Fetching & Rendering Strategies 🔵
- Fetch in Server Components close to where data is used; request deduplication with `cache()`
- Parallel vs sequential fetching; avoiding waterfalls; preloading
- Static vs dynamic rendering; what makes a route dynamic (`cookies`, `headers`, `searchParams`)
- Streaming; Partial Prerendering: static shell plus dynamic holes
- `generateStaticParams`; the data access layer pattern and DTOs

#### 4.5 Caching: Cache Components, "use cache" & Revalidation 🔵
- The Cache Components model: dynamic by default, cache by opting in
- `"use cache"` on files, components, and functions; how cache keys are derived from arguments
- `cacheLife` profiles and `cacheTag`
- Invalidation: `revalidateTag`, `updateTag` (read-your-writes), `revalidatePath`, `refresh`
- Client router cache behavior; runtime vs build-time caching
- 🟣 Designing a tagging scheme per entity and tenant; debugging stale data; cache stampede risks

#### 4.6 Server Actions & Mutations 🟢
- `"use server"`: actions are public HTTP endpoints, so authenticate, authorize, and validate in each
- Calling from forms and event handlers; pending and optimistic UI
- Returning errors vs throwing; revalidation and redirect after mutation
- Security: closures and encrypted bound values, CSRF protections, rate limiting
- When to use a Route Handler instead

#### 4.7 Route Handlers & Backend-for-Frontend Patterns 🔵
- `route.ts`: HTTP methods, Web `Request` / `Response`, streaming responses
- Webhook endpoints: raw body, signature verification
- BFF pattern: aggregation, token handling, hiding internal services
- 🟣 Next.js as full backend vs Next.js in front of a separate API: decision criteria

#### 4.8 Proxy (Middleware), Authentication & Multi-Tenant Routing 🔵
- `proxy.ts` (formerly middleware): what belongs there (redirects, rewrites, headers) and what does not (heavy logic, full auth)
- Auth architecture: session cookie, optimistic check in proxy, real check in the data access layer
- Auth libraries (Auth.js, Better Auth) and hosted providers; protecting pages, actions, and handlers
- Multi-tenancy: subdomain and custom-domain routing via rewrites; tenant resolution; tenant-scoped caching

#### 4.9 Metadata, SEO, Internationalization, Images & Fonts 🟢
- Metadata API, `generateMetadata`, Open Graph images, `sitemap`, `robots`, structured data
- i18n: locale routing, message loading, formatting with `Intl`, RTL support
- `next/image`: sizing, `sizes`, priority, formats, remote patterns
- `next/font`: self-hosting, subsetting, avoiding layout shift; `next/script` strategies

#### 4.10 Performance & Core Web Vitals 🔵
- Bundle analysis; `dynamic()` imports; reducing client JS
- Improving LCP (priority images, streaming), INP (less hydration, transitions), CLS (reserved space)
- Turbopack; build performance in large apps
- Field monitoring: `useReportWebVitals`, RUM, OpenTelemetry instrumentation

#### 4.11 Deployment, Self-Hosting & Production Security 🔵
- Deployment targets: managed platform, Node server, Docker `standalone` output, static export, adapters
- Self-hosting concerns: shared cache handler across instances, image optimization, streaming through proxies
- Environment variables: build-time vs runtime, `NEXT_PUBLIC_` exposure
- Security headers, CSP with nonces, Server Action allowed origins, data tainting
- 🟣 Cost and lock-in analysis of platform choice; multi-region considerations

**Part project:** Acme Orders storefront and dashboard on Next.js: tenant subdomains, cached catalog with tag invalidation, Server Action mutations, auth, i18n in two languages, deployed with Docker.

**Exit criteria:** for any route you can state what is static, cached, or dynamic and why, and you can explain exactly what invalidates each cached piece.

---

<a id="part-05"></a>
## Part 05 — Node.js

**Goal:** understand the runtime well enough to diagnose production problems from first principles.

#### 5.1 Node Architecture: V8, libuv & Event Loop Phases 🔵
- Components: V8, libuv, C++ bindings, core JS modules
- Event loop phases: timers, pending callbacks, poll, check, close
- `process.nextTick` vs promise microtasks vs `setImmediate` vs `setTimeout(0)`
- What is truly async in the kernel (network) vs the thread pool (fs, DNS lookup, crypto, zlib)
- Differences from the browser event loop

#### 5.2 Blocking Code, the Thread Pool & Worker Threads 🔵
- How one CPU-heavy request stalls all others; measuring event-loop delay and utilization
- Typical blockers: large `JSON.parse`, sync APIs, catastrophic regex (ReDoS), big loops
- Thread pool size (`UV_THREADPOOL_SIZE`) and saturation
- Worker threads: `MessageChannel`, transferables, `SharedArrayBuffer`, `Atomics`, worker pools (Piscina)
- Partitioning work vs offloading to a queue

#### 5.3 Buffers, Encodings & Binary Data 🟢
- `Buffer` and `Uint8Array`; allocation (`alloc` vs `allocUnsafe`)
- Encodings: UTF-8, base64, base64url, hex; multi-byte characters split across chunks
- Endianness; parsing binary protocols; `TextEncoder` / `TextDecoder`
- `Blob`, `File`, and `ArrayBuffer` interop

#### 5.4 Streams & Backpressure 🔵
- Readable, Writable, Duplex, Transform; flowing vs paused; object mode
- Backpressure: `highWaterMark`, `write()` return value, `drain`
- `pipeline()` and `stream/promises` over `.pipe()` for error handling and cleanup
- Async iteration over streams; Web Streams interop
- Use cases: large file processing, CSV/JSON streaming, proxying, compression

#### 5.5 File System & Process I/O 🟢
- `fs/promises`, file handles, atomic writes (write temp then rename), file watching
- Path handling, `import.meta.dirname`, path traversal prevention
- `process`: `argv`, `env`, `stdin` / `stdout` / `stderr`, exit codes, signals
- Built-ins worth knowing: `--env-file`, `--watch`, `node:test`, `parseArgs`, the permission model

#### 5.6 EventEmitter, Async Hooks & AsyncLocalStorage 🔵
- `EventEmitter`: synchronous emit, the special `error` event, listener leaks, `once`, `on` as async iterator
- `EventTarget` in Node
- `AsyncLocalStorage`: request-scoped context (request ID, tenant, user) without passing parameters
- Context loss pitfalls; performance cost; `diagnostics_channel`

#### 5.7 HTTP, Networking & the Fetch API 🔵
- `node:http` server internals: keep-alive, `headersTimeout`, `requestTimeout`, slow-client attacks
- Built-in `fetch` (undici): connection pooling, agents/dispatchers, timeouts, retries
- Sockets with `net` and `tls`; HTTP/2 basics
- DNS: `lookup` vs `resolve`, caching
- Running behind a proxy: `X-Forwarded-*` headers, trust settings

#### 5.8 Configuration, Logging & Error Strategy 🟢
- Twelve-factor config; validate env at startup and fail fast; separating secrets
- Structured JSON logging (Pino): levels, correlation IDs, redaction, child loggers
- Error taxonomy: operational vs programmer; a central error handler
- `uncaughtException` and `unhandledRejection`: log, then crash and restart

#### 5.9 Child Processes, Clustering & Scaling a Node Process 🔵
- `spawn`, `exec`, `execFile`, `fork`; stdio, IPC, shell-injection risk
- The `cluster` module vs multiple containers behind a load balancer
- Statelessness requirements: externalized sessions, sticky sessions for WebSockets
- 🟣 Vertical vs horizontal scaling; sizing memory and CPU limits per instance

#### 5.10 Diagnostics: Profiling, Heap Snapshots & Memory Leaks 🔵
- `--inspect`, CPU profiles, flame graphs; finding hot paths
- Heap snapshots: the three-snapshot technique, retainers, allocation timelines
- `perf_hooks`: event-loop delay histogram, `PerformanceObserver`
- Heap limits (`--max-old-space-size`), OOM kills in containers, diagnostic reports
- Safe production profiling

#### 5.11 Graceful Shutdown, Health Checks & Running in Containers 🟢
- Handling `SIGTERM`: stop accepting, drain in-flight requests, close DB and queue connections, exit
- Liveness vs readiness vs startup probes; what each should check
- Docker: multi-stage builds, slim or distroless images, non-root user, PID 1 and signal forwarding
- Memory and CPU limits vs Node's view of resources; using the lockfile for reproducible installs

**Part project:** a streaming CSV order-import service: handles files larger than memory, applies backpressure, offloads validation to a worker pool, carries a request ID through `AsyncLocalStorage`, and shuts down gracefully.

**Exit criteria:** you can find a memory leak and an event-loop block in a running service using only profiling tools.

---

<a id="part-06"></a>
## Part 06 — Express & NestJS

**Goal:** build and structure backend services that a team can maintain for years.

#### 6.1 Express Internals: Middleware, Routing & the Request Lifecycle 🟢
- The middleware chain: `(req, res, next)`, ordering, short-circuiting
- Router, mounting, path matching in Express 5
- Body parsing, static files, common middleware (helmet, cors, compression)
- Express 5 changes: rejected promises forwarded to the error handler
- Landscape awareness: Fastify (schemas, speed), Hono (Web standards, edge); when each fits

#### 6.2 Express Error Handling, Validation & Project Structure 🟢
- Error middleware (four arguments); mapping domain errors to HTTP responses
- Request validation with a schema library; typed request handlers
- Layering: routes → controllers → services → repositories
- Dependency injection without a framework; testability; app vs server separation

#### 6.3 NestJS Architecture: Modules, Providers & Dependency Injection 🔵
- Modules: `imports`, `providers`, `exports`; feature, shared, global, and dynamic modules
- The DI container: tokens, `useClass` / `useValue` / `useFactory`, custom providers
- Injection scopes: singleton, request, transient, and the cost of request scope
- Circular dependencies: causes, `forwardRef`, and the real fix (restructure)
- Lifecycle hooks; `ModuleRef`; lazy-loaded modules
- 🟣 Module boundaries as architecture: mapping modules to business capabilities

#### 6.4 Controllers, DTOs & Validation with Standard Schema 🟢
- Controllers, route decorators, parameter decorators, custom decorators
- DTOs as the API boundary; never expose entities directly
- Validation approaches: `class-validator` + `ValidationPipe` vs schema-first (Zod, Valibot) through Standard Schema
- Transformation, whitelisting unknown fields, response serialization
- OpenAPI generation from DTOs or schemas

#### 6.5 The Request Pipeline: Middleware, Guards, Interceptors, Pipes & Filters 🔵
- Exact order: middleware → guards → interceptors (before) → pipes → handler → interceptors (after) → exception filters
- Guards for authentication and authorization; `ExecutionContext`, `Reflector`, metadata
- Interceptors: logging, timeouts, caching, response mapping (RxJS basics)
- Pipes for validation and transformation; exception filters for consistent error shapes
- Binding levels: global, controller, method

#### 6.6 Configuration, Request Context & Multi-Tenancy in NestJS 🔵
- `ConfigModule`, validated config, typed namespaces
- Request context with `AsyncLocalStorage` (for example `nestjs-cls`) instead of request-scoped providers
- Tenant resolution: subdomain, header, or token claim
- Tenant-aware data access; durable providers; preventing cross-tenant leaks in caches and logs

#### 6.7 Data Access in NestJS 🔵
- Choosing Prisma, Drizzle, TypeORM, or MikroORM: trade-offs
- Repository pattern; keeping persistence out of domain logic
- Transactions across services: unit of work, transactional context via ALS
- Migrations in deployment; connection pool lifecycle; testing against a real database

#### 6.8 Background Jobs, Scheduling & Queues 🔵
- BullMQ: queues, workers, concurrency, retries with backoff, delayed and repeatable jobs
- Idempotent job handlers; dead-letter handling; poison messages
- Cron scheduling and distributed locking so a job runs once across instances
- Flows and job dependencies; running workers as separate processes; queue monitoring

#### 6.9 Microservices & Transports 🔵
- Nest microservice transports: TCP, Redis, NATS, RabbitMQ, Kafka, gRPC
- Request-response vs event patterns; hybrid applications
- Serialization, timeouts, retries, error propagation across services
- 🟣 Start with a modular monolith; extraction criteria; the distributed monolith failure mode

#### 6.10 NestJS in Production: Observability, Performance & Upgrades 🔵
- OpenTelemetry tracing, metrics, health checks (Terminus), structured logs
- Fastify adapter; caching; compression; rate limiting (`@nestjs/throttler`)
- Graceful shutdown hooks; startup time; memory profile
- API versioning; planning major-version upgrades; dependency hygiene

**Part project:** the Acme Orders API in NestJS: tenant-aware modules for orders, products, and users; validated DTOs; a guard-based permission system; BullMQ jobs for emails; OpenAPI docs.

**Exit criteria:** you can draw the Nest request pipeline from memory and justify every module boundary in your project.

---

<a id="part-07"></a>
## Part 07 — Databases, Caching & Data Modeling

**Goal:** design schemas that survive growth, and explain any slow query or concurrency bug.

#### 7.1 Relational Fundamentals & Data Modeling 🟢
- Relations, primary and foreign keys, cardinality (1:1, 1:N, M:N)
- Normalization (1NF–3NF) and deliberate denormalization
- Entity modeling from requirements; ER diagrams
- Key choice: serial vs UUIDv4 vs UUIDv7 / ULID, natural vs surrogate keys
- Modeling patterns: soft delete, audit columns, temporal data, polymorphic associations, trees

#### 7.2 SQL Mastery: Joins, CTEs, Window Functions & Aggregation 🟢
- Join types, including anti-join, semi-join, and `LATERAL`
- `GROUP BY`, `HAVING`, `FILTER`, grouping sets
- CTEs and recursive CTEs (hierarchies, graphs)
- Window functions: `ROW_NUMBER`, `RANK`, `LAG` / `LEAD`, frames, running totals
- `INSERT ... ON CONFLICT` (upsert), `RETURNING`, `MERGE`; NULL semantics and three-valued logic

#### 7.3 Schema Design, Constraints & Migrations 🔵
- Data types: `numeric` for money, `timestamptz`, `jsonb`, arrays, enums vs lookup tables
- Constraints: `NOT NULL`, `UNIQUE`, `CHECK`, foreign keys, exclusion constraints
- Zero-downtime migrations: the expand → migrate → contract pattern
- Dangerous operations: table rewrites, long locks, `CREATE INDEX CONCURRENTLY`, `NOT VALID` constraints, `lock_timeout`
- Batched backfills; migration tooling; rollback strategy

#### 7.4 Indexes: How They Work & How to Choose Them 🔵
- B-tree structure; why column order matters in composite indexes; leftmost prefix
- Covering indexes (`INCLUDE`), index-only scans, partial indexes, expression indexes
- Other types: GIN (jsonb, full-text, arrays), GiST, BRIN, hash
- Selectivity and cardinality; when the planner ignores an index
- Index cost: write overhead, bloat, unused index detection

#### 7.5 Query Planning & Performance Tuning 🔵
- Reading `EXPLAIN (ANALYZE, BUFFERS)`: scan types, join algorithms, estimated vs actual rows
- Statistics, `ANALYZE`, misestimates
- Finding slow queries with `pg_stat_statements`; the N+1 problem
- Keyset pagination vs `OFFSET`; rewriting queries; materialized views
- Vacuum, autovacuum, bloat; key configuration (`work_mem`, `shared_buffers`)

#### 7.6 Transactions, Isolation Levels & MVCC 🔵
- ACID, precisely
- Anomalies: dirty read, non-repeatable read, phantom, lost update, write skew
- Isolation levels in PostgreSQL: Read Committed, Repeatable Read (snapshot), Serializable (SSI)
- MVCC: row versions, snapshots, dead tuples, why long transactions hurt
- Serialization failures and retry loops; savepoints

#### 7.7 Locking, Concurrency Control & Idempotency 🔵
- Row locks: `SELECT ... FOR UPDATE`, `SKIP LOCKED` (job queues), `NOWAIT`
- Table lock modes; deadlocks: detection and prevention by consistent ordering
- Optimistic concurrency with a version column vs pessimistic locking
- Advisory locks; distributed locks and their limits (fencing tokens)
- Idempotency keys, unique constraints as guards, exactly-once *effects*

#### 7.8 Multi-Tenancy Strategies & Row-Level Security 🟣
- Models: shared schema with `tenant_id`, schema per tenant, database per tenant: isolation, cost, operations
- PostgreSQL RLS: policies, setting tenant context per transaction, behavior with connection pooling
- Tenant-leading indexes and unique constraints
- Noisy neighbors, per-tenant limits, tenant migration, sharding by tenant
- Per-tenant backup, export, and deletion

#### 7.9 ORMs, Query Builders & Connection Pooling 🔵
- ORM vs query builder vs raw SQL: Prisma, Drizzle, Kysely trade-offs
- Avoiding N+1; relation loading strategies; knowing the SQL your ORM emits
- Pool sizing: why bigger is not better; `max_connections`
- PgBouncer modes (session vs transaction) and their limits; pooling in serverless
- Timeouts at every level: statement, lock, idle-in-transaction

#### 7.10 Replication, Partitioning & Backups 🔵
- Streaming replication, sync vs async, replication lag, read-your-writes problems
- Logical replication and its uses
- Failover and high availability; managed-service behavior
- Table partitioning (range, list, hash), partition pruning, retention by dropping partitions
- Backups: base backups plus WAL, point-in-time recovery, RPO/RTO, restore drills

#### 7.11 Caching Patterns & Invalidation 🔵
- Patterns: cache-aside, read-through, write-through, write-behind
- TTL design, jitter, negative caching
- Invalidation strategies: on write, event-driven, versioned keys
- Stampede protection: locking, request coalescing, stale-while-revalidate, probabilistic early expiry
- Cache layers (in-process, distributed, CDN) and consistency between them
- 🟣 Deciding what *not* to cache; cache as a liability when it hides a slow system

#### 7.12 Redis in Depth 🔵
- Data structures and their use cases: strings, hashes, lists, sets, sorted sets, streams, HyperLogLog
- Single-threaded execution model; pipelining; transactions; Lua scripts and functions for atomicity
- Expiry, eviction policies, memory analysis
- Persistence (RDB, AOF); replication, Sentinel, Cluster and hash slots
- Recipes: rate limiter, distributed lock (and its caveats), leaderboard, session store, pub/sub vs streams
- Ecosystem awareness: Valkey and managed alternatives

#### 7.13 NoSQL & Search: Document Stores, Key-Value & Full-Text Search 🔵
- Document databases (MongoDB): modeling by access pattern, embedding vs referencing
- Wide-column and key-value stores (DynamoDB): partition and sort keys, single-table design
- Full-text search: PostgreSQL `tsvector` vs Elasticsearch / OpenSearch / Typesense; inverted index, analyzers, relevance (BM25)
- Vector search: `pgvector`, HNSW indexes, hybrid search
- Keeping a search index in sync with the source of truth
- 🟣 Polyglot persistence: the operational cost of each extra datastore

#### 7.14 Data Lifecycle: CDC, Analytics & Zero-Downtime Data Migrations 🟣 *(new)*
- OLTP vs OLAP; columnar stores (ClickHouse, BigQuery, DuckDB); why not to run analytics on the primary
- Change data capture (Debezium, logical decoding); ETL vs ELT
- Migrating between databases or schemas live: dual writes, backfill, verification, cutover
- Data retention, archiving, and deletion policies
- Time-series data handling

**Part project:** the Acme Orders schema: multi-tenant with RLS, an inventory reservation flow that is correct under concurrency (prove it with a test that runs 100 parallel orders), keyset pagination, a Redis cache with stampede protection, and one zero-downtime column migration.

**Exit criteria:** you can read any `EXPLAIN` plan, name the anomaly behind a concurrency bug, and choose the isolation level or lock that fixes it.

---

<a id="part-08"></a>
## Part 08 — API Design & Messaging

**Goal:** design contracts that are easy to use, hard to misuse, and safe to evolve.

#### 8.1 HTTP Semantics for API Designers 🟢
- Methods: safe, idempotent, cacheable; correct use of `PUT` vs `PATCH` vs `POST`
- Status codes used precisely (`201`, `202`, `204`, `409`, `412`, `422`, `429`)
- Content negotiation; conditional requests with `ETag` / `If-Match` for optimistic concurrency
- Caching headers for APIs; `Location`, `Retry-After`, `Link`

#### 8.2 REST Resource Design, Pagination & Filtering 🟢
- Resource modeling, naming, nesting depth; actions that are not CRUD
- Pagination: offset vs cursor/keyset; stable ordering; response shape
- Filtering, sorting, field selection, expansion of related resources
- Bulk operations; long-running operations (`202` plus a status resource)
- Consistent conventions for dates, money, enums, and IDs

#### 8.3 Errors, Versioning, Idempotency & API Evolution 🔵
- Problem Details (RFC 9457): machine-readable error codes, validation error format
- Versioning strategies: URL, header, date-based; the cost of each
- Backward-compatible changes vs breaking changes; tolerant readers
- `Idempotency-Key` implementation: storage, request fingerprint, replaying responses
- Deprecation and sunset policy; communicating change to consumers

#### 8.4 OpenAPI, Contracts & Documentation 🔵
- OpenAPI 3.1 structure; design-first vs code-first
- Generating typed clients and server stubs; contract linting (Spectral)
- Breaking-change detection in CI
- Documentation that works: quick start, examples, error catalog, changelog
- 🟣 API governance: style guide, review process, treating the API as a product

#### 8.5 GraphQL: Schema Design, Resolvers & Performance 🔵
- Schema design: types, nullability, connections for pagination, mutation payloads, error modeling
- Resolvers and the N+1 problem; DataLoader batching
- Security and cost: depth and complexity limits, persisted queries
- Caching challenges; federation overview; subscriptions
- 🟣 When GraphQL is the right choice (many clients, varied data needs) and when it is overhead

#### 8.6 RPC Styles: tRPC & gRPC 🔵
- tRPC: end-to-end types without code generation; best inside a TypeScript monorepo
- gRPC: Protocol Buffers, schema evolution rules, four streaming modes, deadlines, status codes
- gRPC-Web and Connect; internal vs public API suitability
- 🟣 Choosing REST vs GraphQL vs RPC per boundary (public, BFF, service-to-service)

#### 8.7 Real-Time: Polling, SSE & WebSockets 🔵
- Short polling, long polling, Server-Sent Events, WebSockets, WebTransport: trade-offs
- SSE: reconnection, `Last-Event-ID`, proxy buffering issues
- WebSockets: handshake, heartbeats, reconnection with backoff, authentication, backpressure
- Scaling connections: sticky sessions, pub/sub backplane, connection limits
- Presence, ordering, and delivery guarantees; managed real-time services

#### 8.8 File Uploads, Object Storage & Media 🟢 *(new)*
- Object storage model (S3-compatible): buckets, keys, storage classes, lifecycle rules
- Direct-to-storage uploads with presigned URLs; multipart and resumable uploads
- Validation: size, type sniffing, malware scanning; never trust the client filename
- Serving: CDN, signed URLs for private content, range requests
- Image and video processing pipelines; storing metadata in the database

#### 8.9 Webhooks & Third-Party Integrations 🔵
- Receiving: signature verification (HMAC), replay protection, respond fast then process async, deduplicate
- Sending: retries with backoff, signing, delivery logs, endpoint management, SSRF protection
- Integration resilience: timeouts, circuit breakers, vendor rate limits, sandbox testing
- Anti-corruption layer around third-party models; payment provider integration patterns

#### 8.10 Messaging Fundamentals: Queues, Logs & Delivery Guarantees 🔵
- Queue (RabbitMQ, SQS) vs log (Kafka) semantics: consumption, retention, replay
- At-most-once, at-least-once, and why exactly-once delivery is really idempotent processing
- Ordering, partitions, consumer groups, rebalancing
- Acknowledgements, visibility timeouts, dead-letter queues, poison messages
- Backpressure and consumer lag; message schema evolution

#### 8.11 Event-Driven Architecture: Outbox, Sagas & Event Sourcing 🟣
- The dual-write problem; transactional outbox; inbox for deduplication; CDC as an alternative
- Event types: notification, event-carried state transfer, domain vs integration events
- Sagas: choreography vs orchestration, compensating actions; workflow engines (Temporal)
- Event sourcing and CQRS: projections, snapshots, when the complexity is justified
- Living with eventual consistency in the UI and in support processes

#### 8.12 Rate Limiting, Throttling & API Gateways 🔵
- Algorithms: fixed window, sliding window, token bucket, leaky bucket
- Distributed rate limiting with Redis; limit keys (user, tenant, IP, API key)
- Response contract: `429`, `Retry-After`, rate-limit headers
- Quotas and plans; load shedding
- API gateway responsibilities: auth, routing, limits, transformation; gateway vs BFF vs service mesh

**Part project:** a public Acme Orders API: OpenAPI-first, cursor pagination, idempotent order creation, Problem Details errors, signed outgoing webhooks with retries, an outbox publishing order events, presigned invoice uploads, per-tenant rate limits.

**Exit criteria:** you can review an API design and list its evolution risks, and you can explain why your order flow never loses or duplicates an event.

---

<a id="part-09"></a>
## Part 09 — Security & Authentication

**Goal:** think like an attacker, build like a defender, and make the secure path the default path.

#### 9.1 Threat Modeling & Security Principles 🔵
- Principles: least privilege, defense in depth, secure defaults, fail closed, zero trust
- Threat modeling with STRIDE; data-flow diagrams; trust boundaries
- OWASP Top 10 and API Security Top 10 as checklists
- Risk rating: likelihood × impact; accepting vs mitigating risk
- 🟣 Running a threat-modeling session for a new design

#### 9.2 Injection & Input Handling 🟢
- SQL injection and parameterized queries; ORM raw-query pitfalls
- NoSQL injection, command injection, path traversal, template injection
- Validation (allow-list) vs sanitization vs output encoding: each has a different job
- Prototype pollution, mass assignment, ReDoS

#### 9.3 XSS, CSP & Browser Security 🔵
- Stored, reflected, and DOM-based XSS; what React escapes and what it does not (`dangerouslySetInnerHTML`, `href` URLs)
- Sanitizing HTML (DOMPurify); Trusted Types
- Content Security Policy: nonces, hashes, `strict-dynamic`, report-only rollout
- Security headers: HSTS, `X-Content-Type-Options`, `frame-ancestors`, Referrer-Policy, Permissions-Policy
- Subresource Integrity; third-party script risk

#### 9.4 CSRF, CORS, Cookies & the Same-Origin Policy 🔵
- Origin vs site; what the same-origin policy actually blocks
- CORS: simple vs preflighted requests, credentials, common misconfigurations
- Cookie attributes: `HttpOnly`, `Secure`, `SameSite`, `__Host-` prefix, partitioned cookies
- CSRF defenses: SameSite, tokens, Origin checks, Fetch Metadata
- Clickjacking; cross-origin isolation headers (COOP, COEP, CORP)

#### 9.5 SSRF, Deserialization & Server-Side Attacks 🔵
- SSRF: cloud metadata endpoints, DNS rebinding, allow-lists, egress controls
- Insecure deserialization; XXE; unsafe YAML
- File upload attacks; zip bombs; open redirects
- HTTP request smuggling; cache poisoning; host header attacks

#### 9.6 Password Storage, Sessions & Session Security 🟢
- Hashing with Argon2id (or bcrypt/scrypt); salts, peppers, parameter tuning
- Password policy per NIST: length over complexity, breached-password checks
- Server-side sessions: ID entropy, storage, rotation on login, idle and absolute timeouts, revocation
- Account-flow security: enumeration, reset tokens, email change, brute-force and credential-stuffing defenses

#### 9.7 Tokens & JWT: Design and Pitfalls 🔵
- JWT structure; JWS vs JWE; signature algorithms (HS256, RS256, ES256, EdDSA)
- Mandatory validation: `alg`, `iss`, `aud`, `exp`; key rotation via JWKS
- Classic attacks: `alg: none`, algorithm confusion, weak secrets, `kid` injection
- Revocation problem: short-lived access tokens, refresh-token rotation with reuse detection
- Token storage in browsers; the BFF pattern; when plain sessions are the better choice

#### 9.8 OAuth 2 & OpenID Connect 🔵
- Roles and grants: Authorization Code with PKCE, Client Credentials, Device Code; why Implicit and Password grants are gone
- OAuth 2.1 direction and security best practices
- OIDC: ID token vs access token, UserInfo, discovery
- `state`, `nonce`, exact redirect-URI matching
- Enterprise SSO: SAML basics, SCIM provisioning
- 🟣 Build vs buy identity (Keycloak, Auth0, Clerk, WorkOS): criteria and exit costs

#### 9.9 MFA, Passkeys & WebAuthn 🔵
- Factors: TOTP, SMS weaknesses, push, hardware keys
- WebAuthn: registration and authentication ceremonies, challenge, origin binding, attestation
- Passkeys: synced vs device-bound, conditional UI (autofill), phishing resistance
- Recovery flows as the weakest link; step-up authentication for sensitive actions

#### 9.10 Authorization Models: RBAC, ABAC & ReBAC 🟣
- Authentication vs authorization; broken access control (IDOR/BOLA) as the top API risk
- RBAC: roles, permissions, hierarchies, role explosion
- ABAC and policy engines (OPA, Cedar); ReBAC and Zanzibar-style systems (OpenFGA, SpiceDB)
- Enforcement points: gateway, service, data layer (RLS); centralized policy vs scattered checks
- Tenant isolation in authorization; testing permission matrices

#### 9.11 Secrets, Cryptography Basics & Data Protection 🔵
- Secrets management: vaults, cloud secret managers, rotation, no secrets in git or images
- Symmetric (AES-GCM) vs asymmetric (RSA, ECC) encryption; hashing vs MAC vs signature
- Never invent crypto; use vetted libraries; secure randomness
- Encryption in transit and at rest; envelope encryption with a KMS; field-level encryption
- Key rotation; constant-time comparison

#### 9.12 Supply-Chain Security 🔵
- npm risks: typosquatting, malicious install scripts, compromised maintainers, dependency confusion
- Lockfiles, `npm ci`, pinning, minimum release age, auditing (`npm audit`, Socket, Snyk)
- SBOMs, provenance and signing (Sigstore, SLSA levels)
- CI/CD hardening: least-privilege tokens, OIDC to cloud, pinned actions, protected branches
- Container image scanning; automated updates (Renovate, Dependabot)

#### 9.13 Audit Logging, Privacy & Compliance 🟣
- Audit logs: who, what, when, where; immutability; tenant-visible audit trails
- Security monitoring and alerting on suspicious patterns
- Privacy: PII classification, data minimization, GDPR rights (access, deletion, portability), retention, residency
- Compliance overview: SOC 2, ISO 27001, PCI DSS scope reduction, HIPAA awareness
- Security incident response; secure SDLC and security champions

**Part project:** harden Acme Orders: write a STRIDE threat model, add passkey login plus an OIDC provider, implement RBAC with tenant isolation tested by a permission matrix, add a strict CSP, and produce an audit log.

**Exit criteria:** you can attack your own application across the OWASP Top 10 and explain each defense in depth.

---

<a id="part-10"></a>
## Part 10 — Testing & Code Quality

**Goal:** a codebase the team can change quickly without fear.

#### 10.1 Testing Strategy & Philosophy 🔵
- What tests are for: confidence, design feedback, documentation
- Pyramid vs trophy vs honeycomb; choosing a shape for your architecture
- Test behavior, not implementation; cost vs value of each test type
- Coverage as a signal, not a target; mutation testing
- Flaky tests: causes, quarantine, zero-tolerance policy
- 🟣 Defining a test strategy for a team and a risk-based test plan

#### 10.2 Unit Testing & Test Doubles 🟢
- Vitest / Jest / `node:test`; arrange-act-assert; naming; one reason to fail
- Doubles: dummy, stub, spy, mock, fake, and the cost of over-mocking
- Controlling time, randomness, and the network
- Design for testability: pure core, dependency injection
- Property-based testing (fast-check); snapshot tests and their misuse

#### 10.3 Integration Testing with Real Dependencies 🔵
- Testcontainers for PostgreSQL, Redis, and brokers
- Isolation strategies: transaction rollback, truncate, schema or database per worker
- Test data: factories and builders over shared fixtures
- Testing migrations, queue consumers, and transactional behavior
- Keeping the integration suite fast and parallel

#### 10.4 Testing APIs & Contracts 🔵
- HTTP-level tests with Supertest or framework injection; testing auth and error paths
- Mocking outbound HTTP with MSW or nock
- Consumer-driven contract testing (Pact); provider verification
- Schema-based testing against the OpenAPI document; backward-compatibility checks

#### 10.5 Testing React Components 🟢
- Testing Library principles: query by role and label, act like a user
- `user-event`, async utilities, avoiding `act` warnings
- MSW for network; testing hooks; testing forms and error states
- Vitest browser mode vs jsdom; what to do about Server Components (test via E2E or as functions)
- Accessibility assertions; visual regression testing (Storybook, Chromatic)

#### 10.6 End-to-End Testing with Playwright 🔵
- Locators, auto-waiting, web-first assertions
- Fixtures, authentication state reuse, API-seeded test data
- Parallelism, sharding, retries, trace viewer
- Network interception; visual comparisons; mobile emulation
- Scope: critical user journeys only; smoke tests against production

#### 10.7 Performance, Load & Security Testing 🔵
- Load test types: smoke, load, stress, spike, soak; tools (k6, Artillery)
- Realistic workload models; reading percentiles (p95, p99); coordinated omission
- Frontend performance testing with Lighthouse CI and budgets
- SAST, DAST, dependency and secret scanning in the pipeline
- Chaos experiments and game days

#### 10.8 Code Quality: Linting, Formatting, Types & Code Review 🟢
- ESLint with typescript-eslint (type-aware rules), Biome / Oxlint, Prettier
- Git hooks, conventional commits, strictness ratchets
- Code review: what to look for, small PRs, tone, turnaround time, automation of the trivial
- Complexity metrics and their limits; documentation standards
- 🟣 Setting engineering standards that teams actually follow

#### 10.9 Refactoring & Technical Debt 🔵
- Code smells and the core refactorings; refactor in small, safe, tested steps
- Characterization tests and seams for legacy code
- Branch by abstraction; parallel change
- Classifying debt (deliberate vs accidental); a debt register
- 🟣 Making the business case for paying debt; refactor vs rewrite decision

**Part project:** bring Acme Orders to a full test strategy: unit tests on domain logic, Testcontainers integration tests, a contract test between frontend and API, five Playwright journeys, and a k6 load test with a written report.

**Exit criteria:** you can defend where every type of test sits and why, and your CI suite is fast and not flaky.

---

<a id="part-11"></a>
## Part 11 — Cloud, DevOps & Delivery *(new)*

**Goal:** ship safely many times a day and operate what you ship.

#### 11.1 Linux, Networking & Cloud Primitives 🟢
- Linux essentials: processes, signals, file descriptors, permissions, `systemd`, basic debugging tools (`top`, `ss`, `curl`, `dig`, `strace`)
- Networking: IP, CIDR, subnets, NAT, ports, firewalls, DNS record types
- Cloud building blocks: compute, object storage, managed databases, queues, VPC, security groups
- IAM: principals, roles, policies, least privilege
- Regions and availability zones; the shared responsibility model

#### 11.2 Containers & Docker 🟢
- Images vs containers; layers and build cache; namespaces and cgroups in brief
- Dockerfile best practices: multi-stage, small base, non-root, `.dockerignore`, reproducible installs
- Networking, volumes, health checks; Docker Compose for local environments
- Image tagging, registries, scanning, signing

#### 11.3 Kubernetes & Orchestration Essentials 🔵
- Core objects: Pod, Deployment, Service, Ingress / Gateway API, ConfigMap, Secret, Job, CronJob
- Requests and limits; probes; rolling updates; pod disruption budgets
- Autoscaling: HPA, KEDA (queue-based), cluster autoscaling
- Helm or Kustomize; GitOps (Argo CD, Flux)
- 🟣 When Kubernetes is overkill: managed container platforms (ECS/Fargate, Cloud Run, Fly, Render)

#### 11.4 Serverless, Edge & Managed Platforms 🔵
- Functions as a service: cold starts, concurrency model, limits, pricing
- Edge runtimes: Web-standard APIs, constraints, good use cases
- Database access from serverless: pooling, HTTP drivers, serverless databases
- Event-driven patterns with managed queues, schedulers, and workflows
- 🟣 Serverless vs containers vs PaaS: cost curve, lock-in, operations burden

#### 11.5 Infrastructure as Code & Environments 🔵
- Terraform / OpenTofu: providers, state, modules, plan and apply, drift
- Alternatives: Pulumi, CDK, SST
- Environment strategy: dev, preview per PR, staging, production; environment parity
- Secrets and config per environment; policy as code

#### 11.6 CI/CD, Quality Gates & Release Engineering 🔵
- Pipeline design: fast feedback first, caching, parallelism, affected-only builds in monorepos
- Quality gates: types, lint, tests, security scans, bundle and performance budgets
- Trunk-based development vs long-lived branches; merge queues
- Build once, promote the same artifact; database migrations in the pipeline
- Versioning, changelogs, release automation
- DORA metrics: deployment frequency, lead time, change failure rate, time to restore

#### 11.7 Deployment Strategies, Feature Flags & Progressive Delivery 🔵
- Rolling, blue-green, canary; automated rollback on SLO breach
- Feature flags: release, experiment, ops, and permission toggles; flag lifecycle and cleanup
- Separating deploy from release; dark launches; shadow traffic
- Backward-compatible deploys: API and schema compatibility across versions (N and N-1)

#### 11.8 Observability in Practice: Logs, Metrics, Traces & SLOs 🔵
- Three pillars plus profiling; structured logs with correlation IDs
- Metrics: counters, gauges, histograms; RED and USE methods; cardinality control
- Distributed tracing with OpenTelemetry: spans, context propagation, sampling
- SLI, SLO, error budgets; burn-rate alerting; alert on symptoms, not causes
- Dashboards that answer questions; frontend observability (RUM, error tracking)

#### 11.9 Incident Response, On-Call & Postmortems 🟣
- Incident lifecycle: detect, triage, mitigate, resolve, learn
- Roles: incident commander, communications, scribe; severity levels
- Mitigate first, diagnose second; rollback as the default move
- Runbooks; on-call health and sustainable rotations
- Blameless postmortems; contributing factors over "root cause"; tracking action items

#### 11.10 Cost Engineering (FinOps) 🟣
- Cloud pricing models: compute, storage, data transfer (egress), managed-service premiums
- Unit economics: cost per tenant, per request, per order
- Right-sizing, autoscaling, reserved or committed use, spot instances
- Tagging, budgets, anomaly alerts
- Cost as an architecture quality attribute in every design review

**Part project:** take Acme Orders to production: Docker images, Terraform-managed infrastructure, a CI/CD pipeline with gates and preview environments, canary deploys behind a feature flag, OpenTelemetry tracing, two SLOs with alerts, and one simulated incident with a written postmortem.

**Exit criteria:** you can deploy on a Friday afternoon without stress, and you can answer "what does one order cost us?"

---

<a id="part-12"></a>
## Part 12 — System Design (Backend + Frontend)

**Goal:** design systems that meet stated requirements, and communicate the design clearly under time pressure.

#### 12.1 The System Design Method & Interview Framework 🔵
- A repeatable flow: clarify requirements → estimate → API → data model → high-level design → deep dives → bottlenecks and trade-offs
- Functional vs non-functional requirements; turning vague goals into numbers
- Driving the conversation; managing time; drawing clear diagrams
- Stating trade-offs explicitly: "I choose X over Y because Z, at the cost of W"
- Common mistakes: jumping to a solution, over-engineering, ignoring data

#### 12.2 Estimation & Capacity Planning 🔵
- Back-of-envelope math: QPS, storage, bandwidth, memory
- Numbers to memorize: latency of memory, SSD, network; powers of two; seconds per day
- Average vs peak load; read/write ratio; growth projection
- Latency budgets across a request path; headroom
- Load testing to validate the estimate

#### 12.3 Load Balancing, Reverse Proxies & CDNs 🔵
- Layer 4 vs layer 7 balancing; algorithms (round robin, least connections, consistent hashing)
- Health checks, connection draining, TLS termination
- Reverse proxy duties: routing, compression, buffering, caching
- CDN: edge caching, cache keys, purging, origin shielding, edge compute
- Global traffic management: GeoDNS, anycast

#### 12.4 Scaling Data: Replication, Sharding & Consistency 🟣
- Read replicas and replication lag handling
- Sharding: key choice, hash vs range, hot partitions, resharding, cross-shard queries
- Consistent hashing with virtual nodes
- Consistency models: strong, eventual, causal, read-your-writes, monotonic reads
- Leader-follower, multi-leader, and leaderless replication; quorums; conflict resolution

#### 12.5 Distributed Systems Fundamentals: CAP, PACELC, Consensus & Clocks 🟣
- The fallacies of distributed computing; partial failure
- CAP in practice (the choice is made during a partition); PACELC (latency vs consistency otherwise)
- Consensus: what Raft provides (leader election, replicated log) and where you rely on it (etcd, ZooKeeper)
- Time: clock skew, logical clocks, vector clocks, hybrid logical clocks
- Why two-phase commit is avoided; split brain and fencing

#### 12.6 Reliability Patterns: Timeouts, Retries, Circuit Breakers & Bulkheads 🔵
- Timeouts everywhere; deadline propagation
- Retries with exponential backoff and jitter; retry budgets; retry storms
- Circuit breakers; bulkheads; rate limiting and load shedding
- Graceful degradation and fallbacks; idempotency as the enabler of retries
- Backpressure across services; queues as buffers; failure-mode analysis

#### 12.7 Multi-Region, Availability & Disaster Recovery 🟣 *(new)*
- Availability math: nines, serial vs parallel dependencies
- Single points of failure; redundancy across zones and regions
- Active-passive vs active-active; data replication across regions; conflict handling
- RPO and RTO; backup, pilot light, warm standby, hot standby
- Data residency constraints; cell-based architecture; DR drills

#### 12.8 Frontend Architecture: Rendering Strategies & Performance Budgets 🔵
- CSR, SSR, SSG, ISR, streaming, partial prerendering, islands, resumability: trade-off matrix
- Choosing per page type (marketing, dashboard, feed, editor)
- State and data architecture for large apps; API layer design; error and loading strategy
- Performance budgets tied to business metrics
- Frontend system design interview format: requirements, component tree, data model, API, optimizations

#### 12.9 Frontend at Scale: Micro-Frontends, Monorepos & Design Systems 🟣
- Monorepos: Turborepo / Nx, task graph, remote cache, package boundaries, ownership
- Micro-frontends: Module Federation, route-level composition; the costs (duplication, UX drift, coordination)
- Design system as a platform: tokens, components, versioning, adoption metrics
- Shared code strategy; dependency version policy
- Organizational fit: team autonomy vs consistency

#### 12.10 Case Studies I: Rate Limiter, Notification System, News Feed & Search 🔵
- Rate limiter: algorithm choice, distributed counters, failure behavior
- Notification system: channels, templates, preferences, retries, deduplication, priority
- News feed: fan-out on write vs read, ranking, pagination, the celebrity problem
- Search and autocomplete: indexing pipeline, relevance, typeahead with tries or prefix indexes

#### 12.11 Case Studies II: Payments, Chat, File Storage & Multi-Tenant SaaS 🟣 *(new)*
- Payments and ledger: double-entry bookkeeping, idempotency, reconciliation, provider webhooks
- Real-time chat and collaboration: connection gateway, ordering, presence, offline sync
- File storage and sharing: chunking, deduplication, metadata service, permissions
- Multi-tenant SaaS platform: isolation tiers, tenant routing, per-tenant limits, billing metering

#### 12.12 Capstone: Designing Acme Orders at Scale 🟣
- Requirements: 10,000 tenants, 50 million orders per month, 99.95% availability, EU and US data residency
- Full design: API, data model, service boundaries, sync and async flows
- Scaling plan from 10 to 10,000 tenants: what changes at each stage
- Failure analysis, SLOs, security model, cost estimate
- Deliverable: a design document with C4 diagrams and ADRs, presented in 45 minutes

**Part project:** the 12.12 capstone design document, reviewed by a peer or mentor.

**Exit criteria:** given any product prompt, you can produce a defensible design in 45 minutes and adapt it when requirements change.

---

<a id="part-13"></a>
## Part 13 — Software Architecture *(new)*

**Goal:** structure software so it stays cheap to change, and make trade-offs explicit.

#### 13.1 Architectural Thinking: Quality Attributes & Trade-Offs 🟣
- Architecture as the set of decisions that are expensive to change
- Quality attributes: performance, scalability, availability, security, modifiability, testability, operability, cost
- Quality attribute scenarios (stimulus, response, measure); architecturally significant requirements
- Every decision is a trade-off; "it depends" must be followed by "on what"
- Reversible vs irreversible decisions; deferring to the last responsible moment

#### 13.2 Design Principles: Coupling, Cohesion & SOLID 🔵
- Coupling and cohesion as the core measures; connascence
- SOLID applied pragmatically in TypeScript; dependency inversion in practice
- Information hiding; deep vs shallow modules
- DRY vs the wrong abstraction; YAGNI; rule of three
- The design patterns that still matter: strategy, adapter, decorator, observer, factory, repository

#### 13.3 Architecture Styles: Layered, Hexagonal, Clean & Vertical Slice 🔵
- Layered architecture and its failure modes
- Hexagonal (ports and adapters), onion, and clean architecture: the dependency rule
- Vertical slice / feature-based structure
- Applying each in NestJS and Next.js; folder structure follows architecture
- 🟣 Choosing by complexity: avoid heavy architecture for CRUD

#### 13.4 Domain-Driven Design: Strategic 🟣
- Ubiquitous language; subdomains (core, supporting, generic) and where to invest
- Bounded contexts; context mapping (customer-supplier, conformist, anti-corruption layer, shared kernel)
- Discovery techniques: event storming, domain storytelling
- Aligning contexts with teams

#### 13.5 Domain-Driven Design: Tactical 🔵
- Entities, value objects, aggregates and invariants, aggregate sizing
- Domain services, application services, repositories, factories
- Domain events; the rich vs anemic model debate
- Making illegal states unrepresentable with TypeScript types

#### 13.6 Modular Monolith to Microservices 🟣
- Modular monolith: enforced boundaries, module APIs, separate schemas
- Reasons to split that are valid (independent scaling, team autonomy, fault isolation) and reasons that are not
- Decomposition by bounded context; data ownership; no shared database
- Costs: network, consistency, operations, testing, local development
- Service granularity; distributed monolith warning signs

#### 13.7 Evolutionary Architecture & Legacy Modernization 🟣
- Fitness functions: automated checks on architectural properties (dependency rules, performance budgets)
- Strangler fig, branch by abstraction, anti-corruption layers
- Incremental migration planning; running old and new in parallel; verification
- Why big-bang rewrites fail; managing risk and stakeholder expectations
- Framework and major-version upgrade strategy

#### 13.8 Documenting Architecture: C4, ADRs & RFCs 🟣
- C4 model: context, container, component diagrams; diagrams as code (Mermaid, Structurizr)
- Architecture Decision Records: context, decision, alternatives, consequences
- RFC / design-doc process: template, review, decision, follow-up
- arc42 overview; keeping docs alive next to the code
- Writing for the audience: executive summary vs engineer detail

#### 13.9 Governance, Platform Engineering & Developer Experience 🟣
- Golden paths and paved roads; internal developer platforms
- Standards vs autonomy; a tech radar (adopt, trial, assess, hold)
- Architecture review without becoming a gate; guardrails over approvals
- Inner source, shared libraries, service templates
- Measuring developer experience (DORA, SPACE)

**Part project:** refactor one Acme Orders module to hexagonal architecture with a rich domain model; write five ADRs for the system; draw C4 context and container diagrams; add one fitness function to CI that enforces module boundaries.

**Exit criteria:** you can explain your architecture to a new engineer in ten minutes and to an executive in two.

---

<a id="part-14"></a>
## Part 14 — AI Engineering for Full-Stack *(new)*

**Goal:** build reliable LLM-powered features and judge when AI is the right tool.

#### 14.1 LLM Fundamentals for Engineers 🟢
- Tokens, context windows, sampling parameters, non-determinism
- Model families and selection: capability vs latency vs cost; hosted vs open-weight
- Hallucination and its causes; knowledge cutoff
- API basics: messages, system prompts, streaming, rate limits, pricing per token
- Prompt caching and batch processing

#### 14.2 Prompting, Structured Output & Tool Calling 🔵
- Prompt design: clear instructions, examples, role, constraints, output format
- Structured output with JSON Schema; validate everything with your schema library
- Tool (function) calling: defining tools, the call loop, error handling
- Prompt versioning and management as code
- Multimodal inputs: images, documents, audio

#### 14.3 Streaming AI UX in React & Next.js 🔵
- Streaming over SSE; rendering partial output; cancellation
- AI SDK patterns: chat state, tool results as UI, generative UI
- UX for uncertainty: citations, edit and retry, confidence cues, human confirmation
- Latency perception; optimistic interaction; long-running tasks in the background

#### 14.4 Embeddings, Vector Search & RAG 🔵
- Embeddings and similarity; chunking strategies
- Vector storage: `pgvector` vs dedicated vector databases
- Retrieval quality: hybrid search, reranking, metadata filtering, query rewriting
- RAG pipeline: ingest, retrieve, augment, generate, cite
- Tenant isolation and permission-aware retrieval; keeping the index fresh

#### 14.5 Agents, Workflows & MCP 🟣
- Workflows (fixed steps) vs agents (model decides); start with the simplest that works
- Agent loop: plan, act, observe; memory; context management
- Model Context Protocol: servers, tools, resources; exposing your product through MCP
- Durable execution for long tasks; human-in-the-loop approval
- Multi-agent patterns and their costs

#### 14.6 Evals, Observability & Cost 🟣
- Evaluation sets: golden data, code-based checks, LLM-as-judge, human review
- Regression testing prompts and models in CI
- Tracing LLM calls; tracking quality, latency, and token cost per feature and tenant
- Cost controls: model routing, caching, context trimming, budgets
- Online feedback loops

#### 14.7 AI Security & Governance 🟣
- Prompt injection (direct and indirect) and why it is not fully solved; limiting blast radius
- Least-privilege tools; sandboxing; confirming destructive actions
- Data leakage, PII handling, provider data-retention terms
- Output handling as untrusted input (XSS, SQL, command execution)
- OWASP Top 10 for LLM applications; regulatory awareness (EU AI Act)

#### 14.8 AI-Assisted Development 🔵
- Working with coding agents: clear specifications, small tasks, context files, verification
- Reviewing generated code: correctness, security, maintainability; you own what you merge
- AI in code review, testing, and migration work
- 🟣 Team policy: where AI helps, where it harms, skill development for juniors

**Part project:** add an AI assistant to Acme Orders: natural-language order search over RAG with tenant-safe retrieval, a tool-calling agent that drafts orders with human approval, an eval suite in CI, and an MCP server exposing read-only order data.

**Exit criteria:** you can show measured quality for your AI feature and explain its failure modes and security limits.

---

<a id="part-15"></a>
## Part 15 — Technical Leadership & the Architect Role *(new)*

**Goal:** multiply the output of teams, not only your own.

#### 15.1 The Role: Senior vs Staff vs Architect 🟣
- Scope growth: task → feature → system → organization
- Staff archetypes: tech lead, architect, solver, right hand
- The "architect elevator": moving between executives and engineers
- Staying hands-on; avoiding the ivory tower
- Finding and choosing high-leverage work

#### 15.2 Technical Strategy, Vision & Roadmaps 🟣
- Diagnosis → guiding policy → coherent actions
- Writing a technical vision and a strategy document
- Aligning technology with business goals and constraints
- Roadmaps: now / next / later; sequencing by risk and value
- Balancing feature work, platform work, and debt

#### 15.3 Decision Making: Build vs Buy & Technology Selection 🟣
- Decision frameworks: reversible vs irreversible, weighted criteria, cost of delay
- Build vs buy vs open source: total cost of ownership, core vs commodity, exit plan
- Technology evaluation: proof of concept, maturity, community, hiring market, team skills
- Innovation tokens and boring technology
- Disagree and commit; recording decisions in ADRs

#### 15.4 Communication, Writing & Influence 🟣
- Writing as the main tool: design docs, proposals, status updates
- Structure: conclusion first; one idea per paragraph
- Influence without authority: build trust, find sponsors, pre-align before the meeting
- Translating technical risk into business language for product and executives
- Running effective design reviews; handling disagreement

#### 15.5 Estimation, Planning & Delivering Large Projects 🟣
- Estimation under uncertainty: ranges, reference classes, and re-estimation
- Breaking large work into milestones that each deliver value
- De-risking early: prototypes, spikes, tackling the hardest part first
- Managing dependencies across teams; scope negotiation
- Tracking and reporting; landing the project (migration finished, old system removed)

#### 15.6 Mentoring, Hiring & Engineering Culture 🟣
- Mentoring vs coaching vs sponsoring; delegation that develops people
- Feedback: specific, timely, kind
- Code review and design review as teaching tools
- Interviewing: structured questions, rubrics, reducing bias
- Building culture: psychological safety, blamelessness, quality standards

#### 15.7 Organization Design: Conway's Law & Team Topologies 🟣
- Conway's law and the inverse Conway maneuver
- Team types: stream-aligned, platform, enabling, complicated-subsystem
- Interaction modes; cognitive load as a design constraint
- Ownership boundaries matching architecture boundaries
- Working with product and design as a triad

#### 15.8 Interviews & Career: Senior, Staff & Architect 🔵
- Loop structure: coding, system design, frontend design, architecture deep dive, behavioral
- Behavioral stories in STAR form: conflict, failure, influence, ambiguity, mentoring
- Presenting a past project: context, your decisions, trade-offs, results, what you would change
- Building a promotion case: evidence of scope and impact
- Continuous learning: reading list, public writing, talks, open source

**Part project:** write a one-page technical strategy for Acme Orders for the next 12 months; write an RFC for one significant change and have it reviewed; mentor one person through a part of this path.

**Exit criteria:** other engineers seek your review on designs, and your written proposals get adopted.

---

## Recommended reading

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
