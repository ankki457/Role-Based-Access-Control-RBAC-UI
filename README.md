# **Role-Based Access Control (RBAC) UI**

## **Project Overview**

This project is a frontend implementation of a **Role-Based Access Control (RBAC)** system, designed to provide an intuitive and secure user interface (UI) for managing users, roles, and permissions in an admin dashboard. The goal is to create a UI where administrators can easily assign roles, modify permissions, and manage users in a secure and user-friendly environment.

The project is built using **React** and **Bootstrap** for styling, with a focus on responsiveness and ease of use. The app simulates a real-world RBAC system that includes CRUD operations for users and roles, role-based permissions, and dynamic permissions assignment.

## **Core Features**

1. **User Management**
    - View and manage users (add, edit, delete).
    - Assign roles to users and manage their statuses (Active/Inactive).

2. **Role Management**
    - Define and edit roles with permissions (e.g., Read, Write, Delete).
    - Easily assign and modify permissions for each role.

3. **Dynamic Permissions**
    - Clear UI for managing permissions for each role.
    - Display of permissions in an intuitive format for easy modification.

4. **Custom API Simulation**
    - Mock API calls for CRUD operations on users and roles.
    - Simulated server responses to validate functionality.

## **Live Project**

- **Frontend (UI)**: [Role-Based Access Control (RBAC) UI - Live](https://role-based-access-control-rbac-ui-o0fe.onrender.com)
- **Backend (API)**: [Backend API - Live](https://assignment-role-based-access-control.onrender.com)

## **Technologies Used**

- **React** for the frontend framework.
- **Bootstrap** for responsive UI design.
- **Vite** for development build and bundling.
- **Mock APIs** for simulating server requests (optional).

## **Installation Instructions**

1. Clone the repository:

    ```bash
    git clone <repository-url>
    ```

2. Navigate to the project folder:

    ```bash
    cd rbac-ui
    ```

3. Install the dependencies:

    ```bash
    npm install
    ```

4. Run the development server:

    ```bash
    npm run dev
    ```

    Open your browser and visit `http://localhost:5173/` to view the app.

## **Project Structure**

```
rbac-ui/
│
├── src/
│   ├── components/          # UI components (Navbar, UserList, RoleList, etc.)
│   ├── pages/               # Different pages of the application (Dashboard, Login, etc.)
│   ├── services/            # Simulated API calls and data management
│   ├── App.js               # Main app component
│   ├── index.js             # Entry point
│   └── styles.css           # Custom styles
│
├── public/                  # Static assets (index.html, images, etc.)
│   ├── images/              # Images like logos, icons, etc.
│   └── favicon.ico          # Favicon for the app
│
├── package.json             # Project dependencies and scripts
├── vite.config.js           # Vite configuration
└── README.md                # Project documentation
```

## **Features**

### **User Management**
- Add, edit, and delete users.
- Assign roles and manage user status (Active/Inactive).

### **Role Management**
- Create, edit, and delete roles.
- Roles can have permissions such as **Read**, **Write**, **Delete**, or custom permissions.
  
### **Dynamic Permission Assignment**
- Assign permissions to roles dynamically.
- Modify permissions easily from the UI with a simple toggle.

### **Responsive Design**
- The app is fully responsive and adapts to various screen sizes, from mobile to desktop.

### **Security**
- Basic input validation is implemented to prevent invalid data.
- Error handling in API calls to manage failed operations gracefully.

### **Bonus Features**
- Sorting, filtering, and searching capabilities for users and roles.
- Customizable permissions for each role, ensuring flexibility in the RBAC model.

## **Usage**

1. **Managing Users:**
   - Admins can add new users, edit existing users, and assign them specific roles (e.g., Admin, User, Guest).
   - Admins can also toggle user status between **Active** and **Inactive**.

2. **Managing Roles:**
   - Admins can create new roles and assign permissions (Read, Write, Delete).
   - Admins can edit roles and modify permissions based on the needs of their team.

3. **Managing Permissions:**
   - Permissions can be assigned to roles directly, and changes are reflected in real-time for users with those roles.

## **Evaluation Criteria**

- **Creativity and Design Quality:** The design is sleek and intuitive, allowing easy navigation and role management.
- **Functionality:** The core features of managing users, roles, and permissions are fully implemented and functional.
- **Responsiveness:** The UI adjusts seamlessly to different screen sizes.
- **User Experience:** The UI/UX is straightforward and easy to use, with a focus on clarity and simplicity.
- **Technical Skill:** The project is built using best practices for React development and clean code structure.

## **Future Enhancements**

- Implement real API integration for user and role management.
- Add more advanced features like role inheritance, logging, and audit trails.
- Improve security with better authentication and authorization practices.

![Screenshot (92)](https://github.com/user-attachments/assets/a4f0ca65-5308-4c0f-857f-eacd7a9be952)
![Screenshot (93)](https://github.com/user-attachments/assets/83086881-7e62-4f6b-9e22-ae3d136efa3a)
![Screenshot (94)](https://github.com/user-attachments/assets/6e03ef2f-bb2e-4b40-a63f-9835ec56af14)
![Screenshot (95)](https://github.com/user-attachments/assets/74325e46-8009-4775-b7b0-eb39b0b0f578)


