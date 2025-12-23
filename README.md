# 💰 Savings App API - Backend Solution

[testing api](#-testing-the-api)

[![Node.js](https://img.shields.io/badge/Node.js-18.x-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-lightgrey)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.x-green)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

> **Tutor/Developer Project**: A robust savings application backend that I built to help my students understand wallet management, transaction handling, and financial application architecture.

## 🎯 Overview

This is a production-ready savings application API that allows users to create savings plans, make payments, track progress, and manage their financial goals. Built as a teaching tool to demonstrate real-world financial app development concepts to my students.

### ✨ Key Features

- 🔐 **JWT-based Authentication** with refresh tokens
- 💳 **Paystack Integration** for payment processing (NGN)
- 📊 **Savings Plan Management** with flexible configurations
- 💰 **Wallet System** for tracking user balances
- 📈 **Transaction History** with detailed records
- ⚡ **Recurring Payments** with auto-debit support
- 🔒 **Security Best Practices** implemented throughout

## 🏗️ Architecture

```text
┌─────────────────────────────────────────────┐
│ Client │
└─────────────────────────────────────────────┘
│
┌─────────────────────────────────────────────┐
│ Express Server │
│ ┌─────────┐ ┌──────────┐ ┌────────────┐ │
│ │ Auth │ │ Savings │ │ Payments │ │
│ │ Routes │ │ Routes │ │ Routes │ │
│ └─────────┘ └──────────┘ └────────────┘ │
└─────────────────────────────────────────────┘
│
┌─────────────────────────────────────────────┐
│ Controllers & Services │
└─────────────────────────────────────────────┘
│
┌─────────────────────────────────────────────┐
│ MongoDB Database │
│ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ │
│ │Users │ │Plans │ │Trans │ │Wallet│ │
│ └──────┘ └──────┘ └──────┘ └──────┘ │
└─────────────────────────────────────────────┘

```


## 🚀 Quick Start

### Prerequisites

- Node.js 18.x or higher
- MongoDB 6.x or higher
- Paystack account (for payment processing)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/savings-app-api.git
cd savings-app-api

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env


```


### Server
```text
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
```

### Database
```text
MONGODB_URI=mongodb://localhost:27017/savings_app
```

### JWT
```text
JWT_ACCESS_SECRET=your_access_secret_key_here
JWT_REFRESH_SECRET=your_refresh_secret_key_here
JWT_ACCESS_EXPIRES_IN=15m
JWT_REFRESH_EXPIRES_IN=7d
```

### Paystack (for Nigerian payments)
```text
PAYSTACK_SECRET_KEY=your_paystack_secret_key
PAYSTACK_PUBLIC_KEY=your_paystack_public_key
PAYSTACK_BASE_URL=https://api.paystack.co
PAYSTACK_SECRET_HASH=your_webhook_secret_hash

```


### Development mode
```text
npm run dev
```

### Production mode
```text
npm start
```

### Run tests
```text
npm test
```


## 📚 API Documentation

### Swagger Documentation
Once the server is running, visit:  
**http://localhost:5000/api-docs**

---

### 🔑 Key Endpoints

```text

| Method | Endpoint                          | Description                     | Auth Required |
|------|----------------------------------|---------------------------------|--------------|
| POST | /api/v1/auth/register            | Register new user               | No           |
| POST | /api/v1/auth/login               | User login                      | No           |
| GET  | /api/v1/auth/me                  | Get current user                | Yes          |
| POST | /api/v1/savings                  | Create savings plan             | Yes          |
| GET  | /api/v1/savings                  | Get user's savings plans        | Yes          |
| POST | /api/v1/payments/initialize      | Initialize payment              | Yes          |
| GET  | /api/v1/payments/verify          | Verify payment                  | No           |

---

```

### 🔐 Authentication

All protected endpoints require a JWT token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```


## 🗄️ Database Models

### 👤 User Model

- Basic user information with authentication

- Refresh token storage for secure session management

- Email verification support

### 💰 SavingsPlan Model

- Flexible savings configurations (duration, amount, recurrence)

- Progress tracking with automatic completion detection

- Support for one-time and recurring payments

### 👛 Wallet Model

- User balance tracking

- Total savings aggregation

- Currency support (NGN by default)

### 💳 Transaction Model

- Detailed payment records

- Paystack integration for Nigerian payments

- Status tracking (pending, successful, failed)

## 🔧 Technology Stack

- Runtime: Node.js

- Framework: Express.js

- Database: MongoDB with Mongoose ODM

- Authentication: JWT with bcrypt password hashing

- Payments: Paystack API (Nigeria)

- Validation: Built-in Mongoose validation

- Security: Helmet, CORS, rate limiting ready

- Documentation: Swagger / OpenAPI

## 🛡️ Security Features

- Password hashing with bcrypt (12 rounds)

- JWT tokens with short-lived access tokens

- Refresh token rotation

- Environment-based configuration

- Input validation and sanitization

- CORS configuration

- Centralized error handling middleware

- Request rate limiting (ready for implementation)


## 🧪 Testing the API

### Using cURL

```bash
# Register a new user
curl -X POST http://localhost:5000/api/v1/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "password": "securepassword123",
    "phone": "+2348012345678"
  }'

# Create a savings plan (after authentication)
curl -X POST http://localhost:5000/api/v1/savings \
  -H "Authorization: Bearer <your_token>" \
  -H "Content-Type: application/json" \
  -d '{
    "title": "New Car Fund",
    "targetAmount": 5000000,
    "monthlyAmount": 100000,
    "durationMonths": 12
  }'

  ```
