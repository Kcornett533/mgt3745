# PROBE-001: bolt.new Specification Probe

| | |
|---|---|
| Date | 2026-10-08 |
| Accountable | Kenneth Riley II |
| Responsible | bolt.new (one prompt, no follow-ups) |
| Input | context/FEATURES.md as of commit 0d0f20c, nothing else |
| Delegation record | docs/DDR-001.md |
| Code kept | None |

## What bolt Had to Guess

| # | What bolt assumed | Why it had to guess | Change to FEATURES.md |
|---|---|---|---|
| 1 | Created a tri-state qualification tier: "Conditionally Eligible" in addition to "Eligible" and "Ineligible". | FEATURES.md F-01 defined binary badge assignment but did not explicitly prohibit indeterminate middle states for partial coursework submissions. | Added explicit EARS statement to F-01 confirming evaluation status is strictly binary (`Eligible` or `Ineligible`) with no conditional staging. |
| 2 | Added an administrative landing page with multi-route navigation ("Apply Now" vs. "Recruiter Portal") and marketing feature cards. | FEATURES.md specified triage and intake behavior without prescribing client-side page layout or routing architecture. | Added explicit entry under `## Exclusions` stating multi-page marketing routes and public informational landing pages are out of scope. |
| 3 | Provisioned proprietary Bolt Cloud Database with Row Level Security (RLS) policies. | FEATURES.md F-03 stated relational persistence requirements without forbidding third-party managed database platforms. | Added explicit EARS statement to F-03 restricting persistence strictly to edge-native Cloudflare D1 bound via `env.DB`. |
| 4 | Implemented interactive candidate record mutation controls (recruiter status dropdown overwrite, notes saving, and record deletion). | FEATURES.md F-04 described recruiter search and triage filtering but did not define record mutability or deletion constraints. | Added explicit entry under `## Exclusions` forbidding candidate record deletion or manual post-submission status mutation to preserve audit trails. |
| 5 | Added applicant institution/university and general contact info inputs to the intake form schema. | FEATURES.md F-01 and F-02 specified degree alignment, timeline, and work authorization without defining non-qualifying identity attributes. | Added explicit EARS boundary in F-02 stating intake schema is strictly limited to candidate name, accredited degree, graduation year, work authorization, and artifact URL. |