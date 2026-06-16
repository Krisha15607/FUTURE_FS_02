# 🚀 LeadFlow CRM — Client Lead Management System

A sleek, premium, full-stack Client Lead Management System (CRM) designed to capture, organize, and track leads through a dynamic sales pipeline.

[![Live Demo](https://img.shields.io/badge/Live_Demo-Visit_App-00c853?style=for-the-badge&logo=vercel&logoColor=white)](https://lead-crm-frontend-mocha.vercel.app/)
[![Frontend](https://img.shields.io/badge/Frontend-React_&_Vite-61dafb?style=for-the-badge&logo=react&logoColor=white)](https://react.dev)
[![Backend](https://img.shields.io/badge/Backend-Node.js_&_Express-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![Database](https://img.shields.io/badge/Database-MongoDB-47a248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com)

---

## 🔗 Live Links

*   **✨ Production Live Preview:** [https://lead-crm-frontend-mocha.vercel.app/](https://lead-crm-frontend-mocha.vercel.app/)
*   **🔌 Backend Endpoint:** `https://lead-crm-backend-eta.vercel.app`
*   **💻 Code Repository:** [GitHub Repository](https://github.com/Krisha15607/FUTURE_FS_02)

---

## ✨ Features

*   🔐 **Secure Admin Login** — JWT-based authentication for administrative dashboard access.
*   📋 **Pipeline Management** — Real-time progress updates through pipelines: `New` ➔ `Contacted` ➔ `Converted`.
*   📝 **Timeline & Notes** — Chronological logs to track client communications, notes, and progress history.
*   📅 **Follow-ups Scheduler** — Interactive task checklists to schedule, prioritize, and complete follow-up calls or meetings.
*   📊 **Analytics Dashboard** — Modern metrics grid displaying conversion rates, total revenue/leads, and lead source splits.
*   🔌 **Public Webhook API** — Fully functional `/api/leads` endpoint with API key authorization for seamless third-party website integrations.
*   🔍 **Advanced Filters** — Search leads instantly by name/email, filter by source or status, and sort chronologically.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React (Vite), Vanilla CSS (Modern Design System), React Icons |
| **Backend** | Node.js, Express.js, JWT Authentication |
| **Database** | MongoDB Atlas (via Mongoose ODM) |
| **Deployment** | Vercel (both Frontend & Backend) |

---

## 📂 Folder Directory Layout

```text
Client Lead Management System/
├── backend/
│   ├── middleware/
│   │   └── auth.js          # JWT Authentication Guard
│   ├── models/
│   │   ├── Lead.js          # Lead schema (Details, Notes, Timeline, Tasks)
│   │   └── User.js          # Encrypted Admin User schema
│   ├── routes/
│   │   ├── auth.js          # Auth endpoints (Login, registration checks)
│   │   └── leads.js         # Leads CRUD, Status Pipeline, and Sub-tasks API
│   ├── server.js            # Express Server Config
│   └── vercel.json          # Serverless Vercel Deployment Configuration
│
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── Dashboard.jsx    # Metrics and list overview
    │   │   ├── LeadDetails.jsx  # Notes, Tasks, and Edit drawer
    │   │   ├── Login.jsx        # Admin sign-in screen
    │   │   └── WebhookDocs.jsx  # API snippet developer documentation
    │   ├── App.jsx              # Application state and routing
    │   ├── index.css            # Custom CSS premium theme UI
    │   └── main.jsx
    └── package.json
```

---

## 🚀 Getting Started Locally

### 1. Clone the Repository
```bash
git clone https://github.com/Krisha15607/FUTURE_FS_02.git
cd FUTURE_FS_02
```

### 2. Configure Environment Variables
Inside the `backend/` directory, create a `.env` file based on `.env.example`:
```env
PORT=5050
MONGODB_URI=your_mongodb_connection_uri
JWT_SECRET=your_jwt_secret_key
```

### 3. Installation & Seeding
In the `backend/` folder:
```bash
npm install
node seedAdmin.js   # Seeds default admin credentials
npm run dev
```

In the `frontend/` folder:
```bash
npm install
npm run dev
```

### 🔑 Default Admin Account
*   **Email**: `admin@crm.com`
*   **Password**: `Admin@1234`

---

## 🔌 API Webhook Integration

To submit leads to your CRM pipeline from any contact form, send a `POST` request to:
`https://lead-crm-backend-eta.vercel.app/api/leads`

#### Example Payload:
```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "source": "Landing Page",
  "message": "Interested in your product pricing."
}
```

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for details.

<!-- cache-refresh -->