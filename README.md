# BookMitra - The Book Store Application

![GitHub license](https://img.shields.io/github/license/Uvesh-Multani/BookMitra)
![GitHub last commit](https://img.shields.io/github/last-commit/Uvesh-Multani/BookMitra)

**BookMitra** is a web-based bookstore application built with **PHP**, **MySQL**, **JavaScript**, and **CSS**. It provides a seamless experience for browsing, searching, and purchasing books online. Key features include user authentication, a shopping cart, order management, and a dedicated admin panel for managing products, orders, and user messages. The application is responsive, optimized for both desktop and mobile devices, and styled with a modern, user-friendly interface.

🔗 **Repository**: [https://github.com/Uvesh-Multani/BookMitra](https://github.com/Uvesh-Multani/BookMitra)

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Folder Structure](#folder-structure)
- [Codebase Summary](#codebase-summary)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features
- **User Authentication**: Secure registration, login, and logout for users and admins.
- **Book Catalog**: Browse and search books with a grid-based layout and dynamic search functionality.
- **Shopping Cart**: Add, update, or remove books with real-time total calculations.
- **Order Management**: Place orders, view order history, and track payment status.
- **Admin Panel**: Manage books, orders, users, and customer messages.
- **Responsive Design**: Mobile-friendly interface using CSS and Font Awesome icons.
- **Contact Form**: Users can send messages to admins, stored in the database.

## Technologies Used
- **Frontend**:
  - HTML5
  - CSS3 (`css/style.css` for user pages, `css/admin_style.css` for admin panel)
  - JavaScript (`js/script.js` for user interactions, `js/admin_script.js` for admin panel)
  - Font Awesome 6.0.0 (via CDN for icons)
- **Backend**:
  - PHP (server-side logic for authentication, cart, and order management)
- **Database**:
  - MySQL (schema defined in `shop_db.sql`)
- **Tools**:
  - XAMPP/WAMP (local server environment)
  - Git (version control)

## Installation
To run **BookMitra** locally, follow these steps:

### Prerequisites
- XAMPP/WAMP or any PHP-compatible server (Apache recommended)
- MySQL database server
- Git for cloning the repository
- A modern web browser (e.g., Chrome, Firefox)

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Uvesh-Multani/BookMitra.git

2. **Navigate to the Project Directory**:
```bash

cd BookMitra
```

Set Up the Web Server:
Copy the BookMitra folder to your XAMPP/WAMP htdocs directory (e.g., C:/xampp/htdocs/BookMitra).

Start Apache and MySQL from the XAMPP/WAMP control panel.

Configure the Database:
See the Database Setup (#database-setup) section below.

Update Configuration:
Open config.php and verify/update the database credentials:
php

$conn = mysqli_connect('localhost', 'root', '', 'shop_db') or die('connection failed');

Access the Application:
Open a browser and navigate to http://localhost/BookMitra.

The homepage (home.php) should load.

Database Setup
Open phpMyAdmin (http://localhost/phpmyadmin).

Create a new database named shop_db.

Import the shop_db.sql file from the repository root to set up the required tables.

Verify the database connection settings in config.php.

Database Schema (from shop_db.sql)
cart: Stores cart items (id, user_id, name, price, quantity, image).

message: Stores user messages (id, user_id, name, email, number, message).

orders: Stores order details (id, user_id, name, number, email, method, address, total_products, total_price, placed_on, payment_status).

products: Stores book details (id, name, price, image).

users: Stores user details (id, name, email, password, user_type).

Folder Structure
The folder structure of BookMitra, as hosted on https://github.com/Uvesh-Multani/BookMitra, is as follows:

BookMitra/
├── css/
│   ├── admin_style.css        # Admin panel styles
│   └── style.css             # Main application styles
├── images/
│   ├── heading-bg.webp       # Background image for headings
│   ├── Isaac Asimov.webp     # Author image
│   ├── J.K. Rowling.webp     # Author image
│   ├── Jessica Barry.webp    # Author image
│   ├── Jhon Collins.webp     # Author image
│   ├── Robin Sharma.webp     # Author image
│   ├── Victoria Aveyard.webp # Author image
├── js/
│   ├── admin_script.js       # Admin panel JavaScript
│   └── script.js             # Main application JavaScript
├── uploaded_img/             # Directory for uploaded book images
├── about.php                 # About page
├── add_to_cart.php           # Script to add items to cart
├── admin_contacts.php        # Admin page for managing messages
├── admin_header.php          # Admin panel header
├── admin_orders.php          # Admin page for managing orders
├── admin_page.php            # Admin dashboard
├── admin_products.php        # Admin page for managing products
├── admin_users.php           # Admin page for managing users
├── cart.php                  # Shopping cart page
├── checkout.php              # Checkout page
├── config.php                # Database connection configuration
├── contact.php               # Contact page
├── footer.php                # Common footer
├── header.php                # Common header
├── home.php                  # Homepage
├── login.php                 # Login page
├── logout.php                # Logout script
├── orders.php                # User orders page
├── register.php              # Registration page
├── search_page.php           # Search page
├── shop.php                  # Shop page with all products
├── shop_db.sql               # Database schema
├── README.md                 # Project documentation

Explore the full structure on GitHub: https://github.com/Uvesh-Multani/BookMitra.
Codebase Summary
Using Gitingest (https://gitingest.com), the BookMitra codebase was analyzed:
Repository: uvesh-multani/bookmitra

Files Analyzed: 34

Estimated Tokens: 25.4k

Exclusions: *.md files and src/ directory

File Size Limit: Files under 50kb

Key Components
PHP Files: Handle backend logic for:
Authentication (login.php, register.php)

Cart management (cart.php, add_to_cart.php)

Checkout (checkout.php)

Admin functionalities (admin_page.php, admin_products.php, etc.)

CSS Files: 
style.css: User-facing page styles with a purple-themed design.

admin_style.css: Admin panel styles, using the Rubik font.

JavaScript Files:
script.js: Toggles menus and user boxes on user pages.

admin_script.js: Handles admin panel interactions (e.g., navbar toggling).

SQL File: shop_db.sql defines the MySQL schema for five tables.

Images: Author images and background images in images/.

For a detailed text digest of the codebase, visit https://gitingest.com/Uvesh-Multani/BookMitra or replace "hub" with "ingest" in the GitHub URL (e.g., https://gitingest.com/Uvesh-Multani/BookMitra).
Usage
For Users:
Register or log in via register.php or login.php.

Browse books on shop.php or search via search_page.php.

Add books to the cart (cart.php) and proceed to checkout (checkout.php).

View order history on orders.php.

Send messages to admins via contact.php.

For Admins:
Log in with admin credentials to access admin_page.php.

Manage products (admin_products.php), orders (admin_orders.php), users (admin_users.php), and messages (admin_contacts.php).

Contributing
Contributions are welcome! To contribute:
Fork the repository: https://github.com/Uvesh-Multani/BookMitra.

Create a new branch:
bash

git checkout -b feature-branch

Commit your changes:
bash

git commit -m "Add feature"

Push to the branch:
bash

git push origin feature-branch

Open a pull request on GitHub.

Please include clear documentation and ensure code aligns with the project’s PHP and CSS standards.
## License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
### For questions, suggestions, or feedback:
**GitHub**: Uvesh-Multani

**Email**: cypronium2004@gmail.com

**Issues**: https://github.com/Uvesh-Multani/BookMitra/issues

