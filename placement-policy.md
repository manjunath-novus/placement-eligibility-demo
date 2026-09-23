# Placement Eligibility Checker — Synthetic Demo Policy

> **Important:** This is synthetic demo data created for a Microsoft Agent-a-thon project. It is not a real college placement policy and must not be treated as actual placement eligibility rules.

## Purpose
Use this policy together with the synthetic placement-drive announcements to evaluate a student's eligibility.

## Student profile fields
The student profile may include:
- Branch
- Current CGPA
- Active backlogs
- 10th percentage
- 12th percentage
- Graduation year
- Academic gap after 12th/diploma
- Academic gap during degree
- Previous campus offer
- Any other field explicitly required by a drive

## Interpretation rules
- A requirement written as "minimum X" or "X+" is inclusive. Meeting exactly X satisfies the requirement.
- "No active backlog" means active backlogs must equal 0.
- "Maximum N active backlogs" means active backlogs must be less than or equal to N.
- A branch requirement must match one of the branches explicitly listed in the drive announcement.
- Previous campus offer, gap-year, and similar conditions apply only when the specific drive explicitly states them.
- Do not invent or assume a criterion that is not present in the drive announcement.

## Missing information
- If a drive requires a student field that has not been provided, return **Need more info**.
- Name the exact missing field.
- Do not guess missing values.

## Verdict definitions
Use exactly one of:
- **Eligible** — all stated criteria are satisfied.
- **Not eligible** — at least one stated criterion is not satisfied.
- **Need more info** — a required field is missing.

## Evidence rule
Use only the synthetic placement-drive announcements and this synthetic policy. Do not use outside knowledge about companies or real-world hiring criteria.

## Demo disclosure
All companies, deadlines, requirements, and document lists in the accompanying drive dataset are fictional/synthetic and are intended only for demonstration.
