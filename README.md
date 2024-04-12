## Table of Contents

- [Models](#models)
  - [Cart](#cart)
  - [Order](#order)
  - [Product](#product)
  - [User](#user)
- [Routes](#routes)
  - [Auth](#auth)
  - [Cart](#cart-1)
  - [Order](#order-1)
  - [Product](#product-1)
  - [Stripe](#stripe)
  - [User](#user-1)
  - [Verify Token](#verify-token)
- [Server Setup](#server-setup)

---

### Models

#### Cart

The `cart.js` schema defines the structure for a user's shopping cart. It includes the user's ID (`userId`) and an array of products (`products`). Each product in the cart has a `productId` and a `quantity` indicating how many of that product the user has added to their cart. The `Cart` schema is used to model and store cart-related data in MongoDB.

#### Order

The `order.js` schema represents an order in the eCommerce system. It includes fields such as `userId` to associate the order with a user, `products` array to store the ordered products and their quantities, `amount` for the total order amount, `address` for shipping information, and `status` to track the order's status (e.g., pending, shipped). The `Order` schema is used to store order-related information in the database.

#### Product

The `product.js` schema defines the structure for products available in the eCommerce platform. It includes fields like `title`, `desc` (description), `img` (image URL), `categories` (an array of categories the product belongs to), `size`, `color`, and `price`. This schema is used to model product data and store it in the MongoDB database.

#### User

The `users.js` schema represents user data in the system. It includes fields like `username`, `email`, `password` (hashed), and `isAdmin` (a boolean indicating whether the user is an administrator). The `User` schema is used for user authentication, registration, and management within the eCommerce application.

---

### Routes

The `routes` directory organizes the API endpoints and their corresponding logic for handling various functionalities in the eCommerce application.

#### Auth

Routes related to user authentication, such as user registration (`POST /register`) and user login (`POST /login`) using JWT tokens and encryption.

#### Cart

Routes for managing a user's shopping cart, including creating, updating, deleting carts, retrieving user carts, and retrieving all carts (admin access).

#### Order

Routes for managing orders, including creating, updating, deleting orders, retrieving user orders, retrieving all orders (admin access), and calculating monthly income from orders.

#### Product

Routes for managing products, including creating, updating, deleting products, retrieving a specific product, and retrieving all products.

#### Stripe

Routes for processing payment transactions using the Stripe API.

#### User

Routes for user management, including updating user information, deleting users, retrieving specific users, retrieving all users, and retrieving user statistics.

#### Verify Token

Middleware functions for verifying JWT tokens for authentication and authorization purposes.

---

### Server Setup

Add instructions and details for setting up the server environment, including installing dependencies, configuring environment variables, and starting the server.
