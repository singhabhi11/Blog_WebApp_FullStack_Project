# React + Vite

# Project Name

> Replace this title and description with your actual project name and a one-line summary of what it does.

A full-stack web application built with the **MERN stack** (MongoDB, Express.js, React.js, Node.js), featuring secure authentication, image uploads via Cloudinary, and a RESTful API backend.

## Features

- User authentication with JWT (JSON Web Tokens) and password hashing via bcrypt
- Secure cookie-based session handling
- Image/file uploads handled with Multer and stored on Cloudinary
- RESTful API architecture built with Express.js
- MongoDB database integration via Mongoose
- CORS-enabled backend for cross-origin frontend communication
- Environment-based configuration using dotenv

## Tech Stack

**Backend:**
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT (jsonwebtoken) for authentication
- bcryptjs for password hashing
- Multer + Datauri + Cloudinary for file/image uploads
- cookie-parser, cors, dotenv

**Frontend:**
- React.js (located in the `frontend/` directory)

## Prerequisites

Before running this project, make sure you have installed:

- [Node.js](https://nodejs.org/) (v16 or higher recommended)
- [MongoDB](https://www.mongodb.com/) (local instance or MongoDB Atlas connection string)
- A [Cloudinary](https://cloudinary.com/) account (for image upload functionality)

## Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd <project-folder>
   ```

2. **Install dependencies and build the project**
   ```bash
   npm run build
   ```
   This installs backend dependencies, then installs and builds the frontend.

   Alternatively, install manually:
   ```bash
   npm install
   npm install --prefix frontend
   ```

3. **Set up environment variables**

   Create a `.env` file in the root directory and add the following:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```
   > Update the variable names above to match what your `backend/server.js` and config files actually expect.

## Running the Project

**Development mode** (with auto-restart via nodemon):
```bash
npm run dev
```

**Production mode:**
```bash
npm start
```

The server will start on `http://localhost:5000` (or the port specified in your `.env` file).

## Project Structure

```
.
├── backend/
│   ├── server.js        # Entry point for the Express server
│   ├── routes/          # API route definitions
│   ├── controllers/     # Route handler logic
│   ├── models/          # Mongoose schemas/models
│   ├── middleware/       # Auth middleware, error handlers, etc.
│   └── config/           # Cloudinary, database config
├── frontend/             # React frontend application
├── .env                  # Environment variables (not committed)
├── .gitignore
├── package.json
└── README.md
```
> Adjust this structure to match your actual folder layout.

## API Endpoints

> Fill in your actual routes here. Example format:

| Method | Endpoint              | Description              | Auth Required |
|--------|------------------------|---------------------------|----------------|
| POST   | `/api/auth/register`   | Register a new user       | No             |
| POST   | `/api/auth/login`      | Log in an existing user   | No             |
| POST   | `/api/auth/logout`     | Log out current user      | Yes            |
| POST   | `/api/upload`          | Upload an image to Cloudinary | Yes        |

## Scripts

| Command         | Description                                      |
|-----------------|---------------------------------------------------|
| `npm run dev`   | Runs the backend server in development mode with nodemon |
| `npm run build` | Installs backend + frontend dependencies and builds the frontend |
| `npm start`     | Runs the backend server (production/start mode)  |

## Environment Variables

| Variable                 | Description                          |
|---------------------------|---------------------------------------|
| `MONGO_URI`               | MongoDB connection string             |
| `JWT_SECRET`               | Secret key used to sign JWT tokens   |
| `CLOUDINARY_CLOUD_NAME`    | Cloudinary account cloud name        |
| `CLOUDINARY_API_KEY`       | Cloudinary API key                   |
| `CLOUDINARY_API_SECRET`    | Cloudinary API secret                |
| `PORT`                     | Port the server runs on              |

## Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -m "Add some feature"`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Author

Abhishek Singh
- GitHub: [github.com/singhabhi11](https://github.com/singhabhi11)
- LinkedIn: [linkedin.com/in/abhishek-singh-b92763288](https://linkedin.com/in/abhishek-singh-b92763288)

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
