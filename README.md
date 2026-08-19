# 🍫 Choco-f - E-Commerce Platform

A full-featured e-commerce web application for selling premium chocolates like Kit Kat and Dairy Milk.

## Features

✅ **User Authentication** - Register and login system with bcrypt password hashing
✅ **Product Catalog** - Browse Kit Kat and Dairy Milk products
✅ **Shopping Cart** - Add/remove products from cart
✅ **Order Management** - Complete checkout and order history
✅ **Admin Dashboard** - Manage products and view orders
✅ **Session Management** - Persistent user sessions
✅ **SQLite Database** - Lightweight, serverless database
✅ **Responsive Design** - Mobile-friendly interface

## Tech Stack

- **Backend**: Node.js + Express.js
- **Frontend**: EJS templates + HTML/CSS
- **Database**: SQLite3
- **Authentication**: bcryptjs
- **Session Management**: express-session

## Getting Started

### Prerequisites
- Node.js v14+
- npm

### Installation

1. Clone the repository:
```bash
git clone https://github.com/kavinjul6-arch/Choco-f.git
cd Choco-f
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

The application will run on `http://localhost:3000`

### Development

For development with auto-reload:
```bash
npm run dev
```

## Project Structure

```
Choco-f/
├── config/
│   └── database.js          # SQLite configuration
├── routes/
│   ├── products.js          # Product routes
│   ├── cart.js              # Shopping cart routes
│   ├── auth.js              # Authentication routes
│   └── admin.js             # Admin routes
├── views/
│   ├── index.ejs            # Homepage
│   ├── products.ejs         # Product listing
│   ├── login.ejs            # Login page
│   ├── register.ejs         # Registration page
│   └── cart.ejs             # Shopping cart
├── server.js                # Main server file
├── package.json             # Dependencies
└── render.yaml              # Render deployment config
```

## API Endpoints

### Products
- `GET /products` - View all products
- `GET /products/:id` - View product details
- `GET /products/api/all` - Get products as JSON

### Authentication
- `GET /auth/login` - Login page
- `POST /auth/login` - Login user
- `GET /auth/register` - Registration page
- `POST /auth/register` - Register user
- `GET /auth/logout` - Logout user

### Shopping Cart
- `GET /cart` - View cart
- `POST /cart/add` - Add item to cart
- `POST /cart/remove/:id` - Remove item from cart
- `POST /cart/checkout` - Checkout and create order

### Admin
- `GET /admin/dashboard` - Admin dashboard (admin only)
- `POST /admin/products/add` - Add new product
- `POST /admin/products/update/:id` - Update product
- `GET /admin/orders` - View all orders

## Database Schema

### Users
- id, email, password, name, created_at

### Products
- id, name, description, price, quantity, image_url, created_at

### Cart Items
- id, user_id, product_id, quantity, added_at

### Orders
- id, user_id, total_price, status, created_at

### Order Items
- id, order_id, product_id, quantity, price

## Deployment on Render

1. Push code to GitHub
2. Go to render.com and create a new Web Service
3. Connect your GitHub repository
4. Render will automatically detect `render.yaml` and deploy
5. Your app will be live!

## Default Products

- **Kit Kat Original** - $1.99 (Crispy wafer with milk chocolate)
- **Dairy Milk** - $2.49 (Rich, creamy milk chocolate)

## Contributing

Feel free to fork this project and submit pull requests for improvements!

## License

MIT License - See LICENSE file for details

## Support

For issues or questions, please open an issue on GitHub.

---

🍫 **Enjoy your Choco-f experience!**