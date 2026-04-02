<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areeba Urooj - AI Automation & DevOps</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,500;1,400;1,500&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'DM Sans', sans-serif;
            background: #faf9f7;
            min-height: 100vh;
            color: #1a1814;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        /* Navigation */
        .navbar {
            background: rgba(250, 249, 247, 0.96);
            backdrop-filter: blur(10px);
            padding: 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid #e4e1db;
            height: 66px;
            display: flex;
            align-items: center;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 52px;
            width: 100%;
        }

        .logo {
            font-family: 'Lora', serif;
            font-size: 1.15rem;
            font-weight: 500;
            color: #1a1814;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0;
        }

        .logo span {
            color: #1a6b3c;
        }

        .logo i { display: none; }

        .nav-links {
            display: flex;
            gap: 38px;
        }

        .nav-links a {
            text-decoration: none;
            color: #8a8680;
            font-weight: 500;
            text-transform: uppercase;
            font-size: 0.8rem;
            letter-spacing: 0.07em;
            transition: color 0.2s;
            position: relative;
            padding-bottom: 3px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            left: 0; bottom: 0;
            width: 0; height: 1.5px;
            background: #1a6b3c;
            transition: width 0.25s ease;
        }

        .nav-links a:hover { color: #1a1814; }
        .nav-links a:hover::after { width: 100%; }

        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            min-height: 100vh;
            max-width: 1200px;
            margin: 0 auto;
            padding: 66px 52px 0;
            gap: 80px;
            position: relative;
            z-index: 1;
        }

        .hero-content {
            flex: 1;
            animation: slideInLeft 0.8s ease-out;
        }

        .hero-image {
            flex: 0 0 auto;
            text-align: center;
            animation: slideInRight 0.8s ease-out;
            position: relative;
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
            border: 2px solid #e4e1db;
            box-shadow: 0 20px 60px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: block;
        }

        .profile-image:hover {
            transform: scale(1.03);
            box-shadow: 0 24px 70px rgba(26,107,60,0.12);
            border-color: #1a6b3c;
        }

        /* no glow on light theme */
        .glow-effect { display: none; }

        .greeting {
            font-size: 0.75rem;
            color: #1a6b3c;
            margin-bottom: 16px;
            text-transform: uppercase;
            letter-spacing: 0.14em;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 10px;
            animation: fadeIn 0.8s ease-out 0.3s both;
        }

        .greeting::before {
            content: '';
            display: inline-block;
            width: 28px;
            height: 1.5px;
            background: #1a6b3c;
        }

        .name {
            font-family: 'Lora', serif;
            font-size: clamp(2.8rem, 4.5vw, 4rem);
            font-weight: 500;
            color: #1a1814;
            margin-bottom: 12px;
            animation: fadeIn 0.8s ease-out 0.4s both;
            line-height: 1.1;
            letter-spacing: -0.03em;
        }

        .title-wrapper {
            margin-bottom: 28px;
            animation: fadeIn 0.8s ease-out 0.5s both;
        }

        .title {
            font-size: 1rem;
            color: #3d3a35;
            font-weight: 500;
            margin-bottom: 5px;
        }

        .subtitle {
            font-size: 0.88rem;
            color: #8a8680;
            font-style: italic;
            font-family: 'Lora', serif;
        }

        .tech-tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 28px;
            animation: fadeIn 0.8s ease-out 0.6s both;
        }

        .tag {
            background: #ffffff;
            border: 1px solid #e4e1db;
            color: #3d3a35;
            padding: 6px 16px;
            border-radius: 4px;
            font-size: 0.76rem;
            font-weight: 500;
            letter-spacing: 0.02em;
            transition: all 0.2s ease;
            cursor: default;
        }

        .tag:hover {
            border-color: #1a6b3c;
            color: #1a6b3c;
            background: #edf7f1;
            transform: translateY(-1px);
        }

        .description {
            font-size: 0.97rem;
            color: #3d3a35;
            line-height: 1.82;
            margin-bottom: 32px;
            max-width: 500px;
            animation: fadeIn 0.8s ease-out 0.6s both;
            font-weight: 300;
        }

        .social-links {
            display: flex;
            gap: 10px;
            margin-bottom: 32px;
            animation: fadeIn 0.8s ease-out 0.7s both;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #ffffff;
            border-radius: 8px;
            border: 1px solid #e4e1db;
            color: #8a8680;
            text-decoration: none;
            transition: all 0.2s ease;
        }

        .social-link:hover {
            border-color: #1a6b3c;
            color: #1a6b3c;
            background: #edf7f1;
            transform: translateY(-2px);
        }

        .social-link i { font-size: 16px; }

        .cta-buttons {
            display: flex;
            gap: 12px;
            animation: fadeIn 0.8s ease-out 0.8s both;
        }

        .btn {
            padding: 12px 26px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.2s ease;
            font-size: 0.83rem;
            letter-spacing: 0.02em;
            position: relative;
            overflow: hidden;
            font-family: 'DM Sans', sans-serif;
        }

        .btn::before { display: none; }

        .btn span { position: relative; z-index: 1; }

        .btn-primary {
            background: #1a6b3c;
            color: #ffffff;
            box-shadow: 0 2px 12px rgba(26,107,60,0.2);
        }

        .btn-primary:hover {
            background: #155730;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(26,107,60,0.25);
        }

        .btn-secondary {
            background: #ffffff;
            color: #3d3a35;
            border: 1px solid #e4e1db;
        }

        .btn-secondary:hover {
            border-color: #3d3a35;
            transform: translateY(-2px);
        }

        /* Animations */
        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-30px); }
            to   { opacity: 1; transform: translateX(0); }
        }

        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(30px); }
            to   { opacity: 1; transform: translateX(0); }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(14px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-container { padding: 0 24px; }

            .hero {
                flex-direction: column;
                text-align: center;
                gap: 40px;
                padding: 100px 24px 40px;
            }

            .hero-content { order: 2; }
            .hero-image   { order: 1; }

            .greeting { justify-content: center; }
            .greeting::before { display: none; }

            .name { font-size: 2.5rem; }

            .profile-image { width: 220px; height: 220px; }

            .nav-links { gap: 18px; }
            .nav-links a { font-size: 0.72rem; }

            .cta-buttons { justify-content: center; }
            .tech-tags   { justify-content: center; }
            .social-links { justify-content: center; }
            .description { margin: 0 auto 32px; }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="index.html" class="logo">
                Areeba <span>&nbsp;Urooj</span>
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
            <div class="greeting">AI Automation Engineer</div>
            <h1 class="name">Areeba Urooj</h1>
            <div class="title-wrapper">
                <div class="title">Building intelligent systems that think for themselves.</div>
                <div class="subtitle">DevOps Background → AI-Powered Solutions</div>
            </div>

            <div class="tech-tags">
                <span class="tag">AI Automation</span>
                <span class="tag">DevOps</span>
                <span class="tag">Cloud</span>
                <span class="tag">MLOps</span>
            </div>

            <p class="description">
                I started in DevOps — cloud infrastructure, CI/CD, Kubernetes — and kept asking what if systems could think for themselves? That question led me here: building AI-powered automation that doesn't just follow scripts, but understands context, predicts issues, and optimizes itself.
            </p>

            <div class="social-links">
                <a href="https://linkedin.com/in/areeba-urooj-8a1606279/" target="_blank" class="social-link" title="LinkedIn">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://github.com/Areeba-Urooj" target="_blank" class="social-link" title="GitHub">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://x.com/areeba_uro86219" target="_blank" class="social-link" title="Twitter">
                    <i class="fab fa-x-twitter"></i>
                </a>
            </div>

            <div class="cta-buttons">
                <a href="projects.html" class="btn btn-primary">
                    <span>View Projects</span>
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

</body>
</html>
