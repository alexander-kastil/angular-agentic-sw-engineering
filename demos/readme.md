# Angular Agentic Software Engineering with Claude Code & GitHub Copilot

This workshop is for experienced Angular developers who want to master modern Angular development and learn to work with AI agents as a natural part of their daily workflow. Over twelve modules you will build real Angular v22 applications using standalone components, signal-based state, signal queries, and inject-based dependency injection throughout. Every concept is introduced through working demos that you can run, extend, and experiment with.

You start by setting up Claude Code and GitHub Copilot as your development partners, learning to write harness files, skills, subagents, and hooks that shape how these agents assist you across every module that follows. The tools and habits you establish here stay with you for the rest of the course, so agentic development is not a standalone topic but a way of working you bring to every subsequent module.

With your tooling in place, you move into Angular's reactive core. Signals are the primary state primitive in modern Angular, and you cover the complete API including `signal()`, `computed()`, `effect()`, `linkedSignal()`, and `model()`, together with `httpResource()`, resource `chain()`, streaming resources, and `debounced()` for declarative data loading. The component module then builds on that foundation with signal queries, modern control flow, content projection, directive composition, programmatic components, `@angular/aria`, and `@defer`.

Signal Forms introduce a schema-driven approach to form construction where field state is exposed as signals that wire directly into your templates, including `validateHttp`, `FormValueControl`, JSON-driven dynamic forms, and date validators. You then step into reactive programming with RxJS, covering flattening and combining strategies, error handling, custom operators, and the interop patterns that connect observables and signals in both directions.

Application-level state comes next with NgRx SignalStore. You build stores using `withState()`, `withComputed()`, `withMethods()`, and `withEntities()`, compose them with `withFeature` and `withProps`, extend resources, and use the events plugin. Advanced routing follows, covering functional guards, HTTP interceptors, signal-based resolvers, route inputs, `provideAppInitializer` with `injectAsync`, `animate.enter`/`animate.leave`, and view transitions.

The last modules focus on production quality. Testing with Vitest covers signal input tests, service tests, SignalStore tests, zoneless async testing, and Playwright, built around a demo where the agent writes the spec and a mutation round proves it. WebMCP then turns the application itself into something an agent can drive: seven demos expose a plain page, a signal, a component, a signal form, a SignalStore and the router as agent tools, and a suite that calls those tools the way an agent would. Optimization and compliance covers Lighthouse, Rolldown bundle optimization, `@defer` triggers, virtual scrolling, image optimization, WCAG 2.2 AA with `@angular/aria`, and a gate on the pull request. Hybrid rendering closes the Angular topics with server routes, `AngularNodeAppEngine`, incremental hydration, and the transfer cache. The course ends with an agentic DevOps track that deploys and verifies a real site.

By the end of the workshop you will have a thorough understanding of how modern Angular applications are structured and a set of agentic workflows that make you faster at building and maintaining them. The combination of deep Angular knowledge and effective AI collaboration is what this course is designed to give you.

## Duration

4.5 Days, 12 Modules

Four full days of 09:00 to 17:00 plus a closing half day, with one hour for lunch and two
15 minute breaks. That is 390 net minutes on days 1 to 4 and 195 on day 5, so 1755 minutes of
class time in total.

## Schedule

| Day | Clock          | Length | Deliverable                                                                               | Description                                                                                                                                                                                                                     |
| --- | -------------- | ------ | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | 09:00 to 09:30 | 30m    | Welcome and environment setup                                                             |                                                                                                                                                                                                                                 |
| 1   | 09:30 to 10:45 | 1h 15m | [Agentic Angular Software Engineering](./01-agentic-dev/)                                 | Angular CLI MCP server, harness files, Angular agent skills, the Angular expert subagent, hooks and quality gates (6 demos)                                                                                                     |
| 1   | 10:45 to 11:00 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 1   | 11:00 to 11:40 | 40m    | [Lab: Build the Secrets and Document Vault Workbench](../labs/lab-01/readme.md)           | Give the agent the repository: MCP servers, harness files, a design system, a subagent and a hook, then run the five-list workbench                                                                                             |
| 1   | 11:40 to 12:40 | 1h 00m | Lunch                                                                                     |                                                                                                                                                                                                                                 |
| 1   | 12:40 to 14:55 | 2h 15m | [Mastering Signals](./02-signals/)                                                        | signal(), computed(), effect(), inputs, model(), linkedSignal, httpResource, resource chain, debounced(), @Service and injectAsync, the DevTools signal graph (16 demos)                                                        |
| 1   | 14:55 to 15:10 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 1   | 15:10 to 15:50 | 40m    | [Lab: Load the Secrets of a List with Signals](../labs/lab-02/readme.md)                  | Selection as state, lists that load themselves, a debounced search and masked values, all in signals                                                                                                                            |
| 1   | 15:50 to 17:00 | 1h 10m | [Component Composition and Signal Queries](./03-components/)                              | Template syntax and control flow, signal queries, content projection, directive composition, programmatic components, resource() and @defer, @angular/aria, agent-driven refactoring (14 demos)                                 |
| 2   | 09:00 to 09:45 | 45m    | [Component Composition and Signal Queries (continued)](./03-components/)                  | Remaining topics (14 demos)                                                                                                                                                                                                     |
| 2   | 09:45 to 10:20 | 35m    | [Lab: Compose the Workbench from Accessible Components](../labs/lab-03/readme.md)         | Split the page into a resizable two-pane workbench built on @angular/aria, with version history loaded on request                                                                                                               |
| 2   | 10:20 to 10:35 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 2   | 10:35 to 13:05 | 2h 30m | [Signal Forms](./04-signal-forms/)                                                        | Form basics and fields, validators including validateHttp and validateAsync, error handling with isSignalErrorState, arrays and dynamic forms, AI-written tests (22 demos)                                                      |
| 2   | 13:05 to 14:05 | 1h 00m | Lunch                                                                                     |                                                                                                                                                                                                                                 |
| 2   | 14:05 to 14:40 | 35m    | [Lab: Edit a Secret with a Signal Form](../labs/lab-04/readme.md)                         | Turn the detail pane into an editable signal form with a server-side name check and one PUT on save                                                                                                                             |
| 2   | 14:40 to 14:55 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 2   | 14:55 to 16:05 | 1h 10m | [RxJS Where It Still Matters](./05-reactive/)                                             | Subscribe, stream and signal, flattening and combining strategies, error handling and custom operators, signal interop, rxResource, agent-assisted migration (8 demos)                                                          |
| 2   | 16:05 to 16:35 | 30m    | [Lab: Upload, Export and Retry with RxJS](../labs/lab-05/readme.md)                       | A file upload with live progress, a CSV export and one retry operator shared by every risky call                                                                                                                                |
| 2   | 16:35 to 17:00 | 25m    | [State Management with NgRx SignalStore](./06-ngrx-signals/)                              | withState, withComputed, withMethods, withEntities, store composition, resource extensions and the events plugin (13 demos)                                                                                                     |
| 3   | 09:00 to 10:25 | 1h 25m | [State Management with NgRx SignalStore (continued)](./06-ngrx-signals/)                  | Remaining topics (13 demos)                                                                                                                                                                                                     |
| 3   | 10:25 to 10:40 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 3   | 10:40 to 11:15 | 35m    | [Lab: Replace the Scattered Signals with a SignalStore](../labs/lab-06/readme.md)         | Move the state of three components into one SecretsStore assembled from three features                                                                                                                                          |
| 3   | 11:15 to 13:25 | 2h 10m | [Advanced Routing and App Initialization](./07-routing-app-init/)                         | provideAppInitializer with injectAsync, functional guards, HTTP interceptors, error handling, signal-based resolvers, route inputs, animate.enter and animate.leave, view transitions, route-driven SignalStore (18 demos)      |
| 3   | 13:25 to 14:25 | 1h 00m | Lunch                                                                                     |                                                                                                                                                                                                                                 |
| 3   | 14:25 to 15:00 | 35m    | [Lab: Put the Workbench State in the URL](../labs/lab-07/readme.md)                       | Route parameters for the selected list and open secret, a guard, an interceptor and a resolver that make deep links work                                                                                                        |
| 3   | 15:00 to 15:15 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 3   | 15:15 to 17:00 | 1h 45m | [Advanced Testing with Vitest and Playwright](./08-testing/)                              | Karma to Vitest migration, Vitest fundamentals, signal input, form and store tests, zoneless async testing, Playwright, agent-written specs proven by mutation (19 demos)                                                       |
| 4   | 09:00 to 09:25 | 25m    | [Advanced Testing with Vitest and Playwright (continued)](./08-testing/)                  | Remaining topics (19 demos)                                                                                                                                                                                                     |
| 4   | 09:25 to 10:00 | 35m    | [Lab: Let the Agent Write the Specs and Prove Them by Mutation](../labs/lab-08/readme.md) | Agent-written specs for the fragile parts, a Playwright run against the real API, and deliberate breakage to check the specs                                                                                                    |
| 4   | 10:00 to 10:15 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 4   | 10:15 to 11:25 | 1h 10m | [WebMCP - The Agentic Web](./09-webmcp/)                                                  | A counterpart page for the agent, signals, components, signal forms and SignalStore methods as tools, navigation tools, end-to-end tool tests (7 demos)                                                                         |
| 4   | 11:25 to 11:55 | 30m    | [Lab: Expose the Workbench as Agent Tools](../labs/lab-09/readme.md)                      | Expose the store, router and form as agent tools, and choose the short list of tools the agent must never get                                                                                                                   |
| 4   | 11:55 to 12:55 | 1h 00m | Lunch                                                                                     |                                                                                                                                                                                                                                 |
| 4   | 12:55 to 14:45 | 1h 50m | [Optimization and Compliance](./10-optimize-compliance/)                                  | Lighthouse and Core Web Vitals, Rolldown bundle optimization and budgets, @defer triggers, zoneless and DevTools profiling, virtual scrolling, image optimization, WCAG 2.2 AA, compliance gates on the pull request (15 demos) |
| 4   | 14:45 to 15:00 | 15m    | Break                                                                                     |                                                                                                                                                                                                                                 |
| 4   | 15:00 to 15:30 | 30m    | [Lab: Measure the Workbench and Gate What You Fixed](../labs/lab-10/readme.md)            | Measure the bundle, a list of two thousand secrets and the accessibility of the masked control, fix the findings, and gate the pull request                                                                                     |
| 4   | 15:30 to 16:35 | 1h 05m | [Hybrid Rendering and Hydration](./11-ssr/)                                               | Server routes with RenderMode and getPrerenderParams, Express 5 with AngularNodeAppEngine, incremental hydration and triggers, transfer cache with httpResource, measured CSR versus SSR delta (7 demos)                        |
| 4   | 16:35 to 17:00 | 25m    | Buffer                                                                                    |                                                                                                                                                                                                                                 |
| 5   | 09:00 to 09:30 | 30m    | [Lab: Choose a Render Mode per Route](../labs/lab-11/readme.md)                           | Add SSR, decide the render mode for each route, and prove the choice by reading the HTML off the wire                                                                                                                           |
| 5   | 09:30 to 11:10 | 1h 40m | [Agentic Angular DevOps](./12-agentic-devops/)                                            | The deployment agent with allowlists and manifest, bootstrapping and hardening an Ubuntu box, multi-stage containers behind Caddy, DNS before the first ACME attempt, Core Web Vitals and SEO loop (4 demos)                    |
| 5   | 11:10 to 11:45 | 35m    | [Lab: Deploy the Workbench to an Ubuntu Box over SSH](../labs/lab-12/readme.md)           | Ship both images over SSH, put a Caddy edge with TLS in front of the API and the app, and hand the redeploy loop to an agent                                                                                                    |
| 5   | 11:45 to 12:00 | 15m    | Wrap-up                                                                                   |                                                                                                                                                                                                                                 |
| 5   | 12:00 to 12:15 | 15m    | Buffer                                                                                    |                                                                                                                                                                                                                                 |

## Audience

- Experienced Angular developers adopting modern Angular v22 patterns
- Teams migrating from legacy patterns to signals, Signal Forms, and NgRx SignalStore
- Developers seeking structured coverage of advanced routing, testing, performance, compliance, and SSR

## Prerequisites

- Solid experience with Angular (components, services, routing, forms)
- Familiarity with TypeScript and RxJS basics

## Modules

### [Module 01: Agentic Angular Software Engineering](./01-agentic-dev/)

- The Angular CLI MCP Server
- Harness Files: CLAUDE.md, AGENTS.md, copilot-instructions.md
- Angular Agent Skills
- The Angular Expert Subagent
- Hooks and Quality Gates

### [Module 02: Mastering Signals](./02-signals/)

- Signals Fundamentals: signal(), computed(), effect()
- Signal Patterns: inputs, model(), linkedSignal, equality
- Async Signals: httpResource(), resource chain(), debounced()
- @Service and injectAsync
- Signals Tooling: the DevTools signal graph

### [Module 03: Component Composition and Signal Queries](./03-components/)

- Modern Template Syntax and Control Flow
- Signal Queries: viewChild, viewChildren, contentChild, contentChildren
- Content Projection, Directive Composition, Programmatic Components
- Data Loading with resource() and @defer
- Accessible Composition with @angular/aria
- Component Antipatterns and Agent-Driven Refactoring

### [Module 04: Signal Forms](./04-signal-forms/)

- Signal Form Basics: form(), fields, submission
- Validation: validators, validateHttp, validateAsync, validateStandardSchema
- Error Handling with isSignalErrorState
- Advanced: arrays, nested objects, dynamic forms
- Signal Forms and Agents: AI-written tests

### [Module 05: RxJS Where It Still Matters](./05-reactive/)

- Subscribe vs Stream vs Signal
- Flattening and Combining Strategies
- Error Handling and Custom Operators
- Signal Interop Both Ways, rxResource, debounce
- Agent-Assisted RxJS to Signals Migration

### [Module 06: State Management with NgRx SignalStore](./06-ngrx-signals/)

- SignalStore Fundamentals: withState(), withComputed(), withMethods()
- Entity Management with withEntities()
- Store Composition: signalMethod, withFeature, withProps
- Resource Extensions and Linked State
- The Events Plugin and Deep Signals

### [Module 07: Advanced Routing and App Initialization](./07-routing-app-init/)

- provideAppInitializer with injectAsync, @Service
- Functional Guards, HTTP Interceptors, Error Handling
- Signal-Based Resolvers and Route Inputs
- animate.enter / animate.leave and View Transitions
- Route-Driven SignalStore

### [Module 08: Advanced Testing with Vitest and Playwright](./08-testing/)

- Karma to Vitest Migration
- Vitest Fundamentals: pipes, directives, services, components
- Signal Inputs, Forms and Store Testing
- Zoneless Async: whenStable, TestBed.tick, getLastFixture
- Playwright Fundamentals
- Agent-Written Specs, Proven by Mutation

### [Module 09: WebMCP - The Agentic Web](./09-webmcp/)

- A Counterpart Page for the Agent
- Signals as WebMCP Tools
- WebMCP in Components
- A Signal Form as an Agent Tool
- SignalStore Methods as Tools
- Navigation Tools for the Agent
- Testing WebMCP Tools End to End

### [Module 10: Optimization and Compliance](./10-optimize-compliance/)

- Core Web Vitals Measurement with Lighthouse
- Bundle Optimization with Rolldown and Budgets
- @defer by Trigger, Zoneless, DevTools Profiling
- Virtual Scrolling and Image Optimization
- WCAG 2.2 AA with @angular/aria
- Compliance Gates on the Pull Request

### [Module 11: Hybrid Rendering and Hydration](./11-ssr/)

- Server Routes with RenderMode and getPrerenderParams
- Express 5 with AngularNodeAppEngine
- Incremental Hydration and Hydrate Triggers
- Transfer Cache with httpResource
- CSR vs SSR Measured Delta

### [Module 12: Agentic Angular DevOps](./12-agentic-devops/)

- The Deployment Agent: Allowlists and Manifest
- Bootstrapping and Hardening an Ubuntu Box
- Multi-Stage Container serving with Caddy
- DNS before the First ACME Attempt
- Core Web Vitals and SEO Loop

### [Optional Module 13: OAuth for Angular](./13-oauth/)

- OAuth 2.0 and OpenID Connect, Reading a JWT
- Bearer Tokens on HttpClient, Functional Auth Interceptor
- Auth State in a SignalStore, Guarding Routes with canMatch, The Sign-In Round Trip
- Firebase Authentication, Microsoft Entra ID with MSAL Angular, MSAL vs Easy Auth
