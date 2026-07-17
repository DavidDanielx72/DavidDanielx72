<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>David Daniel Sepkitt · iOS README</title>
  <!-- Font & Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f2f2f7;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
      padding: 24px 16px 40px;
      display: flex;
      justify-content: center;
    }

    .readme-card {
      max-width: 820px;
      width: 100%;
      background: #ffffff;
      border-radius: 36px;
      box-shadow: 0 12px 40px rgba(0, 0, 0, 0.08), 0 4px 12px rgba(0, 0, 0, 0.02);
      padding: 32px 24px 40px;
    }

    /* ----- iOS MESSAGE BUBBLE (header replacement) ----- */
    .ios-message-group {
      display: flex;
      flex-direction: column;
      gap: 10px;
      margin-bottom: 28px;
      padding: 8px 0 4px;
    }

    .message-row {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      opacity: 0;
      transform: translateY(12px);
      animation: messagePop 0.45s cubic-bezier(0.22, 0.68, 0, 1) forwards;
    }

    .message-row:nth-child(1) { animation-delay: 0.05s; }
    .message-row:nth-child(2) { animation-delay: 0.25s; }
    .message-row:nth-child(3) { animation-delay: 0.45s; }

    @keyframes messagePop {
      0% { opacity: 0; transform: translateY(16px) scale(0.96); }
      100% { opacity: 1; transform: translateY(0) scale(1); }
    }

    .message-bubble {
      background: #e9e9ed;
      padding: 12px 18px;
      border-radius: 22px 22px 22px 6px;
      font-size: 1.1rem;
      font-weight: 500;
      color: #1c1c1e;
      box-shadow: 0 1px 2px rgba(0,0,0,0.04);
      max-width: 85%;
      word-break: break-word;
      line-height: 1.4;
      letter-spacing: -0.01em;
      border: 0.5px solid rgba(0,0,0,0.02);
    }

    .avatar {
      flex-shrink: 0;
      width: 40px;
      height: 40px;
      background: #007aff;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-weight: 600;
      font-size: 1rem;
      background-image: linear-gradient(145deg, #007aff, #0055b3);
      box-shadow: 0 2px 6px rgba(0, 122, 255, 0.2);
      margin-top: 2px;
    }

    .message-meta {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-top: 4px;
      margin-left: 56px;
      font-size: 0.7rem;
      color: #8e8e93;
      font-weight: 400;
      letter-spacing: 0.2px;
    }

    .message-meta i {
      font-size: 0.6rem;
      opacity: 0.7;
    }

    .header-gif {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      flex-wrap: wrap;
    }

    .header-gif img {
      height: 28px;
      width: auto;
      border-radius: 8px;
    }

    /* ----- rest of README styling ----- */
    .about-section, .tech-section, .projects-section, .connect-section {
      margin-top: 32px;
    }

    .section-title {
      font-size: 1.3rem;
      font-weight: 600;
      letter-spacing: -0.3px;
      color: #1c1c1e;
      padding-bottom: 6px;
      border-bottom: 2px solid #f2f2f7;
      margin-bottom: 18px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .section-title i {
      color: #007aff;
      font-size: 1.2rem;
    }

    .about-text {
      font-size: 1rem;
      line-height: 1.6;
      color: #2c2c2e;
      background: #f8f8fc;
      padding: 20px 22px;
      border-radius: 24px;
      border: 1px solid #f0f0f5;
    }

    .about-text p {
      margin-bottom: 0;
    }

    .badge-list {
      display: flex;
      flex-wrap: wrap;
      gap: 12px 18px;
      background: #f8f8fc;
      padding: 18px 22px;
      border-radius: 24px;
      border: 1px solid #f0f0f5;
      margin-top: 6px;
    }

    .badge-list span {
      font-size: 0.95rem;
      display: flex;
      align-items: center;
      gap: 10px;
      color: #1c1c1e;
    }

    .badge-list i {
      color: #007aff;
      width: 20px;
      font-size: 1.1rem;
    }

    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 16px 24px;
      background: #f8f8fc;
      padding: 20px 16px;
      border-radius: 28px;
      border: 1px solid #f0f0f5;
      margin-top: 8px;
    }

    .tech-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 4px;
      font-size: 0.8rem;
      font-weight: 500;
      color: #3a3a3c;
      min-width: 60px;
    }

    .tech-item img {
      height: 42px;
      width: 42px;
      object-fit: contain;
    }

    .project-card {
      background: #f8f8fc;
      border-radius: 24px;
      padding: 18px 22px;
      border: 1px solid #f0f0f5;
      margin-bottom: 16px;
    }

    .project-card strong {
      color: #1c1c1e;
      font-weight: 600;
    }

    .project-card a {
      color: #007aff;
      text-decoration: none;
      font-weight: 500;
      border-bottom: 1.5px dotted rgba(0, 122, 255, 0.25);
    }

    .project-card a:hover {
      border-bottom: 1.5px solid #007aff;
    }

    .connect-wrapper {
      display: flex;
      justify-content: center;
      gap: 24px;
      margin-top: 16px;
      background: #f8f8fc;
      padding: 18px 20px;
      border-radius: 40px;
      border: 1px solid #f0f0f5;
    }

    .connect-wrapper a {
      color: #1c1c1e;
      font-size: 2.2rem;
      transition: all 0.2s ease;
      display: inline-flex;
    }

    .connect-wrapper a:hover {
      color: #007aff;
      transform: scale(1.05);
    }

    hr {
      border: none;
      border-top: 2px solid #f0f0f5;
      margin: 32px 0 20px;
    }

    .text-muted {
      color: #8e8e93;
      font-size: 0.9rem;
    }

    @media (max-width: 540px) {
      .readme-card { padding: 20px 16px; }
      .message-bubble { font-size: 1rem; padding: 10px 14px; max-width: 90%; }
      .avatar { width: 34px; height: 34px; font-size: 0.8rem; }
      .message-meta { margin-left: 48px; }
      .tech-item img { height: 34px; width: 34px; }
    }
  </style>
</head>
<body>
<div class="readme-card">

  <!-- ===== IOS MESSAGE HEADER ===== -->
  <div class="ios-message-group">
    <!-- message 1: name + gif -->
    <div class="message-row">
      <div class="avatar">👨‍💻</div>
      <div>
        <div class="message-bubble">
          <span class="header-gif">
            <img src="https://media.giphy.com/media/xTiTnxpQ3ghPiB2Hp6/giphy.gif" width="24" height="24" alt="wave">
            <strong>David Daniel Sepkitt</strong>
            <img src="https://media.giphy.com/media/xTiTnxpQ3ghPiB2Hp6/giphy.gif" width="24" height="24" alt="wave">
          </span>
        </div>
        <div class="message-meta">
          <i class="fas fa-check-circle" style="color: #34c759;"></i> Read · Today 14:32
        </div>
      </div>
    </div>

    <!-- message 2: role -->
    <div class="message-row">
      <div class="avatar">📱</div>
      <div>
        <div class="message-bubble" style="background: #e9e9ed;">
          <span style="font-weight: 600; color: #0033A0;">3rd Year ICT Student</span> 
          <span style="margin:0 6px;">·</span> 
          <span style="font-weight: 600; color: #0033A0;">Front-End Developer</span>
        </div>
        <div class="message-meta">
          <i class="fas fa-check-circle" style="color: #34c759;"></i> Read · 14:33
        </div>
      </div>
    </div>

    <!-- message 3: about me teaser -->
    <div class="message-row">
      <div class="avatar">🧑‍🎓</div>
      <div>
        <div class="message-bubble" style="background: #e9e9ed; font-weight: 500;">
          <i class="fas fa-arrow-right" style="color: #007aff; margin-right: 6px;"></i> 
          About Me · Cape Town, SA
        </div>
        <div class="message-meta">
          <i class="fas fa-check-circle" style="color: #34c759;"></i> Read · 14:34
        </div>
      </div>
    </div>
  </div>
  <!-- END iOS MESSAGE HEADER -->

  <!-- ===== ABOUT ME ===== -->
  <div class="about-section">
    <div class="section-title">
      <i class="fas fa-user-graduate"></i> About Me
    </div>
    <div class="about-text">
      <p>
        I am from Cape Town, South Africa. I am currently a third year student at the Cape Peninsula University of Technology, pursuing a Diploma in Information and Communication Technology in Applications Development. I am passionate about everything tech-related and enjoy learning new technologies to constantly improve my skills and broaden my knowledge.
      </p>
    </div>

    <div class="badge-list" style="margin-top: 18px;">
      <span><i class="fas fa-seedling"></i> Currently learning: <strong>Advanced Java, React, C & C++</strong></span>
      <span><i class="fas fa-laptop-code"></i> Self-learned: <strong>React, TypeScript, CSS, JavaScript, WordPress</strong></span>
      <span><i class="fas fa-brain"></i> Love learning new technologies</span>
      <span><i class="fas fa-bullseye"></i> Goal: grow into a well-rounded developer</span>
    </div>
  </div>

  <!-- ===== TECH STACK ===== -->
  <div class="tech-section">
    <div class="section-title">
      <i class="fas fa-code"></i> Tech Stack
    </div>

    <div style="font-weight: 600; font-size: 0.9rem; color: #3a3a3c; margin: 6px 0 8px 8px;">💻 Languages &amp; Technologies</div>
    <div class="tech-grid">
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=java" alt="Java"><span>Java</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=js" alt="JavaScript"><span>JS</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=ts" alt="TypeScript"><span>TS</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=html" alt="HTML"><span>HTML</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=css" alt="CSS"><span>CSS</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=react" alt="React"><span>React</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=mysql" alt="SQL"><span>SQL</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=wordpress" alt="WordPress"><span>WP</span></div>
    </div>

    <div style="font-weight: 600; font-size: 0.9rem; color: #3a3a3c; margin: 22px 0 8px 8px;">🧰 Tools &amp; IDEs</div>
    <div class="tech-grid">
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=git" alt="Git"><span>Git</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=github" alt="GitHub"><span>GitHub</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=vscode" alt="VS Code"><span>VS Code</span></div>
      <div class="tech-item"><img src="https://skillicons.dev/icons?i=figma" alt="Figma"><span>Figma</span></div>
      <div class="tech-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/intellij/intellij-original.svg" height="42" alt="IntelliJ"><span>IntelliJ</span></div>
      <div class="tech-item"><img src="https://upload.wikimedia.org/wikipedia/commons/9/98/Apache_NetBeans_Logo.svg" height="42" alt="NetBeans"><span>NetBeans</span></div>
    </div>
  </div>

  <!-- ===== PROJECTS ===== -->
  <div class="projects-section">
    <div class="section-title">
      <i class="fas fa-folder-open"></i> Projects
    </div>

    <div class="project-card">
      <strong>🌿 Rietfontein Website (Front-End)</strong>
      <p style="margin-top: 6px; color: #2c2c2e;">
        Updated the front end of <a href="https://rietfontein.co.za/" target="_blank">rietfontein.co.za</a> · Modernized look &amp; feel according to owner’s vision. Implemented responsive design using <strong>WordPress</strong> (HTML, CSS, JS, PHP).
      </p>
    </div>

    <div class="project-card">
      <strong>📁 My Portfolio Website</strong>
      <p style="margin-top: 6px; color: #2c2c2e;">
        View full portfolio, CV, and mock interview video: 
        <a href="https://daviddanielx72.github.io/" target="_blank">David Daniel Portfolio</a>
      </p>
    </div>
  </div>

  <!-- ===== CONNECT ===== -->
  <div class="connect-section">
    <div class="section-title">
      <i class="fas fa-share-alt"></i> Connect With Me
    </div>
    <div class="connect-wrapper">
      <a href="https://www.linkedin.com/in/david-sepkitt-811837362/" target="_blank" aria-label="LinkedIn">
        <i class="fab fa-linkedin" style="color: #0a66c2;"></i>
      </a>
    </div>
    <p style="text-align: center; font-size: 0.75rem; color: #8e8e93; margin-top: 18px; letter-spacing: 0.3px;">
      <i class="fas fa-message" style="margin-right: 4px;"></i> iOS message style · David Daniel Sepkitt
    </p>
  </div>

  <div style="margin-top: 24px; border-top: 1px solid #f0f0f5; padding-top: 14px; font-size: 0.7rem; color: #8e8e93; text-align: center;">
    <i class="fas fa-info-circle"></i> All information from original README — preserved.
  </div>
</div>
</body>
</html>
