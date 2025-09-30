# Ahad-Job-Configs
# 🚀 Ahad Job Portal - API Routes

## 🌐 Base URL
```
http://localhost:8080
```

## 🔐 AUTHENTICATION ROUTES (No JWT Required)

### User Registration
**POST** `/api/v1/register/user`

### Company Registration  
**POST** `/api/v1/register/company`

### Login
**POST** `/api/v1/auth/login`

### Validate Token
**POST** `/api/v1/auth/validate`

---

## 👤 USER ROUTES (JWT Protected)

### User Profile
**GET** `/api/v1/users/profile`  
**PUT** `/api/v1/users/profile`

### User Information
**GET** `/api/v1/user-info`  
**PUT** `/api/v1/user-info`

### Educations
**GET** `/api/v1/educations`  
**POST** `/api/v1/educations`  
**PUT** `/api/v1/educations/{id}`  
**DELETE** `/api/v1/educations/{id}`

### Achievements
**GET** `/api/v1/achievements`  
**POST** `/api/v1/achievements`  
**PUT** `/api/v1/achievements/{id}`  
**DELETE** `/api/v1/achievements/{id}`

### Job History
**GET** `/api/v1/job-history`  
**POST** `/api/v1/job-history`  
**PUT** `/api/v1/job-history/{id}`  
**DELETE** `/api/v1/job-history/{id}`

---

## 🏢 COMPANY ROUTES (JWT Protected)

### Company Profile
**GET** `/api/v1/companies/profile`  
**PUT** `/api/v1/companies/profile`

### Company Information
**GET** `/api/v1/company-information`  
**PUT** `/api/v1/company-information`

### Company Addresses
**GET** `/api/v1/company-addresses`  
**POST** `/api/v1/company-addresses`  
**PUT** `/api/v1/company-addresses/{id}`  
**DELETE** `/api/v1/company-addresses/{id}`

---

## 💼 JOB ROUTES (Mixed Access)

### Jobs (Public GET, Protected POST/PUT/DELETE)
**GET** `/api/v1/jobs` - Public  
**GET** `/api/v1/jobs/{id}` - Public  
**POST** `/api/v1/jobs` - Protected  
**PUT** `/api/v1/jobs/{id}` - Protected  
**DELETE** `/api/v1/jobs/{id}` - Protected

### Job Applications
**GET** `/api/v1/applications` - Protected  
**POST** `/api/v1/applications` - Protected  
**GET** `/api/v1/applications/{id}` - Protected  
**PUT** `/api/v1/applications/{id}` - Protected

### Categories (Public)
**GET** `/api/v1/categories` - Public  
**GET** `/api/v1/categories/{id}` - Public

---

## 🔔 NOTIFICATION ROUTES (JWT Protected)

### Notifications
**GET** `/api/v1/notifications`  
**POST** `/api/v1/notifications`  
**GET** `/api/v1/notifications/{id}`  
**PUT** `/api/v1/notifications/{id}`

### Emails
**GET** `/api/v1/emails`  
**POST** `/api/v1/emails`

### Alerts
**GET** `/api/v1/alerts`  
**POST** `/api/v1/alerts`

---

## 🔒 ACCESS TYPES

- **Public**: No JWT token required
- **Protected**: JWT token required in Authorization header
- **Mixed**: Some methods public, some protected

## 📨 REQUEST HEADERS

**For Protected Routes:**
```
Authorization: Bearer <jwt_token>
Content-Type: application/json
```

**Example:**
```http
GET /api/v1/users/profile
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
Content-Type: application/json
```
