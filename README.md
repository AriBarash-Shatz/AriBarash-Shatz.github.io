<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Hope Gangloff — Gallery (recreation)</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header" role="banner">
    <div class="wrap">
      <a class="brand" href="#">HOPE GANGLOFF</a>

      <nav class="main-nav" role="navigation" aria-label="Main">
        <button id="menuToggle" class="menu-toggle" aria-expanded="false" aria-controls="menuList">
          ☰
        </button>

        <ul id="menuList" class="nav-list">
          <li><a href="#paintings">Paintings</a></li>
          <li><a href="#drawings">Drawings</a></li>
          <li><a href="#postcards">Postcards</a></li>
          <li><a href="#posters">Posters</a></li>
          <li><a href="#illustrations">Illustrations</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <section id="gallery" class="wrap gallery" aria-label="Artwork gallery">
      <!-- Example item format: replace src and alt with your images and captions -->
      <article class="card" tabindex="0">
        <a class="media" href="images/IMG_3032.jpg" aria-label="Open full image: Search In the Rain">
          <img src="images/IMG_3032.jpg" alt="Search In the Rain — acrylic on canvas" loading="lazy">
          <div class="meta">
            <h3 class="title">Search In the Rain</h3>
            <p class="subtitle">Acrylic on canvas — 36" × 62" — 2017</p>
          </div>
        </a>
      </article>

      <article class="card" tabindex="0">
        <a class="media" href="images/IMG_5567.jpg" aria-label="Open full image: Birch Stand">
          <img src="images/IMG_5567.jpg" alt="Birch Stand — 2019" loading="lazy">
          <div class="meta">
            <h3 class="title">Birch Stand South of Cheney Cabin</h3>
            <p class="subtitle">2019</p>
          </div>
        </a>
      </article>

      <article class="card" tabindex="0">
        <a class="media" href="images/Hope_Halya_fullsize-1.jpg" aria-label="Open full image: Portrait">
          <img src="images/Hope_Halya_fullsize-1.jpg" alt="Portrait — acrylic on linen" loading="lazy">
          <div class="meta">
            <h3 class="title">Portrait</h3>
            <p class="subtitle">Acrylic on linen — 72" × 48"</p>
          </div>
        </a>
      </article>

      <!-- repeat card elements for all images -->
    </section>

    <section class="wrap info" id="contact" aria-labelledby="contactHeading">
      <h2 id="contactHeading">Contact & Representation</h2>
      <p>Represented by Susan Inglett Gallery — inquiries: <a href="mailto:info@inglettgallery.com">info@inglettgallery.com</a></p>
    </section>
  </main>

  <footer class="site-footer">
    <div class="wrap">
      <p>&copy; <span id="year"></span> Hope Gangloff — recreation</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
/* styles.css — precise spacing & hover effects tuned for gallery look-and-feel */

/* ---------- variables ---------- */
:root{
  --bg: #f9f7f3;       /* soft off-white */
  --paper: #ffffff;
  --text: #0b0b0b;
  --muted: #6b6b6b;
  --accent: #000000;
  --gap: 20px;
  --card-radius: 6px;
  --shadow-elev: 10px 18px 28px rgba(10,10,10,0.06);
  --hover-shadow: 10px 30px 50px rgba(10,10,10,0.12);
  --max-width: 1180px;
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  font-size: 16px;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
}

/* Respect reduced motion preference */
@media (prefers-reduced-motion: reduce) {
  * { transition: none !important; animation: none !important; scroll-behavior: auto !important; }
}

/* ---------- layout ---------- */
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  line-height:1.35;
}

/* wrapper to center content and limit width */
.wrap{
  width:calc(100% - 48px);
  max-width:var(--max-width);
  margin:0 auto;
}

/* header */
.site-header{
  position:sticky;
  top:0;
  background:linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,255,255,0.92));
  backdrop-filter: blur(6px);
  border-bottom:1px solid rgba(0,0,0,0.04);
  z-index:50;
}
.site-header .wrap{
  display:flex;
  gap:12px;
  align-items:center;
  justify-content:space-between;
  padding:20px 0;
}

/* brand */
.brand{
  font-weight:700;
  letter-spacing:0.12em;
  text-decoration:none;
  color:var(--accent);
  font-size:0.98rem;
}

/* nav */
.main-nav{ display:flex; align-items:center; gap:12px; }
.menu-toggle{
  display:none;
  border:0;
  background:transparent;
  font-size:1.05rem;
  cursor:pointer;
}
.nav-list{
  display:flex;
  gap:18px;
  list-style:none;
  margin:0;
  padding:0;
}
.nav-list a{
  text-decoration:none;
  color:var(--text);
  font-size:0.95rem;
  padding:6px 4px;
  border-radius:4px;
}
.nav-list a:hover,
.nav-list a:focus{
  outline:none;
  color:var(--accent);
  text-decoration:underline;
}

/* gallery grid */
.gallery{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  gap:var(--gap);
  padding:28px 0 60px;
}

/* card */
.card{
  background:transparent;
  border-radius:var(--card-radius);
  overflow:visible;
  position:relative;
  min-height:160px;
  display:flex;
  align-items:stretch;
}
.card:focus-within { outline: 3px solid rgba(0,0,0,0.06); border-radius:var(--card-radius); }

/* anchor contains media + meta */
.media{
  display:block;
  width:100%;
  text-decoration:none;
  color:inherit;
  border-radius:var(--card-radius);
  overflow:hidden;
  position:relative;
  background:var(--paper);
  box-shadow: var(--shadow-elev);
  transition: transform 280ms cubic-bezier(.2,.9,.25,1), box-shadow 280ms;
}

/* image sizing — keep a consistent tall crop similar to the inspiration */
.media img{
  display:block;
  width:100%;
  height: calc(100% * 0.68);
  object-fit:cover;
  transform-origin:center center;
  transition: transform 360ms cubic-bezier(.2,.9,.25,1);
}

/* caption overlay at bottom */
.meta{
  position:absolute;
  left:0;
  right:0;
  bottom:0;
  padding:14px 16px;
  transform: translateY(0%);
  background: linear-gradient(180deg, rgba(255,255,255,0.0), rgba(8,8,8,0.58));
  color: #fff;
  transition: transform 300ms ease, background 300ms ease;
  display:flex;
  flex-direction:column;
  gap:4px;
}
.title{
  margin:0;
  font-size:1.02rem;
  font-weight:600;
  line-height:1.1;
}
.subtitle{
  margin:0;
  font-size:0.86rem;
  color: rgba(255,255,255,0.85);
  font-weight:400;
}

/* hover / focus effects: scale image, lift card, slide caption up slightly */
.media:hover, .media:focus{
  transform: translateY(-6px);
  box-shadow: var(--hover-shadow);
}
.media:hover img, .media:focus img{
  transform: scale(1.035);
}
.media:hover .meta, .media:focus .meta{
  transform: translateY(-8px);
  background: linear-gradient(180deg, rgba(255,255,255,0.0), rgba(8,8,8,0.68));
}

/* small screens */
@media (max-width:980px){
  .gallery{ grid-template-columns: repeat(2, 1fr); gap:16px; }
  .wrap{ width:calc(100% - 32px) }
}

/* phones */
@media (max-width:640px){
  .site-header .wrap{ padding:14px 0; }
  .menu-toggle{ display:inline-flex; }
  .nav-list{
    position:absolute;
    top:68px;
    right:24px;
    background:var(--paper);
    border:1px solid rgba(0,0,0,0.06);
    box-shadow: 0 6px 18px rgba(0,0,0,0.06);
    flex-direction:column;
    gap:0;
    padding:8px;
    display:none;
    border-radius:6px;
  }
  .nav-list a{ padding:10px 14px; display:block; white-space:nowrap; }
  .gallery{ grid-template-columns: 1fr; gap:14px; padding:18px 0; }
}

/* footer */
.site-footer{
  border-top:1px solid rgba(0,0,0,0.04);
  color:var(--muted);
  padding:24px 0;
  text-align:center;
  font-size:0.95rem;
}
// script.js — small interactions: menu toggle, keyboard "Enter" open, set year
(function () {
  // set copyright year
  const y = new Date().getFullYear();
  document.getElementById('year').textContent = y;

  // mobile menu toggle
  const menuToggle = document.getElementById('menuToggle');
  const menuList = document.getElementById('menuList');
  menuToggle?.addEventListener('click', function () {
    const expanded = this.getAttribute('aria-expanded') === 'true';
    this.setAttribute('aria-expanded', String(!expanded));
    if (!expanded) {
      menuList.style.display = 'flex';
    } else {
      menuList.style.display = 'none';
    }
  });

  // Make cards open images with keyboard Enter key when focused
  document.querySelectorAll('.card').forEach(card => {
    card.addEventListener('keypress', (e) => {
      if (e.key === 'Enter') {
        const link = card.querySelector('.media');
        if (link) link.click();
      }
    });
  });

  // Simple lightbox: open full-size images in a centered overlay
  // NOTE: this is optional, small, and non-blocking — you can remove it if you want native open behavior.
  document.querySelectorAll('.media').forEach(link => {
    link.addEventListener('click', (evt) => {
      evt.preventDefault();
      const href = link.getAttribute('href');
      openLightbox(href, link.querySelector('img').alt || '');
    });
  });

  function openLightbox(src, alt) {
    // create overlay nodes
    const overlay = document.createElement('div');
    overlay.className = 'lg-overlay';
    overlay.tabIndex = 0;
    overlay.innerHTML = `
      <div class="lg-inner" role="dialog" aria-label="${escapeHtml(alt)}">
        <button class="lg-close" aria-label="Close">✕</button>
        <img src="${escapeHtml(src)}" alt="${escapeHtml(alt)}">
      </div>
    `;
    document.body.appendChild(overlay);
    document.body.style.overflow = 'hidden';
    // close handlers
    overlay.querySelector('.lg-close').addEventListener('click', close);
    overlay.addEventListener('click', (e) => { if (e.target === overlay) close(); });
    overlay.addEventListener('keyup', (e) => { if (e.key === 'Escape') close(); });
    overlay.focus();

    function close() {
      document.body.style.overflow = '';
      overlay.remove();
    }
  }

  function escapeHtml(s) {
    return String(s).replace(/[&<>"']/g, (m) => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[m]));
  }
})();
