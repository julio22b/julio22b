<!DOCTYPE html>
<html>
<head>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Mono:wght@400;500&display=swap');

{ margin: 0; padding: 0; box-sizing: border-box; }

body {
background: #0d1117;
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
color: #e6edf3;
padding: 32px;
max-width: 860px;
margin: 0 auto;
}

.banner {
background: #0a0f1e;
border-radius: 16px;
padding: 48px 40px 40px;
position: relative;
overflow: hidden;
font-family: 'Syne', sans-serif;
margin-bottom: 32px;
}

.grid-bg {
position: absolute;
inset: 0;
background-image:
linear-gradient(rgba(56, 130, 246, 0.06) 1px, transparent 1px),
linear-gradient(90deg, rgba(56, 130, 246, 0.06) 1px, transparent 1px);
background-size: 40px 40px;
animation: gridDrift 20s linear infinite;
}

@keyframes gridDrift {
0% { background-position: 0 0; }
100% { background-position: 40px 40px; }
}

.glow-orb {
position: absolute;
border-radius: 50%;
filter: blur(60px);
opacity: 0.35;
}

.orb1 { width: 260px; height: 260px; background: #1a4fd6; top: -80px; left: -60px; }

.orb2 { width: 200px; height: 200px; background: #0ea5e9; bottom: -60px; right: 40px; }

.content { position: relative; z-index: 2; }

.tag {
display: inline-block;
font-family: 'DM Mono', monospace;
font-size: 11px;
letter-spacing: 0.12em;
color: #60a5fa;
background: rgba(96, 165, 250, 0.12);
border: 1px solid rgba(96, 165, 250, 0.25);
padding: 4px 12px;
border-radius: 999px;
margin-bottom: 20px;
animation: fadeUp 0.6s ease both;
}

.name {
font-size: 52px;
font-weight: 800;
color: #ffffff;
line-height: 1;
margin: 0 0 8px;
animation: fadeUp 0.6s 0.1s ease both;
letter-spacing: -1px;
}

.name span {
background: linear-gradient(90deg, #60a5fa, #38bdf8);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
}

.title {
font-family: 'DM Mono', monospace;
font-size: 14px;
color: #94a3b8;
margin: 0 0 32px;
animation: fadeUp 0.6s 0.2s ease both;
letter-spacing: 0.05em;
}

.divider {
width: 48px;
height: 2px;
background: linear-gradient(90deg, #3b82f6, transparent);
margin-bottom: 28px;
animation: fadeUp 0.6s 0.25s ease both;
}

.stats {
display: flex;
gap: 32px;
margin-bottom: 32px;
animation: fadeUp 0.6s 0.3s ease both;
}

.stat-num {
font-size: 22px;
font-weight: 800;
color: #f1f5f9;
}

.stat-num span { color: #60a5fa; }
.stat-label {
font-family: 'DM Mono', monospace;
font-size: 10px;
color: #64748b;
letter-spacing: 0.1em;
text-transform: uppercase;
margin-top: 2px;
}

.stack {
display: flex;
gap: 10px;
flex-wrap: wrap;
animation: fadeUp 0.6s 0.4s ease both;
}

.chip {
display: flex;
align-items: center;
gap: 6px;
background: rgba(255,255,255,0.05);
border: 1px solid rgba(255,255,255,0.1);
border-radius: 8px;
padding: 6px 12px;
color: #e2e8f0;
font-family: 'DM Mono', monospace;
font-size: 12px;
transition: all 0.2s ease;
}

.chip:hover {
background: rgba(96, 165, 250, 0.12);
border-color: rgba(96, 165, 250, 0.35);
transform: translateY(-2px);
}

.chip-dot {
width: 7px;
height: 7px;
border-radius: 50%;
display: inline-block;
}

@keyframes fadeUp {
from { opacity: 0; transform: translateY(14px); }
to   { opacity: 1; transform: translateY(0); }
}

.bottom-row {
display: flex;
justify-content: space-between;
align-items: flex-end;
margin-top: 32px;
padding-top: 24px;
border-top: 1px solid rgba(255,255,255,0.07);
animation: fadeUp 0.6s 0.5s ease both;
}

.status {
display: flex;
align-items: center;
gap: 8px;
font-family: 'DM Mono', monospace;
font-size: 11px;
color: #64748b;
}

.status-dot {
width: 7px;
height: 7px;
border-radius: 50%;
background: #22c55e;
box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.5);
animation: pulse 2s infinite;
}

@keyframes pulse {
0%   { box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.5); }
70%  { box-shadow: 0 0 0 6px rgba(34, 197, 94, 0); }
100% { box-shadow: 0 0 0 0 rgba(34, 197, 94, 0); }
}

.link {
font-family: 'DM Mono', monospace;
font-size: 11px;
color: #3b82f6;
text-decoration: none;
letter-spacing: 0.05em;
}

.link:hover { color: #60a5fa; }
/* Bio section */
.bio {
padding: 0 4px;
line-height: 1.75;
font-size: 15px;
color: #c9d1d9;
}

.bio p { margin-bottom: 20px; }

.bio strong { color: #e6edf3; }

.bio ul {
list-style: none;
padding: 0;
margin-bottom: 20px;
}

.bio ul li {
display: flex;
gap: 10px;
margin-bottom: 12px;
align-items: flex-start;
}

.bio ul li .icon { flex-shrink: 0; font-size: 16px; margin-top: 2px; }

.bio ul li .label {
color: #e6edf3;
font-weight: 600;
}

</style>
</head>
<body>
<div class="banner">
  <div class="grid-bg"></div>
  <div class="glow-orb orb1"></div>
  <div class="glow-orb orb2"></div>
  <div class="content">
    <div class="tag">// senior frontend engineer</div>
    <h1 class="name">Hi, I'm <span>Julio</span></h1>
    <p class="title">Building reliable, high-scale frontend systems</p>
    <div class="divider"></div>
<div class="stats">
  <div class="stat">
    <div class="stat-num"><span>88%</span></div>
    <div class="stat-label">Test coverage</div>
  </div>
  <div class="stat">
    <div class="stat-num"><span>73%</span></div>
    <div class="stat-label">Error reduction</div>
  </div>
  <div class="stat">
    <div class="stat-num"><span>5+</span></div>
    <div class="stat-label">Years remote</div>
  </div>
</div>

<div class="stack">
  <div class="chip"><span class="chip-dot" style="background:#61dafb;"></span>React</div>
  <div class="chip"><span class="chip-dot" style="background:#3178c6;"></span>TypeScript</div>
  <div class="chip"><span class="chip-dot" style="background:#c21325;"></span>Jest</div>
  <div class="chip"><span class="chip-dot" style="background:#3c873a;"></span>Node.js</div>
  <div class="chip"><span class="chip-dot" style="background:#336791;"></span>PostgreSQL</div>
  <div class="chip"><span class="chip-dot" style="background:#e97627;"></span>NoSQL</div>
</div>

<div class="bottom-row">
  <div class="status">
    <div class="status-dot"></div>
    Open to remote opportunities
  </div>
  <a class="link" href="https://juliobermudez.netlify.app/">juliobermudez.netlify.app →</a>
</div>
  </div>
</div>
<div class="bio">
  <p>
    Dedicated Senior Frontend Engineer with 5+ years of remote experience specializing in
    <strong>Warehouse Management Systems (WMS)</strong> and high-scale data flows.
  </p>
  <ul>
    <li>
      <span class="icon">🚀</span>
      <span><span class="label">Reliability:</span> Scaled test coverage from 36% → 88% using Jest and Selenium — turning a fragile codebase into a ship-with-confidence system.</span>
    </li>
    <li>
      <span class="icon">🗂️</span>
      <span><span class="label">Efficiency:</span> Engineered validation features that slashed data entry errors by 73%, directly reducing operational cost.</span>
    </li>
    <li>
      <span class="icon">🔧</span>
      <span><span class="label">Modernization:</span> Led legacy migrations to ES6+, cutting development time by 17%.</span>
    </li>
  </ul>
  <p>
    Currently architecting scalable WMS solutions and refining full-stack patterns with Node.js and SQL/NoSQL databases.
  </p>
</div>
</body>
</html>
