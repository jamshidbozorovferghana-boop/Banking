<!doctype html>

<html lang="uz">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Banking.uz — Bank maqolalari</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
  <style>
    /* =========================
       Variables / Palette
       ========================= */
    :root{
      --turquoise:#2aa6a1; /* primary */
      --gold:#d4a017; /* accent */
      --beige:#f8f6f2; /* page bg */
      --deep:#182026; /* text */
      --muted:#6b6b6b;
      --max-width:1100px;
      --radius:12px;
      --pattern-opacity:0.06;
    }/* Reset / base */
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
  background:var(--beige);color:var(--deep);-webkit-font-smoothing:antialiased;
  line-height:1.5;font-size:16px;
  -webkit-text-size-adjust:100%;
}

a{color:inherit;text-decoration:none}

/* Layout container */
.container{max-width:var(--max-width);margin:0 auto;padding:28px}

/* Header */
header{display:flex;align-items:center;justify-content:space-between;padding:12px 0}
.brand{display:flex;align-items:center;gap:14px}
.logo{
  width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--turquoise),#57c6c0);
  display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-family:Playfair Display,serif;font-size:20px;box-shadow:0 6px 18px rgba(24,32,38,0.08)
}
.site-name{font-weight:700;font-family:Playfair Display,serif}
nav a{margin-left:18px;color:var(--deep);font-weight:600}

/* Hero */
.hero{
  margin-top:18px;padding:36px;border-radius:16px;position:relative;overflow:hidden;
  background:linear-gradient(180deg,rgba(255,255,255,0.6),rgba(255,255,255,0.4));
  box-shadow:0 8px 30px rgba(24,32,38,0.06)
}
.hero-grid{display:flex;gap:24px;align-items:center}
.hero-left{flex:1}
.hero h1{margin:0;font-size:32px;font-family:Playfair Display,serif}
.hero p{margin-top:10px;color:var(--muted)}
.cta-row{margin-top:18px;display:flex;gap:12px}
.btn{padding:10px 16px;border-radius:10px;font-weight:600;cursor:pointer;border:0}
.btn-primary{background:var(--turquoise);color:white}
.btn-outline{background:transparent;border:2px solid rgba(0,0,0,0.06)}

/* Hero pattern (Uzbek motif) */
.motif{position:absolute;right:-6%;top:-6%;opacity:var(--pattern-opacity);width:420px;height:420px;transform:rotate(10deg)}

/* Articles section */
.articles{margin-top:28px;display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
.card{background:white;padding:16px;border-radius:12px;box-shadow:0 6px 18px rgba(24,32,38,0.06);display:flex;flex-direction:column;gap:10px}
.card img{width:100%;height:140px;object-fit:cover;border-radius:8px}
.category{font-size:12px;color:var(--muted);font-weight:600}
.card h3{margin:0;font-size:18px}
.card p{margin:0;color:var(--muted);font-size:14px}
.read-more{margin-top:auto;display:flex;justify-content:space-between;align-items:center}

/* Article page (single view) */
.article-page{display:none;padding:26px;background:white;border-radius:12px;box-shadow:0 8px 30px rgba(24,32,38,0.06);margin-top:28px}
.article-page.active{display:block}
.breadcrumbs{font-size:13px;color:var(--muted);margin-bottom:12px}
.article-hero{display:flex;gap:20px;align-items:flex-start}
.article-hero img{width:220px;height:140px;object-fit:cover;border-radius:10px}
.article-meta{color:var(--muted);font-size:14px}

/* Footer */
footer{margin-top:40px;padding:18px 0;color:var(--muted);font-size:14px}
.footer-motif{height:36px;display:inline-block;vertical-align:middle;margin-left:10px;opacity:0.9}

/* Responsive */
@media (max-width:820px){
  .hero-grid{flex-direction:column}
  .article-hero{flex-direction:column}
  .logo{width:48px;height:48px}
}

/* Small utility */
.muted{color:var(--muted)}

  </style>
</head>
<body>
  <div style="position:relative;overflow:hidden;">
    <!-- Decorative repeating motif in background using inline SVG for Uzbek feel -->
    <svg class="motif" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" aria-hidden>
      <defs>
        <pattern id="uzmotif" width="40" height="40" patternUnits="userSpaceOnUse">
          <rect width="40" height="40" fill="none"></rect>
          <path d="M20 2 L24 16 L36 20 L24 24 L20 38 L16 24 L4 20 L16 16 Z" fill="var(--turquoise)"></path>
        </pattern>
      </defs>
      <rect width="100%" height="100%" fill="url(#uzmotif)"></rect>
    </svg><div class="container">
  <header>
    <div class="brand">
      <div class="logo">B</div>
      <div>
        <div class="site-name">Banking.uz</div>
        <div class="muted" style="font-size:13px">Maqolalar va tahlillar — o'zbek tilida</div>
      </div>
    </div>
    <nav>
      <a href="#home" onclick="showSection('home')">Home</a>
      <a href="#articles" onclick="showSection('articles')">Maqolalar</a>
    </nav>
  </header>

  <!-- HERO / HOME -->
  <main id="home" class="hero">
    <div class="hero-grid">
      <div class="hero-left">
        <h1>Banking haqida oddiy, aniq va ishonchli maqolalar</h1>
        <p>Bank xizmatlari, risk boshqaruvi, shaxsiy moliya va fintech sohalaridagi amaliy maqolalar. Boshlovchilar va mutaxassislar uchun o'zbek tilida.</p>
        <div class="cta-row">
          <button class="btn btn-primary" onclick="showSection('articles')">Maqolalarga o‘tish</button>
          <button class="btn btn-outline" onclick="alert('Kirish: hali mavjud emas')">A'zo bo'lish</button>
        </div>
      </div>

      <div style="width:420px;max-width:40%;">
        <!-- Featured article card -->
        <div class="card" style="padding:18px;background:linear-gradient(180deg,white, #fbfbfb)">
          <div class="category">Trend</div>
          <h3>Banklashuvda yangi tendensiyalar: raqamli banklar va fintech</h3>
          <p class="muted">Qisqacha: Raqamli banklarning o'sishi, Open Banking, va mijoz tajribasini yaxshilash usullari.</p>
          <div class="read-more">
            <small class="muted">18 sentyabr 2025</small>
            <button class="btn" onclick="openArticle(1)">Batafsil</button>
          </div>
        </div>
      </div>

    </div>
  </main>

  <!-- ARTICLES LIST -->
  <section id="articles" style="margin-top:18px">
    <div style="display:flex;justify-content:space-between;align-items:center">
      <h2 style="margin:0">Maqolalar</h2>
      <div class="muted">Kategoriya: <strong>Banking Basics</strong></div>
    </div>

    <div class="articles" style="margin-top:14px">

      <!-- Sample cards -->
      <article class="card">
        <img src="https://images.unsplash.com/photo-1542228262-5b3f2b2b0b0b?auto=format&fit=crop&w=800&q=60" alt="article">
        <div class="category">Banking Basics</div>
        <h3>Bank hisoblarini tushunish: depozitdan kreditgacha</h3>
        <p>Depozit turlari, foizlar va hisob yuritish qoidalari haqida boshlang'ich uchun qo'llanma.</p>
        <div class="read-more">
          <small class="muted">12 sentyabr 2025</small>
          <div>
            <button class="btn" onclick="openArticle(2)">O'qish</button>
          </div>
        </div>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1515165562835-c5f78b6f1b2c?auto=format&fit=crop&w=800&q=60" alt="article">
        <div class="category">Personal Finance</div>
        <h3>Shaxsiy byudjet: oylik xarajatlarni boshqarish</h3>
        <p>Budjet tuzishning oddiy tizimi va eng ko'p uchraydigan xatoliklar.</p>
        <div class="read-more">
          <small class="muted">05 sentyabr 2025</small>
          <div>
            <button class="btn" onclick="openArticle(3)">O'qish</button>
          </div>
        </div>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=800&q=60" alt="article">
        <div class="category">Risk & Compliance</div>
        <h3>Kredit riskini baholash: asosiy ko'rsatkichlar</h3>
        <p>Kredit berishda qarz oluvchining to'lov qobiliyatini qanday baholash kerak.</p>
        <div class="read-more">
          <small class="muted">28 avgust 2025</small>
          <div>
            <button class="btn" onclick="openArticle(4)">O'qish</button>
          </div>
        </div>
      </article>

    </div>
  </section>

  <!-- Article single view (hidden by default) -->
  <section id="article-view" class="article-page" aria-live="polite"></section>

  <footer>
    <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap">
      <div>© <strong>Banking.uz</strong> — barcha huquqlar himoyalangan.</div>
      <div class="muted">Yaratildi: an'anaviy naqshlar + zamonaviy dizayn</div>
    </div>
  </footer>

</div>

  </div>  <script>
    // Simple navigation/show sections
    function showSection(id){
      document.getElementById('home').style.display = id === 'home' ? 'block' : 'none';
      document.getElementById('articles').style.display = id === 'articles' ? 'block' : 'none';
      // Hide article view when switching
      document.getElementById('article-view').classList.remove('active');
    }

    // Prepare initial state: show home
    showSection('home');

    // Minimal article data store (you will replace this with back-end data later)
    const articles = {
      1:{id:1,title:'Banklashuvda yangi tendensiyalar: raqamli banklar va fintech',category:'Trend',date:'2025-09-18',img:'https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=900&q=60',content:`<p>Raqamli banklar va fintech ekotizimi bank sohasini tubdan o'zgartirmoqda...</p><p>Open Banking, API integratsiyalari va foydalanuvchi tajribasini yaxshilash usullari haqida to'liq tahlil.</p>`},
      2:{id:2,title:'Bank hisoblarini tushunish: depozitdan kreditgacha',category:'Banking Basics',date:'2025-09-12',img:'https://images.unsplash.com/photo-1542228262-5b3f2b2b0b0b?auto=format&fit=crop&w=900&q=60',content:`<p>Bank hisoblari turi: shaxsiy, jamoaviy, biznes hisoblari...</p><h3>Depozit turlari</h3><p>Oddiy depozit, muddatli depozit va hisob-kitob xususiyatlari...</p>`},
      3:{id:3,title:"Shaxsiy byudjet: oylik xarajatlarni boshqarish",category:'Personal Finance',date:'2025-09-05',img:'https://images.unsplash.com/photo-1515165562835-c5f78b6f1b2c?auto=format&fit=crop&w=900&q=60',content:`<p>Shaxsiy byudjetni tuzish - bu moliyaviy intizomning asosi...</p>`},
      4:{id:4,title:'Kredit riskini baholash: asosiy ko\'rsatkichlar',category:'Risk & Compliance',date:'2025-08-28',img:'https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=900&q=60',content:`<p>Kredit riskini baholashda LTV, DTI va boshqa ko\'rsatkichlar muhim...</p>`}
    };

    function openArticle(id){
      const a = articles[id];
      if(!a) return alert('Maqola topilmadi');
      const view = document.getElementById('article-view');
      view.innerHTML = `\
        <div class="breadcrumbs"><a href="#" onclick="showSection('articles')">Maqolalar</a> › <span class="muted">${a.category}</span></div>\
        <h2>${a.title}</h2>\
        <div class="article-meta">${a.date} — <span class="muted">${a.category}</span></div>\
        <div class="article-hero" style="margin-top:12px">\
          <img src="${a.img}" alt="cover">\
          <div style="flex:1">${a.content}</div>\
        </div>\
        <div style="margin-top:22px;color:var(--muted)">Manba va tavsiyalar: maqolani kengaytiring va manbalarni ko'rsating.</div>\
      `;
      view.classList.add('active');
      // Hide other sections so the article reads like a page
      document.getElementById('home').style.display = 'none';
      document.getElementById('articles').style.display = 'none';
      window.scrollTo({top:0,behavior:'smooth'});
    }
  </script></body>
</html>
