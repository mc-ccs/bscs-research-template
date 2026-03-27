# Definition of Done

This section should define the minimum conditions that a backlog item must satisfy before the team reports it as complete during a sprint review.

Use the institutional baseline below, then add project-specific quality checks when needed.

## Institutional Minimum Definition of Done

A backlog item should normally be counted as complete only when:

- the work has been committed to the correct repository
- a pull request has been created and reviewed according to the approved workflow
- the related acceptance criteria have been satisfied
- relevant testing or verification has been completed successfully
- CI checks pass when applicable
- related documentation has been updated
- evidence is available for the next sprint review

## Project-Specific Additions

The team may extend the Definition of Done with additional requirements such as:

- code review by a domain specialist or designated lead
- updated diagrams, screenshots, or release notes
- security checks for sensitive modules
- dataset verification or model evaluation for analytics projects
- deployment verification for hosted systems

## Recommended Table Format

| DoD Item | Required for All Stories | Notes |
| --- | --- | --- |
| Work committed to repository | Yes | Identify the branch or pull request pattern used by the team. |
| Pull request reviewed | Yes | Reference `CODEOWNERS` or the agreed review rule. |
| Acceptance criteria satisfied | Yes | Link to the user story, issue, or checklist. |
| Testing completed | Yes | State the type of testing expected for the story. |
| CI checks passed when applicable | Yes | Use `N/A` only with justification. |
| Documentation updated | Yes | Include manuscript, README, or appendix updates when relevant. |
| Extra project-specific condition | No | Add rows as needed. |

## Writing Reminder

This section should describe the **actual quality gate** used by the team, not a generic definition copied from Scrum references.


---
[⬅️ Previous](c-sprint-structure.md) | [Next ➡️](e-system-architecture.md)
