
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurul Hidayu Bt Suut | Multimedia Computing Specialist</title>
    <!-- Use Inter font for modern, professional feel -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons (used in contact, skills, and theme toggle) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* * ======================================================
         * 1. CSS Variables & Theming Setup
         * ======================================================
         */
        :root {
            /* Light Mode Theme - Vibrant Pink Accent */
            --primary-color: #E91E63; /* Main Pink */
            --secondary-color: #fce4ec; /* Lightest Pink for alternating sections */
            --text-color: #212529; /* Dark Gray/Black for body text */
            --background-color: #ffffff;
            --card-color: #ffffff;
            --border-color: #f8bbd0; /* Soft border color */
            --shadow-color: rgba(233, 30, 99, 0.15); /* Pink shadow */
        }
        
  /* Dark Mode Override when 'dark-mode' class is applied to body */
        body.dark-mode {
            --primary-color: #ff80ab;
            --text-color: #f0f0f0;
            --background-color: #1a1a1a;
            --card-color: #2a2a2a;
            --secondary-color: #2a2a2a; 
            --border-color: #3c3c3c;
            --shadow-color: rgba(255, 255, 255, 0.05);
        }
/* * ======================================================
         * 2. Base & Utility Styles
         * ======================================================
         */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
body {
            font-family: 'Inter', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            transition: background-color 0.5s, color 0.5s;
            line-height: 1.6;
        }
a {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.3s;
        }
a:hover, a:focus {
            color: var(--primary-color); 
            text-decoration: underline;
            outline: 2px solid var(--primary-color);
            outline-offset: 3px;
            border-radius: 4px;
        }
        /* Focus state for accessibility */
        button:focus-visible, a:focus-visible, input:focus-visible, textarea:focus-visible {
            outline: 2px solid var(--primary-color);
            outline-offset: 3px;
        }
.container {
            max-width: 1100px; 
            margin: 0 auto;
            padding: 0 1.5rem;
        }
.section {
            padding: 7rem 0; 
            border-bottom: 1px solid var(--border-color);
            background-color: var(--background-color);
        }
        /* Apply secondary background to alternating sections */
        #home, #experience, #contact {
            background-color: var(--secondary-color);
        }
        .section:last-of-type {
            border-bottom: none;
        }

.section-title {
            font-size: 2.8rem;
            margin-bottom: 4rem;
            font-weight: 900;
            color: var(--primary-color); 
            text-align: center;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        /* * ======================================================
         * 3. Header & Navigation Styles
         * ======================================================
         */
        .header {
            background-color: var(--card-color);
            box-shadow: 0 1px 6px var(--shadow-color);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
.nav {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 65px;
            position: relative;
        }

  .nav-list {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

  .nav-link {
            font-weight: 700;
            padding: 0.5rem 0;
            color: var(--text-color);
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: color 0.3s;
        }
        
  .theme-toggle {
            position: absolute;
            right: 1.5rem;
            cursor: pointer;
            font-size: 1.4rem;
            background: none;
            border: none;
            color: var(--text-color);
            transition: transform 0.2s, color 0.3s;
        }
        /* * ======================================================
         * 4. Home (Hero) Section Styles
         * ======================================================
         */
        #home {
            padding: 10rem 0 12rem 0;
            text-align: center;
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        .profile-visual {
            width: 160px;
            height: 160px;
            border-radius: 50%;
            background-color: var(--primary-color);
            margin: 0 auto 2.5rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            font-weight: 900;
            color: white;
            box-shadow: 0 10px 30px var(--shadow-color);
        }
.hero-title {
            font-size: 5.5rem;
            margin-bottom: 0.5rem;
            font-weight: 900;
            line-height: 1;
        }
        .hero-title span {
            color: var(--primary-color);
        }
.hero-subtitle {
            font-size: 1.7rem;
            margin-bottom: 3.5rem;
            font-weight: 500;
            color: #6c757d; 
        }
        .hero-cta {
            background-color: var(--primary-color); 
            color: white; 
            padding: 1rem 3.5rem;
            border-radius: 50px; 
            font-weight: 700;
            transition: background-color 0.3s, transform 0.1s;
            box-shadow: 0 4px 15px rgba(233, 30, 99, 0.4);
            display: inline-block;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        .hero-cta:hover {
             background-color: #C2185B; 
             transform: translateY(-2px);
        }

  /* * ======================================================
         * 5. Section Specific Styles
         * ======================================================
         */
         /* About Section */
        #about p {
            max-width: 800px;
            margin: 0 auto 1.5rem auto;
            text-align: center;
            font-size: 1.15rem;
            color: #495057; 
        }

  /* Experience Section (Timeline/List structure) */
        .experience-entry {
            margin-bottom: 3.5rem;
            padding-bottom: 2.5rem;
            border-bottom: 1px solid var(--border-color);
            display: grid;
            grid-template-columns: 200px 1fr; 
            gap: 3rem;
            align-items: flex-start;
        }
        
  .experience-entry:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

  .entry-date {
            font-size: 1rem;
            font-weight: 700;
            color: var(--primary-color);
            white-space: nowrap; 
            padding-top: 0.25rem;
            text-align: right; 
        }
        
  .entry-details {
             border-left: 3px solid var(--primary-color);
             padding-left: 2rem;
        }

  .entry-title {
            font-size: 1.6rem;
            font-weight: 800;
            margin-bottom: 0.25rem;
        }
        
  .entry-company {
            font-size: 1.1rem;
            font-weight: 500;
            color: #6c757d;
            margin-bottom: 1rem;
        }

  .entry-description ul {
            list-style: none;
            padding-left: 0;
            margin-top: 0.5rem;
            font-size: 1rem;
        }
        
  .entry-description li {
            position: relative;
            margin-bottom: 0.7rem;
            padding-left: 1.5rem;
        }
        
  .entry-description li::before {
            content: '•';
            position: absolute;
            left: 0;
            top: 0;
            font-weight: 900;
            color: var(--primary-color);
        }

  /* Projects Section (Grid Layout) */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
            gap: 2.5rem;
            max-width: 100%;
            margin: 0 auto;
        }

  .project-card {
            background-color: var(--card-color);
            padding: 2.5rem;
            border-radius: 10px;
            box-shadow: 0 8px 20px var(--shadow-color);
            border: 1px solid var(--border-color);
            transition: box-shadow 0.3s, transform 0.3s;
        }

  .project-card:hover {
            box-shadow: 0 15px 30px var(--shadow-color);
            transform: translateY(-8px);
        }
        
  .tech-stack-label {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            font-size: 0.75rem;
            font-weight: 700;
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

  .project-card h3 {
            font-size: 1.8rem;
            margin-bottom: 0.6rem;
            color: var(--text-color);
            font-weight: 800;
        }

  .project-card p {
            margin-bottom: 1.5rem;
            color: #495057;
        }
        
   /* Skills & Courses Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            text-align: center;
        }

  .skill-group h4 {
            font-size: 1.4rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
            font-weight: 700;
        }

  .skill-list {
            list-style: none;
            padding: 0;
            line-height: 2;
        }

  #key-courses {
            padding-top: 4rem;
        }

  .course-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-top: 3rem;
        }

  .course-list li {
            background-color: var(--primary-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

 /* Contact Section */
        .contact-info-container {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }
        .contact-list {
            list-style: none;
            padding: 0;
            margin-top: 3rem;
        }
        
  .contact-list li {
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
        }
        
  .contact-icon {
            color: var(--primary-color);
            font-size: 1.8rem;
        }
        
  .references-note {
            margin-top: 3rem;
            font-style: italic;
            color: #6c757d;
        }

  /* * ======================================================
         * 6. Footer & Responsiveness
         * ======================================================
         */
        .footer {
            text-align: center;
            padding: 3rem 0;
            font-size: 0.9rem;
            color: #6c757d;
            background-color: var(--background-color);
        }

  /* Media Queries for Responsiveness */
        @media (max-width: 767px) {
            .hero-title { font-size: 3rem; }
            .hero-subtitle { font-size: 1.2rem; }
            .section { padding: 4rem 0; }
            
  .experience-entry {
                 grid-template-columns: 1fr; /* Stack on mobile */
            }
            .entry-date { margin-bottom: 1rem; text-align: left; }
            .entry-details { border-left: none; padding-left: 0; }
            
  .skills-grid, .projects-grid { grid-template-columns: 1fr; }
            .nav-list { gap: 1rem; }
            .theme-toggle { right: 0.5rem; }
            .nav { height: auto; padding: 1rem 0; }
            .course-list li { font-size: 0.85rem; padding: 0.6rem 1rem; }
            .skills-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
<!-- ====================================================== -->
    <!-- PRIMARY NAVIGATION (Sticky Header) -->
    <!-- ====================================================== -->
    <header class="header">
        <div class="container">
            <nav class="nav">
                <ul class="nav-list">
                    <li><a href="#home" class="nav-link smooth-scroll">Home</a></li>
                    <li><a href="#about" class="nav-link smooth-scroll">About</a></li>
                    <li><a href="#projects" class="nav-link smooth-scroll">Projects</a></li>
                    <li><a href="#experience" class="nav-link smooth-scroll">Experience</a></li>
                    <li><a href="#skills" class="nav-link smooth-scroll">Skills</a></li>
                    <li><a href="#contact" class="nav-link smooth-scroll">Contact</a></li>
                </ul>
                <button id="theme-toggle" class="theme-toggle" aria-label="Toggle dark and light theme">
                    <span id="theme-icon">🌙</span>
                </button>
            </nav>
        </div>
    </header>
<main>
        <!-- ====================================================== -->
        <!-- SECTION: HOME (HERO) -->
        <!-- Focus: Identity & Main Pitch -->
        <!-- ====================================================== -->
        <section id="home" class="section">
            <div class="container">
                <div class="profile-visual" aria-label="Profile Photo Placeholder">
                    NH
                </div>
                <h1 class="hero-title">I'm <span>Nurul Hidayu</span>.</h1>
                <p class="hero-subtitle">Multimedia Computing Student | UI/UX & Java Specialist </p>
                <a href="#projects" class="hero-cta smooth-scroll">View Portfolio</a>
            </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: ABOUT (CAREER PROFILE) -->
        <!-- Focus: Summary of Strengths & Goals -->
        <!-- ====================================================== -->
        <section id="about" class="section">
            <div class="container">
                <h2 class="section-title">Career Profile</h2>
                <p>I am a third-year student at UNIMAS, driven to bridge design and functionality. My academic focus on Human-Computer Interaction (HCI) and UI/UX Design (Figma) complements a solid foundation in core development languages like Java and Python.</p>
            </div>
        </section>
      <!-- ====================================================== -->
        <!-- SECTION: PROJECTS (TECHNICAL SHOWCASE) -->
        <!-- Focus: Hard Skills & Deliverables -->
        <!-- ====================================================== -->
        <section id="projects" class="section">
            <div class="container">
                <h2 class="section-title">Key Technical Projects</h2>
                <div class="projects-grid">
                    <!-- Project 1: ART Mobile App Prototype -->
                    <div class="project-card">
                        <span class="tech-stack-label">UI/UX & Mobile Design</span>
                        <h3>ART Mobile App Prototype (Sarawak Metro)</h3>
                        <p>Developed a high-fidelity mobile application prototype for the Autonomous Rapid Transit (ART) system in Sarawak. This project focused on creating intuitive user flows for ticket purchasing, route planning, and real-time transit tracking.</p>
                        <ul>
                            <li>Tool Used: Figma (High-Fidelity Prototyping)</li>
                            <li>Achievement: Applied usability testing feedback to significantly refine navigation and interface accessibility.</li>
                        </ul>
                    </div>
<!-- Project 2: Mental Health Awareness Web App -->
                    <div class="project-card">
                        <span class="tech-stack-label">Full-Stack Web Development</span>
                        <h3>Mental Health Awareness Web Application</h3>
                        <p>Designed and built a functional web application providing educational content and interactive self-assessment quizzes related to mental well-being, demonstrating end-to-end development capabilities.</p>
                        <ul>
                            <li>Tech Stack: Java, HTML, CSS, MySQL</li>
                            <li>Achievement:Managed database operations (MySQL) and designed responsive, engaging user interfaces.</li>
                        </ul>
                    </div>
                    <!-- Project 3: Car Rental Management Website -->
                    <div class="project-card">
                        <span class="tech-stack-label">Database & Backend Integration</span>
                        <h3>Car Rental Management Website ("ZoomRentals")</h3>
                        <p>Constructed a robust car rental website featuring dynamic listing, booking, and comprehensive admin management features, proving ability to handle complex data and secure administrative interfaces.</p>
                        <ul>
                            <li>**Tech Stack:** HTML, PHP, MySQL</li>
                            <li>**Achievement:** Implemented reliable backend logic for data persistence and user session management.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: EXPERIENCE (PROFESSIONAL HISTORY) -->
        <!-- Focus: Soft Skills & Quantified Commercial Results -->
        <!-- ====================================================== -->
        <section id="experience" class="section">
            <div class="container">
                <h2 class="section-title">Professional & Commercial Experience</h2>

  <div class="experience-entry">
                    <div class="entry-date">2023</div>
                    <div class="entry-details">
                        <div class="entry-title">Book Reseller</div>
                        <div class="entry-company">Self-initiated Project | Pusa, Sarawak</div>
                        <div class="entry-description">
                            <ul>
                                <li>**Sales Success:Generated RM300 in sales within just three days by selling unused SPM notebooks, demonstrating entrepreneurial drive.</li>
                                <li>Commercial Skills:Successfully applied negotiation, persuasive communication, and basic market pricing strategies to interact with customers and close sales.</li>
                            </ul>
                        </div>
                    </div>
                </div>
<div class="experience-entry">
                     <div class="entry-date">2022</div>
                    <div class="entry-details">
                        <div class="entry-title">Event Catering & Food Service Assistant</div>
                        <div class="entry-company">Freelance/Part-time | Pusa, Sarawak</div>
                        <div class="entry-description">
                            <ul>
                                <li>**Teamwork in High-Pressure:** Collaborated effectively in fast-paced event environments to ensure timely delivery and service quality.</li>
                                <li>Attention to Detail:Maintained strict hygiene and safety standards during food preparation and service operations.</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
  </div>
						</section>
        <!-- ====================================================== -->
        <!-- SECTION: SKILLS & EDUCATION -->
        <!-- Focus: Tools, Languages, and Academic Depth -->
        <!-- ====================================================== -->
        <section id="skills" class="section">
            <div class="container">
                <h2 class="section-title">Technical Expertise & Education</h2>
                <div class="skills-grid">
                    <div class="skill-group">
                        <h4><i class="fas fa-code"></i> Core Development</h4>
                        <ul class="skill-list">
                            <li>Java Backend Logic, OOP</li>
                            <li>Python Scripting, Data Handling</li>
                            <li>HTML5, CSS3, JavaScript</li>
                            <li>C / C++ / Kotlin Fundamentals</li>
                        </ul>
                    </div>
                    <div class="skill-group">
                        <h4><i class="fas fa-palette"></i> Design & Data</h4>
                        <ul class="skill-list">
                            <li>**UI/UX Design** (Figma Expert)</li>
                            <li>MySQL (Database Management)</li>
                            <li>Canva / Unity Hub</li>
                            <li>System Analysis & Design (SAD)</li>
                        </ul>
                    </div>
                    <div class="skill-group">
                        <h4><i class="fas fa-handshake"></i> Professional Skills</h4>
                        <ul class="skill-list">
                            <li>Teamwork & Collaboration</li>
                            <li>Problem Solving & Critical Thinking</li>
                            <li>Effective Communication</li>
                            <li>Project Management</li>
                        </ul>
                    </div>
                </div>
                <!-- Related University Coursework -->
                <div id="key-courses" style="text-align: center;">
                    <h3 style="font-size: 1.8rem; font-weight: 700; color: var(--primary-color); margin-top: 4rem;">Relevant University Coursework</h3>
                    <ul class="course-list">
                        <li>UI/UX Design</li>
                        <li>Human-Computer Interaction (HCI)</li>
                        <li>Web Application Development</li>
                        <li>Mobile Application Development</li>
                        <li>Database Concept & Design</li>
                        <li>Computer Graphics</li>
                        <li>Game Design and Development</li>
                        <li>Project Management</li>
                    </ul>
                </div>
                </div>
        </section>
<!-- ====================================================== -->
        <!-- SECTION: CONTACT -->
        <!-- Focus: Call to Action and Contact Details -->
        <!-- ====================================================== -->
        <section id="contact" class="section">
            <div class="container">
                <h2 class="section-title">Get In Touch</h2>
                <div class="contact-info-container">
                    <p style="font-size: 1.15rem; color: #495057;">I am eager to contribute my technical and design skills to a growth-oriented team. Please feel free to reach out to discuss internship opportunities or my projects.</p>
                    <ul class="contact-list">
                        <li>
                            <span class="contact-icon"><i class="fas fa-envelope"></i></span>
                            <a href="mailto:nurulhidayu1111@gmail.com">nurulhidayu1111@gmail.com</a>
                        </li>
                        <li>
                            <span class="contact-icon"><i class="fas fa-phone"></i></span>
                            <span>+60 193375235</span>
                        </li>
                        <li style="font-size: 1.2rem;">
                            <span class="contact-icon"><i class="fas fa-map-marker-alt"></i></span>
                            <span>Kuching, Sarawak, Malaysia</span>
                        </li>
                    </ul>
                    <p class="references-note">References are available upon request, including lecturers Ts. Nurfauza binti Jali and Puan Nur Azima Alya Binti Narawi.</p>
                </div>
            </div>
        </section>
    </main>
<!-- ====================================================== -->
    <!-- FOOTER -->
    <!-- ====================================================== -->
    <footer class="footer">
        <div class="container">
            &copy; 2025 Nurul Hidayu Bt Suut. All rights reserved. | Built by Veronica Lydia .
        </div>
    </footer>
<!-- ====================================================== -->
    <!-- JAVASCRIPT LOGIC -->
    <!-- Focus: Smooth scrolling and theme management -->
    <!-- ====================================================== -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Helper function to safely query elements
            const $ = selector => document.querySelector(selector);
// --- 1. Smooth Scrolling Implementation ---
            const smoothScrollLinks = document.querySelectorAll('.smooth-scroll');
            smoothScrollLinks.forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = $(targetId);
                    if (targetElement) {
                        targetElement.scrollIntoView({ behavior: 'smooth' });
                    }
                });
            });
// --- 2. Dark/Light Theme Toggle Logic ---
            const body = document.body;
            const themeToggleBtn = $('#theme-toggle');
            const themeIcon = $('#theme-icon');
            const THEME_KEY = 'theme'; // Key for localStorage
/**
             * Sets the application theme and updates localStorage and the toggle icon.
             * @param {boolean} isDarkMode - True for dark mode, false for light mode.
             */
            function setTheme(isDarkMode) {
                if (isDarkMode) {
                    body.classList.add('dark-mode');
                    localStorage.setItem(THEME_KEY, 'dark');
                    themeIcon.textContent = '☀️'; // Sun icon for dark mode
                    themeToggleBtn.setAttribute('aria-label', 'Switch to light theme');
                } else {
                    body.classList.remove('dark-mode');
                    localStorage.setItem(THEME_KEY, 'light');
                    themeIcon.textContent = '🌙'; // Moon icon for light mode
                    themeToggleBtn.setAttribute('aria-label', 'Switch to dark theme');
                }
            }
// Initialization: Check and apply saved theme
            function initializeTheme() {
                // Default to 'light' if no preference is saved
                const savedTheme = localStorage.getItem(THEME_KEY);
                const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
                
  // If a theme is saved, use it. Otherwise, check OS preference (prefersDark)
                if (savedTheme === 'dark' || (!savedTheme && prefersDark)) {
                    setTheme(true);
                } else {
                    setTheme(false);
                }
            }

  // Event Listener for the button click
            if (themeToggleBtn) {
                themeToggleBtn.addEventListener('click', () => {
                    const isCurrentlyDark = body.classList.contains('dark-mode');
                    setTheme(!isCurrentlyDark);
                });
            }

  // Run initialization
            initializeTheme();
        });
    </script>
</body>
</html>
