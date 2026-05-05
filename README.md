# 🎓 Internship Management System

> A web-based platform for students to submit internship details and for faculty to evaluate and manage them.

![Node.js](https://img.shields.io/badge/Node.js-Express-green?logo=node.js)
![MySQL](https://img.shields.io/badge/Database-MySQL%20(Aiven)-blue?logo=mysql)
![EJS](https://img.shields.io/badge/Template-EJS-yellow)
![Vercel](https://img.shields.io/badge/Deploy-Vercel-black?logo=vercel)

---

## 📌 Overview

The Internship Management System is a full-stack web application that streamlines the internship submission and evaluation process between students and faculty.

**Students can:**
- Log in and submit internship details (company, role, stipend, dates)
- Upload offer letter, completion letter, and LOR
- View their internship status and faculty evaluation

**Faculty can:**
- Log in and view all students
- Evaluate students on technical skills, communication, professionalism, and more
- Create and manage student groups
- View submitted attachments

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Node.js + Express.js |
| Database | MySQL (hosted on Aiven Cloud) |
| Template Engine | EJS |
| File Uploads | Multer |
| Frontend | HTML, CSS, JavaScript, Chart.js |
| Deployment | Vercel |

---

## 📁 Project Structure

```
internship-management-system/
├── public/
│   ├── index.ejs                  # Landing page
│   ├── student-login.ejs          # Student login
│   ├── student-dashboard.ejs      # Student dashboard
│   ├── internship-submission.ejs  # Internship form
│   ├── faculty-login.ejs          # Faculty login
│   ├── faculty-dashboard.ejs      # Faculty dashboard
│   ├── evaluation-form.ejs        # Evaluation form
│   ├── group-management.ejs       # Group management
│   ├── view-attachments.ejs       # View uploaded files
│   └── *.css                      # Stylesheets
├── uploads/                       # Uploaded files (git-ignored)
├── server.js                      # Main Express server
├── backup.sql                     # Database schema
├── ca.pem                         # Aiven SSL certificate
├── package.json
├── .env                           # Environment variables (git-ignored)
└── vercel.json                    # Vercel deployment config
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js installed
- MySQL database (Aiven or local)

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/RRoshiniDevi/internship-management-system.git
cd internship-management-system

# 2. Install dependencies
npm install

# 3. Create a .env file
touch .env
```

### Configure `.env`
```
DB_HOST=your_database_host
DB_PORT=your_database_port
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_NAME=your_database_name
```

### Set up the Database
Import the schema using `backup.sql`:
```bash
mysql -u your_user -p your_database < backup.sql
```

### Run the App
```bash
npm start
```
Visit `http://localhost:3000` in your browser. ✅

---

## 🗄️ Database Tables

| Table | Purpose |
|-------|---------|
| `users` | Stores student and faculty accounts |
| `students` | Student profile details |
| `faculty` | Faculty profile details |
| `internships` | Internship submission records |
| `evaluations` | Faculty evaluation records |
| `groups_table` | Faculty-created student groups |
| `group_students` | Student-group assignments |

---

## 🔭 Future Improvements

- [ ] Add proper session management (JWT/cookies)
- [ ] Email notifications for evaluation completion
- [ ] Admin dashboard for overall monitoring
- [ ] Export evaluation reports as PDF

---

## 👤 Author

**R Roshini Devi** — IWP CIA-3 Project
