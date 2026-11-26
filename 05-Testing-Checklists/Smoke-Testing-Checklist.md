
# Smoke Testing Checklist – SauceDemo

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | SauceDemo |
| Document Type | Smoke Testing Checklist |
| Document ID | SMK-DOC-001 |
| Version | 1.0 |
| Prepared By | Vishal Sharma |
| Testing Type | Manual Smoke Testing |
| Environment | Public Demo |
| Application URL | https://www.saucedemo.com/ |
| Execution Status | Pending |

## 2. Objective

The objective of smoke testing is to verify
that the critical application functionality
is working and the application is suitable
for further detailed testing.

## 3. Reference Documents

- [BRD](../01-Requirements/BRD.md)
- [FRD](../01-Requirements/FRD.md)
- [SRS](../01-Requirements/SRS.md)
- [Test Plan](../02-Test-Planning/Test-Plan.md)
- [Test Strategy](../02-Test-Planning/Test-Strategy.md)
- [Test Scenarios](../03-Test-Design/Test-Scenarios.md)
- [Test Cases](../03-Test-Design/SauceDemo_Test_Cases.xlsx)
- [RTM](../03-Test-Design/SauceDemo_RTM.xlsx)

## 4. Test Environment

| Component | Details |
|---|---|
| Operating System | Windows |
| Browser | Google Chrome |
| Browser Version | To be recorded |
| Application Environment | Public Demo |
| Execution Date | Pending |
| Executed By | Vishal Sharma |

## 5. Preconditions

- Application URL is accessible.
- Internet connection is available.
- Supported browser is available.
- Valid demo credentials are available.
- Required test data is prepared.
- Application state is reset where required.

## 6. Test Data

| Field | Value |
|---|---|
| Username | standard_user |
| Password | secret_sauce |
| Invalid Password | invalid_password |
| First Name | Test |
| Last Name | User |
| Postal Code | 12345 |

Only public demo credentials and synthetic
customer information will be used.

## 7. Smoke Testing Checklist

| Smoke ID | Module | Checklist Item | Scenario ID | Expected Result | Priority | Status |
|---|---|---|---|---|---|---|
| SMK-001 | Application | Open application URL | TS-001 | Login page loads successfully | High | Not Executed |
| SMK-002 | Login | Verify login fields and button | TS-001 | Required login controls are visible | High | Not Executed |
| SMK-003 | Login | Login with valid credentials | TS-002 | User logs in successfully | High | Not Executed |
| SMK-004 | Login | Login with invalid password | TS-004 | Access is denied and error appears | High | Not Executed |
| SMK-005 | Login | Submit empty login fields | TS-007 | Mandatory field validation appears | High | Not Executed |
| SMK-006 | Authentication | Verify successful login redirection | TS-009 | User reaches product listing | High | Not Executed |
| SMK-007 | Products | Verify product listing | TS-016 | Products are displayed | High | Not Executed |
| SMK-008 | Products | Verify product information | TS-017, TS-020 | Product names and prices are visible | High | Not Executed |
| SMK-009 | Products | Open product details | TS-033 | Selected product details appear | High | Not Executed |
| SMK-010 | Products | Sort products by price | TS-028 | Products appear in ascending price order | Medium | Not Executed |
| SMK-011 | Cart | Add product to cart | TS-039 | Selected product is added | High | Not Executed |
| SMK-012 | Cart | Verify cart count | TS-041 | Cart count updates correctly | High | Not Executed |
| SMK-013 | Cart | Open shopping cart | TS-042 | Selected products are displayed | High | Not Executed |
| SMK-014 | Cart | Remove product from cart | TS-046 | Selected product is removed | High | Not Executed |
| SMK-015 | Cart | Verify Continue Shopping | TS-050 | User returns to product listing | Medium | Not Executed |
| SMK-016 | Checkout | Initiate checkout with selected product | TS-052 | Checkout information page opens | High | Not Executed |
| SMK-017 | Checkout | Submit empty mandatory field | TS-058 | Validation error appears | High | Not Executed |
| SMK-018 | Checkout | Enter valid customer information | TS-057 | User can proceed to order summary | High | Not Executed |
| SMK-019 | Order Summary | Verify selected products | TS-071 | Correct products are displayed | High | Not Executed |
| SMK-020 | Order Summary | Verify subtotal | TS-073 | Subtotal matches selected product price | High | Not Executed |
| SMK-021 | Order Summary | Verify total calculation | TS-076 | Total equals subtotal plus displayed tax | High | Not Executed |
| SMK-022 | Order Summary | Click Finish | TS-077 | Simulated order completes successfully | High | Not Executed |
| SMK-023 | Confirmation | Verify confirmation message | TS-082 | Successful order message appears | High | Not Executed |
| SMK-024 | Confirmation | Verify Back Home functionality | TS-083 | User returns to product listing | Medium | Not Executed |
| SMK-025 | Cart | Verify cart after order completion | TS-084 | Purchased items are cleared | High | Not Executed |
| SMK-026 | Navigation | Open and close application menu | TS-087, TS-088 | Menu opens and closes correctly | Medium | Not Executed |
| SMK-027 | Logout | Logout from application | TS-092, TS-093 | User returns to login page | High | Not Executed |
| SMK-028 | Session | Access protected page after logout | TS-094 | Unauthorized access is denied | High | Not Executed |
| SMK-029 | E2E | Complete single-product purchase | TS-117 | Complete purchase workflow succeeds | High | Not Executed |
| SMK-030 | UI/UX | Verify critical buttons and controls | TS-101 | Critical controls are visible and functional | High | Not Executed |

## 8. Execution Guidelines

- Execute critical smoke checks before
  detailed functional testing.
- Reset application state between independent
  test checks where required.
- Add a product again before checkout if
  the cart was emptied during removal testing.
- Record actual results in the Test Cases sheet.
- Capture evidence for failed checks.
- Report reproducible defects in the Bug Tracker.
- Update the associated requirement mapping.
- Record blocked checks separately.
- Do not mark unexecuted checks as Pass.

## 9. Smoke Testing Status

| Status | Description |
|---|---|
| Pass | Actual result matches expected result |
| Fail | Actual result does not match expected result |
| Blocked | Testing cannot proceed due to a dependency |
| Not Executed | Checklist item has not been executed |
| Not Applicable | Checklist item does not apply |

## 10. Smoke Testing Summary

| Metric | Count |
|---|---:|
| Total Smoke Checks | 30 |
| High Priority | 26 |
| Medium Priority | 4 |
| Executed | 0 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Executed | 30 |
| Pass Percentage | N/A |
| Identified Defects | 0 |

Pass Percentage = Passed / Executed x 100

Executed = Passed + Failed

Actual metrics will be updated after execution.

Zero identified defects does not indicate
that the application is defect-free.

## 11. Smoke Testing Acceptance Criteria

- Application is accessible.
- Valid user login is successful.
- Product listing is available.
- Shopping cart functionality is working.
- Checkout workflow is accessible.
- Order calculation is correct.
- Simulated order completion is successful.
- Logout functionality is working.
- No unresolved critical blocker prevents
  further detailed testing.

## 12. Smoke Testing Decision

| Decision | Description |
|---|---|
| Proceed | Critical smoke checks pass |
| Conditional Proceed | Minor failures exist but unaffected testing can continue |
| Hold | Critical functionality fails or testing is blocked |
| Pending | Smoke testing has not been completed |

Current Decision: Pending

## 13. Blocker Management

If critical smoke testing fails:

1. Record the failed checklist item.
2. Capture actual application behavior.
3. Collect supporting evidence.
4. Report the defect or environment blocker.
5. Identify affected testing activities.
6. Suspend affected detailed testing.
7. Resume testing when the blocker is resolved
   or a safe workaround is available.

## 14. Defect and Evidence Tracking

| Smoke ID | Bug ID | Severity | Evidence | Remarks |
|---|---|---|---|---|
| Pending | Pending | Pending | Pending | Execution not started |

Defect details will be maintained in:

[Bug Tracker](../04-Defect-Management/SauceDemo_Bug_Tracker.xlsx)

## 15. Assumptions and Limitations

- This is an independent QA practice project.
- Requirements are independently proposed.
- Official application specifications are unavailable.
- Actual smoke testing has not started.
- No real financial transactions are performed.
- No internal API or database access is available.
- Smoke testing decisions are educational and
  do not represent actual production approval.

## 16. Revision History

| Version | Description | Author |
|---|---|---|
| 1.0 | Initial Smoke Testing Checklist | Vishal Sharma |

## 17. Disclaimer

This document is prepared for educational
practice and professional QA portfolio development.

All execution results and defect reports
will be based on actual application testing.

No confidential company or client information
is included.
