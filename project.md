
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        header {
            background: #333;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #ff6347;
        }

        section {
            padding: 2rem 0;
            text-align: center;
        }

        .project {
            margin: 2rem auto;
            text-align: left;
            max-width: 800px;
        }

        .project img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 4px;
            padding: 5px;
        }

        footer {
            background: #333;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
            position: relative;
            bottom: 0;
            width: 100%;
        }

        form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        form label {
            margin-top: 1rem;
        }

        form input, form textarea {
            margin-top: 0.5rem;
            padding: 0.5rem;
            width: 80%;
            max-width: 400px;
        }

        form button {
            margin-top: 1rem;
            padding: 0.5rem 1rem;
            background: #333;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background 0.3s;
        }

        form button:hover {
            background: #ff6347;
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
    </header>

    <section id="about">
        <h1>About Me</h1>
        <p>Hello! I'm a final year engineering student specializing in software development. I have a passion for coding and problem-solving.</p>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        <div class="project">
        <div class="project">
            <h3>Project 1: Online Learning Platform</h3>
            <img src="https://via.placeholder.com/800x400" alt="Online Learning Platform">
            <p>An online learning platform that provides educational courses and resources. It includes user authentication, course enrollment, and progress tracking.</p>
        </div>
        <div class="project">
            <h3>Project 2: Financial Tracking App</h3>
            <img src="https://via.placeholder.com/800x400" alt="Financial Tracking App">
            <p>A financial tracking application that helps users to manage their expenses and incomes. It includes features like budget planning, expense categorization, and financial reports.</p>
        </div>
        <div class="project">
            <h3>Project 3: Real-time Chat Application</h3>
            <img src="https://via.placeholder.com/800x400" alt="Real-time Chat Application">
            <p>A real-time chat application that allows users to communicate instantly. It includes features like group chats, direct messages, and media sharing.</p>
        </div>
        <div class="project">
            <h3>Project 4: Health and Fitness Tracker</h3>
            <img src="https://via.placeholder.com/800x400" alt="Health and Fitness Tracker">
            <p>A health and fitness tracker application that helps users to monitor their fitness activities and health metrics. It includes features like workout tracking, diet planning, and progress reports.</p>
        </div>
    </section>

    <section id="skills">
        <h2>Skills</h2>
        <ul>
            <li>Programming Languages: JavaScript, Python, Java</li>
            <li>Web Development: HTML, CSS, React</li>
            <li>Tools: Git, Docker</li>
        </ul>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <form id="contact-form">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            
            <label for="message">Message:</label>
            <textarea id="message" name="message" required></textarea>
            
            <button type="submit">Send</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Final Year Engineering Student</p>
    </footer>

    <script>
        // Smooth scrolling to sections
        document.querySelectorAll('nav ul li a').forEach(anchor => {
            anchor.addEventListener('click', function(event) {
                event.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Form validation and submission handling
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            let name = document.getElementById('name').value.trim();
            let email = document.getElementById('email').value.trim();
            let message = document.getElementById('message').value.trim();

            if (name === '' || email === '' || message === '') {
                alert('Please fill in all fields.');
                return;
            }

            if (!validateEmail(email)) {
                alert('Please enter a valid email address.');
                return;
            }

            alert('Thank you for your message, ' + name + '! I will get back to you soon.');
            // Clear the form
            document.getElementById('contact-form').reset();
        });

        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }
    </script>
</body>
</html>
