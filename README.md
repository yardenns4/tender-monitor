# TenderMonitor

An end-to-end tender monitoring system that automates the discovery, storage, and management of Israeli Land Authority (RMI) tenders.

---

## 🚀 Overview

TenderMonitor is a full-stack system that continuously monitors new tenders, downloads tender booklets, stores them in Google Drive, and synchronizes structured data into a custom-built application for user interaction.

The system was designed to solve a real-world problem: efficiently tracking and managing tenders without manual effort.

---

## 🎯 Problem

Users who want to participate in tenders currently need to:
- Manually search the RMI website
- Track updates themselves
- Download and manage files manually
- Keep track of relevant tenders

This process is inefficient, time-consuming, and prone to missing opportunities.

---

## 💡 Solution

TenderMonitor automates the entire flow:

- Automated tender monitoring via API
- File download and storage (Google Drive)
- Data synchronization into a structured database
- Custom web application for:
  - Viewing tenders
  - Managing favorites ("My Tenders")
  - Receiving notifications on new tenders
  - Opening files directly

---

## 🧠 System Architecture
RMI API → n8n → Google Drive → Base44 → Web Application


### Key Components:
- **n8n** – workflow automation & orchestration  
- **Google Drive** – file storage layer  
- **Base44** – backend, database, and UI framework  
- **Web App** – user-facing interface  

---

## ✨ Core Features

- Automated tender ingestion pipeline  
- File management and storage  
- Favorites system ("My Tenders")  
- Real-time notifications for new tenders  
- User authentication and management  
- Search capabilities  

---

## 📸 Screenshots

### Login
<img width="218" height="368" alt="sign up screen" src="https://github.com/user-attachments/assets/26de9484-c501-4412-a615-332509433fcb" />

### Home Dashboard
<img width="359" height="319" alt="Home Screen" src="https://github.com/user-attachments/assets/3f5442db-3bae-4c89-9c34-a5a03f34240e" />

### Active Tenders
<img width="344" height="413" alt="Active Tender Screen" src="https://github.com/user-attachments/assets/b1cdc34c-f3f0-43ef-b68e-fccf1ead5fd6" />

### Favorites ("My Tenders")
<img width="332" height="377" alt="My favorites screen" src="https://github.com/user-attachments/assets/b910635a-5ecd-455e-a254-e91cedc81b66" />

### New Tender Email
<img width="277" height="313" alt="NewTenderEmail" src="https://github.com/user-attachments/assets/3dfaed5a-9c85-4db2-80ce-ba8f446f3f80" />


---

## 🌐 Live Application

👉 https://cautious-tender-track-pro.base44.app

> Note: The application is still under active development.  
> Accessibility features (for compliance with standards) are planned for upcoming versions.

---

## 🛠️ Technologies

- Base44 (backend + UI)
- n8n (automation workflows)
- Google Drive API
- REST APIs
- Data modeling & entity design

---

## 🧠 Skills & Concepts Demonstrated

- End-to-end system design  
- Automation pipelines and orchestration  
- API integrations  
- Data modeling (entities, relationships, normalization)  
- Event-driven workflows (trigger-based automation)  
- Product thinking and UX design  
- Full data flow architecture (ingestion → storage → presentation)  

---

## 🗄️ Data Model

The system is built on a structured data model designed for scalability and future analytics.

### Core Entities:

**Tender**
- tender_id  
- title  
- shchuna (location)  
- file_name  
- file_date  
- drive_file_url  
- active Status
- created At
- updated At

**User**
- user_id  
- email  
- role
- name
- first Name
- last Name
- registration Completed
- google Drive Access
- mailing List Status
- synchronization Status 

**UserFavoriteTender**
- user_id  
- tender_id  

**Notification**
- type (e.g., new_tender)  
- tender_id  
- tender Title
- created_at
- file Name
- tender Number
- neighborhood (Shchuna)

---

### Relationships:

- A user can save multiple tenders (many-to-many)
- A tender can be saved by multiple users
- Notifications are linked to tenders and events

---

### Design Considerations:

- Separation between operational data (tenders) and user interactions (favorites, notifications)
- Designed for future behavioral tracking and analytics
- Supports scalable queries and filtering

  ---

## 📊 Data & BI Perspective

The system was designed with future data analysis and BI capabilities in mind:

- Structured entities (Tender, User, Favorites, Notifications)
- Clear relationships between data sources
- Ability to track user behavior (favorites, interactions, engagement)
- Prepared foundation for:
  - Behavioral analysis
  - usage tracking
  - data-driven feature development

Future versions will include leveraging this data to identify patterns and optimize product decisions.

---

## 🔮 Future Roadmap

Planned enhancements include:

- AI-powered assistance for analyzing tenders  
- Smart recommendations based on user behavior  
- Advanced search and filtering  
- Personalized notifications  
- Behavioral analytics and BI dashboards  
- Accessibility improvements (UI/UX compliance)

---

## ⚠️ Note

This project integrates multiple external systems (n8n, Base44, Google Drive),
therefore the full source code is not publicly available.

This repository focuses on system design, architecture, and product implementation.

---

## 👨‍💻 Author

Yarden Moshe

