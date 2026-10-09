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
