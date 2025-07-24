### 

###  **MVP Feature Summary – Shipping Company Registration Approval (ADM-VEND-APPLY)**

**Module:** Admin CMS  
 **Stage:** MVP  
 **Priority:** High  
 **Status:** Scheduled  
 **Target Duration:** 1.5 working days  
 **Total Estimated Hours:** \~43.5 hours

---

### **User Story**

As an **admin operator**, I need the ability to **review, approve, reject**, or **request revisions** for shipping company registration requests through a secure and efficient interface—so I can manage vendor onboarding professionally and ensure service integrity.

---

### **Acceptance Criteria**

* Admin dashboard displays **list of all vendor registration requests**

* Each request has a **detailed view**: company info, contacts, attachments

* Actionable buttons: **\[Approve\] \[Reject\] \[Request Revision\]**

* Actions update the server and **trigger email notifications** automatically

* System enforces **CSRF protection** and **secure JWT-based sessions**

* All status updates are reflected **instantly in UI**

* UI is **fully responsive** and **accessible (WCAG compliant)**

* QA must test **full flow coverage** and **email delivery reliability**

---

### 

### 

### 

### **Task Breakdown**

| \# | Task Description | Role | Owner(s) | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define approval flow and edge cases | PM | Tuong | 1.5 | Flowchart: New → Under Review → Approved / Rejected / Needs Revision |
| 2 | Design UI components: List view \+ Detail panel | Design | Vi | 6 | Focus on responsive layout, clear button states, visual hierarchy |
| 3 | Frontend implementation: UI rendering, CSRF handling | FE | Khoi, Nhan | 18 | Includes real-time feedback, secure request handling, form state |
| 4 | Backend: Status update API, email trigger logic | BE | Cuong, Minh | 12 | Atomic updates, rollback on failure, async email dispatch |
| 5 | QA: Functional test across flows and devices | QA | Nhat, Vi | 6 | Includes testing all status transitions, mobile layout, email checks |

---

### **Execution Timeline (1.5 Days)**

| Day | Focus | Tasks | Team | Notes |
| ----- | ----- | ----- | ----- | ----- |
| Day 1 AM | Requirement Finalization \+ UI Design | Tasks 1–2 | Tuong, Vi | Finalize flow and wireframes by noon |
| Day 1–2 | Development (FE \+ BE) | Tasks 3–4 | Khoi, Nhan, Cuong, Minh | Execute simultaneously, based on shared schema |
| Day 2 | QA & Final Validation | Task 5 | Nhat, Vi | Review logic, layout, and email functionality |

**Frontend and backend work in parallel** after the UI handoff. QA runs immediately once a stable build is ready.

---

### 

### 

###  **Key Dependencies**

* Finalized registration schema for vendors

* Pre-approved email templates (Approve, Reject, Request Edit)

* JWT session validation and CSRF middleware

* Secure permissions for Admin role

* (Optional) Admin-facing action log or history trail

---

### **Recommendations & Notes**

* Use standardized ENUMs: `PENDING`, `APPROVED`, `REJECTED`, `REVISION_REQUESTED`

* Ensure all actions log timestamp, actor, and before/after state (for audit)

* Email service must handle delivery failure and provide resend options

* UI must clearly show success/error/loading states for every action

* Consider adding **filter/search by status** for future scalability

