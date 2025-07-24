<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shivam Maurya | CSE Student & Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Mono:wght@300;400;500&display=swap');
        
        :root {
            --primary: #2563eb;
            --secondary: #7e22ce;
            --dark: #0f172a;
            --light: #f8fafc;
            --accent: #06b6d4;
            --card-bg: rgba(255, 255, 255, 0.08);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, var(--dark), #1e293b);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 4rem 0 3rem;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        .header-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at top right, var(--secondary), transparent 40%),
                        radial-gradient(circle at bottom left, var(--primary), transparent 40%);
            opacity: 0.2;
            z-index: 1;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(90deg, var(--primary), var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(37, 99, 235, 0.3);
            animation: gradientShift 6s infinite alternate;
        }
        
        h2 {
            font-size: 1.8rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }
        
        h3 {
            font-size: 1.4rem;
            color: #94a3b8;
            max-width: 800px;
            margin: 0 auto 1.5rem;
            font-weight: 400;
            line-height: 1.8;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-top: 1rem;
            background: var(--card-bg);
            display: inline-block;
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .profile-views {
            display: inline-block;
            background: var(--card-bg);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            margin: 1.5rem 0;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Section Styles */
        section {
            margin-bottom: 3rem;
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }
        
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }
        
        .card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 1.5rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
            backdrop-filter: blur(10px);
        }
        
        .card:hover {
            transform: translateY(-5px);
            border-color: rgba(6, 182, 212, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .card h4 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--accent);
            display: flex;
            align-items: center;
        }
        
        .card h4 i {
            margin-right: 0.8rem;
            font-size: 1.2rem;
        }
        
        .card ul {
            padding-left: 1.5rem;
        }
        
        .card li {
            margin-bottom: 0.7rem;
            position: relative;
        }
        
        .card li::before {
            content: '▹';
            position: absolute;
            left: -1.3rem;
            color: var(--accent);
        }
        
        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .stat-card h3 {
            font-size: 2.5rem;
            margin: 0.5rem 0;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-card p {
            color: #94a3b8;
        }
        
        /* Tech Stack */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 1.5rem;
        }
        
        .tech-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 90px;
            transition: var(--transition);
        }
        
        .tech-item:hover {
            transform: translateY(-5px);
        }
        
        .tech-icon {
            width: 70px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--card-bg);
            border-radius: 50%;
            margin-bottom: 0.8rem;
            font-size: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Contact Section */
        .contact-badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .badge {
            display: inline-flex;
            align-items: center;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            background: var(--card-bg);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-decoration: none;
            color: var(--light);
            font-weight: 500;
            transition: var(--transition);
            backdrop-filter: blur(10px);
        }
        
        .badge:hover {
            transform: translateY(-3px);
            background: rgba(37, 99, 235, 0.2);
            border-color: rgba(37, 99, 235, 0.3);
        }
        
        .badge i {
            margin-right: 0.7rem;
            font-size: 1.2rem;
        }
        
        /* Snake Animation Container */
        .snake-container {
            margin: 3rem auto;
            max-width: 800px;
            background: var(--card-bg);
            border-radius: 15px;
            padding: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
            color: #94a3b8;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Animations */
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }
        
        .fade-in {
            animation: fadeIn 1s ease-out forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .delay-1 { animation-delay: 0.1s; }
        .delay-2 { animation-delay: 0.2s; }
        .delay-3 { animation-delay: 0.3s; }
        .delay-4 { animation-delay: 0.4s; }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            h2 { font-size: 1.5rem; }
            h3 { font-size: 1.1rem; }
            .container { padding: 1.5rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="header-bg"></div>
            <div class="header-content">
                <h1>Hi 👋, I'm Shivam Maurya</h1>
                <h2>Computer Science & Engineering Student</h2>
                <h3>A passionate 2nd-year B.Tech student exploring the world of web development and competitive programming. I believe in <em>code + consciousness</em> — blending technical growth with spiritual values.</h3>
                <div class="profile-views fade-in">
                    <i class="fas fa-eye"></i> <span id="viewCount">0</span> Profile Views
                </div>
                <div class="tagline fade-in delay-1">
                    <i class="fas fa-code"></i> Coding with Consciousness
                </div>
            </div>
        </header>

        <main>
            <!-- Current Work Section -->
            <section class="fade-in delay-1">
                <h2 class="section-title"><i class="fas fa-tasks"></i> Current Work</h2>
                <div class="cards">
                    <div class="card">
                        <h4><i class="fab fa-cuttlefish"></i> C/C++ Programming</h4>
                        <ul>
                            <li>Learning C++ and improving core C programming skills</li>
                            <li>Building responsive websites using HTML and CSS</li>
                            <li>Exploring DSA and problem-solving techniques</li>
                            <li>Developing personal projects to improve my skills</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fas fa-laptop-code"></i> Web Development</h4>
                        <ul>
                            <li>Creating responsive and accessible websites</li>
                            <li>Implementing modern CSS techniques</li>
                            <li>Learning JavaScript for interactive elements</li>
                            <li>Building portfolio projects to showcase skills</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fas fa-brain"></i> Problem Solving</h4>
                        <ul>
                            <li>Practicing Data Structures & Algorithms daily</li>
                            <li>Solving problems on coding platforms</li>
                            <li>Participating in coding contests</li>
                            <li>Developing algorithmic thinking skills</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Currently Learning Section -->
            <section class="fade-in delay-2">
                <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Currently Learning</h2>
                <div class="cards">
                    <div class="card">
                        <h4><i class="fab fa-cuttlefish"></i> Advanced C++</h4>
                        <ul>
                            <li>Object-Oriented Programming principles</li>
                            <li>STL (Standard Template Library)</li>
                            <li>Memory management and optimization</li>
                            <li>Modern C++ features (C++11/14/17)</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fab fa-css3-alt"></i> Frontend Design</h4>
                        <ul>
                            <li>Advanced CSS techniques and animations</li>
                            <li>Responsive design principles</li>
                            <li>CSS frameworks (Bootstrap, Tailwind)</li>
                            <li>Design systems and UI/UX fundamentals</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fab fa-git-alt"></i> DevOps & Tools</h4>
                        <ul>
                            <li>Git & GitHub for version control</li>
                            <li>Collaboration workflows</li>
                            <li>Open-source contribution practices</li>
                            <li>Basic DevOps principles</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Collaboration Section -->
            <section class="fade-in delay-3">
                <h2 class="section-title"><i class="fas fa-hands-helping"></i> Collaboration</h2>
                <div class="cards">
                    <div class="card">
                        <h4><i class="fas fa-handshake"></i> Looking to Collaborate On</h4>
                        <ul>
                            <li>Beginner-friendly open source projects</li>
                            <li>Static websites or mini-apps</li>
                            <li>Web development-based student projects</li>
                            <li>Communities that support learning and growth</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fas fa-question-circle"></i> Looking for Help With</h4>
                        <ul>
                            <li>Advanced C++ concepts (STL, OOP)</li>
                            <li>Improving CSS designs and animations</li>
                            <li>Git and GitHub workflow for collaboration</li>
                            <li>Open-source contribution best practices</li>
                        </ul>
                    </div>
                    <div class="card">
                        <h4><i class="fas fa-comments"></i> Ask Me About</h4>
                        <ul>
                            <li>Starting with C programming as a beginner</li>
                            <li>Basics of HTML/CSS and creating webpages</li>
                            <li>Learning code while being Krishna conscious</li>
                            <li>Balancing college, bhakti, and coding</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Tech Stack Section -->
            <section class="fade-in delay-4">
                <h2 class="section-title"><i class="fas fa-laptop-code"></i> Tech Stack</h2>
                <div class="tech-stack">
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-html5" style="color: #e34f26;"></i>
                        </div>
                        <span>HTML5</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-css3-alt" style="color: #264de4;"></i>
                        </div>
                        <span>CSS3</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-cuttlefish" style="color: #004482;"></i>
                        </div>
                        <span>C</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-cuttlefish" style="color: #004482;"></i>
                            <span style="position: absolute; margin-top: 5px;">++</span>
                        </div>
                        <span>C++</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-git-alt" style="color: #f34f29;"></i>
                        </div>
                        <span>Git</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-github" style="color: #ffffff;"></i>
                        </div>
                        <span>GitHub</span>
                    </div>
                </div>
            </section>

            <!-- Stats Section -->
            <section>
                <h2 class="section-title"><i class="fas fa-chart-line"></i> GitHub Stats</h2>
                <div class="stats">
                    <div class="stat-card fade-in">
                        <i class="fas fa-code-branch fa-2x"></i>
                        <h3>15+</h3>
                        <p>Projects</p>
                    </div>
                    <div class="stat-card fade-in delay-1">
                        <i class="fas fa-code fa-2x"></i>
                        <h3>1000+</h3>
                        <p>Lines of Code</p>
                    </div>
                    <div class="stat-card fade-in delay-2">
                        <i class="fas fa-medal fa-2x"></i>
                        <h3>5+</h3>
                        <p>Hackathons</p>
                    </div>
                    <div class="stat-card fade-in delay-3">
                        <i class="fas fa-book fa-2x"></i>
                        <h3>10+</h3>
                        <p>Contributions</p>
                    </div>
                </div>
            </section>

            <!-- Contact Section -->
            <section>
                <h2 class="section-title"><i class="fas fa-envelope"></i> Connect With Me</h2>
                <div class="contact-badges">
                    <a href="mailto:shivam2024maurya@gmail.com" class="badge fade-in">
                        <i class="fas fa-envelope"></i> Email
                    </a>
                    <a href="https://www.linkedin.com/in/shivam-maurya-66b539339" target="_blank" class="badge fade-in delay-1">
                        <i class="fab fa-linkedin-in"></i> LinkedIn
                    </a>
                    <a href="https://github.com/Shivam-Maurya-2024" target="_blank" class="badge fade-in delay-2">
                        <i class="fab fa-github"></i> GitHub
                    </a>
                </div>
            </section>

            <!-- Snake Animation -->
            <section class="snake-container fade-in delay-4">
                <img src="https://profile-readme-generator.com/assets/snake.svg" alt="Snake animation" style="width: 100%;">
            </section>
        </main>

        <!-- Fun Fact Section -->
        <section class="fade-in">
            <h2 class="section-title"><i class="fas fa-lightbulb"><