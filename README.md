<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areeba Urooj - DevOps & Cloud Enthusiast</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            color: #333;
        }

        /* Navigation */
        .navbar {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
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
            color: #00bcd4;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #666;
            font-weight: 500;
            text-transform: uppercase;
            font-size: 14px;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: #00bcd4;
            transform: translateY(-2px);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 50%;
            background-color: #00bcd4;
            transition: all 0.3s ease;
            transform: translateX(-50%);
        }

        .nav-links a:hover::after {
            width: 100%;
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
        }

        .hero-content {
            flex: 1;
            animation: slideInLeft 1s ease-out;
        }

        .hero-image {
            flex: 1;
            text-align: center;
            animation: slideInRight 1s ease-out;
        }

        .profile-container {
            position: relative;
            display: inline-block;
        }

        .profile-image {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 6px solid #00bcd4;
            box-shadow: 0 20px 40px rgba(0,188,212,0.3);
            transition: transform 0.3s ease;
        }

        .profile-image:hover {
            transform: scale(1.05);
        }

        .cloud-bg {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 400px;
            height: 400px;
            opacity: 0.1;
            z-index: -1;
            background: url('./assets/cloud.png') no-repeat center;
            background-size: contain;
        }

        .greeting {
            font-size: 24px;
            color: #666;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-out 0.5s both;
        }

        .name {
            font-size: 48px;
            font-weight: bold;
            color: #333;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-out 0.7s both;
        }

        .title {
            font-size: 20px;
            color: #00bcd4;
            margin-bottom: 30px;
            font-weight: 500;
            animation: fadeIn 1s ease-out 0.9s both;
        }

        .description {
            font-size: 16px;
            color: #666;
            line-height: 1.6;
            margin-bottom: 40px;
            max-width: 500px;
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
            background-color: #00bcd4;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,188,212,0.3);
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(0,188,212,0.4);
            background-color: #00acc1;
        }

        .social-link i {
            font-size: 22px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            animation: fadeIn 1s ease-out 1.5s both;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 14px;
        }

        .btn-primary {
            background-color: #00bcd4;
            color: white;
            box-shadow: 0 4px 15px rgba(0,188,212,0.3);
        }

        .btn-primary:hover {
            background-color: #00acc1;
            transform: translateY(-2px);
            box-shadow: 0 6px 25px rgba(0,188,212,0.4);
        }

        .btn-secondary {
            background-color: transparent;
            color: #00bcd4;
            border: 2px solid #00bcd4;
        }

        .btn-secondary:hover {
            background-color: #00bcd4;
            color: white;
            transform: translateY(-2px);
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
                font-size: 36px;
            }

            .profile-image {
                width: 250px;
                height: 250px;
            }

            .nav-links {
                gap: 20px;
            }

            .nav-links a {
                font-size: 12px;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
        }

        /* Floating elements for visual interest */
        .floating-shapes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .shape {
            position: absolute;
            background: rgba(0, 188, 212, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        .shape:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }

        .shape:nth-child(2) {
            width: 60px;
            height: 60px;
            top: 70%;
            left: 80%;
            animation-delay: 2s;
        }

        .shape:nth-child(3) {
            width: 100px;
            height: 100px;
            top: 40%;
            left: 90%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
            }
        }
    </style>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="floating-shapes">
        <div class="shape"></div>
        <div class="shape"></div>
        <div class="shape"></div>
    </div>

    <nav class="navbar">
        <div class="nav-container">
            <a href="index.html" class="logo">Areeba Urooj</a>
            <div class="nav-links">
                <a href="about.html">ABOUT</a>
                <a href="projects.html">PROJECTS</a>
                <a href="experience.html">EDUCATION & EXPERIENCE</a>
                <a href="contact.html">CONTACT</a>
            </div>
        </div>
    </nav>

    <main class="hero">
        <div class="hero-content">
            <div class="greeting">Hi, I'm</div>
            <h1 class="name">AREEBA UROOJ</h1>
            <div class="title">DevOps & Cloud Enthusiast</div>
            <p class="description">
                Passionate about cloud technologies, automation, and building scalable infrastructure. 
                I love turning complex problems into elegant solutions through code and cutting-edge technology.
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
                <a href="projects.html" class="btn btn-primary">View My Work</a>
                <a href="contact.html" class="btn btn-secondary">Get In Touch</a>
            </div>
        </div>

        <div class="hero-image">
            <div class="profile-container">
                <div class="cloud-bg"></div>
                <img src="./assets/profile.jpg" alt="Areeba Urooj" class="profile-image">
            </div>
        </div>
    </main>
</body>
</html>
