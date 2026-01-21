
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fruits Club - Fresh Fruit Delivery</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #4CAF50;
            --primary-dark: #388E3C;
            --secondary: #FF9800;
            --light: #f9f9f9;
            --dark: #333;
            --gray: #777;
            --light-gray: #eee;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .btn-secondary {
            background: var(--secondary);
        }
        
        .btn-secondary:hover {
            background: #F57C00;
        }
        
        .btn-whatsapp {
            background: #25D366;
        }
        
        .btn-whatsapp:hover {
            background: #128C7E;
        }
        
        .btn-email {
            background: #EA4335;
        }
        
        .btn-email:hover {
            background: #D14836;
        }
        
        .btn-admin {
            background: #9C27B0;
        }
        
        .btn-admin:hover {
            background: #7B1FA2;
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            font-size: 32px;
            color: var(--primary);
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo i {
            color: var(--primary);
            font-size: 28px;
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 24px;
            color: var(--primary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .cart-icon {
            position: relative;
            cursor: pointer;
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--secondary);
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .user-avatar {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background-color: var(--primary);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        .admin-badge {
            background: #9C27B0;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            margin-left: 5px;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1619566636858-adf3ef46400b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 100px 0;
        }
        
        .hero h2 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        /* Login Section */
        .login-section, .register-section {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 60vh;
        }
        
        .login-container, .register-container {
            background: white;
            border-radius: 8px;
            padding: 40px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 400px;
        }
        
        .login-container h2, .register-container h2 {
            text-align: center;
            margin-bottom: 30px;
            color: var(--primary);
        }
        
        .login-tabs {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .login-tab {
            flex: 1;
            padding: 10px;
            text-align: center;
            cursor: pointer;
            border-bottom: 2px solid transparent;
            transition: all 0.3s;
        }
        
        .login-tab.active {
            border-bottom: 2px solid var(--primary);
            color: var(--primary);
            font-weight: bold;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            border: 1px solid var(--light-gray);
            border-radius: 4px;
            font-size: 16px;
        }
        
        .login-btn, .register-btn {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
        }
        
        .register-link, .login-link {
            text-align: center;
            margin-top: 20px;
        }
        
        .register-link a, .login-link a {
            color: var(--primary);
            text-decoration: none;
        }
        
        .register-link a:hover, .login-link a:hover {
            text-decoration: underline;
        }
        
        /* Fruits Section */
        .fruits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .fruit-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            position: relative;
        }
        
        .fruit-card:hover {
            transform: translateY(-5px);
        }
        
        .fruit-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .stock-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: bold;
        }
        
        .in-stock {
            background: var(--primary);
            color: white;
        }
        
        .out-of-stock {
            background: #f44336;
            color: white;
        }
        
        .fruit-info {
            padding: 20px;
        }
        
        .fruit-info h3 {
            margin-bottom: 10px;
            font-size: 20px;
        }
        
        .fruit-price {
            color: var(--primary);
            font-weight: bold;
            font-size: 18px;
            margin-bottom: 15px;
        }
        
        .fruit-price::before {
            content: "₹";
        }
        
        .quantity-controls {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .quantity-btn {
            background: var(--light-gray);
            border: none;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .quantity {
            margin: 0 10px;
            font-weight: bold;
        }
        
        /* Orders Section */
        .orders-section {
            background-color: var(--light);
        }
        
        .orders-container {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .order-card {
            background: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            border-left: 4px solid var(--primary);
        }
        
        .order-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .order-id {
            font-weight: bold;
            color: var(--primary);
            font-size: 18px;
        }
        
        .order-date {
            color: var(--gray);
            font-size: 14px;
        }
        
        .order-status {
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: bold;
        }
        
        .status-pending {
            background: #FFF3CD;
            color: #856404;
        }
        
        .status-ready {
            background: #D1ECF1;
            color: #0C5460;
        }
        
        .status-completed {
            background: #D4EDDA;
            color: #155724;
        }
        
        .order-details {
            margin-bottom: 15px;
        }
        
        .order-items {
            margin-bottom: 10px;
        }
        
        .order-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .order-total {
            display: flex;
            justify-content: space-between;
            font-weight: bold;
            margin-top: 10px;
            padding-top: 10px;
            border-top: 1px solid var(--light-gray);
        }
        
        .tracking-container {
            margin-top: 15px;
            padding: 15px;
            background: var(--light);
            border-radius: 8px;
        }
        
        .tracking-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .tracking-steps {
            display: flex;
            justify-content: space-between;
            position: relative;
            margin: 20px 0;
        }
        
        .tracking-steps::before {
            content: '';
            position: absolute;
            top: 15px;
            left: 0;
            right: 0;
            height: 2px;
            background: var(--light-gray);
            z-index: 1;
        }
        
        .tracking-step {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            z-index: 2;
        }
        
        .step-icon {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: white;
            border: 2px solid var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 5px;
            font-size: 14px;
        }
        
        .step-label {
            font-size: 12px;
            text-align: center;
            max-width: 80px;
        }
        
        .step-active .step-icon {
            background: var(--primary);
            border-color: var(--primary);
            color: white;
        }
        
        .step-completed .step-icon {
            background: var(--primary);
            border-color: var(--primary);
            color: white;
        }
        
        .step-completed .step-label {
            color: var(--primary);
            font-weight: bold;
        }
        
        .step-active .step-label {
            color: var(--primary);
            font-weight: bold;
        }
        
        .tracking-info {
            margin-top: 15px;
            padding: 10px;
            background: white;
            border-radius: 4px;
            font-size: 14px;
        }
        
        .no-orders {
            text-align: center;
            padding: 40px;
            color: var(--gray);
        }
        
        .area-restriction {
            background: #fff3cd;
            border: 1px solid #ffeaa7;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 30px;
            text-align: center;
        }
        
        .area-restriction h3 {
            color: #856404;
            margin-bottom: 10px;
        }
        
        .area-restriction p {
            color: #856404;
            margin-bottom: 15px;
        }
        
        /* Admin Panel - Hidden on front page */
        .admin-panel {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--dark);
            color: white;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 999;
            max-width: 300px;
            max-height: 400px;
            overflow-y: auto;
            display: none; /* Hidden by default */
        }
        
        .admin-panel.visible {
            display: block; /* Only show when admin is logged in */
        }
        
        .admin-panel h3 {
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .admin-orders {
            max-height: 200px;
            overflow-y: auto;
            margin-bottom: 15px;
        }
        
        .admin-order {
            background: rgba(255,255,255,0.1);
            padding: 8px;
            margin-bottom: 8px;
            border-radius: 4px;
            font-size: 12px;
        }
        
        .admin-order.new {
            border-left: 3px solid var(--secondary);
        }
        
        .admin-order.ready {
            border-left: 3px solid #4CAF50;
        }
        
        .order-actions {
            margin-top: 5px;
            display: flex;
            gap: 5px;
        }
        
        .order-action-btn {
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            padding: 3px 6px;
            border-radius: 3px;
            font-size: 10px;
            cursor: pointer;
        }
        
        /* Admin Dashboard */
        .admin-dashboard {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }
        
        .admin-dashboard h2 {
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .dashboard-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .stat-card {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            text-align: center;
        }
        
        .stat-value {
            font-size: 32px;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .stat-label {
            color: var(--gray);
            font-size: 14px;
        }
        
        .user-management, .product-management {
            margin-top: 30px;
        }
        
        .user-management h3, .product-management h3 {
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .product-list, .user-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .product-edit-card, .user-edit-card {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
        }
        
        .product-edit-card h4, .user-edit-card h4 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .edit-form {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .edit-form input, .edit-form select {
            padding: 8px;
            border: 1px solid var(--light-gray);
            border-radius: 4px;
        }
        
        .edit-actions {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        /* Orders Management */
        .orders-management {
            margin-top: 30px;
        }
        
        .orders-management h3 {
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .orders-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .orders-table th, .orders-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .orders-table th {
            background: var(--primary);
            color: white;
            font-weight: 600;
        }
        
        /* Users Table */
        .users-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin-top: 20px;
        }
        
        .users-table th, .users-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .users-table th {
            background: var(--primary);
            color: white;
            font-weight: 600;
        }
        
        /* Checkout Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: white;
            border-radius: 8px;
            padding: 30px;
            width: 90%;
            max-width: 600px;
            max-height: 90vh;
            overflow-y: auto;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .modal-header h2 {
            color: var(--primary);
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--gray);
        }
        
        .checkout-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        
        .checkout-form .form-group {
            margin-bottom: 15px;
        }
        
        .full-width {
            grid-column: 1 / -1;
        }
        
        .location-section {
            margin: 20px 0;
            padding: 15px;
            background: var(--light);
            border-radius: 8px;
        }
        
        .location-info {
            margin-top: 10px;
            padding: 10px;
            background: white;
            border-radius: 4px;
            font-size: 14px;
        }
        
        .order-summary {
            margin-top: 20px;
            padding: 15px;
            background: var(--light);
            border-radius: 8px;
        }
        
        .notification-options {
            margin-top: 20px;
            padding: 15px;
            background: var(--light);
            border-radius: 8px;
        }
        
        .notification-buttons {
            display: flex;
            gap: 10px;
            margin-top: 10px;
            flex-wrap: wrap;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }
        
        .contact-info {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 10px;
            color: var(--primary);
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid var(--light-gray);
            border-radius: 4px;
            font-size: 16px;
            resize: vertical;
            min-height: 120px;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 18px;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-icons a {
            color: white;
            font-size: 20px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 14px;
        }
        
        /* Notification */
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--primary);
            color: white;
            padding: 15px 20px;
            border-radius: 4px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            z-index: 1000;
        }
        
        /* Hidden sections */
        .hidden {
            display: none;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 15px;
            }
            
            .hero h2 {
                font-size: 36px;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .checkout-form {
                grid-template-columns: 1fr;
            }
            
            .admin-panel {
                bottom: 10px;
                right: 10px;
                left: 10px;
                max-width: none;
            }
            
            .notification-buttons {
                flex-direction: column;
            }
            
            .product-list, .user-list {
                grid-template-columns: 1fr;
            }
            
            .orders-table, .users-table {
                display: block;
                overflow-x: auto;
            }
            
            .tracking-steps {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }
            
            .tracking-steps::before {
                display: none;
            }
            
            .tracking-step {
                flex-direction: row;
                gap: 10px;
            }
            
            .step-label {
                max-width: none;
            }
        }
        
        @media (max-width: 576px) {
            nav ul li {
                margin-left: 15px;
            }
            
            .hero {
                padding: 60px 0;
            }
            
            .hero h2 {
                font-size: 28px;
            }
            
            .hero p {
                font-size: 16px;
            }
            
            .section-title {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-apple-alt"></i>
                <h1>Fruits Club</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li id="fruits-nav" class="hidden"><a href="#fruits">Fruits</a></li>
                    <li id="cart-nav" class="hidden"><a href="#cart">Cart</a></li>
                    <li id="orders-nav" class="hidden"><a href="#orders">My Orders</a></li>
                    <li id="admin-dashboard-nav" class="hidden"><a href="#admin-dashboard">Admin</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li id="cart-icon" class="cart-icon hidden">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="cart-count">0</span>
                    </li>
                    <li id="user-info" class="user-info hidden">
                        <div class="user-avatar">U</div>
                        <span id="username-display">User</span>
                        <span id="admin-badge" class="admin-badge hidden">Admin</span>
                        <button id="logout-btn" class="btn btn-secondary" style="padding: 5px 10px; font-size: 14px;">Logout</button>
                    </li>
                    <li id="login-nav">
                        <a href="#login" class="btn">Login</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Fresh Fruits Delivered to Your Door</h2>
            <p>Enjoy the finest selection of seasonal fruits delivered fresh from our farms to your home. Currently serving Anatapur area only.</p>
            <a href="#login" class="btn">Login or register to Order</a>
        </div>
    </section>

    <!-- Login Section -->
    <section id="login" class="login-section">
        <div class="container">
            <div class="login-container">
                <h2>Login to Fruits Club</h2>
                <div class="login-tabs">
                    <div class="login-tab active" data-tab="customer">Customer Login</div>
                    <div class="login-tab" data-tab="admin">Admin Login</div>
                </div>
                <form id="loginForm">
                    <div class="form-group">
                        <label for="username">Username</label>
                        <input type="text" id="username" required>
                    </div>
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" required>
                    </div>
                    <button type="submit" class="btn login-btn">Login</button>
                </form>
                <div class="register-link">
                    <p>Don't have an account? <a href="#" id="register-link">Register here</a></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Register Section -->
    <section id="register" class="register-section hidden">
        <div class="container">
            <div class="register-container">
                <h2>Create an Account</h2>
                <form id="registerForm">
                    <div class="form-group">
                        <label for="reg-fullname">Full Name</label>
                        <input type="text" id="reg-fullname" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-email">Email Address</label>
                        <input type="email" id="reg-email" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-phone">Phone Number</label>
                        <input type="tel" id="reg-phone" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-username">Username</label>
                        <input type="text" id="reg-username" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-password">Password</label>
                        <input type="password" id="reg-password" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-confirm-password">Confirm Password</label>
                        <input type="password" id="reg-confirm-password" required>
                    </div>
                    <div class="form-group">
                        <label for="reg-address">Delivery Address</label>
                        <textarea id="reg-address" required></textarea>
                    </div>
                    <div class="form-group">
                        <label for="reg-city">City</label>
                        <input type="text" id="reg-city" value="Anatapur" readonly required>
                    </div>
                    <div class="form-group">
                        <label for="reg-pincode">Pincode</label>
                        <input type="text" id="reg-pincode" required>
                    </div>
                    <button type="submit" class="btn register-btn">Create Account</button>
                </form>
                <div class="login-link">
                    <p>Already have an account? <a href="#" id="login-link">Login here</a></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Orders Section -->
    <section id="orders" class="orders-section hidden">
        <div class="container">
            <h2 class="section-title">My Orders</h2>
            <div class="orders-container" id="orders-container">
                <div class="no-orders">
                    <i class="fas fa-box-open" style="font-size: 48px; margin-bottom: 15px; color: #ccc;"></i>
                    <h3>No orders yet</h3>
                    <p>Your order history will appear here once you place an order.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Admin Dashboard -->
    <section id="admin-dashboard" class="hidden">
        <div class="container">
            <h2 class="section-title">Admin Dashboard</h2>
            <div class="admin-dashboard">
                <h2>Welcome, Admin!</h2>
                <div class="dashboard-stats">
                    <div class="stat-card">
                        <div class="stat-value" id="total-orders">0</div>
                        <div class="stat-label">Total Orders</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="pending-orders">0</div>
                        <div class="stat-label">Pending Orders</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="ready-orders">0</div>
                        <div class="stat-label">Ready Orders</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="completed-orders">0</div>
                        <div class="stat-label">Completed Orders</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">₹<span id="total-revenue">0</span></div>
                        <div class="stat-label">Total Revenue</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="total-users">0</div>
                        <div class="stat-label">Total Users</div>
                    </div>
                </div>
                
                <div class="orders-management">
                    <h3>Orders Management</h3>
                    <div class="table-container">
                        <table class="orders-table">
                            <thead>
                                <tr>
                                    <th>Order ID</th>
                                    <th>Customer</th>
                                    <th>Items</th>
                                    <th>Total</th>
                                    <th>Status</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="orders-table-body">
                                <!-- Orders will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <div class="user-management">
                    <h3>User Management</h3>
                    <div class="table-container">
                        <table class="users-table">
                            <thead>
                                <tr>
                                    <th>Username</th>
                                    <th>Full Name</th>
                                    <th>Email</th>
                                    <th>Phone</th>
                                    <th>Address</th>
                                    <th>Orders</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="users-table-body">
                                <!-- Users will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <div class="product-management">
                    <h3>Product Management</h3>
                    <div class="product-list" id="product-management-list">
                        <!-- Product edit cards will be generated by JavaScript -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Fruits Section (Hidden until login) -->
    <section id="fruits" class="hidden">
        <div class="container">
            <h2 class="section-title">Our Fresh Fruits</h2>
            <div class="area-restriction">
                <h3><i class="fas fa-map-marker-alt"></i> Service Area Notice</h3>
                <p>We currently deliver only within Anatapur city limits. Please ensure your delivery address is in Anatapur.</p>
            </div>
            <div class="fruits-grid">
                <!-- Fruit cards will be generated by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Cart Section (Hidden until login) -->
    <section id="cart" class="hidden" style="background-color: var(--light);">
        <div class="container">
            <h2 class="section-title">Your Cart</h2>
            <div class="cart-container">
                <div class="cart-items">
                    <!-- Cart items will be generated by JavaScript -->
                    <p class="empty-cart-message">Your cart is empty. Add some fruits!</p>
                </div>
                <div class="cart-summary">
                    <div class="cart-total">
                        <span>Total:</span>
                        <span class="total-price">0.00</span>
                    </div>
                    <button class="btn checkout-btn" id="open-checkout" disabled>Proceed to Checkout</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Checkout Modal -->
    <div id="checkout-modal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Complete Your Order</h2>
                <button class="close-modal">&times;</button>
            </div>
            <form id="checkoutForm">
                <div class="checkout-form">
                    <div class="form-group full-width">
                        <h3>Personal Information</h3>
                    </div>
                    <div class="form-group">
                        <label for="full-name">Full Name *</label>
                        <input type="text" id="full-name" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone Number *</label>
                        <input type="tel" id="phone" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email Address *</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group full-width">
                        <h3>Delivery Address</h3>
                    </div>
                    <div class="form-group">
                        <label for="house-no">House/Flat No. *</label>
                        <input type="text" id="house-no" required>
                    </div>
                    <div class="form-group">
                        <label for="street">Street/Area *</label>
                        <input type="text" id="street" required>
                    </div>
                    <div class="form-group">
                        <label for="landmark">Landmark</label>
                        <input type="text" id="landmark">
                    </div>
                    <div class="form-group">
                        <label for="city">City *</label>
                        <input type="text" id="city" value="Anatapur" readonly required>
                    </div>
                    <div class="form-group">
                        <label for="pincode">Pincode *</label>
                        <input type="text" id="pincode" required>
                    </div>
                    <div class="form-group">
                        <label for="state">State *</label>
                        <select id="state" required>
                            <option value="Andhra Pradesh" selected>Andhra Pradesh</option>
                        </select>
                    </div>
                    <div class="form-group full-width location-section">
                        <h3>Current Location</h3>
                        <p>Allow location access for faster delivery</p>
                        <button type="button" id="get-location" class="btn btn-secondary">Get My Location</button>
                        <div id="location-info" class="location-info">
                            <p>Location not yet retrieved</p>
                        </div>
                    </div>
                    <div class="form-group full-width">
                        <h3>Delivery Instructions</h3>
                        <textarea id="instructions" placeholder="Any special delivery instructions?"></textarea>
                    </div>
                    <div class="form-group full-width order-summary">
                        <h3>Order Summary</h3>
                        <div id="checkout-items">
                            <!-- Order items will be populated by JavaScript -->
                        </div>
                        <div class="order-total">
                            <span>Total:</span>
                            <span id="checkout-total">₹0.00</span>
                        </div>
                    </div>
                    <div class="form-group full-width notification-options">
                        <h3>Send Order Confirmation</h3>
                        <p>Choose how to send order details to admin:</p>
                        <div class="notification-buttons">
                            <button type="button" id="send-whatsapp" class="btn btn-whatsapp">
                                <i class="fab fa-whatsapp"></i> Send via WhatsApp
                            </button>
                            <button type="button" id="send-email" class="btn btn-email">
                                <i class="fas fa-envelope"></i> Send via Email
                            </button>
                            <button type="button" id="send-both" class="btn btn-secondary">
                                <i class="fas fa-paper-plane"></i> Send Both
                            </button>
                        </div>
                    </div>
                    <div class="form-group full-width">
                        <button type="submit" class="btn" style="width: 100%; padding: 15px; font-size: 18px;">Place Order</button>
                    </div>
                </div>
            </form>
        </div>
    </div>

    <!-- Admin Panel - Hidden on front page, only visible on admin page -->
    <div class="admin-panel" id="admin-panel">
        <h3><i class="fas fa-user-shield"></i> Admin Orders</h3>
        <div class="admin-orders" id="admin-orders">
            <p>No new orders</p>
        </div>
        <div class="order-actions">
            <button id="refresh-orders" class="btn btn-secondary" style="padding: 5px 10px; font-size: 12px;">Refresh</button>
        </div>
    </div>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get in Touch</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Umanagar, Anatapur, Andhra Pradesh</p>
                    <p><i class="fas fa-phone"></i> +91 7207199308</p>
                    <p><i class="fas fa-envelope"></i> puramvenkatadri@gmail.com</p>
                    <p><i class="fas fa-clock"></i> Mon-Sat: 6:00 AM - 9:00 PM</p>
                    <p><i class="fas fa-map-pin"></i> Currently serving Anatapur area only</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Send us a Message</h3>
                    <form id="messageForm">
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Your Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Fruits Club</h3>
                    <p>Delivering fresh, high-quality fruits directly to your doorstep. Currently serving Anatapur area.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#fruits">Fruits</a></li>
                        <li><a href="#cart">Cart</a></li>
                        <li><a href="#orders">My Orders</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Customer Service</h3>
                    <ul>
                        <li><a href="#">FAQ</a></li>
                        <li><a href="#">Shipping Policy</a></li>
                        <li><a href="#">Returns & Refunds</a></li>
                        <li><a href="#">Terms of Service</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Service Area</h3>
                    <p>We currently deliver only within:</p>
                    <p><strong>Anatapur, Andhra Pradesh</strong></p>
                    <p>More areas coming soon!</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2026 Fruits Club. All rights reserved. | Currently serving Anatapur area only</p>
            </div>
        </div>
    </footer>

    <script>
        // User authentication state
        let isLoggedIn = false;
        let currentUser = null;
        let isAdmin = false;

        // Registered users data - Now using a simulated "server" storage
        let registeredUsers = [];
        let serverDataLoaded = false;

        // Fruit data with prices in Indian Rupees
        let fruits = [
            {
                id: 1,
                name: "Fresh Apples",
                price: 180,
                image: "https://images.unsplash.com/photo-1568702846914-96b305d2aaeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80",
                description: "Crisp and sweet red apples, perfect for snacking. (per kg)",
                inStock: true
            },
            {
                id: 2,
                name: "Juicy Oranges",
                price: 120,
                image: "https://images.unsplash.com/photo-1547514701-42782101795e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80",
                description: "Sweet and tangy oranges, packed with vitamin C. (per kg)",
                inStock: true
            },
            {
                id: 3,
                name: "Ripe Bananas",
                price: 60,
                image: "https://images.unsplash.com/photo-1571771894821-ce9b6c11b08e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1480&q=80",
                description: "Perfectly ripe bananas, great for smoothies or snacks. (per dozen)",
                inStock: true
            },
            {
                id: 4,
                name: "Sweet Strawberries",
                price: 350,
                image: "https://images.unsplash.com/photo-1464454709131-ffd692591ee5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80",
                description: "Fresh, sweet strawberries, perfect for desserts. (per kg)",
                inStock: false
            },
            {
                id: 5,
                name: "Tropical Pineapples",
                price: 80,
                image: "https://images.unsplash.com/photo-1550258987-190a2d41a8ba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80",
                description: "Sweet and tangy pineapples, great for tropical dishes. (per piece)",
                inStock: true
            },
            {
                id: 6,
                name: "Fresh Grapes",
                price: 150,
                image: "https://images.unsplash.com/photo-1537640538966-79f74189e399?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1398&q=80",
                description: "Sweet seedless grapes, perfect for snacking. (per kg)",
                inStock: true
            }
        ];

        // Cart state
        let cart = [];

        // Admin orders state
        let adminOrders = [];

        // User orders state - now stored per user
        let userOrders = {};

        // DOM elements
        const loginSection = document.getElementById('login');
        const registerSection = document.getElementById('register');
        const fruitsSection = document.getElementById('fruits');
        const cartSection = document.getElementById('cart');
        const ordersSection = document.getElementById('orders');
        const adminDashboardSection = document.getElementById('admin-dashboard');
        const fruitsNav = document.getElementById('fruits-nav');
        const cartNav = document.getElementById('cart-nav');
        const ordersNav = document.getElementById('orders-nav');
        const adminDashboardNav = document.getElementById('admin-dashboard-nav');
        const cartIcon = document.getElementById('cart-icon');
        const userInfo = document.getElementById('user-info');
        const loginNav = document.getElementById('login-nav');
        const usernameDisplay = document.getElementById('username-display');
        const adminBadge = document.getElementById('admin-badge');
        const logoutBtn = document.getElementById('logout-btn');
        const loginForm = document.getElementById('loginForm');
        const registerForm = document.getElementById('registerForm');
        const loginTabs = document.querySelectorAll('.login-tab');
        const fruitsGrid = document.querySelector('.fruits-grid');
        const cartItems = document.querySelector('.cart-items');
        const totalPriceElement = document.querySelector('.total-price');
        const cartCount = document.querySelector('.cart-count');
        const checkoutBtn = document.getElementById('open-checkout');
        const emptyCartMessage = document.querySelector('.empty-cart-message');
        const messageForm = document.getElementById('messageForm');
        const productManagementList = document.getElementById('product-management-list');
        const ordersTableBody = document.getElementById('orders-table-body');
        const usersTableBody = document.getElementById('users-table-body');
        const refreshOrdersBtn = document.getElementById('refresh-orders');
        const adminPanel = document.getElementById('admin-panel');
        const ordersContainer = document.getElementById('orders-container');
        const registerLink = document.getElementById('register-link');
        const loginLink = document.getElementById('login-link');
        
        // Admin stats elements
        const totalOrdersElement = document.getElementById('total-orders');
        const pendingOrdersElement = document.getElementById('pending-orders');
        const readyOrdersElement = document.getElementById('ready-orders');
        const completedOrdersElement = document.getElementById('completed-orders');
        const totalRevenueElement = document.getElementById('total-revenue');
        const totalUsersElement = document.getElementById('total-users');
        
        // Checkout modal elements
        const checkoutModal = document.getElementById('checkout-modal');
        const closeModalBtn = document.querySelector('.close-modal');
        const checkoutForm = document.getElementById('checkoutForm');
        const getLocationBtn = document.getElementById('get-location');
        const locationInfo = document.getElementById('location-info');
        const checkoutItems = document.getElementById('checkout-items');
        const checkoutTotal = document.getElementById('checkout-total');
        const sendWhatsappBtn = document.getElementById('send-whatsapp');
        const sendEmailBtn = document.getElementById('send-email');
        const sendBothBtn = document.getElementById('send-both');
        
        // Admin panel elements
        const adminOrdersContainer = document.getElementById('admin-orders');

        // Initialize the page
        document.addEventListener('DOMContentLoaded', async () => {
            // Check if user is already logged in
            checkLoginStatus();
            
            // Load all data from the simulated server
            await loadAllDataFromServer();
            
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    
                    // Don't scroll to protected sections if not logged in
                    if ((targetId === '#fruits' || targetId === '#cart' || targetId === '#orders' || targetId === '#admin-dashboard') && !isLoggedIn) {
                        showNotification('Please login to access this section');
                        return;
                    }
                    
                    // If clicking on My Orders, show only orders section
                    if (targetId === '#orders' && isLoggedIn && !isAdmin) {
                        hideAllSections();
                        ordersSection.classList.remove('hidden');
                        renderUserOrders();
                    }
                    
                    // If clicking on Home, show only home section
                    if (targetId === '#home' && isLoggedIn && !isAdmin) {
                        hideAllSections();
                        fruitsSection.classList.remove('hidden');
                    }
                    
                    document.querySelector(targetId).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
            
            // Login tabs functionality
            loginTabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    loginTabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');
                });
            });
            
            // Modal functionality
            checkoutBtn.addEventListener('click', openCheckoutModal);
            closeModalBtn.addEventListener('click', closeCheckoutModal);
            
            // Close modal when clicking outside
            window.addEventListener('click', (e) => {
                if (e.target === checkoutModal) {
                    closeCheckoutModal();
                }
            });
            
            // Location functionality
            getLocationBtn.addEventListener('click', getCurrentLocation);
            
            // Checkout form submission
            checkoutForm.addEventListener('submit', placeOrder);
            
            // Cart icon click to scroll to cart
            cartIcon.addEventListener('click', () => {
                if (isLoggedIn && !isAdmin) {
                    hideAllSections();
                    cartSection.classList.remove('hidden');
                    document.querySelector('#cart').scrollIntoView({
                        behavior: 'smooth'
                    });
                } else if (isAdmin) {
                    showNotification('Admins cannot place orders');
                } else {
                    showNotification('Please login to view your cart');
                }
            });
            
            // Notification buttons
            sendWhatsappBtn.addEventListener('click', () => sendOrderNotification('whatsapp'));
            sendEmailBtn.addEventListener('click', () => sendOrderNotification('email'));
            sendBothBtn.addEventListener('click', () => sendOrderNotification('both'));
            
            // Refresh orders button
            refreshOrdersBtn.addEventListener('click', updateAdminPanel);
            
            // Register and login links
            registerLink.addEventListener('click', showRegisterForm);
            loginLink.addEventListener('click', showLoginForm);
            
            // Register form submission
            registerForm.addEventListener('submit', registerUser);
            
            // Load any existing admin orders from localStorage as backup
            loadLocalBackupData();
        });

        // =============================================
        // SIMULATED SERVER/DATABASE FUNCTIONS
        // =============================================

        // Load all data from simulated server
        async function loadAllDataFromServer() {
            try {
                // In a real app, this would be an API call
                // For simulation, we'll use localStorage with a special key that acts as our "shared database"
                const serverKey = 'fruitsClubServerData';
                const serverData = localStorage.getItem(serverKey);
                
                if (serverData) {
                    const parsedData = JSON.parse(serverData);
                    registeredUsers = parsedData.users || [];
                    adminOrders = parsedData.orders || [];
                    userOrders = parsedData.userOrders || {};
                    fruits = parsedData.fruits || fruits; // Use default fruits if none in server
                    
                    console.log('Data loaded from shared server storage');
                    serverDataLoaded = true;
                } else {
                    // Initialize with some sample data if no server data exists
                    await initializeServerData();
                }
            } catch (error) {
                console.error('Error loading server data:', error);
                // Fall back to local storage
                loadLocalBackupData();
            }
        }

        // Initialize server data with sample users
        async function initializeServerData() {
            // Create some sample users
            registeredUsers = [
                {
                    fullName: "John Doe",
                    email: "john@example.com",
                    phone: "9876543210",
                    username: "john",
                    password: "password123",
                    address: "123 Main Street, Anatapur",
                    city: "Anatapur",
                    pincode: "515001",
                    role: "customer",
                    registrationDate: new Date().toISOString()
                },
                {
                    fullName: "Jane Smith",
                    email: "jane@example.com",
                    phone: "9876543211",
                    username: "jane",
                    password: "password123",
                    address: "456 Park Avenue, Anatapur",
                    city: "Anatapur",
                    pincode: "515002",
                    role: "customer",
                    registrationDate: new Date().toISOString()
                }
            ];

            // Create admin user
            const adminUser = {
                fullName: "Admin User",
                email: "admin@fruitsclub.com",
                phone: "7207199308",
                username: "admin",
                password: "admin123",
                address: "Umanagar, Anatapur",
                city: "Anatapur",
                pincode: "515001",
                role: "admin",
                registrationDate: new Date().toISOString()
            };

            registeredUsers.push(adminUser);

            // Initialize empty data structures
            adminOrders = [];
            userOrders = {};

            // Save to server
            await saveAllDataToServer();
            console.log('Server data initialized with sample users');
        }

        // Save all data to simulated server
        async function saveAllDataToServer() {
            try {
                const serverData = {
                    users: registeredUsers,
                    orders: adminOrders,
                    userOrders: userOrders,
                    fruits: fruits,
                    lastUpdated: new Date().toISOString()
                };

                const serverKey = 'fruitsClubServerData';
                localStorage.setItem(serverKey, JSON.stringify(serverData));
                
                // Also save as backup in device storage
                saveLocalBackupData();
                
                console.log('Data saved to shared server storage');
                return true;
            } catch (error) {
                console.error('Error saving to server:', error);
                return false;
            }
        }

        // Save backup data to device localStorage
        function saveLocalBackupData() {
            try {
                // Save registered users
                localStorage.setItem('fruitsClubRegisteredUsers', JSON.stringify(registeredUsers));
                
                // Save admin orders
                localStorage.setItem('fruitsClubAdminOrders', JSON.stringify(adminOrders));
                
                // Save user orders
                localStorage.setItem('fruitsClubUserOrders', JSON.stringify(userOrders));
                
                // Save fruits
                localStorage.setItem('fruitsClubFruits', JSON.stringify(fruits));
            } catch (error) {
                console.error('Error saving local backup:', error);
            }
        }

        // Load backup data from device localStorage
        function loadLocalBackupData() {
            try {
                // Load registered users
                const savedUsers = localStorage.getItem('fruitsClubRegisteredUsers');
                if (savedUsers) {
                    registeredUsers = JSON.parse(savedUsers);
                }
                
                // Load admin orders
                const savedOrders = localStorage.getItem('fruitsClubAdminOrders');
                if (savedOrders) {
                    adminOrders = JSON.parse(savedOrders);
                }
                
                // Load user orders
                const savedUserOrders = localStorage.getItem('fruitsClubUserOrders');
                if (savedUserOrders) {
                    userOrders = JSON.parse(savedUserOrders);
                }
                
                // Load fruits
                const savedFruits = localStorage.getItem('fruitsClubFruits');
                if (savedFruits) {
                    fruits = JSON.parse(savedFruits);
                }
                
                console.log('Data loaded from local backup storage');
            } catch (error) {
                console.error('Error loading local backup:', error);
            }
        }

        // =============================================
        // APPLICATION FUNCTIONS (Updated to use server)
        // =============================================

        // Show register form
        function showRegisterForm(e) {
            e.preventDefault();
            loginSection.classList.add('hidden');
            registerSection.classList.remove('hidden');
            
            // Scroll to register section
            document.querySelector('#register').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Show login form
        function showLoginForm(e) {
            e.preventDefault();
            registerSection.classList.add('hidden');
            loginSection.classList.remove('hidden');
            
            // Scroll to login section
            document.querySelector('#login').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Register new user
        async function registerUser(e) {
            e.preventDefault();
            
            const fullName = document.getElementById('reg-fullname').value;
            const email = document.getElementById('reg-email').value;
            const phone = document.getElementById('reg-phone').value;
            const username = document.getElementById('reg-username').value;
            const password = document.getElementById('reg-password').value;
            const confirmPassword = document.getElementById('reg-confirm-password').value;
            const address = document.getElementById('reg-address').value;
            const city = document.getElementById('reg-city').value;
            const pincode = document.getElementById('reg-pincode').value;
            
            // Validate form
            if (!fullName || !email || !phone || !username || !password || !confirmPassword || !address || !pincode) {
                showNotification('Please fill in all required fields');
                return;
            }
            
            if (password !== confirmPassword) {
                showNotification('Passwords do not match');
                return;
            }
            
            if (city.toLowerCase() !== 'anatapur') {
                showNotification('Sorry, we currently deliver only in Anatapur area');
                return;
            }
            
            // Check if username already exists (in server data)
            if (registeredUsers.find(user => user.username === username)) {
                showNotification('Username already exists. Please choose a different username.');
                return;
            }
            
            // Check if email already exists
            if (registeredUsers.find(user => user.email === email)) {
                showNotification('Email already registered. Please use a different email.');
                return;
            }
            
            // Create new user
            const newUser = {
                fullName: fullName,
                email: email,
                phone: phone,
                username: username,
                password: password,
                address: address,
                city: city,
                pincode: pincode,
                role: 'customer',
                registrationDate: new Date().toISOString()
            };
            
            // Add to registered users
            registeredUsers.push(newUser);
            
            // Initialize empty orders for new user
            if (!userOrders[username]) {
                userOrders[username] = [];
            }
            
            // Save to server
            const saved = await saveAllDataToServer();
            
            if (saved) {
                // Show success message
                showNotification('Registration successful! You can now login with your credentials.');
                
                // Clear form
                registerForm.reset();
                
                // Redirect to login
                showLoginForm(e);
            } else {
                showNotification('Error saving registration. Please try again.');
            }
        }

        // Hide all sections except login
        function hideAllSections() {
            fruitsSection.classList.add('hidden');
            cartSection.classList.add('hidden');
            ordersSection.classList.add('hidden');
            adminDashboardSection.classList.add('hidden');
            registerSection.classList.add('hidden');
        }

        // Check login status
        function checkLoginStatus() {
            const savedUser = localStorage.getItem('fruitsClubUser');
            if (savedUser) {
                const user = JSON.parse(savedUser);
                if (user.role === 'admin') {
                    loginAdmin(user);
                } else {
                    loginUser(user);
                }
            }
        }

        // Login form submission
        loginForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const activeTab = document.querySelector('.login-tab.active').dataset.tab;
            
            // Simple validation
            if (username && password) {
                if (activeTab === 'admin') {
                    // Admin login - check in server data
                    const adminUser = registeredUsers.find(u => 
                        u.username === username && 
                        u.password === password && 
                        u.role === 'admin'
                    );
                    
                    if (adminUser) {
                        loginAdmin(adminUser);
                        localStorage.setItem('fruitsClubUser', JSON.stringify(adminUser));
                    } else if (username === 'admin' && password === 'admin123') {
                        // Fallback for initial admin
                        const fallbackAdmin = {
                            username: 'admin',
                            firstName: 'Admin',
                            role: 'admin'
                        };
                        loginAdmin(fallbackAdmin);
                        localStorage.setItem('fruitsClubUser', JSON.stringify(fallbackAdmin));
                    } else {
                        showNotification('Invalid admin credentials');
                    }
                } else {
                    // Customer login - check in server data
                    const user = registeredUsers.find(u => 
                        u.username === username && 
                        u.password === password && 
                        u.role === 'customer'
                    );
                    
                    if (user) {
                        loginUser(user);
                        localStorage.setItem('fruitsClubUser', JSON.stringify(user));
                    } else {
                        showNotification('Invalid username or password');
                    }
                }
            } else {
                showNotification('Please enter both username and password');
            }
        });

        // Login user (customer)
        function loginUser(user) {
            isLoggedIn = true;
            isAdmin = false;
            currentUser = user;
            
            // Update UI
            loginSection.classList.add('hidden');
            registerSection.classList.add('hidden');
            fruitsSection.classList.remove('hidden');
            fruitsNav.classList.remove('hidden');
            cartNav.classList.remove('hidden');
            ordersNav.classList.remove('hidden');
            adminDashboardNav.classList.add('hidden');
            cartIcon.classList.remove('hidden');
            userInfo.classList.remove('hidden');
            loginNav.classList.add('hidden');
            adminBadge.classList.add('hidden');
            adminPanel.classList.remove('visible'); // Hide admin panel for customers
            
            usernameDisplay.textContent = user.fullName;
            document.querySelector('.user-avatar').textContent = user.fullName.charAt(0).toUpperCase();
            
            // Render fruits and update cart
            renderFruits();
            updateCart();
            
            showNotification(`Welcome back, ${user.fullName}! We deliver only in Anatapur area.`);
            
            // Scroll to fruits section
            document.querySelector('#fruits').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Login admin
        function loginAdmin(user) {
            isLoggedIn = true;
            isAdmin = true;
            currentUser = user;
            
            // Update UI
            loginSection.classList.add('hidden');
            registerSection.classList.add('hidden');
            adminDashboardSection.classList.remove('hidden');
            fruitsNav.classList.add('hidden');
            cartNav.classList.add('hidden');
            ordersNav.classList.add('hidden');
            adminDashboardNav.classList.remove('hidden');
            cartIcon.classList.add('hidden');
            userInfo.classList.remove('hidden');
            loginNav.classList.add('hidden');
            adminBadge.classList.remove('hidden');
            adminPanel.classList.add('visible'); // Show admin panel only for admin
            
            usernameDisplay.textContent = user.fullName || user.firstName;
            document.querySelector('.user-avatar').textContent = user.fullName ? user.fullName.charAt(0).toUpperCase() : 'A';
            
            // Render admin dashboard
            renderAdminDashboard();
            updateAdminPanel();
            
            showNotification(`Welcome, ${user.fullName || user.firstName}!`);
            
            // Scroll to admin dashboard
            document.querySelector('#admin-dashboard').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Logout user
        logoutBtn.addEventListener('click', () => {
            isLoggedIn = false;
            isAdmin = false;
            currentUser = null;
            
            // Update UI
            loginSection.classList.remove('hidden');
            hideAllSections();
            fruitsNav.classList.add('hidden');
            cartNav.classList.add('hidden');
            ordersNav.classList.add('hidden');
            adminDashboardNav.classList.add('hidden');
            cartIcon.classList.add('hidden');
            userInfo.classList.add('hidden');
            loginNav.classList.remove('hidden');
            adminBadge.classList.add('hidden');
            adminPanel.classList.remove('visible'); // Hide admin panel on logout
            
            // Clear cart
            cart = [];
            updateCart();
            
            // Clear login form
            loginForm.reset();
            
            // Remove user from localStorage
            localStorage.removeItem('fruitsClubUser');
            
            showNotification('You have been logged out');
            
            // Scroll to login section
            document.querySelector('#login').scrollIntoView({
                behavior: 'smooth'
            });
        });

        // Render fruits to the page
        function renderFruits() {
            fruitsGrid.innerHTML = '';
            
            fruits.forEach(fruit => {
                const fruitCard = document.createElement('div');
                fruitCard.className = 'fruit-card';
                
                fruitCard.innerHTML = `
                    <div class="fruit-img" style="background-image: url('${fruit.image}')"></div>
                    <div class="stock-badge ${fruit.inStock ? 'in-stock' : 'out-of-stock'}">
                        ${fruit.inStock ? 'In Stock' : 'Out of Stock'}
                    </div>
                    <div class="fruit-info">
                        <h3>${fruit.name}</h3>
                        <p class="fruit-price">${fruit.price.toFixed(2)}</p>
                        <p>${fruit.description}</p>
                        <div class="quantity-controls">
                            <button class="quantity-btn minus" data-id="${fruit.id}" ${!fruit.inStock ? 'disabled' : ''}>-</button>
                            <span class="quantity" data-id="${fruit.id}">0</span>
                            <button class="quantity-btn plus" data-id="${fruit.id}" ${!fruit.inStock ? 'disabled' : ''}>+</button>
                        </div>
                        <button class="btn add-to-cart" data-id="${fruit.id}" ${!fruit.inStock ? 'disabled' : ''}>
                            ${fruit.inStock ? 'Add to Cart' : 'Out of Stock'}
                        </button>
                    </div>
                `;
                
                fruitsGrid.appendChild(fruitCard);
            });
            
            // Add event listeners to buttons
            document.querySelectorAll('.add-to-cart').forEach(button => {
                button.addEventListener('click', addToCart);
            });
            
            document.querySelectorAll('.quantity-btn.plus').forEach(button => {
                button.addEventListener('click', increaseQuantity);
            });
            
            document.querySelectorAll('.quantity-btn.minus').forEach(button => {
                button.addEventListener('click', decreaseQuantity);
            });
        }

        // Render user orders - NOW SHOWS ONLY CURRENT USER'S ORDERS
        function renderUserOrders() {
            ordersContainer.innerHTML = '';
            
            const currentUserOrders = getCurrentUserOrders();
            
            if (currentUserOrders.length === 0) {
                ordersContainer.innerHTML = `
                    <div class="no-orders">
                        <i class="fas fa-box-open" style="font-size: 48px; margin-bottom: 15px; color: #ccc;"></i>
                        <h3>No orders yet</h3>
                        <p>Your order history will appear here once you place an order.</p>
                    </div>
                `;
                return;
            }
            
            // Sort orders by date (newest first)
            const sortedOrders = [...currentUserOrders].reverse();
            
            sortedOrders.forEach(order => {
                const orderCard = document.createElement('div');
                orderCard.className = 'order-card';
                
                // Format date
                const orderDate = new Date(order.timestamp).toLocaleDateString('en-IN', {
                    day: '2-digit',
                    month: 'short',
                    year: 'numeric'
                });
                
                // Get status class
                let statusClass = '';
                if (order.status === 'pending') statusClass = 'status-pending';
                if (order.status === 'ready') statusClass = 'status-ready';
                if (order.status === 'completed') statusClass = 'status-completed';
                
                orderCard.innerHTML = `
                    <div class="order-header">
                        <div>
                            <div class="order-id">${order.id}</div>
                            <div class="order-date">Placed on ${orderDate}</div>
                        </div>
                        <div class="order-status ${statusClass}">${order.status}</div>
                    </div>
                    <div class="order-details">
                        <div class="order-items">
                            ${order.items.map(item => `
                                <div class="order-item">
                                    <span>${item.name} x ${item.quantity}</span>
                                    <span>₹${(item.price * item.quantity).toFixed(2)}</span>
                                </div>
                            `).join('')}
                        </div>
                        <div class="order-total">
                            <span>Total Amount:</span>
                            <span>₹${order.total.toFixed(2)}</span>
                        </div>
                    </div>
                    <div class="tracking-container">
                        <div class="tracking-title">Order Tracking</div>
                        <div class="tracking-steps">
                            <div class="tracking-step ${order.status !== 'pending' ? 'step-completed' : 'step-active'}">
                                <div class="step-icon"><i class="fas fa-shopping-cart"></i></div>
                                <div class="step-label">Order Placed</div>
                            </div>
                            <div class="tracking-step ${order.status === 'ready' || order.status === 'completed' ? 'step-completed' : (order.status === 'pending' ? '' : 'step-active')}">
                                <div class="step-icon"><i class="fas fa-utensils"></i></div>
                                <div class="step-label">Preparing</div>
                            </div>
                            <div class="tracking-step ${order.status === 'completed' ? 'step-completed' : (order.status === 'ready' ? 'step-active' : '')}">
                                <div class="step-icon"><i class="fas fa-shipping-fast"></i></div>
                                <div class="step-label">On the Way</div>
                            </div>
                            <div class="tracking-step ${order.status === 'completed' ? 'step-active' : ''}">
                                <div class="step-icon"><i class="fas fa-home"></i></div>
                                <div class="step-label">Delivered</div>
                            </div>
                        </div>
                        <div class="tracking-info">
                            <p><strong>Delivery Address:</strong> ${order.delivery.address}</p>
                            ${order.delivery.instructions ? `<p><strong>Instructions:</strong> ${order.delivery.instructions}</p>` : ''}
                            <p><strong>Estimated Delivery:</strong> ${getEstimatedDelivery(order.timestamp, order.status)}</p>
                        </div>
                    </div>
                `;
                
                ordersContainer.appendChild(orderCard);
            });
        }

        // Get estimated delivery time
        function getEstimatedDelivery(timestamp, status) {
            const orderDate = new Date(timestamp);
            
            if (status === 'completed') {
                // For completed orders, show actual delivery time (estimated)
                const deliveryDate = new Date(orderDate.getTime() + 60 * 60 * 1000); // 1 hour after order
                return deliveryDate.toLocaleTimeString('en-IN', { hour: '2-digit', minute: '2-digit' }) + 
                       ', ' + deliveryDate.toLocaleDateString('en-IN', { day: '2-digit', month: 'short' });
            } else if (status === 'ready') {
                // For ready orders, show soon
                return 'Within 30 minutes';
            } else {
                // For pending orders, show estimated time
                const estimatedDate = new Date(orderDate.getTime() + 45 * 60 * 1000); // 45 minutes after order
                return estimatedDate.toLocaleTimeString('en-IN', { hour: '2-digit', minute: '2-digit' }) + 
                       ', ' + estimatedDate.toLocaleDateString('en-IN', { day: '2-digit', month: 'short' });
            }
        }

        // Render admin dashboard
        function renderAdminDashboard() {
            // Update stats
            updateAdminStats();
            
            // Render orders table
            renderOrdersTable();
            
            // Render users table
            renderUsersTable();
            
            // Render product management
            productManagementList.innerHTML = '';
            
            fruits.forEach(fruit => {
                const productCard = document.createElement('div');
                productCard.className = 'product-edit-card';
                
                productCard.innerHTML = `
                    <h4>${fruit.name}</h4>
                    <div class="edit-form">
                        <label>Price (₹)</label>
                        <input type="number" id="price-${fruit.id}" value="${fruit.price}" min="1">
                        <label>Stock Status</label>
                        <select id="stock-${fruit.id}">
                            <option value="true" ${fruit.inStock ? 'selected' : ''}>In Stock</option>
                            <option value="false" ${!fruit.inStock ? 'selected' : ''}>Out of Stock</option>
                        </select>
                        <div class="edit-actions">
                            <button class="btn update-product" data-id="${fruit.id}">Update</button>
                            <button class="btn btn-secondary delete-product" data-id="${fruit.id}">Delete</button>
                        </div>
                    </div>
                `;
                
                productManagementList.appendChild(productCard);
            });
            
            // Add event listeners
            document.querySelectorAll('.update-product').forEach(button => {
                button.addEventListener('click', updateProduct);
            });
            
            document.querySelectorAll('.delete-product').forEach(button => {
                button.addEventListener('click', deleteProduct);
            });
        }

        // Render orders table
        function renderOrdersTable() {
            ordersTableBody.innerHTML = '';
            
            if (adminOrders.length === 0) {
                ordersTableBody.innerHTML = `
                    <tr>
                        <td colspan="6" style="text-align: center;">No orders found</td>
                    </tr>
                `;
                return;
            }
            
            // Show all orders in reverse order (newest first)
            const sortedOrders = [...adminOrders].reverse();
            
            sortedOrders.forEach(order => {
                const orderRow = document.createElement('tr');
                
                // Get status badge class
                let statusClass = '';
                if (order.status === 'pending') statusClass = 'status-pending';
                if (order.status === 'ready') statusClass = 'status-ready';
                if (order.status === 'completed') statusClass = 'status-completed';
                
                orderRow.innerHTML = `
                    <td>${order.id}</td>
                    <td>${order.customer.fullName}</td>
                    <td>${order.items.length} items</td>
                    <td>₹${order.total.toFixed(2)}</td>
                    <td><span class="status-badge ${statusClass}">${order.status}</span></td>
                    <td>
                        <button class="btn order-action-btn mark-ready" data-id="${order.id}" ${order.status !== 'pending' ? 'disabled' : ''}>Ready</button>
                        <button class="btn order-action-btn mark-completed" data-id="${order.id}" ${order.status !== 'ready' ? 'disabled' : ''}>Delivered</button>
                        <button class="btn btn-secondary order-action-btn view-details" data-id="${order.id}">Details</button>
                    </td>
                `;
                
                ordersTableBody.appendChild(orderRow);
            });
            
            // Add event listeners to order action buttons
            document.querySelectorAll('.mark-ready').forEach(button => {
                button.addEventListener('click', markOrderReady);
            });
            
            document.querySelectorAll('.mark-completed').forEach(button => {
                button.addEventListener('click', markOrderCompleted);
            });
            
            document.querySelectorAll('.view-details').forEach(button => {
                button.addEventListener('click', viewOrderDetails);
            });
        }

        // Render users table in admin dashboard
        function renderUsersTable() {
            usersTableBody.innerHTML = '';
            
            if (registeredUsers.length === 0) {
                usersTableBody.innerHTML = `
                    <tr>
                        <td colspan="7" style="text-align: center;">No users found</td>
                    </tr>
                `;
                return;
            }
            
            registeredUsers.forEach(user => {
                const userRow = document.createElement('tr');
                
                // Count orders for this user
                const userOrderCount = userOrders[user.username] ? userOrders[user.username].length : 0;
                
                // Format registration date
                const regDate = user.registrationDate ? 
                    new Date(user.registrationDate).toLocaleDateString('en-IN', {
                        day: '2-digit',
                        month: 'short',
                        year: 'numeric'
                    }) : 'N/A';
                
                userRow.innerHTML = `
                    <td>${user.username}</td>
                    <td>${user.fullName}</td>
                    <td>${user.email}</td>
                    <td>${user.phone}</td>
                    <td>${user.address.substring(0, 30)}${user.address.length > 30 ? '...' : ''}</td>
                    <td>${userOrderCount} orders</td>
                    <td>
                        <button class="btn btn-secondary view-user-orders" data-username="${user.username}">View Orders</button>
                        <button class="btn btn-admin delete-user" data-username="${user.username}">Delete</button>
                    </td>
                `;
                
                usersTableBody.appendChild(userRow);
            });
            
            // Add event listeners to user action buttons
            document.querySelectorAll('.view-user-orders').forEach(button => {
                button.addEventListener('click', viewUserOrders);
            });
            
            document.querySelectorAll('.delete-user').forEach(button => {
                button.addEventListener('click', deleteUser);
            });
        }

        // View user orders in admin
        function viewUserOrders(e) {
            const username = e.target.getAttribute('data-username');
            const user = registeredUsers.find(u => u.username === username);
            
            if (user) {
                const userOrderList = userOrders[username] || [];
                let message = `Orders for ${user.fullName} (${user.username})\n\n`;
                
                if (userOrderList.length === 0) {
                    message += 'No orders placed yet.';
                } else {
                    userOrderList.forEach((order, index) => {
                        message += `Order ${index + 1}:\n`;
                        message += `ID: ${order.id}\n`;
                        message += `Date: ${new Date(order.timestamp).toLocaleDateString()}\n`;
                        message += `Status: ${order.status}\n`;
                        message += `Total: ₹${order.total.toFixed(2)}\n`;
                        message += `Items: ${order.items.map(item => `${item.name} x ${item.quantity}`).join(', ')}\n`;
                        message += `---\n`;
                    });
                }
                
                alert(message);
            }
        }

        // Delete user
        async function deleteUser(e) {
            const username = e.target.getAttribute('data-username');
            const user = registeredUsers.find(u => u.username === username);
            
            if (user && confirm(`Are you sure you want to delete user "${user.fullName}" (${user.username})? This will also delete all their orders.`)) {
                // Remove user from registered users
                registeredUsers = registeredUsers.filter(u => u.username !== username);
                
                // Remove user orders
                if (userOrders[username]) {
                    delete userOrders[username];
                }
                
                // Save to server
                await saveAllDataToServer();
                
                // Update admin dashboard
                renderAdminDashboard();
                updateAdminStats();
                
                showNotification(`User "${user.fullName}" deleted successfully`);
            }
        }

        // Update admin stats
        function updateAdminStats() {
            const totalOrders = adminOrders.length;
            const pendingOrders = adminOrders.filter(order => order.status === 'pending').length;
            const readyOrders = adminOrders.filter(order => order.status === 'ready').length;
            const completedOrders = adminOrders.filter(order => order.status === 'completed').length;
            const totalRevenue = adminOrders.reduce((sum, order) => sum + order.total, 0);
            const totalUsers = registeredUsers.filter(u => u.role === 'customer').length;
            
            totalOrdersElement.textContent = totalOrders;
            pendingOrdersElement.textContent = pendingOrders;
            readyOrdersElement.textContent = readyOrders;
            completedOrdersElement.textContent = completedOrders;
            totalRevenueElement.textContent = totalRevenue.toFixed(2);
            totalUsersElement.textContent = totalUsers;
        }

        // Update product
        async function updateProduct(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const fruitIndex = fruits.findIndex(f => f.id === fruitId);
            
            if (fruitIndex !== -1) {
                const newPrice = parseFloat(document.getElementById(`price-${fruitId}`).value);
                const newStockStatus = document.getElementById(`stock-${fruitId}`).value === 'true';
                
                fruits[fruitIndex].price = newPrice;
                fruits[fruitIndex].inStock = newStockStatus;
                
                // Save to server
                await saveAllDataToServer();
                
                // If user is customer, update the fruits display
                if (!isAdmin) {
                    renderFruits();
                }
                
                showNotification(`Product "${fruits[fruitIndex].name}" updated successfully`);
            }
        }

        // Delete product
        async function deleteProduct(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const fruitIndex = fruits.findIndex(f => f.id === fruitId);
            
            if (fruitIndex !== -1 && confirm(`Are you sure you want to delete "${fruits[fruitIndex].name}"?`)) {
                const deletedFruit = fruits.splice(fruitIndex, 1)[0];
                
                // Save to server
                await saveAllDataToServer();
                
                renderAdminDashboard();
                
                // If user is customer, update the fruits display
                if (!isAdmin) {
                    renderFruits();
                }
                
                showNotification(`Product "${deletedFruit.name}" deleted successfully`);
            }
        }

        // Get current user's orders
        function getCurrentUserOrders() {
            if (!currentUser || !currentUser.username) return [];
            return userOrders[currentUser.username] || [];
        }

        // Save current user's orders
        async function saveCurrentUserOrders(orders) {
            if (!currentUser || !currentUser.username) return;
            userOrders[currentUser.username] = orders;
            await saveAllDataToServer();
        }

        // Add item to cart
        function addToCart(e) {
            if (!isLoggedIn) {
                showNotification('Please login to add items to cart');
                return;
            }
            
            if (isAdmin) {
                showNotification('Admins cannot place orders');
                return;
            }
            
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const fruit = fruits.find(f => f.id === fruitId);
            const quantityElement = document.querySelector(`.quantity[data-id="${fruitId}"]`);
            const quantity = parseInt(quantityElement.textContent);
            
            if (quantity === 0) {
                alert('Please select at least one item');
                return;
            }
            
            if (!fruit.inStock) {
                alert('This item is out of stock');
                return;
            }
            
            const existingItem = cart.find(item => item.id === fruitId);
            
            if (existingItem) {
                existingItem.quantity += quantity;
            } else {
                cart.push({
                    id: fruitId,
                    name: fruit.name,
                    price: fruit.price,
                    image: fruit.image,
                    quantity: quantity
                });
            }
            
            // Reset quantity display
            quantityElement.textContent = '0';
            
            updateCart();
            showNotification(`${quantity} ${fruit.name} added to cart!`);
        }

        // Increase quantity
        function increaseQuantity(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const quantityElement = document.querySelector(`.quantity[data-id="${fruitId}"]`);
            let quantity = parseInt(quantityElement.textContent);
            quantity++;
            quantityElement.textContent = quantity;
        }

        // Decrease quantity
        function decreaseQuantity(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const quantityElement = document.querySelector(`.quantity[data-id="${fruitId}"]`);
            let quantity = parseInt(quantityElement.textContent);
            
            if (quantity > 0) {
                quantity--;
                quantityElement.textContent = quantity;
            }
        }

        // Update cart display
        function updateCart() {
            // Update cart count
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            // Update cart items
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                emptyCartMessage.style.display = 'block';
                checkoutBtn.disabled = true;
            } else {
                emptyCartMessage.style.display = 'none';
                checkoutBtn.disabled = false;
                
                cart.forEach(item => {
                    const cartItem = document.createElement('div');
                    cartItem.className = 'cart-item';
                    
                    cartItem.innerHTML = `
                        <div class="cart-item-info">
                            <div class="cart-item-img" style="background-image: url('${item.image}')"></div>
                            <div class="cart-item-details">
                                <h4>${item.name}</h4>
                                <p class="cart-item-price">${item.price.toFixed(2)} each</p>
                            </div>
                        </div>
                        <div class="cart-item-controls">
                            <div class="quantity-controls">
                                <button class="quantity-btn minus-cart" data-id="${item.id}">-</button>
                                <span class="quantity">${item.quantity}</span>
                                <button class="quantity-btn plus-cart" data-id="${item.id}">+</button>
                            </div>
                            <p class="cart-item-total">₹${(item.price * item.quantity).toFixed(2)}</p>
                            <button class="btn remove-from-cart" data-id="${item.id}">Remove</button>
                        </div>
                    `;
                    
                    cartItems.appendChild(cartItem);
                });
                
                // Add event listeners to cart buttons
                document.querySelectorAll('.plus-cart').forEach(button => {
                    button.addEventListener('click', increaseCartQuantity);
                });
                
                document.querySelectorAll('.minus-cart').forEach(button => {
                    button.addEventListener('click', decreaseCartQuantity);
                });
                
                document.querySelectorAll('.remove-from-cart').forEach(button => {
                    button.addEventListener('click', removeFromCart);
                });
            }
            
            // Update total price
            const totalPrice = cart.reduce((total, item) => total + (item.price * item.quantity), 0);
            totalPriceElement.textContent = `${totalPrice.toFixed(2)}`;
        }

        // Increase quantity in cart
        function increaseCartQuantity(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const item = cart.find(item => item.id === fruitId);
            item.quantity++;
            updateCart();
        }

        // Decrease quantity in cart
        function decreaseCartQuantity(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            const item = cart.find(item => item.id === fruitId);
            
            if (item.quantity > 1) {
                item.quantity--;
            } else {
                // Remove item if quantity becomes 0
                cart = cart.filter(item => item.id !== fruitId);
            }
            
            updateCart();
        }

        // Remove item from cart
        function removeFromCart(e) {
            const fruitId = parseInt(e.target.getAttribute('data-id'));
            cart = cart.filter(item => item.id !== fruitId);
            updateCart();
            showNotification('Item removed from cart');
        }

        // Open checkout modal
        function openCheckoutModal() {
            if (cart.length === 0) {
                showNotification('Your cart is empty!');
                return;
            }
            
            // Populate checkout items
            checkoutItems.innerHTML = '';
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                const orderItem = document.createElement('div');
                orderItem.className = 'order-item';
                orderItem.innerHTML = `
                    <span>${item.name} x ${item.quantity}</span>
                    <span>₹${itemTotal.toFixed(2)}</span>
                `;
                checkoutItems.appendChild(orderItem);
            });
            
            checkoutTotal.textContent = `₹${total.toFixed(2)}`;
            
            // Show modal
            checkoutModal.style.display = 'flex';
        }

        // Close checkout modal
        function closeCheckoutModal() {
            checkoutModal.style.display = 'none';
        }

        // Get current location
        function getCurrentLocation() {
            if (!navigator.geolocation) {
                locationInfo.innerHTML = '<p class="location-error">Geolocation is not supported by this browser.</p>';
                return;
            }
            
            locationInfo.innerHTML = '<p class="location-loading">Getting your location...</p>';
            
            navigator.geolocation.getCurrentPosition(
                // Success callback
                (position) => {
                    const latitude = position.coords.latitude;
                    const longitude = position.coords.longitude;
                    
                    // Check if location is in Anatapur area (approximate coordinates)
                    const isInAnatapur = checkAnatapurArea(latitude, longitude);
                    
                    if (isInAnatapur) {
                        locationInfo.innerHTML = `
                            <p><strong>Location retrieved successfully!</strong></p>
                            <p>Coordinates: ${latitude.toFixed(6)}, ${longitude.toFixed(6)}</p>
                            <p><i class="fas fa-check-circle" style="color: green;"></i> You are in our service area (Anatapur)</p>
                        `;
                    } else {
                        locationInfo.innerHTML = `
                            <p><strong>Location retrieved successfully!</strong></p>
                            <p>Coordinates: ${latitude.toFixed(6)}, ${longitude.toFixed(6)}</p>
                            <p><i class="fas fa-exclamation-triangle" style="color: orange;"></i> You are outside our service area. We deliver only in Anatapur.</p>
                        `;
                    }
                },
                // Error callback
                (error) => {
                    let errorMessage = 'Unable to retrieve your location. ';
                    
                    switch(error.code) {
                        case error.PERMISSION_DENIED:
                            errorMessage += 'Please allow location access in your browser settings.';
                            break;
                        case error.POSITION_UNAVAILABLE:
                            errorMessage += 'Location information is unavailable.';
                            break;
                        case error.TIMEOUT:
                            errorMessage += 'The request to get your location timed out.';
                            break;
                        default:
                            errorMessage += 'An unknown error occurred.';
                    }
                    
                    locationInfo.innerHTML = `<p class="location-error">${errorMessage}</p>`;
                }
            );
        }

        // Check if location is in Anatapur area (simplified check)
        function checkAnatapurArea(lat, lng) {
            // Approximate coordinates for Anatapur area
            const anatapurLatMin = 14.60;
            const anatapurLatMax = 14.80;
            const anatapurLngMin = 77.55;
            const anatapurLngMax = 77.75;
            
            return (lat >= anatapurLatMin && lat <= anatapurLatMax && 
                    lng >= anatapurLngMin && lng <= anatapurLngMax);
        }

        // Update admin panel with orders
        function updateAdminPanel() {
            adminOrdersContainer.innerHTML = '';
            
            if (adminOrders.length === 0) {
                adminOrdersContainer.innerHTML = '<p>No new orders</p>';
                return;
            }
            
            // Show only the 5 most recent orders
            const recentOrders = adminOrders.slice(-5).reverse();
            
            recentOrders.forEach(order => {
                const orderElement = document.createElement('div');
                orderElement.className = `admin-order ${order.status === 'pending' ? 'new' : ''} ${order.status === 'ready' ? 'ready' : ''} ${order.status === 'completed' ? 'completed' : ''}`;
                
                orderElement.innerHTML = `
                    <div class="order-id">${order.id}</div>
                    <div>${order.customer.fullName} - ₹${order.total.toFixed(2)}</div>
                    <div>${order.items.length} items - ${order.status}</div>
                    <div class="order-actions">
                        <button class="order-action-btn mark-ready" data-id="${order.id}" ${order.status !== 'pending' ? 'disabled' : ''}>Ready</button>
                        <button class="order-action-btn mark-completed" data-id="${order.id}" ${order.status !== 'ready' ? 'disabled' : ''}>Delivered</button>
                        <button class="order-action-btn view-details" data-id="${order.id}">Details</button>
                    </div>
                `;
                
                adminOrdersContainer.appendChild(orderElement);
            });
            
            // Add event listeners to order action buttons
            document.querySelectorAll('.mark-ready').forEach(button => {
                button.addEventListener('click', markOrderReady);
            });
            
            document.querySelectorAll('.mark-completed').forEach(button => {
                button.addEventListener('click', markOrderCompleted);
            });
            
            document.querySelectorAll('.view-details').forEach(button => {
                button.addEventListener('click', viewOrderDetails);
            });
            
            // Update admin stats and orders table
            if (isAdmin) {
                updateAdminStats();
                renderOrdersTable();
            }
        }

        // Mark order as ready
        async function markOrderReady(e) {
            const orderId = e.target.getAttribute('data-id');
            const order = adminOrders.find(o => o.id === orderId);
            
            if (order) {
                order.status = 'ready';
                
                // Save to server
                await saveAllDataToServer();
                
                updateAdminPanel();
                showNotification(`Order ${orderId} marked as ready for delivery`);
                
                // Update user order status
                updateUserOrderStatus(orderId, 'ready');
                
                // Send delivery alert
                sendDeliveryAlert(order, 'ready');
            }
        }

        // Mark order as completed
        async function markOrderCompleted(e) {
            const orderId = e.target.getAttribute('data-id');
            const order = adminOrders.find(o => o.id === orderId);
            
            if (order) {
                order.status = 'completed';
                
                // Save to server
                await saveAllDataToServer();
                
                updateAdminPanel();
                showNotification(`Order ${orderId} marked as delivered`);
                
                // Update user order status
                updateUserOrderStatus(orderId, 'completed');
                
                // Send delivery alert
                sendDeliveryAlert(order, 'delivered');
            }
        }

        // Update user order status
        async function updateUserOrderStatus(orderId, status) {
            // Find which user this order belongs to
            for (const username in userOrders) {
                const userOrder = userOrders[username].find(o => o.id === orderId);
                if (userOrder) {
                    userOrder.status = status;
                    
                    // Save to server
                    await saveAllDataToServer();
                    
                    // If the current user is viewing orders and this is their order, update the display
                    if (isLoggedIn && !isAdmin && currentUser.username === username && ordersSection.classList.contains('hidden') === false) {
                        renderUserOrders();
                    }
                    break;
                }
            }
        }

        // View order details
        function viewOrderDetails(e) {
            const orderId = e.target.getAttribute('data-id');
            const order = adminOrders.find(o => o.id === orderId);
            
            if (order) {
                let details = `Order ID: ${order.id}\n`;
                details += `Customer: ${order.customer.fullName}\n`;
                details += `Phone: ${order.customer.phone}\n`;
                details += `Email: ${order.customer.email}\n`;
                details += `Address: ${order.delivery.address}\n`;
                details += `Instructions: ${order.delivery.instructions || 'None'}\n`;
                details += `Items:\n`;
                order.items.forEach(item => {
                    details += `- ${item.name} x ${item.quantity} - ₹${(item.price * item.quantity).toFixed(2)}\n`;
                });
                details += `Total: ₹${order.total.toFixed(2)}\n`;
                details += `Status: ${order.status}\n`;
                details += `Order Time: ${new Date(order.timestamp).toLocaleString()}\n`;
                
                alert(details);
            }
        }

        // Send delivery alert
        function sendDeliveryAlert(order, status) {
            const phoneNumber = "917207199308";
            const email = "puramvenkatadri@gmail.com";
            
            let message = "";
            if (status === 'ready') {
                message = `🚚 *DELIVERY ALERT - ORDER READY* 🚚\n\n`;
                message += `Order ${order.id} is ready for delivery!\n\n`;
            } else {
                message = `✅ *DELIVERY ALERT - ORDER DELIVERED* ✅\n\n`;
                message += `Order ${order.id} has been successfully delivered!\n\n`;
            }
            
            message += `*Customer:* ${order.customer.fullName}\n`;
            message += `*Phone:* ${order.customer.phone}\n`;
            message += `*Address:* ${order.delivery.address}\n`;
            message += `*Total:* ₹${order.total.toFixed(2)}\n\n`;
            message += `Please proceed with ${status === 'ready' ? 'delivery' : 'completion'} process.`;
            
            // Send WhatsApp message
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
            
            // Send email
            const subject = encodeURIComponent(`Order ${order.id} ${status === 'ready' ? 'Ready for Delivery' : 'Delivered'}`);
            const body = encodeURIComponent(message.replace(/\*/g, ''));
            const mailtoUrl = `mailto:${email}?subject=${subject}&body=${body}`;
            window.location.href = mailtoUrl;
        }

        // Send order to admin
        async function sendOrderToAdmin(orderData) {
            // Add timestamp and mark as new
            orderData.timestamp = new Date().toISOString();
            orderData.status = 'pending';
            orderData.isNew = true;
            
            // Add to admin orders
            adminOrders.push(orderData);
            
            // Save to server
            await saveAllDataToServer();
            
            // Update admin panel
            updateAdminPanel();
            
            // In a real application, you would send this to a server
            console.log('Order sent to admin:', orderData);
            
            // Remove "new" status after 10 seconds
            setTimeout(() => {
                orderData.isNew = false;
                saveAllDataToServer();
                updateAdminPanel();
            }, 10000);
        }

        // Format order details for message
        function formatOrderMessage(order) {
            let message = `🍎 *NEW FRUIT ORDER* 🍎\n\n`;
            message += `*Order ID:* ${order.id}\n`;
            message += `*Customer:* ${order.customer.fullName}\n`;
            message += `*Phone:* ${order.customer.phone}\n`;
            message += `*Email:* ${order.customer.email}\n\n`;
            message += `*Delivery Address:*\n${order.delivery.address}\n`;
            
            if (order.delivery.instructions) {
                message += `*Instructions:* ${order.delivery.instructions}\n`;
            }
            
            message += `\n*Order Items:*\n`;
            order.items.forEach(item => {
                message += `• ${item.name} x ${item.quantity} - ₹${(item.price * item.quantity).toFixed(2)}\n`;
            });
            
            message += `\n*Total Amount:* ₹${order.total.toFixed(2)}\n`;
            message += `*Order Time:* ${new Date(order.timestamp).toLocaleString()}\n\n`;
            message += `📍 *Location Details:*\n${order.delivery.location}`;
            
            return message;
        }

        // Send order notification via WhatsApp
        function sendWhatsAppNotification(order) {
            const phoneNumber = "917207199308"; // International format without +
            const message = encodeURIComponent(formatOrderMessage(order));
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${message}`;
            
            window.open(whatsappUrl, '_blank');
            showNotification('Order details opened in WhatsApp');
        }

        // Send order notification via Email
        function sendEmailNotification(order) {
            const email = "puramvenkatadri@gmail.com";
            const subject = encodeURIComponent(`New Fruit Order - ${order.id}`);
            const body = encodeURIComponent(formatOrderMessage(order).replace(/\*/g, ''));
            const mailtoUrl = `mailto:${email}?subject=${subject}&body=${body}`;
            
            window.location.href = mailtoUrl;
            showNotification('Order details opened in email client');
        }

        // Send order notification
        function sendOrderNotification(type) {
            if (cart.length === 0) {
                showNotification('Your cart is empty!');
                return;
            }
            
            // Validate form before sending
            const fullName = document.getElementById('full-name').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const city = document.getElementById('city').value;
            
            // Check if city is Anatapur
            if (city.toLowerCase() !== 'anatapur') {
                showNotification('Sorry, we currently deliver only in Anatapur area');
                return;
            }
            
            if (!fullName || !phone || !email) {
                showNotification('Please fill in your personal information first');
                return;
            }
            
            // Create order object
            const orderId = 'FC' + Date.now().toString().slice(-6);
            const formData = {
                fullName: fullName,
                phone: phone,
                email: email,
                houseNo: document.getElementById('house-no').value,
                street: document.getElementById('street').value,
                landmark: document.getElementById('landmark').value,
                city: document.getElementById('city').value,
                pincode: document.getElementById('pincode').value,
                state: document.getElementById('state').value,
                instructions: document.getElementById('instructions').value,
                location: locationInfo.textContent,
                items: [...cart],
                total: cart.reduce((total, item) => total + (item.price * item.quantity), 0)
            };
            
            const order = {
                id: orderId,
                customer: {
                    fullName: formData.fullName,
                    phone: formData.phone,
                    email: formData.email
                },
                delivery: {
                    address: `${formData.houseNo}, ${formData.street}, ${formData.landmark ? formData.landmark + ', ' : ''}${formData.city}, ${formData.state} - ${formData.pincode}`,
                    instructions: formData.instructions,
                    location: formData.location
                },
                items: formData.items,
                total: formData.total,
                status: 'pending'
            };
            
            // Send based on type
            if (type === 'whatsapp' || type === 'both') {
                sendWhatsAppNotification(order);
            }
            
            if (type === 'email' || type === 'both') {
                sendEmailNotification(order);
            }
            
            // Also send to admin panel
            sendOrderToAdmin(order);
            
            // Add to current user's orders
            const currentUserOrders = getCurrentUserOrders();
            currentUserOrders.push(order);
            saveCurrentUserOrders(currentUserOrders);
            
            showNotification(`Order notification sent via ${type === 'both' ? 'WhatsApp & Email' : type}`);
        }

        // Place order
        async function placeOrder(e) {
            e.preventDefault();
            
            // Get form values
            const formData = {
                fullName: document.getElementById('full-name').value,
                phone: document.getElementById('phone').value,
                email: document.getElementById('email').value,
                houseNo: document.getElementById('house-no').value,
                street: document.getElementById('street').value,
                landmark: document.getElementById('landmark').value,
                city: document.getElementById('city').value,
                pincode: document.getElementById('pincode').value,
                state: document.getElementById('state').value,
                instructions: document.getElementById('instructions').value,
                location: locationInfo.textContent,
                items: [...cart],
                total: cart.reduce((total, item) => total + (item.price * item.quantity), 0)
            };
            
            // Check if city is Anatapur
            if (formData.city.toLowerCase() !== 'anatapur') {
                showNotification('Sorry, we currently deliver only in Anatapur area. Please update your delivery address.');
                return;
            }
            
            // Generate order ID
            const orderId = 'FC' + Date.now().toString().slice(-6);
            
            // Create complete order object
            const order = {
                id: orderId,
                customer: {
                    fullName: formData.fullName,
                    phone: formData.phone,
                    email: formData.email
                },
                delivery: {
                    address: `${formData.houseNo}, ${formData.street}, ${formData.landmark ? formData.landmark + ', ' : ''}${formData.city}, ${formData.state} - ${formData.pincode}`,
                    instructions: formData.instructions,
                    location: formData.location
                },
                items: formData.items,
                total: formData.total,
                status: 'pending'
            };
            
            // Send order to admin
            await sendOrderToAdmin(order);
            
            // Add to current user's orders
            const currentUserOrders = getCurrentUserOrders();
            currentUserOrders.push(order);
            await saveCurrentUserOrders(currentUserOrders);
            
            // Show confirmation to user
            alert(`Order placed successfully!\n\nOrder ID: ${orderId}\nTotal: ₹${formData.total.toFixed(2)}\n\nWe will deliver to:\n${formData.fullName}\n${formData.houseNo}, ${formData.street}\n${formData.city}, ${formData.state} - ${formData.pincode}\n\nYou will receive a confirmation email shortly.`);
            
            // Clear cart and close modal
            cart = [];
            updateCart();
            closeCheckoutModal();
            checkoutForm.reset();
            locationInfo.innerHTML = '<p>Location not yet retrieved</p>';
            
            showNotification(`Order #${orderId} placed successfully!`);
        }

        // Show notification
        function showNotification(message) {
            // Create notification element
            const notification = document.createElement('div');
            notification.className = 'notification';
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            // Remove notification after 3 seconds
            setTimeout(() => {
                notification.style.transform = 'translateX(100%)';
                notification.style.opacity = '0';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // Contact form submission
        messageForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            // In a real application, this would send the data to a server
            // For this demo, we'll just show a confirmation
            alert(`Thank you for your message, ${name}! We'll get back to you at ${email} as soon as possible.`);
            
            // Reset form
            messageForm.reset();
        });
    </script>
</body>
</html>
