<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Kinshu Keshri · AI/ML Engineer</title>
<meta name="description" content="AI/ML engineering student building production-grade GenAI, RAG and autonomous agent systems.">
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🧠</text></svg>">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700;12..96,800&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#F5F6FB; --surface:#FFFFFF; --ink:#13152E; --muted:#5B5F7A; --line:#DFE1EE;
  --accent:#3B4BFF; --accent-soft:#E6E9FF; --ok:#0E9F6E;
  --display:"Bricolage Grotesque",system-ui,sans-serif; --body:"Instrument Sans",system-ui,sans-serif;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){--bg:#0F1226;--surface:#171B38;--ink:#EEF0FF;--muted:#A0A5C8;--line:#2A2F57;--accent:#7C89FF;--accent-soft:#23295A;--ok:#34D399}
}
:root[data-theme="dark"]{--bg:#0F1226;--surface:#171B38;--ink:#EEF0FF;--muted:#A0A5C8;--line:#2A2F57;--accent:#7C89FF;--accent-soft:#23295A;--ok:#34D399}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth;scroll-padding-top:80px}
body{background:var(--bg);color:var(--ink);font:400 17px/1.65 var(--body);-webkit-font-smoothing:antialiased}
a{color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:3px;border-radius:6px}
.wrap{max-width:1080px;margin:0 auto;padding:0 24px}
h1,h2,h3{font-family:var(--display);line-height:1.08;letter-spacing:-.02em}
h2{font-size:clamp(30px,4.5vw,46px);font-weight:800;margin-bottom:12px}
section{padding:88px 0}
.lead{color:var(--muted);max-width:60ch;margin-bottom:40px}

/* nav */
nav{position:sticky;top:0;z-index:20;background:color-mix(in srgb,var(--bg) 85%,transparent);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
nav .wrap{display:flex;align-items:center;justify-content:space-between;height:64px}
.logo{font:800 20px var(--display);text-decoration:none}
.links{display:flex;gap:26px;align-items:center;font-size:15px;font-weight:500}
.links a{text-decoration:none;color:var(--muted)}
.links a:hover{color:var(--ink)}
#theme{background:none;border:1px solid var(--line);color:var(--ink);width:38px;height:38px;border-radius:50%;cursor:pointer;font-size:16px}
@media(max-width:720px){.links a:not(.keep){display:none}}

/* hero */
.hero{padding:88px 0 56px}
.status{display:inline-flex;gap:10px;align-items:center;font-size:14px;font-weight:500;background:var(--surface);border:1px solid var(--line);padding:6px 14px;border-radius:99px;margin-bottom:28px}
.dot{width:8px;height:8px;border-radius:50%;background:var(--ok);box-shadow:0 0 0 0 var(--ok);animation:pulse 2s infinite}
@keyframes pulse{70%{box-shadow:0 0 0 8px transparent}100%{box-shadow:0 0 0 0 transparent}}
.hero h1{font-size:clamp(44px,9vw,104px);font-weight:800;max-width:12ch}
.hero p.sub{font-size:clamp(18px,2.2vw,22px);color:var(--muted);max-width:56ch;margin:26px 0 34px}
.btns{display:flex;flex-wrap:wrap;gap:12px}
.btn{display:inline-block;padding:13px 24px;border-radius:12px;font-weight:600;text-decoration:none;border:1px solid var(--line);background:var(--surface);transition:transform .15s}
.btn:hover{transform:translateY(-2px)}
.btn.pri{background:var(--accent);border-color:var(--accent);color:#fff}
:root[data-theme="dark"] .btn.pri{color:#0F1226}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]) .btn.pri{color:#0F1226}}

/* pipeline — the one memorable thing */
.pipe{margin-top:64px;background:var(--surface);border:1px solid var(--line);border-radius:20px;padding:28px}
.pipe-head{display:flex;justify-content:space-between;flex-wrap:wrap;gap:8px;font-size:14px;color:var(--muted);margin-bottom:22px}
.pipe-head b{color:var(--ink);font-weight:600}
.steps{display:grid;grid-template-columns:repeat(6,1fr);gap:10px}
.step{position:relative;padding:14px 12px;border:1px solid var(--line);border-radius:12px;font-size:14px;font-weight:600;background:var(--bg);transition:.35s}
.step small{display:block;font-weight:400;color:var(--muted);font-size:12.5px;margin-top:2px}
.step.on{background:var(--accent-soft);border-color:var(--accent)}
.bar{height:8px;border-radius:99px;background:var(--line);margin-top:22px;overflow:hidden}
.bar i{display:block;height:100%;width:100%;background:var(--accent);border-radius:99px;transition:width .9s cubic-bezier(.3,.8,.2,1)}
.count{display:flex;justify-content:space-between;margin-top:10px;font:700 15px var(--display)}
@media(max-width:760px){.steps{grid-template-columns:repeat(2,1fr)}}

/* stats */
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px;margin-top:28px}
.stat{padding:4px 0 4px 16px;border-left:3px solid var(--accent)}
.stat b{display:block;font:800 34px var(--display)}
.stat span{color:var(--muted);font-size:15px}

/* projects */
.filters{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:28px}
.chip{border:1px solid var(--line);background:var(--surface);color:var(--ink);padding:7px 16px;border-radius:99px;font:500 14px var(--body);cursor:pointer}
.chip[aria-pressed="true"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.proj{background:var(--surface);border:1px solid var(--line);border-radius:20px;padding:32px;margin-bottom:20px}
.proj[hidden]{display:none}
.proj-top{display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap;align-items:baseline}
.proj h3{font-size:clamp(22px,3vw,30px);font-weight:700}
.when{color:var(--muted);font-size:14px}
.proj .tag{color:var(--accent);font-weight:600;font-size:15px;margin:6px 0 14px}
.proj ul{padding-left:20px;color:var(--muted);display:grid;gap:9px;margin:16px 0 22px}
.proj li::marker{color:var(--accent)}
.tech{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:20px}
.tech span{font-size:13px;background:var(--accent-soft);padding:3px 11px;border-radius:8px;font-weight:500}
.proj a.gh{font-weight:600;text-decoration:none;border-bottom:2px solid var(--accent)}

/* wins */
.wins{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px}
.win{background:var(--accent);color:#fff;border-radius:20px;padding:30px}
:root[data-theme="dark"] .win{color:#0F1226}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]) .win{color:#0F1226}}
.win .big{font:800 54px/1 var(--display)}
.win h3{font-size:22px;margin:10px 0}
.win p{opacity:.92;font-size:16px}

/* skills */
.skills{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px}
.skill{border-top:2px solid var(--ink);padding-top:14px}
.skill h3{font-size:19px;margin-bottom:10px}
.skill p{color:var(--muted);font-size:15.5px}

/* timeline */
.tl{border-left:2px solid var(--line);margin-left:6px;display:grid;gap:34px}
.tl article{position:relative;padding-left:28px}
.tl article::before{content:"";position:absolute;left:-7px;top:9px;width:12px;height:12px;border-radius:50%;background:var(--accent);box-shadow:0 0 0 4px var(--bg)}
.tl h3{font-size:22px;font-weight:700}
.tl .when{margin-bottom:6px}
.tl p{color:var(--muted);max-width:68ch}

/* contact */
.contact{text-align:left}
.contact h2{font-size:clamp(36px,7vw,80px);max-width:14ch}
.mail{display:inline-block;font:700 clamp(20px,3.4vw,34px) var(--display);margin:10px 0 28px;border-bottom:3px solid var(--accent);text-decoration:none;word-break:break-all}
footer{border-top:1px solid var(--line);padding:28px 0;color:var(--muted);font-size:14px}

@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
</style>
</head>
<body>

<nav><div class="wrap">
  <a class="logo" href="#top">kinshu.</a>
  <div class="links">
    <a href="#work">Projects</a><a href="#wins">Wins</a><a href="#skills">Skills</a><a href="#path">Experience</a>
    <a class="keep" href="#contact">Contact</a>
    <button id="theme" aria-label="Toggle light and dark theme">◐</button>
  </div>
</div></nav>

<header class="hero" id="top"><div class="wrap">
  <div class="status"><span class="dot"></span>B.Tech CSE (AI &amp; Data Science) · IIIT Raichur · 2028</div>
  <h1>Kinshu Keshri</h1>
  <p class="sub">I build GenAI and machine learning systems that run in production: RAG platforms with page-level citations, and autonomous agents that work without anyone watching.</p>
  <div class="btns">
    <a class="btn pri" href="#work">See my projects</a>
    <a class="btn" href="https://github.com/KINSHU07" target="_blank" rel="noopener">GitHub</a>
    <a class="btn" href="https://linkedin.com/in/kinshu-keshri" target="_blank" rel="noopener">LinkedIn</a>
  </div>

  <div class="pipe" aria-label="Animated diagram of my lead generation agent pipeline">
    <div class="pipe-head"><span><b>Autonomous Lead Generation Agent</b>, running every 6 hours</span><span>Press a step to replay</span></div>
    <div class="steps" id="steps"></div>
    <div class="bar"><i id="fill"></i></div>
    <div class="count"><span id="n">1,400+ raw records</span><span id="m" style="color:var(--accent)"></span></div>
  </div>

  <div class="stats">
    <div class="stat"><b>2</b><span>First-place hackathon wins</span></div>
    <div class="stat"><b>471</b><span>Qualified leads delivered to a real client</span></div>
    <div class="stat"><b>5+ days</b><span>Agent ran with zero manual intervention</span></div>
    <div class="stat"><b>15</b><span>pytest tests on the RAG data layer</span></div>
  </div>
</div></header>

<section id="work"><div class="wrap">
  <h2>Projects</h2>
  <p class="lead">Two systems built end to end: ingestion, retrieval or scoring, deployment, and tests.</p>
  <div class="filters" role="group" aria-label="Filter projects">
    <button class="chip" aria-pressed="true" data-f="all">All</button>
    <button class="chip" aria-pressed="false" data-f="rag">RAG</button>
    <button class="chip" aria-pressed="false" data-f="agent">Agents</button>
    <button class="chip" aria-pressed="false" data-f="cloud">Cloud</button>
  </div>

  <article class="proj" data-t="agent cloud">
    <div class="proj-top"><h3>Autonomous Lead Generation Agent</h3><span class="when">May – Jun 2026</span></div>
    <div class="tag">Built for Julio Hoyos &amp; Company, a 30-year NJ accounting firm</div>
    <div class="tech"><span>Python</span><span>Playwright</span><span>BeautifulSoup</span><span>Streamlit</span><span>Google Places API</span><span>Foursquare</span><span>n8n</span><span>GCP Cloud Run</span><span>Azure App Service</span></div>
    <ul>
      <li>A 6-step pipeline (scrape, deduplicate, rule-score, ICP-qualify, enrich, personalize) on a 6-hour self-scheduled runner with cron logging. It ran 5+ days with no manual input.</li>
      <li>Two-layer qualification: a 0–100 rule scorer over 6 weighted signals, then a strict ICP qualifier (7/10 or higher). It surfaced 101 high-priority leads from 1,400+ raw records.</li>
      <li>Multi-source ingestion from a 50-query Playwright Google Maps scraper, Yellow Pages and the NJ business registry, with Google Places and Foursquare fallbacks for about $16 total.</li>
      <li>11 industry-specific outreach emails and a Streamlit dashboard with live filters, charts and 3-click send. Checkpoints save every 10 rows.</li>
    </ul>
    <a class="gh" href="https://github.com/KINSHU07" target="_blank" rel="noopener">View on GitHub</a>
  </article>

  <article class="proj" data-t="rag cloud">
    <div class="proj-top"><h3>AI Due Diligence Copilot</h3><span class="when">Aug 2026</span></div>
    <div class="tag">Evidence-based company research with RAG. Every claim cites a page.</div>
    <div class="tech"><span>Python</span><span>Streamlit</span><span>PostgreSQL</span><span>pgvector</span><span>SQLAlchemy</span><span>Alembic</span><span>Hugging Face API</span><span>PyMuPDF</span><span>GCP</span><span>Azure</span></div>
    <ul>
      <li>Q&amp;A, risk analysis, growth opportunities, financial snapshots and a due-diligence scorecard, all with mandatory page-level citations and no fabricated claims.</li>
      <li>Chunk text and its 768-dim embedding live in one transactional row in pgvector, which avoids the index drift of file-based stores like FAISS. Page-bounded chunks (1,500 chars, 200 overlap) keep citations exact.</li>
      <li>Zero paid APIs: Hugging Face Inference with exponential-backoff retry and a multi-model fallback chain to ride out free-tier limits and cold starts.</li>
      <li>Alembic migrations, connection pooling with pre-ping, and 15 pytest tests covering rollback on failed ingestion, cascade deletes and retrieval, run against live PostgreSQL.</li>
    </ul>
    <a class="gh" href="https://github.com/KINSHU07" target="_blank" rel="noopener">View on GitHub</a>
  </article>
</div></section>

<section id="wins"><div class="wrap">
  <h2>Hackathon wins</h2>
  <p class="lead">Two first places, both with working products rather than slideware.</p>
  <div class="wins">
    <div class="win"><div class="big">1st / 80</div><h3>IIT Dharwad Hackathon</h3><p>An AI Student Guidance System giving personalized academic and career-path recommendations from a student's profile. Judged best overall for innovation, technical depth and impact.</p></div>
    <div class="win"><div class="big">1st / 50</div><h3>AI AIXPO, IIIT Raichur</h3><p>Deep Agro, a full-stack assistant for farmers: crop recommendation (ML), plant disease detection (CNN with transfer learning) and a LangChain advisory agent.</p></div>
  </div>
</div></section>

<section id="skills"><div class="wrap">
  <h2>Skills</h2>
  <p class="lead">Python first, with enough systems work to ship what I train.</p>
  <div class="skills">
    <div class="skill"><h3>Languages</h3><p>Python, C++, C, SQL</p></div>
    <div class="skill"><h3>AI &amp; ML</h3><p>PyTorch, TensorFlow, Scikit-learn, CNN / RNN / LSTM, NLP, Computer Vision, Transfer Learning, Fine-Tuning, LLM Evals</p></div>
    <div class="skill"><h3>GenAI &amp; RAG</h3><p>LangChain, LangGraph, Haystack, RAG, Transformers, Vector Embeddings, Prompt Engineering</p></div>
    <div class="skill"><h3>MLOps &amp; Cloud</h3><p>GCP Cloud Run, Azure App Service, Docker, CI/CD, pgvector, FAISS, PostgreSQL, Alembic, SQLAlchemy</p></div>
    <div class="skill"><h3>Automation</h3><p>Autonomous agents, pipeline orchestration, Playwright, BeautifulSoup, n8n, webhooks</p></div>
    <div class="skill"><h3>APIs &amp; Tools</h3><p>FastAPI, Streamlit, Hugging Face, OpenAI, Google Places, Foursquare, Pandas, NumPy, spaCy, MongoDB Atlas, Git</p></div>
  </div>
</div></section>

<section id="path"><div class="wrap">
  <h2>Experience and leadership</h2>
  <p class="lead">In order, newest first.</p>
  <div class="tl">
    <article><h3>Lead Generation Consultant, Julio Hoyos &amp; Company</h3><div class="when">May – Jun 2026 · Dover, NJ</div><p>Designed and deployed the lead generation agent. Delivered 471 qualified leads (101 high-priority), personalized emails and a live dashboard. Ranked first among 6 competitors in the internship challenge.</p></article>
    <article><h3>Core Member, Entrepreneurship Cell, IIIT Raichur</h3><div class="when">Nov 2025 – Present</div><p>Secured corporate sponsorships through targeted proposals and co-organized startup talks and innovation workshops with founders and industry speakers.</p></article>
    <article><h3>ML Convenor, DeepLabs (AI &amp; ML Club), IIIT Raichur</h3><div class="when">Oct 2025 – Present</div><p>Lead a 10+ member club. Designed a GenAI curriculum covering LangChain, RAG and prompt engineering, and mentored 5+ students to independent deployments and hackathon wins.</p></article>
  </div>
</div></section>

<section id="contact"><div class="wrap contact">
  <h2>Let's build something.</h2>
  <p class="lead">Open to internships, research collaborations and AI projects.</p>
  <a class="mail" href="mailto:kinshukeshri2@gmail.com">kinshukeshri2@gmail.com</a>
  <div class="btns">
    <a class="btn pri" href="https://linkedin.com/in/kinshu-keshri" target="_blank" rel="noopener">LinkedIn</a>
    <a class="btn" href="https://github.com/KINSHU07" target="_blank" rel="noopener">GitHub</a>
    <a class="btn" href="tel:+918340270721">+91 83402 70721</a>
  </div>
</div></section>

<footer><div class="wrap">© <span id="yr"></span> Kinshu Keshri</div></footer>

<script>
// Pipeline animation
const S=[["Scrape","Maps, Yellow Pages",1400],["Deduplicate","Merge repeats",1100],["Rule-score","0–100, 6 signals",760],["ICP-qualify","7/10 or higher",471],["Enrich","Web, phone, email",471],["Personalize","11 email templates",101]];
const M=["1,400+ raw records","Duplicates removed","Scored on 6 signals","471 qualified leads","Contacts enriched","101 high-priority leads"];
const box=document.getElementById("steps"),fill=document.getElementById("fill"),n=document.getElementById("n"),m=document.getElementById("m");
S.forEach((s,i)=>{const b=document.createElement("button");b.className="step";b.style.cursor="pointer";b.style.textAlign="left";b.style.font="inherit";b.style.color="inherit";b.innerHTML=s[0]+"<small>"+s[1]+"</small>";b.onclick=()=>{clearInterval(t);go(i)};box.appendChild(b)});
function go(i){[...box.children].forEach((c,j)=>c.classList.toggle("on",j<=i));fill.style.width=(S[i][2]/1400*100)+"%";n.textContent=M[i];m.textContent=S[i][2].toLocaleString()+" in the pipeline"}
let i=0,t;function start(){go(0);t=setInterval(()=>{i=(i+1)%S.length;go(i)},2200)}start();

// Project filter
document.querySelectorAll(".chip").forEach(c=>c.onclick=()=>{
  document.querySelectorAll(".chip").forEach(x=>x.setAttribute("aria-pressed",x===c));
  document.querySelectorAll(".proj").forEach(p=>p.hidden=!(c.dataset.f==="all"||p.dataset.t.includes(c.dataset.f)));
});

// Theme toggle
const root=document.documentElement;
document.getElementById("theme").onclick=()=>{
  const dark=root.dataset.theme?root.dataset.theme==="dark":matchMedia("(prefers-color-scheme:dark)").matches;
  root.dataset.theme=dark?"light":"dark";
};
document.getElementById("yr").textContent=new Date().getFullYear();
</script>
</body>
</html>
