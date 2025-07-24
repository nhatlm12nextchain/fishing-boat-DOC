### **MVP Feature Specification – Search & Filter Components**

* **Module:** Search / Filter

* **Stage:** MVP

* **Priority:** High

* **Status:** Scheduled

* **Target Delivery:** 4 working days

* **Total Estimated Hours:** \~120 hours

---

### **Overview**

This module comprises three core user-interactive filters designed to enhance the search and discovery experience. Each component must deliver fast, accessible, and responsive interactions across both mobile and desktop environments:

* **Date Selection Calendar** (`SF-CALENDAR`)

* **Region Selection Popup** (`SF-REGION`)

* **Species Filter** (`SF-SPECIES`)

---

### **User Stories**

* As a **user**, I want to select only valid departure dates so I don’t encounter booking errors.

* As a **user**, I want the region filter to load quickly and clearly show my selected areas.

* As a **user**, I want to select multiple popular species for filtering without the page reloading.

* As an **operator**, I need control over departure time rules, region groupings, and monthly species popularity data.

---

### **Task Breakdown**

| No. | Component | Role | Est. Hours | Assigned To | Description |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Date Calendar | PM | 1.5 hrs | Nhat | Define departure restrictions (UTC+9, cutoff 30 mins pre-departure) |
| 2 | Date Calendar | Design | 6 hrs | Vi | UI design with inactive date styles and accessible color palette |
| 3 | Date Calendar | Frontend | 18 hrs | Khoi, Nhan | Build calendar with disabled past/invalid dates |
| 4 | Date Calendar | Backend | 12 hrs | Cuong, Minh | Validate date logic server-side and sync with timezone |
| 5 | Region Popup | PM | 1.5 hrs | Nhat | Define region groupings by ISO-3166-2 (city/county \+ nearby areas) |
| 6 | Region Popup | Design | 6 hrs | Vi | Design popup UI and region counter display (≤200ms response) |
| 7 | Region Popup | Frontend | 21 hrs | Khoi, Nhan | Dynamic region list, selection logic, loading spinner |
| 8 | Region Popup | Backend | 15 hrs | Cuong, Minh | Region API with real-time count aggregation |
| 9 | Species Filter | PM | 1.5 hrs | Nhat | Define popularity logic via monthly scheduler |
| 10 | Species Filter | Design | 7.5 hrs | Vi | UI design for multi-select buttons/checkboxes |
| 11 | Species Filter | Frontend | 18 hrs | Khoi, Nhan | Multi-select UI with 1-hour local cache |
| 12 | Species Filter | Backend | 12 hrs | Cuong, Minh | RRULE-based scheduler, optimized data queries |

---

### 

### 

### 

### **Parallel Work Plan (4 Working Days)**

| Block | Focus Area | Tasks Included | Team Members | Duration Estimate |
| ----- | ----- | ----- | ----- | ----- |
| A | Calendar Logic & UI | Tasks 1–4 | Vi, FE, BE | \~2 days (parallel) |
| B | Region Filter Module | Tasks 5–8 | All roles | \~3 days total effort |
| C | Species Filter Module | Tasks 9–12 | All roles | \~2.5–3 days total effort |
| D | QA & Integration Review | All Modules | Nhat, Vi (Day 4\) | \~6 hours final review |

---

### **Key Dependencies**

* Unified timezone configuration (UTC+9) for date validation

* Region data structure following ISO-3166-2 for city/county mapping

* Species ranking data updated monthly via backend scheduler

* Local client-side caching for region/species selections

* API endpoints for validation, region counts, and popularity queries

---

### **Additional Notes**

* All UI components must comply with accessibility standards (contrast ratio, keyboard navigation, ARIA roles).

* Region popup and species filters must respond within **200ms**, with fallback spinners for longer loads.

* Date selection must be strictly validated on the backend to prevent manipulation or timezone mismatches.

* Admin panel must support updates to species popularity, with backend auto-updates driven by cron scheduler.

* Final QA and integration testing is scheduled for **Day 4**, focusing on cross-filter interactions, invalid input handling, and network edge cases.