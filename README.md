<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areeba Urooj — AI Automation Engineer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;0,600;1,400;1,500&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --bg:        #faf9f7;
            --bg-2:      #f2f0ec;
            --ink:       #1a1814;
            --ink-2:     #3d3a35;
            --muted:     #8a8680;
            --border:    #e4e1db;
            --accent:    #1a6b3c;
            --accent-bg: #edf7f1;
            --accent-mid:#2d9e5f;
            --white:     #ffffff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        html, body {
            height: 100%;
            overflow: hidden; /* single screen, no scroll */
        }

        body {
            font-family: 'DM Sans', sans-serif;
            background: var(--bg);
            color: var(--ink);
            -webkit-font-smoothing: antialiased;
            display: flex;
            flex-direction: column;
        }

        /* ── NAV ── */
        .nav {
            background: rgba(250,249,247,0.96);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 56px;
            height: 62px;
            flex-shrink: 0;
        }

        .nav-logo {
            font-family: 'Lora', serif;
            font-size: 1.1rem;
            font-weight: 500;
            color: var(--ink);
            text-decoration: none;
        }

        .nav-logo span { color: var(--accent); }

        .nav-links { display: flex; gap: 36px; }

        .nav-links a {
            text-decoration: none;
            font-size: 0.8rem;
            font-weight: 500;
            letter-spacing: 0.06em;
            text-transform: uppercase;
            color: var(--muted);
            transition: color 0.2s;
            position: relative;
            padding-bottom: 3px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            left: 0; bottom: 0;
            width: 0; height: 1.5px;
            background: var(--accent);
            transition: width 0.25s ease;
        }

        .nav-links a:hover { color: var(--ink); }
        .nav-links a:hover::after { width: 100%; }

        /* ── MAIN AREA (fills remaining height) ── */
        .main {
            flex: 1;
            display: grid;
            grid-template-columns: 260px 1fr 300px;
            border-top: none;
            overflow: hidden;
        }

        /* ── LEFT PANEL ── */
        .panel-left {
            border-right: 1px solid var(--border);
            padding: 48px 36px;
            display: flex;
            flex-direction: column;
            gap: 32px;
        }

        .profile-avatar {
            width: 90px;
            height: 90px;
            border-radius: 50%;
            border: 1.5px solid var(--border);
            background: var(--bg-2);
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Lora', serif;
            font-size: 1.4rem;
            font-style: italic;
            color: var(--accent);
            flex-shrink: 0;
            transition: border-color 0.2s;
        }

        .profile-avatar:hover { border-color: var(--accent); }

        .profile-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .left-name {
            font-family: 'Lora', serif;
            font-size: 1.05rem;
            font-weight: 500;
            color: var(--ink);
            margin-bottom: 4px;
        }

        .left-role {
            font-size: 0.72rem;
            font-weight: 700;
            letter-spacing: 0.08em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 3px;
        }

        .left-loc {
            font-size: 0.76rem;
            color: var(--muted);
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .left-divider {
            height: 1px;
            background: var(--border);
        }

        .left-label {
            font-size: 0.62rem;
            font-weight: 700;
            letter-spacing: 0.14em;
            text-transform: uppercase;
            color: var(--border);
            margin-bottom: 10px;
        }

        .social-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 2px;
        }

        .social-list a {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 8px 10px;
            border-radius: 6px;
            text-decoration: none;
            color: var(--muted);
            font-size: 0.82rem;
            transition: all 0.18s;
        }

        .social-list a i { width: 14px; text-align: center; font-size: 0.8rem; }
        .social-list a:hover { background: var(--bg-2); color: var(--ink); }

        .avail-badge {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 14px;
            background: var(--accent-bg);
            border: 1px solid rgba(26,107,60,0.15);
            border-radius: 8px;
            font-size: 0.76rem;
            color: var(--accent);
            font-weight: 500;
            margin-top: auto;
        }

        .avail-dot {
            width: 6px; height: 6px;
            border-radius: 50%;
            background: var(--accent-mid);
            flex-shrink: 0;
            animation: pulse 2.2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%,100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.3; transform: scale(0.7); }
        }

        /* ── CENTRE PANEL ── */
        .panel-centre {
            padding: 52px 60px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            border-right: 1px solid var(--border);
        }

        .greeting-row {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.74rem;
            font-weight: 700;
            letter-spacing: 0.14em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 18px;
        }

        .greeting-line {
            width: 28px; height: 1.5px;
            background: var(--accent);
        }

        .hero-name {
            font-family: 'Lora', serif;
            font-size: clamp(2.4rem, 4.5vw, 3.8rem);
            font-weight: 500;
            line-height: 1.08;
            letter-spacing: -0.03em;
            color: var(--ink);
            margin-bottom: 22px;
        }

        .hero-name em {
            font-style: italic;
            color: var(--accent);
        }

        .hero-desc {
            font-size: 0.97rem;
            line-height: 1.82;
            color: var(--ink-2);
            font-weight: 300;
            margin-bottom: 28px;
            max-width: 440px;
        }

        .hero-desc strong { color: var(--ink); font-weight: 600; }

        .hero-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 7px;
            margin-bottom: 32px;
        }

        .hero-tag {
            padding: 5px 14px;
            border-radius: 4px;
            border: 1px solid var(--border);
            background: var(--white);
            font-size: 0.76rem;
            font-weight: 500;
            color: var(--ink-2);
            transition: all 0.18s;
        }

        .hero-tag:hover {
            border-color: var(--accent);
            color: var(--accent);
            background: var(--accent-bg);
        }

        .hero-ctas {
            display: flex;
            gap: 12px;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--accent);
            color: var(--white);
            padding: 11px 22px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.82rem;
            font-weight: 600;
            letter-spacing: 0.02em;
            transition: all 0.2s;
            box-shadow: 0 2px 10px rgba(26,107,60,0.18);
        }

        .btn-primary:hover {
            background: #155730;
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(26,107,60,0.25);
        }

        .btn-secondary {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--ink-2);
            padding: 11px 22px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.82rem;
            font-weight: 500;
            border: 1px solid var(--border);
            background: var(--white);
            transition: all 0.2s;
        }

        .btn-secondary:hover { border-color: var(--ink-2); color: var(--ink); }

        /* ── RIGHT PANEL ── */
        .panel-right {
            padding: 40px 32px;
            display: flex;
            flex-direction: column;
            gap: 0;
            overflow: hidden;
        }

        .right-label {
            font-size: 0.62rem;
            font-weight: 700;
            letter-spacing: 0.14em;
            text-transform: uppercase;
            color: var(--muted);
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .right-label::after {
            content: '';
            flex: 1;
            height: 1px;
            background: var(--border);
        }

        /* mini project cards */
        .mini-cards {
            display: flex;
            flex-direction: column;
            flex: 1;
        }

        .mini-card {
            flex: 1;
            padding: 16px 0;
            border-bottom: 1px solid var(--border);
            text-decoration: none;
            color: inherit;
            display: flex;
            flex-direction: column;
            gap: 5px;
            transition: background 0.15s;
            position: relative;
            padding-right: 20px;
        }

        .mini-card:first-child { border-top: 1px solid var(--border); }

        .mini-card:hover { background: var(--bg-2); padding-left: 8px; border-radius: 4px; }

        .mini-arrow {
            position: absolute;
            right: 0; top: 16px;
            font-size: 0.65rem;
            color: var(--border);
            transition: all 0.15s;
        }

        .mini-card:hover .mini-arrow { color: var(--accent); transform: translateX(2px); }

        .mini-badge {
            font-size: 0.63rem;
            font-weight: 700;
            letter-spacing: 0.08em;
            text-transform: uppercase;
        }

        .mini-badge.ai { color: var(--accent); }
        .mini-badge.devops { color: #1d4ed8; }

        .mini-title {
            font-size: 0.84rem;
            font-weight: 500;
            color: var(--ink);
            line-height: 1.35;
        }

        .mini-desc {
            font-size: 0.76rem;
            color: var(--muted);
            font-weight: 300;
            line-height: 1.5;
        }

        /* see all */
        .see-all {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            color: var(--accent);
            text-decoration: none;
            font-size: 0.78rem;
            font-weight: 500;
            padding-top: 16px;
            border-bottom: 1px solid rgba(26,107,60,0.3);
            width: fit-content;
            padding-bottom: 1px;
            transition: border-color 0.18s;
        }

        .see-all:hover { border-color: var(--accent); }

        /* ── FOOTER BAR ── */
        .footer {
            border-top: 1px solid var(--border);
            padding: 14px 56px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-shrink: 0;
            background: var(--white);
        }

        .footer-left {
            font-family: 'Lora', serif;
            font-size: 0.82rem;
            font-style: italic;
            color: var(--muted);
        }

        .footer-right {
            font-size: 0.74rem;
            color: var(--border);
            letter-spacing: 0.04em;
        }

        /* ── ANIMATIONS ── */
        [data-reveal] {
            opacity: 0;
            transform: translateY(18px);
            animation: reveal 0.65s cubic-bezier(0.16,1,0.3,1) forwards;
        }

        [data-reveal="1"] { animation-delay: 0.05s; }
        [data-reveal="2"] { animation-delay: 0.12s; }
        [data-reveal="3"] { animation-delay: 0.19s; }
        [data-reveal="4"] { animation-delay: 0.26s; }
        [data-reveal="5"] { animation-delay: 0.33s; }
        [data-reveal="6"] { animation-delay: 0.08s; }
        [data-reveal="7"] { animation-delay: 0.16s; }

        @keyframes reveal {
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <!-- NAV -->
    <nav class="nav">
        <a href="index.html" class="nav-logo">Areeba <span>Urooj</span></a>
        <div class="nav-links">
            <a href="about.html">About</a>
            <a href="projects.html">Projects</a>
            <a href="experience.html">Experience</a>
            <a href="contact.html">Contact</a>
        </div>
    </nav>

    <!-- THREE-COLUMN MAIN -->
    <div class="main">

        <!-- LEFT: profile info -->
        <aside class="panel-left">

            <div class="profile-avatar" data-reveal="6">
                <img src="./assets/profile.jpg" alt="Areeba Urooj"
                     onerror="this.style.display='none'; this.parentElement.innerHTML='AU';">
            </div>

            <div data-reveal="6">
                <p class="left-name">Areeba Urooj</p>
                <p class="left-role">AI Automation Engineer</p>
                <p class="left-loc"><i class="fas fa-map-marker-alt" style="font-size:0.65rem;"></i> Abbottabad, Pakistan</p>
            </div>

            <div class="left-divider"></div>

            <div data-reveal="7">
                <p class="left-label">Find me</p>
                <ul class="social-list">
                    <li><a href="https://www.linkedin.com/in/areeba-urooj-8a1606279/" target="_blank"><i class="fab fa-linkedin-in"></i> LinkedIn</a></li>
                    <li><a href="https://github.com/Areeba-Urooj" target="_blank"><i class="fab fa-github"></i> GitHub</a></li>
                    <li><a href="https://x.com/areeba_uro86219" target="_blank"><i class="fab fa-x-twitter"></i> Twitter</a></li>
                    <li><a href="mailto:cmy61677@gmail.com"><i class="fas fa-envelope"></i> Email</a></li>
                </ul>
            </div>

            <div class="avail-badge" data-reveal="7">
                <span class="avail-dot"></span>
                Open to opportunities
            </div>

        </aside>

        <!-- CENTRE: hero text -->
        <section class="panel-centre">

            <p class="greeting-row" data-reveal="1">
                <span class="greeting-line"></span>
                AI Automation Engineer
            </p>

            <h1 class="hero-name" data-reveal="2">
                Well,<br><em>hi there.</em><br>I'm Areeba.
            </h1>

            <p class="hero-desc" data-reveal="3">
                I started in DevOps — cloud infrastructure, CI/CD, Kubernetes — and kept asking <strong>"what if systems could think for themselves?"</strong> That question led me here: building AI-powered automation that adapts, predicts, and scales.
            </p>

            <div class="hero-tags" data-reveal="4">
                <span class="hero-tag">AI Automation</span>
                <span class="hero-tag">MLOps</span>
                <span class="hero-tag">LLM Integration</span>
                <span class="hero-tag">AWS / Azure</span>
                <span class="hero-tag">RAG Systems</span>
                <span class="hero-tag">DevOps</span>
            </div>

            <div class="hero-ctas" data-reveal="5">
                <a href="projects.html" class="btn-primary">
                    View projects <i class="fas fa-arrow-right" style="font-size:0.7rem;"></i>
                </a>
                <a href="about.html" class="btn-secondary">
                    About me
                </a>
            </div>

        </section>

        <!-- RIGHT: recent projects -->
        <aside class="panel-right">

            <p class="right-label" data-reveal="6">Recent projects</p>

            <div class="mini-cards">

                <a href="https://github.com/Areeba-Urooj/multi-model-brochure-creator/tree/main/ollama_brochure_agent" class="mini-card" target="_blank" data-reveal="6">
                    <i class="fas fa-arrow-up-right-from-square mini-arrow"></i>
                    <span class="mini-badge ai">AI Automation</span>
                    <p class="mini-title">Website Analyzer & Brochure Generator</p>
                    <p class="mini-desc">Local LLM · 90% faster · zero API cost</p>
                </a>

                <a href="https://github.com/Areeba-Urooj/linkedin-authority-builder" class="mini-card" target="_blank" data-reveal="6">
                    <i class="fas fa-arrow-up-right-from-square mini-arrow"></i>
                    <span class="mini-badge ai">AI Automation</span>
                    <p class="mini-title">LinkedIn Authority Builder</p>
                    <p class="mini-desc">12-node workflow · LLM + image generation</p>
                </a>

                <a href="https://medium.com/@cmy61677/github-actions-ci-cd-for-a-3-tier-app-on-eks-2d4fc5237a92" class="mini-card" target="_blank" data-reveal="7">
                    <i class="fas fa-arrow-up-right-from-square mini-arrow"></i>
                    <span class="mini-badge devops">DevOps & Cloud</span>
                    <p class="mini-title">Full-Stack CI/CD on EKS</p>
                    <p class="mini-desc">GitHub Actions · DevSecOps · 90% faster deploys</p>
                </a>

                <a href="https://medium.com/@cmy61677/building-a-production-ready-devops-pipeline-from-manual-processes-to-automated-excellence-4743b0d71679" class="mini-card" target="_blank" data-reveal="7">
                    <i class="fas fa-arrow-up-right-from-square mini-arrow"></i>
                    <span class="mini-badge devops">DevOps & Cloud</span>
                    <p class="mini-title">Production DevOps Pipeline with Jenkins</p>
                    <p class="mini-desc">99.9% uptime · zero manual steps</p>
                </a>

            </div>

            <a href="projects.html" class="see-all" data-reveal="7">
                See all projects <i class="fas fa-arrow-right" style="font-size:0.7rem;"></i>
            </a>

        </aside>

    </div>

    <!-- FOOTER -->
    <footer class="footer">
        <span class="footer-left">Areeba Urooj — AI Automation Engineer</span>
        <span class="footer-right">© 2025 · All rights reserved</span>
    </footer>

</body>
</html>
