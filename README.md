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
        html { scroll-behavior: smooth; }

        body {
            font-family: 'DM Sans', sans-serif;
            background: var(--bg);
            color: var(--ink);
            min-height: 100vh;
            -webkit-font-smoothing: antialiased;
        }

        /* ── NAV ── */
        .nav {
            position: sticky;
            top: 0;
            z-index: 200;
            background: rgba(250,249,247,0.96);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 56px;
            height: 66px;
        }

        .nav-logo {
            font-family: 'Lora', serif;
            font-size: 1.15rem;
            font-weight: 500;
            color: var(--ink);
            text-decoration: none;
        }

        .nav-logo span { color: var(--accent); }

        .nav-links { display: flex; gap: 38px; }

        .nav-links a {
            text-decoration: none;
            font-size: 0.82rem;
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

        /* ── HERO ── */
        .hero {
            max-width: 1080px;
            margin: 0 auto;
            padding: 0 56px;
            min-height: calc(100vh - 66px);
            display: grid;
            grid-template-columns: 1fr 340px;
            gap: 80px;
            align-items: center;
            border-bottom: 1px solid var(--border);
        }

        /* LEFT */
        .hero-left {}

        .hero-greeting {
            font-size: 0.78rem;
            font-weight: 600;
            letter-spacing: 0.14em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .greeting-line {
            width: 32px;
            height: 1.5px;
            background: var(--accent);
        }

        .hero-name {
            font-family: 'Lora', serif;
            font-size: clamp(3rem, 6vw, 5.2rem);
            font-weight: 500;
            line-height: 1.06;
            letter-spacing: -0.03em;
            color: var(--ink);
            margin-bottom: 24px;
        }

        .hero-name em {
            font-style: italic;
            color: var(--accent);
        }

        .hero-desc {
            font-size: 1.05rem;
            line-height: 1.85;
            color: var(--ink-2);
            font-weight: 300;
            max-width: 520px;
            margin-bottom: 36px;
        }

        .hero-desc strong {
            color: var(--ink);
            font-weight: 600;
        }

        /* tags */
        .hero-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 44px;
        }

        .hero-tag {
            padding: 6px 16px;
            border-radius: 4px;
            border: 1px solid var(--border);
            background: var(--white);
            font-size: 0.78rem;
            font-weight: 500;
            color: var(--ink-2);
            letter-spacing: 0.02em;
            transition: all 0.18s;
        }

        .hero-tag:hover {
            border-color: var(--accent);
            color: var(--accent);
            background: var(--accent-bg);
        }

        /* CTAs */
        .hero-ctas {
            display: flex;
            gap: 14px;
            align-items: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--accent);
            color: var(--white);
            padding: 13px 26px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.84rem;
            font-weight: 600;
            letter-spacing: 0.03em;
            transition: all 0.2s;
            box-shadow: 0 2px 12px rgba(26,107,60,0.18);
        }

        .btn-primary:hover {
            background: #155730;
            transform: translateY(-2px);
            box-shadow: 0 6px 24px rgba(26,107,60,0.25);
        }

        .btn-secondary {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--ink-2);
            padding: 13px 26px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.84rem;
            font-weight: 500;
            border: 1px solid var(--border);
            background: var(--white);
            transition: all 0.2s;
        }

        .btn-secondary:hover {
            border-color: var(--ink-2);
            color: var(--ink);
            transform: translateY(-2px);
        }

        /* RIGHT — profile card */
        .hero-right {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 28px;
        }

        .profile-card {
            width: 100%;
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 32px 28px;
            text-align: center;
        }

        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 2px solid var(--border);
            background: var(--bg-2);
            margin: 0 auto 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Lora', serif;
            font-size: 1.6rem;
            font-style: italic;
            color: var(--accent);
            overflow: hidden;
            transition: border-color 0.2s;
        }

        .profile-avatar:hover { border-color: var(--accent); }

        .profile-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .profile-name {
            font-family: 'Lora', serif;
            font-size: 1.1rem;
            font-weight: 500;
            color: var(--ink);
            margin-bottom: 5px;
        }

        .profile-role {
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.08em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 4px;
        }

        .profile-loc {
            font-size: 0.78rem;
            color: var(--muted);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }

        .profile-divider {
            height: 1px;
            background: var(--border);
            margin-bottom: 20px;
        }

        .profile-stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }

        .stat {
            text-align: center;
            padding: 12px 8px;
            background: var(--bg);
            border-radius: 6px;
        }

        .stat-num {
            font-family: 'Lora', serif;
            font-size: 1.4rem;
            font-weight: 500;
            color: var(--ink);
            line-height: 1;
            margin-bottom: 4px;
        }

        .stat-label {
            font-size: 0.7rem;
            color: var(--muted);
            font-weight: 400;
            letter-spacing: 0.03em;
        }

        .profile-social {
            display: flex;
            justify-content: center;
            gap: 8px;
        }

        .profile-social a {
            width: 36px;
            height: 36px;
            border-radius: 8px;
            border: 1px solid var(--border);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--muted);
            text-decoration: none;
            font-size: 0.85rem;
            transition: all 0.18s;
        }

        .profile-social a:hover {
            border-color: var(--accent);
            color: var(--accent);
            background: var(--accent-bg);
        }

        /* availability row */
        .avail-row {
            width: 100%;
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 16px;
            background: var(--accent-bg);
            border: 1px solid rgba(26,107,60,0.15);
            border-radius: 8px;
            font-size: 0.8rem;
            color: var(--accent);
            font-weight: 500;
        }

        .avail-dot {
            width: 7px; height: 7px;
            border-radius: 50%;
            background: var(--accent-mid);
            flex-shrink: 0;
            animation: pulse 2.2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%,100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.4; transform: scale(0.7); }
        }

        /* ── POSTS / RECENT SECTION (like Ed Donner's recent posts on homepage) ── */
        .posts-section {
            max-width: 1080px;
            margin: 0 auto;
            padding: 80px 56px 100px;
        }

        .sec-label {
            font-size: 0.68rem;
            font-weight: 700;
            letter-spacing: 0.16em;
            text-transform: uppercase;
            color: var(--muted);
            margin-bottom: 36px;
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .sec-label::after {
            content: '';
            flex: 1;
            height: 1px;
            background: var(--border);
        }

        .posts-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1px;
            background: var(--border);
            border: 1px solid var(--border);
            margin-bottom: 40px;
        }

        .post-card {
            background: var(--white);
            padding: 32px;
            text-decoration: none;
            color: inherit;
            display: block;
            transition: background 0.18s;
            position: relative;
        }

        .post-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 2px;
            background: var(--accent);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.25s;
        }

        .post-card:hover { background: var(--bg); }
        .post-card:hover::before { transform: scaleX(1); }

        .post-badge {
            font-size: 0.68rem;
            font-weight: 700;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .post-badge-dot {
            width: 5px; height: 5px;
            border-radius: 50%;
            background: var(--accent);
        }

        .post-title {
            font-family: 'Lora', serif;
            font-size: 1.1rem;
            font-weight: 500;
            line-height: 1.4;
            color: var(--ink);
            margin-bottom: 10px;
            letter-spacing: -0.01em;
        }

        .post-desc {
            font-size: 0.87rem;
            color: var(--muted);
            line-height: 1.7;
            font-weight: 300;
        }

        .post-arrow {
            position: absolute;
            top: 28px; right: 28px;
            font-size: 0.75rem;
            color: var(--border);
            transition: all 0.18s;
        }

        .post-card:hover .post-arrow {
            color: var(--accent);
            transform: translateX(3px);
        }

        /* see all link */
        .see-all {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--accent);
            text-decoration: none;
            font-size: 0.85rem;
            font-weight: 500;
            border-bottom: 1px solid rgba(26,107,60,0.3);
            padding-bottom: 2px;
            transition: border-color 0.18s;
        }

        .see-all:hover { border-color: var(--accent); }

        /* ── FOOTER ── */
        .footer {
            border-top: 1px solid var(--border);
            padding: 28px 56px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .footer-left {
            font-family: 'Lora', serif;
            font-size: 0.9rem;
            font-style: italic;
            color: var(--muted);
        }

        .footer-links { display: flex; gap: 24px; }

        .footer-links a {
            font-size: 0.78rem;
            color: var(--muted);
            text-decoration: none;
            letter-spacing: 0.04em;
            transition: color 0.18s;
        }

        .footer-links a:hover { color: var(--accent); }

        /* ── ANIMATIONS ── */
        [data-reveal] {
            opacity: 0;
            transform: translateY(22px);
            animation: reveal 0.7s cubic-bezier(0.16,1,0.3,1) forwards;
        }

        [data-reveal="1"] { animation-delay: 0.05s; }
        [data-reveal="2"] { animation-delay: 0.15s; }
        [data-reveal="3"] { animation-delay: 0.25s; }
        [data-reveal="4"] { animation-delay: 0.35s; }
        [data-reveal="5"] { animation-delay: 0.45s; }
        [data-reveal="6"] { animation-delay: 0.20s; }

        @keyframes reveal {
            to { opacity: 1; transform: translateY(0); }
        }

        /* ── RESPONSIVE ── */
        @media (max-width: 900px) {
            .nav { padding: 0 24px; }
            .hero { grid-template-columns: 1fr; padding: 56px 24px 64px; min-height: auto; gap: 48px; }
            .hero-right { flex-direction: row; flex-wrap: wrap; }
            .profile-card { flex: 1; min-width: 260px; }
            .avail-row { width: auto; flex: 1; min-width: 200px; }
            .posts-section { padding: 56px 24px 80px; }
            .posts-grid { grid-template-columns: 1fr; }
            .footer { flex-direction: column; gap: 10px; padding: 24px; text-align: center; }
            .nav-links { gap: 18px; }
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

    <!-- HERO -->
    <section class="hero">
        <div class="hero-left">
            <p class="hero-greeting" data-reveal="1">
                <span class="greeting-line"></span>
                AI Automation Engineer
            </p>

            <h1 class="hero-name" data-reveal="2">
                Well,<br><em>hi there.</em><br>I'm Areeba.
            </h1>

            <p class="hero-desc" data-reveal="3">
                I started in DevOps — cloud infrastructure, CI/CD, Kubernetes — and kept asking
                <strong>"what if systems could think for themselves?"</strong>
                That question led me here: building AI-powered automation that doesn't just follow scripts, but understands context and adapts.
            </p>

            <div class="hero-tags" data-reveal="4">
                <span class="hero-tag">AI Automation</span>
                <span class="hero-tag">MLOps</span>
                <span class="hero-tag">LLM Integration</span>
                <span class="hero-tag">AWS / Azure</span>
                <span class="hero-tag">DevOps</span>
                <span class="hero-tag">RAG Systems</span>
            </div>

            <div class="hero-ctas" data-reveal="5">
                <a href="projects.html" class="btn-primary">
                    View my projects <i class="fas fa-arrow-right" style="font-size:0.75rem;"></i>
                </a>
                <a href="about.html" class="btn-secondary">
                    About me
                </a>
            </div>
        </div>

        <div class="hero-right">
            <div class="profile-card" data-reveal="6">
                <div class="profile-avatar">
                    <img src="./assets/profile.jpg" alt="Areeba Urooj"
                         onerror="this.style.display='none'; this.parentElement.textContent='AU';">
                </div>
                <p class="profile-name">Areeba Urooj</p>
                <p class="profile-role">AI Automation Engineer</p>
                <p class="profile-loc">
                    <i class="fas fa-map-marker-alt" style="font-size:0.7rem;"></i>
                    Abbottabad, Pakistan
                </p>

                <div class="profile-divider"></div>

                <div class="profile-stats">
                    <div class="stat">
                        <p class="stat-num">9+</p>
                        <p class="stat-label">Projects</p>
                    </div>
                    <div class="stat">
                        <p class="stat-num">2+</p>
                        <p class="stat-label">Years DevOps</p>
                    </div>
                    <div class="stat">
                        <p class="stat-num">3M+</p>
                        <p class="stat-label">Readers reached</p>
                    </div>
                    <div class="stat">
                        <p class="stat-num">1</p>
                        <p class="stat-label">OCI Cert</p>
                    </div>
                </div>

                <div class="profile-social">
                    <a href="https://www.linkedin.com/in/areeba-urooj-8a1606279/" target="_blank" title="LinkedIn">
                        <i class="fab fa-linkedin-in"></i>
                    </a>
                    <a href="https://github.com/Areeba-Urooj" target="_blank" title="GitHub">
                        <i class="fab fa-github"></i>
                    </a>
                    <a href="https://x.com/areeba_uro86219" target="_blank" title="Twitter">
                        <i class="fab fa-x-twitter"></i>
                    </a>
                    <a href="mailto:cmy61677@gmail.com" title="Email">
                        <i class="fas fa-envelope"></i>
                    </a>
                </div>
            </div>

            <div class="avail-row" data-reveal="6">
                <span class="avail-dot"></span>
                Open to collaboration & opportunities
            </div>
        </div>
    </section>

    <!-- RECENT PROJECTS (like Ed's homepage posts) -->
    <section class="posts-section">
        <p class="sec-label">Recent projects</p>

        <div class="posts-grid">
            <a href="https://github.com/Areeba-Urooj/multi-model-brochure-creator/tree/main/ollama_brochure_agent" class="post-card" target="_blank" rel="noopener noreferrer">
                <i class="fas fa-arrow-up-right-from-square post-arrow"></i>
                <p class="post-badge"><span class="post-badge-dot"></span>AI Automation</p>
                <h3 class="post-title">AI-Powered Website Analyzer & Brochure Generator</h3>
                <p class="post-desc">Local LLM pipeline that converts raw web data into marketing collateral — 90% reduction in research time, zero API cost.</p>
            </a>

            <a href="https://github.com/Areeba-Urooj/linkedin-authority-builder" class="post-card" target="_blank" rel="noopener noreferrer">
                <i class="fas fa-arrow-up-right-from-square post-arrow"></i>
                <p class="post-badge"><span class="post-badge-dot"></span>AI Automation</p>
                <h3 class="post-title">AI-Powered LinkedIn Authority Builder</h3>
                <p class="post-desc">12-node automated workflow combining LLMs and image generation for professional LinkedIn content at scale.</p>
            </a>

            <a href="https://medium.com/@cmy61677/github-actions-ci-cd-for-a-3-tier-app-on-eks-2d4fc5237a92" class="post-card" target="_blank" rel="noopener noreferrer">
                <i class="fas fa-arrow-up-right-from-square post-arrow"></i>
                <p class="post-badge" style="color: #1d4ed8;"><span class="post-badge-dot" style="background:#1d4ed8;"></span>DevOps & Cloud</p>
                <h3 class="post-title">Full-Stack CI/CD on EKS with GitHub Actions</h3>
                <p class="post-desc">End-to-end DevSecOps pipeline for a 3-tier app — 90% faster deployments with SonarQube, Trivy, and Gitleaks.</p>
            </a>

            <a href="https://medium.com/@cmy61677/building-a-production-ready-devops-pipeline-from-manual-processes-to-automated-excellence-4743b0d71679" class="post-card" target="_blank" rel="noopener noreferrer">
                <i class="fas fa-arrow-up-right-from-square post-arrow"></i>
                <p class="post-badge" style="color: #1d4ed8;"><span class="post-badge-dot" style="background:#1d4ed8;"></span>DevOps & Cloud</p>
                <h3 class="post-title">Production-Ready DevOps Pipeline with Jenkins & EKS</h3>
                <p class="post-desc">Manual → fully automated deployment achieving 99.9% availability with zero manual intervention required.</p>
            </a>
        </div>

        <a href="projects.html" class="see-all">
            See all projects <i class="fas fa-arrow-right" style="font-size:0.75rem;"></i>
        </a>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
        <span class="footer-left">Areeba Urooj</span>
        <div class="footer-links">
            <a href="https://www.linkedin.com/in/areeba-urooj-8a1606279/" target="_blank">LinkedIn</a>
            <a href="https://github.com/Areeba-Urooj" target="_blank">GitHub</a>
            <a href="mailto:cmy61677@gmail.com">Email</a>
        </div>
    </footer>

</body>
</html>
