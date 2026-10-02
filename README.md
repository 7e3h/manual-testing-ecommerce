# E-commerce Manual Testing

## Project Overview

This project demonstrates manual software testing of an e-commerce web application. It showcases practical Quality Assurance (QA) practices, including structured test planning based on IEEE 829 guidelines, comprehensive test coverage for the selected application workflows covering positive and negative edge cases, defect reporting with evidence-based observations, and test execution tracking.

The target system under test is a modern e-commerce web application ([Practice Software Testing](https://practicesoftwaretesting.com)), featuring end-to-end user workflows from account registration to order checkout.

## Testing Activities

- Test case design
- Functional testing
- Negative testing
- Boundary testing
- Bug reporting
- Regression testing

## Test Areas

- User Registration
- Login
- Product Search
- Product Details
- Shopping Cart
- Checkout

## Tools

- Microsoft Excel
- Browser DevTools
- Git/GitHub

---

## 📁 Repository Structure

```text
manual-testing-ecommerce/
│
├── README.md                          # Project documentation and summary
├── Test-Plan/
│   └── test-plan.md                   # Test plan structured according to IEEE 829 guidelines
│
├── Test-Cases/
│   ├── test-cases.xlsx                # Formatted Excel sheet with metrics dashboard & 26 test cases
│   └── test-cases.md                  # Markdown version for quick GitHub browser review
│
└── Bug-Reports/
    ├── BUG-001.md                     # Critical (S1): Checkout subtotal not recalculating on quantity reduction
    ├── BUG-002.md                     # Major (S2): Search returns 500 error and blank screen on script input
    └── BUG-003.md                     # Medium (S3): Registration accepts whitespace in password without warning
```

---

## 📊 Test Execution Summary & Metrics

A total of **26 test cases** were designed, categorized, and executed across all 6 core functional modules:

| Test Module | Total Tests | Passed | Failed | Blocked | Pass Rate (%) | Logged Bugs |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| **User Registration** | 6 | 5 | 1 | 0 | 83.3% | [`BUG-003`](./Bug-Reports/BUG-003.md) |
| **Login & Session** | 6 | 6 | 0 | 0 | 100.0% | None |
| **Product Search & Filters** | 6 | 5 | 1 | 0 | 83.3% | [`BUG-002`](./Bug-Reports/BUG-002.md) |
| **Product Details** | 3 | 3 | 0 | 0 | 100.0% | None |
| **Shopping Cart** | 3 | 3 | 0 | 0 | 100.0% | None |
| **Checkout & Payment** | 2 | 1 | 1 | 0 | 50.0% | [`BUG-001`](./Bug-Reports/BUG-001.md) |
| **TOTAL** | **26** | **23** | **3** | **0** | **88.5%** | **3 Bugs** |

### Test Case Distribution by Type
- **Functional Testing:** 16 cases (61.5%)
- **Negative Testing:** 6 cases (23.1%)
- **Boundary Value Analysis (BVA):** 4 cases (15.4%)

---

## 🐛 Defect Summary (Bug Reports)

| Bug ID | Title | Module | Severity | Priority | Status |
|:---:|:---|:---|:---:|:---:|:---:|
| [**BUG-001**](./Bug-Reports/BUG-001.md) | Subtotal & total not recalculating after quantity reduction at checkout | Checkout | **Critical (S1)** | **High (P1)** | Open |
| [**BUG-002**](./Bug-Reports/BUG-002.md) | Search returns 500 error and blank screen on script characters | Search | **Major (S2)** | **High (P2)** | Open |
| [**BUG-003**](./Bug-Reports/BUG-003.md) | Password field accepts leading/trailing whitespace without warning | Registration | **Medium (S3)** | **Medium (P3)** | Open |

---

## 🔍 How to Review the Test Artifacts

1. **Test Plan:** Open [`Test-Plan/test-plan.md`](./Test-Plan/test-plan.md) to inspect testing strategy, entry/exit criteria, scope, and defect management workflows.
2. **Interactive Excel Suite:** Open [`Test-Cases/test-cases.xlsx`](./Test-Cases/test-cases.xlsx) to view the summary dashboard and complete test case table.
3. **Web Browser View:** Open [`Test-Cases/test-cases.md`](./Test-Cases/test-cases.md) to review all test steps, test data, and expected results directly in GitHub.
4. **Bug Reports:** Review the observed behavior and preliminary findings in the [`Bug-Reports/`](./Bug-Reports/) directory.
