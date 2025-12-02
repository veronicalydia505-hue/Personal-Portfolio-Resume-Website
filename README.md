<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurul Hidayu - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-bg: #0a0a0a;
            --secondary-bg: #1a1a1a;
            --accent-color: #e91e63;
            --accent-light: #ff4081;
            --text-color: #f5f5f5;
            --text-muted: #b0b0b0;
            --card-bg: #1f1f1f;
            --border-color: #333;
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
            background-color: var(--primary-bg);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
            height: 100vh;
        }
        .container {
            max-width: 1920px;
            margin: 0 auto;
            padding: 0 40px;
        }
        /* Scroll Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }
        .fade-in.appear {
            opacity: 1;
            transform: translateY(0);
        }
        /* Header Styles */
        header {
            background-color: var(--secondary-bg);
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            transform: translateY(0);
            transition: transform 0.5s ease, background-color 0.5s ease;
        }
        header.scrolled {
            background-color: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(10px);
        }
        header.hidden {
            transform: translateY(-100%);
        }
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            animation: slideInDown 0.8s ease-out;
        }
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--accent-color);
            position: relative;
            overflow: hidden;
        }
        .logo::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
            transform: translateX(-100%);
            animation: logoUnderline 3s infinite;
        }
        @keyframes logoUnderline {
            0%, 100% {
                transform: translateX(-100%);
            }
            50% {
                transform: translateX(100%);
            }
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin-left: 30px;
            position: relative;
        }
        nav ul li a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
            padding: 5px 0;
        }
        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent-color);
            transition: width 0.3s ease;
        }
        nav ul li a:hover {
            color: var(--accent-color);
        }
        nav ul li a:hover::after {
            width: 100%;
        }
         /* Hero Section - Full Page */
        .hero {
            padding: 120px 0 80px;
            background: linear-gradient(135deg, var(--primary-bg) 0%, #2a0a1a 100%);
            text-align: center;
            min-height: 100vh;
            display: flex;
            align-items: center;
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
            background: radial-gradient(circle at 20% 50%, rgba(233, 30, 99, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(255, 64, 129, 0.1) 0%, transparent 50%);
            animation: floatBackground 20s infinite alternate ease-in-out;
        }
        @keyframes floatBackground {
            0%, 100% {
                transform: translate(0, 0);
            }
            33% {
                transform: translate(-20px, 20px);
            }
            66% {
                transform: translate(20px, -20px);
            }
        }
        .profile-container {
            margin-bottom: 40px;
            position: relative;
            animation: float 6s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
        }
        .profile-pic {
            width: 220px;
            height: 220px;
            border-radius: 50%;
            object-fit: cover;
            border: 6px solid var(--accent-color);
            box-shadow: 0 0 40px rgba(233, 30, 99, 0.4);
            animation: pulse 4s infinite;
        }
        @keyframes pulse {
            0%, 100% {
                box-shadow: 0 0 40px rgba(233, 30, 99, 0.4);
            }
            50% {
                box-shadow: 0 0 60px rgba(233, 30, 99, 0.6);
            }
        }
        .hero h1 {
            font-size: 56px;
            margin-bottom: 15px;
            animation: fadeInUp 1s ease 0.3s both;
        }
        .hero h2 {
            font-size: 28px;
            color: var(--accent-color);
            margin-bottom: 30px;
            animation: fadeInUp 1s ease 0.5s both;
        }
        .hero p {
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--text-muted);
            font-size: 18px;
            animation: fadeInUp 1s ease 0.7s both;
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            animation: fadeInUp 1s ease 0.9s both;
        }
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }
        .btn:hover::before {
            left: 100%;
        }
        .btn:hover {
            background-color: var(--accent-light);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(233, 30, 99, 0.5);
        }
        /* Section Styles - Full Page */
        section {
            padding: 80px 0;
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
        }
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        .section-title h2 {
            font-size: 42px;
            display: inline-block;
            padding-bottom: 15px;
        }
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--accent-color);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        .about-text h3 {
            font-size: 32px;
            margin-bottom: 25px;
        }
        .about-text p {
            margin-bottom: 25px;
            color: var(--text-muted);
            font-size: 17px;
            line-height: 1.8;
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 25px;
        }
        .skill-item {
            background-color: var(--card-bg);
            padding: 25px;
            border-radius: 12px;
            border-left: 5px solid var(--accent-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .skill-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        .skill-item h4 {
            margin-bottom: 15px;
            font-size: 18px;
            display: flex;
            justify-content: space-between;
        }
        .skill-bar {
            height: 10px;
            background-color: var(--secondary-bg);
            border-radius: 5px;
            overflow: hidden;
            position: relative;
        }
        .skill-progress {
            height: 100%;
            background-color: var(--accent-color);
            border-radius: 5px;
            width: 0;
            transition: width 1.5s ease-in-out;
        }
        .skill-progress.animated {
            animation: progressAnimation 1.5s ease-in-out forwards;
        }
        @keyframes progressAnimation {
            from {
                width: 0;
            }
        }
        /* Portfolio Section */
        .portfolio-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
        }
        .add-project-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            font-size: 28px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        .add-project-btn::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.2) 1%, transparent 1%);
            background-size: 10px 10px;
            opacity: 0;
            transition: opacity 0.3s;
        }
        .add-project-btn:hover::before {
            opacity: 1;
            animation: ripple 0.6s linear;
        }
        @keyframes ripple {
            from {
                transform: scale(0);
            }
            to {
                transform: scale(4);
                opacity: 0;
            }
        }
        .add-project-btn:hover {
            background-color: var(--accent-light);
            transform: rotate(90deg);
        }
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 40px;
        }
        .portfolio-item {
            background-color: var(--card-bg);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
            position: relative;
            height: 100%;
        }
        .portfolio-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(233, 30, 99, 0.1), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s ease;
        }
        .portfolio-item:hover::before {
            transform: translateX(100%);
        }
        .portfolio-item:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }
        .portfolio-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        .portfolio-item:hover .portfolio-img {
            transform: scale(1.05);
        }
        .portfolio-content {
            padding: 25px;
        }
        .portfolio-content h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }
        .portfolio-content p {
            color: var(--text-muted);
            margin-bottom: 20px;
            font-size: 16px;
            line-height: 1.6;
        }
        .portfolio-actions {
            display: flex;
            justify-content: space-between;
        }
        .btn-small {
            padding: 10px 20px;
            font-size: 14px;
        }
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--accent-color);
        }
        .btn-outline:hover {
            background-color: var(--accent-color);
        }
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            align-items: center;
            justify-content: center;
            animation: fadeIn 0.3s ease-out;
        }
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        .modal-content {
            background-color: var(--card-bg);
            width: 90%;
            max-width: 900px;
            border-radius: 15px;
            padding: 40px;
            position: relative;
            max-height: 90vh;
            overflow-y: auto;
            animation: slideUp 0.5s ease-out;
        }
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 28px;
            cursor: pointer;
            color: var(--text-muted);
            transition: transform 0.3s, color 0.3s;
        }
        .close-modal:hover {
            color: var(--accent-color);
            transform: rotate(90deg);
        }
        .modal-header {
            margin-bottom: 25px;
        }
        .modal-body {
            margin-bottom: 25px;
        }
        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
        }
        /* Form Styles */
        .form-group {
            margin-bottom: 25px;
        }
        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 500;
            font-size: 16px;
        }
        .form-control {
            width: 100%;
            padding: 15px;
            background-color: var(--secondary-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            color: var(--text-color);
            transition: border-color 0.3s, box-shadow 0.3s;
            font-size: 16px;
        }
        .form-control:focus {
            outline: none;
            border-color: var(--accent-color);
            box-shadow: 0 0 0 3px rgba(233, 30, 99, 0.2);
        }
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 20px;
            transition: transform 0.3s ease;
        }
        .contact-item:hover {
            transform: translateX(15px);
        }
        .contact-icon {
            width: 60px;
            height: 60px;
            background-color: var(--accent-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: transform 0.3s ease, background-color 0.3s;
        }
        .contact-item:hover .contact-icon {
            transform: scale(1.1) rotate(10deg);
            background-color: var(--accent-light);
        }
        .contact-item div h3 {
            margin-bottom: 5px;
            font-size: 20px;
        }
        .contact-item div p {
            color: var(--text-muted);
            font-size: 16px;
        }
        /* Footer */
        footer {
            background-color: var(--secondary-bg);
            padding: 50px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
            animation: shimmer 3s infinite linear;
        }
        @keyframes shimmer {
            0% {
                background-position: -1000px 0;
            }
            100% {
                background-position: 1000px 0;
            }
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-bottom: 30px;
        }
        .social-links a {
            color: var(--text-color);
            font-size: 24px;
            transition: all 0.3s ease;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--card-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        .social-links a::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--accent-color), var(--accent-light));
            opacity: 0;
            transition: opacity 0.3s;
            border-radius: 50%;
        }
        .social-links a:hover::before {
            opacity: 1;
        }
        .social-links a i {
            position: relative;
            z-index: 1;
        }
        .social-links a:hover {
            color: white;
            transform: translateY(-8px) rotate(10deg);
        }
        .copyright {
            color: var(--text-muted);
            font-size: 16px;
            animation: fadeIn 2s ease;
        }
        /* Particles Animation */
        .particles {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 0;
        }
        .particle {
            position: absolute;
            background-color: var(--accent-color);
            border-radius: 50%;
            opacity: 0.3;
        }
        /* Scroll Progress Indicator */
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            width: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-color), var(--accent-light));
            z-index: 1001;
            transition: width 0.1s ease;
        }
        /* Responsive Design */
        @media (max-width: 1200px) {
            .container {
                padding: 0 30px;
            }
        }
    @media (max-width: 992px) {
            .about-content, .contact-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            .skills-grid {
                grid-template-columns: 1fr;
            }
            .portfolio-grid {
                grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
                gap: 30px;
            }
        }@media (max-width: 768px) {
            .container {
                padding: 0 20px;
            }
            .hero h1 {
                font-size: 42px;
            }
            .hero h2 {
                font-size: 24px;
            }
            .hero p {
                font-size: 16px;
            }
            .section-title h2 {
                font-size: 36px;
            }
            nav ul {
                flex-direction: column;
                gap: 10px;
            }
            nav ul li {
                margin-left: 0;
            }
            .portfolio-header {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }
            .add-project-btn {
                margin-top: 10px;
            }
            .profile-pic {
                width: 180px;
                height: 180px;
            }
        }
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 36px;
            }
            .hero h2 {
                font-size: 20px;
            }
            .profile-pic {
                width: 150px;
                height: 150px;
            }
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
            .btn {
                padding: 12px 30px;
                font-size: 14px;
            }
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: var(--secondary-bg);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--accent-color);
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: var(--accent-light);
        }
    </style>
</head>
<body>
    <!-- Scroll Progress Indicator -->
    <div class="scroll-progress" id="scrollProgress"></div>
    <!-- Header -->
    <header id="mainHeader">
        <div class="container header-content">
            <div class="logo">NURUL HIDAYU </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
<!-- Particles Container -->
    <div class="particles" id="particlesContainer"></div>
   <!-- Hero Section -->
<section id="home" class="hero">
    <div class="container">
        <div class="profile-container">
           <img src="profilepic.png" alt="Nurul Hidayu Bt Suut" class="profile-pic">
        </div>
        <h1>Nurul Hidayu</h1>
        <h2>Multimedia Computing Student & UI/UX Designer</h2>
        <p>Third-year Bachelor of Multimedia Computing student at Universiti Malaysia Sarawak (UNIMAS), skilled in Java, Python, HTML/CSS, and UI/UX design. A motivated, fast-learning, and creative individual with strong teaamwork and communication skill.</p>
        <a href="#portfolio" class="btn">View My Work</a>
    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title fade-in">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text fade-in">
                    <h3>My Expertise</h3>
                    <p>A motivated, fast-learning, and creative individual with strong teamwork and communication skills. Seeking an internship opportunity to apply technical and design expertise in real-world projects at Sarawak Energy or within related technology fields.</p>
                    <p>Skilled in Java, Python, HTML/CSS, and UI/UX design with experience in various tools and technologies.</p>
                    <h3 style="margin-top: 30px;">Education</h3>
                    <div id="education-list">
                        <p><strong>Bachelor of Multimedia Computing (Hons)</strong><br>Universiti Malaysia Sarawak (UNIMAS)</p>
                        <p><strong>Foundation in Life Science (Pre-University)</strong><br>Universiti Malaysia Sarawak (UNIMAS)</p>
                    </div>
                    <button class="btn btn-outline" style="margin-top: 15px;" onclick="openAddEducationModal()">
                        <i class="fas fa-plus"></i> Add Education
                    </button>
                </div>
                <div class="skills fade-in">
                    <h3>My Skills</h3>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <h4>Java <span>90%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="90%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>Python <span>85%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="85%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>HTML/CSS <span>95%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="95%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>UI/UX Design <span>90%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="90%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>JavaScript <span>80%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="80%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>Figma <span>85%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="85%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Portfolio Section -->
    <section id="portfolio" class="portfolio">
        <div class="container">
            <div class="portfolio-header">
                <div class="section-title fade-in" style="margin-bottom: 0;">
                    <h2>My Portfolio</h2>
                </div>
                <button class="add-project-btn fade-in" onclick="openAddModal()">
                    <i class="fas fa-plus"></i>
                </button>
            </div>
            <div class="portfolio-grid" id="portfolioGrid">
                <!-- Project 1 -->
                <div class="portfolio-item fade-in">
                    <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Mental Health App" class="portfolio-img">
                    <div class="portfolio-content">
                        <h3>Mental Health Awareness Web App</h3>
                        <p>Developed a web app promoting mental health awareness through interactive quizzes and educational content.</p>
                        <div class="portfolio-actions">
                            <button class="btn btn-small" onclick="openProjectModal(0)">View Details</button>
                            <button class="btn btn-small btn-outline" onclick="openEditModal(0)">Edit</button>
                        </div>
                    </div>
                </div>
                <!-- Project 2 -->
                <div class="portfolio-item fade-in">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="ART Mobile App" class="portfolio-img">
                    <div class="portfolio-content">
                        <h3>ART Mobile App Prototype</h3>
                        <p>Created a high-fidelity mobile app prototype to support the Sarawak Metro ART system.</p>
                        <div class="portfolio-actions">
                            <button class="btn btn-small" onclick="openProjectModal(1)">View Details</button>
                            <button class="btn btn-small btn-outline" onclick="openEditModal(1)">Edit</button>
                        </div>
                    </div>
                </div>
                <!-- Project 3 -->
                <div class="portfolio-item fade-in">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Car Rental Website" class="portfolio-img">
                    <div class="portfolio-content">
                        <h3>Car Rental Management Website</h3>
                        <p>Built a functional car rental website "ZoomRentals" with booking, listing, and admin management features.</p>
                        <div class="portfolio-actions">
                            <button class="btn btn-small" onclick="openProjectModal(2)">View Details</button>
                            <button class="btn btn-small btn-outline" onclick="openEditModal(2)">Edit</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item fade-in">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Location</h3>
                            <p>Kuching, Sarawak, Malaysia</p>
                        </div>
                    </div>
                    <div class="contact-item fade-in">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Phone</h3>
                            <p>+60 193375235</p>
                        </div>
                    </div>
                    <div class="contact-item fade-in">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>nurulhidayu1111@gmail.com</p>
                        </div>
                    </div>
                </div>
                <div class="fade-in">
                    <h3>Send Me a Message</h3>
                    <form id="contactForm" style="margin-top: 20px;">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email" required>
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
          <div class="copyright">
                &copy; 2025 Nurul Hidayu. All Rights Reserved.
            </div>
        </div>
    </footer>
    <!-- Project Detail Modal -->
    <div id="projectModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeProjectModal()">&times;</span>
            <div class="modal-header">
                <h2 id="modalProjectTitle">Project Title</h2>
            </div>
            <div class="modal-body">
                <img id="modalProjectImage" src="" alt="Project Image" style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 5px; margin-bottom: 20px;">
                <p id="modalProjectDescription">Project description will appear here.</p>
                <div id="modalProjectDetails">
                    <!-- Additional project details will be inserted here -->
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-outline" onclick="closeProjectModal()">Close</button>
            </div>
        </div>
    </div>
    <!-- Edit Project Modal -->
    <div id="editModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeEditModal()">&times;</span>
            <div class="modal-header">
                <h2>Edit Project</h2>
            </div>
            <div class="modal-body">
                <form id="editProjectForm">
                    <div class="form-group">
                        <label for="editTitle">Project Title</label>
                        <input type="text" id="editTitle" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="editDescription">Project Description</label>
                        <textarea id="editDescription" class="form-control" required></textarea>
                    </div>
                    <div class="form-group">
                        <label for="editImage">Project Image URL</label>
                        <input type="text" id="editImage" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="editDetails">Project Details</label>
                        <textarea id="editDetails" class="form-control"></textarea>
                    </div>
                </form>
            </div>
            <div class="modal-footer">
                <button class="btn btn-outline" onclick="closeEditModal()">Cancel</button>
                <button class="btn" onclick="saveProjectChanges()">Save Changes</button>
            </div>
        </div>
    </div>
    <!-- Add Project Modal -->
    <div id="addModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeAddModal()">&times;</span>
            <div class="modal-header">
                <h2>Add New Project</h2>
            </div>
            <div class="modal-body">
                <form id="addProjectForm">
                    <div class="form-group">
                        <label for="addTitle">Project Title</label>
                        <input type="text" id="addTitle" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="addDescription">Project Description</label>
                        <textarea id="addDescription" class="form-control" required></textarea>
                    </div>
                    <div class="form-group">
                        <label for="addImage">Project Image URL</label>
                        <input type="text" id="addImage" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="addDetails">Project Details</label>
                        <textarea id="addDetails" class="form-control"></textarea>
                    </div>
                </form>
            </div>
            <div class="modal-footer">
                <button class="btn btn-outline" onclick="closeAddModal()">Cancel</button>
                <button class="btn" onclick="addNewProject()">Add Project</button>
            </div>
        </div>
    </div>
    <!-- Add Education Modal -->
    <div id="addEducationModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeAddEducationModal()">&times;</span>
            <div class="modal-header">
                <h2>Add Education</h2>
            </div>
            <div class="modal-body">
                <form id="addEducationForm">
                    <div class="form-group">
                        <label for="educationTitle">Degree/Program</label>
                        <input type="text" id="educationTitle" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="educationInstitution">Institution</label>
                        <input type="text" id="educationInstitution" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="educationYear">Year/Duration</label>
                        <input type="text" id="educationYear" class="form-control" placeholder="e.g., 2020-2023">
                    </div>
                </form>
            </div>
            <div class="modal-footer">
                <button class="btn btn-outline" onclick="closeAddEducationModal()">Cancel</button>
                <button class="btn" onclick="addNewEducation()">Add Education</button>
            </div>
        </div>
    </div>
<script>
        // Project data
        let projects = [
            {
                title: "Mental Health Awareness Web App",
                description: "Developed a web app promoting mental health awareness through interactive quizzes and educational content.",
                image: "https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                details: "<p><strong>Technologies:</strong> Java, HTML, CSS, MySQL</p><p>Designed user interfaces and managed backend operations using Java and MySQL.</p>"
            },
            {
                title: "ART Mobile App Prototype",
                description: "Created a high-fidelity mobile app prototype to support the Sarawak Metro ART system.",
                image: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                details: "<p><strong>Technologies:</strong> Figma (UI/UX Design)</p><p>Designed user flows and interfaces, applying feedback from usability testing to improve the design.</p>"
            },
            {
                title: "Car Rental Management Website",
                description: "Built a functional car rental website 'ZoomRentals' with booking, listing, and admin management features.",
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                details: "<p><strong>Technologies:</strong> HTML, PHP, MySQL</p><p>Implemented backend integration with MySQL for dynamic data handling.</p>"
            }
        ];
let currentProjectIndex = 0;
        let lastScrollY = window.scrollY;
        let ticking = false;
// Create particles
        function createParticles() {
            const container = document.getElementById('particlesContainer');
            const particleCount = 30;
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                // Random size
                const size = Math.random() * 5 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                // Random position
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100}%`;
                // Random animation
                const duration = Math.random() * 20 + 10;
                const delay = Math.random() * 5;
                particle.style.animation = `floatParticle ${duration}s infinite ${delay}s linear`;
                container.appendChild(particle);
            }
        }
// Particle animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes floatParticle {
                0% {
                    transform: translate(0, 0) rotate(0deg);
                    opacity: 0;
                }
                10% {
                    opacity: 0.5;
                }
                90% {
                    opacity: 0.5;
                }
                100% {
                    transform: translate(${Math.random() * 100 - 50}px, ${Math.random() * 100 - 50}px) rotate(360deg);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
// Scroll progress indicator
        function updateScrollProgress() {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById("scrollProgress").style.width = scrolled + "%";
        }// Header scroll effect
        function updateHeader() {
            const header = document.getElementById('mainHeader');
            const scrollY = window.scrollY;
            if (scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
            // Hide header on scroll down, show on scroll up
            if (scrollY > lastScrollY && scrollY > 200) {
                header.classList.add('hidden');
            } else {
                header.classList.remove('hidden');
            }
            lastScrollY = scrollY;
        }
// Scroll animation for elements
        function checkScroll() {
            const fadeElements = document.querySelectorAll('.fade-in');
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                if (elementTop < window.innerHeight - elementVisible) {
                    element.classList.add('appear');
                    // Animate skill bars
                    if (element.classList.contains('skills')) {
                        setTimeout(() => {
                            const skillBars = document.querySelectorAll('.skill-progress');
                            skillBars.forEach(bar => {
                                const width = bar.getAttribute('data-width');
                                bar.style.width = width;
                                bar.classList.add('animated');
                            });
                        }, 300);
                    }
                }
            });
        }
 // Open project detail modal
        function openProjectModal(index) {
            currentProjectIndex = index;
            const project = projects[index];
            document.getElementById('modalProjectTitle').textContent = project.title;
            document.getElementById('modalProjectImage').src = project.image;
            document.getElementById('modalProjectDescription').textContent = project.description;
            document.getElementById('modalProjectDetails').innerHTML = project.details;
            document.getElementById('projectModal').style.display = 'flex';
        }// Close project detail modal
        function closeProjectModal() {
            document.getElementById('projectModal').style.display = 'none';
        }
// Open edit project modal
        function openEditModal(index) {
            currentProjectIndex = index;
            const project = projects[index];
            document.getElementById('editTitle').value = project.title;
            document.getElementById('editDescription').value = project.description;
            document.getElementById('editImage').value = project.image;
            document.getElementById('editDetails').value = project.details.replace(/<[^>]*>/g, '');
            document.getElementById('editModal').style.display = 'flex';
        }
// Close edit project modal
        function closeEditModal() {
            document.getElementById('editModal').style.display = 'none';
        }
// Save project changes
        function saveProjectChanges() {
            projects[currentProjectIndex].title = document.getElementById('editTitle').value;
            projects[currentProjectIndex].description = document.getElementById('editDescription').value;
            projects[currentProjectIndex].image = document.getElementById('editImage').value;
            projects[currentProjectIndex].details = document.getElementById('editDetails').value;
            // Update the portfolio item
            updatePortfolioItem(currentProjectIndex);
            closeEditModal();
            // Show success animation
            const saveBtn = document.querySelector('#editModal .btn');
            const originalText = saveBtn.textContent;
            saveBtn.textContent = 'Saved!';
            saveBtn.style.backgroundColor = '#4CAF50';
            setTimeout(() => {
                saveBtn.textContent = originalText;
                saveBtn.style.backgroundColor = '';
            }, 1500);
        }
// Open add project modal
        function openAddModal() {
            document.getElementById('addTitle').value = '';
            document.getElementById('addDescription').value = '';
            document.getElementById('addImage').value = '';
            document.getElementById('addDetails').value = '';
            document.getElementById('addModal').style.display = 'flex';
        }
// Close add project modal
        function closeAddModal() {
            document.getElementById('addModal').style.display = 'none';
        }
// Add new project
        function addNewProject() {
            const newProject = {
                title: document.getElementById('addTitle').value,
                description: document.getElementById('addDescription').value,
                image: document.getElementById('addImage').value,
                details: document.getElementById('addDetails').value
            };
            projects.push(newProject);
            // Add the new project to the portfolio grid
            addPortfolioItem(newProject, projects.length - 1);
            closeAddModal();
            // Show success animation
            const addBtn = document.querySelector('#addModal .btn');
            const originalText = addBtn.textContent;
            addBtn.textContent = 'Added!';
            addBtn.style.backgroundColor = '#4CAF50';
            setTimeout(() => {
                addBtn.textContent = originalText;
                addBtn.style.backgroundColor = '';
            }, 1500);
        }
// Open add education modal
        function openAddEducationModal() {
            document.getElementById('educationTitle').value = '';
            document.getElementById('educationInstitution').value = '';
            document.getElementById('educationYear').value = '';
            document.getElementById('addEducationModal').style.display = 'flex';
        }
// Close add education modal
        function closeAddEducationModal() {
            document.getElementById('addEducationModal').style.display = 'none';
        }
// Add new education
        function addNewEducation() {
            const title = document.getElementById('educationTitle').value;
            const institution = document.getElementById('educationInstitution').value;
            const year = document.getElementById('educationYear').value;
            const educationItem = document.createElement('p');
            educationItem.innerHTML = `<strong>${title}</strong><br>${institution}${year ? ` (${year})` : ''}`;
            educationItem.classList.add('fade-in');
            document.getElementById('education-list').appendChild(educationItem);
            // Trigger animation
            setTimeout(() => {
                educationItem.classList.add('appear');
            }, 100);
            closeAddEducationModal();
            // Show success animation
            const addBtn = document.querySelector('#addEducationModal .btn');
            const originalText = addBtn.textContent;
            addBtn.textContent = 'Added!';
            addBtn.style.backgroundColor = '#4CAF50';
            setTimeout(() => {
                addBtn.textContent = originalText;
                addBtn.style.backgroundColor = '';
            }, 1500);
        }
// Update portfolio item in the grid
        function updatePortfolioItem(index) {
            const portfolioItems = document.querySelectorAll('.portfolio-item');
            const item = portfolioItems[index];
            const project = projects[index];
            item.querySelector('h3').textContent = project.title;
            item.querySelector('p').textContent = project.description;
            item.querySelector('img').src = project.image;
        }
// Add new portfolio item to the grid
        function addPortfolioItem(project, index) {
            const portfolioGrid = document.getElementById('portfolioGrid');
            const portfolioItem = document.createElement('div');
            portfolioItem.className = 'portfolio-item fade-in';
            portfolioItem.innerHTML = `
                <img src="${project.image}" alt="${project.title}" class="portfolio-img">
                <div class="portfolio-content">
                    <h3>${project.title}</h3>
                    <p>${project.description}</p>
                    <div class="portfolio-actions">
                        <button class="btn btn-small" onclick="openProjectModal(${index})">View Details</button>
                        <button class="btn btn-small btn-outline" onclick="openEditModal(${index})">Edit</button>
                    </div>
                </div>
            `;
            portfolioGrid.appendChild(portfolioItem);
            // Trigger animation
            setTimeout(() => {
                portfolioItem.classList.add('appear');
            }, 100);
        }
// Smooth scroll for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                if (targetSection) {
                    window.scrollTo({
                        top: targetSection.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
// Close modals when clicking outside
        window.onclick = function(event) {
            const projectModal = document.getElementById('projectModal');
            const editModal = document.getElementById('editModal');
            const addModal = document.getElementById('addModal');
            const addEducationModal = document.getElementById('addEducationModal');
            if (event.target === projectModal) {
                closeProjectModal();
            }
            if (event.target === editModal) {
                closeEditModal();
            }
            if (event.target === addModal) {
                closeAddModal();
            }
            if (event.target === addEducationModal) {
                closeAddEducationModal();
            }
        }
// Contact form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            // Add animation to the button
            const submitBtn = this.querySelector('.btn');
            const originalText = submitBtn.textContent;
            submitBtn.textContent = 'Sending...';
            submitBtn.disabled = true;
            // Simulate sending
            setTimeout(() => {
                submitBtn.textContent = 'Sent!';
                submitBtn.style.backgroundColor = '#4CAF50';
                setTimeout(() => {
                    submitBtn.textContent = originalText;
                    submitBtn.style.backgroundColor = '';
                    submitBtn.disabled = false;
                    this.reset();
                    alert('Thank you for your message! I will get back to you soon.');
                }, 1500);
            }, 1000);
        });
// Initialize on load
        window.addEventListener('load', function() {
            createParticles();
            checkScroll();
            // Animate elements on load
            const heroElements = document.querySelectorAll('.hero h1, .hero h2, .hero p, .hero .btn');
            heroElements.forEach((el, index) => {
                el.style.animationDelay = `${index * 0.2}s`;
            });
        });
// Scroll event listeners
        window.addEventListener('scroll', function() {
            updateScrollProgress();
            updateHeader();
            if (!ticking) {
                window.requestAnimationFrame(function() {
                    checkScroll();
                    ticking = false;
                });
                ticking = true;
            }
        });// Initial check for scroll animations
        checkScroll();
    </script>

