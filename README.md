# Food Order App

A modern food ordering application built with React for the frontend and Express.js for the backend. Users can browse available meals, add items to their cart, and place orders seamlessly.

## Features

- Browse a variety of meals with images and descriptions
- Add meals to cart with quantity management
- View cart summary with total price
- Secure checkout process with customer details validation
- Order submission with confirmation
- Responsive design for mobile and desktop

## Tech Stack

### Frontend

- React 19
- Vite (build tool)
- Context API for state management
- Custom hooks for HTTP requests

### Backend

- Node.js
- Express.js
- File-based data storage (JSON files)
- CORS enabled for frontend communication

## Installation

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Frontend Setup

1. Navigate to the root directory
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
   The frontend will be available at `http://localhost:5173`

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the backend server:
   ```bash
   npm start
   ```
   The backend will run on `http://localhost:3000`

## Usage

1. Start both frontend and backend servers as described above
2. Open your browser and navigate to the frontend URL
3. Browse available meals
4. Add desired meals to your cart
5. Proceed to checkout and fill in your details
6. Submit your order

## API Endpoints

### GET /meals

Retrieves all available meals.

**Response:**

```json
[
  {
    "id": "1",
    "name": "Margherita Pizza",
    "price": "12.99",
    "description": "A classic pizza with fresh mozzarella, tomatoes, and basil on a thin and crispy crust.",
    "image": "margherita-pizza.jpg"
  }
]
```

### POST /orders

Submits a new order.

**Request Body:**

```json
{
  "order": {
    "items": [
      {
        "id": "1",
        "name": "Margherita Pizza",
        "price": "12.99",
        "quantity": 2
      }
    ],
    "customer": {
      "email": "john@example.com",
      "name": "John Doe",
      "street": "123 Main St",
      "postal-code": "12345",
      "city": "Anytown"
    }
  }
}
```

**Response:**

```json
{
  "message": "Order created!"
}
```

## Project Structure

```
food-order/
├── backend/
│   ├── app.js                 # Express server setup
│   ├── package.json
│   ├── data/
│   │   ├── available-meals.json  # Meal data
│   │   └── orders.json          # Order storage
│   └── public/
│       └── images/             # Meal images
├── src/
│   ├── components/             # React components
│   │   ├── Cart.jsx
│   │   ├── Checkout.jsx
│   │   ├── Meals.jsx
│   │   └── ...
│   ├── store/                  # Context providers
│   ├── hooks/                  # Custom hooks
│   └── ...
├── package.json
├── vite.config.js
└── README.md
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the ISC License.
