<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Artist Gallery — Starter</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header">
    <div class="brand">Hope Gangloff (recreation)</div>
    <nav class="main-nav">
      <button class="menu-toggle" aria-expanded="false">Menu</button>
      <ul class="nav-list">
        <li><a href="#paintings">Paintings</a></li>
        <li><a href="#drawings">Drawings</a></li>
        <li><a href="#postcards">Postcards</a></li>
        <li><a href="#posters">Posters</a></li>
        <li><a href="#illustrations">Illustrations</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="gallery" class="gallery">
      <!-- Example gallery items. Replace src and data-title as needed -->
      <figure class="card">
        <img src="images/IMG_3032.jpg" alt="Search In the Rain" loading="lazy">
        <figcaption>
          <h3>Search In the Rain</h3>
          <p>Acrylic on canvas. 36" x 62". 2017.</p>
        </figcaption>
      </figure>

      <figure class="card">
        <img src="images/IMG_5567.jpg" alt="Birch Stand South of Cheney Cabin 2019" loading="lazy">
        <figcaption>
          <h3>Birch Stand South of Cheney Cabin</h3>
          <p>2019</p>
        </figcaption>
      </figure>

      <figure class="card">
        <img src="images/Hope_Halya_fullsize-1.jpg" alt="Portrait" loading="lazy">
        <figcaption>
          <h3>Portrait</h3>
          <p>Acrylic on linen. 72" x 48". 2016.</p>
        </figcaption>
      </figure>

      <!-- add more items here -->
    </section>
  </main>

  <footer class="site-footer" id="contact">
    <p>Represented by Susan Inglett Gallery — inquiries: info@inglettgallery.com</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
