# E-Commerce Backend

This is the backend for an e-commerce application built using Node.js and Express.js, with MongoDB as the database. The backend provides RESTful APIs to manage users, products, orders, and more.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [Usage](#usage)
- [Package Descriptions](#package-descriptions)
- [License](#license)

## Features

- User authentication (JWT-based)
- Product management (CRUD)
- Shopping cart functionality
- Order management
- Wishlist functionality
- Product reviews and ratings
- Coupon and discount system
- Admin dashboard
- Inventory management
- Multi-language support

## Project Structure

```
backend/
├── config/
│   ├── db.js             # MongoDB connection setup
│   ├── dotenv.js         # Environment variables configuration
├── controllers/
│   ├── authController.js  # User authentication logic
│   ├── productController.js # Product management logic
│   ├── orderController.js   # Order management logic
│   ├── wishlistController.js # Wishlist logic
├── middleware/
│   ├── authMiddleware.js  # JWT authentication middleware
│   ├── errorMiddleware.js  # Error handling middleware
├── models/
│   ├── User.js           # User model
│   ├── Product.js        # Product model
│   ├── Order.js          # Order model
│   ├── Coupon.js         # Coupon model
├── routes/
│   ├── authRoutes.js     # Authentication routes
│   ├── productRoutes.js   # Product routes
│   ├── orderRoutes.js     # Order routes
│   ├── wishlistRoutes.js   # Wishlist routes
├── utils/
│   ├── sendEmail.js      # Utility for sending emails
│   ├── logger.js          # Logging utility
├── .env                   # Environment variables
├── server.js              # Entry point of the application
├── package.json           # Node.js dependencies and scripts
```

## Technologies

- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Tokens (JWT)
- bcryptjs
- dotenv
- Multer (for file uploads)
- Nodemailer (for email sending)
- Helmet (for security)
- Morgan (for logging)
- Cors (for handling cross-origin requests)
- Compression (for response compression)
- Winston (for logging)
- Express-Async-Handler (for handling async route handlers)

## Installation

### Backend Setup

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd backend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up the database:**
   - Create a MongoDB database and update the connection string in the `.env` file.

4. **Run the server:**
   ```bash
   npm run dev
   ```

### Environment Variables

Create a `.env` file in the root of your project and add the following variables:

```plaintext
PORT=5000
MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
NODE_ENV=development
```

### API Endpoints

Below are some of the primary API endpoints available in this backend:

#### Authentication

- **POST /api/auth/register** - Register a new user.
- **POST /api/auth/login** - Login a user.

#### Products

- **GET /api/products** - Get all products.
- **GET /api/products/:id** - Get a single product by ID.
- **POST /api/products** - Create a new product (Admin).
- **PUT /api/products/:id** - Update a product (Admin).
- **DELETE /api/products/:id** - Delete a product (Admin).

#### Orders

- **POST /api/orders** - Create a new order.
- **GET /api/orders/:id** - Get an order by ID.
- **GET /api/orders** - Get all orders (Admin).

#### Wishlist

- **POST /api/wishlist/add** - Add a product to the wishlist.
- **GET /api/wishlist** - Get the user's wishlist.

## Usage

To test the API endpoints, you can use tools like [Postman](https://www.postman.com/) or [Insomnia](https://insomnia.rest/). Make sure to include the JWT token in the authorization header for protected routes.

## Package Descriptions

Here’s a breakdown of the key packages used in this backend application:

1. **express**: A minimal web framework for building web applications in Node.js.
2. **mongoose**: An ODM library that provides a schema-based solution for MongoDB interaction.
3. **bcryptjs**: A library for hashing passwords to securely store user credentials.
4. **jsonwebtoken**: A library for generating and verifying JSON Web Tokens for authentication.
5. **cookie-parser**: Middleware for parsing cookies attached to client requests.
6. **express-validator**: Middleware for validating and sanitizing request data.
7. **dotenv**: A zero-dependency module for managing environment variables.
8. **multer**: Middleware for handling file uploads in `multipart/form-data`.
9. **morgan**: An HTTP request logger middleware for logging incoming requests.
10. **nodemailer**: A module for sending emails easily.
11. **cors**: Middleware for enabling Cross-Origin Resource Sharing (CORS).
12. **helmet**: Middleware for securing Express applications by setting various HTTP headers.
13. **compression**: Middleware for compressing HTTP responses.
14. **winston**: A versatile logging library for logging application-level information.
15. **express-async-handler**: Middleware for handling asynchronous route handlers and avoiding repetitive try-catch blocks.

