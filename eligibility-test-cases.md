# Eligibility Policy Test Cases

> These examples use the synthetic policy and drive data in this repository. They are test scenarios, not real placement criteria.

Use these cases to check that an eligibility evaluator applies the policy consistently.

| Case | Input / condition | Expected verdict | Reason |
|---|---|---|---|
| Minimum CGPA boundary | Student CGPA exactly matches a drive's minimum | Eligible, if every other criterion is met | Minimum thresholds are inclusive |
| Below minimum CGPA | Student CGPA is below the stated minimum | Not eligible | A required threshold is not met |
| No active backlogs | Drive says "no active backlog" and student has 0 | Eligible, if every other criterion is met | Zero satisfies the requirement |
| Active backlog present | Drive says "no active backlog" and student has 1 | Not eligible | The zero-backlog requirement is not met |
| Maximum backlog boundary | Drive allows maximum 1 active backlog and student has 1 | Eligible, if every other criterion is met | Maximum limits are inclusive |
| Maximum backlog exceeded | Drive allows maximum 1 active backlog and student has 2 | Not eligible | The allowed maximum is exceeded |
| Branch not listed | Student's branch is not among the explicitly eligible branches | Not eligible | Branch must match a listed branch |
| Missing required field | Drive requires a field that the student profile does not provide | Need more info | The evaluator must not guess missing values |
| Unstated criterion | A drive does not mention a condition such as prior campus offer | Do not reject on that condition | Do not invent criteria |
| Optional extra field absent | A drive does not require a profile field and it is missing | Evaluate other stated criteria | Only required missing fields trigger Need more info |

## Suggested evaluator checks

- Apply every stated drive criterion; do not stop after finding a passing criterion.
- Treat "minimum X" and "X+" as inclusive.
- Treat "maximum N" as less than or equal to N.
- Return exactly one verdict: **Eligible**, **Not eligible**, or **Need more info**.
- When returning **Need more info**, name the exact missing field.
- Keep the synthetic-data disclaimer visible when presenting results.

## Source of truth

These test cases are derived from [placement-policy.md](./placement-policy.md) and should be updated whenever that policy changes.
