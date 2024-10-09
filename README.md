# GrowthX-Assignment

Overview
This is a backend system for an assignment submission portal built with Node.js and MongoDB. Users can upload assignments, and admins can review and manage them.

Features
User registration and login with JWT authentication.
Admin registration and login with JWT authentication.
Users can upload assignments tagged to specific admins.
Admins can view, accept, or reject assignments.
Technologies Used
Node.js
Express.js
MongoDB
Mongoose
JWT (JSON Web Token)
bcryptjs
API Endpoints
User Endpoints
POST /api/users/register: Register a new user.
POST /api/users/login: User login.
POST /api/users/upload: Upload an assignment.
GET /api/users/admins: Fetch all admins.
Admin Endpoints
POST /api/admins/register: Register a new admin.
POST /api/admins/login: Admin login.
GET /api/admins/assignments: Get assignments tagged to the admin.
POST /api/admins/assignments/:id/accept: Accept an assignment.
POST /api/admins/assignments/:id/reject: Reject an assignment.
Setup Instructions
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/assignment-portal.git
cd assignment-portal
Install dependencies:

bash
Copy code
npm install
Create a .env file in the root directory with your MongoDB URI and JWT secret.

Run the server:

bash
Copy code
node server.js
Authentication
Use the JWT token returned on login in the Authorization header as Bearer <token> for protected routes.