# **Role-Based Access Control (RBAC) Authentication System**

## **Project Overview**

This project implements an Authentication and Authorization system using **Role-Based Access Control (RBAC)**. It allows users to register, log in, log out securely, and access resources based on their assigned roles. The system uses **JSON Web Tokens (JWT)** for session management and password hashing with **bcrypt** for security.

Roles supported in this system:
- **Admin**
- **User**
- **Moderator**

Each role has specific access to resources, and the access is controlled by middleware to ensure that users can only access routes and perform actions permitted by their roles.

## **Core Concepts**

1. **Authentication:** Secure login and registration with hashed passwords.
2. **Authorization:** Access control based on user roles (Admin, User, Moderator).
3. **Role-Based Access Control (RBAC):** Managing what users can access based on their roles.
4. **JWT:** Used for session management and ensuring the security of APIs.

## **Features**

- User Registration: Allows users to sign up with a username, password, and role.
- User Login: Users can log in, and upon successful authentication, receive a JWT.
- Role-based Access: Different routes have different levels of access based on roles (e.g., Admin can access user management).
- Secure Passwords: Passwords are hashed using bcrypt before storing in the database.
- JWT Authentication: Secure token-based authentication for session management.
- Logout: Invalidate the JWT on logout to secure the user session.

## **Installation**

Follow the steps below to set up the project on your local machine.

### **Prerequisites**

Make sure you have the following installed:

- **Node.js** (v14 or later)
- **MongoDB** (local or cloud instance like MongoDB Atlas)
- **Postman** (for testing the APIs)

### **Steps to Install**

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-repo/rbac-auth-system.git
   ```

2. **Navigate to the Project Directory:**

   ```bash
   cd rbac-auth-system
   ```

3. **Install Dependencies:**

   Install the required npm packages:

   ```bash
   npm install
   ```

4. **Set Up Environment Variables:**

   Create a `.env` file in the root directory and add the following:

   ```bash
   MONGO_URI=mongodb://your-mongo-uri
   JWT_SECRET=your-secret-key
   ```

   Replace `your-mongo-uri` with your MongoDB connection URI (either local or from MongoDB Atlas), and `your-secret-key` with a secret key used for signing JWT tokens.

5. **Start the Server:**

   Run the following command to start the server:

   ```bash
   npm start
   ```

   The server will be running on `http://localhost:5000`.

---

## **API Endpoints**

### **1. Register User**

**POST** `/api/users/register`

- **Request Body:**

    ```json
    {
        "username": "string",
        "password": "string",
        "role": "string" // Optional, default is 'User'
    }
    ```

- **Response:**

    ```json
    {
        "id": "user_id",
        "username": "username",
        "role": "role",
        "token": "jwt_token"
    }
    ```

### **2. Login User**

**POST** `/api/users/login`

- **Request Body:**

    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```

- **Response:**

    ```json
    {
        "id": "user_id",
        "username": "username",
        "role": "role",
        "token": "jwt_token",
        "msg": "Logged in successfully"
    }
    ```

### **3. Get All Users (Admin Only)**

**GET** `/api/users/`

- **Authorization:** Bearer token with Admin role.

- **Response:**

    ```json
    [
        {
            "id": "user_id",
            "username": "username",
            "role": "role"
        }
    ]
    ```

### **4. Logout User**

**POST** `/api/users/logout`

- **Authorization:** Bearer token.

- **Response:**

    ```json
    {
        "message": "Logged out successfully"
    }
    ```

---

## **Testing with Postman**

### **Steps to Test API with Postman:**

1. **Register User:**

   - **URL:** `http://localhost:5000/api/users/register`
   - **Method:** `POST`
   - **Body:** Select `raw` and choose `JSON`. Then provide the required user data:
     
     ```json
     {
         "username": "john_doe",
         "password": "securepassword",
         "role": "User"
     }
     ```

   - **Response:**

     ```json
     {
         "id": "user_id",
         "username": "john_doe",
         "role": "User",
         "token": "jwt_token"
     }
     ```

2. **Login User:**

   - **URL:** `http://localhost:5000/api/users/login`
   - **Method:** `POST`
   - **Body:** Provide the username and password for the registered user:

     ```json
     {
         "username": "john_doe",
         "password": "securepassword"
     }
     ```

   - **Response:**

     ```json
     {
         "id": "user_id",
         "username": "john_doe",
         "role": "User",
         "token": "jwt_token",
         "msg": "Logged in successfully"
     }
     ```

3. **Get All Users (Admin Only):**

   - **URL:** `http://localhost:5000/api/users/`
   - **Method:** `GET`
   - **Headers:** Add `Authorization` header with the value `Bearer <jwt_token>` from the login response.

   - **Response:** List of all users.

     ```json
     [
         {
             "id": "user_id",
             "username": "john_doe",
             "role": "User"
         }
     ]
     ```

4. **Logout User:**

   - **URL:** `http://localhost:5000/api/users/logout`
   - **Method:** `POST`
   - **Headers:** Add `Authorization` header with the value `Bearer <jwt_token>`.

   - **Response:**

     ```json
     {
         "message": "Logged out successfully"
     }
     ```

---

## **Code Structure**

### **1. `controllers/userController.js`**

Handles user registration, login, fetching users, and logout logic.

### **2. `middlewares/authMiddleware.js`**

Contains middleware for JWT validation (`protect`) and role-based access control (`authorize`).

### **3. `models/User.js`**

User schema with bcrypt password hashing and role handling.

### **4. `routes/userRoutes.js`**

Defines routes for user operations (register, login, get users, logout).

### **5. `server.js`**

Entry point to the application where Express server is set up and routes are registered.

---

## **Security Best Practices**

- **Password Hashing:** Passwords are hashed using `bcryptjs` before storing them in the database.
- **JWT Authentication:** We use JWT tokens for secure, stateless authentication. The token is issued upon login and must be included in the `Authorization` header for protected routes.
- **Role-Based Authorization:** Access control is managed based on the user's role. Middleware functions ensure that only authorized users can access certain resources.

---

## **Conclusion**

This project demonstrates the implementation of an **Authentication**, **Authorization**, and **Role-Based Access Control (RBAC)** system using **JWT**. The system provides secure user registration, login, and role-based access to resources. 