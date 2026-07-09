# ePharma Frontend

Frontend application for the ePharma e-commerce platform, built with React and designed for customers, authenticated users, and admin users.

## Key Features

- Public storefront with product listings by category
- User registration and authentication
- Protected user dashboard and order history routes
- Admin dashboard for managing categories, products, and orders
- Stripe payment integration for checkout
- Cart support and prescription upload after payment

## Tech Stack

- React 17
- React Router DOM
- Stripe Checkout
- Create React App
- Fetch API for backend integration

## Project Structure

- `src/index.js` - application entry point
- `src/Routes.js` - client routing configuration
- `src/core/` - core pages and components like `Home`, `Cart`, and payment handling
- `src/user/` - authentication and user dashboard pages
- `src/admin/` - admin management pages
- `src/auth/helper/` - protected route helpers and auth utilities
- `src/backend.js` - backend API base URL configuration

## Workflow

1. User visits the home page (`/`) and browses products grouped by categories.
2. Guests can sign up (`/signup`) or sign in (`/signin`).
3. Authenticated users access their dashboard (`/user/dashboard`), edit profile (`/user/profile/edit`), and view orders (`/user/orders`).
4. Admin users access the admin dashboard (`/admin/dashboard`) and can manage categories, products, and orders.
5. Customers can add products to their cart and complete checkout using Stripe.
6. After successful payment, the app submits prescription details for the created order.

## Available Routes

- `/` - Home page
- `/signin` - Sign in page
- `/signup` - Sign up page
- `/cart` - Shopping cart page
- `/user/dashboard` - User dashboard (private)
- `/user/profile/edit` - Edit user profile (private)
- `/user/orders` - User order history (private)
- `/admin/dashboard` - Admin dashboard (admin only)
- `/admin/create/category` - Create new category (admin only)
- `/admin/categories` - Manage categories (admin only)
- `/admin/create/product` - Create new product (admin only)
- `/admin/products` - Manage products (admin only)
- `/admin/orders` - Manage orders (admin only)
- `/admin/product/update/:productId` - Update product (admin only)
- `/admin/cateory/update/:categoryId/:userId` - Update category (admin only)

## Setup

```sh
git clone git@github.com:skzaffarekbal/ePharma-frontend.git
cd ePharma-frontend
npm install
npm start
```

> Note: This frontend depends on a separate backend API. The backend must be running and available before the frontend can successfully fetch data.

## Environment Variables

Create a `.env` file in the project root and add:

```env
REACT_APP_BACKEND=<BACKEND_URL>/api
REACT_APP_STRIPEPK=<STRIPE_PUBLIC_KEY>
```

- `REACT_APP_BACKEND` should point to your backend API base URL.
- `REACT_APP_STRIPEPK` should be the Stripe publishable key from your Stripe dashboard.

## Notes

- The app uses `localStorage` to persist JWT authentication data.
- Private routes are enforced by `src/auth/helper/PrivateRoutes.js`.
- Admin-only routes are enforced by `src/auth/helper/AdminRoutes.js`.
- Stripe checkout uses `react-stripe-checkout` and submits payment details to the backend.

## License

This project is provided as-is for the ePharma frontend demo.
