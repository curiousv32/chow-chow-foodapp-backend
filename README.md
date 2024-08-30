# Chow Chow Food Ordering App - Backend

Welcome to the backend repository of the **Chow Chow Food Ordering App**! This backend is responsible for handling API requests, managing the database, processing payments with Stripe, and facilitating the core functionality of the application.

## Overview

The backend of the Chow Chow Food Ordering App is built with **Node.js** and **Express**. It interfaces with a **MongoDB** database and uses **Stripe** for payment processing. This repository contains all the necessary logic for managing restaurants, processing orders, and handling user authentication.

## Live Application

You can try out the live application here: [Chow Chow Live App](https://chow-chow-foodapp-frontend.onrender.com)

## Features

- **User Authentication**: Secure user registration and login with JWT.
- **Restaurant Management**: Create, edit, and delete restaurant details.
- **Order Management**: Place, update, and track orders.
- **Payment Processing**: Integrated with Stripe for secure payments.
- **Real-time Updates**: Order status updates are reflected in real-time.

## Technologies Used

- **Node.js**: Backend runtime environment
- **Express**: Web framework for Node.js
- **MongoDB**: NoSQL database for storing user and restaurant data
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB and Node.js
- **Stripe**: Payment processing service
- **JWT**: JSON Web Tokens for authentication

## Setup and Installation

To set up the backend on your local machine, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/curiousv32/chow-chow-foodapp-backend.git
cd chow-chow-backend
```

```markdown
## 2. Install Dependencies

```bash
npm install
```

## 3. Environment Variables

Create a `.env` file in the root of the project and add the following environment variables:

```bash
PORT=5000
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-secret-key
STRIPE_SECRET_KEY=your-stripe-secret-key
FRONTEND_URL=https://chow-chow-foodapp-frontend.onrender.com
```

## 4. Start the Server

To start the development server, run:

```bash
npm run dev
```

This command will start the server using `nodemon` and also initiate Stripe's local webhook listener if needed.

## 5. Testing the API

You can use tools like Postman or Insomnia to test the API endpoints. Make sure your backend is running, and then use the following base URL for API requests:

```bash
http://localhost:5000/api
```

## 6. Stripe Webhooks

For payment processing, Stripe webhooks are set up to handle events such as payment completion. Ensure you configure Stripe to send events to your server:

```bash
stripe listen --forward-to localhost:5000/api/stripe/webhook
```

## API Endpoints

- **/api/auth/**: User authentication routes (register, login)
- **/api/restaurants/**: CRUD operations for restaurants
- **/api/orders/**: Order creation and management
- **/api/stripe/**: Payment processing routes

## Deployment

The backend can be deployed on services like **Heroku**, **Render**, or **Vercel**. Ensure you configure your environment variables appropriately for the production environment.

### Example Deployment on Render

1. **Connect your repository** to Render.
2. **Set environment variables** in the Render dashboard.
3. **Deploy the service** and ensure the backend is correctly linked to your frontend.

## Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request. Ensure your code follows the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License.

## Contact

For any questions or issues, feel free to reach out:

**Email**: curiousv32@gmail.com
```
