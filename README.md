
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=DM+Sans:wght@300;400;500;600&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body, .readme-root {
    font-family: 'DM Sans', sans-serif;
    background: #0d1117;
    color: #e6edf3;
    min-height: 100vh;
  }

  .readme-root {
    max-width: 860px;
    margin: 0 auto;
    padding: 32px 24px;
  }

  /* --- HERO --- */
  .hero {
    position: relative;
    padding: 40px 0 32px;
    border-bottom: 1px solid #21262d;
    margin-bottom: 36px;
  }

  .hero-grid {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 24px;
    align-items: center;
  }

  .hero-greeting {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: #58a6ff;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .hero-name {
    font-size: 40px;
    font-weight: 600;
    line-height: 1.1;
    color: #f0f6fc;
    margin-bottom: 10px;
  }

  .hero-name span {
    color: #58a6ff;
  }

  .hero-role {
    font-size: 15px;
    color: #8b949e;
    font-weight: 400;
    line-height: 1.6;
    max-width: 480px;
  }

  .hero-avatar {
    width: 88px;
    height: 88px;
    border-radius: 50%;
    background: linear-gradient(135deg, #1f6feb 0%, #388bfd 50%, #58a6ff 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Space Mono', monospace;
    font-size: 26px;
    font-weight: 700;
    color: #fff;
    flex-shrink: 0;
    border: 2px solid #30363d;
  }

  .status-row {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-top: 16px;
    flex-wrap: wrap;
  }

  .status-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: #3fb950;
    flex-shrink: 0;
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .status-text {
    font-size: 13px;
    color: #3fb950;
    font-family: 'Space Mono', monospace;
  }

  /* --- SECTION TITLES --- */
  .section {
    margin-bottom: 32px;
  }

  .section-title {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #58a6ff;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: #21262d;
  }

  /* --- ABOUT CARD --- */
  .about-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 20px 22px;
    font-size: 14px;
    line-height: 1.75;
    color: #c9d1d9;
  }

  .about-card p + p { margin-top: 10px; }

  .quote-block {
    margin-top: 16px;
    padding: 12px 16px;
    border-left: 3px solid #58a6ff;
    background: #0d1117;
    border-radius: 0 6px 6px 0;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: #58a6ff;
    letter-spacing: 0.5px;
  }

  /* --- TECH STACK --- */
  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 12px;
  }

  .stack-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 16px 18px;
    transition: border-color 0.2s;
  }

  .stack-card:hover {
    border-color: #388bfd;
  }

  .stack-category {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: #6e7681;
    text-transform: uppercase;
    margin-bottom: 12px;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 10px;
    border-radius: 6px;
    font-size: 12px;
    font-weight: 500;
    font-family: 'DM Sans', sans-serif;
    border: 1px solid transparent;
    letter-spacing: 0.2px;
  }

  .badge-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* Colors per tech */
  .b-html   { background: #3d1f0d; border-color: #e34c26; color: #e34c26; }
  .b-html   .badge-dot { background: #e34c26; }
  .b-css    { background: #0d1e3d; border-color: #264de4; color: #6ca5ff; }
  .b-css    .badge-dot { background: #264de4; }
  .b-js     { background: #3d2f00; border-color: #f7df1e; color: #f7df1e; }
  .b-js     .badge-dot { background: #f7df1e; }
  .b-react  { background: #0a2a3d; border-color: #61dafb; color: #61dafb; }
  .b-react  .badge-dot { background: #61dafb; }
  .b-node   { background: #0d2d0d; border-color: #3fb950; color: #3fb950; }
  .b-node   .badge-dot { background: #3fb950; }
  .b-express{ background: #1a1a1a; border-color: #888; color: #aaa; }
  .b-express .badge-dot { background: #888; }
  .b-mongo  { background: #0d2d14; border-color: #4db33d; color: #4db33d; }
  .b-mongo  .badge-dot { background: #4db33d; }
  .b-git    { background: #3d1a0d; border-color: #f05032; color: #f05032; }
  .b-git    .badge-dot { background: #f05032; }
  .b-vscode { background: #0d1f3d; border-color: #007acc; color: #51aaff; }
  .b-vscode .badge-dot { background: #007acc; }
  .b-rest   { background: #1a2a1a; border-color: #58a6ff; color: #58a6ff; }
  .b-rest   .badge-dot { background: #58a6ff; }
  .b-github { background: #1a1a2e; border-color: #8957e5; color: #b98dff; }
  .b-github .badge-dot { background: #8957e5; }

  /* --- FOCUS AREA --- */
  .focus-list {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .focus-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 12px 16px;
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 8px;
    font-size: 14px;
    color: #c9d1d9;
  }

  .focus-icon {
    width: 28px; height: 28px;
    border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 13px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  .fi-blue  { background: #0d1f3d; color: #58a6ff; border: 1px solid #1f3d6e; }
  .fi-green { background: #0d2d14; color: #3fb950; border: 1px solid #1a4d26; }
  .fi-amber { background: #3d2f00; color: #e3b341; border: 1px solid #6e5200; }

  .focus-item strong {
    color: #f0f6fc;
    font-weight: 500;
    display: block;
    margin-bottom: 2px;
    font-size: 13.5px;
  }

  /* --- STATS --- */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 12px;
  }

  .stat-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 18px;
    text-align: center;
  }

  .stat-card img {
    width: 100%;
    border-radius: 6px;
  }

  .stat-placeholder {
    background: #0d1117;
    border-radius: 6px;
    padding: 14px 10px;
    font-size: 11.5px;
    color: #8b949e;
    font-family: 'Space Mono', monospace;
    line-height: 1.6;
  }

  .stat-placeholder .stat-label {
    display: block;
    font-size: 10px;
    color: #6e7681;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  .stat-placeholder .stat-value {
    color: #f0f6fc;
    font-size: 22px;
    font-weight: 700;
  }

  /* --- CONNECT --- */
  .connect-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 9px 18px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 500;
    text-decoration: none;
    font-family: 'DM Sans', sans-serif;
    transition: opacity 0.15s;
    cursor: pointer;
  }

  .connect-btn:hover { opacity: 0.85; }

  .btn-github { background: #21262d; border: 1px solid #30363d; color: #f0f6fc; }
  .btn-linkedin { background: #0b3d6b; border: 1px solid #1366b0; color: #58a6ff; }

  /* --- FOOTER LINE --- */
  .footer-line {
    margin-top: 36px;
    padding-top: 20px;
    border-top: 1px solid #21262d;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
  }

  .footer-mono {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: #6e7681;
    letter-spacing: 1px;
  }

  .footer-mono span { color: #3fb950; }
</style>

<div class="readme-root">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-grid">
      <div>
        <div class="hero-greeting">// hello, world</div>
        <div class="hero-name">Satyam <span>Singh</span></div>
        <div class="hero-role">Full Stack Web Developer · Backend Systems · Modern JavaScript</div>
        <div class="status-row">
          <div class="status-dot"></div>
          <div class="status-text">Open to opportunities</div>
        </div>
      </div>
      <div class="hero-avatar">SS</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-title">About me</div>
    <div class="about-card">
      <p>I'm a developer who enjoys turning ideas into real, working products. My focus is building efficient backend systems while also crafting clean, responsive user interfaces.</p>
      <p>I work with modern JavaScript technologies and continuously deepen my understanding of how real-world applications are designed and scaled. Currently strengthening backend skills through projects that prioritize performance, simplicity, and clean architecture.</p>
      <div class="quote-block">⭐ Consistency beats intensity in the long run.</div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-title">Tech stack</div>
    <div class="stack-grid">
      <div class="stack-card">
        <div class="stack-category">Frontend</div>
        <div class="badge-row">
          <span class="badge b-html"><span class="badge-dot"></span>HTML</span>
          <span class="badge b-css"><span class="badge-dot"></span>CSS</span>
          <span class="badge b-js"><span class="badge-dot"></span>JavaScript</span>
          <span class="badge b-react"><span class="badge-dot"></span>React</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-category">Backend</div>
        <div class="badge-row">
          <span class="badge b-node"><span class="badge-dot"></span>Node.js</span>
          <span class="badge b-express"><span class="badge-dot"></span>Express.js</span>
          <span class="badge b-rest"><span class="badge-dot"></span>REST APIs</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-category">Database</div>
        <div class="badge-row">
          <span class="badge b-mongo"><span class="badge-dot"></span>MongoDB</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-category">Tools</div>
        <div class="badge-row">
          <span class="badge b-git"><span class="badge-dot"></span>Git</span>
          <span class="badge b-github"><span class="badge-dot"></span>GitHub</span>
          <span class="badge b-vscode"><span class="badge-dot"></span>VS Code</span>
        </div>
      </div>
    </div>
  </div>

  <!-- CURRENT FOCUS -->
  <div class="section">
    <div class="section-title">Current focus</div>
    <div class="focus-list">
      <div class="focus-item">
        <div class="focus-icon fi-blue">▣</div>
        <div>
          <strong>Building Full Stack Projects</strong>
          Developing end-to-end applications that connect frontend UX with robust backend logic.
        </div>
      </div>
      <div class="focus-item">
        <div class="focus-icon fi-green">⬡</div>
        <div>
          <strong>Deepening Backend Knowledge</strong>
          Exploring scalable architectures, API design patterns, and server-side performance techniques.
        </div>
      </div>
      <div class="focus-item">
        <div class="focus-icon fi-amber">◈</div>
        <div>
          <strong>Writing Clean & Maintainable Code</strong>
          Practicing SOLID principles and code organization for long-term project sustainability.
        </div>
      </div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-title">GitHub stats</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-placeholder">
          <span class="stat-label">Top Languages</span>
          <div style="display:flex; gap:8px; justify-content:center; flex-wrap:wrap; margin-top:8px;">
            <span class="badge b-js" style="font-size:11px;"><span class="badge-dot"></span>JavaScript</span>
            <span class="badge b-css" style="font-size:11px;"><span class="badge-dot"></span>CSS</span>
            <span class="badge b-html" style="font-size:11px;"><span class="badge-dot"></span>HTML</span>
          </div>
          <div style="margin-top:12px; font-size:10px; color:#6e7681;">
            Live stats via GitHub Readme Stats
          </div>
        </div>
      </div>
      <div class="stat-card">
        <div class="stat-placeholder">
          <span class="stat-label">Activity</span>
          <div class="stat-value" style="font-size:14px; margin-top:4px;">github.com</div>
          <div style="color:#58a6ff; margin-top:6px; font-size:11px;">@Satyamsinghweb</div>
          <div style="margin-top:10px; font-size:10px; color:#6e7681;">Add GitHub Readme Stats widgets</div>
        </div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-title">Connect with me</div>
    <div class="connect-row">
      <a class="connect-btn btn-github" href="https://github.com/Satyamsinghweb" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
      <a class="connect-btn btn-linkedin" href="https://www.linkedin.com/in/satyam1604" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer-line">
    <div class="footer-mono">Satyam Singh · Full Stack Developer</div>
    <div class="footer-mono"><span>▲</span> Building something great</div>
  </div>

</div>
