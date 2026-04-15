# ASP.NET Core Learning Path — Master Index

> 🌐 [Versión en español](../es/00-index.md)

## How to use this path

This learning path is organized into **five progressive levels**, each building on the one before it. You don't need to start at Level 1 — in fact, most working developers won't. The levels are designed so you can jump in wherever your current knowledge ends and your curiosity begins. Level 1 covers foundations for newcomers, Level 2 builds practical skills for day-to-day work, Level 3 tackles the "why does it work that way?" questions, Level 4 walks you through the actual framework source code, and Level 5 prepares you to contribute back to the project.

**Use the self-assessment below to find your starting point.** Answer each question honestly — nobody's grading you. If you answer "no" to a question, that's your level. Start there, work through the modules in order, and move to the next level when you're ready. Each module lists an estimated time, but take as long as you need. Understanding beats speed every time.

Every module is structured around a single driving question — the kind of question that, once you can answer it confidently, means you truly understand the topic. The modules link directly into the ASP.NET Core source code in this repository (`dotnet/aspnetcore`), so you'll be reading real production code, not simplified examples. That's intentional. The best way to understand a framework is to read how it's actually built.

---

## Self-Assessment: Find your level

Work through these questions in order. **The first "no" answer tells you where to start.**

> **Q1: Can you explain what HTTP status codes, headers, and request/response bodies are?**
> - ✅ Yes → continue to Q2
> - ❌ No → **Start at [Level 1 — Foundations](#level-1--foundations)**

> **Q2: Can you describe what middleware does in ASP.NET Core and why ordering matters?**
> - ✅ Yes → continue to Q3
> - ❌ No → **Start at [Level 1 — Foundations](#level-1--foundations)**, module 1.3

> **Q3: Have you built a REST API with ASP.NET Core using either controllers or minimal APIs?**
> - ✅ Yes → continue to Q4
> - ❌ No → **Start at [Level 2 — Practitioner](#level-2--practitioner)**

> **Q4: Can you explain the difference between `Transient`, `Scoped`, and `Singleton` lifetimes — and describe a real bug caused by using the wrong one?**
> - ✅ Yes → continue to Q5
> - ❌ No → **Start at [Level 2 — Practitioner](#level-2--practitioner)**, module 2.3

> **Q5: Have you written a custom `IMiddleware` implementation and configured Kestrel for production use?**
> - ✅ Yes → continue to Q6
> - ❌ No → **Start at [Level 3 — Advanced](#level-3--advanced)**

> **Q6: Can you trace how `DfaMatcher` selects an endpoint, or explain how `ControllerActionInvoker` orchestrates filters?**
> - ✅ Yes → continue to Q7
> - ❌ No → **Start at [Level 4 — Internals](#level-4--internals)**

> **Q7: Have you read the source code of `IApplicationBuilder.Build()` and understand how the middleware delegate chain is compiled?**
> - ✅ Yes → continue to Q8
> - ❌ No → **Start at [Level 4 — Internals](#level-4--internals)**

> **Q8: Have you built `dotnet/aspnetcore` from source, run its test suite, and submitted (or considered submitting) a pull request?**
> - ✅ Yes → **You're at [Level 5 — Expert / Contributor](#level-5--expert--contributor)**. Pick any module that interests you.
> - ❌ No → **Start at [Level 5 — Expert / Contributor](#level-5--expert--contributor)**

---

## Path Overview

### Level 1 — Foundations

*You're new to ASP.NET Core or web development. These modules give you the mental model that everything else builds on.*

| Module | Topic | Est. Effort | Key Question It Answers |
|--------|-------|:-----------:|-------------------------|
| 1.1 | HTTP and Web Server Basics | 2 h | What is HTTP and how does a web server handle requests? |
| 1.2 | Your First ASP.NET Core Application | 3 h | What happens when you run `dotnet new web` and `dotnet run`? |
| 1.3 | The Middleware Pipeline | 2 h | How does a request travel through your application? |
| 1.4 | Routing Fundamentals | 2 h | How does ASP.NET Core map URLs to code? |
| 1.5 | Dependency Injection Basics | 2 h | What is DI and why does ASP.NET Core use it everywhere? |
| 1.6 | Configuration and Environments | 1.5 h | How does your app read settings and adapt to dev/prod? |

**Total estimated effort: ~12.5 hours**

---

### Level 2 — Practitioner

*You understand the basics and want to build real applications. These modules cover the everyday skills of a productive ASP.NET Core developer.*

| Module | Topic | Est. Effort | Key Question It Answers |
|--------|-------|:-----------:|-------------------------|
| 2.1 | Building APIs with Controllers and Minimal APIs | 3 h | What are the two programming models and when should I use each? |
| 2.2 | Model Binding and Validation | 2 h | How does ASP.NET Core turn HTTP data into C# objects? |
| 2.3 | Writing Custom Middleware | 2 h | How do I add my own logic to the request pipeline? |
| 2.4 | Authentication and Authorization Basics | 3 h | How do I secure my endpoints? |
| 2.5 | Error Handling and Logging | 2 h | How do I handle errors gracefully and track what's happening? |
| 2.6 | Entity Framework Core Integration | 3 h | How do I connect to a database and manage data? |

**Total estimated effort: ~15 hours**

---

### Level 3 — Advanced

*You're comfortable building apps and now want to understand the deeper mechanics. These modules turn "it works" into "I know exactly why it works."*

| Module | Topic | Est. Effort | Key Question It Answers |
|--------|-------|:-----------:|-------------------------|
| 3.1 | Middleware Pipeline Deep Dive | 3 h | How does middleware ordering affect behavior, and how do I debug it? |
| 3.2 | Routing Engine Internals | 3 h | How does ASP.NET Core match URLs to endpoints efficiently? |
| 3.3 | DI Scopes and Service Lifetimes | 2 h | Why do lifetime mismatches cause bugs, and how do I fix them? |
| 3.4 | Kestrel Server Configuration | 2 h | How do I configure the web server for production? |
| 3.5 | Performance Optimization | 3 h | Where are the hot paths and how do I optimize them? |
| 3.6 | Advanced Authentication Patterns | 2 h | How do policy schemes, claims transformation, and multi-scheme auth work? |

**Total estimated effort: ~15 hours**

---

### Level 4 — Internals

*You want to read and understand the ASP.NET Core source code. These modules guide you through the framework's most important internals, file by file.*

| Module | Topic | Est. Effort | Key Question It Answers |
|--------|-------|:-----------:|-------------------------|
| 4.1 | IApplicationBuilder and Pipeline Construction | 3 h | How is the middleware pipeline actually built and compiled? |
| 4.2 | DFA Matcher and Endpoint Selection | 4 h | How does routing build and traverse a state machine for URL matching? |
| 4.3 | MVC Action Execution Pipeline | 4 h | How do filters, model binding, and action invocation work internally? |
| 4.4 | ServiceProvider Resolution Mechanics | 3 h | How does DI resolve service graphs and manage scopes? |
| 4.5 | HttpContext and the Features Pattern | 3 h | How does ASP.NET Core abstract server differences? |
| 4.6 | WebApplicationBuilder Internals | 2 h | How does the builder compose hosting, DI, and middleware? |

**Total estimated effort: ~19 hours**

---

### Level 5 — Expert / Contributor

*You're ready to extend, modify, and contribute to the framework itself. These modules teach you how the team works and how to participate.*

| Module | Topic | Est. Effort | Key Question It Answers |
|--------|-------|:-----------:|-------------------------|
| 5.1 | Building ASP.NET Core from Source | 4 h | How do I clone, build, and test the framework locally? |
| 5.2 | Extending the Routing System | 4 h | How do I write custom `MatcherPolicy`, route constraints, and link generators? |
| 5.3 | Writing Framework-Quality Middleware | 3 h | What patterns does the framework use internally for middleware? |
| 5.4 | Custom Authentication Handlers | 3 h | How do I implement a custom authentication scheme from scratch? |
| 5.5 | Contributing to dotnet/aspnetcore | 3 h | What's the contribution workflow, test infrastructure, and review process? |
| 5.6 | Designing Custom Hosting Models | 3 h | How do I create specialized hosts for non-HTTP scenarios? |

**Total estimated effort: ~20 hours**

---

## Topic Areas (organized by skill path)

Use these cross-references to follow a single topic across all five levels — from first encounter to deep expertise.

### 🏗️ Hosting & Startup

- [Level 1: Your First ASP.NET Core Application](01-foundations-aspnet-core.md#lesson-12) — what `dotnet run` does under the hood
- [Level 2: Configuration and Environments](02-practitioner-aspnet-core.md) — `appsettings.json`, environment variables, and the options pattern
- [Level 3: Kestrel Server Configuration](03-advanced-aspnet-core.md) — endpoints, limits, HTTPS, and production tuning
- [Level 4: WebApplicationBuilder Internals](04-internals-aspnet-core.md) — how `WebApplicationBuilder` composes the host
- [Level 5: Designing Custom Hosting Models](05-expert-aspnet-core.md) — building specialized hosts for non-HTTP workloads

### 🔗 Middleware Pipeline

- [Level 1: The Middleware Pipeline](01-foundations-aspnet-core.md#lesson-13) — the request delegate chain and `Use`/`Map`/`Run`
- [Level 2: Writing Custom Middleware](02-practitioner-aspnet-core.md) — convention-based and `IMiddleware` approaches
- [Level 3: Middleware Pipeline Deep Dive](03-advanced-aspnet-core.md) — ordering, branching, and diagnostic debugging
- [Level 4: IApplicationBuilder and Pipeline Construction](04-internals-aspnet-core.md) — how `Build()` compiles the delegate chain
- [Level 5: Writing Framework-Quality Middleware](05-expert-aspnet-core.md) — patterns from the framework's own middleware

### 🗺️ Routing

- [Level 1: Routing Fundamentals](01-foundations-aspnet-core.md#lesson-14) — route templates, parameters, and constraints
- [Level 2: Controllers and Minimal APIs](02-practitioner-aspnet-core.md) — the two programming models and their routing
- [Level 3: Routing Engine Internals](03-advanced-aspnet-core.md) — how the `EndpointRoutingMiddleware` and `EndpointMiddleware` cooperate
- [Level 4: DFA Matcher and Endpoint Selection](04-internals-aspnet-core.md) — the state machine that powers URL matching
- [Level 5: Extending the Routing System](05-expert-aspnet-core.md) — custom `MatcherPolicy`, constraints, and link generators

### 💉 Dependency Injection

- [Level 1: DI Basics](01-foundations-aspnet-core.md#lesson-15) — registering and resolving services
- [Level 2: Service Registration Patterns](02-practitioner-aspnet-core.md) — factory registrations, `TryAdd`, and keyed services
- [Level 3: DI Scopes and Service Lifetimes](03-advanced-aspnet-core.md) — captive dependencies and scope validation
- [Level 4: ServiceProvider Resolution Mechanics](04-internals-aspnet-core.md) — how the container builds and caches service graphs
- [Level 5: Contributing Custom DI Extensions](05-expert-aspnet-core.md) — writing `Add*` extension methods the framework way

### 🔒 Security

- [Level 1: Security Concepts](01-foundations-aspnet-core.md) — HTTPS, CORS, and why security matters from day one
- [Level 2: Authentication and Authorization Basics](02-practitioner-aspnet-core.md) — cookies, JWT, `[Authorize]`, and policies
- [Level 3: Advanced Authentication Patterns](03-advanced-aspnet-core.md) — policy schemes, claims transformation, and multi-scheme auth
- [Level 4: Authorization Pipeline Internals](04-internals-aspnet-core.md) — how `AuthorizationMiddleware` evaluates policies
- [Level 5: Custom Authentication Handlers](05-expert-aspnet-core.md) — implementing `AuthenticationHandler<T>` from scratch

### 🎯 MVC & API Design

- [Level 2: Controllers and Minimal APIs](02-practitioner-aspnet-core.md) — building APIs with both programming models
- [Level 2: Model Binding and Validation](02-practitioner-aspnet-core.md) — turning HTTP requests into validated C# objects
- [Level 3: Performance Optimization](03-advanced-aspnet-core.md) — output caching, response compression, and async patterns
- [Level 4: MVC Action Execution Pipeline](04-internals-aspnet-core.md) — `ControllerActionInvoker`, filters, and the resource pipeline
- [Level 5: Contributing to dotnet/aspnetcore](05-expert-aspnet-core.md) — the full contribution workflow and test infrastructure
