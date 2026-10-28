<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Navigation Bar -->
    <header>
        <nav class="navbar">
            <div class="logo">MyPortfolio</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm <span class="highlight">John Doe</span></h1>
            <p>Computer Science Student & Web Developer</p>
            <a href="resume.pdf" class="btn" download>Download Resume</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <h2>About Me</h2>
        <p>I am a passionate undergraduate student eager to build interactive and responsive web applications using modern web development technologies.</p>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section bg-light">
        <h2>Technical Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">HTML5</div>
            <div class="skill-card">CSS3</div>
            <div class="skill-card">JavaScript</div>
            <div class="skill-card">Git & GitHub</div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="filter-buttons">
            <button class="filter-btn active" data-filter="all">All</button>
            <button class="filter-btn" data-filter="web">Web</button>
            <button class="filter-btn" data-filter="js">JavaScript</button>
        </div>
        <div class="projects-grid" id="projects-container">
            <!-- Dynamically injected via JavaScript -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section bg-light">
        <h2>Contact Me</h2>
        <form id="contact-form">
            <div class="form-group">
                <input type="text" id="name" placeholder="Your Name" required>
            </div>
            <div class="form-group">
                <input type="email" id="email" placeholder="Your Email" required>
            </div>
            <div class="form-group">
                <textarea id="message" placeholder="Your Message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn">Send Message</button>
            <p id="form-feedback"></p>
        </form>
    </section>

    <footer>
        <p>&copy; 2026 Student Portfolio. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    line-height: 1.6;
    color: #333;
    scroll-behavior: smooth;
}

/* Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #2c3e50;
    color: #fff;
    padding: 1rem 5%;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 20px;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #3498db;
}

/* Hero Section */
.hero {
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero-bg.jpg') no-repeat center center/cover;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
    padding: 0 20px;
}

.hero h1 {
    font-size: 3rem;
    margin-bottom: 10px;
}

.highlight {
    color: #3498db;
}

.btn {
    display: inline-block;
    background: #3498db;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    text-decoration: none;
    margin-top: 15px;
    cursor: pointer;
    transition: background 0.3s;
}

.btn:hover {
    background: #2980b9;
}

/* Sections */
.section {
    padding: 80px 10% 50px;
    text-align: center;
}

.bg-light {
    background: #f9f9f9;
}

.section h2 {
    margin-bottom: 40px;
    font-size: 2.2rem;
    color: #2c3e50;
}

/* Skills Grid */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
}

.skill-card {
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    font-weight: bold;
    color: #2c3e50;
}

/* Projects */
.filter-buttons {
    margin-bottom: 30px;
}

.filter-btn {
    background: #ddd;
    border: none;
    padding: 8px 16px;
    margin: 0 5px;
    border-radius: 4px;
    cursor: pointer;
    transition: 0.3s;
}

.filter-btn.active, .filter-btn:hover {
    background: #3498db;
    color: #fff;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
}

.project-card {
    background: #fff;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    text-align: left;
}

.project-card h3 {
    margin-bottom: 10px;
    color: #2c3e50;
}

/* Contact Form */
#contact-form {
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.form-group input, .form-group textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

footer {
    text-align: center;
    padding: 20px;
    background: #2c3e50;
    color: #fff;
}
// Project Data Array
const projects = [
    { title: "Portfolio Website", category: "web", description: "A responsive personal portfolio built using HTML, CSS, and JS." },
    { title: "Task Manager", category: "js", description: "An interactive to-do list application with local storage support." },
    { title: "E-Commerce Landing Page", category: "web", description: "A modern product landing page layout designed with CSS Flexbox." },
    { title: "Weather App", category: "js", description: "A weather forecast tool fetching real-time data using JavaScript fetch API." }
];

const projectsContainer = document.getElementById('projects-container');
const filterButtons = document.querySelectorAll('.filter-btn');

// Function to Display Projects
function displayProjects(filteredProjects) {
    projectsContainer.innerHTML = '';
    filteredProjects.forEach(project => {
        const card = document.createElement('div');
        card.classList.add('project-card');
        card.innerHTML = `
            <h3>${project.title}</h3>
            <p>${project.description}</p>
            <a href="#" class="btn">View Project</a>
        `;
        projectsContainer.appendChild(card);
    });
}

// Initial Render
displayProjects(projects);

// Filter Event Listeners
filterButtons.forEach(button => {
    button.addEventListener('click', (e) => {
        document.querySelector('.filter-btn.active').classList.remove('active');
        e.target.classList.add('active');
        
        const filter = e.target.getAttribute('data-filter');
        if (filter === 'all') {
            displayProjects(projects);
        } else {
            const filtered = projects.filter(p => p.category === filter);
            displayProjects(filtered);
        }
    });
});

// Contact Form Validation Logic
const contactForm = document.getElementById('contact-form');
const formFeedback = document.getElementById('form-feedback');

contactForm.addEventListener('submit', (e) => {
    e.preventDefault();
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();
    const message = document.getElementById('message').value.trim();
    
    // Simple Email Regex Validation
    const emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;

    if (name === "" || email === "" || message === "") {
        formFeedback.style.color = "red";
        formFeedback.textContent = "Please fill in all mandatory fields.";
    } else if (!email.match(emailPattern)) {
        formFeedback.style.color = "red";
        formFeedback.textContent = "Please enter a valid email address.";
    } else {
        formFeedback.style.color = "green";
        formFeedback.textContent = "Thank you! Your message has been sent successfully.";
        contactForm.reset();
    }
});
