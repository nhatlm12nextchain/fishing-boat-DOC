## **✅ MVP Feature Breakdown – CMS Features**

---

### **1\. Manual Approval of Shipping Company Deposit**

**Feature ID:** `ADM-SETTLE-MANUAL`  
 **Target Duration:** 2.5 working days  
 **Total Est. Hours:** 42  
 **Status:** Scheduled  
 **Dependencies:** `RSV-FORM`, `ADM-VEND-DETAIL`

#### **🎯 User Story**

As an **admin operator**, I need to **upload, verify, and approve/reject deposit slips** for manual transfers, so I can validate payments securely.

#### **🧩 Task Breakdown**

| \# | Task | Role | Owner(s) | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define deposit approval flow | PM | Tuong | 1.5 | Include logic for Approve/Reject \+ file handling |
| 2 | UI design: slip preview, buttons | Design | Vi | 4.5 | Responsive design with clear action states |
| 3 | Frontend: upload \+ actions | Frontend | Khoi, Nhan | 12 | CSRF-secure, toast feedback, image preview |
| 4 | Backend: update API \+ logging | Backend | Cuong, Minh | 18 | Transaction-safe updates, action logging |
| 5 | QA: upload & action scenarios | QA | Vi, Nhat | 6 | Test edge cases, layout responsiveness |

---

### **2\. Catch Report Registration**

**Feature ID:** `CMS-JOHANG`  
 **Target Duration:** 6 working days  
 **Total Est. Hours:** 76.5  
 **Status:** Scheduled  
 **Dependencies:** `JOHANG-API`, `CMS-STATS`

#### 

#### **🎯 User Story**

As a **shipping company**, I want to **upload catch reports** with images and metadata, schedule exposure, and track the published data efficiently.

#### **🧩 Task Breakdown**

| \# | Task | Role | Owner(s) | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define report data structure | PM | Tuong | 1.5 | Confirm policy for tagging, images, exposure |
| 2 | UI design: upload, tag, date | Design | Vi | 9 | Drag-and-drop upload, delete button, preview |
| 3 | Frontend: multi-upload UI | Frontend | Khoi, Nhan | 27 | Chunk upload, image preview, progress bar |
| 4 | Backend: S3 \+ cron exposure | Backend | Cuong, Minh | 30 | Schedule publish via cron, tag storage |
| 5 | QA: upload/publish/delete tests | QA | Vi, Nhat | 9 | End-to-end CRUD flow testing |

---

### **3\. Operation Date & Round Management**

**Feature ID:** `CMS-SCHEDULE`  
 **Target Duration:** 4 working days  
 **Total Est. Hours:** 58.5  
 **Status:** Scheduled  
 **Dependencies:** `RSV-FORM`, `RES-LIST`

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### **🎯 User Story**

As a **shipping company**, I want to manage my **operation calendar and rounds** with full control and real-time visibility.

#### **🧩 Task Breakdown**

| \# | Task | Role | Owner(s) | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define date/round policy | PM | Tuong | 1.5 | Define rules for add/edit/delete per ship |
| 2 | Calendar UI design | Design | Vi | 6 | Round badges, tooltips, status indicators |
| 3 | Frontend: calendar logic | Frontend | Khoi, Nhan | 27 | Debounce inputs, visual feedback, state sync |
| 4 | Backend: calendar CRUD | Backend | Cuong, Minh | 18 | Index for fast queries, atomic updates |
| 5 | QA: behavior \+ responsive test | QA | Tuong, Nhat | 6 | Handle edge cases, mobile UI, empty states |

---

### **4\. Usage Time and Seat Settings**

**Feature ID:** `CMS-SEAT`  
 **Target Duration:** 8 working days  
 **Total Est. Hours:** 27  
 **Status:** Scheduled  
 **Dependencies:** `CMS-SCHEDULE`, `RSV-FORM`

#### **🎯 User Story**

As an **operator**, I want to configure **usage time blocks and seat availability**, and see those reflected immediately in the reservation system.

#### **🧩 Task Breakdown**

| \# | Task | Role | Owner(s) | Est. Hours | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | Define seat/time structure | Frontend | Khoi, Nhan | 4 | UI logic for modular blocks |
| 2 | Build config UI | Frontend | Khoi, Nhan | 6 | Input validations for overlaps |
| 3 | Optimistic UI update logic | Frontend | Khoi, Nhan | 4 | Rollback on failure |
| 4 | API/WebSocket integration | Frontend | Khoi, Nhan | 5 | Live updates on seat availability |
| 5 | Toast notifications | Frontend | Khoi, Nhan | 2 | Success/error feedback |
| 6 | Cross-module testing | Frontend | Khoi, Nhan | 3 | Sync with reservation & calendar |
| 7 | Responsive polish | Frontend | Khoi, Nhan | 3 | Adjust layout for mobile/tablet |

