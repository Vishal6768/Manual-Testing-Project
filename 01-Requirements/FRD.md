
# Functional Requirement Document (FRD)

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | SauceDemo E-commerce Application |
| Document Type | Functional Requirement Document |
| Document Version | 1.0 |
| Prepared By | Vishal Sharma |
| Status | Draft |
| Reference Document | [BRD](BRD.md) |
| Application URL | https://www.saucedemo.com/ |

## 2. Purpose

This document defines proposed functional requirements,
business rules, input validations, expected application
behavior and acceptance criteria for the SauceDemo
e-commerce application.

The document will serve as a reference for test scenario
creation, test case design, requirement traceability
and functional validation.

## 3. Functional Modules

- Login and Authentication
- Product Listing
- Product Details
- Product Sorting
- Shopping Cart
- Checkout Information
- Order Summary
- Order Confirmation
- Navigation
- Logout and Session Management
- UI/UX and Error Handling

## 4. User Roles

| User Role | Description |
|---|---|
| Authenticated User | User with valid application access |
| Unauthenticated User | User who has not logged in |
| Locked-Out User | User whose application access is restricted |

## 5. Functional Requirements

### 5.1 Login and Authentication

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-001 | BR-001 | Login page shall display username and password fields. | High |
| FR-002 | BR-001 | Valid credentials shall allow successful login. | High |
| FR-003 | BR-002 | Invalid username or password shall display an error message. | High |
| FR-004 | BR-002 | Empty username shall trigger mandatory field validation. | High |
| FR-005 | BR-002 | Empty password shall trigger mandatory field validation. | High |
| FR-006 | BR-002 | Locked-out users shall not gain application access. | High |
| FR-007 | BR-001 | Successful login shall redirect users to the product listing page. | High |
| FR-008 | BR-020 | Unauthenticated users shall not access protected application pages. | High |

#### Acceptance Criteria

- Valid users can log in successfully.
- Invalid credentials do not allow access.
- Mandatory field validation works correctly.
- Password input is masked.
- Locked-out users receive an appropriate error message.

### 5.2 Product Listing

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-009 | BR-003 | Available products shall be displayed after successful login. | High |
| FR-010 | BR-004 | Each product shall display its name, image, description and price. | High |
| FR-011 | BR-007 | Available products shall provide an Add to Cart option. | High |
| FR-012 | BR-008 | Added products shall provide a Remove option. | High |
| FR-013 | BR-006 | Selecting a product shall open its corresponding details page. | Medium |
| FR-014 | BR-004 | Product information shall remain consistent across related pages. | High |

#### Acceptance Criteria

- Product listing loads successfully.
- Product information is displayed correctly.
- Product controls are functional.
- Product details correspond to the selected item.

### 5.3 Product Sorting

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-015 | BR-005 | Users shall be able to sort products by name from A to Z. | Medium |
| FR-016 | BR-005 | Users shall be able to sort products by name from Z to A. | Medium |
| FR-017 | BR-005 | Users shall be able to sort products by price from low to high. | Medium |
| FR-018 | BR-005 | Users shall be able to sort products by price from high to low. | Medium |
| FR-019 | BR-025 | Sorting shall not unexpectedly modify selected cart items. | High |

#### Acceptance Criteria

- All available sorting options function correctly.
- Product order matches the selected sorting option.
- Sorting does not cause unexpected data loss.

### 5.4 Product Details

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-020 | BR-006 | Product details page shall display the selected product information. | High |
| FR-021 | BR-007 | Users shall be able to add products from the details page. | High |
| FR-022 | BR-008 | Users shall be able to remove previously selected products. | High |
| FR-023 | BR-022 | Users shall be able to return to the product listing page. | Medium |

### 5.5 Shopping Cart

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-024 | BR-007 | Users shall be able to add an available product to the cart. | High |
| FR-025 | BR-010 | Cart indicator shall update after adding a product. | High |
| FR-026 | BR-009 | Cart page shall display selected products. | High |
| FR-027 | BR-009 | Cart shall display correct product names, prices and quantities. | High |
| FR-028 | BR-008 | Users shall be able to remove products from the cart. | High |
| FR-029 | BR-010 | Cart indicator shall update after removing a product. | High |
| FR-030 | BR-011 | Continue Shopping shall return users to the product listing page. | Medium |
| FR-031 | BR-025 | Selected cart items shall remain consistent during normal navigation. | High |
| FR-032 | BR-012 | Checkout control shall navigate users to checkout information. | High |

#### Acceptance Criteria

- Products can be added and removed.
- Cart count matches selected items.
- Cart displays accurate product information.
- Navigation preserves selected items where expected.

### 5.6 Checkout Information

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-033 | BR-012 | Checkout page shall display customer information fields. | High |
| FR-034 | BR-013 | First Name shall be validated as a mandatory field. | High |
| FR-035 | BR-013 | Last Name shall be validated as a mandatory field. | High |
| FR-036 | BR-013 | Postal Code shall be validated as a mandatory field. | High |
| FR-037 | BR-021 | Missing mandatory information shall display an appropriate error. | High |
| FR-038 | BR-012 | Valid checkout information shall allow progression to the order summary. | High |
| FR-039 | BR-018 | Cancel shall return users to the shopping cart. | Medium |

#### Input Validation

| Field | Required | Expected Validation |
|---|---|---|
| First Name | Yes | Empty input shall display an error. |
| Last Name | Yes | Empty input shall display an error. |
| Postal Code | Yes | Empty input shall display an error. |

Maximum field lengths, special character restrictions
and postal code formats are not officially specified.

These inputs will be explored during testing without
automatically classifying unspecified behavior as defects.

### 5.7 Order Summary

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-040 | BR-014 | Order summary shall display selected products. | High |
| FR-041 | BR-014 | Product prices shall match the shopping cart. | High |
| FR-042 | BR-015 | Item subtotal shall equal the sum of selected product prices multiplied by their quantities. | High |
| FR-043 | BR-015 | Tax amount shall be displayed. | High |
| FR-044 | BR-015 | Total shall equal the item subtotal plus displayed tax. | High |
| FR-045 | BR-016 | Finish shall complete the simulated purchase. | High |
| FR-046 | BR-018 | Cancel shall exit the checkout process without completing the order. | Medium |

#### Calculation Rules

Item Subtotal = Sum of (Product Price × Quantity)

Order Total = Item Subtotal + Displayed Tax

The official tax calculation policy is unavailable.
Testing will verify displayed arithmetic and consistency.

### 5.8 Order Confirmation

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-047 | BR-017 | Successful checkout shall display an order confirmation page. | High |
| FR-048 | BR-017 | Confirmation page shall display a successful order message. | High |
| FR-049 | BR-022 | Back Home shall return users to the product listing page. | Medium |
| FR-050 | BR-025 | Completed order items should no longer remain in the active cart. | High |

### 5.9 Navigation and Logout

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-051 | BR-022 | Application menu shall open and close correctly. | Medium |
| FR-052 | BR-022 | Available menu options shall navigate to their intended destinations. | Medium |
| FR-053 | BR-019 | Logout shall terminate authenticated access. | High |
| FR-054 | BR-019 | Successful logout shall redirect users to the login page. | High |
| FR-055 | BR-020 | Protected pages shall restrict access after logout. | High |
| FR-056 | BR-025 | Application navigation shall maintain consistent workflow behavior. | High |

### 5.10 UI/UX and Error Handling

| FR ID | BRD Reference | Functional Requirement | Priority |
|---|---|---|---|
| FR-057 | BR-021 | Validation errors shall be visible and understandable. | Medium |
| FR-058 | BR-022 | Buttons and navigation controls shall remain functional. | High |
| FR-059 | BR-023 | Application layout shall remain usable across selected screen sizes. | Medium |
| FR-060 | BR-024 | Critical workflows shall function across selected browsers. | Medium |
| FR-061 | BR-023 | Text and important controls shall remain readable and accessible. | Medium |
| FR-062 | BR-025 | Displayed information shall remain consistent throughout the purchase workflow. | High |

## 6. End-to-End Functional Workflow

1. Open SauceDemo.
2. Enter valid username and password.
3. Click Login.
4. Verify product listing.
5. Select a product.
6. Add the product to the cart.
7. Open the shopping cart.
8. Verify selected product information.
9. Initiate checkout.
10. Enter customer information.
11. Continue to the order summary.
12. Verify subtotal, tax and total.
13. Complete the simulated purchase.
14. Verify order confirmation.
15. Return to the product listing.
16. Log out.

## 7. Exception and Negative Scenarios

| Scenario ID | Scenario | Expected Behavior |
|---|---|---|
| EX-001 | Invalid login credentials | Access denied with error message |
| EX-002 | Empty username | Mandatory field validation |
| EX-003 | Empty password | Mandatory field validation |
| EX-004 | Locked-out user login | Access denied |
| EX-005 | Direct protected page access without login | Access restricted |
| EX-006 | Missing checkout first name | Validation error |
| EX-007 | Missing checkout last name | Validation error |
| EX-008 | Missing checkout postal code | Validation error |
| EX-009 | Checkout cancellation | Order not completed |
| EX-010 | Protected page access after logout | Access restricted |

## 8. Non-Functional Validation

| Reference | Validation Area | Approach |
|---|---|---|
| NFR-001 | Usability | Manual user journey review |
| NFR-002 | Compatibility | Chrome and Edge browser checks |
| NFR-003 | Responsiveness | Desktop and mobile viewport checks |
| NFR-004 | Reliability | Repeated critical workflow execution |
| NFR-005 | Performance | Exploratory response time observations |
| NFR-006 | Security | Basic authentication and session checks |
| NFR-007 | Error Handling | Positive and negative input validation |
| NFR-008 | Accessibility | Basic keyboard navigation checks |

Native Android and iOS application testing is outside
the scope of this web-based practice project.

## 9. Test Environment

| Component | Details |
|---|---|
| Application | SauceDemo |
| Environment | Public Demo |
| Operating System | Windows |
| Primary Browser | Google Chrome |
| Secondary Browser | Microsoft Edge |
| Browser Versions | To be recorded during execution |
| Test Data | Public demo credentials and synthetic customer information |
| Testing Approach | Manual Black Box Testing |

## 10. Requirement Traceability

Each functional requirement is mapped to its
corresponding business requirement.

Test cases will reference functional requirement IDs.

Traceability Flow:

Business Requirement (BR)
    -> Functional Requirement (FR)
    -> Test Scenario (TS)
    -> Test Case (TC)
    -> Test Execution
    -> Defect Report (BUG), if applicable

## 11. Assumptions and Dependencies

- Public demo application availability.
- Availability of valid demo credentials.
- Access to supported browsers.
- Stable internet connectivity.
- Proposed business and functional requirements.
- No internal source code or database access.
- No official product owner or development team access.

## 12. Out of Scope

- Real payment processing.
- Real financial transactions.
- Backend database verification.
- Internal API testing.
- Advanced security and penetration testing.
- Load and stress testing.
- Native Android and iOS application testing.
- Actual production deployment approval.

## 13. Functional Acceptance Criteria

- High-priority functional requirements are covered.
- Critical end-to-end workflows are validated.
- Authentication and session behavior are verified.
- Product and shopping cart information remain consistent.
- Checkout mandatory fields are validated.
- Order calculations are verified.
- Order confirmation is displayed after successful checkout.
- Identified defects and testing limitations are documented.
- Outstanding risks are included in the test summary.

## 14. Document Revision History

| Version | Description | Author |
|---|---|---|
| 1.0 | Initial functional requirement document | Vishal Sharma |

## 15. Disclaimer

This FRD is independently prepared for a professional
QA portfolio and educational practice.

It is not an official SauceDemo functional specification.

The requirements represent proposed testing expectations.
Actual application behavior will be recorded during
test execution.

Unspecified or ambiguous behavior will be documented
as observations or requirement clarification items.

No confidential company or client information is included.
