# EVALS.md

Stub from mgt3745-group-template. Accountable: Regina Choi (Reviewer)

## Opportunity Solution Tree

```mermaid
flowchart TD
    O["Outcome: Help accounting and finance students demonstrate entry-level audit readiness through verifiable evidence"]

    O --> P1["Opportunity 1: Students lack clarity about the skills employers expect"]
    O --> P2["Opportunity 2: Students struggle to demonstrate skills beyond coursework and self-reported claims"]
    O --> P3["Opportunity 3: Recruiters need to verify qualifications efficiently"]

    P1 --> S1["Solution: Provide a clear list of role-related requirements"]
    P2 --> S2["Solution: Let students submit coursework and project evidence"]
    P3 --> S3["Solution: Provide transparent eligibility checks and filtering"]

    S1 --> A1["Test: Ask accounting students whether the requirements are clear and useful"]
    S2 --> A2["Test: Ask students and recruiters whether submitted evidence helps demonstrate readiness"]
    S3 --> A3["Test: Ask recruiters whether the proposed checks match actual screening needs"]
```

## Riskiest Assumption (RAT)

**Assumption:** Accounting students and recruiters will find it useful to evaluate accounting skills using actual coursework and project evidence.

**Why it is risky:** Students may not have enough practical experience to provide this evidence, and recruiters may prefer their existing screening methods. Our interviews support parts of the problem, but they do not prove that users would use our proposed tool.

**Test:** Interview accounting students or recent graduates and recruiters about how they currently prepare for or evaluate entry-level accounting applications. Ask them to review the proposed requirements and explain whether the evidence would help them.

**Evidence to collect:** Examples of evidence students can provide, how recruiters currently check qualifications, and specific feedback about the proposed tool.

**Decision rule:** Continue with the proposed solution if interviews provide concrete evidence that the problem exists and the proposed checks address it. Otherwise, revise the problem or solution before committing to implementation.


## Evals Planned for Phase 2

### Evaluation 1: Requirement Clarity

* **Question:** Can accounting students understand the role requirements and identify what they need to demonstrate?
* **Method:** Ask students or recent graduates to review the proposed requirements and explain them in their own words.
* **Evidence:** Record misunderstandings, questions, and whether participants can identify relevant next steps.

### Evaluation 2: Evidence Submission

* **Question:** Can a student identify relevant coursework or project evidence and associate it with the appropriate skill or requirement?
* **Method:** Ask a participant to complete a representative evidence-submission task using the prototype.
* **Evidence:** Record task completion, errors, confusion, and feedback.

### Evaluation 3: Verification and Screening

* **Question:** Can a recruiter understand the eligibility result and identify which requirements a candidate meets or does not meet?
* **Method:** Ask a recruiter or a suitable proxy to evaluate example candidate profiles using the proposed checks.
* **Evidence:** Record incorrect interpretations, missing information, and whether the results are understandable.

### Evaluation 4: User Value

* **Question:** Does the proposed tool address a problem that students or recruiters actually experience?
* **Method:** Compare prototype feedback with examples from participant interviews about their existing preparation or screening process.
* **Evidence:** Record supporting evidence, contradictory evidence, and changes needed to the proposed solution.

## Prediction Stakes

### Prediction Stake: Regina Choi

**Prediction:** I predict that accounting students and recent graduates will find a clear list of role-related requirements useful, but some will struggle to identify strong evidence of their skills when they have limited internship or practical experience.

**Reasoning:** The team's research includes an interview with a 2025 accounting graduate who struggled to identify the skills employers expected and lacked internship evidence to point to. However, one interview does not establish how common this experience is.

**What would support my prediction:** During Phase 2 evaluation, participants identify the requirements as useful but have difficulty connecting their coursework or projects to the evidence requested.

**What would contradict my prediction:** Participants consistently identify appropriate evidence without difficulty, or they do not find the requirements useful.

**When to check:** During Phase 2, after the team tests the relevant prototype with intended users.

### Prediction Stake: Kamyaab Cornett (Implementer)

- **Prediction:** I predict that our team will maintain 100% compliance with our pull request and review rules with zero direct commits to `main` during Phase 2. Enforcing our DOM safety rules and database input checks during code reviews will catch and fix at least two data formatting or payload bugs before any code is merged.
- 
- **Reasoning:** In HW5 and individual projects, unvalidated inputs and direct branch edits caused silent UI breakages and database errors. Having strict branch protection, CODEOWNERS enforcement, and clear review standards creates a reliable filter before code reaches production.
- 
- **What would support my prediction:** Review logs on pull requests show identified input/formatting issues that were corrected before merging, and zero direct commits appear on `main`.
- 
- **What would contradict my prediction:** Unvetted code bypasses PR review into `main`, or input validation errors slip through into production without being caught during review.
- 
- **When to check:** At the conclusion of Phase 2, by inspecting the repository's git commit history, pull request review logs, and database error traces.

## Where the Stakes Disagree
