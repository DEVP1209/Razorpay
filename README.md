# Razorpay Payment Integration React Node App

## Overview
This application integrates Razorpay payment gateway into a React frontend with a Node.js backend. It allows users to make payments securely using Razorpay's services.

## Prerequisites
- Node.js installed on your machine.
- React.js installed globally or in the project.
- Razorpay account and API keys (KEY_ID and KEY_SECRET).
- Basic knowledge of React.js and Node.js.

## Setup
1. Clone or download the repository.
2. Navigate to the project directory.
3. Install dependencies:
   ```bash
   npm install
# Razorpay Payment Integration React Node App

## Setup Environment Variables
1. Create a `.env` file in the root directory.
2. Add the following environment variables:
    ```
    KEY_ID=YOUR_RAZORPAY_KEY_ID
    KEY_SECRET=YOUR_RAZORPAY_KEY_SECRET
    ```
    Replace `YOUR_RAZORPAY_KEY_ID` and `YOUR_RAZORPAY_KEY_SECRET` with your actual Razorpay API keys.

## Run the Application
```bash
npm start
```

# Backend

The backend server is responsible for handling payment orders and verifying payments through Razorpay's API.

## Server-side Code

The server-side code is located in the `server/routes/payment.js` file.

### /orders Endpoint:
- Creates a new payment order using Razorpay API.
- Expects the `amount` field in the request body to specify the order amount.
- Generates a unique receipt ID for the order.

### /verify Endpoint:
- Verifies the payment using the received parameters (`razorpay_order_id`, `razorpay_payment_id`, and `razorpay_signature`).
- Compares the signature with the expected signature using the provided secret key.

# Frontend

The frontend is a simple demo with a payment form that allows users to enter their card details and make payments.

## Client-side Code

The client-side code is located in the `src` directory.

### App.js:
- Makes a POST request to the backend `/orders` endpoint to create a payment order.
- Renders the payment form with card details.
- Handles form submission and payment processing.

# Usage

1. Open the application in your web browser.
2. Theres Just a Card
3. Click on the Buy Now button to initiate the payment process.
4. Upon successful payment, you will receive a confirmation message.

## Note

- This application is a basic implementation and may require additional features for production use, such as error handling, user authentication, and secure storage of API keys.
- Ensure to follow security best practices, such as using HTTPS, to protect sensitive information during payment transactions.

## Resources

- [Razorpay Documentation](https://razorpay.com/docs/)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [React Documentation](https://reactjs.org/docs/getting-started.html)

## License

This project is licensed under the MIT License.

Feel free to contribute or provide feedback!

