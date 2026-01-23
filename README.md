<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areeba Urooj - AI Automation & DevOps</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #fff;
            overflow-x: hidden;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }

        /* Navigation */
        .navbar {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #fff;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: #00ff88;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 500;
            text-transform: uppercase;
            font-size: 14px;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: #00ff88;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            min-height: 100vh;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            gap: 60px;
            position: relative;
            z-index: 1;
        }

        .hero-content {
            flex: 1;
            animation: slideInLeft 1s ease-out;
        }

        .hero-image {
            flex: 1;
            text-align: center;
            animation: slideInRight 1s ease-out;
            position: relative;
        }

        .profile-container {
            position: relative;
            display: inline-block;
        }

        .profile-image {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #00ff88;
            box-shadow: 0 20px 60px rgba(0, 255, 136, 0.3);
            transition: transform 0.3s ease;
        }

        .profile-image:hover {
            transform: scale(1.05) rotate(2deg);
        }

        /* Glowing effect behind profile */
        .glow-effect {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(0, 255, 136, 0.3) 0%, transparent 70%);
            border-radius: 50%;
            animation: pulse 3s ease-in-out infinite;
            z-index: -1;
        }

        @keyframes pulse {
            0%, 100% {
                transform: translate(-50%, -50%) scale(1);
                opacity: 0.5;
            }
            50% {
                transform: translate(-50%, -50%) scale(1.1);
                opacity: 0.8;
            }
        }

        .greeting {
            font-size: 20px;
            color: #00ff88;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-out 0.5s both;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
        }

        .name {
            font-size: 56px;
            font-weight: bold;
            color: #fff;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-out 0.7s both;
            line-height: 1.2;
        }

        .title-wrapper {
            margin-bottom: 30px;
            animation: fadeIn 1s ease-out 0.9s both;
        }

        .title {
            font-size: 24px;
            color: #fff;
            font-weight: 500;
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 16px;
            color: rgba(255, 255, 255, 0.7);
            font-style: italic;
        }

        .tech-tags {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 30px;
            animation: fadeIn 1s ease-out 1.1s both;
        }

        .tag {
            background: rgba(0, 255, 136, 0.2);
            border: 1px solid #00ff88;
            color: #00ff88;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
        }

        .tag:hover {
            background: #00ff88;
            color: #667eea;
            transform: translateY(-2px);
        }

        .description {
            font-size: 16px;
            color: rgba(255, 255, 255, 0.9);
            line-height: 1.8;
            margin-bottom: 40px;
            max-width: 550px;
            animation: fadeIn 1s ease-out 1.1s both;
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin-bottom: 40px;
            animation: fadeIn 1s ease-out 1.3s both;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 50%;
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            transform: translateY(-5px);
            background: #00ff88;
            border-color: #00ff88;
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.4);
        }

        .social-link i {
            font-size: 20px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            animation: fadeIn 1s ease-out 1.5s both;
        }

        .btn {
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 14px;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .btn:hover::before {
            width: 300px;
            height: 300px;
        }

        .btn span {
            position: relative;
            z-index: 1;
        }

        .btn-primary {
            background: #00ff88;
            color: #667eea;
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0, 255, 136, 0.5);
        }

        .btn-secondary {
            background: transparent;
            color: #fff;
            border: 2px solid #fff;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-3px);
        }

        /* Animations */
        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
                gap: 40px;
                padding-top: 100px;
            }

            .hero-content {
                order: 2;
            }

            .hero-image {
                order: 1;
            }

            .name {
                font-size: 40px;
            }

            .profile-image {
                width: 250px;
                height: 250px;
            }

            .nav-links {
                gap: 15px;
            }

            .nav-links a {
                font-size: 11px;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                text-align: center;
            }

            .tech-tags {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- Animated particles -->
    <div class="particles" id="particles"></div>

    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="index.html" class="logo">
                <i class="fas fa-robot"></i>
                Areeba Urooj
            </a>
            <div class="nav-links">
                <a href="about.html">About</a>
                <a href="projects.html">Projects</a>
                <a href="experience.html">Experience</a>
                <a href="contact.html">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <main class="hero">
        <div class="hero-content">
            <div class="greeting">👋 Hello, I'm</div>
            <h1 class="name">AREEBA UROOJ</h1>
            <div class="title-wrapper">
                <div class="title">AI Automation Engineer</div>
                <div class="subtitle">DevOps Background → AI-Powered Solutions</div>
            </div>

            <div class="tech-tags">
                <span class="tag">AI Automation</span>
                <span class="tag">DevOps</span>
                <span class="tag">Cloud</span>
                <span class="tag">MLOps</span>
            </div>
            
            <p class="description">
                Started my journey in DevOps and cloud infrastructure, but discovered my passion for AI automation. 
                Now I build intelligent systems that combine the best of both worlds—scalable infrastructure 
                powered by cutting-edge AI to automate complex workflows and solve real-world problems.
            </p>
            
            <div class="social-links">
                <a href="https://linkedin.com/in/areeba-urooj-8a1606279/" target="_blank" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://github.com/Areeba-Urooj" target="_blank" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://twitter.com/your_username" target="_blank" class="social-link">
                    <i class="fab fa-x-twitter"></i>
                </a>
            </div>

            <div class="cta-buttons">
                <a href="projects.html" class="btn btn-primary">
                    <span>View AI Projects</span>
                </a>
                <a href="contact.html" class="btn btn-secondary">
                    <span>Let's Collaborate</span>
                </a>
            </div>
        </div>

        <div class="hero-image">
            <div class="profile-container">
                <div class="glow-effect"></div>
                <img src="./assets/profile.jpg" alt="Areeba Urooj" class="profile-image">
            </div>
        </div>
    </main>

    <script>
        // Create animated particles
        const particlesContainer = document.getElementById('particles');
        const particleCount = 50;

        for (let i = 0; i < particleCount; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 15 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
            particlesContainer.appendChild(particle);
        }
    </script>
</body>
</html>
