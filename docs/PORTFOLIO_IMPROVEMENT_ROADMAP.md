# Portfolio-Driven Improvement Roadmap

## Goal

Improve `awesome-llm-apps` using lessons proven in the connected project portfolio, while keeping every existing product independent.

## Phase 1 — Foundation

- [x] Audit the connected project portfolio.
- [x] Identify reusable patterns.
- [x] Document product-to-pattern mapping.
- [ ] Add a reusable pattern index to the main README.
- [ ] Add a standard example contract: purpose, architecture, setup, env vars, run command, expected output, limitations.

## Phase 2 — High-value reusable patterns

### A. Grounded generation

Create a small example showing:

`document/data -> schema -> retrieval -> constrained generation -> validation`

Requirements:
- explicit source-of-truth rules
- no invented facts
- structured output
- validation failure path

### B. Deterministic + AI decision engine

Create an example showing:

`normalized records -> deterministic score -> AI explanation -> decision`

The AI must not silently override deterministic business rules.

### C. Provider router

Create a provider abstraction with:

- primary provider
- fallback provider
- local/demo provider
- timeout/error classification
- provider selection telemetry

### D. Content safety / duplicate guard

Create a reusable content pipeline demonstrating:

`candidate -> history/similarity check -> generation -> quality check -> persist`

### E. Human approval gate

Create a small generative-media workflow demonstrating:

`generate -> validate -> human approval -> publish`

### F. Always-on agent

Document a production-minded scheduled agent pattern:

`trigger -> collect -> reason -> act -> state -> notification`

Include retry and idempotency guidance.

## Phase 3 — Production quality

- Add evaluation examples instead of relying only on successful demos.
- Add structured logging examples.
- Add cost/usage accounting examples.
- Add failure and fallback tests.
- Add security guidance for secrets and tool permissions.
- Add reproducible setup instructions.
- Prefer pinned dependencies where appropriate.
- Add CI checks for representative examples.

## Phase 4 — Better developer experience

Every promoted example should answer these questions immediately:

1. What does it do?
2. Why is this pattern useful?
3. What does the architecture look like?
4. Which model/provider is used?
5. What API keys are required?
6. How do I run it?
7. What output should I expect?
8. What happens when the provider fails?
9. What are the security/licensing limitations?
10. How can I adapt it to my own application?

## Priority order

1. Grounded generation
2. Deterministic + AI hybrid decisioning
3. Provider/fallback routing
4. Evaluation and failure handling
5. Human approval gates
6. Always-on/idempotent agents
7. Cost and observability patterns
8. More domain examples

## Success criterion

The repository should not merely contain more AI demos. A developer should be able to discover a pattern, understand the trade-offs, run it locally, and adapt it to a real product in a predictable way.
