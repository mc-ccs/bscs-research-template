# Validation Plan

This section presents the plan for evaluating whether the developed system meets its intended objectives, functional requirements, and quality targets. The validation plan should show how the proponents will gather evidence that the system is correct, usable, reliable, and appropriate for the identified users.

## Validation Objectives

The validation activities should confirm the following:

- The system features work according to the stated requirements
- The generated outputs are correct and consistent
- The system is usable by the intended users
- The application performs acceptably under normal operating conditions
- Defects discovered during testing are documented and resolved before final demonstration

## Validation Approach

The standard validation strategy combines technical testing and user-centered evaluation. Teams should treat the sections below as the default validation structure unless an approved exception has been documented.

### 1. Functional Validation

Functional validation verifies that each feature behaves as expected. This may include:

- Account login and role-based access
- Data encoding and editing
- Search, filtering, and retrieval
- Report generation
- Export or print functions
- Notifications and workflow transitions

For each feature, define the test input, expected behavior, actual result, and status of the test case.

### 2. Usability Evaluation

Usability evaluation measures whether the target users can effectively use the system. A common approach is to ask representative users to perform tasks in the system and then answer a structured questionnaire, such as the System Usability Scale (SUS), a Likert-scale instrument, or a school-approved evaluation form.

For user-facing systems, this section should identify the actual user-validation instrument that will be used. If SUS or SEQ will not be used, the approved alternative should be stated explicitly.

The final manuscript should state:

- The number of respondents
- The profile of respondents
- The evaluation instrument used
- The scoring interpretation
- The resulting usability score or rating

### 3. Performance and Reliability Checks

If the project includes measurable performance, reliability, accuracy, or repeatability concerns, include the relevant technical checks here.

- Response time during common transactions
- Accuracy of generated results
- Successful handling of repeated requests
- Stability during continuous use
- Proper data saving and retrieval

These checks do not need to be industrial-scale performance tests, but they should be sufficient to show that the prototype works reliably under the study's intended scope.

### 4. Security and Data Integrity Checks

For projects that store user information or sensitive records, validation should also verify that:

- Unauthorized users cannot access restricted modules
- Input validation prevents invalid or unsafe entries
- User actions are restricted based on role
- Stored data remains consistent after create, update, and delete operations

## Standard Validation Matrix

The table below should be completed and tailored when preparing the final validation evidence.

| Validation Area | Method | Participants / Basis | Expected Outcome |
| --- | --- | --- | --- |
| Functional correctness | Test cases | Developers / proponents | All critical features pass |
| Usability | Survey or evaluation form | Target users | Acceptable usability score |
| Accuracy of outputs | Result comparison | Manual checking or baseline rules | Outputs match expected results |
| Reliability | Repeated execution | Proponents | Stable behavior across repeated runs |
| Security / access control | Role-based tests | Proponents / admin tester | Unauthorized access is blocked |

## Acceptance Criteria

The study should define clear criteria for considering the system acceptable. At minimum, the acceptance criteria should include the following:

- All core features pass functional testing
- No critical defects remain unresolved before final defense
- User evaluation results meet the minimum acceptable score required by the institution
- The system produces correct outputs for the defined test cases
- The deployed prototype can be demonstrated successfully from start to finish

## Documentation of Results

All validation evidence should be summarized in Chapter 4. Supporting materials may be placed in the appendices, such as:

- Test case tables
- Evaluation forms
- Survey summaries
- Screenshots of outputs
- Error logs or bug-fix summaries

## Final Customization Notes

Before final submission, tailor this validation plan to the actual research project by specifying:

- The exact testing instruments used
- The exact number and type of evaluators
- The scoring or interpretation method
- The success thresholds approved by the adviser or research manual
- Any additional validation required by the study, such as model accuracy, expert review, or comparative analysis


---
[⬅️ Previous](f-logic-flow.md) | [Next ➡️](../05-chapter-4-results/a-scrum-execution.md)
