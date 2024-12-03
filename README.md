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

## **Technologies Used**

- **React** for the frontend framework.
- **Bootstrap** for responsive UI design.
- **Vite** for development build and bundling.
- **Mock APIs** for simulating server requests (optional).

## **Installation Instructions**

1. Clone the repository:

    ```bash
    git clone https://github.com/ankki457/Role-Based-Access-Control-RBAC-UI/tree/main/Frontend
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
    live project `https://role-based-access-control-rbac-ui-o0fe.onrender.com`
    BAackend Api `https://assignment-role-based-access-control.onrender.com`

## **Project Structure**

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

![Screenshot (92)](https://github.com/user-attachments/assets/5fe0779f-c48d-4b52-93a4-0cbd631fcf76)
![Screenshot (93)](https://github.com/user-attachments/assets/d6854b4e-5160-404d-adec-d943406156f9)
![Screenshot (94)](https://github.com/user-attachments/assets/dc9e9a72-e37c-40eb-b52b-e93fbddf16a5)
![Screenshot (95)](https://github.com/user-attachments/assets/0e713323-6eb9-4b8d-bd99-24c25266564e)



