==============================
FILE 1: index.html
==============================

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <nav>
        <div class="logo">MK</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button id="themeToggle" class="theme-btn">🌙</button>
    </nav>

    <section id="home">
        <div class="hero">
            <p class="greeting">Hi, my name is</p>
            <h1>Muhammad Khan</h1>
            <h2>I build things for the web.</h2>
            <p class="description">
                I'm a full-stack developer specializing in creating
                exceptional digital experiences. Currently focused on
                building accessible, human-centered products.
            </p>
            <a href="#projects" class="cta-btn">View My Work</a>
        </div>
    </section>

    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div class="about-text">
                <p>
                    Hello! I'm a passionate developer based in India who
                    enjoys creating things that live on the internet. My
                    interest in web development started back in 2020 when
                    I decided to try editing custom themes — turns out
                    hacking together a re-themed button taught me a lot
                    about HTML & CSS!
                </p>
                <p>
                    Fast-forward to today, and I've had the privilege of
                    working on various projects. My main focus these days
                    is building accessible, inclusive products and digital
                    experiences for a variety of clients.
                </p>
                <div class="skills">
                    <span>JavaScript</span>
                    <span>React</span>
                    <span>Node.js</span>
                    <span>Python</span>
                    <span>MongoDB</span>
                    <span>AWS</span>
                </div>
            </div>
            <div class="about-image">
                <div class="image-placeholder">📷</div>
            </div>
        </div>
    </section>

    <section id="projects">
        <h2 class="section-title">Some Things I've Built</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-top">
                    <div class="folder-icon">📁</div>
                    <div class="project-links">
                        <a href="#">🔗</a>
                    </div>
                </div>
                <h3>Weather Dashboard</h3>
                <p>
                    A real-time weather application with location-based
                    forecasts, interactive maps, and severe weather alerts
                    using OpenWeather API.
                </p>
                <div class="project-tech">
                    <span>React</span>
                    <span>API</span>
                    <span>CSS Grid</span>
                </div>
            </div>

            <div class="project-card">
                <div class="project-top">
                    <div class="folder-icon">📁</div>
                    <div class="project-links">
                        <a href="#">🔗</a>
                    </div>
                </div>
                <h3>Task Manager App</h3>
                <p>
                    Full-stack task management application with drag-and-drop
                    functionality, user authentication, and real-time updates.
                </p>
                <div class="project-tech">
                    <span>Node.js</span>
                    <span>Express</span>
                    <span>MongoDB</span>
                </div>
            </div>

            <div class="project-card">
                <div class="project-top">
                    <div class="folder-icon">📁</div>
                    <div class="project-links">
                        <a href="#">🔗</a>
                    </div>
                </div>
                <h3>E-Commerce Platform</h3>
                <p>
                    A modern e-commerce platform with payment integration,
                    inventory management, and an intuitive admin dashboard.
                </p>
                <div class="project-tech">
                    <span>Next.js</span>
                    <span>Stripe</span>
                    <span>PostgreSQL</span>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2 class="section-title">Get In Touch</h2>
        <p class="contact-description">
            I'm currently looking for new opportunities. Whether you have
            a project or just want to say hi, feel free to reach out!
        </p>
        <a href="mailto:hello@example.com" class="cta-btn">Say Hello</a>
    </section>

    <footer>
        <p>Designed & Built by Muhammad Khan &copy; 2026</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>


==============================
FILE 2: style.css
==============================

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --bg: #0a192f;
    --bg-secondary: #112240;
    --text: #ccd6f6;
    --text-secondary: #8892b0;
    --accent: #64ffda;
    --card-bg: #112240;
    --nav-bg: rgba(10, 25, 47, 0.85);
}

[data-theme="light"] {
    --bg: #ffffff;
    --bg-secondary: #f0f4f8;
    --text: #1a202c;
    --text-secondary: #4a5568;
    --accent: #2b6cb0;
    --card-bg: #ffffff;
    --nav-bg: rgba(255, 255, 255, 0.85);
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Space Grotesk', sans-serif;
    background-color: var(--bg);
    color: var(--text);
    line-height: 1.6;
    transition: background-color 0.3s, color 0.3s;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    background: var(--nav-bg);
    backdrop-filter: blur(10px);
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 28px;
    font-weight: 700;
    color: var(--accent);
    border: 2px solid var(--accent);
    width: 45px;
    height: 45px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 8px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 30px;
}

nav ul li a {
    color: var(--text);
    text-decoration: none;
    font-size: 14px;
    font-weight: 500;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: var(--accent);
}

.theme-btn {
    background: transparent;
    border: 1px solid var(--accent);
    color: var(--accent);
    padding: 8px 14px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 16px;
    transition: all 0.3s;
}

.theme-btn:hover {
    background: var(--accent);
    color: var(--bg);
}

section {
    min-height: 100vh;
    padding: 120px 50px 50px;
    max-width: 1000px;
    margin: 0 auto;
}

#home {
    display: flex;
    align-items: center;
}

.hero {
    max-width: 700px;
}

.greeting {
    color: var(--accent);
    font-size: 18px;
    margin-bottom: 15px;
    font-weight: 500;
}

.hero h1 {
    font-size: 72px;
    font-weight: 700;
    line-height: 1.1;
    margin-bottom: 10px;
}

.hero h2 {
    font-size: 56px;
    font-weight: 600;
    color: var(--text-secondary);
    line-height: 1.1;
    margin-bottom: 20px;
}

.hero .description {
    font-size: 18px;
    color: var(--text-secondary);
    max-width: 550px;
    margin-bottom: 40px;
}

.cta-btn {
    display: inline-block;
    padding: 16px 32px;
    border: 2px solid var(--accent);
    color: var(--accent);
    text-decoration: none;
    border-radius: 6px;
    font-size: 16px;
    font-weight: 500;
    transition: all 0.3s;
}

.cta-btn:hover {
    background: var(--accent);
    color: var(--bg);
}

.section-title {
    font-size: 32px;
    margin-bottom: 40px;
    position: relative;
    display: inline-block;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 0;
    width: 60%;
    height: 3px;
    background: var(--accent);
    border-radius: 2px;
}

.about-content {
    display: grid;
    grid-template-columns: 3fr 2fr;
    gap: 50px;
    align-items: center;
}

.about-text p {
    color: var(--text-secondary);
    margin-bottom: 20px;
    font-size: 16px;
}

.skills {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 25px;
}

.skills span {
    background: var(--bg-secondary);
    color: var(--accent);
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
    border: 1px solid var(--accent);
}

.image-placeholder {
    width: 250px;
    height: 250px;
    background: var(--bg-secondary);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
    border: 2px solid var(--accent);
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
}

.project-card {
    background: var(--card-bg);
    padding: 30px;
    border-radius: 10px;
    transition: transform 0.3s;
    border: 1px solid transparent;
}

.project-card:hover {
    transform: translateY(-8px);
    border-color: var(--accent);
}

.project-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.folder-icon {
    font-size: 40px;
}

.project-links a {
    color: var(--text);
    text-decoration: none;
    font-size: 22px;
    transition: color 0.3s;
}

.project-links a:hover {
    color: var(--accent);
}

.project-card h3 {
    margin-bottom: 12px;
    font-size: 22px;
}

.project-card p {
    color: var(--text-secondary);
    font-size: 14px;
    margin-bottom: 20px;
}

.project-tech {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
}

.project-tech span {
    color: var(--text-secondary);
    font-size: 12px;
    font-weight: 500;
}

#contact {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.contact-description {
    color: var(--text-secondary);
    max-width: 500px;
    margin-bottom: 40px;
    font-size: 16px;
}

footer {
    text-align: center;
    padding: 30px;
    color: var(--text-secondary);
    font-size: 13px;
}

@media (max-width: 768px) {
    .hero h1 {
        font-size: 42px;
    }

    .hero h2 {
        font-size: 32px;
    }

    .about-content {
        grid-template-columns: 1fr;
    }

    .image-placeholder {
        width: 180px;
        height: 180px;
        margin: 0 auto;
    }

    nav {
        padding: 15px 25px;
    }

    nav ul {
        gap: 15px;
    }

    nav ul li a {
        font-size: 12px;
    }

    section {
        padding: 100px 25px 50px;
    }
}


==============================
FILE 3: script.js
==============================

const themeToggle = document.getElementById('themeToggle');
const html = document.documentElement;

const savedTheme = localStorage.getItem('theme') || 'dark';
html.setAttribute('data-theme', savedTheme);
themeToggle.textContent = savedTheme === 'dark' ? '☀️' : '🌙';

themeToggle.addEventListener('click', () => {
    const currentTheme = html.getAttribute('data-theme');
    const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
    html.setAttribute('data-theme', newTheme);
    themeToggle.textContent = newTheme === 'dark' ? '☀️' : '🌙';
    localStorage.setItem('theme', newTheme);
});
