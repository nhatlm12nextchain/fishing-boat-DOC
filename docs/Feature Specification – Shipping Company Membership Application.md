### **MVP Feature Specification – Shipping Company Membership Application (OP-SIGNUP)**

* **Feature Name:** Shipping Company Membership Application

* **Feature ID:** OP-SIGNUP

* **Module:** Onboarding – Partner Registration

* **Stage:** MVP

* **Priority:** High

* **Status:** Scheduled

* **Target Delivery:** 2 working days

* **Estimated Total Effort:** \~72 hours

---

### **Goal**

Enable shipping companies to apply for platform membership by submitting detailed business information and required documentation through a structured form. Submissions will enter a **pending approval** workflow before gaining access to the system.

---

### **User Story**

As a shipping company representative, I want to apply for membership by submitting my business information and official documents so that I can be reviewed and approved before using the platform.

---

### 

### 

### 

### 

### **Acceptance Criteria**

* Form must collect the following:

  * Company Name

  * Business Registration Number

  * Representative Name

  * Contact Information

  * File Upload (e.g., Business Registration Certificate)

* File upload requirements:

  * Accepted formats: JPG, PNG, PDF

  * Mandatory upload for required documents

* Upon successful submission:

  * Account enters “Pending Approval” status

  * Access to platform features is restricted until approval

  * Admin is notified via CMS or back-office system

* The interface must support:

  * Responsive mobile layout

  * Clear inline validation for input errors, missing files, and duplicates

  * Disabled re-submission if application is already pending or approved

---

### **Task Breakdown**

| No. | Task Description | Role | Assigned To | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define form fields, validation, and approval logic | PM | Tuong | 3 hrs | Includes access control, approval logic |
| 2 | UI/UX Design: input form \+ document upload section | Design | Vi | 9 hrs | Prioritize usability for mobile and bulk input |
| 3 | Frontend Development: form, validation, upload | Frontend | Khoi, Nhan | 30 hrs | Includes all error states, redirect after submit |
| 4 | Backend Development: API, file storage, status logic | Backend | Cuong, Minh | 24 hrs | Handle secure file saving and status tracking |
| 5 | QA Testing: data validation, reapply scenarios | QA | Nhat, Vi | 6 hrs | Includes edge cases, errors, duplicate entries |

---

### **Parallel Work Plan**

| Block | Area | Tasks | Team | Est. Duration |
| ----- | ----- | ----- | ----- | ----- |
| A | Planning & UI Design | 1, 2 | Tuong, Vi | 4–5 hrs |
| B | Backend Development | 4 | Cuong, Minh | 6–8 hrs |
| C | Frontend Development | 3 | Khoi, Nhan | 10–12 hrs |
| D | QA & Review | 5 | Nhat, Vi | 4–6 hrs |

---

### **Technical Dependencies**

* Shipping company database schema

* File storage integration (e.g., AWS S3)

* CMS/Admin notification system

* Approval status logic (Pending → Approved/Rejected)

* File type and size validator

* Login restrictions for unapproved applications *(optional for MVP)*

---

