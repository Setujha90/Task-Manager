# 🚀 Task Management System

<div align="center">

![Task Manager](https://img.shields.io/badge/Task-Manager-blue?style=for-the-badge)
![MERN Stack](https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge)
![Hacktoberfest](https://img.shields.io/badge/Hacktoberfest-2024-orange?style=for-the-badge)

**A modern, responsive task management application built with the MERN stack**

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [API](#-api-documentation) • [Contributing](#-contributing)

</div>

---

## 📋 Project Overview

The **Task Management System** is a full-stack web application designed to help individuals and teams organize their work efficiently. Built with modern web technologies, it provides a seamless experience for managing projects, tracking tasks, and collaborating with team members.

### 🎯 What Makes This Special?

- **🔐 Secure Authentication**: JWT-based user authentication with bcrypt password hashing
- **📱 Responsive Design**: Tailwind CSS ensures perfect display across all devices
- **⚡ Real-time Updates**: Instant task status updates and project synchronization
- **🎨 Modern UI/UX**: Clean, intuitive interface with custom icons and smooth transitions
- **🔍 Advanced Filtering**: Search and filter tasks by status, priority, and deadlines
- **🐳 Docker Ready**: Complete containerization for easy deployment

---

## 🌟 Features

### 👤 User Management
- **Secure Registration & Login** with email validation
- **JWT Authentication** with secure cookie handling
- **Protected Routes** ensuring data privacy
- **Password Reset** functionality (planned)

### 📁 Project Management
- **Create & Organize** projects with descriptions
- **Update & Delete** projects with associated tasks
- **Project-based Task Filtering** for better organization
- **Visual Project Cards** with responsive grid layout

### ✅ Task Management
- **Create Tasks** with deadlines, priorities, and project assignment
- **Status Tracking**: Pending ↔ Completed with visual indicators
- **Priority Levels**: Low, Medium, High with color coding
- **Task Search** and filtering capabilities
- **Bulk Operations** for efficient management

### 🎨 User Experience
- **Responsive Navbar** with active link highlighting
- **Dashboard Overview** with task count summaries
- **Toast Notifications** for user feedback
- **Loading States** and error handling
- **Mobile-First Design** with hamburger menu

---

## 🛠️ Technology Stack

### Frontend
<div>
  <img src="https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react&logoColor=white" alt="React" />
  <img src="https://img.shields.io/badge/React_Router-6.26.2-CA4245?style=for-the-badge&logo=react-router&logoColor=white" alt="React Router" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-3.4.13-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/React_Icons-5.3.0-E10051?style=for-the-badge&logo=react&logoColor=white" alt="React Icons" />
  <img src="https://img.shields.io/badge/React_Toastify-10.0.5-45CC11?style=for-the-badge&logo=react&logoColor=white" alt="React Toastify" />
</div>

### Backend
<div>
  <img src="https://img.shields.io/badge/Node.js-Latest-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-4.21.0-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" />
  <img src="https://img.shields.io/badge/MongoDB-Latest-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Mongoose-8.7.0-880000?style=for-the-badge&logo=mongoose&logoColor=white" alt="Mongoose" />
  <img src="https://img.shields.io/badge/JWT-9.0.2-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT" />
  <img src="https://img.shields.io/badge/Bcrypt-5.1.1-3178C6?style=for-the-badge&logo=npm&logoColor=white" alt="Bcrypt" />
  <img src="https://img.shields.io/badge/Zod-3.23.8-2D4A87?style=for-the-badge&logo=zod&logoColor=white" alt="Zod" />
</div>

### DevOps & Tools
<div>
  <img src="https://img.shields.io/badge/Docker-Latest-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Docker_Compose-Latest-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Compose" />
  <img src="https://img.shields.io/badge/CORS-2.8.5-FF6B6B?style=for-the-badge&logo=npm&logoColor=white" alt="CORS" />
  <img src="https://img.shields.io/badge/Nodemon-3.1.7-76D04B?style=for-the-badge&logo=nodemon&logoColor=white" alt="Nodemon" />
</div>

---

## 🏗️ Project Architecture

```
Task-Manager/
├── 📁 Task-Management-Backend/          # Node.js/Express Backend
│   ├── 📁 config/                       # Environment configurations
│   ├── 📁 controllers/                  # Route controllers
│   │   ├── auth-controllers.js          # Authentication logic
│   │   ├── project-controllers.js       # Project CRUD operations
│   │   ├── task-controllers.js          # Task management
│   │   └── healthcheck-controllers.js   # Health monitoring
│   ├── 📁 middlewares/                  # Custom middleware
│   │   ├── auth-middleware.js           # JWT verification
│   │   └── zod-validator-middleware.js  # Request validation
│   ├── 📁 models/                       # MongoDB schemas
│   │   ├── user-models.js               # User schema
│   │   ├── project-models.js            # Project schema
│   │   └── task-models.js               # Task schema
│   ├── 📁 routes/                       # API routes
│   ├── 📁 utils/                        # Utility functions
│   ├── 📁 lib/                          # Libraries and helpers
│   ├── server.js                        # Entry point
│   └── 🐳 Dockerfile                    # Backend containerization
├── 📁 task-manager-ui/                  # React Frontend
│   ├── 📁 public/                       # Static assets
│   ├── 📁 src/
│   │   ├── 📁 components/               # Reusable components
│   │   │   ├── Dashboard.jsx            # Main dashboard
│   │   │   ├── TaskList.jsx             # Task management
│   │   │   ├── ProjectList.jsx          # Project overview
│   │   │   ├── Navbar.jsx               # Navigation
│   │   │   ├── Login.jsx                # Authentication
│   │   │   └── ...                      # Other components
│   │   ├── 📁 hooks/                    # Custom React hooks
│   │   │   └── useResponsive.jsx        # Responsive breakpoints
│   │   ├── 📁 assets/                   # Images and icons
│   │   ├── App.jsx                      # Main application
│   │   ├── config.js                    # API configuration
│   │   └── App.css                      # Global styles
│   ├── tailwind.config.js               # Tailwind configuration
│   └── 🐳 Dockerfile                    # Frontend containerization
├── 🐳 docker-compose.yml                # Multi-container setup
└── 📖 README.md                         # Project documentation
```

---

## 🚀 Quick Start

### Prerequisites
- **Node.js** (v16 or higher)
- **MongoDB** (local or cloud)
- **Git**

### Option 1: Docker Deployment (Recommended)

```bash
# Clone the repository
git clone https://github.com/LakshmiSowmya04/Task-Manager.git
cd Task-Manager

# Start all services with Docker Compose
docker-compose up --build

# Access the application
# Frontend: http://localhost:3000
# Backend: http://localhost:5000
# MongoDB: localhost:27017
```

### Option 2: Manual Installation

#### Backend Setup
```bash
cd Task-Management-Backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Edit .env with your configurations

# Start development server
npm run dev
```

#### Frontend Setup
```bash
cd task-manager-ui

# Install dependencies
npm install

# Start development server
npm start
```

---

## 🔧 Environment Configuration

### Backend (.env)
```env
JWT_SECRET=your_super_secret_jwt_key
PORT=5000
MONGODB_URI=mongodb://localhost:27017/taskmanager
```

### Frontend (config.js)
```javascript
export const backendApi = "http://localhost:5000";
```

---

## 📊 API Documentation

### Authentication Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/user/register` | User registration |
| POST | `/api/v1/user/login` | User login |
| GET | `/api/v1/user/profile` | Get user profile |

### Project Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/projects` | Get user projects |
| POST | `/api/v1/projects` | Create new project |
| GET | `/api/v1/projects/:id` | Get project by ID |
| PUT | `/api/v1/projects/:id` | Update project |
| DELETE | `/api/v1/projects/:id` | Delete project |

### Task Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/tasks` | Get all tasks |
| POST | `/api/v1/tasks` | Create new task |
| GET | `/api/v1/tasks/p/:projectId` | Get tasks by project |
| GET | `/api/v1/tasks/t/:taskId` | Get task by ID |
| PUT | `/api/v1/tasks/t/:taskId` | Update task |
| DELETE | `/api/v1/tasks/t/:taskId` | Delete task |

---

## 🤝 Contributing

We welcome contributions from developers of all skill levels! This project is participating in **Hacktoberfest 2024**.

### How to Contribute

1. **Fork the Repository**
   ```bash
   git fork https://github.com/LakshmiSowmya04/Task-Manager.git
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make Your Changes**
   - Add new features
   - Fix bugs
   - Improve documentation
   - Enhance UI/UX

4. **Commit Your Changes**
   ```bash
   git commit -m "Add: Amazing new feature"
   ```

5. **Push and Create PR**
   ```bash
   git push origin feature/amazing-feature
   ```

### 🎯 Contribution Ideas

- 🔍 **Search & Filter**: Enhanced task filtering options
- 📱 **Mobile App**: React Native version
- 🔔 **Notifications**: Real-time notifications system
- 📊 **Analytics**: Task completion analytics
- 🎨 **Themes**: Dark/Light mode toggle
- 🌐 **i18n**: Multi-language support
- 📧 **Email**: Email notifications for deadlines
- 📈 **Reports**: Progress tracking and reports

### Join Our Community
- 💬 [Discord Channel](https://discord.gg/nxD63YsJ)
- 🐛 [Issue Tracker](https://github.com/LakshmiSowmya04/Task-Manager/issues)
- 📖 [Contribution Guidelines](https://github.com/LakshmiSowmya04/Task-Manager/blob/main/CONTRIBUTING.md)

---

## 📸 Screenshots

### Dashboard Overview
> Clean, intuitive dashboard showing task summaries and quick actions

### Project Management
> Organize work into projects with detailed descriptions and task counts

### Task Management
> Comprehensive task creation with priorities, deadlines, and status tracking

### Responsive Design
> Perfect display across desktop, tablet, and mobile devices

---

## 🚧 Roadmap

- [ ] **Real-time Collaboration** - Multi-user project collaboration
- [ ] **File Attachments** - Upload files to tasks
- [ ] **Time Tracking** - Built-in time tracking for tasks
- [ ] **Calendar Integration** - Sync with Google Calendar
- [ ] **Advanced Analytics** - Productivity insights and reports
- [ ] **Mobile Apps** - iOS and Android applications
- [ ] **API Keys** - Third-party integrations
- [ ] **Webhooks** - External service notifications

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 💝 Acknowledgments

- **Contributors**: Thank you to all our amazing contributors!
- **Hacktoberfest**: Proud participant in Hacktoberfest 2024
- **Open Source**: Built with ❤️ for the open source community

---

<div align="center">

**[⭐ Star this repository](https://github.com/LakshmiSowmya04/Task-Manager) if you found it helpful!**

Made with ❤️ by [LakshmiSowmya04](https://github.com/LakshmiSowmya04) and contributors

</div>
