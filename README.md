# Food Delivery System

A modular, scalable backend architecture for a food delivery application system.

## Project Overview

This project implements a comprehensive food delivery system with support for customers, restaurants/vendors, delivery drivers, and administrators. The architecture follows best practices for Node.js/TypeScript backend development with a focus on modularity, scalability, and maintainability.

## Architecture

The system is designed with a modular architecture where each feature is self-contained in its own module directory. This promotes:

- **Modularity**: Each feature (restaurants, menus, users) is self-contained
- **Separation of Concerns**: Code related to controllers, services, DTOs, and entities are grouped within their respective modules
- **Scalability**: Easier to add new features or modules without impacting others
- **Maintainability**: Clear organization makes it easier to find and update code

## Project Structure

```
/src
├── app.module.ts          # Root application module
├── main.ts                # Application entry point
├── common/                # Shared utilities, constants, base classes
│   └── errors/            # Custom error classes
├── config/                # Application configuration
├── database/              # Database setup and migrations
│   └── migrations/        # SQL migration scripts
├── modules/               # Feature modules
│   ├── users/             # User module
│   ├── restaurants/       # Restaurant module
│   ├── menus/             # Menu module
│   └── orders/            # Order module
└── docs/                  # Project documentation
```

## Getting Started

### Prerequisites

- Node.js (v16 or later)
- TypeScript
- PostgreSQL (for production)

### Installation

1. Clone the repository
2. Install dependencies: `npm install`
3. Create a `.env` file based on `.env.example`
4. Start the development server: `npm run dev`

## API Endpoints

The API follows RESTful principles with the following main endpoints:

### Authentication
- `POST /api/auth/register`: Register a new user
- `POST /api/auth/login`: Login and get access token

### Users
- `GET /api/users`: Get all users (admin only)
- `GET /api/users/:id`: Get user by ID
- `PUT /api/users/:id`: Update user
- `DELETE /api/users/:id`: Delete user

### Restaurants
- `GET /api/restaurants`: Get all restaurants
- `GET /api/restaurants/:id`: Get restaurant by ID
- `POST /api/restaurants`: Create new restaurant
- `PUT /api/restaurants/:id`: Update restaurant
- `DELETE /api/restaurants/:id`: Delete restaurant

### Menu Items
- `GET /api/menus`: Get all menu items
- `GET /api/menus/:id`: Get menu item by ID
- `POST /api/menus`: Create new menu item
- `PUT /api/menus/:id`: Update menu item
- `DELETE /api/menus/:id`: Delete menu item

### Orders
- `GET /api/orders`: Get all orders
- `GET /api/orders/:id`: Get order by ID
- `POST /api/orders`: Create new order
- `PUT /api/orders/:id`: Update order
- `POST /api/orders/:id/cancel`: Cancel order

## License

MIT"# cuddly-octo-carnival" 
