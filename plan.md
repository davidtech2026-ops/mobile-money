# Wave Program Sprint Plan: Mobile Money

## Overview
The Wave Program accelerates the Mobile Money platform by breaking roadmap milestones into well-scoped, bite-sized sprint issues. We structure tasks across distinct technical tracks to welcome both first-time contributors and seasoned blockchain/backend engineers.

---

## Issue Categories & Scoped Work

### 1. Bug Fixes & Hardening (Low–Medium Complexity)
* **Ingest & Reconciliation**: Fix edge-case event drops during Soroban RPC lag or blockchain re-orgs in `ingest-go` and `ingest-node`.
* **State Machine Inconsistencies**: Resolve transaction status desyncs between local database caches and on-chain payment states.
* **Error Propagation**: Standardize RFC-7807 problem details across API endpoints and CLI error messages.

### 2. Feature Enhancements & Adapters (Medium–High Complexity)
* **MNO Connector Extensions**: Add new Mobile Network Operator payment rail mock adapters (e.g., M-Pesa, Orange Money, MTN MoMo).
* **Soroban Contract Capabilities**: Extend escrow and vault contracts in `contracts/` with batched payouts, timelock cancellations, and token allowlists.
* **SDK Feature Parity**: Implement missing multi-currency conversion helpers and signature verification utils across TypeScript and Kotlin SDKs.

### 3. Testing, Quality & Security (Medium Complexity)
* **Contract & Pact Testing**: Expand consumer-driven contract tests (`pacts/`) for third-party MNO callbacks.
* **Mutation & Coverage**: Boost Stryker mutation testing scores in core transfer workers and Soroban contract validation suites.
* **E2E & Load Testing**: Add Playwright test flows for the Developer Portal and k6 load scenarios benchmarking ingestion throughput.

### 4. Documentation & Developer Experience (DX) (Low–Medium Complexity)
* **Cookbooks & Tutorials**: Create end-to-end integration guides (e.g., "Accepting MoMo payments via Soroban") for the developer portal.
* **Interactive References**: Update OpenAPI specs, Postman collections, and add runnable code samples in `examples/`.
* **Onboarding & Local Setup**: Streamline `docker-compose.dev.yml` workflows and improve contribution setup guides.

---

## Issue Scoping & Sprint Workflow

Every sprint issue follows a standardized template:
1. **Context & User Story**: Why this change is needed and who benefits.
2. **Acceptance Criteria**: Clear, unambiguous checklists verifying success.
3. **Pointers & Files**: Direct links to target directories (e.g., `src/`, `contracts/`, `sdk/`).
4. **Testing Requirements**: Minimum unit/integration tests expected.

### Labeling Taxonomy
* **Type**: `bug`, `feature`, `documentation`, `testing`
* **Scope**: `good-first-issue`, `help-wanted`, `contracts`, `sdk`, `backend`
* **Effort**: `size:S` (1–2 days), `size:M` (3–5 days), `size:L` (1 sprint)

Maintainers provide review feedback within **48 hours** to ensure contributors maintain momentum through the sprint cycle.
