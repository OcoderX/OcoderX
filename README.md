<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>OcoderX | GitHub Portfolio README Style</title>

  <link rel="preconnect" href="https://cdnjs.cloudflare.com" />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
  />

  <style>
    :root {
      --bg: #0d1117;
      --bg-soft: rgba(22, 27, 34, 0.72);
      --card: rgba(22, 27, 34, 0.62);
      --card-strong: rgba(30, 41, 59, 0.78);
      --border: rgba(255, 255, 255, 0.10);
      --text: #e6edf3;
      --muted: #8b949e;
      --blue: #2f81f7;
      --blue-soft: rgba(47, 129, 247, 0.16);
      --green: #3fb950;
      --shadow: 0 20px 60px rgba(0, 0, 0, 0.45);
      --radius: 24px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(47, 129, 247, 0.15), transparent 26%),
        radial-gradient(circle at bottom right, rgba(63, 185, 80, 0.10), transparent 22%),
        linear-gradient(135deg, #0d1117 0%, #0b1220 45%, #111827 100%);
      min-height: 100vh;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background:
        linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
      background-size: 36px 36px;
      pointer-events: none;
      mask-image: radial-gradient(circle at center, black 55%, transparent 100%);
    }

    .container {
      width: min(1180px, calc(100% - 32px));
      margin: 40px auto 60px;
    }

    .hero {
      position: relative;
      overflow: hidden;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, rgba(17, 24, 39, 0.80), rgba(15, 23, 42, 0.62));
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      border-radius: 32px;
      box-shadow: var(--shadow);
      padding: 28px;
      animation: fadeUp 0.9s ease;
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: auto -80px -80px auto;
      width: 220px;
      height: 220px;
      background: radial-gradient(circle, rgba(47,129,247,0.25), transparent 68%);
      filter: blur(10px);
      pointer-events: none;
    }

    .banner {
      height: 220px;
      border-radius: 24px;
      background:
        linear-gradient(120deg, rgba(47,129,247,0.20), rgba(63,185,80,0.10)),
        url('https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1400&q=80') center/cover;
      border: 1px solid rgba(255,255,255,0.08);
      position: relative;
      overflow: hidden;
    }

    .banner::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(13,17,23,0.75), rgba(13,17,23,0.10));
    }

    .hero-content {
      position: relative;
      margin-top: -72px;
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 24px;
    }

    .profile-main,
    .profile-side,
    .section-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      box-shadow: var(--shadow);
    }

    .profile-main {
      padding: 28px;
    }

    .profile-side {
      padding: 24px;
    }

    .top {
      display: flex;
      gap: 20px;
      align-items: flex-start;
      flex-wrap: wrap;
    }

    .avatar-wrap {
      position: relative;
      width: 136px;
      height: 136px;
      flex-shrink: 0;
    }

    .avatar-wrap::before {
      content: "";
      position: absolute;
      inset: -5px;
      border-radius: 50%;
      background: linear-gradient(135deg, rgba(47,129,247,0.9), rgba(63,185,80,0.7));
      filter: blur(10px);
      opacity: 0.65;
      z-index: 0;
    }

    .avatar {
      position: relative;
      z-index: 1;
      width: 100%;
      height: 100%;
      border-radius: 50%;
      object-fit: cover;
      border: 4px solid #0d1117;
      background: #0d1117;
      transition: transform 0.35s ease;
    }

    .avatar-wrap:hover .avatar {
      transform: scale(1.05) rotate(1deg);
    }

    .identity {
      flex: 1;
      min-width: 240px;
      padding-top: 10px;
    }

    .name-row {
      display: flex;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
      margin-bottom: 8px;
    }

    .name {
      font-size: 2rem;
      font-weight: 800;
      letter-spacing: -0.03em;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid rgba(47,129,247,0.30);
      background: var(--blue-soft);
      color: #8ec5ff;
      padding: 8px 12px;
      border-radius: 999px;
      font-size: 0.86rem;
      font-weight: 600;
    }

    .username {
      font-size: 1.05rem;
      color: var(--muted);
      margin-bottom: 12px;
    }

    .bio {
      font-size: 1rem;
      line-height: 1.8;
      color: #dce3ea;
      max-width: 680px;
    }

    .meta {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 18px;
    }

    .meta-item {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.06);
      color: #c9d1d9;
      font-size: 0.94rem;
      transition: transform 0.25s ease, border-color 0.25s ease, background 0.25s ease;
    }

    .meta-item:hover {
      transform: translateY(-3px);
      border-color: rgba(47,129,247,0.45);
      background: rgba(47,129,247,0.10);
    }

    .cta-row {
      display: flex;
      gap: 14px;
      margin-top: 22px;
      flex-wrap: wrap;
    }

    .btn {
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 12px 18px;
      border-radius: 14px;
      font-weight: 700;
      border: 1px solid var(--border);
      transition: 0.28s ease;
      cursor: pointer;
    }

    .btn-primary {
      color: white;
      background: linear-gradient(135deg, #1f6feb, #2f81f7);
      box-shadow: 0 12px 30px rgba(47,129,247,0.25);
    }

    .btn-primary:hover {
      transform: translateY(-4px) scale(1.01);
      box-shadow: 0 18px 36px rgba(47,129,247,0.38);
    }

    .btn-secondary {
      color: var(--text);
      background: rgba(255,255,255,0.04);
    }

    .btn-secondary:hover {
      transform: translateY(-4px);
      background: rgba(255,255,255,0.08);
      border-color: rgba(255,255,255,0.18);
    }

    .card-title {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      margin-bottom: 18px;
    }

    .card-title h3 {
      font-size: 1.05rem;
      font-weight: 800;
      letter-spacing: -0.02em;
    }

    .card-title i {
      color: #58a6ff;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 14px;
      margin-bottom: 22px;
    }

    .stat {
      padding: 18px;
      border-radius: 18px;
      background: linear-gradient(180deg, rgba(255,255,255,0.05), rgba(255,255,255,0.03));
      border: 1px solid rgba(255,255,255,0.07);
      transition: transform 0.28s ease, box-shadow 0.28s ease, border-color 0.28s ease;
    }

    .stat:hover {
      transform: translateY(-6px) scale(1.02);
      border-color: rgba(47,129,247,0.45);
      box-shadow: 0 14px 34px rgba(0,0,0,0.30);
    }

    .stat .icon {
      width: 42px;
      height: 42px;
      border-radius: 12px;
      display: grid;
      place-items: center;
      margin-bottom: 12px;
      background: rgba(47,129,247,0.12);
      color: #7db8ff;
      font-size: 1rem;
    }

    .stat h4 {
      font-size: 1.45rem;
      margin-bottom: 6px;
    }

    .stat p {
      color: var(--muted);
      font-size: 0.93rem;
    }

    .mini-links {
      display: grid;
      gap: 12px;
    }

    .mini-link {
      text-decoration: none;
      color: var(--text);
      padding: 14px 16px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,0.07);
      background: rgba(255,255,255,0.03);
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      transition: 0.28s ease;
    }

    .mini-link:hover {
      transform: translateX(6px);
      background: rgba(47,129,247,0.08);
      border-color: rgba(47,129,247,0.45);
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 22px;
      margin-top: 22px;
    }

    .section-card {
      padding: 24px;
      animation: fadeUp 0.9s ease both;
    }

    .section-card:nth-child(2) { animation-delay: 0.08s; }
    .section-card:nth-child(3) { animation-delay: 0.16s; }
    .section-card:nth-child(4) { animation-delay: 0.24s; }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .chip {
      padding: 10px 14px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
      color: #d9e2ec;
      font-size: 0.92rem;
      transition: 0.25s ease;
    }

    .chip:hover {
      transform: translateY(-3px) scale(1.04);
      background: rgba(47,129,247,0.11);
      border-color: rgba(47,129,247,0.42);
      box-shadow: 0 10px 24px rgba(0,0,0,0.22);
    }

    .projects {
      display: grid;
      gap: 16px;
    }

    .project {
      padding: 18px;
      border-radius: 18px;
      border: 1px solid rgba(255,255,255,0.07);
      background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(255,255,255,0.02));
      transition: 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .project::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.06), transparent);
      transform: translateX(-130%);
      transition: 0.7s ease;
    }

    .project:hover::before {
      transform: translateX(130%);
    }

    .project:hover {
      transform: translateY(-6px);
      border-color: rgba(47,129,247,0.42);
      box-shadow: 0 16px 36px rgba(0,0,0,0.28);
    }

    .project h4 {
      font-size: 1.05rem;
      margin-bottom: 8px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .project p {
      color: #c7d0d9;
      line-height: 1.7;
      font-size: 0.95rem;
      margin-bottom: 12px;
    }

    .project-meta {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .tag {
      font-size: 0.82rem;
      padding: 7px 11px;
      border-radius: 999px;
      background: rgba(63,185,80,0.10);
      border: 1px solid rgba(63,185,80,0.18);
      color: #9ae6a5;
    }

    .cert-list {
      display: grid;
      gap: 14px;
    }

    .cert {
      padding: 18px;
      border-radius: 18px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
      transition: 0.28s ease;
    }

    .cert:hover {
      transform: translateY(-5px);
      border-color: rgba(47,129,247,0.40);
      background: rgba(47,129,247,0.08);
    }

    .cert-top {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      align-items: center;
      margin-bottom: 8px;
      flex-wrap: wrap;
    }

    .cert h4 {
      font-size: 1rem;
    }

    .cert small {
      color: var(--muted);
      font-size: 0.88rem;
    }

    .placeholder {
      color: #9fb3c8;
      border-left: 3px solid rgba(47,129,247,0.55);
      padding-left: 12px;
      margin-top: 8px;
      line-height: 1.7;
      font-size: 0.93rem;
    }

    .footer-note {
      margin-top: 22px;
      text-align: center;
      color: var(--muted);
      font-size: 0.92rem;
    }

    .typing {
      display: inline-block;
      white-space: nowrap;
      overflow: hidden;
      border-right: 2px solid #58a6ff;
      animation: typing 4s steps(34, end) infinite alternate, blink 0.8s step-end infinite;
      max-width: 100%;
    }

    @keyframes typing {
      from { width: 0; }
      to { width: 100%; }
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(18px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 980px) {
      .hero-content,
      .grid {
        grid-template-columns: 1fr;
      }

      .profile-side {
        order: 2;
      }
    }

    @media (max-width: 640px) {
      .container {
        width: min(100% - 18px, 1180px);
        margin: 18px auto 32px;
      }

      .hero,
      .profile-main,
      .profile-side,
      .section-card {
        border-radius: 22px;
      }

      .hero {
        padding: 16px;
      }

      .banner {
        height: 170px;
        border-radius: 18px;
      }

      .hero-content {
        margin-top: -52px;
        gap: 16px;
      }

      .profile-main,
      .profile-side,
      .section-card {
        padding: 18px;
      }

      .avatar-wrap {
        width: 110px;
        height: 110px;
      }

      .name {
        font-size: 1.6rem;
      }

      .stats {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 460px) {
      .stats {
        grid-template-columns: 1fr;
      }

      .meta {
        flex-direction: column;
      }

      .cta-row {
        flex-direction: column;
      }

      .btn {
        justify-content: center;
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <main class="container">
    <section class="hero">
      <div class="banner"></div>

      <div class="hero-content">
        <div class="profile-main">
          <div class="top">
            <div class="avatar-wrap">
              <img
                class="avatar"
                src="https://avatars.githubusercontent.com/u/583231?v=4"
                alt="OcoderX Avatar"
                onerror="this.src='https://source.unsplash.com/300x300/?developer,technology';"
              />
            </div>

            <div class="identity">
              <div class="name-row">
                <h1 class="name">Khojiakbar Obidov</h1>
                <span class="badge">
                  <i class="fa-brands fa-github"></i>
                  README Style Portfolio
                </span>
              </div>

              <div class="username">@OcoderX</div>

              <p class="bio">
                <span class="typing">Student of Tashkent University of Information Technologies</span>
              </p>

              <div class="meta">
                <div class="meta-item">
                  <i class="fa-solid fa-location-dot"></i>
                  Tashkent, Uzbekistan
                </div>
                <div class="meta-item">
                  <i class="fa-solid fa-building-columns"></i>
                  TUIT
                </div>
                <div class="meta-item">
                  <i class="fa-brands fa-telegram"></i>
                  @OcoderX / t.me/OcoderXbot
                </div>
                <div class="meta-item">
                  <i class="fa-solid fa-shield-halved"></i>
                  AI & Cybersecurity Learner
                </div>
              </div>

              <div class="cta-row">
                <a href="https://github.com/OcoderX" class="btn btn-primary" target="_blank">
                  <i class="fa-brands fa-github"></i>
                  View GitHub
                </a>
                <a href="#certificates" class="btn btn-secondary">
                  <i class="fa-solid fa-certificate"></i>
                  My Certificates
                </a>
              </div>
            </div>
          </div>
        </div>

        <aside class="profile-side">
          <div class="card-title">
            <h3><i class="fa-solid fa-chart-simple"></i> Live Profile Snapshot</h3>
          </div>

          <div class="stats">
            <div class="stat">
              <div class="icon"><i class="fa-solid fa-book-bookmark"></i></div>
              <h4>4</h4>
              <p>Repositories</p>
            </div>

            <div class="stat">
              <div class="icon"><i class="fa-solid fa-users"></i></div>
              <h4>3</h4>
              <p>Followers</p>
            </div>

            <div class="stat">
              <div class="icon"><i class="fa-solid fa-user-check"></i></div>
              <h4>4</h4>
              <p>Following</p>
            </div>

            <div class="stat">
              <div class="icon"><i class="fa-solid fa-star"></i></div>
              <h4>1</h4>
              <p>Starred</p>
            </div>
          </div>

          <div class="mini-links">
            <a class="mini-link" href="https://github.com/OcoderX" target="_blank">
              <span><i class="fa-brands fa-github"></i> GitHub Profile</span>
              <i class="fa-solid fa-arrow-up-right-from-square"></i>
            </a>

            <a class="mini-link" href="https://t.me/OcoderXbot" target="_blank">
              <span><i class="fa-brands fa-telegram"></i> Telegram</span>
              <i class="fa-solid fa-arrow-up-right-from-square"></i>
            </a>
          </div>
        </aside>
      </div>
    </section>

    <section class="grid">
      <div class="section-card">
        <div class="card-title">
          <h3><i class="fa-solid fa-code"></i> Tech Stack</h3>
        </div>

        <div class="skills">
          <span class="chip">Python</span>
          <span class="chip">Git</span>
          <span class="chip">GitHub</span>
          <span class="chip">HTML</span>
          <span class="chip">CSS</span>
          <span class="chip">JavaScript</span>
          <span class="chip">Telegram Bot</span>
          <span class="chip">Responsive UI</span>
          <span class="chip">AI Learning</span>
          <span class="chip">Cybersecurity Learning</span>
        </div>
      </div>

      <div class="section-card">
        <div class="card-title">
          <h3><i class="fa-solid fa-address-card"></i> About Me</h3>
        </div>

        <p style="line-height:1.9; color:#d6dee6;">
          I’m building my developer journey through real projects, practical coding,
          community activity, and continuous learning. This profile combines a GitHub README
          look with a modern portfolio presentation so it feels both authentic and premium.
        </p>
      </div>

      <div class="section-card">
        <div class="card-title">
          <h3><i class="fa-solid fa-diagram-project"></i> Featured Projects</h3>
        </div>

        <div class="projects">
          <div class="project">
            <h4><i class="fa-solid fa-robot"></i> robo_ai</h4>
            <p>
              Collaborative repository with AI-related direction. Good to present as an
              early project in your profile showcase.
            </p>
            <div class="project-meta">
              <span class="tag">AI</span>
              <span class="tag">Collaboration</span>
              <span class="tag">GitHub Project</span>
            </div>
          </div>

          <div class="project">
            <h4><i class="fa-brands fa-telegram"></i> tatu</h4>
            <p>
              Python-based Telegram automation/tooling project. Great candidate to highlight
              practical coding and scripting experience.
            </p>
            <div class="project-meta">
              <span class="tag">Python</span>
              <span class="tag">Telegram Bot</span>
              <span class="tag">Automation</span>
            </div>
          </div>
        </div>
      </div>

      <div class="section-card" id="certificates">
        <div class="card-title">
          <h3><i class="fa-solid fa-certificate"></i> Coursera Certificates</h3>
        </div>

        <div class="cert-list">
          <div class="cert">
            <div class="cert-top">
              <h4><i class="fa-solid fa-brain"></i> AI Certificate</h4>
              <small>Coursera • Add when ready</small>
            </div>
            <div class="placeholder">
              Place your AI certificate title here. Example:
              “Generative AI”, “AI For Everyone”, “Machine Learning”, or any Coursera AI program name.
            </div>
          </div>

          <div class="cert">
            <div class="cert-top">
              <h4><i class="fa-solid fa-shield-halved"></i> Cybersecurity Certificate</h4>
              <small>Coursera • Add when ready</small>
            </div>
            <div class="placeholder">
              Place your cybersecurity certificate title here. Example:
              “Google Cybersecurity Professional Certificate” or your completed security course name.
            </div>
          </div>
        </div>
      </div>
    </section>

    <p class="footer-note">
      Designed in GitHub README spirit • enhanced with glassmorphism, hover interactions, and responsive portfolio layout
    </p>
  </main>
</body>
</html>
