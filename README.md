# Ex01 Portfolio
## Date: 12.02.2026

## AIM :
To create a Portfolio using HTML and CSS.

## ALGORITHM :
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

## PROGRAM :
## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Deepika | Home</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

<nav>
  <h1 class="logo">Deepika.</h1>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="skills.html">Skills</a></li>
    <li><a href="education.html">Education</a></li>
    <li><a href="toolkit.html">Toolkit</a></li>
  </ul>
</nav>

<section class="hero">
  <img src="photo.jpg" alt="Deepika Profile Photo" class="profile-img">
  <h2>Hi, I'm <span>Deepika</span></h2>
  <p>Building modern web apps as a Full Stack Developer & ML Engineer</p>
  <a href="skills.html"><button>Explore My Work</button></a>
</section>

<footer>
  <p>© 2026 Deeps | Built with ❤️ using HTML & CSS</p>
</footer>

</body>
</html>
```
## style.css
```
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  text-align: center;
}

nav {
  background: #111;
  color: white;
  padding: 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

nav ul li a {
  color: white;
  text-decoration: none;
}

.hero {
  padding: 50px;
}

.profile-img {
  width: 180px;
  border-radius: 50%;
  margin: 20px 0;
}

button {
  padding: 10px 20px;
  background: black;
  color: white;
  border: none;
  cursor: pointer;
}

footer {
  background: #111;
  color: white;
  padding: 10px;
  margin-top: 30px;
}


## about.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>About | Deepika</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

<nav>
  <h1 class="logo">Deepika.</h1>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="skills.html">Skills</a></li>
    <li><a href="education.html">Education</a></li>
    <li><a href="toolkit.html">Toolkit</a></li>
  </ul>
</nav>

<section class="section">
  <img src="photo.jpg" class="profile-img">
  <h2>About Me</h2>
  <p>
    I am an Artificial Intelligence and Data Science student who enjoys building
    modern and user-friendly websites. I am passionate about learning new
    technologies and improving my technical skills every day.
  </p>
  <p>
    I love working on small projects and building real-world applications
    that help me grow as a developer.
  </p>
</section>

<footer>
  <p>© 2026 Deepika</p>
</footer>

</body>
</html>
```
## education.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Education | Deepika</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

<nav>
  <h1 class="logo">Deepika.</h1>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="skills.html">Skills</a></li>
    <li><a href="education.html">Education</a></li>
    <li><a href="toolkit.html">Toolkit</a></li>
  </ul>
</nav>

<section class="section">
  <h2>Education</h2>

  <div class="edu-card">
    <h3>2024 – 2028</h3>
    <p><strong>B.Tech – Artificial Intelligence & Data Science</strong></p>
    <p>Saveetha Engineering College, Chennai</p>
  </div>

  <div class="edu-card">
    <h3>2022 – 2023</h3>
    <p><strong>Government Higher Secondary School</strong></p>
    <p>Bio-Maths Group</p>
  </div>

</section>

<footer>
  <p>© 2026 Deepika</p>
</footer>

</body>
</html>
```
## skills.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Skills | Deepika</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

<nav>
  <h1 class="logo">Deepika.</h1>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="skills.html">Skills</a></li>
    <li><a href="education.html">Education</a></li>
    <li><a href="toolkit.html">Toolkit</a></li>
  </ul>
</nav>

<section class="section">
  <h2>My Skills</h2>

  <div class="card-container">
    <div class="card">Python Programming</div>
    <div class="card">Data Structures</div>
    <div class="card">Machine Learning Basics</div>
    <div class="card">Artificial Intelligence Concepts</div>
    <div class="card">HTML & CSS</div>
    <div class="card">SQL & Database</div>
    <div class="card">Problem Solving</div>
    <div class="card">Communication Skills</div>
  </div>

</section>

<footer>
  <p>© 2026 Deepika</p>
</footer>

</body>
</html>
```
## toolkit.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Toolkit | Deepika</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

<nav>
  <h1 class="logo">Deepika.</h1>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="skills.html">Skills</a></li>
    <li><a href="education.html">Education</a></li>
    <li><a href="toolkit.html">Toolkit</a></li>
  </ul>
</nav>

<section class="section">
  <h2>My Toolkit</h2>

  <div class="card-container">
    <div class="card">VS Code</div>
    <div class="card">Git & GitHub</div>
    <div class="card">Chrome DevTools</div>
    <div class="card">Figma</div>
    <div class="card">Python Libraries</div>
  </div>
</section>

<footer>
  <p>© 2026 Deepika</p>
</footer>

</body>
</html>

```


## OUTPUT :
<img width="1226" height="911" alt="127 0 0 1_5500_index html" src="https://github.com/user-attachments/assets/a81d356f-7f71-4e44-94e3-4f91ef56e350" />
<img width="1226" height="911" alt="127 0 0 1_5500_about html" src="https://github.com/user-attachments/assets/b4012fd8-f7f8-4537-b598-02530d9b8bb4" />
<img width="1226" height="911" alt="127 0 0 1_5500_education html" src="https://github.com/user-attachments/assets/3583577e-0053-49f5-9b7b-52abfb2855e9" />
<img width="1226" height="911" alt="127 0 0 1_5500_skills html" src="https://github.com/user-attachments/assets/e2ab342d-32e4-44e1-b828-a81abdb691d9" />
<img width="1226" height="911" alt="127 0 0 1_5500_toolkit html" src="https://github.com/user-attachments/assets/df2a2226-1f43-4de0-aa79-270ad0d03ad5" />

## RESULT :
The program for creating Portfolio using HTML and CSS is executed successfully.
