
# Business Requirement Document (BRD)

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | SauceDemo E-commerce Application |
| Document Type | Business Requirement Document |
| Document Version | 1.0 |
| Prepared By | Vishal Sharma |
| Role | QA Engineer - Independent Practice Project |
| Status | Draft |
| Application URL | https://www.saucedemo.com/ |

## 2. Business Overview

SauceDemo is a demonstration e-commerce application
that allows users to browse products, manage their
shopping cart and complete a simulated purchase.

This document defines proposed business requirements
for validating the application from a QA perspective.

## 3. Business Objectives

- Provide a reliable user authentication process.
- Allow users to browse available products.
- Provide accurate product information and pricing.
- Allow users to manage shopping cart items.
- Provide a simple and reliable checkout process.
- Maintain accurate order calculations.
- Provide clear order confirmation.
- Ensure a consistent and user-friendly experience.
- Minimize functional errors and workflow interruptions.

## 4. Project Scope

### 4.1 In Scope

- User Authentication
- Login and Logout
- Product Listing
- Product Details
- Product Sorting
- Shopping Cart Management
- Checkout Information
- Order Summary
- Order Confirmation
- Session Management
- UI/UX Validation
- Error Handling
- Browser Compatibility
- Responsive Design Validation

### 4.2 Out of Scope

- Real Payment Gateway Integration
- Real Financial Transactions
- Product Delivery and Logistics
- Inventory Administration
- Backend Database Access
- Internal API Validation
- Advanced Security Testing
- Load and Stress Testing
- Native Android and iOS Applications

## 5. Proposed Stakeholders

| Stakeholder | Responsibility |
|---|---|
| Product Owner | Define business objectives and priorities |
| Business Analyst | Document and clarify requirements |
| Development Team | Implement application functionality |
| QA Engineer | Validate requirements and report defects |
| UI/UX Designer | Define user experience and interface |
| Project Manager | Coordinate project delivery |
| End User | Browse products and complete orders |

These stakeholder roles represent a simulated
software delivery environment.

## 6. Business Requirements

| Requirement ID | Business Requirement | Priority |
|---|---|---|
| BR-001 | Users should be able to access the application using valid credentials. | High |
| BR-002 | Invalid or unauthorized users should not gain access. | High |
| BR-003 | Users should be able to view available products. | High |
| BR-004 | Product names, descriptions and prices should be displayed accurately. | High |
| BR-005 | Users should be able to sort products using available sorting options. | Medium |
| BR-006 | Users should be able to view individual product details. | Medium |
| BR-007 | Users should be able to add products to the shopping cart. | High |
| BR-008 | Users should be able to remove products from the shopping cart. | High |
| BR-009 | The shopping cart should display selected products accurately. | High |
| BR-010 | The cart indicator should reflect the number of selected items. | High |
| BR-011 | Users should be able to continue shopping after adding products. | Medium |
| BR-012 | Users should be able to initiate the checkout process. | High |
| BR-013 | Mandatory checkout information should be validated. | High |
| BR-014 | Order summary should display selected products and prices accurately. | High |
| BR-015 | Subtotal, tax and total calculations should be accurate. | High |
| BR-016 | Users should be able to complete a simulated purchase. | High |
| BR-017 | Successful order completion should display a confirmation message. | High |
| BR-018 | Users should be able to cancel checkout using available controls. | Medium |
| BR-019 | Users should be able to log out successfully. | High |
| BR-020 | Unauthorized access to protected pages should be restricted. | High |
| BR-021 | Application error messages should be clear and understandable. | Medium |
| BR-022 | Application navigation should be consistent and functional. | Medium |
| BR-023 | The interface should remain usable across supported screen sizes. | Medium |
| BR-024 | Core functionality should work across selected supported browsers. | Medium |
| BR-025 | Application workflows should maintain consistent data throughout the user journey. | High |

## 7. Proposed Business Rules

- Valid credentials are required to access protected features.
- Locked-out users should not gain application access.
- Product prices should remain consistent throughout checkout.
- Cart count should reflect the selected items.
- Mandatory checkout fields must be completed.
- Order totals should reflect the displayed subtotal and tax.
- Order confirmation should appear after successful checkout.
- Logout should terminate authenticated access.
- Invalid inputs should display appropriate error messages.
- Application navigation should not cause unexpected data loss.

## 8. Non-Functional Requirements

| Requirement ID | Category | Requirement |
|---|---|---|
| NFR-001 | Usability | Application navigation should be understandable. |
| NFR-002 | Compatibility | Core workflows should work on selected browsers. |
| NFR-003 | Responsiveness | Interface should remain usable across selected screen sizes. |
| NFR-004 | Reliability | Core workflows should behave consistently during repeated execution. |
| NFR-005 | Performance | Application should respond within reasonable limits during normal usage. |
| NFR-006 | Security | Protected pages should restrict unauthorized access. |
| NFR-007 | Error Handling | Error messages should provide meaningful information. |
| NFR-008 | Accessibility | Basic interface controls should support keyboard interaction. |

Performance thresholds and advanced security
requirements are not defined for this practice project.

## 9. Business Process Flow

User Opens Application
        |
        v
Login
        |
        v
Product Listing
        |
        v
Product Selection
        |
        v
Add to Cart
        |
        v
Shopping Cart
        |
        v
Checkout Information
        |
        v
Order Summary
        |
        v
Order Confirmation
        |
        v
Logout

## 10. Assumptions

- The public demo application is available for testing.
- Demo credentials are available.
- Testing does not involve real financial transactions.
- Requirements are proposed for educational QA practice.
- Application behavior may change without prior notice.
- Testing will be performed using available environments.

## 11. Constraints

- No access to internal source code.
- No access to production databases.
- No access to internal API documentation.
- No access to official business requirement documents.
- Limited access to development and deployment environments.
- Defect resolution cannot be controlled by the tester.

## 12. Business Risks

| Risk ID | Risk Description | Impact |
|---|---|---|
| R-001 | Authentication failure | High |
| R-002 | Incorrect product pricing | High |
| R-003 | Shopping cart data inconsistency | High |
| R-004 | Checkout failure | High |
| R-005 | Incorrect order total | High |
| R-006 | Session management issues | High |
| R-007 | Browser compatibility issues | Medium |
| R-008 | UI layout inconsistency | Medium |
| R-009 | Demo application unavailability | High |
| R-010 | Incomplete requirement coverage | Medium |

## 13. Proposed Acceptance Criteria

- Critical business workflows are successfully validated.
- All high-priority business requirements are covered.
- No unresolved critical defects remain for a simulated release recommendation.
- Product and cart information remain consistent.
- Checkout calculations are accurate.
- Valid users can complete the end-to-end purchase flow.
- Invalid user actions display appropriate error messages.
- Test execution results and identified defects are documented.
- Outstanding risks and testing limitations are communicated.

## 14. QA Deliverables

- Business Requirement Document
- Functional Requirement Document
- Software Requirement Specification
- Test Plan
- Test Strategy
- Test Scenarios
- Test Cases
- Requirement Traceability Matrix
- Defect Reports
- Smoke Testing Checklist
- Sanity Testing Checklist
- Regression Testing Checklist
- UI/UX Testing Checklist
- Sprint QA Report
- Test Execution Report
- QA Metrics Report
- Release Readiness Checklist
- Test Summary Report

## 15. Document Revision History

| Version | Description | Author |
|---|---|---|
| 1.0 | Initial proposed business requirements | Vishal Sharma |

## 16. Disclaimer

This document is independently prepared for a
professional QA portfolio and educational practice.

It is not an official SauceDemo business requirement
document. Requirements are proposed testing expectations
and must be validated during application testing.

No confidential company or client information is included.
