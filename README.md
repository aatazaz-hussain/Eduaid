# 🎓 EduAid — Study Now, Pay Later Education Platform

<p align="center">
  <b>A web-based education financing and scholarship management platform designed to help students access higher education through flexible Study Now, Pay Later (SNPL) opportunities.</b>
</p>

<p align="center">

![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js&logoColor=white)
![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Bootstrap](https://img.shields.io/badge/UI-Bootstrap%205-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![JavaScript](https://img.shields.io/badge/Frontend-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Status](https://img.shields.io/badge/Status-Academic%20Project-198754?style=for-the-badge)

</p>

---

## 📌 Overview

**EduAid** is a full-stack web application focused on improving access to higher education in Pakistan through **Study Now, Pay Later (SNPL)** education financing and scholarship opportunities.

The platform provides a public-facing education portal where students can:

- 🎓 Explore available scholarships
- 🔎 Search and filter scholarship opportunities
- 📝 Submit scholarship applications
- 📊 Check application status
- 📰 Read education-related news
- ℹ️ Learn about EduAid and its mission
- 📞 Contact the organization

An administrative dashboard allows authorized administrators to:

- 👥 Review submitted applications
- ✅ Verify applications
- 🏆 Grant scholarships
- ❌ Mark applicants as not eligible
- 🗑️ Delete applications
- 🎓 Add, edit and delete scholarships
- 📥 Export selected applications as PDF
- 🔔 Monitor new applications
- 📧 Send application-status emails

The backend is implemented with **Node.js + Express.js**, while **SQLite** is used for persistent data storage.

---

# ✨ Key Features

| Feature | Description |
|---|---|
| 🎓 Scholarship Discovery | Browse available SNPL scholarship opportunities |
| 🔎 Search & Filtering | Search scholarships by title, description or eligibility |
| 📝 Online Applications | Students can submit scholarship applications through an online form |
| 📊 Application Status | Applicants can check scholarship application status |
| 🛡️ Admin Dashboard | Manage applications and scholarships |
| ✅ Application Verification | Change application status from the admin panel |
| 🏆 Scholarship Granting | Mark eligible applications as granted |
| 💺 Seat Management | Scholarship seats decrease when applications are granted |
| 📥 PDF Export | Export selected applications into a PDF document |
| 🔔 Admin Notifications | Track newly submitted/unseen applications |
| 📧 Email Notifications | Notify applicants when their application status changes |
| 👤 User Registration | Student/user registration with bcrypt password hashing |
| 🔐 JWT Authentication | Token-based authentication for registered users |
| 🔑 Admin Sessions | Express session-based administrator authentication |
| 📰 News Portal | Education and scholarship-related news content |
| 🏫 University Showcase | Displays partner university logos |
| 📱 Responsive UI | Bootstrap-based responsive layouts |
| ✨ Animations | AOS (Animate On Scroll) effects |
| 🗄️ SQLite Database | Local relational database for users, applications and scholarships |

---

# 🎯 Project Purpose

EduAid is designed around a simple problem:

> **Financial limitations should not prevent deserving students from accessing quality education.**

The platform aims to create a digital bridge between students and education-financing opportunities by combining:

```text
Students
   │
   ▼
Scholarship Discovery
   │
   ▼
Online Application
   │
   ▼
Administrative Verification
   │
   ├── Verified
   ├── Granted
   └── Not Eligible
   │
   ▼
Status Notification
```

The project's central concept is **Study Now, Pay Later (SNPL)**, allowing students to pursue education while accessing flexible financing opportunities.

---

# 🏗️ System Architecture

EduAid follows a lightweight full-stack web architecture:

```text
┌────────────────────────────────────────────────────┐
│                    FRONTEND                        │
│                                                    │
│ HTML5 + CSS3 + Bootstrap 5 + JavaScript           │
│ Bootstrap Icons + AOS                              │
│                                                    │
│ Home | Scholarships | Application | Status | News  │
└─────────────────────────┬──────────────────────────┘
                          │
                          │ HTTP / Form / Fetch API
                          ▼
┌────────────────────────────────────────────────────┐
│                  EXPRESS SERVER                    │
│                                                    │
│ Node.js + Express.js                               │
│ Sessions + JWT + Multer + Body Parser              │
│                                                    │
│ Authentication | Applications | Scholarships       │
│ Status | Notifications | PDF Export | Email        │
└─────────────────────────┬──────────────────────────┘
                          │
             ┌────────────┼─────────────┐
             │            │             │
             ▼            ▼             ▼
        ┌─────────┐  ┌──────────┐  ┌───────────┐
        │ SQLite  │  │ Nodemailer│  │ PDFKit    │
        │ Database│  │ Email     │  │ PDF Export│
        └─────────┘  └──────────┘  └───────────┘
```

---

# 🧰 Technology Stack

## Backend

- **Node.js**
- **Express.js 5**
- `express-session`
- `body-parser`
- `multer`
- `bcrypt`
- `jsonwebtoken`
- `nodemailer`
- `pdfkit`
- `sqlite3`

## Frontend

- HTML5
- CSS3
- JavaScript
- Bootstrap 5.3
- Bootstrap Icons
- AOS 2.3.1

## Database

- SQLite3

## Authentication

Two authentication approaches are present:

### Registered Users

```text
bcrypt
   ↓
Password Hashing
   ↓
SQLite users table
   ↓
JWT
```

### Administrator

```text
Admin Login
   ↓
Express Session
   ↓
req.session.admin
   ↓
Protected Admin Routes
```

---

# 📁 Project Structure

The supplied project is organized approximately as follows:

```text
EDUAID/
│
├── server.js
├── package.json
├── package-lock.json
│
├── data/
│   └── eduaid.db
│
├── public/
│   ├── home.html
│   ├── index3.html
│   ├── login.html
│   ├── register.html
│   ├── scholarships.html
│   ├── apply-form.html
│   ├── status.html
│   ├── how-it-works.html
│   ├── about.html
│   ├── news.html
│   ├── contact.html
│   ├── admin-login.html
│   ├── admin-panel.html
│   ├── style.css
│   │
│   └── images/
│       ├── logo.png
│       ├── inspiration.png
│       ├── students.jpg
│       ├── aleena-nadeem.jpg
│       ├── author1.jpg
│       ├── author2.jpg
│       ├── author3.jpg
│       ├── author4.jpg
│       ├── news1.jpg
│       ├── news2.jpg
│       ├── news3.jpg
│       ├── news4.jpg
│       ├── news5.jpg
│       ├── news6.jpg
│       ├── pu.png
│       ├── lums.png
│       ├── fast.png
│       ├── nust.png
│       └── pmas.png
│
├── node_modules/
└── .git/
```

> **Note:** The supplied ZIP also contains `node_modules/` and the Git metadata directory. These generally should not be committed to a clean GitHub repository.

---

# 🗄️ Database Design

The project uses:

```text
data/eduaid.db
```

SQLite tables are created automatically by `server.js`.

The main entities are:

```text
USERS
   │
   └── Authentication

APPLICATIONS
   │
   └── Scholarship Applications

SCHOLARSHIPS
   │
   └── Available Financing Opportunities
```

---

# 👤 Users Table

The `users` table stores registered users.

```sql
users
├── id
├── name
├── email
└── password
```

Passwords are hashed with:

```text
bcrypt
```

rather than being stored directly in plaintext.

---

# 📝 Applications Table

The `applications` table stores scholarship submissions.

Main fields include:

```text
id
name
father_name
dob
domicile
city
phone
email

inter_uni
inter_cgpa

bachelor_uni
bachelor_cgpa

master_uni
master_cgpa

phd_uni
phd_cgpa

scholarship_type
status
submitted_at
notified
```

### Application status values

The admin panel supports:

```text
Unverified
Verified
Granted
Not Eligible
```

---

# 🎓 Scholarships Table

The `scholarships` table stores available opportunities.

```text
id
title
description
eligibility
deadline
seats_left
```

Example conceptual record:

```text
Title:
EduAid Technology Scholarship

Description:
Financial assistance for eligible students.

Eligibility:
Students meeting defined academic criteria.

Deadline:
2025-12-31

Seats:
25
```

---

# 🔗 Data Relationship

The application and scholarship systems are connected through:

```text
Scholarship
     │
     │ title
     ▼
Application
     │
     ├── Applicant Information
     ├── Academic Background
     ├── Application Status
     └── Submission Date
```

When an application is granted, the server attempts to reduce the corresponding scholarship's `seats_left` value.

---

# 👥 User Workflows

## 🎓 Student Workflow

```text
Visit EduAid
      │
      ▼
Browse Scholarships
      │
      ▼
Search / Filter
      │
      ▼
Select Opportunity
      │
      ▼
Apply Now
      │
      ▼
Fill Application
      │
      ├── Personal Information
      ├── Contact Information
      ├── Domicile
      ├── Academic History
      └── Scholarship Selection
      │
      ▼
Submit
      │
      ▼
Application Stored
      │
      ▼
Check Application Status
```

---

# 🛡️ Administrator Workflow

```text
Admin Login
     │
     ▼
Admin Panel
     │
     ├── Applications
     │      │
     │      ├── Review
     │      ├── Verify
     │      ├── Grant
     │      ├── Reject
     │      └── Delete
     │
     ├── Scholarships
     │      │
     │      ├── Add
     │      ├── Edit
     │      └── Delete
     │
     ├── Notifications
     │
     └── PDF Export
```

---

# 🔐 Authentication

## User Registration

Endpoint:

```http
POST /api/register
```

Registration data:

```text
name
email
password
```

The server:

1. Receives registration data.
2. Checks that admin credentials are not being registered.
3. Hashes the password using bcrypt.
4. Inserts the user into SQLite.
5. Returns a success message.

---

# 🔑 User Login

Endpoint:

```http
POST /api/login
```

The server:

1. Looks up the user by email.
2. Compares the supplied password with the bcrypt hash.
3. Generates a JWT token.
4. Returns the token and user's name.

JWT expiration:

```text
2 hours
```

---

# 🛡️ JWT-Protected Profile

Endpoint:

```http
GET /api/user-profile
```

The endpoint requires:

```http
Authorization: Bearer <JWT_TOKEN>
```

The middleware verifies the JWT before allowing access.

---

# 🔐 Administrator Authentication

Admin login:

```http
POST /admin-login
```

The server checks administrator credentials and establishes:

```javascript
req.session.admin = true
```

Protected admin pages/APIs verify this session before returning sensitive information.

---

# 🎓 Scholarship APIs

## Get Scholarships

```http
GET /api/scholarships
```

Optional query parameters:

```text
search
deadline
```

Example:

```text
/api/scholarships?search=technology&deadline=upcoming
```

The endpoint searches:

```text
title
description
eligibility
```

and only returns records where:

```text
seats_left > 0
```

---

## Add Scholarship

```http
POST /api/scholarships/add
```

Parameters:

```text
title
description
eligibility
deadline
seats_left
```

---

## Edit Scholarship

```http
POST /api/scholarships/edit
```

Parameters:

```text
id
title
description
eligibility
deadline
seats_left
```

---

## Delete Scholarship

```http
POST /api/scholarships/delete
```

Parameter:

```text
id
```

---

# 📝 Application APIs

## Submit Application

```http
POST /submit-application
```

The application form supports:

### Personal information

```text
Name
Father Name
Date of Birth
Domicile
City
Phone
Email
```

### Academic information

```text
Intermediate University
Intermediate CGPA

Bachelor University
Bachelor CGPA

Master University
Master CGPA

PhD University
PhD CGPA
```

### Scholarship

```text
Scholarship Type
```

The backend stores missing academic levels as:

```text
N/A
```

---

# 📊 Application Status

Page:

```text
/status
```

Form endpoint:

```http
POST /status-check
```

The system retrieves applications according to the selected scholarship and displays:

```text
Applicant Name
Father Name
Highest Degree
Application Status
```

Status badges are visually differentiated:

| Status | Display |
|---|---|
| 🟡 Unverified | Secondary |
| 🟠 Verified | Warning |
| 🟢 Granted | Success |
| 🔴 Not Eligible | Danger |

---

# 📥 PDF Export

Administrators can select multiple applications and export them as a PDF.

Endpoint:

```http
POST /api/download-selected
```

The server uses:

```text
PDFKit
```

The generated document includes information such as:

```text
Application ID
Name
Father Name
Email
Phone
City
Scholarship
Status
Submission Date
```

Generated files use a timestamped filename similar to:

```text
Selected_Applications_XXXXXXXXXXXX.pdf
```

---

# 🔔 Notification System

EduAid tracks newly submitted applications using a `notified` column.

Initial state:

```text
notified = 0
```

When administrators retrieve applications, the application records are marked as notified.

Endpoint:

```http
GET /api/notifications
```

The admin dashboard polls the endpoint periodically and displays a notification badge when new applications exist.

The current frontend checks every:

```text
10 seconds
```

---

# 📧 Email Notifications

When an administrator changes an application status, the backend attempts to send an email to the applicant.

Supported status updates include:

```text
Verified
Granted
Not Eligible
Unverified
```

Email content contains:

```text
Applicant Name
Scholarship
New Application Status
EduAid branding/message
```

The project uses:

```text
Nodemailer
```

with Gmail SMTP configuration.

---

# ⚙️ Prerequisites

Before running EduAid, install:

- **Node.js**
- **npm**
- Git
- A modern web browser

Check Node.js:

```bash
node --version
```

Check npm:

```bash
npm --version
```

Recommended Node.js version:

```text
Node.js 18+
```

The project uses modern Express 5 and current npm packages, so a recent LTS version is recommended.

---

# 🚀 Installation

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/eduaid.git
cd eduaid
```

---

## 2. Install dependencies

```bash
npm install
```

This installs dependencies defined in:

```text
package.json
```

including:

```text
express
sqlite3
bcrypt
jsonwebtoken
express-session
multer
body-parser
nodemailer
pdfkit
```

---

# ▶️ Running the Application

## Development mode

The project includes:

```json
"dev": "nodemon server.js"
```

Run:

```bash
npm run dev
```

---

## Production-style start

Run:

```bash
npm start
```

The server starts on:

```text
http://localhost:3000
```

---

# 🌐 Application Pages

| Page | Purpose |
|---|---|
| `home.html` | Landing/login entry page |
| `index3.html` | Main EduAid information portal |
| `login.html` | User login |
| `register.html` | User registration |
| `how-it-works.html` | Explains the EduAid process |
| `scholarships.html` | Scholarship discovery and filtering |
| `apply-form.html` | Scholarship application form |
| `status.html` | Application status checking |
| `about.html` | Mission, inspiration and values |
| `news.html` | Education/news section |
| `contact.html` | Contact information/form |
| `admin-login.html` | Administrator login |
| `admin-panel.html` | Administrative management dashboard |

---

# 🎨 UI & Design

EduAid uses a clean education-focused visual identity.

### Primary colors

The frontend is heavily based around:

```text
Bootstrap Success Green
#198754

Dark Green
#025C46

Primary Green
#017B5F
```

The design uses:

- Bootstrap 5
- Responsive navigation
- Green call-to-action buttons
- Card-based scholarship layouts
- Responsive tables
- Hero sections
- Image-based storytelling
- Bootstrap Icons
- AOS animations

---

# 🏫 University Showcase

The homepage includes a carousel highlighting Pakistani universities:

- Punjab University
- LUMS
- FAST-NUCES
- NUST
- PMAS-Arid Agriculture University

University logos are stored under:

```text
public/images/
```

---

# 📰 News Section

The project includes six predefined news cards covering education-related topics such as:

- Digital learning
- Tuition-free education
- STEM education
- Women in technology
- International graduate opportunities
- AI research funding

The news content is currently static HTML rather than database-driven.

---

# 💡 About EduAid

The About page communicates three core values:

### 🔓 Access

> Every student deserves education regardless of income.

### 🛡️ Integrity

> Transparency, fairness and accountability.

### 💡 Impact

> Creating long-term educational change rather than short-term relief.

The page also presents EduAid's mission around removing financial barriers to higher education.

---

# 🧱 Backend Components

| Component | Responsibility |
|---|---|
| `server.js` | Main Express server and all application routes |
| `sqlite3` | Database persistence |
| `bcrypt` | Password hashing |
| `jsonwebtoken` | User authentication tokens |
| `express-session` | Administrator sessions |
| `multer` | Form/multipart parsing |
| `nodemailer` | Email notifications |
| `pdfkit` | PDF application export |
| `body-parser` | URL-encoded request parsing |

---

# 🔄 Complete Application Flow

```text
                    ┌───────────────┐
                    │    Visitor    │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │    EduAid     │
                    │    Website    │
                    └───────┬───────┘
                            │
             ┌──────────────┼───────────────┐
             │              │               │
             ▼              ▼               ▼
        Scholarships     Register/Login     News
             │              │
             ▼              ▼
        Apply Now       JWT Authentication
             │
             ▼
       Application
             │
             ▼
          SQLite
             │
             ▼
       Admin Review
             │
      ┌──────┼────────┐
      │      │        │
      ▼      ▼        ▼
   Verify  Grant   Not Eligible
      │      │        │
      └──────┼────────┘
             ▼
       Email Notification
             │
             ▼
       Status Available
```

---

# 🔒 Security Considerations

The project contains some good security foundations, especially:

- bcrypt password hashing
- Parameterized SQLite queries
- JWT authentication
- Session-based admin protection

However, there are **important security issues that should be fixed before publishing or deploying this application publicly.**

## 🚨 1. Secrets are hard-coded

The supplied `server.js` contains hard-coded secrets, including:

- Express session secret
- JWT secret
- Gmail SMTP credentials

These should **not** be committed to GitHub.

Use environment variables instead:

```env
SESSION_SECRET=your_secure_session_secret
JWT_SECRET=your_secure_jwt_secret
SMTP_USER=your_email
SMTP_PASS=your_app_password
```

Then load them through environment configuration.

---

## 🚨 2. Gmail credentials should be rotated

The supplied project contains a real-looking SMTP username/password inside the source code.

If these credentials are still active, **change/revoke them before uploading the project to a public GitHub repository.**

Do not expose email credentials in source code.

---

## 🚨 3. Admin credentials are hard-coded

The admin login currently uses credentials directly in `server.js`.

For production:

```text
Do not hard-code administrator passwords.
```

Use hashed credentials stored in a database or secure authentication provider.

---

## 🚨 4. Application status privacy

The `/status-check` implementation retrieves applications based only on the selected scholarship type.

This means a user could potentially see other applicants associated with that scholarship.

A production system should require a private identifier such as:

```text
Application ID
Email + verification
CNIC/application reference
Secure status token
```

and return only the corresponding applicant's record.

---

## 🚨 5. File upload handling

The application submission endpoint uses:

```text
multer
```

for multipart form parsing, but the current implementation does not appear to persist or validate uploaded documents.

Production systems should implement:

- File type validation
- File size limits
- Malware scanning
- Secure storage
- Randomized filenames
- Access control

---

# ⚠️ Known Limitations

### 1. No production configuration system

Secrets and configuration values are embedded directly in the source.

### 2. Static news content

News is currently hard-coded in HTML rather than managed through the database/admin panel.

### 3. Static contact information

The displayed contact details are currently embedded in the frontend.

### 4. Scholarship filtering logic

The `deadline` query is treated as a text pattern rather than robust date-based comparison.

A future implementation should parse dates and support:

```text
Upcoming
Expired
Closing Soon
```

based on actual dates.

### 5. Application status lookup

The current status-check flow can expose multiple records for a scholarship rather than identifying a single applicant securely.

### 6. Admin authorization

The administrator account uses a simple session flag rather than a database-backed role/permission system.

### 7. No CSRF protection

State-changing form/API requests should use CSRF protection where appropriate.

### 8. No rate limiting

Login and application endpoints should have rate limiting to prevent abuse.

### 9. No centralized error handling

The server contains route-specific error responses rather than a comprehensive error-handling layer.

### 10. No automated test suite

The supplied project does not contain a dedicated unit/integration testing framework.

---

# 🧹 Recommended `.gitignore`

A clean GitHub repository should not include:

```gitignore
# Dependencies
node_modules/

# Environment variables
.env
.env.*
!.env.example

# Database
*.db
*.sqlite
*.sqlite3

# Logs
*.log
npm-debug.log*

# Generated files
*.pdf

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/
```

If a demo SQLite database is required for evaluation, keep a sanitized sample database separately.

---

# 📦 Recommended `.env.example`

After moving secrets out of `server.js`, the repository can include:

```env
PORT=3000

SESSION_SECRET=replace_with_secure_random_value
JWT_SECRET=replace_with_secure_random_value

SMTP_HOST=smtp.gmail.com
SMTP_PORT=465
SMTP_USER=your_email@example.com
SMTP_PASS=your_gmail_app_password
```

The real `.env` file should never be committed.

---

# 🧪 Testing Recommendations

A future automated test suite should cover:

## Authentication

- User registration
- Duplicate email registration
- Password hashing
- Valid login
- Invalid login
- JWT generation
- Expired JWT
- Protected profile access

## Scholarships

- List scholarships
- Search scholarships
- Filter scholarships
- Add scholarship
- Edit scholarship
- Delete scholarship
- Seat availability

## Applications

- Submit application
- Validate required fields
- Store academic information
- Application status update
- Application deletion
- PDF export

## Admin

- Valid admin login
- Invalid admin login
- Protected admin pages
- Protected admin APIs
- Logout/session destruction

## Email

- Status email generation
- SMTP failure handling
- Invalid recipient handling

---

# 🛣️ Future Improvements

Potential next-generation improvements include:

- 🔐 Secure environment-based configuration
- 👤 Proper role-based access control
- 🧑‍🎓 Applicant dashboard
- 📊 Personalized application tracking
- 🔎 Advanced scholarship matching
- 🤖 AI-powered scholarship recommendations
- 📄 Secure document uploads
- 📑 Application document verification
- 📧 Professional email templates
- 📱 Progressive Web App support
- 📰 CMS-based news management
- 🛡️ Improved privacy controls
- 🔒 CSRF protection
- 🚦 API rate limiting
- 📅 Real date-based scholarship deadlines
- 📈 Admin analytics dashboard
- 📊 Scholarship statistics
- 🔍 Application search/filtering
- 🧪 Automated tests
- 🐳 Docker deployment
- ☁️ Cloud database support
- 🔄 Database migrations
- 🔐 Production HTTPS deployment
- 📚 API documentation with OpenAPI/Swagger

---

# 🖼️ Screenshots

For a polished GitHub repository, add screenshots such as:

```text
screenshots/
├── home.png
├── scholarships.png
├── application-form.png
├── application-status.png
├── admin-login.png
└── admin-dashboard.png
```

Then display them in the README:

```markdown
![EduAid Home](screenshots/home.png)
```

Recommended showcase order:

1. 🏠 Homepage
2. 🎓 Scholarship discovery
3. 📝 Application form
4. 📊 Status page
5. 🛡️ Admin dashboard

---

# 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/eduaid.git

# Enter the project
cd eduaid

# Install dependencies
npm install

# Start development server
npm run dev
```

Open:

```text
http://localhost:3000
```

For a normal start:

```bash
npm start
```

---

# 📊 Project Summary

| Category | Details |
|---|---|
| 🎓 Project | EduAid |
| 💡 Purpose | Education financing & scholarship platform |
| 🌍 Target | Students in Pakistan |
| 💰 Model | Study Now, Pay Later (SNPL) |
| ⚙️ Backend | Node.js + Express.js |
| 🎨 Frontend | HTML + CSS + JavaScript |
| 🧩 UI Framework | Bootstrap 5 |
| 🗄️ Database | SQLite |
| 🔐 User Auth | bcrypt + JWT |
| 🛡️ Admin Auth | Express Session |
| 📧 Email | Nodemailer |
| 📄 PDF | PDFKit |
| 📎 Form Upload | Multer |
| ✨ Animation | AOS |
| 🌐 Port | 3000 |
| 📌 Status | Academic / Development Project |

---

# 👨‍💻 Developer

## Aatazaz Hussain

**EduAid — Study Now, Pay Later Education Platform**

The project demonstrates practical implementation of:

```text
Full-Stack Web Development
+
Node.js / Express
+
SQLite Database
+
Authentication
+
Scholarship Management
+
Application Processing
+
PDF Generation
+
Email Notifications
+
Responsive Web Design
```

---

# 📄 License

No explicit license was included in the supplied project.

Before making the repository public, add an appropriate license such as:

- MIT
- Apache 2.0
- GPL-3.0

For an academic project, a custom academic/project license can also be used.

---

<p align="center">
  <b>🎓 EduAid</b><br>
  <i>Empowering students. Expanding access. Financing futures.</i>
</p>
