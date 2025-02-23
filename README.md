Online Banking API

Overview

Welcome to the Online Banking API, which provides secure access to banking services, including account management, fund transfers, and transaction history. This API follows the OpenAPI 3.0.3 specification and uses JWT-based authentication.

API Specifications

Version: 1.0.0

OpenAPI Version: 3.0.3

Contact: support@bank.com

Base URLs

Production: https://api.bank.com/v1

Staging: https://staging.api.bank.com/v1

Authentication

This API uses JWT Bearer Authentication. To access protected routes, include the JWT token in the Authorization header:

Authorization: Bearer <your_token_here>

Endpoints

Authentication

POST /auth/login - Authenticate and receive a JWT token.

POST /auth/logout - Log out and invalidate the JWT token.

Account Management

GET /accounts/{id} - Retrieve account details by ID.

PUT /accounts/{id} - Update account information.

Transactions

POST /transactions/transfer - Initiate a fund transfer.

GET /transactions/history - Retrieve transaction history.

Request & Response Examples

Login Request

{
  "email": "john.doe@example.com",
  "password": "securepassword"
}

Login Response

{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}

Error Response

{
  "message": "Invalid token",
  "errorCode": 401
}

Security

This API enforces security through JWT authentication and secure HTTPS connections.

License

This project is licensed under the MIT License.

Contact

For support, reach out to support@bank.com.
