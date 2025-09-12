<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Noorjahan Akter - Frontend Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #f8f9fa;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 60px 20px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 20px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #5D3FD3;
            margin-bottom: 20px;
            box-shadow: 0 0 25px rgba(93, 63, 211, 0.5);
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #ff6b6b, #5D3FD3, #4facfe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #d0d0d0;
        }
        
        .typing-text {
            font-size: 1.2rem;
            color: #a991f7;
            margin-bottom: 30px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, #5D3FD3, #8B5CF6);
            color: white;
            text-decoration: none;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(93, 63, 211, 0.3);
        }
        
        .social-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(93, 63, 211, 0.5);
        }
        
        section {
            background: rgba(13, 17, 33, 0.8);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
        }
        
        h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #8B5CF6;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        h2 i {
            color: #5D3FD3;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 30px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .tech-category {
            background: rgba(45, 45, 85, 0.4);
            padding: 20px;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .tech-category:hover {
            transform: translateY(-5px);
            background: rgba(65, 65, 115, 0.4);
        }
        
        .tech-category h4 {
            color: #8B5CF6;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }
        
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .tech-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 70px;
        }
        
        .tech-icon img {
            width: 40px;
            height: 40px;
            object-fit: contain;
            margin-bottom: 8px;
        }
        
        .tech-icon span {
            font-size: 0.8rem;
            text-align: center;
            color: #d0d0d0;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-card {
            background: rgba(45, 45, 85, 0.4);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(65, 65, 115, 0.4);
        }
        
        .stat-card h3 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #8B5CF6;
        }
        
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .project-card {
            background: rgba(45, 45, 85, 0.4);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            background: rgba(65, 65, 115, 0.4);
        }
        
        .project-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            color: #8B5CF6;
            margin-bottom: 10px;
        }
        
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            color: #a0a0a0;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=388&q=80" alt="Noorjahan Akter" class="profile-img">
            <h1>Noorjahan Akter</h1>
            <p class="tagline">Frontend Developer & UI Enthusiast</p>
            <p class="typing-text">Crafting beautiful and functional web experiences</p>
            
            <div class="social-links">
                <a href="https://www.linkedin.com/in/noorjahan-akter-meem30" class="social-btn">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://www.facebook.com/noorjahan.akter.251879" class="social-btn">
                    <i class="fab fa-facebook-f"></i>
                </a>
                <a href="mailto:noorjahanmeem220@gmail.com" class="social-btn">
                    <i class="far fa-envelope"></i>
                </a>
                <a href="https://github.com/noorjahan220" class="social-btn">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </header>
        
        <section class="about">
            <h2><i class="fas fa-user"></i> About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I'm a Frontend Developer based in Dhaka, Bangladesh, passionate about creating beautiful and functional web applications. I enjoy turning complex problems into simple, beautiful, and intuitive designs.</p>
                    <br>
                    <p>🔭 I'm currently building a full-stack e-commerce platform with React & Node.js.</p>
                    <p>🌱 I'm learning advanced MongoDB optimization and TypeScript.</p>
                    <p>👯 I'm looking to collaborate on impactful open-source projects.</p>
                    <p>💬 Ask me about React, JavaScript, and modern web development.</p>
                </div>
                <img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" alt="Coding GIF" width="300">
            </div>
        </section>
        
        <section class="skills">
            <h2><i class="fas fa-laptop-code"></i> Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-category">
                    <h4>Frontend</h4>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">
                            <span>React</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript">
                            <span>JavaScript</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5">
                            <span>HTML5</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3">
                            <span>CSS3</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg" alt="Tailwind CSS">
                            <span>Tailwind</span>
                        </div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h4>Backend</h4>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js">
                            <span>Node.js</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express.js">
                            <span>Express</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB">
                            <span>MongoDB</span>
                        </div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h4>Tools & Platforms</h4>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git">
                            <span>Git</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub">
                            <span>GitHub</span>
                        </div>
                        <div class="tech-icon">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" alt="Figma">
                            <span>Figma</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="github-stats">
            <h2><i class="fas fa-chart-line"></i> GitHub Stats</h2>
            <div class="stats">
                <div class="stat-card">
                    <h3>50+</h3>
                    <p>Repositories</p>
                </div>
                <div class="stat-card">
                    <h3>120+</h3>
                    <p>Commits</p>
                </div>
                <div class="stat-card">
                    <h3>15+</h3>
                    <p>Projects</p>
                </div>
                <div class="stat-card">
                    <h3>8</h3>
                    <p>Technologies</p>
                </div>
            </div>
        </section>
        
        <section class="projects">
            <h2><i class="fas fa-code"></i> Featured Projects</h2>
            <div class="projects">
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80" alt="E-commerce Project" class="project-img">
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>Full-stack e-commerce application with React, Node.js, and MongoDB.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="Task Manager" class="project-img">
                    <div class="project-content">
                        <h3>Task Management App</h3>
                        <p>Productivity application with drag-and-drop functionality and real-time updates.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1531403009284-440f080d1e12?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="Social Media App" class="project-img">
                    <div class="project-content">
                        <h3>Social Media Dashboard</h3>
                        <p>Interactive dashboard with analytics and user engagement metrics.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <footer>
            <p>© 2023 Noorjahan Akter. All Rights Reserved.</p>
            <p>📧 noorjahanmeem220@gmail.com</p>
        </footer>
    </div>

    <script>
        // Simple typing effect
        document.addEventListener('DOMContentLoaded', function() {
            const texts = [
                'Crafting beautiful and functional web experiences',
                'Passionate about clean code and UI/UX',
                'Turning ideas into interactive reality'
            ];
            let textIndex = 0;
            let charIndex = 0;
            const typingElement = document.querySelector('.typing-text');
            let isDeleting = false;
            
            function type() {
                const currentText = texts[textIndex];
                
                if (isDeleting) {
                    typingElement.textContent = currentText.substring(0, charIndex - 1);
                    charIndex--;
                } else {
                    typingElement.textContent = currentText.substring(0, charIndex + 1);
                    charIndex++;
                }
                
                let typeSpeed = isDeleting ? 50 : 100;
                
                if (!isDeleting && charIndex === currentText.length) {
                    typeSpeed = 2000;
                    isDeleting = true;
                } else if (isDeleting && charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                    typeSpeed = 500;
                }
                
                setTimeout(type, typeSpeed);
            }
            
            setTimeout(type, 1000);
        });
    </script>
</body>
</html>
