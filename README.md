# Project Management System (PMS)

A modern web application for managing projects, tasks, and teams with real-time updates and role-based access.

## 🚀 How It Works

### User Authentication & Roles
- **Secure Login System:** JWT-based authentication with password hashing
- **Role-Based Access Control:**
  - **Admin:** Full system access - manage users, projects, tasks, and system settings
  - **Manager:** Project management - create/manage projects, assign tasks, track progress
  - **Member:** Task-focused - view assigned tasks, update status, add comments

### Project Management Workflow
1. **Project Creation:** Managers/Admins create projects with details, timeline, and budget
2. **Team Assembly:** Add team members with specific roles (developer, designer, tester)
3. **Task Breakdown:** Create tasks for each project phase with priorities and deadlines
4. **Progress Tracking:** Monitor project milestones and overall completion status
5. **Status Updates:** Update project status (planning → active → completed)

### Task Management System
- **Task Creation:** Detailed task creation with descriptions, priorities, and due dates
- **Assignment System:** Assign tasks to team members with clear responsibilities
- **Status Tracking:** Real-time status updates (todo → in-progress → review → completed)
- **Progress Monitoring:** Visual progress bars and percentage tracking
- **Checklist System:** Create and manage task checklists with completion tracking
- **Time Logging:** Track time spent on tasks for project analytics
- **Comments & Collaboration:** Add comments and discuss task details

### Real-Time Features
- **Live Updates:** Socket.IO integration provides instant updates across all users
- **Real-Time Notifications:** Toast notifications for status changes and updates
- **Live Collaboration:** Multiple users can work simultaneously with live sync
- **Instant Status Changes:** Task and project status updates appear immediately

### User Interface & Experience
- **Responsive Design:** Works seamlessly on desktop, tablet, and mobile devices
- **Modern UI:** Clean, intuitive interface built with Tailwind CSS
- **Dashboard Overview:** Quick stats, recent projects, and overdue tasks
- **Advanced Filtering:** Search and filter projects/tasks by status, priority, assignee

### Data Management
- **MongoDB Database:** NoSQL database for flexible data storage
- **User Profiles:** Manage personal information, departments, and positions
- **Activity Tracking:** Monitor user activities and project changes
- **Data Validation:** Server-side validation for all user inputs

### Security Features
- **JWT Authentication:** Secure token-based authentication
- **Password Hashing:** bcryptjs for secure password storage
- **Route Protection:** Middleware-based access control for all API endpoints
- **Input Validation:** Comprehensive validation for all user inputs
- **Error Handling:** Graceful error handling with user-friendly messages

## 🛠 Tech Stack
- **Frontend:** React, Tailwind CSS, React Router, Axios, Socket.IO Client
- **Backend:** Node.js, Express.js, MongoDB, Mongoose, JWT, Socket.IO
- **Other:** bcryptjs (password hashing), Express Validator, React Hook Form

## ⚡ Quick Start

### Prerequisites
- **Node.js** (v16 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- **MongoDB** (local installation or MongoDB Atlas account)

### Step 1: Clone and Setup
```bash
# Clone the repository
git clone <repo-url>
cd PMS

# Install server dependencies
npm install

# Install client dependencies
cd client
npm install
cd ..
```

### Step 2: Environment Configuration
Create a `config.env` file in the root directory:
```env
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/pms
JWT_SECRET=your-super-secret-jwt-key-here
```

**For MongoDB Atlas users:**
```env
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/pms
```

### Step 3: Database Setup
**Option A: Local MongoDB**
1. Install MongoDB locally
2. Start MongoDB service
3. Database will be created automatically

**Option B: MongoDB Atlas**
1. Create account at [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create a new cluster
3. Get your connection string
4. Update `MONGODB_URI` in `config.env`

### Step 4: Create Default Users
```bash
node setup-admin.js
```
This creates:
- **Admin:** `admin@example.com` / `password123`
- **Manager:** `manager@example.com` / `password123`
- **Member:** `member@example.com` / `password123`

### Step 5: Start the Application
```bash
# Start the backend server (from root directory)
npm start

# In a new terminal, start the frontend
cd client
npm start
```

### Step 6: Access the Application
- **Frontend:** Open [http://localhost:3000](http://localhost:3000)
- **Backend API:** Running on [http://localhost:5000](http://localhost:5000)

### Step 7: Login and Explore
1. Login with any of the default credentials above
2. Start by creating a project as Admin/Manager
3. Add team members to your project
4. Create and assign tasks
5. Track progress and updates in real-time!

### Troubleshooting
- **Port already in use:** Kill existing processes with `taskkill /F /IM node.exe`
- **MongoDB connection failed:** Check your `MONGODB_URI` in `config.env`
- **Module not found:** Run `npm install` in both root and client directories

---
**Tech Used:** React • Node.js • Express • MongoDB • Tailwind CSS • Socket.IO 