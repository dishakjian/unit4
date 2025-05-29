# KOMORAH
# Criterion A: Planning
## Problem Definition
(See evidence of Consultation in the Appendix)
Ms R is the Head of Pastoral at a diverse international boarding school with over 200 students. Her role involves managing student movement, residential life, and wellbeing. The school uses Orah, a commercial tracking platform, but Ms R finds it inefficient and misaligned with the school’s needs. Its interface is unintuitive, and movement requests often fail due to buggy approvals, unclear steps, or missing notifications. Students become frustrated and stop submitting leave forms. Staff waste time chasing sign-ins due to the lack of curfew alerts. Automation regularly breaks: check-ins don’t update, curfew alerts fail, and emergency rolls arrive late or not at all. Staff can’t prioritize high-risk students, leading to manual double-checking and reduced efficiency.
Orah’s wellbeing module is underdeveloped, lacking guided reflections, counselling calendars, or personalized insights. It presents raw data without trends, preventing early intervention. Ms R cannot track patterns in wellbeing. Parents also struggle with the system’s unintuitiveness and language, making communication harder.
Another issue is the return time on passes: students aren’t signed in automatically at that time, making the field pointless. Additionally, rejected passes must be completely redone instead of being edited, wasting student time and discouraging use.
While Outdoor Education and other school trips are common, staff can’t directly take students on passes. This causes friction, inconsistent tracking, and added admin and student burdens, which affect student safety and engagement.
While Orah is the primary system, Ms R has also considered Komodo, a wellbeing-centered platform. Komodo allows for emotional check-ins and trends but lacks the logistical features needed for daily movement tracking.
## Proposed Solution
To meet the school’s logistical and wellbeing needs while addressing the daily frustrations voiced by Ms R, I proposed building a web-based application. Unlike desktop apps, a web application is accessible from any device, making it ideal for an international school community where students, staff, and parents log in from various locations. Web apps offer centralized access, real-time updates, and cross-platform compatibility, which improves communication and usability across roles and time zones. 
To address both the logistical and wellbeing gaps, I proposed to create an integrated system that combines the movement management features of Orah with the mental health and trends analysis capabilities inspired by Komodo. 
I proposed using Python for development due to its readable syntax, rapid development capabilities, and strong support for scalability. Compared to Java or JavaScript, Python allows faster prototyping and easier maintenance, crucial in a high-demand school setting.
For the backend, I proposed Flask, a lightweight Python framework. Flask is modular and flexible, allowing features to be built around the workflows of Ms R and her team. Unlike Django, which enforces a rigid structure and comes with prebuilt modules that may not align with the school’s needs, Flask offers full control over each feature’s design.
I proposed using SQLite as the database as it requires no separate server and integrates seamlessly with Flask. This reduces setup time, allows faster testing, and enables real-world feedback from staff and students without unnecessary technical barriers unlike PostgreSQL or My SQL .

## Success Criteria 
(See evidence of Approval in the Appendix)
### 1. Leave Request & Movement Management System
- Students can request overnight, non-local, and local trips.
- Supports shared leave and chaperone-initiated passes.
- Parents can approve or reject in real time.
- Curfew alerts and sign-in tracking.

**Issues Tackled:**  
> “Movement requests often fail due to unclear steps, buggy approval systems, or missing notifications.”  
> “Staff waste time chasing sign-ins due to the lack of curfew alerts.”  
> “Students get frustrated and stop submitting leave forms entirely.”  
> “While Outdoor Education and other school trips are common, staff can’t directly take students on passes. This causes friction, inconsistent tracking, and added admin and student burdens.”  
> “Rejected passes must be completely redone instead of being edited, wasting student time and discouraging use.”  
> “The return time on passes: students aren’t signed in automatically at that time, making the field pointless.”

---

### 2. Automated Curfew and Attendance Alerts
Automated reminders and alerts will notify students and staff when a student misses curfew or fails to sign in. Emergency roll calls can be triggered instantly with live updates.

**Issues Tackled:**  
> “Alerts don’t trigger when students miss curfew, and the system often lags or glitches during high-traffic times.”  
> “Emergency roll notifications are sent late or not at all, leaving staff scrambling to ensure everyone's safety.”  
> “Staff waste time chasing sign-ins due to the lack of curfew alerts.”

---

### 3. Weekly Wellness Check-Ins and Mood Heatmaps
Students will complete brief weekly wellbeing surveys. Data will be processed into visual graphs for counselors and staff, identifying campus-wide patterns in stress, anxiety, or homesickness.

**Issues Tackled:**  
> “Ms R cannot track patterns in wellbeing.”  
> “Without meaningful input or analysis, the system fails to support early intervention, and vulnerable students are easily overlooked.”

---

### 4. Counselor & Staff Dashboards
- Counselors see mood trends, student reflections, and session logs.
- Staff create trip-specific passes and manage group leave easily.

**Issues Tackled:**  
> “Staff can’t prioritize high-risk students, leading to manual double-checking and reduced efficiency.”  
> “Orah’s wellbeing module is underdeveloped, lacking guided reflections, counselling calendars...”  
> “Staff can’t directly take students on passes... which affect student safety and engagement.”

---

### 5. Wellness Resource Hub and Counseling Appointments
- Students complete weekly mood check-ins with stress tags and optional reflections.
- They can book counselling or learning support sessions.
- A wellness resource library and in-app reminders encourage self-care habits.

**Issues Tackled:**  
> “Orah’s wellbeing module is underdeveloped, lacking guided reflections, counselling calendars, or personalized insights.”  
> “It presents raw data without trends, preventing early intervention.”  
> “Ms R cannot track patterns in wellbeing.” 

---

### 6. Secure Multi-Role Login System
A secure authentication system will be developed where students, staff, counselors, and parents have distinct access levels and permissions. Each user will only access functionalities relevant to their role, protecting sensitive information and reducing user confusion.

**Issues Tackled:**  
> “The app’s interface is unintuitive for both students and staff.”  
> “Movement requests often fail due to unclear steps, buggy approval systems, or missing notifications.”  
> “Ms R finds [Orah] inefficient and misaligned with the school’s needs. Its interface is unintuitive...”  
> “Parents also struggle with the system’s unintuitiveness and language, making communication harder.”

---

### 7. Multi-Language Parent Interface
Parents can select their preferred language to receive notifications, leave request updates, and system alerts, improving inclusivity for non-English speaking families.

**Issues Tackled:**  
> “Parents also struggle with the system’s unintuitiveness and language, making communication harder.”

# Criterion B: Design

## Record of Tasks
| Task No. | Planned Action                                                    | Planned Outcome                                                                                                         | Time Estimate | Target Completion Date | Criterion |
|----------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|---------------|-------------------------|-----------|
| 1        | **Planning: Initial consultation with client**                     | Documented inefficiencies (e.g., buggy approvals, missing alerts, poor wellbeing tracking)                              | 30 min        | 17 Apr                  | A         |
| 2        | **Planning: Draft scenario document**                             | Clear justification for project (linked to Appendix)                                                                     | 1 hr          | 18 Apr                  | A         |
| 3        | **Planning: Define tech stack (Flask/SQLite)**                    | 250-word rationale for tech stack (accessibility, real-time updates, scalability)                                        | 1 hr          | 22 Apr                  | A         |
| 4        | **Planning: Finalize success criteria**                           | Criteria mapped to Orah’s flaws (e.g., "Auto-sign-in at return time" vs. Orah’s manual process)                          | 1 hr          | 28 Apr                  | A         |
| 5        | **Planning: Secure client sign-off**                              | Signed approval form (Appendix evidence)                                                                                 | 30 min        | 29 Apr                  | A         |
| 6        | **Design: Create low-fidelity wireframes**                        | Visualized UI flow for dashboards (linked in Appendix)                                                                   | 2 hr          | 1 May                   | B         |
| 7        | **Design: Model ER diagram**                                      | Tables for `Users`, `LeaveRequests`, `MoodLogs` with relationships (Appendix)                                           | 1.5 hr        | 2 May                   | B         |
| 8        | **Design: Draft UML for backend logic**                          | Blueprints for auth, leave requests, alerts (Appendix)                                                                  | 2 hr          | 3 May                   | B         |
| 9        | **Design: Map leave approval/curfew flowchart**                   | Visualized steps for request submission → parent/staff approval → auto-sign-in/curfew checks                            | 2 hr          | 3 May                   | B         |
| 10       | **Design: Develop test plan**                                     | Tests aligned to success criteria (e.g., "Curfew alerts fire within 5 mins of missed sign-in")                           | 1 hr          | 3 May                   | B         |
| 11       | **Development: Set up Flask/SQLite boilerplate**                  | Scaffolded `auth`, `student`, `staff`, `parent` modules                                                                 | 1 hr          | 4 May                   | C         |
| 12       | **Development: Code role-based authentication (JWT)**             | Secure login with session management                                                                                    | 2 hr          | 5 May                   | C         |
| 13       | **Development: Implement multi-role access control**              | Decorators to restrict routes (e.g., parents can’t access staff dashboards)                                             | 2 hr          | 6 May                   | C         |
| 14       | **Development: Build leave request form**                         | Supports local/OEd/overnight trips + parent auto-notify                                                                 | 3 hr          | 7 May                   | C         |
| 15       | **Development: Develop staff dashboard**                          | View pending requests, trigger rolls, filter high-risk students                                                        | 2 hr          | 8 May                   | C         |
| 16       | **Development: Define SQLite models (SQLAlchemy)**                | Defined `User`, `LeaveRequest`, `MoodLog`, `Notification` classes with CRUD methods                                    | 2 hr          | 8 May                   | C         |
| 17       | **Development: Code parent dashboard**                            | Approve/reject requests, view history, select language (EN/JP/KR)                                                      | 2 hr          | 9 May                   | C         |
| 18       | **Development: Build notification system**                        | Alerts for approvals, curfew violations, missed check-ins                                                              | 2 hr          | 10 May                  | C         |
| 19       | **Development: Implement automated curfew checks**                | Scans DB at curfew times; flags missing students                                                                        | 2.5 hr        | 11 May                  | C         |
| 20       | **Development: Code group leave logic**                           | Staff create passes for multiple students; auto-sign-out on trip start                                                 | 2 hr          | 12 May                  | C         |
| 21       | **Development: Build wellbeing check-in form**                    | Weekly survey with mood/energy levels; data stored for trends                                                          | 3 hr          | 13 May                  | C         |
| 22       | **Development: Develop counselor dashboard**                      | Visualizations of campus-wide stress/anxiety patterns; filter by dorm/gender                                           | 2 hr          | 14 May                  | C         |
| 23       | **Development: Create wellness resource hub**                     | Curated articles/videos on mental health; linked to student check-in data                                               | 1.5 hr        | 15 May                  | C         |
| 24       | **Development: Implement counseling booking system**              | Students request sessions; counselors manage calendar                                                                   | 2 hr          | 16 May                  | C         |
| 25       | **Development: Integrate multi-language UI**                      | Parents toggle EN/JP/KR for notifications/dashboards                                                                    | 1.5 hr        | 17 May                  | C         |
| 26       | **Testing: Run unit tests for login/auth**                        | Verified role restrictions (e.g., parent can’t access staff routes)                                                     | 1 hr          | 18 May                  | D         |
| 27       | **Testing: Execute integration tests for leave flow**             | Validated parent approval → status update → student notification                                                        | 1.5 hr        | 19 May                  | D         |
| 28       | **Testing: Validate curfew alert triggers**                       | Confirmed alerts fire when students miss curfew; tested edge cases (e.g., no internet)                                 | 1 hr          | 20 May                  | D         |
| 29       | **Testing: Conduct client UAT session**                           | Feedback on UI intuitiveness (e.g., "Language toggle is clear")                                                         | 1.5 hr        | 21 May                  | D         |
| 30       | **Testing: Debug auto-sign-in logic**                             | Patched issue where attendance wasn’t updated automatically (vs. Orah’s flaw)                                          | 3 hr          | 22 May                  | D         |
| 31       | **Testing: Fix rejected pass editing**                            | Enabled students to edit rejected requests without resubmitting from scratch                                           | 2 hr          | 22 May                  | D         |
