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
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        /* Header Styles */
        header {
            background-color: var(--secondary-bg);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--accent-color);
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin-left: 30px;
        }
        nav ul li a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent-color);
            transition: width 0.3s;
        }
        nav ul li a:hover {
            color: var(--accent-color);
        }
        nav ul li a:hover::after {
            width: 100%;
        }
        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, var(--primary-bg) 0%, #2a0a1a 100%);
            text-align: center;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }
        .profile-container {
            margin-bottom: 30px;
        }
        .profile-pic {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--accent-color);
            box-shadow: 0 0 20px rgba(233, 30, 99, 0.3);
        }
        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }
        .hero h2 {
            font-size: 24px;
            color: var(--accent-color);
            margin-bottom: 20px;
        }
        .hero p {
            max-width: 600px;
            margin: 0 auto 30px;
            color: var(--text-muted);
        }
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        .btn:hover {
            background-color: var(--accent-light);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(233, 30, 99, 0.4);
        }
        /* Section Styles */
        section {
            padding: 100px 0;
        }
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        .section-title h2 {
            font-size: 36px;
            display: inline-block;
            padding-bottom: 10px;
        }
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background-color: var(--accent-color);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
        }
        .about-text p {
            margin-bottom: 20px;
            color: var(--text-muted);
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        .skill-item {
            background-color: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid var(--accent-color);
        }
        .skill-item h4 {
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
        }
        .skill-bar {
            height: 8px;
            background-color: var(--secondary-bg);
            border-radius: 4px;
            overflow: hidden;
        }
        .skill-progress {
            height: 100%;
            background-color: var(--accent-color);
            border-radius: 4px;
        }
        /* Portfolio Section */
        .portfolio-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }
        .add-project-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            font-size: 24px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        .add-project-btn:hover {
            background-color: var(--accent-light);
            transform: rotate(90deg);
        }
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        .portfolio-item {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
            position: relative;
        }
        .portfolio-item:hover {
            transform: translateY(-10px);
        }
        .portfolio-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .portfolio-content {
            padding: 20px;
        }
        .portfolio-content h3 {
            margin-bottom: 10px;
        }
        .portfolio-content p {
            color: var(--text-muted);
            margin-bottom: 15px;
        }
        .portfolio-actions {
            display: flex;
            justify-content: space-between;
        }
        .btn-small {
            padding: 8px 15px;
            font-size: 14px;
        }
        .btn-outline {
            background-color: transparent;
            border: 1px solid var(--accent-color);
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
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        .modal-content {
            background-color: var(--card-bg);
            width: 90%;
            max-width: 800px;
            border-radius: 10px;
            padding: 30px;
            position: relative;
            max-height: 90vh;
            overflow-y: auto;
        }
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            cursor: pointer;
            color: var(--text-muted);
        }
        .close-modal:hover {
            color: var(--accent-color);
        }
        .modal-header {
            margin-bottom: 20px;
        }
        .modal-body {
            margin-bottom: 20px;
        }
        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 10px;
        }
        /* Form Styles */
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        .form-control {
            width: 100%;
            padding: 12px;
            background-color: var(--secondary-bg);
            border: 1px solid var(--border-color);
            border-radius: 5px;
            color: var(--text-color);
        }
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--accent-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
        }
        /* Footer */
        footer {
            background-color: var(--secondary-bg);
            padding: 40px 0;
            text-align: center;
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .social-links a {
            color: var(--text-color);
            font-size: 20px;
            transition: color 0.3s;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--card-bg);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .social-links a:hover {
            color: var(--accent-color);
            transform: translateY(-3px);
        }
        .copyright {
            color: var(--text-muted);
            font-size: 14px;
        }
        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content, .contact-content {
                grid-template-columns: 1fr;
            }
            .skills-grid {
                grid-template-columns: 1fr;
            }
            .hero h1 {
                font-size: 36px;
            }
            .hero h2 {
                font-size: 20px;
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
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">NURUL HIDAYU</div>
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
<section id="home" class="hero">
        <div class="container">
            <div class="profile-container">
                <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80" alt="Nurul Hidayu" class="profile-pic">
            </div>
            <h1>Nurul Hidayu</h1>
            <h2>Multimedia Computing Student & UI/UX Designer</h2>
            <p>Third-year Bachelor of Multimedia Computing student at Universiti Malaysia Sarawak (UNIMAS), skilled in Java, Python, HTML/CSS, and UI/UX design. A motivated, fast-learning, and creative individual with strong teamwork and communication skills.</p>
            <a href="#portfolio" class="btn">View My Work</a>
        </div>
    </section>
<!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
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
                <div class="skills">
                    <h3>My Skills</h3>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <h4>Java <span>90%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 90%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>Python <span>85%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>HTML/CSS <span>95%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 95%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>UI/UX Design <span>90%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 90%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>JavaScript <span>80%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 80%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <h4>Figma <span>85%</span></h4>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 85%"></div>
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
                <div class="section-title" style="margin-bottom: 0;">
                    <h2>My Portfolio</h2>
                </div>
                <button class="add-project-btn" onclick="openAddModal()">
                    <i class="fas fa-plus"></i>
                </button>
            </div>
            <div class="portfolio-grid" id="portfolioGrid">
                <!-- Project 1 -->
                <div class="portfolio-item">
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
                <div class="portfolio-item">
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
                <div class="portfolio-item">
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
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Location</h3>
                            <p>Kuching, Sarawak, Malaysia</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Phone</h3>
                            <p>+60 193375235</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>nurulhidayu1111@gmail.com</p>
                        </div>
                    </div>
                </div>
                <div>
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
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-behance"></i></a>
                <a href="#"><i class="fab fa-dribbble"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
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
// Open project detail modal
        function openProjectModal(index) {
            currentProjectIndex = index;
            const project = projects[index];
            document.getElementById('modalProjectTitle').textContent = project.title;
            document.getElementById('modalProjectImage').src = project.image;
            document.getElementById('modalProjectDescription').textContent = project.description;
            document.getElementById('modalProjectDetails').innerHTML = project.details;
            document.getElementById('projectModal').style.display = 'flex';
        }
// Close project detail modal
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
            alert('Project updated successfully!');
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
            alert('Project added successfully!');
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
            educationItem.innerHTML = '<strong>${title}</strong><br>${institution}${year ? '(${year})` : ''}`;
            document.getElementById('education-list').appendChild(educationItem);
            closeAddEducationModal();
            alert('Education added successfully!');
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
            portfolioItem.className = 'portfolio-item';
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
        }
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
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });
    </script>
</body>
</html>
