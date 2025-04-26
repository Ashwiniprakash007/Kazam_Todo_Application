# ✨ Kazam Todo Application

🔗 **Frontend Deployed Link**: [Kazam Frontend](https://kazam-energy.netlify.app/)

🔗 **Backend Deployed Link**: [Kazam Backend](https://kazam-backend-server-1.onrender.com)

In case if frontend URL is not working properly please refresh the Backend Deployed link by clicking on Deploye Manually and commit latest changes.


## 📅 Project Overview
A **full-stack To-Do Application** with secure authentication, CRUD operations, JWT-based authorization, and token revocation.

---

## 👥 Authentication Features
- **Signup** with email and password
- **Login** with email and password
- **JWT-based Authentication**:
  - **Access Token**: Short-lived
  - **Refresh Token**: Long-lived, stored in **HttpOnly Cookie**
- **Logout**:
  - Refresh token revoked/blacklisted
- **Protected Routes**:
  - Middleware verifies JWTs

---

## 🔢 To-Do Features
- **Authenticated users can**:
  - Create new to-dos (title, description, due date, status)
  - Retrieve all their to-dos
  - Update to-dos
  - Delete to-dos
  - **Filter** to-dos (pending / completed)
  - **Mark as completed**
- **Bonus**:
  - Pagination for todos
  - Implemnted Light and Dark Theme
  - Docker support 

---

## 🛠️ Tech Stack

### 📈 Frontend (React + TypeScript)
- React (with **TypeScript**) for UI development
- **TailwindCSS** for styling
- **Axios** for API calls (with credentials)
- JWT Token Refresh mechanism
- Loading & Error handling
- **Dark Mode Toggle** (Bonus Feature)



---

### 🚀 Backend (Express + MongoDB)
- **Express.js** for RESTful APIs
- **MongoDB Atlas** as database
- **Mongoose** for schema modeling
- **bcrypt** for password hashing
- **jsonwebtoken** for access & refresh token management
- **CORS** with credentials enabled
- **Helmet** for HTTP security

**Middlewares**:
- JWT Verification
- Refresh Token Revocation Check
- Error Handling Middleware


---

## 📆 Models

### 🧑 User Model
- `email`: String
- `passwordHash`: String

### 📋 Todo Model
- `title`: String
- `description`: String
- `status`: String (Pending / Completed)
- `dueDate`: Date
- `owner`: Reference to User

---

## 🛡️ Security
- Passwords hashed with **bcrypt**
- Access and Refresh tokens with **JWT**
- Refresh tokens stored in **HttpOnly Cookies**
- **Helmet** used for extra HTTP security
- **CORS** enabled for frontend-backend communication

---

## 🛫 Deployment
- Frontend deployed on **Netlify**
- Backend deployed on **Render**
- Environment variables secured

---

## 🖊️ Bonus Features
- 🌙 Dark mode toggle
- 📑 Pagination for better performance
- Docker support 


---

## 🔧 How to Run Locally

### 1. Clone the repositories
```bash
git clone <your_frontend_repo_url>
git clone <your_backend_repo_url>
```

### 2. Setup Backend
```bash
cd backend
npm install
npm run dev

```

#### Create a .env file in backend and add:
```bash
PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
REFRESH_SECRET=your_refresh_secret
FRONTEND_URL=http://localhost:5173
```
### 3. Setup Frontend
```bash
cd frontend
npm install
npm run dev
```




