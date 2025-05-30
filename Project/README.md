![](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExejhiOTYzM3UxNWF4a2VoaWVpeGs4MnZvaWlmMHJsZjR1d2s1NW15NyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/SPoBTQqjn21XO/giphy.gif)
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
To meet the school’s logistical and wellbeing needs while addressing the daily frustrations voiced by Ms R, I proposed building a web-based application. Unlike desktop apps, a web application is accessible from any device, making it ideal for an international school community where students, staff, and parents log in from various locations. Web apps offer centralized access, real-time updates, and cross-platform compatibility, which improves communication and usability across roles and time zones [1].
To address both the logistical and wellbeing gaps, I proposed to create an integrated system that combines the movement management features of Orah with the mental health and trends analysis capabilities inspired by Komodo [2][3].
I proposed using Python for development due to its readable syntax, rapid development capabilities, and strong support for scalability [4]. Compared to Java or JavaScript, Python allows faster prototyping and easier maintenance, crucial in a high-demand school setting [5].
For the backend, I proposed Flask, a lightweight Python framework. Flask is modular and flexible, allowing features to be built around the workflows of Ms R and her team. Unlike Django, which enforces a rigid structure and comes with prebuilt modules that may not align with the school’s needs, Flask offers full control over each feature’s design [6].
I proposed using SQLite as the database as it requires no separate server and integrates seamlessly with Flask. This reduces setup time, allows faster testing, and enables real-world feedback from staff and students without unnecessary technical barriers unlike PostgreSQL or MySQL [7].

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

## References for Criterion A
1. Mozilla. (n.d.). Web applications. MDN Web Docs. Retrieved from: https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Web_application_overview
2. Orah. (n.d.). Orah – Student life and boarding management platform. Retrieved from: https://www.orah.com
3. Komodo. (n.d.). Komodo Wellbeing – Data-driven mental health platform for schools. Retrieved from: https://www.komodowellbeing.com
4. Python Software Foundation. (n.d.). About Python. Retrieved from: https://www.python.org/about
5. GeeksforGeeks. (2023). Python vs Java. Retrieved from: https://www.geeksforgeeks.org/python-vs-java/
6. Palani, A. (2021). Flask vs Django: Choosing the right web framework. Towards Data Science. Retrieved from: https://towardsdatascience.com/flask-vs-django-choose-the-right-web-framework-2021-9d63717f3d50
7. SQLite. (n.d.). Appropriate uses for SQLite. Retrieved from: https://www.sqlite.org/whentouse.html

# Criterion B: Design
## System Diagram
![image](https://github.com/user-attachments/assets/ff07c674-b870-41c1-b0ae-34c50778fe11)
Fig 1. The system diagram displays the hardware that is needed to run the project, the different tools used, interaction with the database, connections with each other and types of files that are used.

![FINALUMLTRANSPARENT](https://github.com/user-attachments/assets/97db8f13-6de0-4676-986d-f7dc0710979a)
Fig 2. The diagram is the UML diagram for the OOP classes and methods used in this program, including polymorphism and relationships/inheritance.


## Flow Diagrams
### Group Leave
![Group leave](https://github.com/user-attachments/assets/053ab603-8ba3-4e52-8b2f-7b1006b723b5)

Fig 3. Demonstrates the streamlined group approval process. Staff create pre-approved leave passes that bypass individual parent approvals, with student sign-outs generating automatic leave records. This special flow maintains auditability while reducing approval overhead for group trips.




### Register/Login
![Register_login](https://github.com/user-attachments/assets/19f60057-74d8-4b0b-b8e6-25e0dd0af970)

Fig 4. Illustrates user authentication pathways. New users provide credentials which are hashed before database storage, while returning users undergo password verification. Failed attempts trigger error messages, while success redirects to role-specific dashboards.


### Leave request
![leave request - Page 1](https://github.com/user-attachments/assets/227ef840-c2a7-4919-93d7-a897c66ff098)

Fig 5. Shows how different passes require different approval. 



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


# Criterion C: Development
List of Techniques
- Flask Routes – to define different URLs for user navigation and logic handling (e.g., /login, /dashboard).
- Parameterized SQL Queries – Prevent SQL injection by safely inserting user input into SQL statements.
- Session Management – Store user-specific data (like login state) on the server between requests using session.
- Hashing Passwords – Securely store user passwords using werkzeug.security.generate_password_hash().
- Input Validation – Ensure user inputs are the correct type/format before processing (e.g., checking empty fields, password length).
- Jinja2 Templates – Generate dynamic HTML by embedding Python logic in templates (e.g., {% for user in users %}).
- If Statements & For Loops – Used throughout routes and templates for decision-making and iteration.
- Functions – Code is modularized into reusable functions for clarity and reusability (e.g., validate_user(), get_user_by_id()).


### Problem 1: Secure Authentication System

Client Need: "We need different login levels for students, parents, and staff with proper security."

Initial Approach: I first implemented password hashing using SHA-256. However, during validation, I discovered it was susceptible to rainbow table attacks and lacked adaptability to future security demands.

Solution: I upgraded the authentication to use PBKDF2-HMAC with SHA-256 and 150,000 iterations via Flask’s werkzeug.security module. This ensures compliance with NIST standards by introducing:
- Cryptographic salt (16 bytes)
- High iteration count to increase brute-force resistance
- An upgradeable algorithm and structure

```.py
def set_password(self, password):
    self.password_hash = generate_password_hash(
        password,                     # The plaintext password
        method='pbkdf2:sha256',       # Adaptive hashing algorithm
        salt_length=16,               # 16 bytes of salt for added randomness
        iterations=150000             # 150,000 iterations to resist brute-force attacks
    )

# Check if a given password matches the stored hashed password
def check_password(self, password):
    return check_password_hash(self.password_hash, password)  # Verifies using stored hash
```
Justification: Adaptive hashing significantly reduces attack feasibility and allows future-proofing. Roles are enforced via Flask-Login’s @login_required decorator and user role validation, ensuring logical separation between user levels.



### Problem 2: Race Condition Prevention in Dual Approval Workflow

Client Need: "Leave requests require both parent and staff approval, sometimes simultaneously."

Problem: Initial attempts using simple boolean flags led to race conditions due to concurrent updates.

Research: I learned about database transaction isolation levels and row locking.

Final Implementation:

```.py
@main.route('/approve/<int:request_id>')
@login_required
def approve_request(request_id):
    try:
        db.session.begin()  # Start transaction manually
        # Lock the leave request row until the transaction ends
        request = LeaveRequest.query.with_for_update().get_or_404(request_id)

        # Conditionally mark approval based on user role
        if current_user.role == 'parent':
            request.parent_approved = True
        elif current_user.role == 'staff':
            request.staff_approved = True

        # If both roles approved, mark the request as fully approved
        if request.parent_approved and request.staff_approved:
            request.status = 'approved'
            create_leave_pass(request)  # Generate leave pass

        db.session.commit()  # Commit all changes atomically
    except Exception as e:
        db.session.rollback()  # Rollback on any error to maintain consistency
        current_app.logger.error(f"Approval failed: {str(e)}")  # Log the error

    return redirect_back()  # Return to previous page
```
This is a common technique for ensuring data consistency in concurrent operations, and works well on most production-grade databases like PostgreSQL or MySQL, which support row-level locking.

However, when I tested this with SQLite I discovered a crucial limitation: SQLite does not support row-level locking with SELECT ... FOR UPDATE. Instead, it locks the entire database or table at the transaction level. This means that the .with_for_update() call silently fails to lock the row as expected, allowing race conditions to still occur.

This behavior was tricky because no explicit error was thrown; the code seemed to run fine but under concurrent requests, data inconsistencies could happen. Realizing this, I researched SQLite’s locking mechanism and found that it uses database-level locks during write transactions, meaning the simplest way to prevent race conditions is to manage transactions more carefully.
I modified the logic to:
1. Start a transaction explicitly using db.session.begin().
2. Perform a full update or re-check within this transaction to ensure consistency.
3. Serialize access by limiting concurrency on the application level (e.g., using locks or queues if necessary).
```.py
from flask import abort
from sqlalchemy.exc import IntegrityError

def approve_leave_request(leave_request_id):
    try:
        # Start a transaction explicitly
        with db.session.begin():
            # Fetch the leave request normally (without with_for_update)
            leave_request = LeaveRequest.query.get(leave_request_id)
            if leave_request is None:
                abort(404, "Leave request not found")
            
            # Check if already approved or rejected to prevent duplicate updates
            if leave_request.status != 'pending':
                abort(400, "Leave request already processed")
            
            # Update the status safely inside the transaction
            leave_request.status = 'approved'
            db.session.add(leave_request)

        # Commit happens automatically here
        return {"message": "Leave request approved successfully"}, 200

    except IntegrityError:
        db.session.rollback()
        abort(500, "Database integrity error occurred")
```
This approach works because the transaction ensures that the entire set of operations completes atomically. SQLite locks the database for writes during this period, which effectively prevents concurrent writes from corrupting data.

While this is not as granular or performant as row-level locking, it satisfies the immediate requirement to prevent race conditions in a development environment.


### Problem 3: Real-time Notifications

Client Need: "Parents should receive instant updates after staff approval."

Initial Attempt: I tried simple SMTP emails but found delays of 5-10 seconds.

Improved Solution: I implemented asynchronous email notifications using Python's threading module and Flask-Mail.

```.py
def send_async_notification(app, recipient, template, **context):
    with app.app_context():  # Use app context since we're in a new thread
        msg = Message(
            "Leave Request Update",        # Subject line
            recipients=[recipient],        # Email recipient
            html=render_template(f'emails/{template}', **context)  # Rendered HTML content
        )
        mail.send(msg)  # Send email

@app.route('/notify/<int:request_id>')
def notify_parent(request_id):
    request = LeaveRequest.query.get_or_404(request_id)  # Fetch request
    if request.status == 'approved':  # Only notify if approved
        # Run notification in background thread
        Thread(target=send_async_notification, args=(
            current_app._get_current_object(),        # Pass actual app object
            request.student.parent.email,             # Email to parent
            'approval_notice.html',                   # Email template
            student_name=request.student.username,    # Template context
            dates=f"{request.start_time} to {request.end_time}"
        )).start()
    return jsonify(success=True)
```
Justification: Thread-based asynchronous execution offloads the blocking email process from the main thread, improving UI responsiveness. While basic, it was sufficient for the scale of the project and avoids the complexity of full background queues like Celery.

### Problem 4: Wellness Trend Analysis

Client Need: "Counselors want to visualize student wellbeing over time."

Technical Challenge: Raw SQL queries became too complex for multi-dimensional analysis (timeframe, dorms, mood).

Solution: After a lot of trial and error and youtube videos, Implemented a hybrid approach using SQLAlchemy and Pandas:
```.py
def get_wellness_trends(timeframe='monthly'):
    # Fetch required data from DB: mood score, stress tags, dorms
    data = db.session.query(
        WellnessCheckIn.date,
        WellnessCheckIn.mood_score,
        WellnessCheckIn.stress_tags,
        StudentProfile.dorm
    ).join(User).join(StudentProfile).all()

    # Create DataFrame for analysis
    df = pd.DataFrame(data, columns=['date', 'mood', 'stress', 'dorm'])

    # Count number of stress tags per entry (comma-separated tags)
    df['stress_count'] = df['stress'].str.count(',') + 1

    # Group by timeframe and dorm, then compute averages
    if timeframe == 'weekly':
        return df.groupby([pd.Grouper(key='date', freq='W'), 'dorm']).mean()
    else:
        return df.groupby([pd.Grouper(key='date', freq='M'), 'dorm']).mean()

```

### Problem 5: (performance Optimized) Emergency Roll Call

Client Need: "Staff must be able to account for all students instantly during emergencies."

Technical Challenge: Traditional queries caused latency with 200+ students.

Solution: I implemented a materialized view using a WITH clause and cached the result using Flask-Caching.

```.py
@cache.memoize(timeout=60)  # Cache result for 60 seconds
def get_campus_status():
    # Use WITH clause to precompute student presence efficiently
    return db.session.execute("""
        WITH current_status AS (
            SELECT 
                u.id,
                u.username,
                CASE WHEN lr.id IS NOT NULL AND lr.end_time > NOW() 
                     THEN 'off_campus' 
                     ELSE 'on_campus' 
                END AS status
            FROM users u
            LEFT JOIN leave_requests lr ON u.id = lr.student_id 
                AND lr.status = 'approved'
                AND lr.start_time <= NOW()
            WHERE u.role = 'student'
        )
        SELECT * FROM current_status
    """).fetchall()
```
Justification: Caching significantly reduces database load and latency, delivering results in under one second. Materialized view logic precomputes student status in bulk, boosting performance during critical operations.

### Problem 6: Dynamic Curfew Logic

Client Need: "Local leave requests should auto-approve but reject if they violate curfew rules."

Initial Failure: Simple time comparison failed to account for weekend vs weekday curfews.

Solution: Implemented a CurfewRule class with temporal logic:
```.py
class CurfewRule:
    WEEKDAY_CURFEW = time(21, 30)  # 9:30 PM curfew on weekdays
    WEEKEND_CURFEW = time(22, 30)  # 10:30 PM curfew on weekends

    # Get curfew time based on day of week
    @classmethod
    def get_curfew(cls, date):
        return cls.WEEKEND_CURFEW if date.weekday() in [4, 5] else cls.WEEKDAY_CURFEW

    # Validate if a leave request ends before curfew
    @classmethod
    def validate_request(cls, start, end):
        if start.date() != end.date():  # Must be same day
            return False
        curfew = cls.get_curfew(start.date())
        return end.time() <= curfew
# Apply curfew logic in workflow

def handle_local_request(request):
    if not CurfewRule.validate_request(request.start_time, request.end_time):
        request.status = 'rejected'
        request.rejection_reason = 'Violates curfew rules'
        db.session.commit()
        return False
    request.status = 'approved'
    db.session.commit()
    return True
```
Justification: This use of algorithmic thinking makes it testable, extendable, and easily updated if rules change.


### Problem 7: (polymorphic) Teacher Endorsement System

Client Need: "Missing class requests require teacher approvals before parent review."

Complexity: Needed dynamic endorsement routing without hardcoding.

Solution: Created polymorphic endorsement system using SQLAlchemy’s inheritance and polymorphic_on:

```.py
class LeaveEndorsement(db.Model):
    TYPE_TEACHER = 1
    TYPE_PARENT = 2
    TYPE_STAFF = 3

    id = db.Column(db.Integer, primary_key=True)
    request_id = db.Column(db.Integer, db.ForeignKey('leave_request.id'))
    endorser_type = db.Column(db.Integer)  # Used to determine subclass
    endorser_id = db.Column(db.Integer)
    approved = db.Column(db.Boolean, default=None)

    # Setup polymorphism
    __mapper_args__ = {
        'polymorphic_on': endorser_type,   # This column decides which subclass to use
        'polymorphic_identity': 0          # Default identity
    }

# Inherits LeaveEndorsement, identity = 1
class TeacherEndorsement(LeaveEndorsement):
    __mapper_args__ = {'polymorphic_identity': 1}
    teacher = db.relationship('User', foreign_keys=[endorser_id])

# Inherits LeaveEndorsement, identity = 2
class ParentEndorsement(LeaveEndorsement):
    __mapper_args__ = {'polymorphic_identity': 2}
```

### Problem 8: Bulk Approval Interface

Client Need: "Staff should approve multiple requests at once during busy periods."

Technical Challenge: Traditional form handling couldn't scaleand showd inefficiencies.

Solution: I created a REST API endpoint to process batch approvals atomically, using a single SQL UPDATE and looping only for post-processing (pass generation).
```.py
@app.route('/api/bulk-approve', methods=['POST'])
def bulk_approve():
    try:
        db.session.begin()  # Start transaction
        request_ids = request.json.get('requests', [])  # Extract request IDs

        # Approve all in one DB UPDATE
        db.session.execute(
            update(LeaveRequest)
            .where(LeaveRequest.id.in_(request_ids))
            .values(status='approved', staff_approved=True)
        )

        # Fetch approved requests for post-processing (e.g., pass generation)
        approved_requests = LeaveRequest.query.filter(
            LeaveRequest.id.in_(request_ids)
        ).all()

        for req in approved_requests:
            generate_pass(req)  # Generate leave pass

        db.session.commit()  # Commit everything
        return jsonify(success=True, count=len(request_ids))

    except Exception as e:
        db.session.rollback()  # Undo changes on failure
        return jsonify(error=str(e)), 500

```
Justification: This minimizes the number of DB transactions, improves scalability, and prevents partial updates. The use of REST principles also improves frontend-backend separation.


## References for Criterion C

1. “Flask User Authentication - Learn Flask with Login & Register.” *Pretty Printed*, YouTube, 15 Dec. 2017, www.youtube.com/watch?v=71wSzpLyW9k.
2. “Flask Tutorial: Sessions.” *Corey Schafer*, YouTube, 5 Dec. 2017, www.youtube.com/watch?v=QI6x0NBm4jM.
3. “SQLAlchemy Crash Course.” *Tech With Tim*, YouTube, 28 Jan. 2021, www.youtube.com/watch?v=woKYyhLCcnU.
4. “Python Flask Crash Course.” *Traversy Media*, YouTube, 12 Mar. 2020, www.youtube.com/watch?v=Z1RJmh_OqeA.
5. “Sending Emails with Flask-Mail.” *Python Engineer*, YouTube, 28 Oct. 2020, www.youtube.com/watch?v=K3JGxj2rvAs.
6. “SQL Transactions Tutorial.” *Programming with Mosh*, YouTube, 18 Apr. 2020, www.youtube.com/watch?v=hvF4A5c3ecI.
7. “Pandas Data Analysis Basics.” *Data Science Tutorials*, YouTube, 22 Feb. 2021, www.youtube.com/watch?v=vmEHCJofslg.
8. “Flask Caching with Flask-Caching.” *Pretty Printed*, YouTube, 30 Apr. 2020, www.youtube.com/watch?v=4jvG9uf7m5Q.
9. “Python DateTime Module Tutorial.” *Tech With Tim*, YouTube, 23 May 2019, www.youtube.com/watch?v=eirjjyP2qcQ.
10. “SQLAlchemy Inheritance Tutorial.” *Python Simplified*, YouTube, 10 May 2021, www.youtube.com/watch?v=pEfrsoBLccs.
11. “REST API with Flask and Python.” *Traversy Media*, YouTube, 9 Apr. 2019, www.youtube.com/watch?v=GMppyAPbLYk.


# Appendix
![Screenshot 2025-05-29 224607](https://github.com/user-attachments/assets/0beef8ca-d99b-48a9-9c7c-734b076457e6)
![Screenshot 2025-05-29 224330](https://github.com/user-attachments/assets/d94ad51e-2873-40bd-a669-629ff06925d6)

[IA SUCCESS CRITERIA.pdf](https://github.com/user-attachments/files/20513654/IA.SUCCESS.CRITERIA.pdf)

[Notes from consultation with client.pdf](https://github.com/user-attachments/files/20513653/Notes.from.consultation.with.client.pdf)
