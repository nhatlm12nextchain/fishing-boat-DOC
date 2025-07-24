**PRODUCT REQUIREMENT DOCUMENT**

**"Modu-eui Bada" Fishing Boat Reservation Platform**

**Authors:** Minh Nhat Luong, Tuong Tran

---

### **Overview** 

#### **Background & References:**

* **WBS Document:** [Latest WBS](https://docs.google.com/spreadsheets/d/1yxKaClFUQE-lB_s6atj98uc5cfv_t5U6OXycQ2IZBd8/edit?usp=sharing)  
* **Reference Sites:**  
  * http://wooseong.thefishing.kr/  
  * https://www.sunsang24.com/  
* **Initial PRD Draft:** [View Here](https://docs.google.com/document/d/1j9Q6r0HF6l9NlA5z4HweOGkLcRJOR1GBXtaX4h_P6Pg/edit?usp=sharing)

  #### **Objectives:**

To build a Minimum Viable Product (MVP) web application that facilitates fishing boat bookings and services, while also providing robust management tools for admins and shipping companies. The core focus is to deliver essential features quickly, ensuring strong usability and scalability.

---

### **User Stories**

**For Users:**

* Register and login via email/password.  
* Receive personalized trip recommendations.  
* Manage personal profile and preferences.  
* Search and filter boat trips by criteria.  
* View detailed boat/trip information.  
* Book trips and complete secure payments.  
* View past/upcoming bookings.  
* Receive real-time booking status notifications.  
* Use the application on both desktop and mobile.

**For Shipping Companies:**

* Submit applications for membership.  
* Add, edit, and manage boats and trip schedules.  
* Approve or decline booking requests.  
* Receive notifications for user activity.  
* Access a dashboard with analytics, reviews, and schedules.  
* Upload content and deposit proof.

**For CMS/Admins:**

* Manage all user and company accounts.  
* Intervene in bookings and handle disputes.  
* Update platform content.  
* Generate reports and insights.  
* Approve boat and company submissions.  
  ---

  ### **Functional Requirements**

**User-Focused (MVP):**

* **Auth & Profile:** Secure registration, JWT-based login, password policies, and real-time validation.  
* **Search & Discovery:** Real-time filters with client/server-side caching.  
* **Boat Details:** Full descriptions, ratings, captain profiles, and trip specs.  
* **Booking System:** Calendar-based booking with secure payment integration and policy-bound edits.  
* **Notification System:** Real-time via email/SMS.  
* **Reviews:** Post-trip feedback with verified publishing.  
* **Responsive UX:** Fully mobile-friendly with accessible UI.

**Shipping Company (MVP):**

* **Application Process:** Submit required documents, admin review system.  
* **Boat Listings:** Add/manage boats, secure uploads.  
* **Calendar Management:** Time slots, real-time updates.  
* **Booking Control:** Approve/decline with reason, auto refunds.  
* **Reports & Deposits:** Upload reports and deposit slips, track admin approval.  
* **Dashboard:** Centralized view of activities.

**Admin Panel (MVP):**

* **Admin Dashboard:** Monitor activity, summary views.  
* **Account Management:** Review, deactivate, assist.  
* **Content/Dispute Management:** Manage TOS/FAQs, record dispute decisions.  
* **Approval Systems:** Handle new submissions and deposit proofs.  
  ---

  ### 

  ### 

### 

  ### **User Journey**

1. Visit the homepage, choose a role.  
2. Search and apply filters.  
3. Browse boat detail pages.  
4. Proceed with booking.  
5. Confirm booking and notify stakeholders.  
6. Shipping company approves/declines.  
7. Post-trip review submitted.  
   ---

   ### **Security & Performance**

* JWT \+ CSRF protection, password lockout after 5 failed attempts.  
* Secure data encryption, XSS-safe file uploads.  
* System response target: \<200ms, 99.5% uptime.  
* Caching and scheduler update strategies.  
* Optimized UX with skeleton loading and accessible markup.  
  ---

  ### **Success Metrics**

**User:**

* Weekly signups  
* Search-to-booking conversion  
* Satisfaction scores  
* Repeat bookings

**Business:**

* Monthly onboarded companies  
* Monthly bookings  
* Gross revenue & per booking metrics  
* Company churn rate

**Technical:**

* Uptime \>99.5%  
* Page load \<2s  
* Error rate \<1%  
* Notification success \>98%  
    
    
    
    
  ---

  ### **Tracking & QA Coverage**

* Registrations, searches, detailed views, bookings, cancellations.  
* Content uploads, reviews, admin actions.  
  ---

  ### **Technical Architecture**

| Component | Techology |
| ----- | :---- |
| Frontend (User) | NextJS |
| Frontend (Admin) | ReactJS |
| Backend | NodeJS |
| Database | PostgreSQL |
| Deployment (FE) | Vercel |
| Deployment (BE) | Render |

  ---

  ### **Scalability & Risks**

**Scalability:**

* MVP ready for 500+ users and companies  
* Load balancing, daily backups

**Challenges:**

* Double-booking prevention  
* Last-minute cancellations  
* Dispute resolution and fraud detection  
* Timely payouts

