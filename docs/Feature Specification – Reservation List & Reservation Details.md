### **MVP Feature Specification – Reservation List & Reservation Details**

* **Modules:** Reservation History (`RES-LIST`) & Reservation Details (`RES-DETAIL`)

* **Stage:** MVP

* **Priority:** Medium

* **Status:** Scheduled

* **Target Delivery:** 4 working days

* **Total Estimated Hours:** \~121.5 hours

---

### **User Stories**

* As an **operator**, I want to define and manage various reservation status types to clearly reflect booking progress.

* As a **user**, I want to browse my reservation history by tabs (Scheduled, Completed, Canceled) with clear, contextual actions.

* As a **user**, I want to view detailed information about each reservation, securely and accurately.

* As a **tester**, I want to ensure data access is secure, properly permissioned, and follows data retention rules.

---

### **Acceptance Criteria**

#### **Reservation List (`RES-LIST`)**

* UI tabs: Scheduled, Completed, Canceled, Refunded, Expired

* Supports real-time filtering and pagination

* Action buttons shown/hidden depending on reservation status

* Persistent scroll and tab state across navigation

* Historical data accessible for up to **2 years**

* Fast API response for filtered queries

#### **Reservation Details (`RES-DETAIL`)**

* Displays trip date, ship name, payment method, and all related booking details

* Cancel/Review buttons appear based on reservation status and time conditions

* Access is **JWT-authenticated** and limited to the user's own bookings

* Sensitive payment info is masked (e.g., partial card number)

* Unauthorized access returns appropriate errors (e.g., 403 Forbidden)

---

### **Task Breakdown**

#### **📄 Reservation List (RES-LIST)**

| No. | Task Description | Role | Assignees | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define status ENUM and flow logic | PM | Nhat, Tuong | 3 hrs | 5 status types: Scheduled, Completed, Canceled, Refunded, Expired |
| 2 | Tab UI layout and behavior | Design | Vi | 9 hrs | Focus handling, tab scroll memory, transitions |
| 3 | Frontend development: tab logic and filters | Frontend | Khoi, Nhan | 30 hrs | Includes skeleton states, button logic, tab management |
| 4 | Backend: filter, pagination, query optimization | Backend | Cuong, Minh | 24 hrs | Efficient queries using indexed status filters |
| 5 | QA: tab behavior, data retention, UI tests | QA | Nhat, Vi | 9 hrs | Ensure 2-year data is displayed, test all status flows |

---

#### **📄 Reservation Details (RES-DETAIL)**

| No. | Task Description | Role | Assignees | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 6 | Define detail fields and masking requirements | PM | Tuong | 1.5 hrs | Secure display of sensitive payment info |
| 7 | Design layout with visual hierarchy | Design | Vi | 6 hrs | Prioritized info: trip, ship, status actions |
| 8 | Frontend: dynamic layout, button states | Frontend | Khoi, Nhan | 18 hrs | Buttons shown based on status and schedule logic |
| 9 | Backend: detail API with access controls | Backend | Cuong, Minh | 15 hrs | JWT-based validation, self-only access restriction |
| 10 | QA: access control & error testing | QA | Nhat, Vi | 6 hrs | Invalid tokens, wrong IDs, expired access coverage |

---

### **Parallel Execution Plan (4 Working Days)**

| Day | Focus Area | Tasks | Team | Notes |
| ----- | ----- | ----- | ----- | ----- |
| Day 1 | Planning & UI Design | Tasks 1, 2, 6, 7 | Tuong, Vi | Define status structure and UI layout |
| Day 1–3 | Backend & Frontend Dev | Tasks 3, 4, 8, 9 | Khoi, Nhan, Cuong, Minh | Simultaneous development of both RES-LIST and RES-DETAIL |
| Day 4 | QA & Integration Testing | Tasks 5, 10 | Nhat, Vi | Full flow validation on devices/browsers; access and retention checks |

*Note: Backend and frontend are developed concurrently. QA begins final validation on Day 4, with early checks possible for completed endpoints.*

---

### **Dependencies**

* Defined ENUM and flow logic for reservation statuses

* Frontend state routing and scroll/tab state preservation

* Secure JWT-based session handling

* Time-aware logic for enabling action buttons

* Data masking standards for sensitive fields (e.g., payment info)

---

### **Additional Notes**

* Action buttons across tabs and details must follow a **centralized rule engine** for logic consistency

* Filtering and pagination APIs should be designed with future **scalability** in mind

* Tab and scroll state should **persist** during navigation and reloads

* Reservation detail access must be **strictly scoped** to the logged-in user

* Retention policy (2 years) must be enforced on both frontend UI and backend query filters

