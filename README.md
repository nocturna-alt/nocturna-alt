<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Nocturna • Abril Minerva Estrada Montaño</title>
  <meta name="description" content="Abril Minerva — Data Scientist & Data Engineer. Ethical AI, clean systems, and narrative-driven analytics. IIMAS–UNAM." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0b0b0c; --panel: rgba(255,255,255,.03); --panel-2: rgba(255,255,255,.02);
      --text: #e6e6e6; --muted:#9aa0a6; --line: rgba(255,255,255,.12);
      --aqua:#64ffda; --violet:#bb86fc; --rose:#cf6679; --code:#081018;
      --glow: 0 0 20px rgba(100, 255, 218, 0.3);
      --violet-glow: 0 0 20px rgba(187, 134, 252, 0.3);
      --rose-glow: 0 0 20px rgba(207, 102, 121, 0.3);
    }
    
    *{box-sizing:border-box}
    html,body{height:100%}
    
    body{
      margin:0; color:var(--text); 
      background: linear-gradient(135deg, #090a0f 0%, #14151b 50%, #1a1b23 100%);
      background-attachment: fixed;
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif; 
      line-height:1.6; padding:24px;
      position: relative;
    }
    
    /* Animated background particles */
    body::before {
      content: '';
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background-image: 
        radial-gradient(circle at 20% 80%, rgba(100, 255, 218, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 80% 20%, rgba(187, 134, 252, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 40% 40%, rgba(207, 102, 121, 0.1) 0%, transparent 50%);
      animation: float 20s ease-in-out infinite;
      z-index: -1;
    }
    
    @keyframes float {
      0%, 100% { transform: translate(0, 0) rotate(0deg); }
      33% { transform: translate(30px, -30px) rotate(120deg); }
      66% { transform: translate(-20px, 20px) rotate(240deg); }
    }
    
    .wrap{max-width:1100px;margin:0 auto; position: relative;}
    
    header{ text-align:center; margin: 6vh 0 4vh}
    
    .hero-gif {
      margin: 2rem 0;
      filter: drop-shadow(var(--glow));
      border-radius: 16px;
      overflow: hidden;
      position: relative;
    }
    
    .hero-gif::after {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(45deg, transparent, rgba(100, 255, 218, 0.1), transparent);
      animation: scan 3s linear infinite;
    }
    
    @keyframes scan {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }
    
    .title{
      font-family:"JetBrains Mono",monospace; font-weight:700; 
      font-size:clamp(32px,6vw,52px); letter-spacing:.5px;
      background:linear-gradient(45deg,var(--aqua),var(--violet),var(--rose)); 
      -webkit-background-clip:text; background-clip:text; -webkit-text-fill-color:transparent;
      text-shadow: var(--glow);
      animation: pulse 3s ease-in-out infinite;
      position: relative;
    }
    
    .title::after {
      content: '';
      position: absolute;
      bottom: -8px; left: 50%;
      transform: translateX(-50%);
      width: 60px; height: 2px;
      background: linear-gradient(90deg, var(--aqua), var(--violet), var(--rose));
      animation: glow-line 2s ease-in-out infinite alternate;
    }
    
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.8; }
    }
    
    @keyframes glow-line {
      from { box-shadow: 0 0 5px var(--aqua); }
      to { box-shadow: 0 0 20px var(--violet); }
    }
    
    .subtitle{color:var(--muted); margin-top:1rem; font-size: 1.1rem;}

    .panel{
      background:var(--panel); border:1px solid var(--line); border-radius:14px; 
      padding:28px; backdrop-filter: blur(8px); margin: 2rem 0;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .panel::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(45deg, transparent, rgba(100, 255, 218, 0.05), transparent);
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    .panel:hover::before {
      opacity: 1;
    }
    
    .panel:hover {
      border-color: var(--aqua);
      box-shadow: var(--glow);
      transform: translateY(-2px);
    }
    
    .grid{display:grid; gap:18px}
    .grid.cols-3{grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
    .grid.cols-2{grid-template-columns:repeat(auto-fit,minmax(320px,1fr))}
    
    h2{
      font-family:"JetBrains Mono",monospace; color:var(--aqua); 
      font-size:1.25rem; margin:0 0 14px;
      position: relative;
      display: inline-block;
    }
    
    h2::after {
      content: '';
      position: absolute;
      bottom: -4px; left: 0;
      width: 100%; height: 2px;
      background: linear-gradient(90deg, var(--aqua), var(--violet));
      animation: expand 0.5s ease-out;
    }
    
    @keyframes expand {
      from { width: 0; }
      to { width: 100%; }
    }
    
    h3{margin:.2rem 0 .6rem; font-size:1.05rem; color: var(--text);}
    
    .kicker{
      display:inline-block; font-family:"JetBrains Mono",monospace; 
      font-size:.8rem; letter-spacing:.2px; color:var(--muted); 
      border:1px dashed var(--line); border-radius:999px; padding:.3rem .7rem;
      animation: float-badge 2s ease-in-out infinite alternate;
      background: var(--panel-2);
    }
    
    @keyframes float-badge {
      from { transform: translateY(0); box-shadow: 0 0 5px rgba(100, 255, 218, 0.2); }
      to { transform: translateY(-2px); box-shadow: 0 0 15px rgba(100, 255, 218, 0.4); }
    }
    
    .highlight{
      background:linear-gradient(90deg,rgba(100,255,218,.12),rgba(187,134,252,.12)); 
      border-left:3px solid var(--aqua); padding:14px 16px; margin:14px 0; 
      border-radius:8px; position: relative;
      overflow: hidden;
    }
    
    .highlight::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 4px; height: 100%;
      background: linear-gradient(180deg, var(--aqua), var(--violet), var(--rose));
      animation: rainbow-border 3s linear infinite;
    }
    
    @keyframes rainbow-border {
      0% { background: linear-gradient(180deg, var(--aqua), var(--violet), var(--rose)); }
      33% { background: linear-gradient(180deg, var(--violet), var(--rose), var(--aqua)); }
      66% { background: linear-gradient(180deg, var(--rose), var(--aqua), var(--violet)); }
      100% { background: linear-gradient(180deg, var(--aqua), var(--violet), var(--rose)); }
    }

    .code{
      background:var(--code); border:1px solid #17202a; border-radius:10px; 
      padding:18px; font-family:"JetBrains Mono",monospace; font-size:.92rem; 
      color:#b7ffe8; overflow:auto; position: relative;
      box-shadow: inset 0 0 20px rgba(0,0,0,0.5);
    }
    
    .code::before {
      content: '// Terminal';
      position: absolute;
      top: 8px; right: 12px;
      font-size: 0.7rem;
      color: var(--muted);
      opacity: 0.7;
    }
    
    .code::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--aqua), transparent);
      animation: scan-line 2s linear infinite;
    }
    
    @keyframes scan-line {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }
    
    code{font-family:"JetBrains Mono",monospace}
    a{color:var(--aqua); text-decoration:none; transition: all 0.3s ease;}
    a:hover{text-decoration:underline wavy 1px; color: var(--violet); text-shadow: var(--violet-glow);}
    
    .pill{
      display:inline-block; padding:.35rem .7rem; border:1px solid var(--line); 
      border-radius:999px; color:#cdd3d8; margin:.2rem .25rem 0 0; 
      background:var(--panel-2); transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .pill::before {
      content: '';
      position: absolute;
      top: 0; left: -100%;
      width: 100%; height: 100%;
      background: linear-gradient(90deg, transparent, rgba(100, 255, 218, 0.2), transparent);
      transition: left 0.5s ease;
    }
    
    .pill:hover::before {
      left: 100%;
    }
    
    .pill:hover {
      border-color: var(--aqua);
      background: rgba(100, 255, 218, 0.1);
      transform: translateY(-1px);
      box-shadow: var(--glow);
    }
    
    .row{display:flex; gap:12px; flex-wrap:wrap}
    .cards{display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:14px}
    
    .card{
      background:var(--panel-2); border:1px solid var(--line); 
      border-radius:12px; padding:16px; transition: all 0.3s ease;
      position: relative; overflow: hidden;
    }
    
    .card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(135deg, transparent, rgba(187, 134, 252, 0.05), transparent);
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    .card:hover::before {
      opacity: 1;
    }
    
    .card:hover {
      border-color: var(--violet);
      transform: translateY(-3px);
      box-shadow: var(--violet-glow);
    }
    
    .soft{color:var(--muted)}
    
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin: 24px 0;
    }
    
    .stat-item {
      text-align: center;
      background: var(--panel-2);
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 20px;
      transition: all 0.3s ease;
      position: relative;
    }
    
    .stat-item:hover {
      border-color: var(--rose);
      box-shadow: var(--rose-glow);
      transform: scale(1.02);
    }
    
    .stat-item h3 {
      color: var(--rose);
      margin-bottom: 10px;
    }
    
    .spotify-embed {
      margin: 20px 0;
      text-align: center;
    }
    
    .spotify-embed img {
      border-radius: 12px;
      filter: drop-shadow(var(--violet-glow));
      transition: transform 0.3s ease;
    }
    
    .spotify-embed img:hover {
      transform: scale(1.02);
    }
    
    .baphy-section {
      background: var(--panel);
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 28px;
      margin: 2rem 0;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    
    .baphy-section::before {
      content: '🐈‍⬛';
      position: absolute;
      top: -15px;
      left: 20px;
      font-size: 2rem;
      background: var(--bg);
      padding: 0 10px;
      border-radius: 50%;
      animation: float-cat 3s ease-in-out infinite;
    }
    
    @keyframes float-cat {
      0%, 100% { transform: translateY(0) rotate(0deg); }
      50% { transform: translateY(-5px) rotate(5deg); }
    }
    
    .baphy-section .code {
      text-align: left;
      margin-top: 20px;
    }
    
    footer{margin:48px 0; text-align:center; color:var(--muted)}
    
    .quote-section {
      text-align: center;
      margin: 3rem 0;
      position: relative;
    }
    
    .quote-section img {
      border-radius: 8px;
      filter: drop-shadow(0 4px 8px rgba(0,0,0,0.3));
      transition: all 0.3s ease;
    }
    
    .quote-section img:hover {
      filter: drop-shadow(var(--glow));
      transform: scale(1.01);
    }
    
    .skills-visual {
      text-align: center;
      margin: 20px 0;
    }
    
    .skills-visual img {
      transition: transform 0.3s ease;
      filter: drop-shadow(0 2px 8px rgba(0,0,0,0.3));
    }
    
    .skills-visual img:hover {
      transform: scale(1.05);
      filter: drop-shadow(var(--glow));
    }
    
    .github-stats {
      text-align: center;
      margin: 20px 0;
    }
    
    .github-stats img {
      border-radius: 8px;
      margin: 10px;
      transition: all 0.3s ease;
    }
    
    .github-stats img:hover {
      transform: translateY(-2px);
      filter: drop-shadow(var(--violet-glow));
    }
    
    .philosophy-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 16px;
      margin: 20px 0;
    }
    
    .philosophy-item {
      background: var(--panel-2);
      border: 1px solid var(--line);
      border-radius: 8px;
      padding: 16px;
      text-align: center;
      transition: all 0.3s ease;
    }
    
    .philosophy-item:hover {
      border-color: var(--aqua);
      box-shadow: var(--glow);
      transform: translateY(-2px);
    }
    
    .emoji-large {
      font-size: 2rem;
      margin-bottom: 10px;
      display: block;
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="kicker">nocturna.dev</div>
      <h1 class="title">Abril Minerva — Digital Wanderer</h1>
      <p class="subtitle">Data Science • Data Engineering • Ethical AI • IIMAS–UNAM</p>
      <div class="hero-gif">
        <img src="https://media.giphy.com/media/siCRldvfdu3Ic/giphy.gif" alt="Digital Moon" width="500"/>
      </div>
    </header>

    <section class="panel" aria-labelledby="about">
      <h2 id="about">About</h2>
      <p>
        I'm a Data Scientist in training at <strong>IIMAS–UNAM</strong> with experience in <em>data engineering, automation, and predictive modeling</em>. I bridge technical expertise with philosophical inquiry and aesthetics. I transitioned from Computer Engineering to Data Science without losing a semester, and my work focuses on building AI systems that are efficient, ethical, and human‑centered.
      </p>
      <div class="highlight">
        <strong>Current focus:</strong> Automating business processes for SMEs & advancing research in ethical ML and NLP. Building technology that tells stories and changes perspectives.
      </div>
      
      <div class="code">
# Personal mission statement
def life_purpose():
    return {
        'learn': 'Something new every day',
        'create': 'Technology that matters', 
        'share': 'Knowledge freely and openly',
        'improve': 'Both code and world, one commit at a time'
    }

# What drives me
passions = ['AI ethics', 'Clean architecture', 'Narrative-driven data', 'Violin & music theory']
</div>
    </section>

    <section class="panel" aria-labelledby="stack">
      <h2 id="stack">Tech Stack</h2>
      <div class="skills-visual">
        <img src="https://skillicons.dev/icons?i=python,java,js,r,matlab,sklearn,tensorflow,pandas,mongodb,postgres,mysql,docker,gcp,git,linux,vscode&perline=8" alt="Tech Stack"/>
      </div>
      <div class="row">
        <span class="pill">Python</span><span class="pill">SQL</span><span class="pill">Java</span><span class="pill">JavaScript</span><span class="pill">Bash</span>
        <span class="pill">Scikit‑learn</span><span class="pill">XGBoost</span><span class="pill">TensorFlow</span>
        <span class="pill">Pandas</span><span class="pill">Dask</span><span class="pill">PySpark</span>
        <span class="pill">MongoDB</span><span class="pill">PostgreSQL</span><span class="pill">MySQL</span>
        <span class="pill">Airflow</span><span class="pill">Docker</span><span class="pill">GCP</span>
        <span class="pill">Plotly</span><span class="pill">Streamlit</span><span class="pill">Matplotlib</span>
      </div>
      
      <div class="code">
# Daily workflow
def daily_routine():
    morning = ['coffee', 'code_review', 'model_training']
    afternoon = ['debugging', 'feature_engineering', 'documentation']
    evening = ['research', 'violin_practice', 'feed_baphy']
    return {
        'productivity': sum([morning, afternoon, evening]),
        'balance': 'work_hard_live_well'
    }
</div>
    </section>

    <section class="panel" aria-labelledby="activity">
      <h2 id="activity">GitHub Activity</h2>
      <div class="github-stats">
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=carcinogenetista01&theme=tokyo-night" alt="Activity Graph"/>
      </div>
      
      <div class="stats-grid">
        <div class="stat-item">
          <h3>🔥 Current Streak</h3>
          <p>Building consistent coding habits</p>
        </div>
        <div class="stat-item">
          <h3>⚡ Languages</h3>
          <p>Python • Java • R • JavaScript</p>
        </div>
        <div class="stat-item">
          <h3>🚀 Focus Areas</h3>
          <p>ML • NLP • Data Engineering</p>
        </div>
      </div>
    </section>

    <section class="panel spotify-embed" aria-labelledby="music">
      <h2 id="music">Currently Vibing To</h2>
      <div class="spotify-embed">
        <img src="https://spotify-recently-played-readme.vercel.app/api?user=abril_monta%C3%B1o_dn&width=600" alt="Spotify Recently Played"/>
      </div>
      
      <div class="code">
# Music preferences for different coding moods
coding_soundtrack = {
    'deep_focus': ['Paganini', 'Classical', 'Post-rock'],
    'debugging': ['Emo', 'Alternative Rock', 'Lo-fi'],
    'late_night': ['Dark Ambient', 'Synthwave', 'Violin pieces'],
    'data_viz': ['Electronic', 'Instrumental', 'Cinematic']
}

def get_playlist(task, hour):
    if hour > 22 or hour < 6:
        return coding_soundtrack['late_night']
    elif 'debug' in task.lower():
        return coding_soundtrack['debugging'] 
    return coding_soundtrack['deep_focus']
</div>
    </section>

    <section class="panel" aria-labelledby="experience">
      <h2 id="experience">Experience</h2>
      <div class="grid cols-2">
        <div class="card">
          <h3>Data Solutions Developer — Parco Ingeniería</h3>
          <p class="soft">Jan 2021 – Dec 2023 · Mexico City</p>
          <ul>
            <li>Designed ETL pipelines handling <strong>10GB+/day</strong>, reducing costs by 40%.</li>
            <li>Optimized SQL/NoSQL databases to increase performance by 30%.</li>
            <li>Collaborated with cross‑functional teams to deliver scalable solutions.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Founder — Automated Invoicing for SMEs</h3>
          <p class="soft">2024 – Present</p>
          <p>Developing an AI‑powered system to streamline billing for local businesses using automated document processing and intelligent data extraction.</p>
        </div>
      </div>
    </section>

    <section class="panel" aria-labelledby="projects">
      <h2 id="projects">Featured Projects</h2>
      <div class="grid cols-3">
        <div class="card">
          <h3>🌍 Climate Tracker</h3>
          <p>IoT sensors + ML models to monitor air quality across CDMX with real-time data processing.</p>
        </div>
        <div class="card">
          <h3>📊 GreenTech Solutions</h3>
          <p>Air pollution forecasting with Prophet & ARIMA models achieving 85% accuracy.</p>
        </div>
        <div class="card">
          <h3>🔎 NLP Ethics Research</h3>
          <p>Analyzing bias in language models and developing mitigation strategies for fair AI.</p>
        </div>
        <div class="card">
          <h3>📈 Divorce Prediction Mexico</h3>
          <p>Predictive modeling of divorce rates using socioeconomic data and demographic trends.</p>
        </div>
        <div class="card">
          <h3>💻 Interactive Dashboards</h3>
          <p>Real-time analytics dashboards with Streamlit, MongoDB and advanced visualizations.</p>
        </div>
        <div class="card">
          <h3>🤖 AutoML Pipeline</h3>
          <p>Automated machine learning pipeline for SMEs with model selection and hyperparameter tuning.</p>
        </div>
      </div>
    </section>

    <section class="baphy-section" aria-labelledby="baphy">
      <h2 id="baphy">Baphy.exe — System Administrator</h2>
      <div style="margin: 20px 0;">
        <img src="https://media2.giphy.com/media/9QkuSuf7vc3Ly/giphy.webp" alt="Digital Cat" width="350" style="border-radius: 12px; filter: drop-shadow(var(--violet-glow));">
      </div>
      
      <p><strong>Meet Baphy</strong> — the feline overlord of this workspace. Official job title: Senior Code Quality Assurance Specialist. Actual job description: professional keyboard warmer and bug detector (literally sits on bugs in the code until I fix them).</p>
      
      <div class="code">
class Baphy:
    def __init__(self):
        self.species = "Felis catus"
        self.color = "void_black"
        self.role = "Chief Debugging Officer"
        self.skills = ["keyboard_testing", "human_supervision", "entropy_generation"]
        self.office_hours = "24/7 (mostly napping)"
    
    def debug_session(self):
        if self.is_hungry():
            return "CRITICAL ERROR: Feed me first"
        elif self.is_sleepy():
            return "WARNING: Will nap on keyboard"
        return "Debugging authorized. Proceed with caution."
    
    def code_review(self, code):
        self.sit_on_keyboard()
        return "Needs more cat hair for optimal performance"
</div>
    </section>

    <section class="panel" aria-labelledby="philosophy">
      <h2 id="philosophy">Philosophy & Interests</h2>
      <div class="philosophy-grid">
        <div class="philosophy-item">
          <span class="emoji-large">🧘</span>
          <h3>Mindfulness</h3>
          <p>Daily meditation for mental clarity and better problem-solving.</p>
        </div>
        <div class="philosophy-item">
          <span class="emoji-large">🎮</span>
          <h3>Gaming</h3>
          <p>Indie games and narrative-driven experiences. Exploring procedural generation.</p>
        </div>
        <div class="philosophy-item">
          <span class="emoji-large">🎻</span>
          <h3>Violin</h3>
          <p>Classical music enthusiast, blending logic with artistic expression.</p>
        </div>
        <div class="philosophy-item">
          <span class="emoji-large">📚</span>
          <h3>Literature</h3>
          <p>Philosophy, mystery novels, and horror stories for creative inspiration.</p>
        </div>
        <div class="philosophy-item">
          <span class="emoji-large">☕</span>
          <h3>Café Culture</h3>
          <p>Local coffee shops as perfect hubs for coding and reflection.</p>
        </div>
        <div class="philosophy-item">
          <span class="emoji-large">🌱</span>
          <h3>Ethics</h3>
          <p>Vegetarian lifestyle and advocate for responsible AI development.</p>
        </div>
      </div>
    </section>

    <section class="panel" aria-labelledby="principles">
      <h2 id="principles">Core Principles</h2>
      <div class="highlight">
        <strong>Code Philosophy:</strong>
        <ol style="margin-top: 10px;">
          <li><strong>Elegance over complexity</strong> — Simple solutions are often the most powerful</li>
          <li><strong>Fail fast, learn faster</strong> — Every bug is a teacher in disguise</li>
          <li><strong>Human-centered design</strong> — Technology should serve people, not the other way around</li>
          <li><strong>Open knowledge</strong> — Share what you learn freely and openly</li>
        </ol>
      </div>
      
      <div class="code">
# Life operating system
def existence():
    while True:
        learn_something_new()
        write_clean_code()
        play_violin()
        feed_baphy()
        if world.needs_improvement():
            contribute_positively()
        sleep(8)  # Important for debugging brain.exe
</div>
    </section>

    <div class="quote-section">
      <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark" alt="Random Quote" loading="lazy" />
    </div>

    <footer>
      <div class="highlight" style="text-align: center; border-left: none; border: 1px solid var(--line);">
        <p style="margin: 0; font-style: italic; color: var(--aqua);">
          "The best code tells a story, and the best stories change how we see the world."
        </p>
        <p style="margin: 10px 0 0 0; color: var(--muted);">
          Thanks for exploring my digital realm. May your code compile on the first try. ✨
        </p>
      </div>
    </footer>
  </div>
</body>
</html>
