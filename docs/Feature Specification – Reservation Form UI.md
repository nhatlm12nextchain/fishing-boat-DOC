### **MVP Feature Specification – Reservation Form UI (Customer) (`RSV-FORM`)**

* **Feature Name:** Reservation Form UI (Customer)

* **Feature ID:** RSV-FORM

* **Module:** Reservation

* **Stage:** MVP

* **Priority:** High

* **Status:** Scheduled

* **Target Delivery:** 1.5 working days

* **Total Estimated Hours:** \~60 hours (executed in parallel)

---

### **User Story**

As a **customer**, I want to fill in all necessary reservation details—such as name, phone number, refund account, and notes—on a single, mobile-friendly screen, and view **real-time pricing updates** when I apply coupons or points, so I can complete the booking process with confidence and convenience.

---

### **Acceptance Criteria**

* Single-page form with required fields: depositor name, phone number, refund account, and optional notes

* **Mobile-first** responsive layout with accessible design (minimum 14px font, high contrast)

* **Live price calculation** that dynamically reflects applied coupons and points

* **Validation** on all fields (required checks, format for phone and account numbers)

* Integrated with **Payment Gateway (PG)** and supports **retry on failure via webhook**

* Ensures **transaction-safe** booking logic and error recovery

* **Clear error messaging** for all potential PG failure points

* Supports both **client-side and server-side** form validation

---

### **Task Breakdown**

| No. | Task Description | Role | Assigned To | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define fields and security standards | PM | Tuong | 3 hrs | Includes PCI-DSS review for refund data; retention and privacy standards |
| 2 | Design responsive UI/UX | Design | Vi | 9 hrs | Mobile-optimized layout, clear grouping, accessibility compliance |
| 3 | Frontend implementation | Frontend | Khoi, Nhan | 18 hrs | Field input, validation, real-time pricing, coupon & point handling |
| 4 | Backend logic and PG integration | Backend | Cuong, Minh | 24 hrs | Reservation API, webhook handling, rollback logic, transaction safety |
| 5 | QA: form, payment flows, edge cases | QA | Nhat, Vi | 6 hrs | Full form validation, PG error simulation, retry/resume testing |

---

### **Parallel Work Plan (1.5 Working Days)**

| Block | Focus Area | Tasks | Team Members | Duration |
| ----- | ----- | ----- | ----- | ----- |
| A | Planning & UI Design | Tasks 1–2 | Tuong, Vi | \~0.5 day |
| B | Frontend Development | Task 3 | Khoi, Nhan | 1.5 days |
| C | Backend Development | Task 4 | Cuong, Minh | \~1–1.25 days |
| D | QA & Final Testing | Task 5 | Nhat, Vi | Final 0.5 day |

---

### 

### **Dependencies**

* Coupon and point logic engine shared between frontend and backend

* PG provider sandbox credentials and webhook endpoints

* Validation rules for phone number, refund account formats

* Standardized error message templates for PG issues

* Security policy for handling sensitive financial data

---

### **Additional Notes**

* Prioritize **clarity in form UX**: clear field spacing, intuitive button placement, grouped inputs

* Ensure **pricing logic matches** between client and server to avoid discrepancies

* Backend should support **rollback and recovery** in case of payment failure

* Implement **local autosave** of form data to prevent loss from session timeout or refresh

* QA team must simulate PG failure conditions to confirm retry workflows and error states work smoothly

