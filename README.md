Here is the complete **README.md** file for your project. Copy and save it as `README.md` in your project directory.  

```md
# 🚀 Spring Boot Security - Job Management System

## 📌 Project Overview
This is a **Spring Boot Security-based Job Management System** with role-based access control.  

### 🔐 Roles & Functionalities:
- **Admin:** Create, View, Edit, and Delete Job Listings.
- **User:** View Jobs, Apply for Jobs, Withdraw Applications.
- **Authentication & Authorization:** Handled using **Spring Security**.

---

## 🛠 Tech Stack
- **Spring Boot** (Security, Web, Data JPA)
- **Spring Security** (Role-based Authentication)
- **Thymeleaf** (Frontend)
- **MySQL** (Database)
- **Maven** (Build Tool)

---

## 📂 Project Structure
```
com.wipro.Wipro_Security
│── config/          # Security configurations
│── controller/      # Controllers for handling requests
│── model/           # Entity classes
│── repository/      # Data access layer
│── service/         # Business logic layer
│── resources/
│   ├── templates/   # Thymeleaf templates
│   ├── application.properties
│   ├── application.yml
│── WiproSecurityApplication.java  # Main class
```

---

## ⚙️ Setup Instructions
### 🔹 Step 1: Clone the Repository
```sh
git clone https://github.com/your-username/job-management-system.git
cd job-management-system
```

### 🔹 Step 2: Configure Database (`application.properties`)
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/springjpa
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 🔹 Step 3: Run the Application
```sh
mvn spring-boot:run
```

### 🔹 Step 4: Access the Application
- **Login Page:** `http://localhost:9092/login`
- **Admin Dashboard:** `http://localhost:9092/admin/home`
- **User Dashboard:** `http://localhost:9092/user/home`

---

## 📝 Operations & Step-by-Step Guide
### ✅ 1. Register a New User or Admin
1. Open `http://localhost:9092/register`
2. Fill in **Name, Email, Password**.
3. Select **Role** (Admin/User).
4. Click **Register**.

---

### 🔑 2. Login as User or Admin
1. Open `http://localhost:9092/login`
2. Enter **Email & Password**.
3. Click **Login**.
4. **Admin Redirects to:** `/admin/home`
5. **User Redirects to:** `/user/home`

---

### 🛠 3. Admin Operations
#### ➤ Create a Job Listing
1. Login as **Admin**.
2. Go to `/admin/home`.
3. Click **"Add Job"**.
4. Enter **Job Title, Salary, Location**.
5. Click **Submit**.

#### ➤ Edit a Job Listing
1. Login as **Admin**.
2. Go to `/admin/home`.
3. Click **"Edit"** next to a job.
4. Modify details & Click **Update**.

#### ➤ Delete a Job Listing
1. Login as **Admin**.
2. Go to `/admin/home`.
3. Click **"Delete"** next to a job.

---

### 👨‍💼 4. User Operations
#### ➤ View Available Jobs
1. Login as **User**.
2. Go to `/user/home`.
3. See the list of available jobs.

#### ➤ Apply for a Job
1. Login as **User**.
2. Click **"Apply"** on a job.
3. Confirm application.

#### ➤ Withdraw Job Application
1. Login as **User**.
2. Click **"Withdraw"** next to applied job.

---

### 🔄 5. Reset Password (Forgot Password)
#### If a User or Admin forgets their password:
1. Go to `http://localhost:9092/forgot-password`.
2. Enter **registered email**.
3. Click **Submit** (A reset link will be sent).
4. Open the email & click the **reset link**.
5. Enter **new password** and confirm.

---

## 📜 Database Schema
### **Userinfo Table**
| ID | Name  | Email  | Password | Roles  |
|----|-------|--------|----------|--------|
| 1  | Admin | admin@example.com | Encrypted | ROLE_ADMIN |
| 2  | User  | user@example.com  | Encrypted | ROLE_USER |

### **Job Table**
| Job ID | Title     | Salary | Location  |
|--------|----------|--------|-----------|
| 101    | Developer | 50,000 | Remote    |
| 102    | Designer  | 45,000 | New York  |

---

## 🚀 API Endpoints (For Postman Testing)
### **Authentication**
- `POST /register` → Register User/Admin  
- `POST /login` → Login  

### **Admin Job Management**
- `POST /admin/jobs` → Add Job  
- `GET /admin/jobs` → View Jobs  
- `PUT /admin/jobs/{id}` → Update Job  
- `DELETE /admin/jobs/{id}` → Delete Job  

### **User Actions**
- `GET /user/jobs` → View Available Jobs  
- `POST /user/apply/{jobId}` → Apply for Job  
- `DELETE /user/withdraw/{jobId}` → Withdraw Application  

### **Password Reset**
- `POST /forgot-password` → Request Reset  
- `POST /reset-password` → Submit New Password  

---

## 📜 License
This project is **open-source** and available for modification.

---
👨‍💻 **Developed by:** [Your Name]  
📧 Contact: your-email@example.com
```

---

### **Steps to Add This to GitHub**
1. Save the file as **`README.md`** in your project root.
2. Open Git Bash and navigate to the project folder:
   ```sh
   cd /path/to/your/project
   ```
3. Add the file to Git:
   ```sh
   git add README.md
   ```
4. Commit the changes:
   ```sh
   git commit -m "Added project README"
   ```
5. Push to GitHub:
   ```sh
   git push origin main
   ```

Now, your **GitHub repository** will display this **README** with all instructions. 🚀 Let me know if you need any modifications! 😊
