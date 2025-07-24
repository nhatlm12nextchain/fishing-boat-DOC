### **CMS Feature: Ship Management**

**Feature ID:** CMS-BOAT  
 **Target Duration:** 5 working days  
 **Total Estimated Hours:** 84  
 **Status:** Scheduled  
 **Dependencies:** BOAT-API, CMS-SEAT

---

**User Story**  
 As a shipping company operator, I want to manage ship records (add, edit, delete) and immediately see the result of those changes through real-time updates and notifications.

---

**Task Breakdown**

| No | Task Description | Role | Assigned To | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define CRUD policy for ship data | PM | Nhat | 1.5 | Add, edit, delete logic, status toggle rules |
| 2 | Design UI for CRUD actions and notification | Design | Vi | 9 | Success states, accessible form layout, status indicators |
| 3 | Implement frontend CRUD and notification UI | Frontend | Khoi, Nhan | 34.5 | Optimistic UI, WebSocket update handling, real-time feedback |
| 4 | Backend API for CRUD and notification handling | Backend | Cuong, Minh | 30 | Retry backoff logic, secure log retention, WebSocket or fallback |
| 5 | QA: CRUD flow and responsiveness test | QA | Nhat, Vi | 9 | Test empty states, UI consistency, mobile and desktop resolution |

---

**Work Plan Summary**

* **Day 1:** Finalize policy and UI design (Tasks 1 and 2\)

* **Days 2–4:** Parallel frontend and backend development (Tasks 3 and 4\)

* **Day 5:** End-to-end QA with real-time interaction and edge cases (Task 5\)

---

**Acceptance Criteria**

* Operators can add, update, or delete ship records with status toggles

* Changes reflect instantly in the UI without reloads

* Success or error notifications display clearly

* Data persists correctly on the backend and logs are stored

* The feature works consistently across devices and screen sizes

