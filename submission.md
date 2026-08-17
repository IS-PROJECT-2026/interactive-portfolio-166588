# Project Submission Report

## 1. Student Details

- **Full Name:** Oyieri Jermaine Obed (Otto Oyieri)
- **GitHub Username:** aawbed
- **Email:** jermaineobed.oyieri@strathmore.edu

---

## 2. Deployed Project Link

- **Live GitHub Pages URL:** https://is-project-2026.github.io/interactive-portfolio-166588/

---

## 3. Reflection — Grounded in Your Git History

### A. Your Best Commit

- **Commit URL:** https://github.com/IS-PROJECT-2026/interactive-portfolio-166588/commit/51823f46c20ddbfbece703a1211b05bc2acffc5
- **Why this one?** It's a clean `fix:` commit that resolves a real merge conflict (a delete-vs-edit clash on the project tag styling) with a descriptive subject and a footer noting the exact conflict cause, so the history explains not just what changed but why.

### B. A Mistake or Struggle

- **Link to the evidence:** https://github.com/IS-PROJECT-2026/interactive-portfolio-166588/commit/3fb6a9a2d2f4aca77cf432e15753519b63428fa
- **What happened and how did you recover?** While drafting the README I stashed my changes to pull a fast-forward update to `main`, then popped the stash back — the diff briefly looked corrupted in the terminal (escaped backticks and mangled links) and I worried the stash had damaged the file. After re-checking with `git diff`, I confirmed it was just terminal rendering, not actual corruption, cleaned up the remaining placeholder text, and committed the README properly.

### C. A Pull Request You're Proud Of

- **PR URL:** https://github.com/IS-PROJECT-2026/interactive-portfolio-166588/pull/19
- **What did you check before merging?** I checked that the README accurately described the live deployment link, listed the real technologies used, and that the Markdown rendered correctly (no stray escape characters) before merging into `main`.

### D. One Thing You Would Do Differently

- **What would you change?** I'd configure branch protection with required status checks from the very first commit instead of relying on repo-owner bypass permissions — right now, as the org owner, my pushes to `main` skip the "PR required" rule entirely, which undercuts the enforcement even though I was still following the PR workflow manually.
- **Link to the evidence of the original decision:** https://github.com/IS-PROJECT-2026/interactive-portfolio-166588/commit/7233dbc37c68f2e76c09532e613afefa0858a48

---

## 4. Screenshots of Key GitHub Features

### A. Milestones and Issues

[PASTE YOUR MILESTONE SCREENSHOT DIRECTLY HERE]

* **Caption:** Three milestones track distinct development phases — Foundation & Structure (10/10 issues closed), Content & Interactivity (4/4 closed), and Deployment & Documentation (3/5 closed).

### B. Project Board

[PASTE YOUR PROJECT BOARD SCREENSHOT DIRECTLY HERE]

* **Caption:** The Kanban board shows issues distributed across To Do, In Progress, and Done, reflecting real task progression rather than a static Done-only board.

### C. Branching Architecture

[PASTE YOUR BRANCHING SCREENSHOT DIRECTLY HERE]

* **Caption:** Branch names follow the `feat/`, `fix/`, `docs/`, `style/`, and `conflict/` convention, each tied to an issue number.

### D. Pull Requests & Traceability

[PASTE YOUR PULL REQUEST SCREENSHOT DIRECTLY HERE]

* **Caption:** PR #19 closes issue #9 and is linked to the Deployment & Documentation milestone, demonstrating traceability from issue to merged code.

---

## 5. Merge Conflict Evidence

### Conflict 1 — Full Chronology

**What cause did you use?** Same-line edit — two branches (`conflict/1-main-description` and `conflict/1-main-description-b`) both rewrote the exact same sentence in `README.md`'s About section, but with different wording.

#### Step 1: Generating the Clash

[PASTE SCREENSHOT OF ATTEMPTED MERGE / TERMINAL WARNING HERE]

* **Caption:** Merging `conflict/1-main-description-b` into `main` (which already had `conflict/1-main-description` merged in) produced a same-line conflict on the About section's opening sentence.

#### Step 2: Inside the Code Editor (Conflict Markers)

![Conflict 1 evidence](./evidence/conflict_evidence_1.png)

* **Caption:** Both branches modified the same sentence describing the portfolio; the final resolution merged the intent of both versions into a single clear sentence.

#### Step 3: Resolution & Clean Merge

[PASTE SCREENSHOT OF CLEAN RESOLUTION HERE]

* **Caption:** After removing the conflict markers and combining both edits, the merge was committed (`c392b01`) and pushed cleanly to `main`.

---

### Conflict 2 — Different Cause

**What cause did you use?** Adjacent-line edit — `conflict/2-terminal-help-a` inserted a new line into the terminal `help` command block, while `conflict/2-terminal-help-b` edited the wording of an existing line directly next to the insertion point.

**Why does this cause trigger a conflict?** Git's three-way merge can't cleanly interleave an inserted line with an edit to a neighboring line inside the same hunk, since it can't determine unambiguously how the two changes should be combined — so it flags the whole region for manual resolution.

![Conflict 2 evidence](./evidence/conflict_evidence_2.png)

* **Caption:** Branch A added a new `stack` line to the terminal help output; branch B reworded the adjacent `skills` line — both changes were kept in the final resolution.

---

### Conflict 3 — Different Cause

**What cause did you use?** Delete-vs-edit conflict — `conflict/3-tags-delete` removed the `.card .tags span` CSS block entirely, while `conflict/3-tags-edit` modified the contents of that same block (adding background pill styling).

**Why does this cause trigger a conflict?** One branch's history shows the block being deleted while the other shows it being changed — Git has no way to reconcile "this content no longer exists" with "this content was edited," so it surfaces the conflict rather than guessing which change should win.

![Conflict 3 evidence](./evidence/conflict_evidence_3.png)

* **Caption:** The delete-side branch removed the tag chip styling block while the edit-side branch enhanced it with a background pill; the resolution kept the enhanced version.

---

## 6. Feedback & Evaluation

- [ ] **Anonymous Evaluation Form:** [Course & Instructor Evaluation](https://forms.gle/YLybnsyXXErKEg3s9)

---

## Final Submission

> **Submission Form:** [https://forms.gle/KrT4VxtFtkU3wtYu8](https://forms.gle/KrT4VxtFtkU3wtYu8)