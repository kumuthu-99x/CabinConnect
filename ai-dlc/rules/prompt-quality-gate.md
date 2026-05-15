# Prompt Quality Gate

Before accepting any AI-generated output, run it through the four-component check below.
If any component fails, revise the prompt or the output before merging.

---

## The Four-Component Check

### 1. Context
> Did the prompt give the AI enough context to produce a correct answer?

- [ ] Relevant domain terms were defined or linked to the glossary
- [ ] The affected files, modules, or services were named explicitly
- [ ] Constraints (security rules, architecture decisions) were referenced
- [ ] No ambiguous pronouns or vague scope ("the thing", "the service")

### 2. Instruction
> Was the task stated clearly and unambiguously?

- [ ] Single, well-scoped task (not "do everything related to bookings")
- [ ] Expected output format was specified (code, list, diagram, prose)
- [ ] Negative constraints were stated ("do not modify the auth flow")
- [ ] Edge cases or known failure modes were called out

### 3. Output Evaluation
> Does the output actually solve the stated problem?

- [ ] Code compiles and passes linting without modification
- [ ] Logic matches the acceptance criteria or requirement
- [ ] No hallucinated APIs, libraries, or method names
- [ ] Security rules from `security.md` are not violated
- [ ] No unnecessary scope creep (extra features, refactors not asked for)

### 4. Risk Assessment
> What breaks if this output is wrong?

- [ ] Impact surface identified (which users, which flows)
- [ ] Reversibility assessed (can this be rolled back easily?)
- [ ] Tests exist or were generated alongside the output
- [ ] A human reviewer has read the diff — not just "it looks right"

---

## Gate Result
| Component | Pass | Fail | Notes |
|-----------|------|------|-------|
| Context | | | |
| Instruction | | | |
| Output | | | |
| Risk | | | |

**Do not merge if any row is Fail.**
