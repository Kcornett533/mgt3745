# DACI-001: Which Problem Does the Team Build?

Commit the Weights section before anyone scores. Weights and scores belong in separate commits; the history is the evidence.

## Roles

| Role | Who |
| :--- | :--- |
| Driver | Kamyaab Cornett |
| Approver | Kenneth Riley II |
| Contributors | Kamyaab Cornett, Kenneth Riley II, Regina Choi, Rishi Ajith |
| Informed | Instructor, Course TAs |

## Options

| Option | Owner | HW1 problem in one line |
| :--- | :--- | :--- |
| A | Regina Choi | Accounting students face career uncertainty and lack methods to demonstrate verifiable skills in an AI-impacted market. |
| B | Kenneth Riley II | High-volume recruiters struggle to verify candidate competencies amidst an influx of unvetted AI-generated resumes. |
| C | Rishi Ajith | Student athletes struggle to coordinate practice schedules around shifting academic conflicts and rest requirements. |
| D | Kamyaab Cornett | Computational workflows lose data provenance across fragmented terminal logs, making analytical outputs hard to audit. |

## Weights (committed before scores)

| Criterion | Weight (1 to 5) | Why this weight |
| :--- | :--- | :--- |
| Still wicked at team scale | 4 | The problem must present genuine structural verification ambiguity, not a trivial CRUD list. |
| Users the team can reach by Oct 22 | 5 | Crucial for Phase 2 validation testing; we must have direct access to students and campus recruiters. |
| Buildable on our stack in three weeks | 5 | Must reliably deploy to Cloudflare Workers + D1 and vanilla JS within the sprint window. |
| Data we can get legally and soon | 4 | Cannot depend on proprietary NDA enterprise ATS databases or restricted financial ledgers. |
| Meaning: at least three of us care | 4 | Team members are all entering AI-impacted quantitative/business job markets. |

## Scores (1 to 5, median of private scores)

| Criterion | Weight | Option A (Regina) | Option B (Kenneth) | Option C (Rishi) | Option D (Kamyaab) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Still wicked at team scale | 4 | 5 (20) | 4 (16) | 3 (12) | 4 (16) |
| Users the team can reach by Oct 22 | 5 | 5 (25) | 4 (20) | 3 (15) | 3 (15) |
| Buildable on our stack in three weeks | 5 | 5 (25) | 5 (25) | 4 (20) | 4 (20) |
| Data we can get legally and soon | 4 | 5 (20) | 4 (16) | 4 (16) | 3 (12) |
| Meaning: at least three of us care | 4 | 5 (20) | 5 (20) | 3 (12) | 4 (16) |
| **Weighted Total** | | **110** | **97** | **75** | **79** |

## Decision

The team selects **Option A (Regina Choi: Accounting Candidate Qualification & Verification Gate)**. It scored highest on user accessibility by October 22, clean buildability on our Cloudflare Worker + D1 stack, and strong team relevance across business and engineering disciplines. Kenneth Riley II, as the designated Approver, approved the decision on October 8, 2026.

## Dissent

Kamyaab noted that accounting and audit standards involve complex regulatory compliance rules that could exceed scope. We mitigated this by bounding intake to four deterministic criteria (degree alignment, graduation timeline, work authorization, and required coursework) rather than building full transaction ledgers.

## What Would Reopen This

- Reopen this decision if the team is unable to recruit at least 3 accounting/business students or recruiters for Phase 2 prototype evaluation by **October 22, 2026**.
- Reopen if Cloudflare D1 storage limits or edge runtime constraints prevent persisting candidate verification records without third-party services.