<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurul Hidayu - UI/UX Designer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }:root {
            --primary: #6C63FF;
            --secondary: #FF6584;
            --dark: #2D2B55;
            --light: #F8F9FA;
            --gray: #6C757D;
            --transition: all 0.3s ease;
        }
body {
            background-color: var(--light);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
.container {
            width: 100%;
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
.navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
.logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--dark);
        }
.logo span {
            color: var(--primary);
        }
.nav-links {
            display: flex;
            list-style: none;
        }
.nav-links li {
            margin-left: 30px;
        }

.nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

.nav-links a:hover {
            color: var(--primary);
        }
.nav-links a.active {
            color: var(--primary);
        }
.nav-links a.active::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: var(--primary);
        }
.mobile-menu {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }
 /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            position: relative;
            overflow: hidden;
        }
.hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
.hero-text {
            flex: 1;
            padding-right: 50px;
        }
.hero-text h1 {
            font-size: 48px;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--dark);
        }
.hero-text h1 span {
            color: var(--primary);
        }
.hero-text h2 {
            font-size: 28px;
            font-weight: 500;
            margin-bottom: 30px;
            color: var(--gray);
        }
.hero-text p {
            font-size: 18px;
            margin-bottom: 40px;
            color: var(--gray);
            max-width: 500px;
        }
.btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary);
            color: white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(108, 99, 255, 0.3);
        }
.btn:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 101, 132, 0.4);
        }
.hero-image {
            flex: 1;
            text-align: center;
            position: relative;
        }.profile-img {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            border: 10px solid white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
.floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
        }
.floating-element {
            position: absolute;
            background-color: white;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            animation: float 6s ease-in-out infinite;
        }
.floating-element:nth-child(1) {
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }
.floating-element:nth-child(2) {
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }
.floating-element:nth-child(3) {
            bottom: 20%;
            left: 5%;
            animation-delay: 4s;
        }
.floating-element i {
            font-size: 24px;
            margin-right: 10px;
            color: var(--primary);
        }
 @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
            100% {
                transform: translateY(0);
            }
        }
/* About Section */
        .about {
            padding: 100px 0;
            background-color: white;
        }
.section-title {
            text-align: center;
            margin-bottom: 60px;
        }
.section-title h2 {
            font-size: 36px;
            color: var(--dark);
            margin-bottom: 15px;
        }
.section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
.about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
.about-text {
            flex: 1;
        }
.about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--dark);
        }
.about-text p {
            margin-bottom: 20px;
            color: var(--gray);
        }
 .about-stats {
            display: flex;
            margin-top: 30px;
        }
.stat {
            flex: 1;
            text-align: center;
            padding: 20px;
        }
.stat h4 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 10px;
        }.stat p {
            color: var(--gray);
            font-weight: 500;
        }
.about-image {
            flex: 1;
            text-align: center;
        }
.about-image img {
            width: 100%;
            max-width: 400px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
/* Services Section */
        .services {
            padding: 100px 0;
            background-color: #f8f9fa;
        }
.services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
.service-card {
            background-color: white;
            padding: 40px 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            text-align: center;
        }
.service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
.service-icon {
            width: 70px;
            height: 70px;
            background-color: rgba(108, 99, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
        }
.service-icon i {
            font-size: 30px;
            color: var(--primary);
        }
.service-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--dark);
        }
.service-card p {
            color: var(--gray);
        }
/* Portfolio Section */
        .portfolio {
            padding: 100px 0;
            background-color: white;
        }
.portfolio-filter {
            display: flex;
            justify-content: center;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }
.filter-btn {
            padding: 8px 20px;
            margin: 0 5px 10px;
            background-color: transparent;
            border: 1px solid var(--gray);
            border-radius: 30px;
            color: var(--gray);
            cursor: pointer;
            transition: var(--transition);
        }
.filter-btn.active, .filter-btn:hover {
            background-color: var(--primary);
            border-color: var(--primary);
            color: white;
        }
.portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
.portfolio-item {
        border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            position: relative;
        }
.portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
.portfolio-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
.portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, transparent, rgba(45, 43, 85, 0.8));
            display: flex;
            align-items: flex-end;
            padding: 20px;
            opacity: 0;
            transition: var(--transition);
        }
.portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }
.portfolio-info h3 {
            color: white;
            margin-bottom: 5px;
        }
.portfolio-info p {
            color: rgba(255, 255, 255, 0.8);
            font-size: 14px;
        }
/* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: #f8f9fa;
        }
.contact-content {
            display: flex;
            gap: 50px;
        }
.contact-info {
            flex: 1;
        }
.contact-info h3 {
            font-size: 24px;
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
.contact-detail {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

.contact-detail i {
            width: 40px;
            height: 40px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
        }
.contact-form {
            flex: 1;
        }
.form-group {
            margin-bottom: 20px;
        }
.form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            transition: var(--transition);
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
            padding: 50px 0 20px;
        }

.footer-content {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
        }
.footer-logo {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
        }
.footer-links h4 {
            margin-bottom: 20px;
            font-size: 18px;
        }
.footer-links ul {
            list-style: none;
        }
.footer-links li {
            margin-bottom: 10px;
        }
.footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
        }
.footer-links a:hover {
            color: white;
        }

.social-links {
            display: flex;
            gap: 15px;
        }

.social-links a {
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: var(--transition);
        }
.social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
.copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.7);
            font-size: 14px;
        }
/* Responsive Styles */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column-reverse;
            }
            
.hero-text {
                padding-right: 0;
                text-align: center;
                margin-top: 50px;
            }
            .about-content {
                flex-direction: column;
            }
            
.contact-content {
                flex-direction: column;
            }
        }

@media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }
            .nav-links.active {
                display: flex;
            }
            
.nav-links li {
                margin: 10px 0;
            }
            
.mobile-menu {
                display: block;
            }
            
.hero-text h1 {
                font-size: 36px;
            }
            
.hero-text h2 {
                fontSize: 24px;
            }
            .profile-img {
                width: 250px;
                height: 250px;
            }
    .footer-content {
                flex-direction: column;
                gap: 30px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">Nurul<span>Hidayu</span></div>
                <ul class="nav-links">
                    <li><a href="#home" class="active">Home</a></li>
                    <li><a href="#about">About Me</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="mobile-menu">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>
<!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Hello, I'm <span>Nurul Hidayu</span></h1>
                    <h2>A Professional UI/UX Designer</h2>
                    <p>I create beautiful, functional, and user-centered digital experiences. With a passion for clean design and seamless interactions.</p>
                    <a href="#contact" class="btn">Hire Me</a>
                </div>
                <div class="hero-image">
                    <!-- Using the profile picture from your screenshot -->
                    <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzUwIiBoZWlnaHQ9IjM1MCIgdmlld0JveD0iMCAwIDM1MCAzNTAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIzNTAiIGhlaWdodD0iMzUwIiByeD0iMTc1IiBmaWxsPSIjNkM2M0ZGIi8+CjxjaXJjbGUgY3g9IjE3NSIgY3k9IjE0MCIgcj0iNjAiIGZpbGw9IiNGRjY1ODQiLz4KPHBhdGggZD0iTTEwMCAyODBDMTAwIDI0MCAxMzAgMjEwIDE3NSAyMTBDMjIwIDIxMCAyNTAgMjQwIDI1MCAyODBWMzUwSDEwMFYyODBaIiBmaWxsPSIjRkY2NTg0Ii8+CjxjaXJjbGUgY3g9IjE0NSIgY3k9IjEzMCIgcj0iMTAiIGZpbGw9IndoaXRlIi8+CjxjaXJjbGUgY3g9IjIwNSIgY3k9IjEzMCIgcj0iMTAiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xNDAgMTgwTDE2MCAyMDBMMjEwIDE2MCIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSI1IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+" alt="Nurul Hidayu" class="profile-img">
                    <div class="floating-elements">
                        <div class="floating-element">
                            <i class="fas fa-palette"></i>
                            <span>UI/UX Design</span>
                        </div>
                        <div class="floating-element">
                            <i class="fas fa-mobile-alt"></i>
                            <span>Mobile Apps</span>
                        </div>
                        <div class="floating-element">
                            <i class="fas fa-code"></i>
                            <span>Web Development</span>
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
                <h2>About Me</h2>
                <p>Get to know more about my background, skills, and experience</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>I'm Nurul Hidayu, a UI/UX Designer based in Malaysia</h3>
                    <p>I'm a passionate UI/UX designer with a strong focus on creating intuitive and engaging user experiences. With a background in Multimedia Computing, I combine technical knowledge with creative design to deliver solutions that are both beautiful and functional.</p>
                    <p>My design process is user-centered, starting with research and ending with pixel-perfect interfaces that solve real problems. I believe in the power of design to transform digital experiences and create meaningful connections between users and products.</p>
                    <div class="about-stats">
                        <div class="stat">
                            <h4>50+</h4>
                            <p>Projects Completed</p>
                        </div>
                        <div class="stat">
                            <h4>3+</h4>
                            <p>Years Experience</p>
                        </div>
                        <div class="stat">
                            <h4>30+</h4>
                            <p>Happy Clients</p>
                        </div>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" alt="About Me">
                </div>
            </div>
        </div>
    </section>
<!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>My Services</h2>
                <p>I offer a wide range of services to help bring your digital ideas to life</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-pencil-ruler"></i>
                    </div>
                    <h3>UI/UX Design</h3>
                    <p>Creating intuitive and engaging user interfaces with a focus on user experience and usability testing.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Mobile App Design</h3>
                    <p>Designing responsive and user-friendly mobile applications for iOS and Android platforms.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>Web Design</h3>
                    <p>Developing modern, responsive websites that provide optimal user experience across all devices.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-bullhorn"></i>
                    </div>
                    <h3>Branding</h3>
                    <p>Creating cohesive brand identities that communicate your values and resonate with your audience.</p>
                </div>
            </div>
        </div>
    </section>
<!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>My Portfolio</h2>
                <p>Check out some of my recent work and projects</p>
            </div>
            <div class="portfolio-filter">
                <button class="filter-btn active" data-filter="all">All</button>
                <button class="filter-btn" data-filter="ui-ux">UI/UX Design</button>
                <button class="filter-btn" data-filter="web">Web Design</button>
                <button class="filter-btn" data-filter="mobile">Mobile Apps</button>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item" data-category="ui-ux">
                    <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80" alt="Project 1" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <div class="portfolio-info">
                            <h3>E-commerce App Design</h3>
                            <p>UI/UX Design</p>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item" data-category="web">
                    <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1115&q=80" alt="Project 2" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <div class="portfolio-info">
                            <h3>Corporate Website</h3>
                            <p>Web Design</p>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item" data-category="mobile">
                    <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Project 3" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <div class="portfolio-info">
                            <h3>Fitness Mobile App</h3>
                            <p>Mobile App</p>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item" data-category="ui-ux">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Project 4" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <div class="portfolio-info">
                            <h3>Dashboard Design</h3>
                            <p>UI/UX Design</p>
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
                <h2>Get In Touch</h2>
                <p>Feel free to reach out for collaborations or just a friendly hello</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Let's Talk About Your Project</h3>
                    <p>I'm always interested in new opportunities and challenges. Whether you have a project in mind or just want to say hello, I'd love to hear from you.</p>
                    <div class="contact-details">
                        <div class="contact-detail">
                            <i class="fas fa-phone-alt"></i>
                            <span>+60 193375235</span>
                        </div>
                        <div class="contact-detail">
                            <i class="fas fa-envelope"></i>
                            <span>nurulhidayu1111@gmail.com</span>
                        </div>
                        <div class="contact-detail">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Kuching, Sarawak, Malaysia</span>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-dribbble"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Subject">
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" placeholder="Your Message" required></textarea>
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
                <div class="footer-about">
                    <div class="footer-logo">Nurul<span>Hidayu</span></div>
                    <p>A passionate UI/UX designer creating beautiful and functional digital experiences.</p>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#portfolio">Portfolio</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Services</h4>
                    <ul>
                        <li><a href="#">UI/UX Design</a></li>
                        <li><a href="#">Web Design</a></li>
                        <li><a href="#">Mobile App Design</a></li>
                        <li><a href="#">Branding</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Connect With Me</h4>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Nurul Hidayu. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
<script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });

// Portfolio Filter
        const filterButtons = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');
filterButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons
                filterButtons.forEach(btn => btn.classList.remove('active'));
                // Add active class to clicked button
                button.classList.add('active');
                const filterValue = button.getAttribute('data-filter');
                portfolioItems.forEach(item => {
                    if (filterValue === 'all' || item.getAttribute('data-category') === filterValue) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
// Smooth Scrolling for Navigation Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    // Close mobile menu if open
                    document.querySelector('.nav-links').classList.remove('active');
                }
            });
        });
// Active Navigation Link on Scroll
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-links a');
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
