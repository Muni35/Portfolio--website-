# Portfolio--website-
My portfolio 
<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
            scroll-behavior: smooth;
        }
        header {
            background: #0073e6;
            color: white;
            padding: 20px;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        nav ul {
            list-style: none;
            padding: 0;
            text-align: center;
        }
        nav ul li {
            display: inline;
            margin: 0 15px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #ffcc00;
        }
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('https://via.placeholder.com/1500x800') no-repeat center center/cover;
            color: white;
            padding: 20px;
        }
        .hero h1 {
            font-size: 3rem;
            margin: 0;
        }
        .hero p {
            font-size: 1.2rem;
        }
        .btn {
            display: inline-block;
            background: #ffcc00;
            color: black;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background 0.3s;
        }
        .btn:hover {
            background: #e6b800;
        }
        section {
            padding: 60px 20px;
            margin-top: 60px;
            text-align: center;
            background: white;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }
        .visible {
            opacity: 1;
            transform: translateY(0);
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #0073e6;
            color: white;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header><section class="hero">
    <div>
        <h1>Hi, I'm Munira Alinur Sheikh</h1>
        <p>Software Developer | Tech Enthusiast | Innovator</p>
        <a href="#projects" class="btn">View My Work</a>
    </div>
</section>

<section id="about" class="fade-in">
    <h2>About Me</h2>
    <p>Write a brief introduction about yourself here.</p>
</section>

<section id="projects" class="fade-in">
    <h2>Projects</h2>
    <div class="project-list" id="projectGallery">
        <!-- Projects will be inserted dynamically here -->
    </div>
</section>

<section id="skills" class="fade-in">
    <h2>Skills</h2>
    <p>List your skills and technologies you work with.</p>
</section>

<section id="contact" class="fade-in">
    <h2>Contact</h2>
    <p>Provide your contact details or a form for messages.</p>
</section>

<footer>
    <p>&copy; 2025 Munira Alinur Sheikh. All Rights Reserved.</p>
</footer>

<script>
    document.addEventListener("DOMContentLoaded", function () {
        const sections = document.querySelectorAll("section");
        
        function revealSections() {
            sections.forEach(section => {
                const rect = section.getBoundingClientRect();
                if (rect.top < window.innerHeight * 0.8) {
                    section.classList.add("visible");
                }
            });
        }
        
        revealSections();
        window.addEventListener("scroll", revealSections);
    });
</script>

</body>
</html>and h