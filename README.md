# E-commerce Website

A full-featured e-commerce website built with Flask, featuring user authentication, shopping cart, product catalog, and admin panel.

## Features

- **Product Catalog**: 56+ products across 6 categories (Electronics, Clothing, Books, Home & Garden, Sports & Outdoors, Beauty & Personal Care)
- **User Authentication**: Registration, login, logout functionality
- **Shopping Cart**: Add/remove items, view cart, checkout process
- **Product Details**: Individual product pages with detailed information
- **Search & Filter**: Search products by name and filter by category
- **Admin Panel**: Manage products, categories, and orders
- **Order Management**: Track user orders and order history

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

### Setup Instructions

1. **Clone or download the project**
   ```bash
   cd ecommerce-website
   ```

2. **Create a virtual environment**
   ```bash
   python3 -m venv venv
   ```

3. **Activate the virtual environment**
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Initialize the database**
   ```bash
   python setup_data.py
   ```

6. **Run the application**
   ```bash
   python app.py
   ```

7. **Access the website**
   Open your browser and go to: `http://127.0.0.1:5000`

## Default Admin Account

- **Username**: admin
- **Password**: admin123
- **Email**: admin@example.com

Use this account to access the admin panel at `/admin`

## Project Structure

```
ecommerce-website/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── setup_data.py         # Database initialization script
├── README.md             # This file
├── instance/
│   └── ecommerce.db      # SQLite database
├── templates/            # HTML templates
│   ├── base.html
│   ├── home.html
│   ├── product_detail.html
│   ├── cart.html
│   ├── checkout.html
│   ├── login.html
│   ├── register.html
│   ├── orders.html
│   └── admin.html
└── static/              # Static files (CSS, JS, images)
    ├── css/
    ├── js/
    └── images/
```

## Usage

### For Customers:
1. Browse products on the home page
2. Click on products to view details
3. Register/login to add items to cart
4. Proceed to checkout and place orders
5. View order history in the orders section

### For Administrators:
1. Login with admin credentials
2. Access admin panel at `/admin`
3. Add new products and categories
4. View and manage all orders

## Dependencies

The application uses the following Python packages:

- **Flask 2.3.3**: Web framework
- **Flask-SQLAlchemy 3.0.5**: Database ORM
- **Flask-Login 0.6.3**: User session management
- **Werkzeug 2.3.7**: WSGI utilities and password hashing
- **Stripe 5.5.0**: Payment processing (configured but not implemented)

## Database Schema

- **Users**: User accounts with authentication
- **Categories**: Product categories
- **Products**: Product catalog with images and details
- **Cart Items**: Shopping cart functionality
- **Orders & Order Items**: Order management system

## Troubleshooting

### Common Issues:

1. **ModuleNotFoundError**: Make sure virtual environment is activated and dependencies are installed
2. **Database errors**: Delete `instance/ecommerce.db` and run `python setup_data.py` again
3. **Port already in use**: Change the port in `app.py` or kill the process using port 5000

### Reset Database:
```bash
rm instance/ecommerce.db
python setup_data.py
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is for educational purposes.
