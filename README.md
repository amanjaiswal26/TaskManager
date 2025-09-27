# Task Management System

A full-stack MERN application for managing tasks with user authentication, priority-based organization, and a modern responsive UI.

## Features

### Backend (Node.js/Express/MongoDB)
- JWT-based authentication
- RESTful API endpoints
- User registration and login
- Task CRUD operations
- Task filtering and pagination
- Priority-based task organization
- Status management (pending/completed)

### Frontend (React/Redux/Chakra UI)
- Modern, responsive UI with Chakra UI
- User authentication flow
- Dashboard with priority columns
- Task creation, editing, and deletion
- Real-time status updates
- Task filtering and search
- Mobile-friendly design

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- bcrypt for password hashing
- CORS for cross-origin requests

### Frontend
- React 19
- Redux Toolkit for state management
- React Router for navigation
- Chakra UI for components
- Axios for API calls

## Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or MongoDB Atlas)
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
```bash
cd Backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the Backend directory:
```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/taskmanager?retryWrites=true&w=majority
JWT_SECRET=your_super_secret_jwt_key_here
PORT=5000
```

4. Start the backend server:
```bash
npm run dev
```

The backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd Frontend/frontend
```

2. Install dependencies:
```bash
npm install @chakra-ui/react @emotion/react @emotion/styled framer-motion react-router-dom @reduxjs/toolkit react-redux axios
```

3. Start the frontend development server:
```bash
npm start
```

The frontend will run on `http://localhost:3000`

## API Endpoints

### Authentication
- `POST /api/v1/auth/register` - Register a new user
- `POST /api/v1/auth/login` - Login user
- `GET /api/v1/auth/me` - Get current user (protected)

### Tasks
- `GET /api/v1/tasks` - Get all tasks for logged-in user
- `GET /api/v1/tasks/:id` - Get single task
- `POST /api/v1/tasks` - Create new task
- `PUT /api/v1/tasks/:id` - Update task
- `PUT /api/v1/tasks/:id/status` - Update task status
- `DELETE /api/v1/tasks/:id` - Delete task

### Query Parameters for Tasks
- `status` - Filter by status (pending/completed)
- `priority` - Filter by priority (Low/Medium/High)
- `page` - Page number for pagination
- `limit` - Number of tasks per page

## Usage

1. **Registration**: Create a new account with name, email, and password
2. **Login**: Sign in with your credentials
3. **Dashboard**: View tasks organized by priority columns
4. **Create Tasks**: Click "Add Task" to create new tasks
5. **Edit Tasks**: Click the menu button on any task card to edit
6. **Update Status**: Toggle the switch to mark tasks as completed
7. **Filter Tasks**: Use the filter dropdowns to view specific tasks
8. **Delete Tasks**: Use the menu to delete tasks with confirmation

## Project Structure

```
ManageTask/
├── Backend/
│   ├── controllers/
│   │   ├── auth.js
│   │   └── tasks.js
│   ├── middleware/
│   │   └── auth.js
│   ├── models/
│   │   ├── User.js
│   │   └── Task.js
│   ├── routes/
│   │   ├── auth.js
│   │   └── tasks.js
│   ├── server.js
│   └── package.json
└── Frontend/
    └── frontend/
        ├── src/
        │   ├── components/
        │   │   ├── Layout.js
        │   │   ├── ProtectedRoute.js
        │   │   ├── TaskCard.js
        │   │   └── TaskModal.js
        │   ├── pages/
        │   │   ├── Dashboard.js
        │   │   ├── LoginPage.js
        │   │   └── RegisterPage.js
        │   ├── store/
        │   │   ├── index.js
        │   │   └── slices/
        │   │       ├── authSlice.js
        │   │       └── taskSlice.js
        │   └── App.js
        └── package.json
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.


