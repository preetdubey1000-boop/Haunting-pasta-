<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Haunting Pasta Wiki</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Uncial+Antiqua&family=Montserrat:wght@300;400;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0b10; --panel:#0f1114; --accent:#8b0000; --muted:#9aa0a6; --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Montserrat,system-ui,Roboto,Arial;background:radial-gradient( circle at 10% 10%, #0a0a0f 0%, #050507 40%, #030304 100% );color:#e6e6e6}
    /* header */
    header{display:flex;align-items:center;justify-content:space-between;padding:18px 28px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);backdrop-filter: blur(4px);border-bottom:1px solid rgba(255,255,255,0.03)}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:56px;height:56px;border-radius:12px;display:grid;place-items:center;background:linear-gradient(135deg,#1a0505, #3b0000);box-shadow:0 6px 20px rgba(0,0,0,0.7), inset 0 -6px 24px rgba(255,255,255,0.02)}
    .logo svg{width:38px;height:38px}
    h1{font-family: 'Uncial Antiqua', serif;margin:0;font-size:20px;letter-spacing:1px}
    .subtitle{font-size:12px;color:var(--muted)}/* layout */
.container{display:grid;grid-template-columns:320px 1fr;gap:20px;padding:22px}
nav{padding:18px;background:var(--panel);border-radius:12px;height:calc(100vh - 116px);overflow:auto;border:1px solid rgba(255,255,255,0.02)}
main{height:calc(100vh - 116px);overflow:auto}

/* search */
.searchbox{display:flex;gap:8px;align-items:center;margin-bottom:14px}
.searchbox input{flex:1;padding:10px 12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:var(--glass);color:inherit}
.filters{display:flex;flex-direction:column;gap:8px}
.pill{padding:8px 10px;border-radius:999px;background:rgba(255,255,255,0.02);font-size:13px;color:var(--muted);display:inline-block}

/* list */
.list{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:14px;padding:12px}
.card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.005));border-radius:12px;padding:10px;position:relative;overflow:hidden;border:1px solid rgba(255,255,255,0.03);cursor:pointer}
.thumb{height:140px;border-radius:8px;overflow:hidden;background:#000;display:flex;align-items:center;justify-content:center}
.thumb img{width:100%;height:100%;object-fit:cover;display:block;transform:scale(1);transition:transform .7s}
.card:hover .thumb img{transform:scale(1.06)}
.meta{padding-top:8px}
.title{font-weight:700;margin:0;font-size:14px}
.short{font-size:13px;color:var(--muted);margin-top:6px}

/* modal */
.modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;padding:24px}
.modal.active{display:flex}
.modal .panel{background:linear-gradient(180deg,#0b0b0f,#071014);border-radius:14px;padding:18px;max-width:900px;width:100%;max-height:90vh;overflow:auto;border:1px solid rgba(255,255,255,0.04)}
.modal .hero{display:flex;gap:18px}
.hero .image{width:360px;height:300px;border-radius:8px;overflow:hidden;flex-shrink:0}
.hero img{width:100%;height:100%;object-fit:cover;display:block}
.hero .info{flex:1}
.meta-row{display:flex;gap:12px;flex-wrap:wrap;margin-top:10px}
.ghostly{color:var(--accent);font-weight:700}

/* footer */
footer{padding:14px 28px;color:var(--muted);font-size:13px}

/* spooky touches */
.glow{filter:drop-shadow(0 0 8px rgba(139,0,0,0.6))}
.scanline:after{content:"";position:absolute;inset:0;background:linear-gradient(transparent 40%, rgba(255,255,255,0.02) 50%, transparent 60%);mix-blend-mode:overlay;pointer-events:none}
.typewriter{display:inline-block;overflow:hidden;white-space:nowrap;animation:type 6s steps(40) infinite}
@keyframes type{0%{width:0}50%{width:100%}100%{width:0}}

/* responsive */
@media(max-width:880px){.container{grid-template-columns:1fr}.logo{display:none}.subtitle{display:none}.brand h1{font-size:16px}.hero .image{width:220px;height:180px}}

  </style>
</head>
<body>
  <header>
    <div class="brand">
      <div class="logo glow" title="Haunting Pasta Wiki"> 
        <!-- spooky SVG -->
        <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M32 4c10.5 0 19 8.5 19 19s-8.5 19-19 19S13 33.5 13 23 21.5 4 32 4z" fill="#a30000" opacity="0.9"/><path d="M20 44c3-6 10-8 12-8s9 2 12 8c3 6 2 12-12 16-14-4-15-10-12-16z" fill="#1b1b1b"/></svg>
      </div>
      <div>
        <h1>Haunting Pasta Wiki</h1>
        <div class="subtitle">5,000+ accounts • Real claims, user submitted</div>
      </div>
    </div>
    <div style="display:flex;gap:12px;align-items:center">
      <div class="pill">Dark • Creepy</div>
      <div class="pill">Indexed • Searchable</div>
    </div>
  </header>  <div class="container">
    <nav>
      <div class="searchbox">
        <input id="search" placeholder="Search title, location, tags..." />
        <button id="randomBtn" title="Surprise me">🎲</button>
      </div>
      <div class="filters">
        <div><strong>Filters</strong></div>
        <div class="pill" id="filterRecent">Recent</div>
        <div class="pill" id="filterVerified">Verified</div>
        <div style="margin-top:8px"><strong>Categories</strong></div>
        <div class="pill">Ghosts</div>
        <div class="pill">Shadow People</div>
        <div class="pill">Poltergeist</div>
        <div style="margin-top:8px"><strong>Tips</strong></div>
        <div style="font-size:13px;color:var(--muted);line-height:1.4">Add real evidence images to the <code>images/</code> folder and update <code>stories.json</code>. Use original sources only — do not impersonate.</div>
      </div>
    </nav><main>
  <section style="padding:12px 18px">
    <div style="display:flex;align-items:center;justify-content:space-between">
      <h2 style="margin:0">Stories <span class="typewriter">— whispered, recorded, remembered</span></h2>
      <div style="color:var(--muted);font-size:13px">Showing <span id="count">0</span> stories</div>
    </div>

    <div id="list" class="list scanline"></div>

    <div style="display:flex;gap:10px;align-items:center;justify-content:center;padding:18px">
      <button id="prev">◀ Prev</button>
      <div id="pages" style="color:var(--muted)"></div>
      <button id="next">Next ▶</button>
    </div>
  </section>

  <footer>
    <div>Made with eerie love — Use responsibly. Replace demo placeholders with real user-submitted stories and images stored in <code>stories.json</code> and <code>/images</code>.</div>
  </footer>
</main>

  </div>  <!-- Modal -->  <div id="modal" class="modal" role="dialog" aria-hidden="true">
    <div class="panel">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <h3 id="mTitle">Title</h3>
        <div style="display:flex;gap:8px;align-items:center"><button id="closeModal">Close ✖</button></div>
      </div>
      <div class="hero">
        <div class="image"><img id="mImg" src="" alt="ghost image" loading="lazy"/></div>
        <div class="info">
          <div id="mText" style="line-height:1.6"></div>
          <div class="meta-row">
            <div class="pill" id="mLocation">Location</div>
            <div class="pill" id="mDate">Date</div>
            <div class="pill" id="mTags">Tags</div>
          </div>
        </div>
      </div>
      <div style="margin-top:14px;color:var(--muted);font-size:13px">Sources / Notes: <span id="mSource"></span></div>
    </div>
  </div>  <script>
    // Demo engine — scalable to 5,000+ stories by loading an external stories.json file.
    // To use real stories: place a JSON array of story objects in ./stories.json with fields:
    // {id, title, excerpt, content, image, location, date, tags, verified, source}

    const PAGE_SIZE = 20;
    let stories = [];
    let currentPage = 1;
    let filtered = [];

    // Helper: create a demo dataset of 5000 placeholders (replace with real data file in production)
    function makeDemo(n=5000){
      const demo = [];
      for(let i=1;i<=n;i++){
        demo.push({
          id: i,
          title: `Haunting #${i}: The House on Lane ${((i%120)+1)}`,
          excerpt: `A brief whisper about event ${i}. Witness reported cold spots and footsteps.`,
          content: `Full account for event ${i}. This is placeholder content generated for demo. Replace with real story text.`,
          image: `images/ghost-${(i%12)+1}.jpg`, // expects images/ghost-1.jpg ... images/ghost-12.jpg as demo
          location: `City ${(i%50)+1}`,
          date: `202${i%6}-0${(i%9)+1}-0${((i%27)+1)}`,
          tags: [i%3===0? 'Poltergeist':'Shadow', i%5===0? 'Verified':'' ].filter(Boolean),
          verified: i%7===0,
          source: i%11===0? `Submitted by user${i}@example.com` : ''
        })
      }
      return demo;
    }

    // If you have a real stories.json file, uncomment the fetch below and remove demo generator.
    // fetch('stories.json').then(r=>r.json()).then(data=>{stories=data; init();}).catch(e=>{console.warn('Could not load stories.json — using demo.');stories=makeDemo(5000);init();});

    // For the purposes of this single-file demo we generate 5,000 placeholders.
    stories = makeDemo(5000);
    init();

    function init(){
      filtered = stories.slice();
      renderPage(1);
      document.getElementById('search').addEventListener('input', onSearch);
      document.getElementById('prev').addEventListener('click', ()=>changePage(currentPage-1));
      document.getElementById('next').addEventListener('click', ()=>changePage(currentPage+1));
      document.getElementById('randomBtn').addEventListener('click', openRandom);
      document.getElementById('closeModal').addEventListener('click', closeModal);
      document.getElementById('modal').addEventListener('click', (e)=>{if(e.target.id==='modal') closeModal();});
      document.getElementById('filterVerified').addEventListener('click',()=>{filtered = stories.filter(s=>s.verified);renderPage(1)});
      document.getElementById('filterRecent').addEventListener('click',()=>{filtered = stories.slice().sort((a,b)=> new Date(b.date)-new Date(a.date));renderPage(1)});
    }

    function onSearch(e){
      const q = e.target.value.trim().toLowerCase();
      if(!q){filtered = stories.slice(); renderPage(1); return}
      filtered = stories.filter(s=> (s.title+s.excerpt+s.location+(s.tags||[]).join(' ')).toLowerCase().includes(q));
      renderPage(1);
    }

    function renderPage(page){
      currentPage = Math.max(1, Math.min(page, Math.ceil(filtered.length/PAGE_SIZE)||1));
      const start = (currentPage-1)*PAGE_SIZE;
      const items = filtered.slice(start, start+PAGE_SIZE);
      const list = document.getElementById('list'); list.innerHTML='';
      items.forEach(it=>{
        const card = document.createElement('div'); card.className='card';
        card.innerHTML = `<div class="thumb">${imgTag(it.image,it.id)}</div>
          <div class="meta">
            <div class="title">${escapeHtml(it.title)}</div>
            <div class="short">${escapeHtml(it.excerpt)}</div>
          </div>`;
        card.addEventListener('click', ()=>openModal(it));
        list.appendChild(card);
      })
      document.getElementById('count').textContent = filtered.length.toLocaleString();
      document.getElementById('pages').textContent = `Page ${currentPage} / ${Math.max(1,Math.ceil(filtered.length/PAGE_SIZE))}`;
      // preload images for the page
      items.forEach(i=>{const im=new Image();im.src=i.image;});
    }

    function changePage(page){ renderPage(page); }

    function openModal(story){
      document.getElementById('mTitle').textContent = story.title;
      const img = document.getElementById('mImg'); img.src = story.image; img.onerror = ()=>{img.src = placeholderSVG();}
      document.getElementById('mText').textContent = story.content;
      document.getElementById('mLocation').textContent = story.location || 'Unknown';
      document.getElementById('mDate').textContent = story.date || 'Unknown';
      document.getElementById('mTags').textContent = (story.tags||[]).join(', ');
      document.getElementById('mSource').textContent = story.source||'—';
      document.getElementById('modal').classList.add('active');
      document.getElementById('modal').setAttribute('aria-hidden','false');
    }
    function closeModal(){document.getElementById('modal').classList.remove('active');document.getElementById('modal').setAttribute('aria-hidden','true');}

    function openRandom(){ const r = stories[Math.floor(Math.random()*stories.length)]; openModal(r); }

    function imgTag(src,id){
      // Use a real image path if available, otherwise fallback to inline SVG silhouette.
      return `<img src="${src}" alt="ghost ${id}" loading="lazy" onerror="this.onerror=null;this.src='data:image/svg+xml;utf8,${encodeURIComponent(placeholderSVG())}'"/>`;
    }

    function placeholderSVG(){
      // a subtle ghost silhouette SVG as fallback (returns markup string)
      return `data:image/svg+xml;utf8,${encodeURIComponent(`
        <svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 200'>
          <rect width='100%' height='100%' fill='#0b0b10'/>
          <g fill='none' stroke='#8b0000' stroke-opacity='0.9' stroke-width='2'>
            <path d='M150 40c30 0 42 20 42 52s-12 46-42 46-42-12-42-46 12-52 42-52z' fill='#111'/>
          </g>
          <text x='50%' y='90%' font-family='Montserrat' font-size='12' fill='#7f7f7f' text-anchor='middle'>Ghost image missing</text>
        </svg>
      `)}`;
    }

    function escapeHtml(s){ return (s+'').replace(/[&<>"']/g, function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":"&#39;"}[c]}); }

    // Accessibility: keyboard close
    window.addEventListener('keydown', (e)=>{ if(e.key==='Escape') closeModal(); });

  </script></body>
</html>
