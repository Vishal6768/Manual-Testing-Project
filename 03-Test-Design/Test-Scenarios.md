
# Test Scenarios – SauceDemo

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | SauceDemo E-commerce Application |
| Document Type | Test Scenarios |
| Document ID | TS-DOC-001 |
| Version | 1.0 |
| Prepared By | Vishal Sharma |
| Testing Type | Manual Testing |
| Status | Designed - Execution Pending |
| Application URL | https://www.saucedemo.com/ |

## 2. Reference Documents

- [BRD](../01-Requirements/BRD.md)
- [FRD](../01-Requirements/FRD.md)
- [SRS](../01-Requirements/SRS.md)
- [Test Plan](../02-Test-Planning/Test-Plan.md)
- [Test Strategy](../02-Test-Planning/Test-Strategy.md)

## 3. Purpose

This document defines high-level test scenarios
for validating the functional and non-functional
requirements of the SauceDemo application.

Each scenario will be used to design detailed
test cases with test data, execution steps,
expected results and actual results.

## 4. Scenario Classification

| Priority | Description |
|---|---|
| High | Critical business functionality |
| Medium | Supporting functionality |
| Low | Minor functionality or visual checks |

| Type | Description |
|---|---|
| Positive | Validation using valid inputs and actions |
| Negative | Validation using invalid inputs and actions |
| Functional | Validation of application functionality |
| UI/UX | Validation of interface and usability |
| E2E | Complete business workflow validation |
| Exploratory | Investigation of unspecified behavior |
| Compatibility | Browser and viewport validation |

## 5. Login and Authentication

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-001 | Verify login page fields and controls. | FR-001 | UI/UX | High |
| TS-002 | Verify login using valid credentials. | FR-002 | Positive | High |
| TS-003 | Verify login using an invalid username. | FR-003 | Negative | High |
| TS-004 | Verify login using an invalid password. | FR-003 | Negative | High |
| TS-005 | Verify login with an empty username. | FR-004 | Negative | High |
| TS-006 | Verify login with an empty password. | FR-005 | Negative | High |
| TS-007 | Verify login with both fields empty. | FR-004, FR-005 | Negative | High |
| TS-008 | Verify login using a locked-out account. | FR-006 | Negative | High |
| TS-009 | Verify redirection after successful login. | FR-007 | Functional | High |
| TS-010 | Verify direct access to protected pages without login. | FR-008 | Negative | High |
| TS-011 | Verify password masking. | FR-001 | UI/UX | Medium |
| TS-012 | Explore login using leading and trailing spaces. | FR-003 | Exploratory | Medium |
| TS-013 | Explore login using case-sensitive credentials. | FR-003 | Exploratory | Medium |
| TS-014 | Explore repeated login button clicks. | FR-002 | Exploratory | Medium |
| TS-015 | Verify visibility and readability of login errors. | FR-057 | UI/UX | Medium |

## 6. Product Listing

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-016 | Verify product listing after successful login. | FR-009 | Functional | High |
| TS-017 | Verify product names are displayed. | FR-010 | Functional | High |
| TS-018 | Verify product images are displayed. | FR-010 | UI/UX | Medium |
| TS-019 | Verify product descriptions are displayed. | FR-010 | Functional | Medium |
| TS-020 | Verify product prices are displayed. | FR-010 | Functional | High |
| TS-021 | Verify Add to Cart controls. | FR-011 | Functional | High |
| TS-022 | Verify Remove controls after adding products. | FR-012 | Functional | High |
| TS-023 | Verify navigation to product details. | FR-013 | Functional | Medium |
| TS-024 | Verify product information consistency across pages. | FR-014 | Functional | High |
| TS-025 | Verify product listing layout and alignment. | FR-059 | UI/UX | Medium |

## 7. Product Sorting

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-026 | Verify sorting by product name A to Z. | FR-015 | Functional | Medium |
| TS-027 | Verify sorting by product name Z to A. | FR-016 | Functional | Medium |
| TS-028 | Verify sorting by price low to high. | FR-017 | Functional | Medium |
| TS-029 | Verify sorting by price high to low. | FR-018 | Functional | Medium |
| TS-030 | Verify cart consistency after sorting. | FR-019 | Functional | High |
| TS-031 | Verify repeated switching between sorting options. | FR-015 to FR-018 | Functional | Medium |
| TS-032 | Explore sorting behavior after page refresh. | FR-019 | Exploratory | Low |

## 8. Product Details

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-033 | Verify selected product details are displayed. | FR-020 | Functional | High |
| TS-034 | Verify product name, description and price consistency. | FR-014, FR-020 | Functional | High |
| TS-035 | Verify adding a product from its details page. | FR-021 | Functional | High |
| TS-036 | Verify removing a product from its details page. | FR-022 | Functional | High |
| TS-037 | Verify Back to Products navigation. | FR-023 | Functional | Medium |
| TS-038 | Verify product details page layout. | FR-059 | UI/UX | Medium |

## 9. Shopping Cart

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-039 | Verify adding a single product to the cart. | FR-024 | Functional | High |
| TS-040 | Verify adding multiple products to the cart. | FR-024 | Functional | High |
| TS-041 | Verify cart count after adding a product. | FR-025 | Functional | High |
| TS-042 | Verify selected products appear in the cart. | FR-026 | Functional | High |
| TS-043 | Verify product names in the cart. | FR-027 | Functional | High |
| TS-044 | Verify product prices in the cart. | FR-027 | Functional | High |
| TS-045 | Verify displayed product quantities. | FR-027 | Functional | High |
| TS-046 | Verify removing a single product. | FR-028 | Functional | High |
| TS-047 | Verify removing multiple products. | FR-028 | Functional | High |
| TS-048 | Verify cart count after removing products. | FR-029 | Functional | High |
| TS-049 | Verify cart state after removing all products. | FR-028, FR-029 | Functional | High |
| TS-050 | Verify Continue Shopping functionality. | FR-030 | Functional | Medium |
| TS-051 | Verify cart consistency during navigation. | FR-031 | Functional | High |
| TS-052 | Verify checkout navigation from the cart. | FR-032 | Functional | High |
| TS-053 | Explore checkout behavior with an empty cart. | FR-032 | Exploratory | Medium |
| TS-054 | Explore cart state after page refresh. | FR-031 | Exploratory | Medium |
| TS-055 | Verify adding all available products to the cart. | FR-024, FR-025 | Functional | High |

## 10. Checkout Information

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-056 | Verify checkout information fields are displayed. | FR-033 | UI/UX | High |
| TS-057 | Verify checkout using valid customer information. | FR-038 | Positive | High |
| TS-058 | Verify checkout with an empty first name. | FR-034 | Negative | High |
| TS-059 | Verify checkout with an empty last name. | FR-035 | Negative | High |
| TS-060 | Verify checkout with an empty postal code. | FR-036 | Negative | High |
| TS-061 | Verify checkout with all mandatory fields empty. | FR-034 to FR-037 | Negative | High |
| TS-062 | Verify appropriate checkout validation messages. | FR-037 | Negative | High |
| TS-063 | Explore numeric characters in name fields. | FR-034, FR-035 | Exploratory | Medium |
| TS-064 | Explore alphabetic characters in postal code. | FR-036 | Exploratory | Medium |
| TS-065 | Explore special characters in checkout fields. | FR-034 to FR-036 | Exploratory | Medium |
| TS-066 | Explore long input values in checkout fields. | FR-034 to FR-036 | Exploratory | Medium |
| TS-067 | Explore whitespace-only checkout inputs. | FR-034 to FR-036 | Exploratory | Medium |
| TS-068 | Verify checkout cancellation. | FR-039 | Functional | Medium |
| TS-069 | Verify navigation to order summary after valid input. | FR-038 | Functional | High |
| TS-070 | Verify checkout form layout and field readability. | FR-059, FR-061 | UI/UX | Medium |

## 11. Order Summary

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-071 | Verify selected products in the order summary. | FR-040 | Functional | High |
| TS-072 | Verify product price consistency. | FR-041 | Functional | High |
| TS-073 | Verify subtotal calculation for one product. | FR-042 | Functional | High |
| TS-074 | Verify subtotal calculation for multiple products. | FR-042 | Functional | High |
| TS-075 | Verify tax amount is displayed. | FR-043 | Functional | High |
| TS-076 | Verify total equals subtotal plus displayed tax. | FR-044 | Functional | High |
| TS-077 | Verify Finish button functionality. | FR-045 | Functional | High |
| TS-078 | Verify order summary cancellation. | FR-046 | Functional | Medium |
| TS-079 | Verify data consistency throughout checkout. | FR-062 | Functional | High |
| TS-080 | Verify order summary layout and readability. | FR-061 | UI/UX | Medium |

## 12. Order Confirmation

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-081 | Verify confirmation page after successful checkout. | FR-047 | Functional | High |
| TS-082 | Verify successful order confirmation message. | FR-048 | Functional | High |
| TS-083 | Verify Back Home functionality. | FR-049 | Functional | Medium |
| TS-084 | Verify cart state after successful order completion. | FR-050 | Functional | High |
| TS-085 | Explore confirmation page refresh behavior. | FR-047 | Exploratory | Medium |
| TS-086 | Explore browser back navigation after order completion. | FR-050, FR-056 | Exploratory | Medium |

## 13. Navigation and Session Management

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-087 | Verify application menu opens correctly. | FR-051 | Functional | Medium |
| TS-088 | Verify application menu closes correctly. | FR-051 | Functional | Medium |
| TS-089 | Verify All Items menu navigation. | FR-052 | Functional | Medium |
| TS-090 | Verify About menu navigation. | FR-052 | Functional | Low |
| TS-091 | Explore Reset App State functionality. | FR-052 | Exploratory | Medium |
| TS-092 | Verify logout functionality. | FR-053 | Functional | High |
| TS-093 | Verify redirection to login after logout. | FR-054 | Functional | High |
| TS-094 | Verify protected page access after logout. | FR-055 | Negative | High |
| TS-095 | Verify browser back behavior after logout. | FR-055 | Negative | High |
| TS-096 | Explore session behavior after browser refresh. | FR-056 | Exploratory | Medium |
| TS-097 | Explore session behavior after closing and reopening the browser. | FR-056 | Exploratory | Medium |
| TS-098 | Verify login after successful logout. | FR-002, FR-053 | Functional | High |

## 14. UI/UX and Accessibility

| Scenario ID | Test Scenario | FRD Reference | Type | Priority |
|---|---|---|---|---|
| TS-099 | Verify application layout consistency. | FR-059 | UI/UX | Medium |
| TS-100 | Verify text readability. | FR-061 | UI/UX | Medium |
| TS-101 | Verify button visibility and functionality. | FR-058 | UI/UX | High |
| TS-102 | Verify image rendering. | FR-010 | UI/UX | Medium |
| TS-103 | Verify error message visibility. | FR-057 | UI/UX | Medium |
| TS-104 | Verify form field alignment. | FR-059 | UI/UX | Medium |
| TS-105 | Verify basic keyboard navigation. | FR-061, NFR-008 | Accessibility | Medium |
| TS-106 | Verify visible keyboard focus indicators. | NFR-008 | Accessibility | Medium |
| TS-107 | Verify content does not overlap at selected viewports. | FR-059 | UI/UX | Medium |
| TS-108 | Verify navigation controls remain accessible. | FR-058, FR-061 | UI/UX | Medium |

## 15. Cross-Browser and Responsive Testing

| Scenario ID | Test Scenario | Requirement Reference | Type | Priority |
|---|---|---|---|---|
| TS-109 | Verify critical workflows in Google Chrome. | FR-060, NFR-002 | Compatibility | High |
| TS-110 | Verify critical workflows in Microsoft Edge. | FR-060, NFR-002 | Compatibility | High |
| TS-111 | Verify application layout at 375 x 667 viewport. | FR-059, NFR-003 | Responsive | Medium |
| TS-112 | Verify application layout at 390 x 844 viewport. | FR-059, NFR-003 | Responsive | Medium |
| TS-113 | Verify application layout at 768 x 1024 viewport. | FR-059, NFR-003 | Responsive | Medium |
| TS-114 | Verify application layout at 1366 x 768 viewport. | FR-059, NFR-003 | Responsive | Medium |
| TS-115 | Verify application layout at 1920 x 1080 viewport. | FR-059, NFR-003 | Responsive | Medium |
| TS-116 | Verify critical workflow usability on a mobile browser viewport. | FR-059, FR-061 | Responsive | High |

## 16. End-to-End Testing

| Scenario ID | Test Scenario | Requirement Reference | Type | Priority |
|---|---|---|---|---|
| TS-117 | Verify complete single-product purchase workflow. | FR-002, FR-024, FR-038, FR-045, FR-047 | E2E | High |
| TS-118 | Verify complete multiple-product purchase workflow. | FR-024, FR-042, FR-044, FR-045 | E2E | High |
| TS-119 | Verify purchase after removing a selected product. | FR-028, FR-042, FR-045 | E2E | High |
| TS-120 | Verify checkout cancellation followed by successful checkout. | FR-039, FR-038, FR-045 | E2E | High |
| TS-121 | Verify invalid checkout input followed by valid input. | FR-037, FR-038 | E2E | High |
| TS-122 | Verify product sorting followed by purchase completion. | FR-015 to FR-019, FR-045 | E2E | High |
| TS-123 | Verify complete purchase followed by logout. | FR-045, FR-047, FR-053 | E2E | High |
| TS-124 | Verify repeated purchase workflows. | FR-050, NFR-004 | E2E | High |

## 17. Exploratory and Reliability Testing

| Scenario ID | Test Scenario | Requirement Reference | Type | Priority |
|---|---|---|---|---|
| TS-125 | Explore application behavior during network interruption. | ERR-010 | Exploratory | Medium |
| TS-126 | Explore repeated rapid Add and Remove actions. | FR-024, FR-028 | Exploratory | Medium |
| TS-127 | Explore repeated Finish button interaction. | FR-045 | Exploratory | Medium |
| TS-128 | Explore application behavior using browser back and forward controls. | FR-056 | Exploratory | Medium |
| TS-129 | Explore application behavior in multiple browser tabs. | FR-056 | Exploratory | Medium |
| TS-130 | Observe response behavior during normal application usage. | NFR-005 | Exploratory | Medium |
| TS-131 | Verify consistency through repeated critical workflows. | NFR-004 | Reliability | High |
| TS-132 | Review overall application usability and navigation. | NFR-001 | Usability | Medium |

## 18. Scenario Summary

| Module | Total Scenarios |
|---|---:|
| Login and Authentication | 15 |
| Product Listing | 10 |
| Product Sorting | 7 |
| Product Details | 6 |
| Shopping Cart | 17 |
| Checkout Information | 15 |
| Order Summary | 10 |
| Order Confirmation | 6 |
| Navigation and Session Management | 12 |
| UI/UX and Accessibility | 10 |
| Cross-Browser and Responsive Testing | 8 |
| End-to-End Testing | 8 |
| Exploratory and Reliability Testing | 8 |
| Total | 132 |

## 19. Scenario Design Status

| Metric | Count |
|---|---:|
| Total Designed Scenarios | 132 |
| Scenarios Executed | 0 |
| Scenarios Pending Execution | 132 |

Execution results will be recorded after
detailed test case preparation and actual testing.

## 20. Test Case Design Guidelines

Each detailed test case should include:

- Test Case ID
- Test Scenario ID
- Requirement ID
- Module
- Test Case Title
- Test Type
- Priority
- Preconditions
- Test Data
- Test Steps
- Expected Result
- Actual Result
- Execution Status
- Defect ID
- Evidence Reference
- Execution Date
- Remarks

A single test scenario may have multiple
associated test cases.

## 21. Requirement Traceability

The following traceability structure
will be maintained:

Business Requirement
    -> Functional Requirement
    -> Test Scenario
    -> Test Case
    -> Test Execution
    -> Defect Report

Detailed mapping will be maintained in
the Requirement Traceability Matrix.

## 22. Assumptions and Limitations

- Scenarios are based on proposed requirements.
- Official SauceDemo specifications are unavailable.
- Actual test execution has not started.
- Unspecified behavior will be treated as exploratory.
- Mobile testing refers to browser viewport testing.
- No real payment transactions will be performed.
- No internal API or database access is available.
- No defect will be reported without actual evidence.
- No test case will be marked Pass without execution.

## 23. Document Revision History

| Version | Description | Author |
|---|---|---|
| 1.0 | Initial design of 132 test scenarios | Vishal Sharma |

## 24. Disclaimer

This document is independently prepared
for educational practice and professional
QA portfolio development.

It is not an official SauceDemo
testing document.

All execution results and defect reports
will be based on actual application testing.

No confidential company or client information
is included.
