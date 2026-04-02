<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Areeba Urooj — AI Automation Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,500;1,400;1,500&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<style>
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

html, body {
    width: 100%; height: 100%;
    overflow: hidden;
    font-family: 'DM Sans', sans-serif;
    background: #faf9f7;
    color: #1a1814;
    -webkit-font-smoothing: antialiased;
}

/* NAV */
nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    height: 62px;
    background: rgba(250,249,247,0.97);
    border-bottom: 1px solid #e4e1db;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 52px;
    z-index: 10;
    backdrop-filter: blur(8px);
}

.logo {
    font-family: 'Lora', serif;
    font-size: 1.1rem;
    font-weight: 500;
    color: #1a1814;
    text-decoration: none;
}

.logo span { color: #1a6b3c; }

.nav-links { display: flex; gap: 36px; }

.nav-links a {
    text-decoration: none;
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    color: #8a8680;
    transition: color 0.2s;
}

.nav-links a:hover { color: #1a1814; }

/* PAGE BODY — two columns, fills screen below nav */
.page {
    position: fixed;
    top: 62px; bottom: 0;
    left: 0; right: 0;
    display: grid;
    grid-template-columns: 300px 1fr;
}

/* LEFT COLUMN */
.left {
    border-right: 1px solid #e4e1db;
    padding: 52px 40px;
    display: flex;
    flex-direction: column;
    gap: 0;
}

.avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    border: 1.5px solid #e4e1db;
    background: #f2f0ec;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Lora', serif;
    font-style: italic;
    font-size: 1.3rem;
    color: #1a6b3c;
    margin-bottom: 20px;
}

.avatar img { width: 100%; height: 100%; object-fit: cover; }

.l-name {
    font-family: 'Lora', serif;
    font-size: 1.05rem;
    font-weight: 500;
    margin-bottom: 5px;
}

.l-role {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.09em;
    text-transform: uppercase;
    color: #1a6b3c;
    margin-bottom: 4px;
}

.l-loc {
    font-size: 0.76rem;
    color: #8a8680;
    display: flex;
    align-items: center;
    gap: 5px;
    margin-bottom: 32px;
}

.divider { height: 1px; background: #e4e1db; margin-bottom: 24px; }

.l-label {
    font-size: 0.6rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #c8c4bc;
    margin-bottom: 10px;
}

.socials { display: flex; flex-direction: column; gap: 2px; margin-bottom: 32px; }

.socials a {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 8px 10px;
    border-radius: 6px;
    text-decoration: none;
    color: #8a8680;
    font-size: 0.82rem;
    transition: all 0.15s;
}

.socials a i { width: 14px; text-align: center; font-size: 0.8rem; }
.socials a:hover { background: #f2f0ec; color: #1a1814; }

.avail {
    margin-top: auto;
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 14px;
    background: #edf7f1;
    border: 1px solid rgba(26,107,60,0.15);
    border-radius: 8px;
    font-size: 0.76rem;
    color: #1a6b3c;
    font-weight: 500;
}

.dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: #2d9e5f;
    flex-shrink: 0;
    animation: blink 2s ease-in-out infinite;
}

@keyframes blink {
    0%,100% { opacity:1; } 50% { opacity:0.3; }
}

/* RIGHT COLUMN */
.right {
    padding: 52px 72px;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.greeting {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #1a6b3c;
    margin-bottom: 18px;
}

.greeting-line { width: 28px; height: 1.5px; background: #1a6b3c; }

h1 {
    font-family: 'Lora', serif;
    font-size: clamp(2.8rem, 4.5vw, 4.2rem);
    font-weight: 500;
    line-height: 1.08;
    letter-spacing: -0.03em;
    margin-bottom: 24px;
}

h1 em { font-style: italic; color: #1a6b3c; }

.desc {
    font-size: 0.97rem;
    line-height: 1.82;
    color: #3d3a35;
    font-weight: 300;
    max-width: 480px;
    margin-bottom: 28px;
}

.desc strong { color: #1a1814; font-weight: 600; }

.tags {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
    margin-bottom: 36px;
}

.tag {
    padding: 5px 14px;
    border-radius: 4px;
    border: 1px solid #e4e1db;
    background: #fff;
    font-size: 0.76rem;
    font-weight: 500;
    color: #3d3a35;
    transition: all 0.15s;
}

.tag:hover { border-color: #1a6b3c; color: #1a6b3c; background: #edf7f1; }

.btns { display: flex; gap: 12px; }

.btn-p {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    background: #1a6b3c;
    color: #fff;
    padding: 12px 24px;
    border-radius: 6px;
    text-decoration: none;
    font-size: 0.82rem;
    font-weight: 600;
    transition: all 0.2s;
    box-shadow: 0 2px 10px rgba(26,107,60,0.2);
}

.btn-p:hover { background: #155730; transform: translateY(-2px); }

.btn-s {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    color: #3d3a35;
    padding: 12px 24px;
    border-radius: 6px;
    text-decoration: none;
    font-size: 0.82rem;
    font-weight: 500;
    border: 1px solid #e4e1db;
    background: #fff;
    transition: all 0.2s;
}

.btn-s:hover { border-color: #3d3a35; }

/* footer bar */
footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    height: 42px;
    border-top: 1px solid #e4e1db;
    background: #fff;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 52px;
    font-size: 0.74rem;
    color: #c8c4bc;
}

footer a {
    color: #c8c4bc;
    text-decoration: none;
    transition: color 0.15s;
}

footer a:hover { color: #1a6b3c; }

.footer-links { display: flex; gap: 20px; }

/* push right column up to account for footer */
.right { padding-bottom: 42px; }
.left  { padding-bottom: 42px; }
</style>
</head>
<body>

<nav>
    <a href="index.html" class="logo">Areeba <span>Urooj</span></a>
    <div class="nav-links">
        <a href="about.html">About</a>
        <a href="projects.html">Projects</a>
        <a href="experience.html">Experience</a>
        <a href="contact.html">Contact</a>
    </div>
</nav>

<div class="page">

    <!-- LEFT -->
    <aside class="left">
        <div class="avatar">
            <img src="./assets/profile.jpg" alt="Areeba Urooj"
                 onerror="this.style.display='none';this.parentElement.textContent='AU'">
        </div>

        <p class="l-name">Areeba Urooj</p>
        <p class="l-role">AI Automation Engineer</p>
        <p class="l-loc"><i class="fas fa-map-marker-alt" style="font-size:.65rem;"></i>Abbottabad, Pakistan</p>

        <div class="divider"></div>

        <p class="l-label">Find me</p>
        <nav class="socials">
            <a href="https://www.linkedin.com/in/areeba-urooj-8a1606279/" target="_blank">
                <i class="fab fa-linkedin-in"></i> LinkedIn
            </a>
            <a href="https://github.com/Areeba-Urooj" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
            <a href="https://x.com/areeba_uro86219" target="_blank">
                <i class="fab fa-x-twitter"></i> Twitter
            </a>
            <a href="mailto:cmy61677@gmail.com">
                <i class="fas fa-envelope"></i> Email
            </a>
        </nav>

        <div class="avail">
            <span class="dot"></span>
            Open to opportunities
        </div>
    </aside>

    <!-- RIGHT -->
    <main class="right">

        <p class="greeting">
            <span class="greeting-line"></span>
            AI Automation Engineer
        </p>

        <h1>Well,<br><em>hi there.</em><br>I'm Areeba.</h1>

        <p class="desc">
            I started in DevOps — cloud infrastructure, CI/CD, Kubernetes — and kept asking <strong>"what if systems could think for themselves?"</strong> That question led me here: building AI-powered automation that adapts, predicts, and scales.
        </p>

        <div class="tags">
            <span class="tag">AI Automation</span>
            <span class="tag">MLOps</span>
            <span class="tag">LLM Integration</span>
            <span class="tag">AWS / Azure</span>
            <span class="tag">RAG Systems</span>
            <span class="tag">DevOps</span>
        </div>

        <div class="btns">
            <a href="projects.html" class="btn-p">
                View projects <i class="fas fa-arrow-right" style="font-size:.7rem;"></i>
            </a>
            <a href="about.html" class="btn-s">About me</a>
        </div>

    </main>
</div>

<footer>
    <span>Areeba Urooj — AI Automation Engineer</span>
    <div class="footer-links">
        <a href="https://www.linkedin.com/in/areeba-urooj-8a1606279/" target="_blank">LinkedIn</a>
        <a href="https://github.com/Areeba-Urooj" target="_blank">GitHub</a>
        <a href="mailto:cmy61677@gmail.com">Email</a>
    </div>
</footer>

</body>
</html>
