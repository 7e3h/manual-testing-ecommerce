# Test Plan: E-Commerce Web Application

**Document ID:** TP-ECOM-001  
**Version:** 1.0  
**Author:** QA Engineering Team  
**Application Under Test (AUT):** Practice E-Commerce Platform (Practice Software Testing / Automation Demo)  
**Date:** October 2026  
**Status:** Approved / Active  

---

## 1. Introduction & Overview

This Test Plan defines the comprehensive manual testing strategy, scope, objectives, resource requirements, and schedule for the Practice E-Commerce Web Application. The objective is to validate end-to-end user flows, data integrity, security validations, and cross-browser consistency before major release increments.

### 1.1 Objectives
- Verify that all core functional modules work strictly according to specified business requirements.
- Identify functional defects, boundary edge-case failures, and usability bottlenecks.
- Validate negative scenarios and proper input error handling across forms.
- Ensure security best practices for authentication, password handling, and checkout transactions.
- Provide transparent test execution records, bug reports, and traceability matrices.

---

## 2. Scope of Testing

### 2.1 In-Scope Features
The following modules will undergo comprehensive functional, negative, and boundary manual testing:
1. **User Registration:** Account creation, required fields, email format validation, duplicate email handling, password strength rules.
2. **User Authentication (Login/Logout):** Standard login, invalid credentials, empty field checks, password visibility toggle, session persistence, logout.
3. **Product Search & Filtering:** Keyword search, partial search, empty search, special character handling, category filtering, price sorting.
4. **Product Details:** Item information display, images, dynamic pricing, stock availability, quantity increment/decrement, boundary limits.
5. **Shopping Cart:** Add to cart, cart counter badge, quantity adjustment, subtotal recalculation, item removal, empty cart state.
6. **Checkout & Payment:** Multi-step checkout, shipping address validation, payment method selection, order calculation, order confirmation.

### 2.2 Out-of-Scope Features
- Load and Stress Performance Testing (simulating >10,000 concurrent users).
- White-box code coverage and source-code unit testing (handled by development team).
- Physical payment gateway processing with real banking networks (mock sandbox payment used).
- Native mobile application testing (scope is responsive web desktop and mobile viewports).

---

## 3. Testing Approach & Methodologies

| Testing Type | Description & Purpose |
|:---|:---|
| **Functional Testing** | Validates each functional requirement against acceptance criteria. |
| **Negative Testing** | Supplies invalid, unexpected, or missing data to verify graceful degradation and informative error messages. |
| **Boundary Value Analysis (BVA)** | Tests boundary values for quantities (0, 1, 99, 100), price filters, and text inputs (min/max characters). |
| **Equivalence Partitioning (EP)** | Segregates inputs into valid and invalid partitions to maximize test coverage with optimized test count. |
| **Defect Reporting & Tracking** | Standardized bug reporting for all discrepancies with severity, priority, steps to reproduce, and logs. |
| **Regression Testing** | Re-verifying previously passed test cases after bug fixes to ensure zero unintended side-effects. |
| **Cross-Browser & Responsive** | Verification across Google Chrome, Mozilla Firefox, Microsoft Edge, and mobile viewports via DevTools. |

---

## 4. Test Environment & Tools

| Component | Specification |
|:---|:---|
| **Browsers** | Google Chrome (Latest), Mozilla Firefox (Latest), MS Edge (Latest) |
| **Resolution / Devices** | Desktop (1920x1080, 1440x900), Tablet (768x1024), Mobile (375x667 DevTools emulation) |
| **Operating System** | Windows 11 / Windows 10 |
| **Test Case Management** | Microsoft Excel (`test-cases.xlsx`) & Markdown Repository |
| **Defect Tracking** | GitHub Issues / Markdown Bug Reports (`BUG-xxx.md`) |
| **Diagnostic Tools** | Browser DevTools (Console, Network tab, Application Storage, Inspect Element) |

---

## 5. Entry & Exit Criteria

### 5.1 Entry Criteria
- AUT test environment is deployed, accessible, and stable.
- Test data (demo accounts, sample product inventory) is provisioned.
- Test Plan is reviewed and approved by stakeholders.
- Test Cases are documented, peer-reviewed, and ready for execution.

### 5.2 Exit Criteria
- 100% of planned test cases executed.
- Minimum 90% overall pass rate achieved.
- Zero open Critical (S1) or Major (S2) defects without documented workarounds.
- All identified defects documented with clear reproduction steps and assigned to dev backlog.
- Final Test Summary report completed and signed off.

---

## 6. Defect Management Lifecycle & Classification

Defects found during testing are categorized using a standard Severity vs. Priority matrix:

| Level | Severity (Technical Impact) | Priority (Business Urgency) |
|:---|:---|:---|
| **Critical / S1 - P1** | Total feature blockage, crash, data corruption, checkout calculation error. | Immediate hotfix required before release. |
| **Major / S2 - P2** | Core feature failure with no immediate workaround (e.g., search 500 error). | High priority fix within current sprint. |
| **Medium / S3 - P3** | Non-critical functionality defect or formatting inconsistency with workaround. | Normal fix queue for upcoming sprint. |
| **Minor / S4 - P4** | Cosmetic layout flaw, typo, alignment irregularity, visual glitch. | Low priority, addressed when bandwidth permits. |

---

## 7. Test Deliverables
1. **Approved Test Plan:** `Test-Plan/test-plan.md`
2. **Master Test Case Suite:** `Test-Cases/test-cases.xlsx` (and GitHub web view `test-cases.md`)
3. **Formal Defect Reports:** `Bug-Reports/BUG-001.md`, `BUG-002.md`, `BUG-003.md`
4. **Summary & Metrics:** Documented in project `README.md`
