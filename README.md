<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurul Hidayu - Multimedia Computing Portfolio</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom font and base styles - Updated for Black and Pink */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #030712; /* Deep Black (Slate 950) */
            color: #F3F4F6; /* Light Gray (High Contrast) */
        }
        /* Style for active navigation links */
        .nav-link.active {
            color: #EC4899; /* Pink 500 Accent */
            border-bottom: 2px solid #EC4899;
        }
        /* Custom button style for interaction */
        .btn-primary {
            /* Updated from indigo to pink */
            @apply px-6 py-3 bg-pink-600 text-white font-semibold rounded-lg shadow-lg hover:bg-pink-700 transition duration-300 ease-in-out transform hover:scale-105;
        }
        /* Custom image class for consistency */
        .responsive-img {
            @apply w-full h-auto rounded-xl object-cover shadow-2xl;
        }
        /* Style for the new Edit button */
        .btn-edit {
            @apply ml-4 px-3 py-1 text-xs font-medium text-black bg-pink-300 rounded-full hover:bg-pink-400 transition duration-150;
        }
        /* Edit modal styles */
        .edit-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        .edit-modal-content {
            background-color: #1f2937;
            padding: 2rem;
            border-radius: 0.5rem;
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
        }
        .edit-textarea {
            width: 100%;
            min-height: 200px;
            background-color: #374151;
            color: white;
            border: 1px solid #4b5563;
            border-radius: 0.375rem;
            padding: 0.75rem;
            margin-bottom: 1rem;
        }
        .edit-input {
            width: 100%;
            background-color: #374151;
            color: white;
            border: 1px solid #4b5563;
            border-radius: 0.375rem;
            padding: 0.75rem;
            margin-bottom: 1rem;
        }
    </style>
</head>
<body class="antialiased">
<!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900/95 backdrop-blur-sm shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <a href="#home" class="text-2xl font-bold text-pink-400">NURUL HIDAYU</a>
                <nav class="hidden md:flex space-x-8">
                    <!-- Links updated to hover:text-pink-400 -->
                    <a href="#about" class="nav-link text-gray-300 hover:text-pink-400 transition duration-150 py-2">About</a>
                    <a href="#skills" class="nav-link text-gray-300 hover:text-pink-400 transition duration-150 py-2">Skills</a>
                    <a href="#projects" class="nav-link text-gray-300 hover:text-pink-400 transition duration-150 py-2">Projects</a>
                    <a href="#contact" class="nav-link text-gray-300 hover:text-pink-400 transition duration-150 py-2">Contact</a>
                </nav>
                <button id="mobile-menu-button" class="md:hidden p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-pink-400" aria-label="Toggle menu">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>
                </button>
            </div>
        </div>
        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden">
            <a href="#about" class="block px-4 py-2 text-base text-gray-300 hover:bg-gray-800" onclick="document.getElementById('mobile-menu').classList.add('hidden')">About</a>
            <a href="#skills" class="block px-4 py-2 text-base text-gray-300 hover:bg-gray-800" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Skills</a>
            <a href="#projects" class="block px-4 py-2 text-base text-gray-300 hover:bg-gray-800" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Projects</a>
            <a href="#contact" class="block px-4 py-2 text-base text-gray-300 hover:bg-gray-800" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Contact</a>
        </div>
    </header>
<main>
        <!-- 1. Hero Section -->
        <section id="home" class="pt-16 pb-20 md:pt-24 md:pb-32 bg-gray-900" style="background-image: url('https://images.unsplash.com/photo-1519681393784-d120267933ba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80'); background-size: cover; background-position: center; background-blend-mode: multiply; background-color: rgba(3, 7, 18, 0.85);">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <div class="max-w-3xl mx-auto">
                    <!-- Updated Profile Image with uploaded file, requested size, and pink border -->
                    <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80" 
                         onerror="this.onerror=null;this.src='https://placehold.co/150x150/EC4899/FFFFFF?text=NH'" 
                         alt="Profile Photo" 
                         class="w-48 h-48 object-cover rounded-full mx-auto mb-6 border-4 border-pink-400 shadow-2xl transition-transform duration-300 hover:scale-105">
                    <!-- Text updated to Pink 300 -->
                    <p class="text-lg font-medium text-pink-300 mb-2 uppercase tracking-widest">
                        Multimedia Computing Student
                    </p>
                    <h1 class="text-5xl md:text-7xl font-extrabold leading-tight text-white mb-6">
                        NURUL HIDAYU BT SUUT
                    </h1>
                    <p class="text-xl text-gray-300 mb-8">
                        A motivated, creative, and fast-learning third-year student at UNIMAS, skilled in UI/UX design, Java, Python, and web development. Seeking an internship to apply technical expertise in real-world technology projects.
                    </p>
                    <a href="#contact" class="btn-primary">Get in Touch</a>
                </div>
            </div>
        </section>
<!-- 2. About Section -->
        <section id="about" class="py-16 md:py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="lg:order-2">
                        <div class="flex items-center mb-6">
                            <!-- Heading updated to Pink 400 -->
                            <h2 class="text-4xl font-bold text-white border-b-2 border-pink-400 pb-2">About Me</h2>
                            <button onclick="editSection('about')" class="btn-edit">
                                Edit Section
                            </button>
                        </div>
                        <p id="about-text-1" class="text-gray-300 mb-4 leading-relaxed">
                            Currently pursuing a Bachelor of Multimedia Computing (Hons) at Universiti Malaysia Sarawak (UNIMAS). My academic journey has equipped me with strong foundational knowledge in programming languages like Java, Python, HTML/CSS, and Kotlin, complemented by expertise in UI/UX design using tools like Figma.
                        </p>
                        <p id="about-text-2" class="text-gray-300 mb-6 leading-relaxed">
                            I thrive in team environments, focusing on effective communication and problem-solving to deliver high-quality, user-centric solutions.
                        </p>
                        <div class="space-y-4">
                            <!-- Education title updated to Pink 400 -->
                            <h3 class="text-2xl font-semibold text-pink-400 mt-8 mb-4">Education</h3>
                            <!-- Card background updated to a darker gray -->
                            <div id="education-1" class="bg-gray-900 p-4 rounded-lg shadow-inner">
                                <p class="font-bold text-white">Bachelor of Multimedia Computing (Hons)</p>
                                <p class="text-sm text-pink-300">Universiti Malaysia Sarawak (UNIMAS) - Current</p>
                            </div>
                            <div id="education-2" class="bg-gray-900 p-4 rounded-lg shadow-inner">
                                <p class="font-bold text-white">Foundation in Life Science (Pre-University)</p>
                                <p class="text-sm text-pink-300">Universiti Malaysia Sarawak (UNIMAS)</p>
                            </div>
                        </div>
                    </div>
                    <div class="lg:order-1">
                         <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" alt="Nurul Hidayu working" class="responsive-img max-h-[500px] lg:max-h-full" onerror="this.onerror=null;this.src='https://placehold.co/600x600/374151/FFFFFF?text=N+H+Profile';">
                    </div>
                </div>
            </div>
        </section>
<!-- 3. Skills Section -->
        <section id="skills" class="py-16 md:py-24 bg-gray-900/50 border-t border-b border-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex items-center justify-center mb-12">
                    <!-- Heading updated to Pink 400 -->
                    <h2 class="text-4xl font-bold text-white border-b-2 border-pink-400 inline-block pb-2">Technical Proficiency</h2>
                    <button onclick="editSection('skills')" class="btn-edit">
                        Edit Section
                    </button>
                </div>
                 <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                    <!-- Card Background and Hover Shadow updated to Pink -->
                    <div id="skills-programming" class="bg-gray-900 p-6 rounded-xl shadow-xl hover:shadow-pink-500/20 transition duration-300">
                        <h3 class="text-2xl font-semibold text-pink-400 mb-3">Programming</h3>
                        <ul class="space-y-2 text-gray-300">
                            <li>Java</li>
                            <li>Python</li>
                            <li>HTML / CSS / JavaScript</li>
                            <li>C / C++</li>
                            <li>Kotlin</li>
                        </ul>
                    </div>
<div id="skills-design" class="bg-gray-900 p-6 rounded-xl shadow-xl hover:shadow-pink-500/20 transition duration-300">
                        <h3 class="text-2xl font-semibold text-pink-400 mb-3">Design & Tools</h3>
                        <ul class="space-y-2 text-gray-300">
                            <li>Figma (UI/UX Design)</li>
                            <li>Canva (Graphics)</li>
                            <li>Unity (Game Design)</li>
                            <li>MySQL (Database)</li>
                            <li>PHP (Web Backend)</li>
                        </ul>
                    </div>
<div id="skills-soft" class="bg-gray-900 p-6 rounded-xl shadow-xl hover:shadow-pink-500/20 transition duration-300">
                        <h3 class="text-2xl font-semibold text-pink-400 mb-3">Soft Skills</h3>
                        <ul class="space-y-2 text-gray-300">
                            <li>Teamwork</li>
                            <li>Communication</li>
                            <li>Leadership</li>
                            <li>Problem Solving</li>
                        </ul>
                    </div>
                    <div id="skills-core" class="col-span-2 md:col-span-1 bg-gray-900 p-6 rounded-xl shadow-xl hover:shadow-pink-500/20 transition duration-300">
                        <h3 class="text-2xl font-semibold text-pink-400 mb-3">Core Studies</h3>
                        <ul class="space-y-2 text-gray-300">
                            <li>UI/UX Design</li>
                            <li>Web Application Development</li>
                            <li>Human-Computer Interaction</li>
                            <li>Database Concept & Design</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
<!-- 4. Projects Section -->
        <section id="projects" class="py-16 md:py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex items-center justify-center mb-12">
                    <!-- Heading updated to Pink 400 -->
                    <h2 class="text-4xl font-bold text-white border-b-2 border-pink-400 inline-block pb-2">Selected Projects & Coursework</h2>
                    <button onclick="editSection('projects')" class="btn-edit">
                        Edit Section
                    </button>
                </div>
                <div class="space-y-12">
                    <!-- Project 1: Mental Health Awareness Web Application -->
                    <div id="project-1" class="grid grid-cols-1 md:grid-cols-3 bg-gray-900 rounded-xl overflow-hidden shadow-2xl hover:shadow-pink-500/30 transition duration-300">
                        <div class="md:col-span-1">
                            <img src="https://placehold.co/600x400/EC4899/030712?text=UI%2FUX+Project" alt="Mental Health App Screenshot" class="w-full h-full object-cover">
                        </div>
                        <div class="md:col-span-2 p-6 lg:p-10">
                            <!-- Tag updated to Pink 600 -->
                            <span class="inline-block bg-pink-600 text-white text-xs font-semibold px-3 py-1 rounded-full mb-3">UI/UX & Web Dev</span>
                            <h3 class="text-3xl font-bold text-white mb-4">Mental Health Awareness Web Application</h3>
                            <p id="project-1-desc" class="text-gray-300 mb-4">
                                Developed a comprehensive web application to promote mental health awareness. The project focused heavily on the user experience and design phase.
                            </p>
                            <ul id="project-1-details" class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Key Contribution: Designed the complete UI/UX of the user interfaces in Figma.</li>
                                <li>Process: Applied feedback from extensive usability testing to iterate and improve the final design.</li>
                                <li>Technologies: Java, HTML, CSS, MySQL.</li>
                            </ul>
                        </div>
                    </div>
<!-- Project 2: Car Rental Management Website - "ZoomRentals" -->
                    <div id="project-2" class="grid grid-cols-1 md:grid-cols-3 bg-gray-900 rounded-xl overflow-hidden shadow-2xl hover:shadow-pink-500/30 transition duration-300">
                        <div class="md:col-span-1">
                            <img src="https://placehold.co/600x400/EC4899/030712?text=PHP+MySQL+System" alt="Car Rental Website Screenshot" class="w-full h-full object-cover">
                        </div>
                        <div class="md:col-span-2 p-6 lg:p-10">
                            <!-- Tag updated to Pink 600 -->
                            <span class="inline-block bg-pink-600 text-white text-xs font-semibold px-3 py-1 rounded-full mb-3">Backend & Database</span>
                            <h3 class="text-3xl font-bold text-white mb-4">Car Rental Management Website - "ZoomRentals"</h3>
                            <p id="project-2-desc" class="text-gray-300 mb-4">
                                Built a full-featured car rental system with interfaces for booking, vehicle listing, and administrator management.
                            </p>
                            <ul id="project-2-details" class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Key Feature: Implemented backend logic using PHP for dynamic data processing and handling.</li>
                                <li>Database: Integrated with MySQL to manage vehicle inventory, bookings, and user accounts.</li>
                                <li>Technologies: HTML, PHP, MySQL.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>
<!-- 5. Contact Section -->
        <section id="contact" class="py-16 md:py-24 bg-gray-900/50 border-t border-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex items-center justify-center mb-12">
                    <!-- Heading updated to Pink 400 -->
                    <h2 class="text-4xl font-bold text-white border-b-2 border-pink-400 inline-block pb-2">Get In Touch</h2>
                    <button onclick="editSection('contact')" class="btn-edit">
                        Edit Section
                    </button>
                </div>
                 <!-- Card background updated to a darker gray -->
                <div class="max-w-3xl mx-auto bg-gray-900 p-8 md:p-12 rounded-xl shadow-2xl">
                    <p id="contact-desc" class="text-gray-300 text-center mb-8">
                        I am currently seeking job opportunities in technology and design. Feel free to connect with me!
                    </p>
<div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-10 text-center">
                        <!-- Inner card backgrounds updated -->
                        <div class="p-4 bg-gray-800 rounded-lg">
                            <p class="font-semibold text-pink-400">Email</p>
                            <p id="contact-email" class="text-lg text-white">nurulhidayu1111@gmail.com</p>
                        </div>
                        <div class="p-4 bg-gray-800 rounded-lg">
                            <p class="font-semibold text-pink-400">Phone</p>
                            <p id="contact-phone" class="text-lg text-white">+60 193375235</p>
                        </div>
                    </div>
<!-- Simple Contact Form Placeholder -->
                    <form class="space-y-4">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-300 mb-1">Name</label>
                            <!-- Input styling updated to pink focus rings -->
                            <input type="text" id="name" name="name" class="w-full p-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-pink-500 focus:border-pink-500 text-white" placeholder="Your Name">
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-300 mb-1">Email</label>
                            <input type="email" id="email" name="email" class="w-full p-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-pink-500 focus:border-pink-500 text-white" placeholder="your.email@example.com">
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-300 mb-1">Message</label>
                            <textarea id="message" name="message" rows="4" class="w-full p-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-pink-500 focus:border-pink-500 text-white" placeholder="I'd like to discuss an opportunity..."></textarea>
                        </div>
                        <!-- Button updated to btn-primary (Pink) -->
                        <button type="submit" class="btn-primary w-full">Send Message</button>
                        <p class="text-xs text-gray-500 text-center pt-2">*This is a placeholder form and does not send emails.</p>
                    </form>
                </div>
            </div>
        </section>
    </main>
<!-- Footer -->
    <footer class="bg-gray-900 py-8 border-t border-gray-700">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-gray-400">
            <p>&copy; 2024 Nurul Hidayu BT Suut. All rights reserved.</p>
            <p class="mt-2 text-sm">Built for an internship application.</p>
        </div>
    </footer>
<!-- Edit Modal -->
    <div id="editModal" class="edit-modal">
        <div class="edit-modal-content">
            <h3 id="editModalTitle" class="text-2xl font-bold text-white mb-4">Edit Section</h3>
            <div id="editModalContent">
                <!-- Dynamic content will be inserted here -->
            </div>
            <div class="flex justify-end space-x-4 mt-4">
                <button id="cancelEdit" class="px-4 py-2 bg-gray-600 text-white rounded-lg hover:bg-gray-700 transition">Cancel</button>
                <button id="saveEdit" class="px-4 py-2 bg-pink-600 text-white rounded-lg hover:bg-pink-700 transition">Save Changes</button>
            </div>
        </div>
    </div>
<script>
        // Edit functionality
        const editModal = document.getElementById('editModal');
        const editModalTitle = document.getElementById('editModalTitle');
        const editModalContent = document.getElementById('editModalContent');
        const cancelEditBtn = document.getElementById('cancelEdit');
        const saveEditBtn = document.getElementById('saveEdit');
        let currentSection = '';
        // Function to open edit modal for a specific section
        function editSection(sectionId) {
            currentSection = sectionId;
        // Set modal title based on section
            let sectionTitle = '';
            switch(sectionId) {
                case 'about':
                    sectionTitle = 'About Section';
                    break;
                case 'skills':
                    sectionTitle = 'Skills Section';
                    break;
                case 'projects':
                    sectionTitle = 'Projects Section';
                    break;
                case 'contact':
                    sectionTitle = 'Contact Section';
                    break;
                default:
                    sectionTitle = 'Edit Section';
            }
            editModalTitle.textContent = sectionTitle;
            // Generate appropriate edit form based on section
            let editForm = '';
            if (sectionId === 'about') {
                const aboutText1 = document.getElementById('about-text-1').textContent;
                const aboutText2 = document.getElementById('about-text-2').textContent;
                const education1Title = document.querySelector('#education-1 .font-bold').textContent;
                const education1Subtitle = document.querySelector('#education-1 .text-sm').textContent;
                const education2Title = document.querySelector('#education-2 .font-bold').textContent;
                const education2Subtitle = document.querySelector('#education-2 .text-sm').textContent;
                editForm = `
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">About Text 1</label>
                        <textarea id="edit-about-text-1" class="edit-textarea">${aboutText1}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">About Text 2</label>
                        <textarea id="edit-about-text-2" class="edit-textarea">${aboutText2}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Education 1</label>
                        <input type="text" id="edit-education-1-title" class="edit-input" value="${education1Title}">
                        <input type="text" id="edit-education-1-subtitle" class="edit-input mt-2" value="${education1Subtitle}">
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Education 2</label>
                        <input type="text" id="edit-education-2-title" class="edit-input" value="${education2Title}">
                        <input type="text" id="edit-education-2-subtitle" class="edit-input mt-2" value="${education2Subtitle}">
                    </div>
                `;
            } else if (sectionId === 'skills') {
                const programmingSkills = Array.from(document.querySelectorAll('#skills-programming li')).map(li => li.textContent).join('\n');
                const designSkills = Array.from(document.querySelectorAll('#skills-design li')).map(li => li.textContent).join('\n');
                const softSkills = Array.from(document.querySelectorAll('#skills-soft li')).map(li => li.textContent).join('\n');
                const coreSkills = Array.from(document.querySelectorAll('#skills-core li')).map(li => li.textContent).join('\n');
                editForm = `
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Programming Skills</label>
                        <textarea id="edit-skills-programming" class="edit-textarea">${programmingSkills}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Design & Tools</label>
                        <textarea id="edit-skills-design" class="edit-textarea">${designSkills}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Soft Skills</label>
                        <textarea id="edit-skills-soft" class="edit-textarea">${softSkills}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Core Studies</label>
                        <textarea id="edit-skills-core" class="edit-textarea">${coreSkills}</textarea>
                    </div>
                `;
            } else if (sectionId === 'projects') {
                const project1Desc = document.getElementById('project-1-desc').textContent;
                const project1Details = Array.from(document.querySelectorAll('#project-1-details li')).map(li => li.textContent).join('\n');
                const project2Desc = document.getElementById('project-2-desc').textContent;
                const project2Details = Array.from(document.querySelectorAll('#project-2-details li')).map(li => li.textContent).join('\n');
                editForm = `
                    <div class="mb-6 p-4 bg-gray-800 rounded-lg">
                        <h4 class="text-lg font-semibold text-pink-400 mb-2">Project 1: Mental Health Awareness Web Application</h4>
                        <div class="mb-3">
                            <label class="block text-sm font-medium text-gray-300 mb-1">Description</label>
                            <textarea id="edit-project-1-desc" class="edit-textarea">${project1Desc}</textarea>
                        </div>
                        <div class="mb-3">
                            <label class="block text-sm font-medium text-gray-300 mb-1">Details (one per line)</label>
                            <textarea id="edit-project-1-details" class="edit-textarea">${project1Details}</textarea>
                        </div>
                    </div>
                    <div class="p-4 bg-gray-800 rounded-lg">
                        <h4 class="text-lg font-semibold text-pink-400 mb-2">Project 2: Car Rental Management Website - "ZoomRentals"</h4>
                        <div class="mb-3">
                            <label class="block text-sm font-medium text-gray-300 mb-1">Description</label>
                            <textarea id="edit-project-2-desc" class="edit-textarea">${project2Desc}</textarea>
                        </div>
                        <div class="mb-3">
                            <label class="block text-sm font-medium text-gray-300 mb-1">Details (one per line)</label>
                            <textarea id="edit-project-2-details" class="edit-textarea">${project2Details}</textarea>
                        </div>
                    </div>
                `;
            } else if (sectionId === 'contact') {
                const contactDesc = document.getElementById('contact-desc').textContent;
                const contactEmail = document.getElementById('contact-email').textContent;
                const contactPhone = document.getElementById('contact-phone').textContent;
                editForm = `
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Contact Description</label>
                        <textarea id="edit-contact-desc" class="edit-textarea">${contactDesc}</textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Email</label>
                        <input type="text" id="edit-contact-email" class="edit-input" value="${contactEmail}">
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-medium text-gray-300 mb-1">Phone</label>
                        <input type="text" id="edit-contact-phone" class="edit-input" value="${contactPhone}">
                    </div>
                `;
            }
            editModalContent.innerHTML = editForm;
            editModal.style.display = 'flex';
        }
         // Function to save changes
        function saveChanges() {
            if (currentSection === 'about') {
                document.getElementById('about-text-1').textContent = document.getElementById('edit-about-text-1').value;
                document.getElementById('about-text-2').textContent = document.getElementById('edit-about-text-2').value;
                document.querySelector('#education-1 .font-bold').textContent = document.getElementById('edit-education-1-title').value;
                document.querySelector('#education-1 .text-sm').textContent = document.getElementById('edit-education-1-subtitle').value;
                document.querySelector('#education-2 .font-bold').textContent = document.getElementById('edit-education-2-title').value;
                document.querySelector('#education-2 .text-sm').textContent = document.getElementById('edit-education-2-subtitle').value;
            } else if (currentSection === 'skills') {
                updateSkillsList('skills-programming', 'edit-skills-programming');
                updateSkillsList('skills-design', 'edit-skills-design');
                updateSkillsList('skills-soft', 'edit-skills-soft');
                updateSkillsList('skills-core', 'edit-skills-core');
            } else if (currentSection === 'projects') {
                document.getElementById('project-1-desc').textContent = document.getElementById('edit-project-1-desc').value;
                updateProjectDetails('project-1-details', 'edit-project-1-details');
                document.getElementById('project-2-desc').textContent = document.getElementById('edit-project-2-desc').value;
                updateProjectDetails('project-2-details', 'edit-project-2-details');
            } else if (currentSection === 'contact') {
                document.getElementById('contact-desc').textContent = document.getElementById('edit-contact-desc').value;
                document.getElementById('contact-email').textContent = document.getElementById('edit-contact-email').value;
                document.getElementById('contact-phone').textContent = document.getElementById('edit-contact-phone').value;
            }
            editModal.style.display = 'none';
        }
         // Helper function to update skills lists
        function updateSkillsList(targetId, sourceId) {
            const skillsList = document.getElementById(targetId).querySelector('ul');
            const skillsText = document.getElementById(sourceId).value;
            const skillsArray = skillsText.split('\n').filter(skill => skill.trim() !== '');
            skillsList.innerHTML = '';
            skillsArray.forEach(skill => {
                const li = document.createElement('li');
                li.textContent = skill;
                skillsList.appendChild(li);
            });
        }
        // Helper function to update project details
        function updateProjectDetails(targetId, sourceId) {
            const detailsList = document.getElementById(targetId);
            const detailsText = document.getElementById(sourceId).value;
            const detailsArray = detailsText.split('\n').filter(detail => detail.trim() !== '');
            detailsList.innerHTML = '';
            detailsArray.forEach(detail => {
                const li = document.createElement('li');
                li.textContent = detail;
                detailsList.appendChild(li);
            });
        }
        // Event listeners for modal buttons
        cancelEditBtn.addEventListener('click', () => {
            editModal.style.display = 'none';
        });
        saveEditBtn.addEventListener('click', saveChanges);
    // Close modal when clicking outside
        editModal.addEventListener('click', (e) => {
            if (e.target === editModal) {
                editModal.style.display = 'none';
            }
        });
// Smooth Scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
// Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
// Optional: Highlight active navigation link based on scroll position
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-link');
        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 70; // Offset for fixed header
                if (scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });
 navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').includes(current)) {
                    link.classList.add('active');
                }
            });
        });
// Pre-set 'Home' as active on load
        document.querySelector('a[href="#home"]').classList.add('active');
    </script>
</body>
</html>
