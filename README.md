# teenhub 
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Your Name — Portfolio</title>
  <meta name="description" content="Modern minimal portfolio." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724; /* dark slate */
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#7dd3fc;
      --glass: rgba(255,255,255,0.04);
      --radius:14px;
      --max:1100px;
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
      background:linear-gradient(180deg,var(--bg),#071025 60%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:32px 20px;
      display:flex;
      justify-content:center;
    }
    .wrap{width:100%;max-width:var(--max)}

    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:52px;height:52px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#60a5fa);display:flex;align-items:center;justify-content:center;font-weight:700;color:#06202a}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600}

    .hero{display:grid;grid-template-columns:1fr 300px;gap:32px;align-items:center;margin-bottom:36px}
    .hero-left h1{font-size:clamp(28px,4vw,40px);margin:0 0 12px}
    .hero-left p{color:var(--muted);margin:0 0 18px;line-height:1.6}
    .cta{display:inline-block;padding:10px 16px;border-radius:10px;background:linear-gradient(90deg,rgba(125,211,252,0.12),rgba(96,165,250,0.08));border:1px solid rgba(125,211,252,0.12);color:var(--accent);text-decoration:none;font-weight:600}

    .profile{background:var(--card);padding:22px;border-radius:16px;box-shadow:0 6px 18px rgba(0,0,0,0.6);display:flex;flex-direction:column;gap:14px}
    .avatar{width:100%;height:300px;border-radius:12px;background:linear-gradient(180deg,#05202b,#07323e);display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:600}
    .meta{display:flex;justify-content:space-between;gap:12px}
    .meta div{color:var(--muted);font-size:14px}

    section{margin-bottom:28px}
    h2{margin:0 0 14px;font-size:18px}

    .projects{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
    .card{background:var(--glass);padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);min-height:120px;display:flex;flex-direction:column;justify-content:space-between}
    .card h3{margin:0;font-size:16px}
    .card p{color:var(--muted);margin:8px 0 0}
    .card button{align-self:flex-start;margin-top:10px;padding:8px 12px;border-radius:10px;border:0;background:transparent;color:var(--accent);cursor:pointer;font-weight:600}

    footer{color:var(--muted);font-size:13px;text-align:center;margin-top:36px}

    /* responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr;}
      .projects{grid-template-columns:repeat(2,1fr)}
      .avatar{height:220px}
    }
    @media (max-width:560px){
      nav a{display:none}
      .projects{grid-template-columns:1fr}
      body{padding:18px}
    }

    /* modal */
    .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(2,6,23,0.6);padding:28px}
    .modal .panel{background:linear-gradient(180deg,#071029,#081726);padding:20px;border-radius:12px;max-width:720px;width:100%;}
    .modal.show{display:flex}
    .close{background:transparent;border:0;color:var(--muted);font-weight:700;cursor:pointer}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo">YN</div>
        <div>
          <div style="font-weight:700">Your Name</div>
          <div style="font-size:13px;color:var(--muted)">Designer · Developer · Creator</div>
        </div>
      </div>
      <nav aria-label="Primary">
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-left">
          <h1>Minimal portfolio for a modern creator</h1>
          <p>Showcase selected work, a short bio, and contact details. Replace text and images here with your own content. Project cards open for more details.</p>
          <a class="cta" href="#projects">View projects</a>
        </div>
        <aside class="profile" aria-label="Profile card">
          <div class="avatar">Place your photo here</div>
          <div style="font-weight:600">Your Name</div>
          <div class="meta">
            <div>Location<br><strong style="color:#fff">City, Country</strong></div>
            <div>Role<br><strong style="color:#fff">Product Designer</strong></div>
          </div>
        </aside>
      </section>

      <section id="about">
        <h2>About</h2>
        <p style="color:var(--muted);margin-top:6px;max-width:70ch">A concise paragraph about you. Mention your primary skills, what you love building, and the type of projects you take on. Keep this short and scannable.</p>
      </section>

      <section id="projects">
        <h2>Projects</h2>
        <div class="projects">
          <article class="card">
            <div>
              <h3>Project Alpha</h3>
              <p>Short subtitle or tech stack — e.g., React • API • Design System</p>
            </div>
            <div>
              <button data-title="Project Alpha" data-desc="Detailed description for Project Alpha. Replace this with your real project summary and links." class="open">Details</button>
            </div>
          </article>

          <article class="card">
            <div>
              <h3>Project Beta</h3>
              <p>Short subtitle — e.g., UI/UX • Web App</p>
            </div>
            <div>
              <button data-title="Project Beta" data-desc="Detailed description for Project Beta. Replace with outcomes, role, and links." class="open">Details</button>
            </div>
          </article>

          <article class="card">
            <div>
              <h3>Project Gamma</h3>
              <p>Short subtitle — e.g., Personal Website</p>
            </div>
            <div>
              <button data-title="Project Gamma" data-desc="Detailed description for Project Gamma. Swap in screenshots and links as needed." class="open">Details</button>
            </div>
          </article>
        </div>
      </section>

      <section id="contact">
        <h2>Contact</h2>
        <p style="color:var(--muted);margin-top:6px">Interested in working together? Email me at <a href="mailto:you@example.com" style="color:var(--accent);text-decoration:none">you@example.com</a> or use the social links below.</p>
        <div style="margin-top:12px;display:flex;gap:12px">
          <a href="#" style="color:var(--muted);text-decoration:none">Twitter</a>
          <a href="#" style="color:var(--muted);text-decoration:none">LinkedIn</a>
          <a href="#" style="color:var(--muted);text-decoration:none">GitHub</a>
        </div>
      </section>

      <footer>
        © <span id="year"></span> Your Name — Built with a minimal template.
      </footer>
    </main>
  </div>

  <div class="modal" id="modal" role="dialog" aria-modal="true" aria-hidden="true">
    <div class="panel" role="document">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <strong id="m-title">Title</strong>
        <button class="close" id="m-close" aria-label="Close">✕</button>
      </div>
      <div id="m-body" style="margin-top:12px;color:var(--muted)">Details</div>
    </div>
  </div>

  <script>
    // small interactive pieces
    document.getElementById('year').textContent = new Date().getFullYear();
    const modal = document.getElementById('modal');
    const mTitle = document.getElementById('m-title');
    const mBody = document.getElementById('m-body');
    document.querySelectorAll('.open').forEach(btn=>{
      btn.addEventListener('click',()=>{
        mTitle.textContent = btn.dataset.title;
        mBody.textContent = btn.dataset.desc;
        modal.classList.add('show');
        modal.setAttribute('aria-hidden','false');
      })
    });
    document.getElementById('m-close').addEventListener('click',()=>{
      modal.classList.remove('show');
      modal.setAttribute('aria-hidden','true');
    })
    modal.addEventListener('click',(e)=>{ if(e.target===modal){ modal.classList.remove('show'); modal.setAttribute('aria-hidden','true'); } })
  </script>
</body>
</html>
