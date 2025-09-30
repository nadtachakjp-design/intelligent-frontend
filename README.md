# Intelligent KPI Management System

Fullstack assessment project with **React + Tailwind (Frontend)** and **Node.js + Express + MongoDB (Backend)**.

---
## Figma
- [Link](https://www.figma.com/design/GrxjUe8mshrmgv4wyTeNPU/intelligent-assessment?node-id=0-1&t=XjKtQeoT79ZLfBYJ-1)

## Live Demo

- **Frontend (Vercel)**: [https://intelligent-frontend-exam.vercel.app/login](https://intelligent-frontend-exam.vercel.app/login)
- **Backend (Render)**: [https://intelligent-backend-klps.onrender.com/api](https://intelligent-backend-klps.onrender.com/api)

### Test Accounts

- **Admin**: `admin1@exam.com` / `1234`
- **User**: `user1@exam.com` / `1234`

---

## Setup Instructions

### Backend

```bash
cd intelligent-backend
npm install
cp .env.example .env   # set MONGO_URI and JWT_SECRET
npm start
```

### Frontend

```bash
cd intelligent-frontend
npm install
cp .env.example .env   # set REACT_APP_API_URL=http://localhost:4000/api
npm run dev
```

---

## API Documentation

### USER

- `GET /users`
- `GET /users/list` → for select options
- `DELETE /users/:id`
- `POST /users`
  ```json
  { "username": "", "email": "", "password": "", "roleName": "user" }
  ```
- `PUT /users/:id`
  ```json
  { "username": "", "email": "", "roleName": "user" }
  ```

### Dashboard

- `GET /dashboard` → Overview
- `GET /dashboard/pie?user=&status=`
- `GET /dashboard/line?user=&status=`
- `GET /dashboard/table?user=&status=`

### KPI

- `GET /kpis`
- `DELETE /kpis/:id`
- `POST /kpis`
  ```json
  {
    "title": "",
    "description": "",
    "targetValue": "",
    "actualValue": "",
    "status": "",
    "assignedUser": "",
    "startDate": "",
    "endDate": ""
  }
  ```
- `PUT /kpis/:id`
  ```json
  {
    "title": "",
    "description": "",
    "targetValue": "",
    "actualValue": "",
    "status": "",
    "assignedUser": "",
    "startDate": "",
    "endDate": ""
  }
  ```

---