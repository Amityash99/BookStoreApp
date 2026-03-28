# BookStore - Full-Stack MERN Application

## Overview

BookStore is a modern full-stack web application built with the **MERN stack** (MongoDB, Express.js, React, Node.js). It provides a platform for managing books, including browsing, user authentication, and course-related features (potentially book courses or recommendations).

- **Backend**: RESTful API for books and users with MongoDB persistence.
- **Frontend**: Responsive React app with Tailwind CSS (DaisyUI), routing, forms, and slick carousels.

## Features

### Backend
- User authentication (signup, login, logout) with bcrypt hashing.
- Book CRUD operations.
- Protected routes and middleware.
- MongoDB integration for data storage.

### Frontend
- User authentication UI (Login, Signup, Logout).
- Home page with Banner and Cards.
- Book/Course browsing (Courses.jsx, Freebook.jsx).
- Responsive navbar and footer.
- Slick carousel for book displays.
- Toast notifications and form validation (react-hook-form).
- Client-side routing.

## Tech Stack

### Backend
| Technology | Version |
|------------|---------|
| Node.js | Latest |
| Express | ^5.2.1 |
| Mongoose | ^9.3.1 |
| bcryptjs | ^3.0.3 |
| cors | ^2.8.6 |
| dotenv | ^17.3.1 |
| nodemon | ^3.1.14 |

### Frontend
| Technology | Version |
|------------|---------|
| React | ^19.2.0 |
| Vite | ^7.3.1 |
| Tailwind CSS + DaisyUI | ^4.2.1 / ^5.5.19 |
| React Router | ^7.13.1 |
| Axios | ^1.13.6 |
| React Hook Form | ^7.71.2 |
| React Hot Toast | ^2.6.0 |
| React Slick | ^0.31.0 |

## Prerequisites

- Node.js (v18+)
- MongoDB (local or Atlas URI in `.env`)
- Git

## Setup & Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd bookStore
   ```

2. **Backend Setup**
   ```bash
   cd Backend
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd ../Frontend
   npm install
   ```

4. **Environment Variables**
   Create `.env` in `Backend/`:
   ```
   PORT=4000
   mongoDBURI=your_mongodb_connection_string
   ```

5. **Run the Application**

   **Backend** (new terminal):
   ```bash
   cd Backend
   npm start
   ```
   Server runs on `http://localhost:4000`

   **Frontend** (new terminal):
   ```bash
   cd Frontend
   npm run dev
   ```
   App opens on `http://localhost:5173` (Vite default)

## API Endpoints

- `POST /user/signup` - Register user
- `POST /user/login` - Login user
- `GET /book` - Get all books
- `POST /book` - Add book
- ... (additional CRUD via controllers)

## Project Structure

```
bookStore/
├── Backend/
│   ├── controller/   # Business logic
│   ├── model/        # Mongoose schemas
│   ├── route/        # Express routes
│   ├── index.js      # Server entry
│   └── package.json
├── Frontend/
│   ├── src/
│   │   ├── components/  # UI components (Navbar, Login, etc.)
│   │   ├── context/     # Auth context
│   │   ├── home/        # Home page
│   │   └── courses/     # Courses/Books
│   ├── public/
│   ├── package.json
│   └── vite.config.js
```

## Scripts

### Backend
- `npm start` - Run with nodemon

### Frontend
- `npm run dev` - Development server
- `npm run build` - Production build
- `npm run lint` - ESLint check
- `npm run preview` - Preview build

## Troubleshooting

- **MongoDB Connection**: Ensure URI is correct and MongoDB is running.
- **CORS Issues**: Backend already configured with `cors()`.
- **Port Conflicts**: Change `PORT` in `.env`.
- **Dependencies**: Delete `node_modules` and `package-lock.json`, then `npm install`.

## Contributing

1. Fork the repo.
2. Create a feature branch.
3. Commit changes.
4. Push and open a PR.

## License

ISC License (see Backend/package.json)

---

