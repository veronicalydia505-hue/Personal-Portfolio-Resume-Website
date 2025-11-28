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
        }
:root {
            --primary: #EC4899;
            --primary-dark: #DB2777;
            --secondary: #F472B6;
            --dark: #111827;
            --darker: #0A0F1C;
            --light: #F3F4F6;
            --gray: #9CA3AF;
            --transition: all 0.3s ease;
        }
body {
            background-color: var(--darker);
            color: var(--light);
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
            background-color: rgba(17, 24, 39, 0.95);
            box-shadow: 0 2px 20px rgba(236, 72, 153, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(236, 72, 153, 0.1);
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
            color: var(--light);
        }
.logo span {
            color: var(--primary);
        }.nav-links {
            display: flex;
            list-style: none;
        }
.nav-links li {
            margin-left: 30px;
        }
.nav-links a {
            text-decoration: none;
            color: var(--light);
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
            color: var(--light);
        }
/* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
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
            background: radial-gradient(circle at 20% 80%, rgba(236, 72, 153, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
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
            color: var(--light);
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
            box-shadow: 0 4px 15px rgba(236, 72, 153, 0.3);
        }
.btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(236, 72, 153, 0.4);
        }
.btn-edit {
            background-color: var(--secondary);
            color: var(--dark);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            margin-left: 15px;
        }
.btn-edit:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-2px);
        }
.hero-image {
            flex: 1;
            text-align: center;
            position: relative;
        }
.profile-img {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            border: 10px solid rgba(236, 72, 153, 0.2);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 2;
        }
.profile-img::after {
            content: '';
            position: absolute;
            top: -15px;
            left: -15px;
            right: -15px;
            bottom: -15px;
            border-radius: 50%;
            border: 2px solid var(--primary);
            opacity: 0.3;
            z-index: -1;
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
            background-color: rgba(17, 24, 39, 0.8);
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            display: flex;
            align-items: center;
            animation: float 6s ease-in-out infinite;
            border: 1px solid rgba(236, 72, 153, 0.2);
            backdrop-filter: blur(10px);
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
            background-color: var(--dark);
            position: relative;
        }
.about::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 80% 20%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
        }
.section-title {
            text-align: center;
            margin-bottom: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
.section-title h2 {
            font-size: 36px;
            color: var(--light);
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
            color: var(--light);
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
            background-color: rgba(17, 24, 39, 0.5);
            border-radius: 10px;
            margin: 0 10px;
            border: 1px solid rgba(236, 72, 153, 0.1);
            transition: var(--transition);
        }
.stat:hover {
            transform: translateY(-5px);
            border-color: rgba(236, 72, 153, 0.3);
        }
.stat h4 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 10px;
        }
.stat p {
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
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(236, 72, 153, 0.1);
        }
/* Skills Section */
        .skills {
            padding: 100px 0;
            background-color: var(--darker);
            position: relative;
        }
.skills::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 80%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
        }
.skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
.skill-card {
            background-color: rgba(17, 24, 39, 0.5);
            padding: 40px 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
            text-align: center;
            border: 1px solid rgba(236, 72, 153, 0.1);
            backdrop-filter: blur(10px);
        }
.skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(236, 72, 153, 0.1);
            border-color: rgba(236, 72, 153, 0.3);
        }
.skill-icon {
            width: 70px;
            height: 70px;
            background-color: rgba(236, 72, 153, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            border: 1px solid rgba(236, 72, 153, 0.2);
        }
.skill-icon i {
            font-size: 30px;
            color: var(--primary);
        }
.skill-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--light);
        }
.skill-card ul {
            list-style: none;
            text-align: left;
            color: var(--gray);
        }
.skill-card li {
            margin-bottom: 8px;
            position: relative;
            padding-left: 20px;
        }
.skill-card li:before {
            content: '▹';
            position: absolute;
            left: 0;
            color: var(--primary);
        }
/* Tools Section */
        .tools {
            padding: 100px 0;
            background-color: var(--dark);
            position: relative;
        }
.tools::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 80% 20%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
        }
.tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
.tool-card {
            background-color: rgba(17, 24, 39, 0.5);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
            text-align: center;
            border: 1px solid rgba(236, 72, 153, 0.1);
            backdrop-filter: blur(10px);
        }
.tool-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(236, 72, 153, 0.1);
            border-color: rgba(236, 72, 153, 0.3);
        }
.tool-icon {
            font-size: 48px;
            color: var(--primary);
            margin-bottom: 20px;
        }
.tool-card h3 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--light);
        }

.progress-bar {
            height: 8px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            margin-bottom: 10px;
            overflow: hidden;
        }
.progress {
            height: 100%;
            background-color: var(--primary);
            border-radius: 4px;
            transition: width 1s ease-in-out;
        }
.percentage {
            font-size: 14px;
            color: var(--gray);
            font-weight: 600;
        }
/* Portfolio Section */
        .portfolio {
            padding: 100px 0;
            background-color: var(--darker);
            position: relative;
        }
.portfolio::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 80%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
        }
.portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
.portfolio-item {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
            position: relative;
            border: 1px solid rgba(236, 72, 153, 0.1);
        }
.portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(236, 72, 153, 0.1);
            border-color: rgba(236, 72, 153, 0.3);
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
            background: linear-gradient(to bottom, transparent, rgba(17, 24, 39, 0.9));
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
.tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 10px;
        }
.tech-tag {
            background-color: rgba(236, 72, 153, 0.2);
            color: var(--primary);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }
/* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: var(--dark);
            position: relative;
        }
.contact::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 80% 20%, rgba(236, 72, 153, 0.05) 0%, transparent 50%);
        }
.contact-content {
            display: flex;
            gap: 50px;
        }.contact-info {
            flex: 1;
        }
.contact-info h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--light);
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
            background-color: rgba(17, 24, 39, 0.5);
            border: 1px solid rgba(236, 72, 153, 0.2);
            border-radius: 5px;
            font-size: 16px;
            transition: var(--transition);
            color: var(--light);
        }
.form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 2px rgba(236, 72, 153, 0.2);
        }
textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
.form-control::placeholder {
            color: var(--gray);
        }
 /* Footer */
        footer {
            background-color: var(--darker);
            color: white;
            padding: 50px 0 20px;
            border-top: 1px solid rgba(236, 72, 153, 0.1);
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
            color: var(--light);
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
            color: var(--primary);
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
/* Edit Modal */
        .edit-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }
.edit-modal-content {
            background-color: var(--dark);
            padding: 2rem;
            border-radius: 10px;
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
            border: 1px solid rgba(236, 72, 153, 0.2);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
.edit-modal h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--light);
            border-bottom: 1px solid rgba(236, 72, 153, 0.2);
            padding-bottom: 10px;
        }
.edit-textarea {
            width: 100%;
            min-height: 150px;
            background-color: rgba(17, 24, 39, 0.5);
            color: var(--light);
            border: 1px solid rgba(236, 72, 153, 0.2);
            border-radius: 5px;
            padding: 12px;
            margin-bottom: 1rem;
            resize: vertical;
        }
.edit-input {
            width: 100%;
            background-color: rgba(17, 24, 39, 0.5);
            color: var(--light);
            border: 1px solid rgba(236, 72, 153, 0.2);
            border-radius: 5px;
            padding: 12px;
            margin-bottom: 1rem;
        }
 .edit-modal-buttons {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
            margin-top: 20px;
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
                background-color: rgba(17, 24, 39, 0.95);
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                backdrop-filter: blur(10px);
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
                font-size: 24px;
            }
            .profile-img {
                width: 250px;
                height: 250px;
            }
            .footer-content {
                flex-direction: column;
                gap: 30px;
            }
            .about-stats {
                flex-direction: column;
                gap: 15px;
            }
            .stat {
                margin: 0;
            }
            .section-title {
                flex-direction: column;
                gap: 15px;
            }
            
.btn-edit {
                margin-left: 0;
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
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#tools">Tools</a></li>
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
                    <h2>Multimedia Computing Student</h2>
                    <p>A motivated, creative, and fast-learning third-year student at UNIMAS, skilled in UI/UX design, Java, Python, and web development. Seeking an internship to apply technical expertise in real-world technology projects.</p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
                <div class="hero-image">
                    <!-- Using the profile picture from your screenshot -->
                    <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80" alt="Nurul Hidayu" class="profile-img">
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
                <button onclick="editSection('about')" class="btn-edit">
                    Edit Section
                </button>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>I'm Nurul Hidayu, a Multimedia Computing Student at UNIMAS</h3>
                    <p id="about-text-1">Currently pursuing a Bachelor of Multimedia Computing (Hons) at Universiti Malaysia Sarawak (UNIMAS). My academic journey has equipped me with strong foundational knowledge in programming languages like Java, Python, HTML/CSS, and Kotlin, complemented by expertise in UI/UX design using tools like Figma.</p>
                    <p id="about-text-2">I thrive in team environments, focusing on effective communication and problem-solving to deliver high-quality, user-centric solutions. I am actively seeking an internship opportunity to apply and grow these technical and creative skills in the professional tech industry.</p>
                    <div class="about-stats">
                        <div class="stat">
                            <h4>3+</h4>
                            <p>Years of Study</p>
                        </div>
                        <div class="stat">
                            <h4>10+</h4>
                            <p>Projects Completed</p>
                        </div>
                        <div class="stat">
                            <h4>5+</h4>
                            <p>Technologies</p>
                        </div>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" alt="About Me">
                </div>
            </div>
        </div>
    </section>
<!-- Skills Section -->
    <section class="skills" id="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
                <button onclick="editSection('skills')" class="btn-edit">
                    Edit Section
                </button>
            </div>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>Programming</h3>
                    <ul id="programming-skills">
                        <li>Java</li>
                        <li>Python</li>
                        <li>HTML / CSS / JavaScript</li>
                        <li>C / C++</li>
                        <li>Kotlin</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-pencil-ruler"></i>
                    </div>
                    <h3>Design & Tools</h3>
                    <ul id="design-skills">
                        <li>Figma (UI/UX Design)</li>
                        <li>Canva (Graphics)</li>
                        <li>Unity (Game Design)</li>
                        <li>MySQL (Database)</li>
                        <li>PHP (Web Backend)</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Soft Skills</h3>
                    <ul id="soft-skills">
                        <li>Teamwork</li>
                        <li>Communication</li>
                        <li>Leadership</li>
                        <li>Problem Solving</li>
                        <li>Fast Learning</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
<!-- Tools Section -->
    <section class="tools" id="tools">
        <div class="container">
            <div class="section-title">
                <h2>My Expertise In Tools</h2>
                <button onclick="editSection('tools')" class="btn-edit">
                    Edit Section
                </button>
            </div>
            <div class="tools-grid">
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fab fa-sketch"></i>
                    </div>
                    <h3>SKETCH</h3>
                    <div class="progress-bar">
                        <div class="progress" style="width: 95%"></div>
                    </div>
                    <div class="percentage">95%</div>
                </div>
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fab fa-adobe"></i>
                    </div>
                    <h3>PHOTOSHOP</h3>
                    <div class="progress-bar">
                        <div class="progress" style="width: 95%"></div>
                    </div>
                    <div class="percentage">95%</div>
                </div>
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fab fa-adobe"></i>
                    </div>
                    <h3>ILLUSTRATOR</h3>
                    <div class="progress-bar">
                        <div class="progress" style="width: 95%"></div>
                    </div>
                    <div class="percentage">95%</div>
                </div>
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fab fa-figma"></i>
                    </div>
                    <h3>FIGMA</h3>
                    <div class="progress-bar">
                        <div class="progress" style="width: 90%"></div>
                    </div>
                    <div class="percentage">90%</div>
                </div>
            </div>
        </div>
    </section>
<!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>Latest Projects</h2>
                <button onclick="editSection('portfolio')" class="btn-edit">
                    Edit Section
                </button>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80" alt="Project 1" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <div class="portfolio-info">
                            <h3 id="project-1-title">Mental Health Awareness Web Application</h3>
                            
