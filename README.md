<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurul Hidayu Bt Suut | UI/UX & Java Specialist</title>
    <!-- Use Inter font for modern, professional feel -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* ======================================================
         * 1. CSS Variables & Light Theme Setup
         * ======================================================
         */
        :root {
            /* Default Dark Theme Colors (kept for reference, but light mode will be default) */
            --bg-primary: #1A2A4F; 
            --bg-secondary: #452829; 
            --accent-color: #F7A5A5; 
            --highlight-color: #FFDBB6; 
            --text-color: #f0f0f0; 
            --text-secondary: #aaaaaa; 
            --border-color: rgba(255, 255, 255, 0.08); 
            --shadow-color: rgba(0, 0, 0, 0.3); 
        }
/* Light Mode Colors (Applied by default via JS initialization) */
        body.light-mode {
            --bg-primary: #ffffff; /* White background */
            --bg-secondary: #f7f7f7; /* Very light gray for cards/sections */
            --accent-color: #E91E63; /* Pink/Rose for primary highlight */
            --highlight-color: #FF9800; /* Orange/Amber for secondary highlight */
            --text-color: #212529; /* Dark text */
            --text-secondary: #6c757d; /* Muted gray text */
            --border-color: #e0e0e0;
            --shadow-color: rgba(0, 0, 0, 0.1);
        }
/* ======================================================
         * 2. Base & Utility Styles
         * ======================================================
         */
         html {
            scroll-behavior: smooth;
        }
body {
            font-family: 'Inter', sans-serif;
            /* Default styles will be overridden by .light-mode class initially */
            background-color: var(--bg-primary);
            color: var(--text-color);
            transition: background-color 0.5s, color 0.5s;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s;
        }
a:hover, a:focus {
            color: var(--highlight-color); 
            outline: 2px solid var(--highlight-color);
            outline-offset: 3px;
            border-radius: 4px;
        }
    button:focus-visible, a:focus-visible, input:focus-visible, textarea:focus-visible {
            outline: 2px solid var(--highlight-color);
            outline-offset: 3px;
        }
.container {
            max-width: 1200px; 
            margin: 0 auto;
            padding: 0 1.5rem;
        }
.section {
            padding: 5rem 0; 
            border-bottom: 1px solid var(--border-color);
        }
.section-title {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
            font-weight: 800;
            color: var(--text-color);
            text-align: center;
        }
        .section-subtitle {
            font-size: 1.1rem;
            margin-bottom: 3rem;
            font-weight: 500;
            color: var(--accent-color);
            text-align: center;
            text-transform: uppercase;
        }
/* ======================================================
         * 3. Header & Navigation Styles
         * ======================================================
         */
        .header {
            background-color: var(--bg-primary);
            box-shadow: 0 2px 10px var(--shadow-color);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
.nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: 900;
            color: var(--highlight-color);
            border: 2px solid var(--accent-color);
            padding: 0.2rem 0.5rem;
            border-radius: 5px;
        }

.nav-list {
            list-style: none;
            display: flex;
            gap: 2rem;
            padding: 0;
            margin: 0;
        }
.nav-link {
            font-weight: 600;
            padding: 0.5rem 0;
            color: var(--text-secondary);
            font-size: 0.95rem;
            transition: color 0.3s;
            text-transform: uppercase;
        }
        
.nav-link:hover {
            color: var(--accent-color);
            text-decoration: none;
            outline: none;
        }
        
.theme-toggle {
            cursor: pointer;
            font-size: 1.4rem;
            background: none;
            border: none;
            color: var(--text-color);
            transition: transform 0.2s, color 0.3s;
        }

/* ======================================================
         * 4. Home (Hero) Section Styles
         * ======================================================
         */
        #home {
            padding: 8rem 0 6rem 0;
            text-align: center;
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        .hero-title {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            font-weight: 900;
            line-height: 1.2;
        }
        .hero-title span {
            color: var(--accent-color);
        }
.hero-subtitle {
            font-size: 1.8rem;
            margin-bottom: 3.5rem;
            font-weight: 700;
            color: var(--highlight-color); 
        }
        .profile-img-container {
            width: 250px;
            height: 250px;
            margin: 0 auto 3rem auto;
            border-radius: 50%;
            overflow: hidden;
            border: 5px solid var(--accent-color);
            box-shadow: 0 0 0 10px rgba(0, 0, 0, 0.05); /* Lighter shadow for light mode */
            /* Added a subtle internal glow/shadow for depth */
            box-shadow: 0 0 20px rgba(233, 30, 99, 0.3); /* Accent shadow */
        }
        /* Styling for the actual image */
        .profile-img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }
 .social-links {
            margin-top: 2rem;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }
.social-links a {
            font-size: 1.5rem;
            color: var(--text-secondary);
            transition: color 0.3s, border-color 0.3s, background-color 0.3s;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            border: 1px solid var(--border-color);
        }
.social-links a:hover {
            color: var(--bg-primary); /* Light text on hover */
            background-color: var(--highlight-color); /* Highlight background */
            border-color: var(--highlight-color);
            outline: none;
        }
 /* ======================================================
         * 5. What Can I Do (Services)
         * ======================================================
         */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }
.service-card {
            background-color: var(--bg-secondary);
            padding: 2.5rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px var(--shadow-color);
            border: 1px solid var(--border-color);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(233, 30, 99, 0.2); /* Accent shadow on hover */
        }

.service-icon {
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }
.service-card h3 {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
.service-card p {
            color: var(--text-secondary);
        }
        
/* ======================================================
         * 6. Skills Section (Restructured per image)
         * ======================================================
         */
        #skills {
            position: relative;
        }
        
.skills-content {
            display: flex;
            gap: 4rem;
            align-items: flex-start; /* Align top, not center */
        }

.skills-section-left {
            flex: 1;
        }
        .skills-section-right {
            flex: 1;
        }
        
/* --- Skills That Standout (Tags) - Updated with image styles --- */
        .skills-standout-wrapper {
            background-color: var(--bg-secondary); /* Use secondary background */
            padding: 2.5rem;
            border-radius: 10px;
            display: flex;
            gap: 2rem;
            align-items: center;
            margin-bottom: 3rem;
            box-shadow: 0 4px 15px var(--shadow-color);
        }
        
.skills-tags-container {
            flex: 1;
        }
        
.skills-tags-container h3 {
            font-size: 1.5rem;
            color: var(--highlight-color);
            margin-bottom: 1rem;
        }
        
.skills-tags-container p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
        }
        
.skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
        }
        
.skill-tag {
            background-color: var(--bg-primary); /* White/Light background for tags */
            color: var(--text-color);
            padding: 0.6rem 1.2rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            border: 1px solid var(--accent-color);
            transition: background-color 0.3s, color 0.3s;
        }

.skill-tag:hover {
            background-color: var(--accent-color);
            color: var(--bg-primary); /* White text on light accent */
        }
        
.skills-image {
            flex-shrink: 0;
            width: 200px; /* Adjust size for small illustrative image */
            height: 200px;
            border-radius: 10px; /* Keep it square/rectangular per image source */
            overflow: hidden;
            border: 4px solid var(--highlight-color);
            box-shadow: 0 0 15px rgba(255, 152, 0, 0.5); /* Orange shadow */
        }
        
.skills-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }
        
/* --- My Expertise in Tools (Grid Cards) --- */
        .skills-card-grid {
            display: grid;
            /* On desktop, show 3 columns. Will adjust for responsiveness below. */
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); 
            gap: 1.5rem;
            padding: 1rem 0;
        }

.skill-square-card {
            background-color: var(--bg-primary);
            padding: 1.5rem 1rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px var(--shadow-color);
            border: 1px solid var(--border-color);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            height: 200px; /* Make it a square card */
        }
.skill-square-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(233, 30, 99, 0.2); /* Accent shadow on hover */
        }
.card-icon-logo {
            font-size: 2.5rem;
            color: var(--highlight-color); /* Highlight color for the logo */
            margin-bottom: 0.5rem;
            padding: 0.5rem;
            background-color: rgba(0, 0, 0, 0.05); /* Subtle background for the icon */
            border-radius: 8px;
        }
.card-title {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--text-secondary);
            text-transform: uppercase;
            margin-bottom: 0.5rem;
            line-height: 1.2;
        }

.card-percentage {
            font-size: 2rem;
            font-weight: 800;
            color: var(--accent-color);
            line-height: 1;
        }
/* ======================================================
         * 7. Latest Projects Section
         * ======================================================
         */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
        }
		.project-card-full {
            background-color: var(--bg-secondary);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 20px var(--shadow-color);
            transition: transform 0.3s;
        }
.project-card-full:hover {
            transform: translateY(-5px);
        }

.project-image-placeholder {
            height: 200px;
            background-color: var(--bg-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            font-weight: 700;
            color: var(--text-secondary);
            border-bottom: 1px solid var(--border-color);
        }

.project-details {
            padding: 1.5rem;
        }

.project-details h3 {
            font-size: 1.5rem;
            font-weight: 800;
            margin-top: 0;
            margin-bottom: 0.5rem;
        }

.project-details p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }
        
.project-details .tech-label {
            display: inline-block;
            color: var(--highlight-color);
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }
        /* ======================================================
         * 8. Contact Section (Form)
         * ======================================================
         */
        .contact-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 3rem;
        }
.contact-form label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--text-color);
        }

.contact-form input, .contact-form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1.5rem;
            border: 1px solid var(--border-color);
            background-color: var(--bg-secondary);
            color: var(--text-color);
            border-radius: 5px;
        }
.contact-form textarea {
            min-height: 120px;
            resize: vertical;
        }
.submit-btn {
            background-color: var(--accent-color);
            color: var(--bg-primary); /* Use a dark text color for better contrast on the light accent button */
            padding: 1rem 2rem;
            border: none;
            border-radius: 5px;
            font-weight: 700;
            cursor: pointer;
            transition: background-color 0.3s;
            text-transform: uppercase;
        }
.submit-btn:hover {
            background-color: #D31959; /* Slightly darker accent */
        }

#form-message {
            margin-top: 1rem;
            padding: 0.75rem;
            background-color: var(--highlight-color);
            color: var(--bg-primary);
            border-radius: 5px;
            font-weight: 600;
            display: none;
        }
        .contact-info-block {
            background-color: var(--bg-secondary);
            padding: 2rem;
            border-radius: 10px;
        }
.contact-info-block h3 {
            color: var(--accent-color);
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

.contact-info-block p {
            margin-bottom: 1.5rem;
        }
         .contact-info-block ul {
            list-style: none;
            padding: 0;
        }
        .contact-info-block li {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        .contact-info-block i {
            color: var(--highlight-color);
        }
/* ======================================================
         * 9. Footer & Responsiveness
         * ======================================================
         */
        .footer {
            text-align: center;
            padding: 3rem 0;
            font-size: 0.9rem;
            color: var(--text-secondary);
            background-color: var(--bg-primary);
        }
/* Media Queries for Responsiveness */
        @media (max-width: 900px) {
            .skills-content {
                flex-direction: column;
            }
            .skills-section-left, .skills-section-right {
                width: 100%;
            }
            .contact-grid {
                grid-template-columns: 1fr;
            }
            /* Adjust the skills standout wrapper for vertical layout */
            .skills-standout-wrapper {
                flex-direction: column;
                padding: 2rem;
            }
            .skills-image {
                width: 150px; 
                height: 150px;
                order: -1; /* Move image above text on mobile */
            }
        }
        @media (max-width: 600px) {
            .nav-list {
                display: none; /* Hide for mobile to keep clean, can add hamburger menu if needed */
            }
            .nav {
                justify-content: space-between;
            }
            .hero-title { font-size: 2.5rem; }
            .hero-subtitle { font-size: 1.4rem; }
            .section { padding: 3rem 0; }
            .projects-grid {
                grid-template-columns: 1fr;
            }
             /* Ensure skills grid wraps nicely on small mobile */
            .skills-card-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body class="light-mode">
<!-- ====================================================== -->
    <!-- PRIMARY NAVIGATION (Sticky Header) -->
    <!-- ====================================================== -->
    <header class="header">
        <div class="container nav">
            <!-- Branding: Changed from PROFILY to initials 'NH' -->
            <div class="logo">NH</div>
            <ul class="nav-list">
                <li><a href="#home" class="nav-link">Home</a></li>
                <li><a href="#services" class="nav-link">Services</a></li>
                <li><a href="#skills" class="nav-link">Skills</a></li>
                <li><a href="#projects" class="nav-link">Projects</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
            <button id="theme-toggle" class="theme-toggle" aria-label="Toggle light and dark theme">
                <span id="theme-icon">🌙</span> 
            </button>
        </div>
    </header>
<main>
        <!-- ====================================================== -->
        <!-- SECTION: HOME (HERO) -->
        <!-- Profile image updated to use the first uploaded file -->
        <!-- ====================================================== -->
        <section id="home" class="section">
            <div class="container">
                <div class="profile-img-container" aria-label="Nurul Hidayu Profile">
                    <!-- USING FIRST UPLOADED IMAGE: Screenshot 2025-11-27 221045.png -->
                    <img src="uploaded:Screenshot 2025-11-27 221045.png-cb963e16-5541-41bd-be1b-a77dfd01dfcf" 
                         alt="Profile photo of Nurul Hidayu"
                         onerror="this.onerror=null; this.src='https://placehold.co/250x250/f0f0f0/E91E63?text=NH';" />
                </div>
                <h1 class="hero-title">I'm <span>Nurul Hidayu</span>.</h1>
                <p class="hero-subtitle">Multimedia Computing Student | UI/UX & Java Specialist</p>
                <div class="social-links">
                    <a href="https://linkedin.com/in/nurul-hidayu" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                    <a href="https://github.com/nurulhidayu" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                    <a href="mailto:nurulhidayu1111@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
                </div>
            </div>
        </section>
        <!-- ====================================================== -->
        <!-- SECTION: WHAT CAN I DO (SERVICES) -->
        <!-- ====================================================== -->
        <section id="services" class="section" style="background-color: var(--bg-secondary);">
            <div class="container">
                <h2 class="section-title">What Can I Do</h2>
                <p class="section-subtitle">My Core Expertise Areas</p>
                <div class="services-grid">
                    
<div class="service-card">
                        <div class="service-icon"><i class="fas fa-palette"></i></div>
                        <h3>UI/UX Design & Prototyping</h3>
                        <p>High-fidelity mobile and web prototyping using Figma, focused on intuitive Human-Computer Interaction (HCI) principles and usability testing.</p>
                    </div>
<div class="service-card">
                        <div class="service-icon"><i class="fas fa-laptop-code"></i></div>
                        <h3>Java & Full-Stack Development</h3>
                        <p>Developing robust backend logic with Java (OOP, C/C++) and building full-stack web applications using HTML, CSS, JavaScript, and integrating with MySQL databases.</p>
                    </div>
 <div class="service-card">
                        <div class="service-icon"><i class="fas fa-database"></i></div>
                        <h3>Database & System Analysis</h3>
                        <p>Designing, implementing, and querying relational databases (MySQL) and applying System Analysis and Project Management principles to software delivery.</p>
                    </div>
                </div>
            </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: SKILLS (Restructured) -->
        <!-- Skills That Standout section is updated with image and dedicated wrapper for a richer look -->
        <!-- ====================================================== -->
        <section id="skills" class="section">
            <div class="container">
                <h2 class="section-title">My Capabilities</h2>
                <p class="section-subtitle">A Deep Dive into My Expertise</p>
<!-- NEW SKILLS STANDOUT WRAPPER (Per the second image/design guidance) -->
                <div class="skills-standout-wrapper">
                    <div class="skills-tags-container">
                        <h3>Skills That Standout</h3>
                        <p>My domain expertise and soft skills are the foundation for successful project execution and teamwork.</p>
                        <div class="skill-tags">
                            <!-- Domain Expertise (from Related Courses in Resume) -->
                            <span class="skill-tag">UI/UX Design</span>
                            <span class="skill-tag">HCI Principles</span>
                            <span class="skill-tag">System Analysis</span>
                            <span class="skill-tag">Project Management</span>
                            <span class="skill-tag">Database Concept & Design</span>
                            <span class="skill-tag">Mobile App Dev</span>
                            <!-- Soft Skills -->
                            <span class="skill-tag">Teamwork</span>
                            <span class="skill-tag">Communication</span>
                            <span class="skill-tag">Problem Solving</span>
                            <span class="skill-tag">Fast Learning</span>
                            <span class="skill-tag">Leadership</span>
                        </div>
                    </div>
                    <!-- USING SECOND UPLOADED IMAGE: Screenshot 2025-11-27 221144.png -->
                    <div class="skills-image" aria-label="Skills highlight visual">
                        <img src="uploaded:Screenshot 2025-11-27 221144.png-b65c7f53-a512-4dce-ba0e-2ace03b12106" 
                             alt="Stylized visual representing UI/UX design skills"
                             onerror="this.onerror=null; this.src='https://placehold.co/200x200/FF9800/212529?text=Skills+Visual';" />
                    </div>
                </div>
				<!-- END NEW SKILLS STANDOUT WRAPPER -->
<!-- MY EXPERTISE IN TOOLS -->
                <div class="skills-content" style="gap: 0; flex-direction: column;">
                    <div class="skills-section-right" style="width: 100%;">
                        <h3 class="section-title" style="text-align: center; margin-top: 0; color: var(--accent-color);">My Expertise in Tools</h3>
                        <p style="color: var(--text-secondary); margin-bottom: 2rem; text-align: center;">Proficiency in key programming languages and design software.</p>
                        <div class="skills-card-grid">
                            <!-- Card 1: Java & C/C++ -->
                            <div class="skill-square-card">
                                <div class="card-icon-logo"><i class="fab fa-java"></i></div>
                                <div class="card-title">Java & C/C++</div>
                                <div class="card-percentage">85%</div>
                            </div>
<!-- Card 2: Figma -->
                            <div class="skill-square-card">
                                <div class="card-icon-logo"><i class="fab fa-figma"></i></div>
                                <div class="card-title">Figma</div>
                                <div class="card-percentage">90%</div>
                            </div>
<!-- Card 3: Web Dev -->
                            <div class="skill-square-card">
                                <div class="card-icon-logo"><i class="fas fa-code"></i></div>
                                <div class="card-title">Web Dev</div>
                                <div class="card-percentage">80%</div>
                            </div>
<!-- Card 4: MySQL -->
                            <div class="skill-square-card">
                                <div class="card-icon-logo"><i class="fas fa-database"></i></div>
                                <div class="card-title">MySQL</div>
                                <div class="card-percentage">75%</div>
                            </div>
                             <!-- Card 5: Python & Kotlin -->
                            <div class="skill-square-card">
                                <div class="card-icon-logo"><i class="fab fa-python"></i></div>
                                <div class="card-title">Python/Kotlin</div>
                                <div class="card-percentage">65%</div>
                            </div>
                            </div>
                    </div>
                </div>
            </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: LATEST PROJECTS -->
        <!-- ====================================================== -->
        <section id="projects" class="section" style="background-color: var(--bg-secondary);">
            <div class="container">
                <h2 class="section-title">My Latest Projects</h2>
                <p class="section-subtitle">Real-world Application of Technical Skills</p>
        <div class="projects-grid">
                    <div class="project-card-full">
                        <div class="project-image-placeholder">UI/UX Prototype Wireframe Example</div>
                        <div class="project-details">
                            <div class="tech-label">Figma, UI/UX Design</div>
                            <h3>ART Mobile App Prototype (Sarawak Metro)</h3>
                            <p>Created a high-fidelity mobile application prototype to support the Sarawak Metro ART system. Designed user flows and interfaces, applying feedback from usability testing to improve the design.</p>
                            <a href="#projects" style="font-size: 0.9rem;">View Case Study <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
<div class="project-card-full">
                        <div class="project-image-placeholder">Web Application Backend Interface Mock</div>
                        <div class="project-details">
                            <div class="tech-label">Java, HTML, CSS, MySQL</div>
                            <h3>Mental Health Awareness Web App</h3>
                            <p>Designed and built a functional web application with Java and MySQL, offering educational content and interactive self-assessment quizzes for mental well-being.</p>
                            <a href="#projects" style="font-size: 0.9rem;">View Repository <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
                    <div class="project-card-full">
                        <div class="project-image-placeholder">Web Application Interface Mock</div>
                        <div class="project-details">
                            <div class="tech-label">HTML, PHP, MySQL</div>
                            <h3>Car Rental Management Website (ZoomRentals)</h3>
                            <p>Built a functional car rental website with booking, listing, and admin management features. Implemented backend integration with MySQL for dynamic data handling and inventory management.</p>
                            <a href="#projects" style="font-size: 0.9rem;">View Project Details <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
                    </div>
            </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: CONTACT -->
        <!-- ====================================================== -->
        <section id="contact" class="section">
            <div class="container">
                <h2 class="section-title">Get In Touch With Me</h2>
                <p class="section-subtitle">Let's Discuss Internship Opportunities!</p>
                <div class="contact-grid">
                    <form class="contact-form" onsubmit="handleFormSubmit(event)">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" name="name" required placeholder="Enter your name">

<label for="email">Your Email</label>
                        <input type="email" id="email" name="email" required placeholder="Enter your email">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required placeholder="What's this about?">
						<label for="message">Your Message</label>
                        <textarea id="message" name="message" required placeholder="Type your message here..."></textarea>
                        <button type="submit" class="submit-btn">Send Message</button>
                        <div id="form-message"></div>
                    </form>
                    <div class="contact-info-block">
                        <h3>Contact Info</h3>
                        <p style="color: var(--text-secondary);">I am available for internship interviews and eager to join a dynamic team in Sarawak.</p>
                        <ul>
                            <li><i class="fas fa-map-marker-alt"></i> Kuching, Sarawak, Malaysia</li>
                            <li><i class="fas fa-phone"></i> +60 193375235</li>
                            <li><i class="fas fa-envelope"></i> nurulhidayu1111@gmail.com</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </main>
	<!-- ====================================================== -->
    <!-- FOOTER -->
    <!-- ====================================================== -->
    <footer class="footer">
        <div class="container">
            <!-- Branding: Removed PROFILY -->
            <p style="margin-top: 1rem;">Multimedia Computing Student at UNIMAS.</p>
            <p>&copy; 2024 Nurul Hidayu Bt Suut. All rights reserved.</p>
        </div>
    </footer>
	<!-- ====================================================== -->
    <!-- JAVASCRIPT LOGIC -->
    <!-- Focus: Theme management and form submission -->
    <!-- ====================================================== -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const body = document.body;
            const themeToggleBtn = document.getElementById('theme-toggle');
            const themeIcon = document.getElementById('theme-icon');
            const THEME_KEY = 'theme-nh-dark-v2'; 

            // --- Theme Toggle Logic ---

// Set the default theme state to light mode
            body.classList.add('light-mode');
            body.classList.remove('dark-mode');
            themeIcon.textContent = '🌙'; 

/**
             * Sets the application theme and updates localStorage and the toggle icon.
             * @param {boolean} isDarkMode - True for dark mode, false for light mode.
             */
            function setTheme(isDarkMode) {
                if (isDarkMode) {
                    body.classList.add('dark-mode');
                    body.classList.remove('light-mode');
                    localStorage.setItem(THEME_KEY, 'dark');
                    themeIcon.textContent = '☀️'; // Sun icon for dark mode
                } else {
                    body.classList.add('light-mode');
                    body.classList.remove('dark-mode');
                    localStorage.setItem(THEME_KEY, 'light');
                    themeIcon.textContent = '🌙'; // Moon icon for light mode
                }
            }
// Initialization: Check and apply saved theme, defaulting to light mode
            function initializeTheme() {
                const savedTheme = localStorage.getItem(THEME_KEY);
                
// If saved, use it. Otherwise, default to light mode
                if (savedTheme === 'dark') {
                    setTheme(true);
                } else {
                    setTheme(false); // Default to light mode
                }
            }

// Event Listener for the button click
            if (themeToggleBtn) {
                themeToggleBtn.addEventListener('click', () => {
                    const isCurrentlyDark = body.classList.contains('dark-mode');
                    setTheme(!isCurrentlyDark);
                });
            }
 initializeTheme();
        });

// --- Form Submission Logic (Replaces forbidden alert()) ---
        function handleFormSubmit(event) {
            event.preventDefault(); // Prevent actual form submission
			const formMessage = document.getElementById('form-message');
            const form = event.target;
            
// Display message to the user
            formMessage.textContent = 'Thank you for your message! I will reply shortly.';
            formMessage.style.display = 'block';

// Log form data (in a real app, this would be a fetch() call)
            const formData = new FormData(form);
            const data = Object.fromEntries(formData.entries());
            console.log('Form Submitted (Data Logged):', data);

// Reset form and hide message after a delay
            setTimeout(() => {
                form.reset();
                formMessage.style.display = 'none';
            }, 3000);
        }
    </script>
</body>
</html>
