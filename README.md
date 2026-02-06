# Employment Task Management

## Tech Stack
- **Frontend**: [React](https://reactjs.org/), [Redux](https://redux.js.org/)
- **Backend**: [Node.js](https://nodejs.org/), [Express](https://expressjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/)
- **Deployment**: [Heroku](https://www.heroku.com/) / [AWS](https://aws.amazon.com/)

## Features
- User authentication
- Task creation, updating, and deletion
- Task prioritization and deadline settings
- User roles and permissions
- Dashboard for task overview

## Architecture
The application follows a typical microservices architecture with separate services for the frontend and backend enabling scalability and maintainability.

## Quick Start
1. Clone the repository:
    ```bash
    git clone https://github.com/github-saba/employment-task-management.git
    cd employment-task-management
    ```
2. Install dependencies for the backend:
    ```bash
    cd backend
    npm install
    ```
3. Set up environment variables (refer to `.env.example`).
4. Start the backend server:
    ```bash
    npm start
    ```
5. Install dependencies for the frontend:
    ```bash
    cd ../frontend
    npm install
    ```
6. Start the frontend application:
    ```bash
    npm start
    ```

## Project Structure
```
employment-task-management/
│
├── backend/               # Backend server
│   ├── routes/            # API routes
│   ├── models/            # Database models
│   └── controllers/       # Business logic
│
└── frontend/              # Frontend application
    ├── components/        # React components
    ├── redux/             # Redux store and reducers
    └── styles/            # CSS styles
```