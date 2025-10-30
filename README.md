# Himalayanherbsnepal
Himalayan Herbs Nepal exports premium Himalayan herbal products worldwide — pure, sustainable, and crafted by nature
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern E-Commerce Website</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4361ee;
            --secondary: #3a0ca3;
            --accent: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4bb543;
            --gray: #6c757d;
            --light-gray: #e9ecef;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: 10px;
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .header-actions {
            display: flex;
            align-items: center;
        }

        .header-actions a {
            margin-left: 20px;
            color: var(--dark);
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .header-actions a:hover {
            color: var(--primary);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 150px 0 100px;
            margin-top: 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,186.7C384,213,480,235,576,213.3C672,192,768,128,864,128C960,128,1056,192,1152,192C1248,192,1344,128,1392,96L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--accent);
            color: white;
            border: none;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .btn:hover {
            background-color: #3ab0d6;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
        }

        /* Products Section */
        .products {
            padding: 100px 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--primary);
            border-radius: 2px;
        }

        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .product-img {
            height: 200px;
            background-color: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .product-img i {
            font-size: 4rem;
            color: var(--primary);
        }

        .product-info {
            padding: 20px;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .product-info p {
            color: var(--gray);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .product-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--primary);
        }

        .add-to-cart {
            background-color: var(--primary);
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .add-to-cart:hover {
            background-color: var(--secondary);
        }

        /* About Section */
        .about {
            padding: 100px 0;
            background-color: var(--light);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-img {
            height: 400px;
            background-color: var(--light-gray);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .about-img i {
            font-size: 8rem;
            color: var(--primary);
        }

        .about-text h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--gray);
        }

        .features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .feature {
            display: flex;
            align-items: flex-start;
        }

        .feature i {
            color: var(--success);
            font-size: 1.5rem;
            margin-right: 15px;
            margin-top: 5px;
        }

        /* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .contact-info p {
            margin-bottom: 30px;
            color: var(--gray);
        }

        .contact-details {
            margin-bottom: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .contact-item i {
            width: 40px;
            height: 40px;
            background-color: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: var(--primary);
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            background-color: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--dark);
            transition: all 0.3s;
        }

        .social-links a:hover {
            background-color: var(--primary);
            color: white;
        }

        .contact-form {
            background-color: var(--light);
            padding: 30px;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-control:focus {
            border-color: var(--primary);
            outline: none;
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 70px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background-color: var(--primary);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 12px;
        }

        .footer-column ul li a {
            color: #b0b0b0;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: white;
        }

        .footer-column p {
            color: #b0b0b0;
            margin-bottom: 20px;
        }

        .newsletter-form {
            display: flex;
            margin-top: 15px;
        }

        .newsletter-form input {
            flex: 1;
            padding: 12px 15px;
            border: none;
            border-radius: 5px 0 0 5px;
            font-size: 1rem;
        }

        .newsletter-form button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0 20px;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .newsletter-form button:hover {
            background-color: var(--secondary);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #b0b0b0;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }

            .about-img {
                height: 300px;
            }

            .hero h1 {
                font-size: 2.8rem;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
            }

            .mobile-menu {
                display: block;
            }

            .header-actions a:not(.mobile-menu) {
                display: none;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .features {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            .products-grid {
                grid-template-columns: 1fr;
            }

            .hero {
                padding: 120px 0 80px;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-cube"></i>
                ModernStore
            </a>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="header-actions">
                <a href="#"><i class="fas fa-search"></i></a>
                <a href="#"><i class="fas fa-shopping-cart"></i></a>
                <a href="#" class="mobile-menu"><i class="fas fa-bars"></i></a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Elevate Your Shopping Experience</h1>
            <p>Discover premium products with exceptional quality and design. We bring you the best from around the world.</p>
            <a href="#products" class="btn">Shop Now</a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-title">
                <h2>Featured Products</h2>
                <p>Check out our carefully curated selection of premium products</p>
            </div>
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-headphones"></i>
                    </div>
                    <div class="product-info">
                        <h3>Wireless Headphones</h3>
                        <p>Premium sound quality with noise cancellation technology</p>
                        <div class="product-price">
                            <span class="price">$199.99</span>
                            <button class="add-to-cart">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <div class="product-info">
                        <h3>Smartphone Pro</h3>
                        <p>Latest technology with advanced camera and performance</p>
                        <div class="product-price">
                            <span class="price">$899.99</span>
                            <button class="add-to-cart">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-laptop"></i>
                    </div>
                    <div class="product-info">
                        <h3>Ultrabook Laptop</h3>
                        <p>Lightweight and powerful for work and entertainment</p>
                        <div class="product-price">
                            <span class="price">$1299.99</span>
                            <button class="add-to-cart">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-smartwatch"></i>
                    </div>
                    <div class="product-info">
                        <h3>Smart Watch</h3>
                        <p>Track your fitness and stay connected on the go</p>
                        <div class="product-price">
                            <span class="price">$249.99</span>
                            <button class="add-to-cart">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Us</h2>
                <p>Learn more about our story and what makes us different</p>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <i class="fas fa-store"></i>
                </div>
                <div class="about-text">
                    <h2>We're Passionate About Quality</h2>
                    <p>Founded in 2015, ModernStore has been committed to providing customers with high-quality products that combine innovative design with exceptional functionality.</p>
                    <p>Our team carefully selects each item in our collection, ensuring they meet our strict standards for quality, sustainability, and value.</p>
                    <div class="features">
                        <div class="feature">
                            <i class="fas fa-check-circle"></i>
                            <div>
                                <h4>Premium Quality</h4>
                                <p>All products are carefully tested</p>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-check-circle"></i>
                            <div>
                                <h4>Fast Shipping</h4>
                                <p>Free delivery on orders over $50</p>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-check-circle"></i>
                            <div>
                                <h4>24/7 Support</h4>
                                <p>Our team is here to help you</p>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-check-circle"></i>
                            <div>
                                <h4>Secure Payment</h4>
                                <p>Your transactions are protected</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch with our team for any inquiries</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Let's Talk</h3>
                    <p>Have questions about our products or services? We're here to help and answer any questions you might have.</p>
                    <div class="contact-details">
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>Our Location</h4>
                                <p>123 Commerce Street, City, State 12345</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>Phone Number</h4>
                                <p>+1 (555) 123-4567</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>Email Address</h4>
                                <p>info@modernstore.com</p>
                            </div>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Your Name">
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="Your Email">
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" placeholder="Subject">
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" placeholder="Your Message"></textarea>
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
                    <h3>ModernStore</h3>
                    <p>Your trusted source for premium products with exceptional quality and design.</p>
                    <div class="newsletter-form">
                        <input type="email" placeholder="Your email">
                        <button type="submit"><i class="fas fa-paper-plane"></i></button>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#products">Products</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Categories</h3>
                    <ul>
                        <li><a href="#">Electronics</a></li>
                        <li><a href="#">Home & Garden</a></li>
                        <li><a href="#">Fashion</a></li>
                        <li><a href="#">Sports & Outdoors</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Customer Service</h3>
                    <ul>
                        <li><a href="#">Shipping Policy</a></li>
                        <li><a href="#">Return Policy</a></li>
                        <li><a href="#">FAQ</a></li>
                        <li><a href="#">Terms & Conditions</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 ModernStore. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript for mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav ul').style.display = 
                document.querySelector('nav ul').style.display === 'flex' ? 'none' : 'flex';
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
