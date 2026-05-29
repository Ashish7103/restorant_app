# 🍽️ Restaurant MERN WebApp

A full-stack restaurant web application built with the MERN (MongoDB, Express, React, Node.js) stack. This application provides both an **Admin Panel** for managing menu items and orders, and a **User Panel** for browsing and ordering food.

---

## 🔗 Live Demo & Video

- **[Live Demo](https://remarkable-babka-0dbfaa.netlify.app/)** - Visit the deployed application
- **[Video Demo](https://drive.google.com/file/d/153OBLRB7-Ey3nS_Z08EEEvJZyuQc75rP/view?usp=sharing)** - Watch a walkthrough of the features

---

## 📋 Table of Contents

- [About](#-about)
- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Getting Started](#-getting-started)
- [Installation](#-installation)
- [Running the Application](#-running-the-application)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 About

This is a complete restaurant management system that allows customers to browse menu items, place orders, and manage their cart. The admin panel enables restaurant staff to:

- Manage menu items (add, edit, delete)
- Track and manage customer orders
- Monitor restaurant operations
- View order history and analytics

The application is fully responsive and optimized for both desktop and mobile devices.

---

## 🛠️ Tech Stack

### Frontend
- **React.js** - User interface library
- **HTML5** - Markup language
- **CSS3** - Styling and responsive design
- **JavaScript (ES6+)** - Client-side logic

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling

### Database
- **MongoDB** - Cloud database solution

---

## ✨ Features

### User Panel
- ✅ Browse restaurant menu with images and descriptions
- ✅ Filter and search menu items
- ✅ Add items to cart and manage quantities
- ✅ Secure checkout process
- ✅ Order tracking and history
- ✅ User authentication and profile management
- ✅ Responsive mobile-friendly interface

### Admin Panel
- ✅ Dashboard with order summary
- ✅ Menu management (CRUD operations)
- ✅ Order management and status updates
- ✅ View customer details and order history
- ✅ Analytics and reporting
- ✅ Admin authentication

---

## 📁 Project Structure

```
restorant_app/
├── frontend/                    # React frontend application
│   ├── public/                 # Static files
│   ├── src/
│   │   ├── components/         # React components
│   │   ├── pages/              # Page components
│   │   ├── styles/             # CSS files
│   │   ├── App.js              # Main App component
│   │   └── index.js            # Entry point
│   ├── package.json            # Frontend dependencies
│   └── README.md               # Frontend-specific docs
│
├── backend/                     # Node.js & Express backend
│   ├── models/                 # MongoDB schemas
│   ├── routes/                 # API routes
│   ├── controllers/            # Route controllers
│   ├── middleware/             # Custom middleware
│   ├── config/                 # Configuration files
│   ├── server.js               # Server entry point
│   ├── package.json            # Backend dependencies
│   └── .env.example            # Environment variables template
│
└── README.md                    # This file
```

---

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14 or higher) - [Download](https://nodejs.org/)
- **npm** (v6 or higher) - Comes with Node.js
- **MongoDB** account - [Create a free cluster](https://www.mongodb.com/cloud/atlas)
- **Git** - [Download](https://git-scm.com/)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Ashish7103/restorant_app.git
cd restorant_app
```

### 2. Set Up Backend

```bash
cd backend
npm install
```

### 3. Set Up Frontend

```bash
cd ../frontend
npm install
```

---

## ⚙️ Installation

### Backend Installation

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory and add your environment variables (see [Environment Variables](#-environment-variables) section)

4. Verify the installation:
   ```bash
   npm list
   ```

### Frontend Installation

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file if needed for API configuration

4. Verify the installation:
   ```bash
   npm list
   ```

---

## 🎯 Running the Application

### Development Mode

#### Run Backend (Terminal 1)
```bash
cd backend
npm start
# or for development with auto-reload
npm run dev
```
The backend server will run on **http://localhost:5000**

#### Run Frontend (Terminal 2)
```bash
cd frontend
npm start
```
The frontend will automatically open at **http://localhost:3000**

### Production Build

#### Build Frontend
```bash
cd frontend
npm run build
```
This creates an optimized production build in the `build/` folder.

#### Deploy Backend
Follow your hosting provider's deployment guidelines for Node.js applications.

---

## 🔐 Environment Variables

### Backend `.env` File

Create a `.env` file in the `backend/` directory:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=your_mongodb_connection_string
DB_NAME=restaurant_db

# Authentication
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d

# Email Configuration (Optional)
EMAIL_HOST=your_email_host
EMAIL_PORT=your_email_port
EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password

# Frontend URL
FRONTEND_URL=http://localhost:3000
```

### Frontend `.env` File (Optional)

Create a `.env` file in the `frontend/` directory:

```env
REACT_APP_API_URL=http://localhost:5000
```

---

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Menu Items
- `GET /api/menu` - Get all menu items
- `GET /api/menu/:id` - Get menu item by ID
- `POST /api/menu` - Create menu item (Admin only)
- `PUT /api/menu/:id` - Update menu item (Admin only)
- `DELETE /api/menu/:id` - Delete menu item (Admin only)

### Orders
- `POST /api/orders` - Create new order
- `GET /api/orders` - Get user orders
- `GET /api/orders/:id` - Get order details
- `PUT /api/orders/:id` - Update order status (Admin only)

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

---

## 🧪 Testing

### Run Frontend Tests
```bash
cd frontend
npm test
```

### Run Backend Tests (if configured)
```bash
cd backend
npm test
```

---

## 🚢 Deployment

### Deploy Frontend to Netlify
1. Build the frontend: `npm run build`
2. Connect your GitHub repo to Netlify
3. Set build command: `npm run build`
4. Set publish directory: `build`

### Deploy Backend to Heroku (or similar)
1. Create a Procfile in the backend directory
2. Push to your hosting platform
3. Set environment variables in the hosting platform

---

## 📝 Contributing

Contributions are welcome! Here's how to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Ashish** - [@Ashish7103](https://github.com/Ashish7103)

---

## 📞 Support & Contact

For issues, questions, or suggestions:
- Open an [Issue](https://github.com/Ashish7103/restorant_app/issues)
- Check existing documentation
- Review the [video demo](https://drive.google.com/file/d/153OBLRB7-Ey3nS_Z08EEEvJZyuQc75rP/view?usp=sharing)

---

## 🙏 Acknowledgments

- React.js community and documentation
- MongoDB for the database solution
- All contributors and users of this project

---

**Happy Coding! 🚀**
