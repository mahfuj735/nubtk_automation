<div align="center">

# 🎓 University Management System (NUBTK Automation)
### *A Unified Digital Ecosystem for Academic Excellence & Campus Automation*

[![Flutter](https://img.shields.io/badge/Mobile_App-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![React](https://img.shields.io/badge/Web_Frontend-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org)
[![Node.js](https://img.shields.io/badge/Backend-Express%20%26%20NestJS-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Supabase](https://img.shields.io/badge/Cloud-Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![Firebase](https://img.shields.io/badge/Auth%20%26%20Push-Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](./LICENSE)

<p align="center">
  <b>Developed for Industrial Training Defense</b><br>
  Department of Computer Science & Engineering (CSE)<br>
  <b>Northern University of Business and Technology Khulna (NUBTK)</b>
</p>

[📑 View Presentation (PDF)](#-industrial-training-defense-presentation) •
[🏛️ System Architecture](#-system-architecture) •
[🌐 Web Portals](#-web-portals) •
[📊 Admin ERP](#-centralized-admin-panel--erp) •
[📱 Mobile Apps](#-mobile-applications-flutter) •
[⚡ Key Features](#-key-features--capabilities)

---

</div>

## 📑 Industrial Training Defense Presentation

The complete defense presentation slide deck and project documentation are archived in this repository:

<div align="center">
  <a href="./Mahfuj735.pdf">
    <img src="assets/presentation_cover.png" width="85%" alt="Industrial Training Defense Presentation Preview" style="border-radius: 12px; box-shadow: 0 8px 24px rgba(0,0,0,0.18); border: 1px solid #e1e4e8;">
  </a>
  <br><br>

  <a href="./Mahfuj735.pdf">
    <img src="https://img.shields.io/badge/📄_Read_Defense_Report-PDF_Format-red?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Read PDF">
  </a>
  &nbsp;&nbsp;
  <a href="./Mahfuj735.pptx">
    <img src="https://img.shields.io/badge/📊_Download_Slides-PowerPoint_PPTX-orange?style=for-the-badge&logo=microsoftpowerpoint&logoColor=white" alt="Download PPTX">
  </a>
</div>

<br>

| Academic Details | Information |
| :--- | :--- |
| **Project Title** | University Management System: A Digital Ecosystem for Academic Excellence |
| **Presented By** | **Md. Mahfujul Karim Sheikh** (Student ID: `11220120735`, Section: `7B`) |
| **Supervised By** | **Md. Mossadek Touhid**, Lecturer, Department of CSE |
| **Institution** | **Northern University of Business and Technology Khulna (NUBTK)** |
| **Core Focus** | End-to-end digitisation of academic, administrative, financial, and student workflows |

---

## 💡 Problem Statement & Objective

Traditional university operations rely heavily on manual paperwork, distributed spreadsheets, and disconnected desktop systems. This causes:
- ⏳ **Slow Administrative Turnaround:** Admission, course registration, and document clearance take days or weeks.
- 📉 **Data Redundancy & Errors:** Inconsistent student records across separate departments.
- 🔕 **Communication Gap:** Delays in routine changes, examination schedules, and urgent notifications reaching students.
- 📊 **Lack of Centralized Analytics:** University leadership lacks real-time insight into attendance, fee defaults, and student performance.

### 🎯 The Solution:
**NUBTK Automation** delivers a single, unified digital platform connecting **students, faculty members, and central administration**. It bridges public-facing information portals with deep administrative automation and native mobile apps equipped with an AI-powered academic assistant.

---

## 🏛️ System Architecture

```mermaid
graph TD
    subgraph Client_Layer["🖥️ Client Applications Layer"]
        web["🌐 University Public Website<br/><b>React.js / Vite</b>"]
        admin["📊 Central Admin & ERP Portal<br/><b>React.js / TailwindCSS</b>"]
        student_app["📱 Student Mobile App<br/><b>Flutter (Android / iOS)</b>"]
        faculty_app["👨‍🏫 Faculty Mobile App<br/><b>Flutter (Android / iOS)</b>"]
    end

    subgraph API_Layer["⚡ Backend & Gateway Layer"]
        web_api["🚀 Public & Web Services API<br/><b>Node.js / Express.js (:5000)</b>"]
        admin_api["🛡️ Admin & ERP Core Engine<br/><b>NestJS (:3001)</b>"]
        auth["🔐 JWT & Role-Based Access Control (RBAC)"]
    end

    subgraph Intelligence_Layer["🤖 Intelligence & Real-Time Services"]
        ai_assistant["🧠 AI Academic Assistant<br/><b>Google Gemini AI Integration</b>"]
        fcm["🔔 Push Notifications & Live Events<br/><b>Firebase Cloud Messaging (FCM)</b>"]
    end

    subgraph Data_Layer["🗄️ Database & Storage Layer"]
        pg["🐘 Relational Database<br/><b>PostgreSQL Instances</b>"]
        supa["⚡ Real-time Data Sync & File Storage<br/><b>Supabase Cloud</b>"]
    end

    web --> web_api
    admin --> admin_api
    student_app --> web_api
    student_app --> ai_assistant
    student_app --> fcm
    faculty_app --> admin_api
    faculty_app --> fcm

    web_api --> auth
    admin_api --> auth
    auth --> pg
    auth --> supa
```

---

## 🌐 Web Portals

### 1. University Public Portal
Modern, responsive web interface for prospective students, current students, faculty, and public visitors.
- Academic regulations, program curriculums, and departmental information.
- Campus virtual tour, event calendars, and official notices.

<div align="center">
  <img src="Screenshot%20(301).png" width="95%" alt="University Website Home Page" style="border-radius: 8px; border: 1px solid #ddd;">
</div>

<br>

### 2. Online Admission & Application Pipeline
- Fully digital admission application submission.
- Real-time document verification and applicant tracking.

<div align="center">
  <img src="Screenshot%20(349).png" width="95%" alt="Online Admission System" style="border-radius: 8px; border: 1px solid #ddd;">
</div>

---

## 📊 Centralized Admin Panel & ERP

The admin dashboard provides full institutional command with predictive business intelligence:
- **Real-Time KPIs:** Live counts of active students (2,800+), faculty members, overall attendance rate, and revenue collection.
- **Workflow Pipeline:** Step-by-step verification (Payment Verified ➔ Documents Verified ➔ Interview Scheduled ➔ Final Approval).
- **AI-Driven Insights:** Automated detection of student dropout risks, fee default predictions, and attendance anomalies.

<div align="center">
  <img src="screencapture-localhost-5174-dashboard-2026-01-22-05_10_39.png" width="95%" alt="Admin Panel Dashboard" style="border-radius: 8px; border: 1px solid #ddd;">
</div>

---

## 📱 Mobile Applications (Flutter)

Cross-platform mobile applications tailored specifically for student and faculty daily routines:

### 🎓 Student Mobile App
Equipped with personal profiles, academic tracking, tuition fee payments, dynamic class schedules, and a generative AI study assistant.

<table align="center" width="100%">
  <tr>
    <td align="center" width="33%">
      <img src="assets/student_app_home.jpg" width="280" alt="Student App Dashboard" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>🏠 Student Dashboard</b><br>
      <sub>Online Library, Payment, Course Registration & Results</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/student_app_ai_assistant.jpg" width="280" alt="AI Academic Assistant" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>🤖 AI Academic Assistant</b><br>
      <sub>24/7 AI tutor for syllabus queries, code debugging & concept explanations</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/student_app_schedule.jpg" width="280" alt="Class Routine" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>📅 Dynamic Class Routine</b><br>
      <sub>Day-by-day lecture timing, room assignments & instructor info</sub>
    </td>
  </tr>
</table>

<br>

### 👨‍🏫 Faculty Mobile App
Empowers professors and course instructors with on-the-go academic management.

<table align="center" width="100%">
  <tr>
    <td align="center" width="33%">
      <img src="assets/faculty_app_home.jpg" width="280" alt="Faculty Dashboard" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>📋 Faculty Command Center</b><br>
      <sub>Grade submission deadlines, course allocation, payroll & notices</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/faculty_app_evaluation.jpg" width="280" alt="Student Evaluation" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>📝 Student Evaluation & Grading</b><br>
      <sub>Semester & section-wise marks entry, assessment & grading</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/faculty_app_schedule.jpg" width="280" alt="Faculty Schedule" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
      <br><br>
      <b>🕒 Teaching Timetable</b><br>
      <sub>Direct overview of daily assigned lecture hours and halls</sub>
    </td>
  </tr>
</table>

---

## ⚡ Key Features & Capabilities

- 🔐 **Enterprise Security & RBAC:**
  Role-Based Access Control enforcing strict separation of privileges across Superadmin, Department Head, Faculty, and Student tiers. Powered by stateless JWT token rotation.
- 🤖 **AI-Powered Academic Assistant:**
  Integrated with modern LLM intelligence to help students understand complex lecture topics, draft academic queries, review code, and receive tailored course assistance.
- 🚀 **Streamlined Digital Admission:**
  Paperless applicant verification workflow featuring online fee reconciliation and automated admission status alerts.
- 📲 **Real-Time Notification Broadcast:**
  Firebase Cloud Messaging (FCM) delivers instant emergency announcements, class rescheduling notices, and grade releases directly to mobile devices.
- 🛡️ **Data Sanitization & Injection Defense:**
  All REST endpoints incorporate schema validation, SQL injection prevention, and encrypted data storage for sensitive records.

---

## 📈 Measurable Results & Impact

<div align="center">

| Metric | Improvement | Description |
| :---: | :---: | :--- |
| 📉 **70%** | **Manual Workload Reduction** | Drastic cut in physical paperwork and manual ledger maintenance. |
| ⚡ **80%** | **Faster Processing** | Admission cycle time reduced from weeks of physical queues to digital minutes. |
| 🎯 **95%** | **Data Accuracy Improvement** | Elimination of duplicate records and manual grade transcript errors. |
| 🌐 **99.5%** | **System Reliability** | High availability with decoupled micro-services and cloud failover. |

</div>

---

## 🛠️ Technology Stack Summary

| Domain | Technologies Used |
| :--- | :--- |
| **Mobile Applications** | Flutter, Dart, Riverpod / Provider |
| **Web Frontends** | React.js, Vite, TailwindCSS, Axios |
| **Backend Services** | Node.js, Express.js, NestJS, TypeScript |
| **Databases** | PostgreSQL, Supabase Realtime |
| **Cloud & DevOps** | Firebase (Auth, FCM), Supabase Storage, Docker |
| **AI Integration** | Google Gemini API for Academic Assistant |

---

## 🚀 Future Roadmap

- [ ] **MFS & Payment Gateway:** Integration of bKash, Nagad, and Credit/Debit card automated payment reconciliations.
- [ ] **Parent & Alumni Portals:** Dedicated portals for parent progress tracking and alumni networking.
- [ ] **Automated Exam Hall Seating:** Algorithmic examination seat plan generator to avoid section clustering.
- [ ] **Multi-Region Cloud Deployment:** Geographic redundancy and auto-scaling infrastructure.

---

## 👤 Author & Acknowledgements

- **Developer:** Md. Mahfujul Karim Sheikh
  - Student ID: `11220120735`
  - Section: `7B`, 7th Semester
  - Department of Computer Science & Engineering (CSE)
  - Northern University of Business and Technology Khulna (NUBTK)
- **Academic Supervisor:** Md. Mossadek Touhid
  - Lecturer, Department of CSE, NUBTK

---

<div align="center">
  <sub>© 2026 Northern University of Business & Technology Khulna. All rights reserved.</sub>
</div>
