<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Laptop Price Predictor — README</title>
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa6b2; --accent:#06b6d4; --glass: rgba(255,255,255,0.03);
      --max-width:1000px;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    html,body{height:100%; margin:0; background:linear-gradient(180deg,#071023 0%, #061224 100%); color:#e6eef6; -webkit-font-smoothing:antialiased;}
    .container{max-width:var(--max-width); margin:36px auto; padding:28px; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border-radius:12px; box-shadow:0 8px 30px rgba(2,6,23,0.7); border:1px solid rgba(255,255,255,0.03);}
    header{display:flex; gap:18px; align-items:center; margin-bottom:18px;}
    .logo{width:64px; height:64px; border-radius:10px; background:linear-gradient(135deg,#0ea5a4,#7c3aed); display:flex; align-items:center; justify-content:center; font-weight:700; font-size:18px; color:white;}
    h1{margin:0; font-size:22px;}
    .badges{display:flex; gap:8px; flex-wrap:wrap; margin-top:6px;}
    .badge{background:var(--glass); padding:6px 10px; border-radius:999px; color:var(--muted); font-size:13px; border:1px solid rgba(255,255,255,0.02);}
    nav{display:flex; gap:12px; margin:18px 0; flex-wrap:wrap;}
    nav a{color:var(--accent); text-decoration:none; font-weight:600; background:rgba(6,182,212,0.06); padding:8px 12px; border-radius:8px;}
    .grid{display:grid; grid-template-columns:1fr 320px; gap:20px;}
    @media (max-width:920px){ .grid{grid-template-columns:1fr;} .sidebar{order:2;} }
    .card{background:rgba(255,255,255,0.02); padding:18px; border-radius:10px; border:1px solid rgba(255,255,255,0.02);}
    .muted{color:var(--muted); font-size:14px;}
    pre{background:#021227; padding:14px; border-radius:8px; overflow:auto; font-size:13px; color:#d8f7ff;}
    table{width:100%; border-collapse:collapse; margin-top:12px;}
    th,td{padding:8px 10px; border-bottom:1px dashed rgba(255,255,255,0.03); text-align:left;}
    .screenshot{width:100%; height:160px; object-fit:cover; border-radius:8px; border:1px solid rgba(255,255,255,0.03);}
    .btn{display:inline-block; padding:10px 14px; border-radius:8px; background:linear-gradient(90deg,var(--accent), #8b5cf6); color:#021027; font-weight:700; text-decoration:none;}
    footer{margin-top:18px; color:var(--muted); font-size:13px; text-align:center;}
    .section-title{display:flex; align-items:center; gap:10px; margin:8px 0 12px; font-size:16px;}
    .small{font-size:13px; color:var(--muted);}
    code.inline{background:#021227;padding:2px 6px;border-radius:6px;color:#9ff0ff;}
  </style>
</head>
<body>
  <div class="container" role="main" aria-labelledby="title">
    <header>
      <div class="logo">LP</div>
      <div>
        <h1 id="title">💻 Laptop Price Predictor</h1>
        <div class="badges">
          <div class="badge">Python • 3.8+</div>
          <div class="badge">ML • Regression</div>
          <div class="badge">Status: Active</div>
          <div class="badge">License: MIT</div>
        </div>
        <div class="muted" style="margin-top:8px;">Predict laptop prices from specs (brand, CPU, RAM, GPU, storage) using a trained ML pipeline.</div>
      </div>
    </header>

    <nav aria-label="Quick links">
      <a href="#project-structure">Structure</a>
      <a href="#installation">Install</a>
      <a href="#usage">Usage</a>
      <a href="#model">Model</a>
      <a href="#results">Results</a>
      <a href="#contribute">Contribute</a>
    </nav>

    <div class="grid" role="region">
      <main>
        <section id="motivation" class="card" aria-labelledby="motivation-title">
          <div class="section-title"><strong id="motivation-title">📌 Motivation</strong></div>
          <p class="muted">Deciding a fair laptop price can be tough. This project provides a fast, explainable, data-driven estimate to help buyers, sellers, and shops price laptops fairly.</p>
        </section>

        <section id="project-structure" class="card" aria-labelledby="structure-title" style="margin-top:16px;">
          <div class="section-title"><strong id="structure-title">📂 Project Structure</strong></div>
          <pre><code>
Laptop_price_predictor/
├── main.py             # Entry script – takes input & returns predicted price
├── requirements.txt    # Python dependencies
├── setup.sh            # Environment setup script
├── df.pkl              # Cleaned dataset (pickled)
├── pipe.pkl            # Trained ML pipeline (preprocessing + model)
├── Procfile            # Deployment config (Heroku/Cloud)
└── README.md           # Project documentation
          </code></pre>
          <p class="small">All important artifacts are included: <code class="inline">df.pkl</code> (processed dataset) and <code class="inline">pipe.pkl</code> (pipeline with model).</p>
        </section>

        <section id="installation" class="card" style="margin-top:16px;" aria-labelledby="install-title">
          <div class="section-title"><strong id="install-title">⚙️ Installation & Setup</strong></div>

          <ol class="muted">
            <li><strong>Clone the repo</strong>
              <pre><code>git clone https://github.com/Riddhima8/Laptop_price_predictor.git
cd Laptop_price_predictor</code></pre>
            </li>
            <li><strong>Create virtual environment</strong>
              <pre><code>python -m venv venv
# Linux/Mac
source venv/bin/activate
# Windows
venv\Scripts\activate</code></pre>
            </li>
            <li><strong>Install dependencies</strong>
              <pre><code>pip install -r requirements.txt</code></pre>
            </li>
            <li class="small muted">Optional: Run <code>bash setup.sh</code> to automate common setup steps.</li>
          </ol>
        </section>

        <section id="usage" class="card" style="margin-top:16px;" aria-labelledby="usage-title">
          <div class="section-title"><strong id="usage-title">▶️ Usage</strong></div>
          <p class="muted">Run the prediction script (example):</p>
          <pre><code>python main.py</code></pre>
          <p class="muted">By default <code>main.py</code> loads <code>pipe.pkl</code>, prompts for specs (or reads a sample input), and prints a predicted price. You can extend <code>main.py</code> to accept CLI args or run as a Flask / Streamlit app for a web UI.</p>

          <div style="margin-top:12px;">
            <strong class="small">Example input fields</strong>
            <table>
              <thead><tr><th>Field</th><th>Type</th><th>Example</th></tr></thead>
              <tbody>
                <tr><td>Company</td><td>categorical</td><td>Dell</td></tr>
                <tr><td>TypeName</td><td>categorical</td><td>Gaming</td></tr>
                <tr><td>RAM (GB)</td><td>numeric</td><td>16</td></tr>
                <tr><td>CPU</td><td>categorical</td><td>Intel Core i7</td></tr>
                <tr><td>GPU</td><td>categorical</td><td>Nvidia GTX 1650</td></tr>
                <tr><td>SSD (GB)</td><td>numeric</td><td>512</td></tr>
              </tbody>
            </table>
          </div>
        </section>

        <section id="model" class="card" style="margin-top:16px;" aria-labelledby="model-title">
          <div class="section-title"><strong id="model-title">🧠 Model & Pipeline</strong></div>
          <p class="muted">Pipeline includes: cleaning → encoding of categorical features → scaling of numeric features → regression model.</p>
          <p class="small">Common model choices: RandomForestRegressor, XGBoost, or Linear Regression. The final pipeline is serialized as <code class="inline">pipe.pkl</code>.</p>
        </section>

        <section id="results" class="card" style="margin-top:16px;" aria-labelledby="results-title">
          <div class="section-title"><strong id="results-title">📈 Results</strong></div>

          <div style="display:flex; gap:12px; align-items:center; flex-wrap:wrap;">
            <img class="screenshot" src="https://raw.githubusercontent.com/plotly/datasets/master/graph/iris-data.png" alt="Placeholder performance chart" />
            <div style="flex:1;">
              <p class="muted"><strong>Example metrics (replace with yours):</strong></p>
              <ul class="muted">
                <li>R² Score: <strong>0.87</strong></li>
                <li>MAE: <strong>4,200 ₹</strong></li>
                <li>RMSE: <strong>6,100 ₹</strong></li>
              </ul>
              <p class="small">Tip: Replace the placeholder image with your real <code>predicted_vs_actual</code> plot saved as PNG and reference it here.</p>
            </div>
          </div>
        </section>

        <section id="future" class="card" style="margin-top:16px;" aria-labelledby="future-title">
          <div class="section-title"><strong id="future-title">🔮 Future Improvements</strong></div>
          <ul class="muted">
            <li>Collect larger & more recent dataset (new laptop models).</li>
            <li>Include more features: battery life, display quality, weight.</li>
            <li>Evaluate ensemble or deep-learning methods.</li>
            <li>Build a web UI (Flask / Streamlit) and deploy (Heroku / Vercel).</li>
          </ul>
        </section>

        <section id="contribute" class="card" style="margin-top:16px;" aria-labelledby="contribute-title">
          <div class="section-title"><strong id="contribute-title">🤝 Contributing</strong></div>
          <p class="muted">Contributions welcome — please follow these steps:</p>
          <ol class="muted">
            <li>Fork the repo</li>
            <li>Create a branch: <code>git checkout -b feature/your-feature</code></li>
            <li>Commit & push changes</li>
            <li>Open a PR</li>
          </ol>
        </section>

        <section id="license" class="card" style="margin-top:16px;" aria-labelledby="license-title">
          <div class="section-title"><strong id="license-title">📜 License</strong></div>
          <p class="muted">This project is licensed under the <strong>MIT License</strong>. Include a <code>LICENSE</code> file in the repo.</p>
        </section>
      </main>

      <aside class="sidebar">
        <div class="card" aria-labelledby="quick-title">
          <div class="section-title"><strong id="quick-title">Quick actions</strong></div>
          <p class="small">Open the GitHub repo or download important artifacts.</p>
          <p style="margin-top:12px;">
            <a class="btn" href="https://github.com/Riddhima8/Laptop_price_predictor" target="_blank" rel="noopener">Open Repo on GitHub</a>
          </p>

          <div style="margin-top:14px;">
            <strong class="small">Important files</strong>
            <ul class="small" style="padding-left:12px; margin-top:8px;">
              <li><code>main.py</code> — predictor script</li>
              <li><code>pipe.pkl</code> — serialized ML pipeline</li>
              <li><code>df.pkl</code> — processed dataset</li>
              <li><code>requirements.txt</code> — dependencies</li>
            </ul>
          </div>

          <div style="margin-top:14px;">
            <strong class="small">Badges</strong>
            <div style="display:flex; gap:8px; margin-top:8px;">
              <img src="https://img.shields.io/badge/Python-3.8%2B-blue?logo=python" alt="python badge" style="height:26px;">
              <img src="https://img.shields.io/badge/ML-Regression-green" alt="ml badge" style="height:26px;">
              <img src="https://img.shields.io/badge/License-MIT-yellow" alt="license badge" style="height:26px;">
            </div>
          </div>

          <div style="margin-top:14px;">
            <strong class="small">Contact</strong>
            <p class="small muted">Open an issue or PR on GitHub for help or collaboration.</p>
          </div>
        </div>

        <div class="card" style="margin-top:14px;">
          <div class="section-title"><strong>Screenshots / Images</strong></div>
          <p class="small muted">Replace placeholders with your charts & UI screenshots:</p>
          <img class="screenshot" src="https://raw.githubusercontent.com/streamlit/streamlit/develop/docs/static/brand/hero.png" alt="app placeholder" style="margin-top:10px;">
        </div>
      </aside>
    </div>

    <footer>
      <p>Made with ❤️ • If this helped you, give the repo a ⭐ on GitHub: <a href="https://github.com/Riddhima8/Laptop_price_predictor" style="color:var(--accent); text-decoration:none;">Riddhima8/Laptop_price_predictor</a></p>
    </footer>
  </div>
</body>
</html>
