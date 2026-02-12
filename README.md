# Ex01 Portfolio
## Date: 12.02.2026

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepika Ramajayam | AI & Data Science Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        
        :root {
            --primary-color: #6C63FF; 
            --secondary-color: #00d4ff; 
            --bg-dark: #0f172a;
            --bg-card: #1e293b;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --gradient: linear-googleapis(135deg, #6C63FF, #00d4ff);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            position: sticky;
            top: 0;
            background-color: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            font-size: 1rem;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary-color);
        }

        .hero {
            height: 90vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            background: radial-gradient(circle at 50% 50%, rgba(108, 99, 255, 0.1) 0%, rgba(15, 23, 42, 1) 70%);
        }

        .hero h3 {
            font-size: 1.5rem;
            color: var(--secondary-color);
            margin-bottom: 10px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        .hero span {
            color: var(--primary-color);
        }

        .hero p {
            max-width: 600px;
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        .btn {
            padding: 12px 30px;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 50px;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
            display: inline-block;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(108, 99, 255, 0.3);
        }

        section {
            padding: 80px 8%;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 80px;
            height: 4px;
            background: var(--primary-color);
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        /* --- Education & Internship (Cards) --- */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background-color: var(--bg-card);
            padding: 30px;
            border-radius: 15px;
            transition: transform 0.3s;
            border: 1px solid rgba(255,255,255,0.05);
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
        }

        .card h3 {
            margin-bottom: 10px;
            color: var(--text-main);
        }

        .card .subtitle {
            color: var(--secondary-color);
            font-size: 0.9rem;
            margin-bottom: 15px;
            display: block;
            font-weight: 600;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .card-icon {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }

        .skill-tag {
            background: rgba(255, 255, 255, 0.05);
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: 500;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-tag i {
            color: var(--secondary-color);
        }

        .skill-tag:hover {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        .skill-tag:hover i {
            color: white;
        }

        .project-showcase {
            background: linear-gradient(rgba(30, 41, 59, 0.9), rgba(30, 41, 59, 0.9)), url('https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .project-content h3 {
            color: var(--secondary-color);
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .project-tech {
            display: flex;
            gap: 10px;
            margin: 20px 0;
        }

        .tech-badge {
            background: rgba(108, 99, 255, 0.2);
            color: #b5b0ff;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
        }

        .project-list li {
            margin-bottom: 10px;
            color: var(--text-muted);
            list-style: none;
            position: relative;
            padding-left: 20px;
        }

        .project-list li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: var(--primary-color);
        }

       
        .contact-box {
            background-color: var(--bg-card);
            text-align: center;
            padding: 50px;
            border-radius: 20px;
            max-width: 800px;
            margin: 0 auto;
        }

        .email-link {
            font-size: 1.2rem;
            color: var(--secondary-color);
            margin-top: 20px;
            display: inline-block;
            border-bottom: 2px solid transparent;
            transition: 0.3s;
        }

        .email-link:hover {
            border-bottom: 2px solid var(--secondary-color);
        }

        footer {
            background-color: #0b1120;
            padding: 40px 8%;
            text-align: center;
            border-top: 1px solid rgba(255,255,255,0.05);
            margin-top: 60px;
        }

        .footer-content h2 {
            font-size: 1.5rem;
            margin-bottom: 5px;
            color: white;
        }

        .footer-info {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 20px;
        }

        .social-icons {
            margin-top: 20px;
        }

        .social-icons a {
            font-size: 1.2rem;
            color: white;
            margin: 0 10px;
            transition: 0.3s;
        }

        .social-icons a:hover {
            color: var(--primary-color);
        }

        
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .nav-links { display: none; } 
            section { padding: 60px 5%; }
        }
    </style>
</head>
<body>


    <nav>
        <div class="logo">Deepika.AI</div>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#experience">Internship</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>


    <section class="hero">
        <h3>Hello, I'm</h3>
        <h1>Deepika Ramajayam</h1>
        <p>AI & Data Science Student | 2nd Year @ Saveetha Engineering College</p>
        <a href="#projects" class="btn">View My Work</a>
    </section>

    <section id="about">
        <h2 class="section-title">Education</h2>
        <div class="grid-container">
           
            <div class="card">
                <div class="card-icon"><i class="fa-solid fa-graduation-cap"></i></div>
                <h3>B.E. AI & Data Science</h3>
                <span class="subtitle">Saveetha Engineering College | 2022 - 2026</span>
                <p>Currently in 2nd Year.</p>
                <p style="margin-top: 10px; font-size: 0.85rem; color: #94a3b8;">
                    Focusing on core AI concepts, Data Structures, and Programming.
                </p>
            </div>
            
            <div class="card">
                <div class="card-icon"><i class="fa-solid fa-school"></i></div>
                <h3>Higher Secondary</h3>
                <span class="subtitle">Govt. Higher Secondary School</span>
                <p>Tiruvannamalai</p>
                <p style="margin-top: 10px; font-size: 0.85rem; color: #94a3b8;">
                    Completed schooling with a focus on Mathematics and Science.
                </p>
            </div>
        </div>
    </section>

    
    <section id="skills">
        <h2 class="section-title">Technical Skills</h2>
        <div class="skills-container">
            <div class="skill-tag"><i class="fa-brands fa-html5"></i> HTML5</div>
            <div class="skill-tag"><i class="fa-brands fa-css3-alt"></i> CSS3</div>
            <div class="skill-tag"><i class="fa-brands fa-js"></i> JavaScript</div>
            <div class="skill-tag"><i class="fa-brands fa-react"></i> React JS</div>
            <div class="skill-tag"><i class="fa-brands fa-java"></i> Java</div>
            <div class="skill-tag"><i class="fa-brands fa-python"></i> Python</div>
            <div class="skill-tag"><i class="fa-solid fa-c"></i> C Programming</div>
            <div class="skill-tag"><i class="fa-brands fa-github"></i> GitHub</div>
            <div class="skill-tag"><i class="fa-brands fa-git-alt"></i> Git</div>
            <div class="skill-tag"><i class="fa-solid fa-code"></i> VS Code</div>
        </div>
    </section>

    
    <section id="experience">
        <h2 class="section-title">Internship Experience</h2>
        <div class="card" style="border-left: 4px solid var(--secondary-color);">
            <h3>AI Intern</h3>
            <span class="subtitle">Retch Solution Pvt Ltd</span>
            <p>Gained hands-on experience in Artificial Intelligence concepts and real-world applications. Collaborated with senior developers to understand AI model integration and data processing workflows.</p>
        </div>
    </section>

    
    <section id="projects">
        <h2 class="section-title">Featured Project</h2>
        <div class="project-showcase">
            <div class="project-content">
                <h3>Medical Advisor Bot</h3>
                <p>An intelligent health assistant designed to bridge the gap between preliminary symptoms and medical advice.</p>
                
                <div class="project-tech">
                    <span class="tech-badge">Python</span>
                    <span class="tech-badge">NLP</span>
                    <span class="tech-badge">React</span>
                </div>

                <ul class="project-list">
                    <li><strong>Symptom Analysis:</strong> Users can input their symptoms in natural language.</li>
                    <li><strong>Recommendation Engine:</strong> Provides first-aid suggestions and home remedies for minor issues.</li>
                    <li><strong>Doctor Retrieval:</strong> Suggests specialized doctors based on the severity of symptoms.</li>
                    <li><strong>Goal:</strong> To reduce panic and provide immediate, reliable health information.</li>
                </ul>
            </div>
        </div>
    </section>

    
    <section id="contact">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-box">
            <p>I am currently open to internships and collaborative projects in AI and Web Development.</p>
            <a href="mailto:deepikaramajayam@gmail.com" class="email-link">
                <i class="fa-solid fa-envelope"></i> deepikaramajayam@gmail.com
            </a>
        </div>
    </section>

    
    <footer>
        <div class="footer-content">
            <h2>Deepika Ramajayam</h2>
            <div class="footer-info">
                <p>Department of AI & Data Science (AIDS)</p>
                <p>2nd Year Student | Saveetha Engineering College</p>
            </div>
            <div class="social-icons">
               
                <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                <a href="#"><i class="fa-brands fa-github"></i></a>
                <a href="mailto:deepikaramajayam@gmail.com"><i class="fa-solid fa-envelope"></i></a>
            </div>
            <p style="margin-top: 20px; font-size: 0.8rem; opacity: 0.6;">&copy; 2024 Deepika R. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>

## OUTPUT

![m5](https://github.com/user-attachments/assets/3874b6e6-d753-4f4c-a9d0-e8ef7de4c9a4)

##![m1](https://github.com/user-attachments/assets/23153038-1d26-4f2c-90d0-e5be7ce16ecd)

![m2](https://github.com/user-attachments/assets/c0ef97f9-c50c-4e5b-8ea2-3ef78a8e6909)

![m3](https://github.com/user-attachments/assets/c797b16c-6bbc-4ead-b149-931121ad174c)

![m4](https://github.com/user-attachments/assets/ab721431-4c76-426f-b2c6-5bc1822a432d)

## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
