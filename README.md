
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .hero-bg {
            background: linear-gradient(135deg, #3b82f6, #a855f7);
        }
        .card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }
        .nav-link {
            transition: color 0.3s ease;
        }
        .nav-link:hover {
            color: #fef08a;
        }
        .btn-cta {
            transition: background-color 0.3s ease, transform 0.3s ease;
        }
        .btn-cta:hover {
            background-color: #7c3aed;
            transform: scale(1.05);
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Hero Section -->
    <section class="hero-bg text-white py-20">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-5xl font-bold mb-4 animate-fade-in">Welcome to My Portfolio</h1>
            <p class="text-xl mb-6">I'm a passionate developer crafting beautiful and functional web experiences.</p>
            <a href="#contact" class="btn-cta bg-purple-600 text-white px-6 py-3 rounded-full font-semibold">Get in Touch</a>
        </div>
    </section>

    <!-- Header -->
    <header class="bg-white shadow sticky top-0 z-10">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold text-blue-600">My Portfolio</h1>
            <nav>
                <ul class="flex space-x-6">
                    <li><a href="#about" class="nav-link text-gray-700 font-semibold">About</a></li>
                    <li><a href="#projects" class="nav-link text-gray-700 font-semibold">Projects</a></li>
                    <li><a href="#contact" class="nav-link text-gray-700 font-semibold">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- About Section -->
    <section id="about" class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-8">About Me</h2>
            <div class="max-w-2xl mx-auto text-center">
                <p class="text-lg text-gray-600 leading-relaxed">
                    I'm a creative developer with a passion for building responsive, user-friendly websites. 
                    With expertise in modern web technologies, I love turning ideas into reality through clean code and stunning designs.
                </p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-8">My Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="card bg-gray-50 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Task Manager</h3>
                    <p class="text-gray-600">A sleek web app built with React and Tailwind CSS for seamless task management.</p>
                </div>
                <div class="card bg-gray-50 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">E-Commerce Platform</h3>
                    <p class="text-gray-600">A fully functional online store with a custom CMS and secure payment integration.</p>
                </div>
                <div class="card bg-gray-50 p-6 rounded-lg shadow-lg">
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Portfolio Website</h3>
                    <p class="text-gray-600">A showcase of my skills with a modern, responsive design.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-8">Get in Touch</h2>
            <div class="max-w-lg mx-auto">
                <div class="mb-6">
                    <label for="name" class="block text-gray-700 font-semibold mb-2">Name</label>
                    <input type="text" id="name" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="Your Name">
                </div>
                <div class="mb-6">
                    <label for="email" class="block text-gray-700 font-semibold mb-2">Email</label>
                    <input type="email" id="email" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="Your Email">
                </div>
                <div class="mb-6">
                    <label for="message" class="block text-gray-700 font-semibold mb-2">Message</label>
                    <textarea id="message" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-600" rows="5" placeholder="Your Message"></textarea>
                </div>
                <button onclick="submitForm()" class="btn-cta w-full bg-blue-600 text-white p-3 rounded-lg font-semibold hover:bg-blue-700">Send Message</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-4 text-center">
            <p class="text-sm">&copy; 2025 My Portfolio. Crafted with passion.</p>
        </div>
    </footer>

    <script>
        function submitForm() {
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            if (name && email && message) {
                alert('Thank you for your message! I’ll get back to you soon.');
                document.getElementById('name').value = '';
                document.getElementById('email').value = '';
                document.getElementById('message').value = '';
            } else {
                alert('Please fill out all fields.');
            }
        }
    </script>
</body>
</html>
