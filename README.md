# WorkTracker – Manual Testing Project

Manual testing project for **WorkTracker**, a web-based employee work-tracking application. It covers the full QA lifecycle, from test planning and test case design to execution, defect reporting and test closure.



---

## Table of Contents

- [Project Overview](#project-overview)
- [Application Under Test](#application-under-test)
- [Scope](#scope)
- [Test Environment](#test-environment)
- [Testing Approach](#testing-approach)
- [Repository Structure](#repository-structure)
- [Test Execution Summary](#test-execution-summary)
- [Module-wise Coverage](#module-wise-coverage)
- [Defect Summary](#defect-summary)
- [Recommendations](#recommendations)
- [Tools Used](#tools-used)
- [How to Use This Repository](#how-to-use-this-repository)

---

## Project Overview

WorkTracker lets employees clock in and out, apply for leave, view salary and tasks, and share feedback. Admins can manage employees, review attendance and leave, calculate salaries, assign tasks and view feedback.

The objective of this project was to verify that the application meets its functional requirements and that the main user workflows work correctly for both **Employee** and **Admin** roles.

## Application Under Test

| Item | Details |
|---|---|
| Application | WorkTracker |
| Type | Web Application |
| URL | https://employee-worktrack-5lmu.vercel.app |
| User Roles | Employee, Admin |
| Testing Type | Manual Testing |

## Scope

**In scope (frontend, Employee and Admin side)**

Registration · Login · Overview · Employees · Attendance · Leaves · Salary · Tasks · Feedback · Profile · Logout

**Out of scope**

Backend, database, API, performance, security, source code and server-side testing.

## Test Environment

| Item | Details |
|---|---|
| Operating System | Windows 11 |
| Browser | Google Chrome |
| Network | Wi-Fi |
| Test Data | Valid and invalid data, multiple test accounts |

## Testing Approach

The following types of testing were planned:

- Functional Testing
- UI Testing
- Smoke Testing
- Integration Testing
- System Testing
- Regression Testing
- Retesting

Both **positive** and **negative** test cases were written for each module.

## Repository Structure

```
WorkTracker Manual Project/
├── WorkTracker-TestPlan.pdf                  # Test strategy, scope, schedule, risks
├── WorkTracker_TestScenario.xlsx             # High-level test scenarios with test case counts
├── WorkTracker-Testcase.xlsx                 # Detailed test cases (one sheet per module)
├── WorkTracker-RTM.xlsx                      # Requirement Traceability Matrix
├── WorkTracker-TestExecution - Report.xlsx   # Execution results (one sheet per module)
├── WorkTracker Defect-Report.xlsx            # Detailed defect log
├── Defect Screenshot.docx                    # Screenshot evidence for the defect
├── WorkTracker-DefectSummary.xlsx            # Defect metrics and summary
├── WorkTrackerTestSummaryReport.pdf          # Test summary report
└── WorkTracker TestClosure.pdf               # Test closure report
```

## Test Execution Summary

| Metric | Result |
|---|---|
| Total Test Cases | 179 |
| Executed | 179 |
| Passed | 178 |
| Failed | 1 |
| Blocked | 0 |
| Not Executed | 0 |
| Execution Percentage | 100% |
| Pass Percentage | 99.44% |
| Fail Percentage | 0.56% |
| Defects Identified | 1 |

## Module-wise Coverage

| Module | Test Cases | Passed | Failed |
|---|:---:|:---:|:---:|
| Register | 14 | 14 | 0 |
| Login | 8 | 8 | 0 |
| Overview | 21 | 21 | 0 |
| Employees | 8 | 8 | 0 |
| Attendance | 18 | 18 | 0 |
| Leave | 23 | 22 | 1 |
| Salary | 22 | 22 | 0 |
| Tasks | 22 | 22 | 0 |
| Feedback | 19 | 19 | 0 |
| Profile | 22 | 22 | 0 |
| Logout | 2 | 2 | 0 |
| **Total** | **179** | **178** | **1** |

Test case ID prefixes: `REG`, `LOG`, `OVR`, `EMP`, `ATT`, `LVE`, `SAL`, `TSK`, `FDB`, `PRF`/`PRE`, `LOU`.

## Defect Summary

| Severity | Count |
|---|:---:|
| Critical | 0 |
| High | 1 |
| Medium | 0 |
| Low | 0 |

| Field | Details |
|---|---|
| Defect ID | DEFECT_001 |
| Title | End Date earlier than Start Date is accepted in Leave Request |
| Related Test Case | TC_LVE_010 |
| Module | Leave |
| Severity / Priority | High / High |
| Status | **Open** |

**Steps to reproduce**
1. Select *Sick Leave* as the leave type.
2. Enter a Start Date and an End Date that is one day before the Start Date (e.g., Start Date: 06-10-2026, End Date: 05-10-2026).
3. Enter the reason *Not Feeling Well*.
4. Click **Submit Leave Request**.

**Expected result:** A "Please fill valid date" validation message is displayed.  
**Actual result:** The leave request is submitted successfully.

The defect was reported to the development team and remained unresolved at the time of test closure.

## Recommendations

Possible enhancements for future releases:

- **Task management:** priorities, deadlines and reminders
- **Dashboards and reporting:** detailed progress and productivity reports
- **User interface:** better responsive design for desktop, tablet and mobile
- **Time tracking:** additional options for recording working hours
- **Notifications:** alerts for task assignments, deadlines and status changes

## Tools Used

| Purpose | Tool |
|---|---|
| Test case management | Microsoft Excel |
| Defect tracking | Microsoft Excel |
| Documentation | Microsoft Word |
| Screenshots | Snipping Tool |
| Browser | Google Chrome |

## How to Use This Repository

1. Start with the **Test Plan** to understand the scope and strategy.
2. Review the **Test Scenarios** and **Test Cases** to see what was tested.
3. Check the **RTM** to trace each requirement to its test cases.
4. Open the **Test Execution Report** for the pass/fail result of every test case.
5. See the **Defect Report**, **Defect Screenshot** and **Defect Summary** for the open defect.
6. Read the **Test Summary Report** and **Test Closure Report** for the final outcome.

---

**Prepared by:** QA Tester
