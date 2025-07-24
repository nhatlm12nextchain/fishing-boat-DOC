### **CMS Feature: Usage Time and Seat Settings (Backend and QA)**

**Feature ID:** CMS-SEAT  
 **Target Duration:** 3 working days  
 **Total Estimated Hours:** 39  
 **Status:** Scheduled  
 **Dependencies:** CMS-SCHEDULE, RSV-FORM

**1\. User Story**  
 As an operator, I want the backend to automatically manage seat closing, integrate with the notification system, and ensure all seat and time configurations work correctly.

---

**Task Breakdown**

| No | Task Description | Role | Assigned To | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 8 | Backend API for schedule and notification | Backend | Cuong, Minh | 30 | Cron-based auto-closing, logging, seat status update |
| 9 | QA: test all combinations and resolutions | QA | Vi, Nhat | 9 | Test mobile and desktop edge cases, invalid states |

---

**Schedule Summary**

* Backend can begin in parallel with frontend (previous CMS-SEAT tasks)

* QA to validate across viewports, browser combinations, and invalid data

---

### **2\. CMS Feature: Ship Management**

**Feature ID:** CMS-BOAT  
 **Target Duration:** 3 working days  
 **Total Estimated Hours:** 10.5 (currently PM and Design only)  
 **Status:** Scheduled  
 **Dependencies:** BOAT-API, CMS-SEAT

**User Story**  
 As a shipping company, I want to manage ship profiles including name, type, status, and delete outdated records, with immediate UI feedback upon change.

---

**Task Breakdown**

| No | Task Description | Role | Assigned To | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define CRUD policy for ship data | PM | Nhat | 1.5 | Includes add, edit, delete logic, and status rules |
| 2 | Design UI for CRUD actions and notification | Design | Vi | 9 | Success indicators, status toggles, accessible form design |

---

**Notes for Next Phase**

* Add frontend and backend implementation tasks for CRUD, validation, and DB schema updates

* Include QA testing for add/edit/delete and mobile compatibility

