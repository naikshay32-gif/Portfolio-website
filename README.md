# Portfolio-website
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Shayan — Web Developer Portfolio</title>
  <meta name="description" content="Portfolio website showing projects, skills and contact info. Created for Coursera Microsoft Web Dev project." />
  <style>
    :root{
      --bg:#0f1113; --card:#151618; --muted:#9aa0a6; --accent:#6fb3ff; --glass:rgba(255,255,255,0.03);
      --radius:14px; --max-width:1100px;
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; background:linear-gradient(180deg,#070809 0%, #0f1113 100%); color:#e6eef6; -webkit-font-smoothing:antialiased;
      display:flex; align-items:center; justify-content:center; padding:28px;
    }
    .wrap{width:100%; max-width:var(--max-width);} 
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;background:linear-gradient(135deg,var(--accent),#7bd389);border-radius:12px;display:grid;place-items:center;font-weight:700}
    .brand h1{font-size:18px;margin:0}
    nav{display:flex;gap:12px}
    .nav-link{background:var(--glass);padding:10px 14px;border-radius:10px;text-decoration:none;color:var(--muted);font-weight:600}
    .cta{background:var(--accent);color:#071022;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:700}
    /* hero */
    .hero{background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);padding:24px;border-radius:var(--radius);display:flex;gap:20px;align-items:center}
    .info{flex:1}
    .title{font-size:22px;margin:0 0 8px}
    .subtitle{margin:0 0 14px;color:var(--muted)}
    .skills{display:flex;flex-wrap:wrap;gap:8px}
    .chip{background:#0b1320;padding:8px 10px;border-radius:999px;color:var(--muted);font-weight:600}
    .preview{width:320px;max-width:40%;min-width:220px}
    .preview img{width:100%;border-radius:10px;display:block}
    /* projects */
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:20px}
    .card{background:var(--card);padding:14px;border-radius:12px;box-shadow:0 6px 18px rgba(0,0,0,0.6)}
    .card h3{margin:0 0 8px}
    .meta{color:var(--muted);font-size:13px;margin-bottom:12px}
    .btn{display:inline-block;padding:8px 12px;border-radius:8px;background:var(--accent);color:#071022;text-decoration:none;font-weight:700}
    /* contact */
    footer{margin-top:24px}
    form{display:grid;gap:10px}
    input,textarea{background:#0b0d0e;border:1px solid rgba(255,255,255,0.03);padding:10px;border-radius:8px;color:var(--muted)}
    .row{display:flex;gap:10px}
    /* responsive */
    @media (max-width:900px){
      .grid{grid-template-columns:repeat(2,1fr)}
      .preview{display:none}
    }
    @media (max-width:600px){
      header{flex-direction:column;align-items:flex-start;gap:12px}
      .grid{grid-template-columns:1fr}
      .row{flex-direction:column}
      body{padding:16px}
    }
    /* accessible focus */
    a:focus, button:focus, input:focus, textarea:focus{outline:3px solid rgba(111,179,255,0.22);outline-offset:2px}
    /* small helper */
    .muted{color:var(--muted);font-size:14px}
  </style>
</head>
<body>
  <main class="wrap" id="main">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">S</div>
        <div>
          <h1>Shayan — Web Developer</h1>
          <div class="muted">BCA AIML · Front-end & Web Projects</div>
        </div>
      </div>
      <nav aria-label="Main navigation">
        <a class="nav-link" href="#projects">Projects</a>
        <a class="nav-link" href="#about">About</a>
        <a class="cta" href="#contact">Contact</a>
      </nav>
    </header>

    <section class="hero" aria-labelledby="intro">
      <div class="info">
        <h2 id="intro" class="title">Hi — I'm Shayan. I build accessible, responsive websites.</h2>
        <p class="subtitle">This portfolio demonstrates semantic HTML, accessibility features, responsive CSS and JavaScript interactivity — built for my Coursera project submission.</p>
        <div class="skills" aria-hidden="false">
          <span class="chip">HTML5</span>
          <span class="chip">CSS3</span>
          <span class="chip">JavaScript</span>
          <span class="chip">Git & GitHub</span>
          <span class="chip">Responsive Design</span>
        </div>
      </div>
      <aside class="preview" aria-hidden="true">
        <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='800' height='560'><rect width='100%' height='100%' fill='%2314191c'/><text x='50%' y='50%' fill='%23ffffff' font-size='24' font-family='Arial' text-anchor='middle'>Project preview</text></svg>" alt="Screenshot preview of project" />
      </aside>
    </section>

    <section id="projects" aria-labelledby="projects-heading">
      <h2 id="projects-heading" style="margin-top:22px">Selected Projects</h2>
      <p class="muted">Click View to open a live demo or the code repository.</p>

      <div style="margin-top:12px">
        <label for="filter" class="muted">Filter:</label>
        <select id="filter" aria-label="Filter projects by type">
          <option value="all">All</option>
          <option value="frontend">Frontend</option>
          <option value="responsive">Responsive</option>
          <option value="js">JavaScript</option>
        </select>
      </div>

      <div class="grid" id="projectGrid">
        <article class="card" data-type="frontend">
          <h3>Personal Portfolio</h3>
          <div class="meta">HTML · CSS · GitHub Pages</div>
          <p class="muted">Semantic, accessible portfolio with contact form. Includes README and hosted on GitHub Pages.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/portfolio">View</a></p>
        </article>

        <article class="card" data-type="responsive">
          <h3>Responsive Grid Layout</h3>
          <div class="meta">CSS Grid · Media Queries</div>
          <p class="muted">A demo showing multi-column responsive layouts that adapt to screen sizes.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/grid">View</a></p>
        </article>

        <article class="card" data-type="js">
          <h3>Interactive To‑Do</h3>
          <div class="meta">JavaScript · LocalStorage</div>
          <p class="muted">A small JS app to add, edit, complete and persist tasks in browser storage.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/todo">View</a></p>
        </article>

        <article class="card" data-type="frontend">
          <h3>Landing Page Clone</h3>
          <div class="meta">HTML · CSS</div>
          <p class="muted">Clean hero section, responsive nav and accessible markup.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/landing">View</a></p>
        </article>

        <article class="card" data-type="responsive">
          <h3>Mobile-first Layout</h3>
          <div class="meta">Mobile-first design · CSS</div>
          <p class="muted">Designed starting from smallest screens and scaled upward using breakpoints.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/mobile">View</a></p>
        </article>

        <article class="card" data-type="js">
          <h3>Form Validator</h3>
          <div class="meta">JS · Accessibility</div>
          <p class="muted">Accessible form validation with clear error messages and ARIA attributes.</p>
          <p style="margin-top:12px"><a class="btn" href="#" data-demo="https://example.github.io/form">View</a></p>
        </article>
      </div>
    </section>

    <section id="about" style="margin-top:20px">
      <h2>About</h2>
      <p class="muted">I'm a BCA AIML student building front-end projects. This site demonstrates the required course criteria: structured HTML, accessibility (alt text, ARIA), CSS styling, JavaScript interactivity and responsiveness.</p>
    </section>

    <section id="contact" style="margin-top:18px">
      <h2>Contact</h2>
      <form id="contactForm" aria-describedby="formHelp">
        <div id="formHelp" class="muted">Send me a message — required fields marked with *</div>
        <div class="row">
          <input id="name" name="name" type="text" placeholder="Your name *" required aria-required="true" />
          <input id="email" name="email" type="email" placeholder="Email *" required aria-required="true" />
        </div>
        <textarea id="message" name="message" rows="5" placeholder="Message *" required aria-required="true"></textarea>
        <div style="display:flex;gap:8px;align-items:center">
          <button type="submit" class="btn">Send Message</button>
          <div id="formStatus" class="muted" role="status" aria-live="polite"></div>
        </div>
      </form>
    </section>

    <footer>
      <p class="muted">© <span id="year"></span> Shayan — Built with HTML, CSS & JavaScript. Hosted on GitHub Pages.</p>
    </footer>
  </main>

  <script>
    // Accessibility: show current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Project filter
    const filter = document.getElementById('filter');
    const grid = document.getElementById('projectGrid');
    filter.addEventListener('change', ()=>{
      const val = filter.value;
      Array.from(grid.children).forEach(card=>{
        if(val==='all' || card.dataset.type===val) card.style.display='block'; else card.style.display='none';
      });
    });

    // Demo buttons open links in new tab; alt behavior if placeholder
    document.querySelectorAll('a[data-demo]').forEach(a=>{
      a.addEventListener('click', e=>{
        e.preventDefault();
        const url = a.dataset.demo;
        // if still placeholder, show quick modal-like message
        if(url.includes('example.github.io')){
          alert('To complete your Coursera submission: host this project on GitHub Pages and paste the URL in the assignment form.');
          return;
        }
        window.open(url, '_blank', 'noopener');
      });
    });

    // Simple contact validation & UX
    const form = document.getElementById('contactForm');
    const status = document.getElementById('formStatus');
    form.addEventListener('submit', (e)=>{
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      if(!name || !email || !message){
        status.textContent = 'Please complete all required fields.';
        return;
      }
      // Basic email pattern
      const pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if(!pattern.test(email)){
        status.textContent = 'Please enter a valid email address.';
        return;
      }
      // Simulate sending
      status.textContent = 'Sending...';
      setTimeout(()=>{
        status.textContent = 'Message sent — thank you! (demo only)';
        form.reset();
      },700);
    });

    // Keyboard accessibility: skip to main on pressing 'm' (example)
    window.addEventListener('keydown', e=>{
      if(e.key.toLowerCase()==='m') document.getElementById('main').focus();
    });
  </script>
</body>
</html>
