# E-Learning System - Complete Project Documentation

> 🌐 **Live Website**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)
> 
> 📧 **Contact**: If you are interested in this project or have any questions, please contact me via email: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Project Structure](#project-structure)
3. [Student Pages](#student-pages)
4. [Instructor Pages](#instructor-pages)
5. [Admin Pages](#admin-pages)
6. [Authentication System](#authentication-system)
7. [Learning Path System](#learning-path-system)
8. [Deployment](#deployment)
9. [Development](#development)
10. [Important Notes](#important-notes)
11. [Support & Maintenance](#support--maintenance)
12. [Contact & Additional Documentation](#contact--additional-documentation)

---

## Project Overview

**E-Learning System** is an online learning platform specifically designed for integrated learning systems in manufacturing environments. The system supports various user roles with specific features for each role.

🌐 **Access the application**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)

### Key Features

- ✅ Course-based learning system
- ✅ Structured Learning Path based on cluster and job level
- ✅ Assignment and grading management
- ✅ Discussion forum
- ✅ SOP (Standard Operating Procedure) library
- ✅ Training schedule
- ✅ Analytics and reporting
- ✅ Multi-level certification system
- ✅ Audit trail for activity tracking

### Target Users

1. **Student** - Employees participating in training
2. **Instructor** - Teachers managing courses
3. **Admin** - System administrator
4. **Manager** - Managers monitoring teams
5. **HRD** - HR division managing training
6. **Supervisor** - Supervisors monitoring teams

---

## Project Structure

The project uses a standard React structure with components organized by role (admin, instructor, student), layout, and shared components. Deployment configuration uses Docker and Caddy for reverse proxy.

---

## Student Pages

### 1. Student Dashboard (`/dashboard`)

**Features:**
- **Welcome Section** with user information:
  - Cluster (Operator, Leader, Supervisor, Manager, Expatriate)
  - Job Level (Basic, Intermediate, Advanced)
  - Certification Level (1-5)
  - Overall Learning Path progress

- **Quick Stats Cards:**
  - Active Training
  - Training Hours
  - Certification Level
  - Average Score

- **My Learning Path Section:**
  - Displays assigned Learning Path
  - Overall progress
  - Progress per track (Technical, Culture, Productivity)
  - Completion status per track

- **My Courses Table:**
  - List of enrolled courses
  - Progress per course
  - Status (Not Started, In Progress, Completed)
  - Action to continue/start course

- **Recent Activity:**
  - Latest notifications
  - Learning activities

- **Quick Actions:**
  - View Schedule
  - Discussion Forum
  - My Certificates

### 2. Course List (`/courses`)

**Features:**
- Grid/list view of courses
- Filter by category
- Search courses
- Course information:
  - Thumbnail
  - Title and description
  - Instructor
  - Rating
  - Number of enrolled students
  - Duration
- Enroll in courses

### 3. Course Detail (`/courses/:courseId`)

**Features:**
- Complete course information
- List of modules and lessons
- Progress tracking per lesson
- Video player for video lessons
- Document viewer for document lessons
- Quiz interface
- Assignment submission
- Navigation between lessons

### 4. Assignments (`/assignments`)

**Features:**
- List of all assignments
- Filter by:
  - Status (Not Started, In Progress, Completed, Late)
  - Course
  - Deadline
- Assignment information:
  - Title and description
  - Related course
  - Deadline
  - Submission status
  - Score (if graded)
- Submit assignment with attachment
- View feedback from instructor

### 5. Grades (`/grades`)

**Features:**
- List of grades from all courses
- Grade breakdown by:
  - Assignment
  - Quiz
  - Final exam
- Grade progress chart
- Overall average grade
- Obtained certificates
- Download certificates

### 6. Schedule (`/schedule`)

**Features:**
- Calendar view of training schedule
- List view of schedule
- Filter by:
  - Date
  - Training type (Classroom, OJT, Practical)
  - Status (Scheduled, Ongoing, Completed)
- Schedule details:
  - Time and location
  - Instructor
  - Training materials
  - Participant list
- Enroll in training
- Attendance

### 7. Discussion Forum (`/forum`)

**Features:**
- List of discussion threads per course
- Create new thread
- Reply to thread
- Search and filter threads
- Like/upvote posts
- Reply notifications
- Mark as read/unread

### 8. SOP Library (`/sop-library`)

**Features:**
- List of SOP documents
- Filter by:
  - Category (Production, Quality, Safety, Maintenance, Warehouse, HR)
  - Department
  - Tags
- Search SOP
- Preview SOP
- Download SOP
- Rate and review SOP
- SOP version
- Download history

### 9. Profile (`/profile`)

**Features:**
- Profile information:
  - Name, email, student ID
  - Department
  - Cluster and Job Level
  - Certification Level
  - Avatar
- Edit profile
- Change password
- Progress summary
- Achievement badges
- Learning history

### 10. Learning Path Viewer (`/learning-path/:pathId`)

**Features:**
- Learning Path visualization
- Tracks in Learning Path:
  - Technical Track
  - Culture Track
  - Productivity Track
- Progress per track
- List of courses per track
- Prerequisites
- Estimated duration
- Navigate to courses

---

## Instructor Pages

### 1. Instructor Dashboard (`/dashboard`)

**Features:**
- **Welcome Section** with quick action "Create New Course"

- **Quick Stats:**
  - Total Courses
  - Total Students
  - Average Rating
  - Active Discussions

- **Workforce Readiness Index:**
  - Workforce readiness index based on progress
  - Progress bar with status (Ready, Fairly Ready, Needs Attention)
  - Breakdown by cluster (Operator, Leader, Supervisor, Manager, Expatriate)

- **Competencies Needing Improvement:**
  - List of competencies with low progress
  - Status (Critical, Attention)
  - Number of affected students
  - Average progress

- **Pass/Fail Statistics:**
  - Overall statistics (Passed, In Progress, Failed)
  - Breakdown by cluster
  - Percentage per category

- **Quick Actions:**
  - Create New Course
  - View Complete Analytics
  - Manage Students

- **Summary Stats:**
  - Total Courses
  - Total Students
  - Readiness Index
  - Pass Rate

### 2. Course Management (`/courses`)

**Features:**
- List of all courses created by instructor
- Create new course
- Edit course
- Delete course
- Duplicate course
- Course status (Draft, Active, Archived)
- Statistics per course:
  - Number of enrolled students
  - Average progress
  - Completion rate
  - Rating

### 3. Instructor Course Detail (`/instructor/courses/:courseId`)

**Features:**
- Course overview
- Module and lesson management:
  - Add/edit/delete module
  - Add/edit/delete lesson
  - Upload video/document
  - Set duration
  - Reorder modules/lessons
- Content management:
  - Video lessons
  - Document lessons
  - Quiz
  - Assignment
- Student statistics:
  - Progress per student
  - Completion rate
  - Average score
- Course settings:
  - Visibility
  - Enrollment settings
  - Prerequisites

### 4. Assignment Management (`/assignments`)

**Features:**
- List of all assignments from all courses
- Create new assignment
- Edit assignment
- Delete assignment
- Filter by course
- View submissions
- Grade assignments
- Provide feedback
- Export grades

### 5. Assignment Detail (`/assignments/:assignmentId`)

**Features:**
- Assignment information
- List of submissions:
  - Student name
  - Submission time
  - Status (Submitted, Graded, Late)
  - Score
- Grade submission:
  - Input score
  - Provide feedback
  - Download attachment
- Statistics:
  - Submission rate
  - Average score
  - Distribution

### 6. Student Management (`/students`)

**Features:**
- List of all students
- Filter by:
  - Cluster
  - Job Level
  - Department
  - Course
- View student details:
  - Profile
  - Progress per course
  - Assignment submissions
  - Grades
- Export student data

### 7. Training Schedule (`/training-schedule`)

**Features:**
- Calendar view of schedule
- Create new schedule:
  - Select course
  - Set date and time
  - Set location
  - Set type (Classroom, OJT, Practical)
  - Set max participants
  - Upload materials
- Edit/delete schedule
- View enrolled students
- Take attendance
- Update status (Scheduled, Ongoing, Completed, Cancelled)
- Export schedule

### 8. Analytics (`/analytics`)

**Features:**
- **Overview Analytics:**
  - Total students
  - Completion rate
  - Average score
  - Engagement metrics

- **Course Analytics:**
  - Progress per course
  - Student engagement
  - Drop-off points
  - Time spent

- **Student Analytics:**
  - Progress per student
  - Performance distribution
  - At-risk students
  - Top performers

- **Cluster Analytics:**
  - Performance per cluster
  - Readiness index per cluster
  - Competency gaps

- **Charts & Graphs:**
  - Progress trends
  - Score distribution
  - Completion funnel
  - Engagement heatmap

- **Export Reports:**
  - PDF reports
  - Excel exports
  - Custom date ranges

### 9. Forum Management (`/forum`)

**Features:**
- List of all threads from all courses
- Filter by course
- View thread details
- Reply to thread
- Pin/unpin thread
- Lock/unlock thread
- Delete thread/reply
- Moderate content
- Analytics:
  - Most active threads
  - Engagement metrics

### 10. SOP Management (`/sop-library`)

**Features:**
- List of all SOPs
- Create new SOP:
  - Upload document
  - Set category
  - Set department
  - Add tags
  - Set version
- Edit SOP
- Archive SOP
- Version control
- View download statistics
- Manage reviews

### 11. Learning Paths (`/learning-paths`)

**Features:**
- List of Learning Paths
- Create new Learning Path
- Edit Learning Path
- Assign courses to tracks
- Set prerequisites
- Assign to students based on cluster/job level

---

## Admin Pages

### 1. Admin Dashboard (`/dashboard`)

**Features:**
- **Welcome Section** with quick action "Add User"

- **Main Stats:**
  - Total Students (with growth percentage)
  - Total Instructors (with growth)
  - Total Courses (with active courses)
  - Monthly Revenue (with growth)

- **System Status:**
  - Server Uptime
  - Active Users
  - Storage Used
  - Bandwidth
  - Status indicators (good/warning/error)

- **Course Overview:**
  - List of all courses
  - Number of students per course
  - Rating per course

- **Recent Activities:**
  - System activity logs
  - User actions
  - System events

- **Alerts:**
  - Storage warnings
  - System alerts
  - Backup status

- **Quick Actions:**
  - Export Data
  - Generate Report
  - System Maintenance

### 2. User Management (`/users`)

**Features:**
- List of all users (Students, Instructors, Admin)
- Filter by:
  - Role
  - Position
  - Department
  - Cluster
  - Status
- Add new user:
  - Input complete data
  - Set role and position
  - Set cluster and job level
  - Assign learning path
- Edit user:
  - Update profile
  - Change role
  - Update cluster/job level
  - Reassign learning path
- Delete user
- Bulk actions:
  - Bulk assign learning path
  - Bulk update cluster
  - Export users
- View user details:
  - Complete profile
  - Activity log
  - Progress summary

### 3. Learning Path Management (`/learning-paths`)

**Features:**
- List of all Learning Paths
- Create new Learning Path:
  - Name and description
  - Target cluster
  - Target job level
  - Tracks (Technical, Culture, Productivity)
  - Assign courses to tracks
  - Set prerequisites
  - Estimated duration
- Edit Learning Path
- Delete Learning Path
- Duplicate Learning Path
- Assign Learning Path to students:
  - Manual assign
  - Auto assign based on cluster/job level
  - Bulk assign
- View statistics:
  - Number of students per Learning Path
  - Average progress
  - Completion rate

### 4. Instructor Management (`/instructors`)

**Features:**
- List of all instructors
- Add new instructor
- Edit instructor
- Delete instructor
- Assign courses to instructor
- View instructor details:
  - Profile
  - Taught courses
  - Rating
  - Total students
  - Performance metrics

### 5. Student Management (`/students`)

**Features:**
- List of all students
- Advanced filter and search
- Add new student
- Edit student
- Delete student
- Bulk operations:
  - Bulk assign learning path
  - Bulk update cluster
  - Bulk export
- View student details:
  - Complete profile
  - Learning path
  - Progress of all courses
  - Certification level
  - Activity history
- Assign learning path
- Update certification level

### 6. Course Management (`/courses` - Admin view)

**Features:**
- List of all courses from all instructors
- Filter by:
  - Instructor
  - Status
  - Category
- View course details
- Approve/reject course
- Archive course
- Delete course
- Statistics per course
- Export course data

### 7. Assignment & Quiz Management (`/assignments` - Admin view)

**Features:**
- List of all assignments and quizzes
- Filter by:
  - Course
  - Instructor
  - Type (Assignment/Quiz)
- View details
- Statistics:
  - Submission rate
  - Average score
  - Distribution
- Export data

### 8. Admin Analytics (`/analytics`)

**Features:**
- **System-wide Analytics:**
  - Total users
  - Active users
  - Course completion rates
  - Overall readiness index

- **User Analytics:**
  - Growth trends
  - User distribution by role/cluster
  - Engagement metrics
  - Retention rates

- **Course Analytics:**
  - Popular courses
  - Completion rates
  - Average ratings
  - Revenue per course

- **Learning Path Analytics:**
  - Progress per Learning Path
  - Completion rates
  - Cluster performance
  - Competency gaps

- **Performance Metrics:**
  - System performance
  - Server metrics
  - Storage usage
  - Bandwidth usage

- **Reports:**
  - Generate custom reports
  - Scheduled reports
  - Export options (PDF, Excel, CSV)

### 9. Audit Trail (`/audit-trail`)

**Features:**
- Log all system activities
- Filter by:
  - User
  - Action type
  - Date range
  - Module/feature
- View log details:
  - User who performed action
  - Time
  - Action details
  - Before/after values
- Search logs
- Export audit logs
- Retention settings

### 10. System Settings (`/settings`)

**Features:**
- **General Settings:**
  - Site name
  - Logo
  - Theme settings
  - Language settings

- **User Settings:**
  - Registration settings
  - Role permissions
  - Default settings

- **Course Settings:**
  - Default course settings
  - Enrollment rules
  - Completion criteria

- **Learning Path Settings:**
  - Auto-assignment rules
  - Prerequisites rules
  - Certification rules

- **Notification Settings:**
  - Email notifications
  - In-app notifications
  - Notification templates

- **System Settings:**
  - Storage settings
  - Backup settings
  - Security settings
  - API settings

- **Maintenance:**
  - System maintenance mode
  - Database backup
  - Cache management
  - Log management

---

## Authentication System

The authentication system supports login and registration with role-based access control. There are 3 main roles: **student** (employee), **instructor** (teacher), and **admin** (administrator). Additionally, there are positions such as manager, HRD, and supervisor. Each user has attributes such as cluster, job level, certification level, and assigned learning path for personalized learning.

---

## Learning Path System

### Learning Path Concept

Learning Path is a structured learning pathway assigned to students based on:
- **Cluster**: Operator, Leader, Supervisor, Manager, Expatriate
- **Job Level**: Basic, Intermediate, Advanced

### Learning Path Structure

Each Learning Path consists of:
1. **Tracks**:
   - **Technical Track** - Technical competencies
   - **Culture Track** - Company culture
   - **Productivity Track** - Productivity

2. **Courses** - Courses assigned to each track

3. **Prerequisites** - Learning Paths that must be completed first

### Auto-Assignment

The system can auto-assign Learning Paths based on:
- User cluster
- User job level
- Department (optional)

### Progress Tracking

- Progress per track
- Overall Learning Path progress
- Completion status per course
- Certification level update

---

## Deployment

The application is deployed using Docker and Caddy as a reverse proxy with automatic SSL.

---

## Development

The project uses React with TypeScript and Tailwind CSS. For development setup, install dependencies and run the development server. The project structure is organized by components per role (admin, instructor, student) and shared components.

---

## Important Notes

The system currently uses mock data for development. For production, integration with backend API, database, and file storage is required. The system is designed considering security, performance, and scalability aspects.

---

## Support & Maintenance

The system supports logging, regular backups, and periodic updates to ensure optimal security and performance.

---

## Contact & Additional Documentation

- **🌐 Live Website**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)
- **📧 Email**: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)
- **🔑 Demo Credentials**: `DEMO_CREDENTIALS.md`

---

**This documentation was created to provide a complete overview of the E-Learning system.**

**If you are interested in this project or have any questions, please contact me via email: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)**

