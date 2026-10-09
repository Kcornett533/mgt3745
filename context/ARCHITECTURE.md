# ARCHITECTURE.md

Stub from mgt3745-group-template. Accountable: the Architect.

## The Gate: Build, Buy, or Delegate

### Weights (commit before scores)
| Criterion | Weight | Reason |
| Cost to start | 4 | Keep the course prototype within a 0 dollar budget. |
| Cost to maintain | 3 | Keep ongoing costs and upkeep manageable for the team. | 
| Time to working | 4 | Build and verify the prototype within 3 weeks. |
| Inspectability | 5 | Teammates must understand eligibility rules, validation, and data access. |
| Switching cost | 4 | HW4 required schema and client changes; HW5 showed substantial delegation review effort. |
| Fit to specification | 5 | Support candidate intake, validation, persistence, filtering, and artifact records. |

### Scoring anchors
Higher scores are better. Scores 2 and 4 fall between these anchors.

| Criterion | 1 means | 3 means | 5 means |
| Cost to start | Payment required | Free with substantial setup | Free with minimal setup |
| Cost to maintain | High recurring cost or upkeep | Manageable upkeep | Little upkeep and no expected cost at prototype scale |
| Time to working | Exceeds 3 weeks | Fits with significant integration work | Quickly testable with familiar components |
| Inspectability | Core behavior can't be inspected | Team can explain some components | Team can inspect and explain rules, schema, and data access |
| Switching cost | Major rewrite and difficult data recovery | Export plus integration changes | Portable data with limited integration changes |
| Fit to specification | Essential requirements unmet | Most requirements met with workarounds | All required behavior supported |

### Scores
**Decision:** How should the team implement candidate intake, eligibility checks, validation, persistent records, filtering, and artifact links?
**Build:** Team-written HTML/CSS/Javascript frontend with a Cloudflare Worker API and D1 database. The team owns validation, eligibility rules, and data-access logic.
**Buy:** Use an existing hosted service such as Airtable, with forms, stored candidate records, filtered views, and configured eligibility formulas. Evaluate whether its available plan supports the required behavior and access controls.
**Delegate:** Have bolt.new generate the frontend and Cloudflare Worker/D1 integration from the team specification. The team inspects, tests, and maintains the output; AI never approves or merges it. PROJECT.md and FEATURES.md propose Cloudflare D1. The Gate evaluates that proposal; choosing another option would require coordinated updates to those files.

### Weighted scores
Scores are planning estimates, not test results. Each cell shows the score followed by its weighted value in parentheses.
| Criterion | Weight | Build | Buy | Delegate |
| Cost to start | 4 | 5 (20) | 3 (12) | 4 (16) |
| Cost to maintain | 3 | 4 (12) | 4 (12) | 3 (9) |
| Time to working | 4 | 4 (16) | 3 (12) | 3 (12) |
| Inspectability | 5 | 5 (25) | 3 (15) | 3 (15) |
| Switching cost | 4 | 4 (16) | 3 (12) | 3 (12) |
| Fit to specification | 5 | 5 (25) | 2 (10) | 4 (20) |
| **Weighted total** | | **114** | **73** | **84** |
### Score rationale and switching costs

**Build:** Rishi and Regina have already deployed Cloudflare Workers with D1 in HW4. This supports a time-to-working score of 4, although binding, CORS, and deployment troubleshooting still take time. Inspectability scores 5 because the team can review its own rules, schema, and API code. Fit scores 5 for the planned design, not the existing prototype: the team must still implement and verify the required behavior and access controls.
**Buy:** A hosted form-and-table service could support basic intake, records, and filtering. Fit scores 2 because the current specification explicitly requires Worker/D1 integration and particular API responses. Selecting Buy would require coordinated specification changes or additional custom code. Plan limits and access controls remain unverified; these scores are provisional.
**Delegate:** Regina's HW5 Bolt output preserved Worker/D1 and introduced no new dependencies, supporting a fit score of 4. However, her DDR reports 0.25 hours for generation and 5 hours for review/fixes, compared with 2.7 hours estimated for a manual build. Time-to-working therefore scores 3: generating code quickly does not establish verified delivery.
**Switching costs:** Rishi's HW4 move from localStorage to D1 required a schema, deployment configuration, and client fetch integration. His HW5 Bolt output used React/Vite and Supabase, illustrating how delegation can introduce a different stack. Regina's output preserved her stack, but still required extensive review. Build scores 4 because the team controls its schema and code, while leaving Cloudflare would still require data migration and integration changes. Buy and Delegate score 3 because exports, configuration, or generated dependencies may require additional migration work.
**Sensitivity check:** Reducing inspectability weight from 5 to 2 produces totals of Build 99, Buy 64, and Delegate 75. Build remains first.
**Recommendation:** Build, subject to team review and approval.
## ADR-001: <decision>

- **Status:**
### Context
### Options
### Decision
### Consequences
### Revisit Trigger

## Architecture Diagram

```mermaid
flowchart LR
    A["<component>"] --> B["<component>"]
```
