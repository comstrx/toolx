# ✨ ToolX - The Comstrx Engineering Toolchain

> Build one enterprise system the hard way.  
> Extract the engineering.  
> Never rebuild it the same way again.

**ToolX** is a focused engineering ecosystem for building production-grade software faster without sacrificing architecture, performance, maintainability, security, or control.

It contains exactly five tools:

```text
RustX
InfraX
SkillX
WebX
MobileX
```

Each tool is:

- self-contained;
- independently usable;
- opinionated;
- production-grade;
- focused on one responsibility;
- free from sibling ToolX dependencies.

ToolX is not designed in isolation.

It is **proven inside SaaSX**, hardened against real requirements, then extracted as reusable engineering infrastructure.

---

## The Vision

Modern software repeatedly rebuilds the same foundations:

```text
backend
web
mobile
infrastructure
engineering knowledge
```

ToolX turns those repeated foundations into reusable systems.

```text
SaaSX builds the evidence.
ToolX captures the engineering.
SkillX captures the knowledge.
```

The long-term goal:

```text
ToolX + SkillX + powerful AI agents
                ↓
build the next enterprise SaaS dramatically faster
```

AI accelerates implementation.

ToolX provides the engineering system.

Human judgment remains in control.

---

# The Five Tools

## RustX

> The coherent Rust foundation for backend, systems, and infrastructure software.

**RustX** is a Rust workspace designed as an extended standard/application library.

It provides consistent primitives and higher-level building blocks for areas such as:

```text
errors
memory
allocation
buffers
SIMD
I/O
logging
parsing
validation
collections
process
system
database
cache
networking
HTTP
web
```

RustX is not a random collection of crates.

Every crate/module follows the same engineering language:

```text
one naming style
one error model
one lifecycle
one configuration philosophy
one dependency direction
one quality bar
```

Dependencies flow one way only.

Performance-sensitive techniques such as SIMD, arenas, preallocation, zero-copy, zero-allocation, cache-aware layouts, and specialized data structures are broadly evaluated and kept only when measurement justifies them.

```text
optimization eligibility = universal
optimization adoption    = evidence-based
```

RustX is born primarily from `saasx/api/core`.

---

## InfraX

> Infrastructure as a programmable operational system.

**InfraX** is a self-contained infrastructure engine written in Rust.

It owns reusable infrastructure concerns such as:

```text
providers
resources
dependency graphs
state
planning
apply
deployment
health
rollback
environments
secret references
observability hooks
```

Product-specific intent belongs in manifests and configuration, not in the engine.

For example:

```text
Infra.lua
environment manifests
.env contracts
secret references
provider configuration
```

InfraX may orchestrate strong ecosystem tools instead of reinventing them:

```text
OpenTofu / Terraform
Docker
Kubernetes
Helm
Argo CD
Ansible
Prometheus
Grafana
Loki
OpenTelemetry
cloud/provider CLIs
secret managers
CI/CD systems
```

InfraX is intentionally independent from RustX until using RustX becomes a proven production advantage.

Conceptually:

```text
saasx/infra → InfraX
```

---

## SkillX

> The engineering knowledge runtime for AI agents.

**SkillX** is not an AI agent.

It is a lightweight Rust runtime that stores structured engineering knowledge as a graph and exposes relevant knowledge to external AI agents through MCP.

Conceptually:

```text
knowledge
   ↓
structured graph
   ↓
Rust runtime
   ↓
MCP
   ↓
AI agent
```

SkillX can contain knowledge about:

```text
Rust
TypeScript / Node
React / Next.js
backend architecture
web/mobile architecture
databases
cache
infrastructure
security
performance
commerce
payments
finance
SaaS
multi-tenancy
catalogs
business workflows
RustX
WebX
MobileX
InfraX
```

The goal is not to make AI autonomous.

The goal is to give strong AI agents the right engineering context, constraints, patterns, and project knowledge at the moment they need it.

Conceptually:

```text
saasx/skill → SkillX
```

---

## WebX

> One spec-driven web engine for every browser surface.

**WebX** is built on:

```text
Next.js
React
TypeScript
```

plus carefully selected production-grade libraries for state, data, forms, motion, icons, accessibility, testing, and other justified needs.

It is designed to power both:

```text
SEO websites
application surfaces
admin panels
```

from one reusable engine.

Project behavior lives in specs:

```text
specs/
├── super/
├── admin/
├── vendor/
├── delivery/
├── client/
└── tenant/
```

The reusable engine stays brand-neutral and business-neutral.

Conceptually:

```text
saasx/web - specs/ = WebX
```

WebX is not a dashboard template and not a low-code toy.

It is a programmable web foundation capable of producing deeply customized enterprise experiences while keeping architecture, behavior, and design coherent.

---

## MobileX

> The spec-driven mobile engine.

**MobileX** applies the same architecture to mobile applications, primarily through React Native and a carefully selected production stack.

Applications are described through specs while the engine remains reusable.

The same foundation can support:

```text
one multi-role app
```

with role-aware experiences after login, or:

```text
separate role-specific builds
```

for client, tenant, vendor, delivery, or other product modes.

Conceptually:

```text
saasx/mobile - specs/ = MobileX
```

One engine.

Different products, roles, flows, themes, and capabilities.

---

# SaaSX → ToolX

ToolX is not invented first and forced onto a product.

The reusable engineering is discovered and proven inside **SaaSX**.

```text
saasx/
├── api/
├── web/
├── mobile/
├── infra/
└── skill/
```

Expected extraction:

```text
saasx/api/core  → RustX
saasx/web       → WebX      (remove specs/)
saasx/mobile    → MobileX   (remove specs/)
saasx/infra     → InfraX
saasx/skill     → SkillX
```

The lifecycle:

```text
real SaaSX requirement
        ↓
build the clean solution
        ↓
identify the reusable primitive
        ↓
test + benchmark + production pressure
        ↓
stabilize the abstraction
        ↓
extract it into ToolX
        ↓
make SaaSX consume the extracted tool
```

Extraction is complete only when SaaSX itself consumes the extracted tool.

The target is **packaging, not architectural surgery**.

---

## Why SaaSX

SaaSX is the real enterprise product that pressure-tests ToolX.

It is designed around:

```text
multi-tenant
multi-role
multi-product-type
unified catalog
```

with surfaces such as:

```text
super panel
admin panel
vendor panel
delivery panel
client SEO site
tenant SEO site
mobile app
```

SaaSX must remain a strong product even if ToolX disappears.

ToolX must remain useful even outside SaaSX.

That separation is intentional.

---

# Core Engineering Laws

## Independence

No ToolX tool depends on another ToolX tool.

```text
RustX   ─┐
WebX    ─┤
MobileX ─┤── independent tools
InfraX  ─┤
SkillX  ─┘
```

Shared philosophy does not require shared runtime dependencies.

## Generic Core, Product Specs

Reusable engines stay generic.

Product-specific concepts belong in:

```text
specs
manifests
configuration
data
knowledge packs
```

not inside reusable cores.

For `saasx/api/core`:

```text
outside → core
core    ↛ outside
```

Architecture tests, lints, and CI should enforce these rules.

## Production First

Production-grade is a **quality constraint**, not a scope requirement.

Every implemented capability should optimize for:

```text
correctness
security
simplicity
performance
maintainability
observability
developer experience
failure behavior
```

## Measure, Do Not Assume

Performance claims require evidence.

Use:

```text
benchmarks
profiling
memory measurements
real workloads
production behavior
```

before accepting complexity.

## One Opinionated Stack

ToolX does not aim to support every language, framework, ORM, UI system, or platform.

It deliberately focuses on a strong vertical stack:

```text
Rust
TypeScript / Node
React / Next.js
React Native
selected databases/cache
selected infrastructure patterns
```

Depth and coherence matter more than ecosystem breadth.

---

# Design Standard

WebX and MobileX must produce interfaces that feel like serious enterprise products, not generated templates.

The bar includes:

```text
strong hierarchy
clean composition
excellent typography
eye comfort
responsive behavior
accessibility
motion
interaction quality
brand coherence
original 3D visual language
```

Light and dark themes are separate art directions, not simple inversions.

Important product states — empty, error, success, onboarding, offers, coupons, rewards, confirmations — should receive deliberate visual treatment.

UI work is complete only when it is:

```text
functionally correct
+ visually exceptional
+ brand-coherent
+ responsive
+ accessible
+ interaction-complete
+ visually verified
```

---

# AI + ToolX

ToolX is designed for an AI-assisted engineering era.

AI can accelerate:

```text
implementation
research
refactoring
testing
benchmarking
documentation
review
```

but architecture remains deliberate.

The intended model:

```text
human engineering judgment
        +
ToolX
        +
SkillX
        +
powerful AI agents
        ↓
extreme engineering leverage
```

The goal is not more agents.

The goal is more correct work per unit of time.

---

# Project Status

## Active ToolX

```text
RustX
WebX
MobileX
InfraX
SkillX
```

These five tools define the current ToolX roadmap.

## Outside ToolX

**AliasX** is a personal Linux/macOS workflow tool and remains outside ToolX.

## Discontinued

```text
AgentX
BashX
```

Development is stopped.

## Deferred

```text
WasmX
PyX
```

They may return later as optional layers around RustX, but they are not part of the current architecture or roadmap.

---

# End State

The target outcome is:

### 1. SaaSX

A real enterprise SaaS capable of competing with serious production systems.

### 2. ToolX

Five production-grade tools that dramatically reduce the cost of building the next SaaSX-class product.

### 3. SkillX

A reusable engineering knowledge system that lets powerful AI agents work inside a disciplined, opinionated architecture instead of rediscovering the same decisions repeatedly.

The flywheel:

```text
SaaSX
  ↓
production evidence
  ↓
ToolX + SkillX
  ↓
AI-assisted enterprise engineering
  ↓
next SaaSX-class system
  ↓
dramatically faster
```

**SaaSX should be the last enterprise SaaS we build the hard way.**

---

# Build the product. Extract the engineering. Compound the advantage.

---

# License

<code>toolx</code> is dual-licensed under either
[MIT](https://github.com/comstrx/toolx/blob/main/LICENSE-MIT) or
[Apache-2.0](https://github.com/comstrx/toolx/blob/main/LICENSE-APACHE), at your option.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this work by you, as defined in the Apache-2.0 license, shall be
dual-licensed as above, without any additional terms or conditions.
