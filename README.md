# Employment/Task Management System

A comprehensive full-stack application for managing employees and their tasks with role-based access control, built with React, Spring Boot, and PostgreSQL.

## 🎯 Features

- **Employee Management**: Create, update, and manage employee profiles
- **Task Management**: Assign, track, and complete tasks
- **Authentication**: JWT-based authentication system
- **Role-Based Access Control (RBAC)**: Different access levels for Admin, Manager, and Employee roles
- **Real-time Updates**: Live task and employee status updates
- **Responsive Design**: Mobile-friendly UI
- **AWS Deployment**: Production-ready deployment configuration

## 📋 Tech Stack

### Frontend
- React 18.x
- Redux Toolkit for state management
- Tailwind CSS for styling
- Axios for API calls
- React Router for navigation

### Backend
- Spring Boot 3.x
- Spring Security with JWT
- Spring Data JPA for database operations
- PostgreSQL database
- Lombok for boilerplate reduction

### Infrastructure
- Docker & Docker Compose
- AWS EC2, RDS, S3, CloudFront
- GitHub Actions for CI/CD

## 🚀 Getting Started

### Prerequisites
- Node.js 16+
- Java 17+
- PostgreSQL 13+
- Docker & Docker Compose
- AWS Account (for deployment)

### Local Development

#### Backend Setup
```bash
cd backend
./mvnw clean install
./mvnw spring-boot:run
```

Backend runs on: `http://localhost:8080`

#### Frontend Setup
```bash
cd frontend
npm install
npm start
```

Frontend runs on: `http://localhost:3000`

### Database Setup
```bash
docker-compose up -d postgres
```

## 📚 Project Structure

```
employment-task-management/
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/taskmanagement/
│   │   │   │   ├── config/
│   │   │   │   ├── controller/
│   │   │   │   ├── service/
│   │   │   │   ├── repository/
│   │   │   │   ├── entity/
│   │   │   │   ├── dto/
│   │   │   │   ├── security/
│   │   │   │   ├── exception/
│   │   │   │   └── TaskManagementApplication.java
│   │   │   └── resources/
│   │   │       └── application.yml
│   │   └── test/
│   ├── pom.xml
│   └── Dockerfile
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── store/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── index.jsx
│   ├── package.json
│   └── Dockerfile
├── docker-compose.yml
├── .github/
│   └── workflows/
│       ├── backend-ci.yml
│       └── frontend-ci.yml
└── README.md
```

## 🔐 Authentication

The system uses JWT (JSON Web Tokens) for authentication:
- Login endpoint: `POST /api/auth/login`
- Token stored in localStorage on client-side
- Token included in Authorization header for API requests
- Token expiration: 24 hours (configurable)

## 👥 Roles & Permissions

- **Admin**: Full system access, user management, role assignment
- **Manager**: Can manage employees, create and assign tasks, view reports
- **Employee**: Can view assigned tasks, update task status

## 🚀 Deployment on AWS

### Prerequisites
- AWS account with appropriate permissions
- AWS CLI configured locally

### Deployment Steps
See [AWS_DEPLOYMENT.md](./AWS_DEPLOYMENT.md) for detailed instructions.

## 📝 API Documentation

See [API_DOCUMENTATION.md](./API_DOCUMENTATION.md) for complete API endpoints and usage examples.

## 🧪 Testing

### Backend Tests
```bash
cd backend
./mvnw test
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 📊 Database Schema

See [DATABASE_SCHEMA.md](./DATABASE_SCHEMA.md) for detailed database structure.

## 🤝 Contributing

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Commit changes: `git commit -m 'Add your feature'`
3. Push to branch: `git push origin feature/your-feature`
4. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📧 Support

For support, email: support@taskmanagement.com

---

**Last Updated**: 2026-02-06
**Version**: 1.0.0