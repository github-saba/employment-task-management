# Employment/Task Management System

A comprehensive full-stack application for managing employees and their tasks with role-based access control, built with React, Spring Boot, and PostgreSQL.
A production-ready full-stack system designed for organizations to manage employees, assign tasks, and enforce role-based access control with secure authentication.

## Features
 
  ### Core Functional Features
- Employee lifecycle management (Create, Update, Deactivate)
- Task assignment, tracking, and completion workflow
- Role-based access control (Admin, Manager, Employee)

### Security & Platform Features
- JWT-based authentication with Spring Security
- API-level authorization enforcement
- Responsive UI for desktop and mobile

### DevOps & Deployment
- Dockerized backend and frontend
- CI/CD pipelines using GitHub Actions
- AWS-ready deployment (EC2, RDS, S3, CloudFront)

## Tech Stack

### Frontend
- React 18.x
- Redux Toolkit for state management
- Tailwind CSS for styling
- Axios for API calls
- React Router for navigation

### Backend
- Spring Boot 3.x – REST API development with layered architecture
- Spring Security + JWT – Stateless authentication and authorization
- Spring Data JPA for database operations
- PostgreSQL – Relational data modeling with transactional integrity
- Lombok for boilerplate reduction

### Infrastructure
- Docker & Docker Compose
- AWS EC2, RDS, S3, CloudFront
- GitHub Actions for CI/CD

## Getting Started

### Prerequisites
- Node.js 16+
- Java 17+
- PostgreSQL 13+
- Docker & Docker Compose
- AWS Account (for deployment)

### Local Development

### Environment Configuration

Backend:
- Configure `application.yml` or `application-dev.yml`
- Required variables:
  - `DB_URL`
  - `DB_USERNAME`
  - `DB_PASSWORD`
  - `JWT_SECRET`

Frontend:
- Create `.env`
  - `REACT_APP_API_BASE_URL=http://localhost:8080`

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

## Project Structure

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

The backend follows a layered architecture:
- controller → REST endpoints
- service → business logic
- repository → data access
- dto → API contracts

```

## Authentication

The system uses JWT (JSON Web Tokens) for authentication:
- Login endpoint: `POST /api/auth/login`
- Token stored in localStorage on client-side
- Token included in Authorization header for API requests
- Token expiration: 24 hours (configurable)
- Token storage:
  - Currently stored in localStorage for simplicity
  - Can be migrated to HttpOnly cookies for enhanced security

## Roles & Permissions

- **Admin**: Full system access, user management, role assignment
- **Manager**: Can manage employees, create and assign tasks, view reports
- **Employee**: Can view assigned tasks, update task status

## Deployment on AWS

### Prerequisites
- AWS account with appropriate permissions
- AWS CLI configured locally

### Deployment Steps
See [AWS_DEPLOYMENT.md](./AWS_DEPLOYMENT.md) for detailed instructions.

## API Documentation

See [API_DOCUMENTATION.md](./API_DOCUMENTATION.md) for complete API endpoints and usage examples.

## Testing

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

## Database Schema

See [DATABASE_SCHEMA.md](./DATABASE_SCHEMA.md) for detailed database structure.

## Contributing

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Commit changes: `git commit -m 'Add your feature'`
3. Push to branch: `git push origin feature/your-feature`
4. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email: thiravidan@gmail.com

---

**Last Updated**: 2026-02-06
**Version**: 1.0.0
