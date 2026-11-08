<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GUDANG PILIHAN - Belanja Cerdas, Pilihan Berkualitas!</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
  <style>
    :root {
      --primary: #ff5722;
      --primary-dark: #e64a19;
      --primary-light: #fff3ef;
      --dark: #111827;
      --dark-soft: #1f2937;
      --gray: #6b7280;
      --gray-light: #f3f4f6;
      --border: #e5e7eb;
      --white: #ffffff;
      --tiktok: #000000;
      --shopee: #ee4d2d;
      --whatsapp: #25d366;
      --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.08);
      --radius: 14px;
      --transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Plus Jakarta Sans', sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background-color: #fafafa;
      color: var(--dark);
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button {
      cursor: pointer;
      border: none;
      outline: none;
      font-family: inherit;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* HEADER */
    header {
      background: var(--white);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.03);
    }

    .nav-wrapper {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 14px 0;
      gap: 20px;
    }

    .brand {
      display: flex;
      flex-direction: column;
    }

    .brand-logo {
      font-size: 1.45rem;
      font-weight: 800;
      letter-spacing: -0.5px;
      color: var(--dark);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .brand-logo span {
      color: var(--primary);
    }

    .brand-slogan {
      font-size: 0.75rem;
      color: var(--gray);
      font-weight: 500;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 24px;
      align-items: center;
    }

    nav a {
      font-size: 0.92rem;
      font-weight: 600;
      color: var(--dark-soft);
      transition: var(--transition);
      position: relative;
    }

    nav a:hover,
    nav a.active {
      color: var(--primary);
    }

    .menu-toggle {
      display: none;
      background: var(--gray-light);
      padding: 8px 12px;
      border-radius: 8px;
      font-size: 1.2rem;
      color: var(--dark);
    }

    /* HERO BANNER */
    .hero {
      background: linear-gradient(135deg, var(--dark) 0%, #262626 60%, #3b1d14 100%);
      color: var(--white);
      padding: 72px 0;
      position: relative;
      overflow: hidden;
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 380px;
      height: 380px;
      background: radial-gradient(circle, rgba(255, 87, 34, 0.35) 0%, transparent 70%);
      top: -100px;
      right: -80px;
      pointer-events: none;
    }

    .hero-content {
      max-width: 720px;
      position: relative;
      z-index: 2;
      animation: fadeUp 0.7s ease-out;
    }

    .hero-badge {
      display: inline-block;
      background: rgba(255, 87, 34, 0.18);
      color: #ff8a65;
      border: 1px solid rgba(255, 87, 34, 0.4);
      padding: 6px 14px;
      border-radius: 999px;
      font-size: 0.82rem;
      font-weight: 700;
      letter-spacing: 0.5px;
      margin-bottom: 16px;
    }

    .hero h1 {
      font-size: clamp(2rem, 4.5vw, 3.1rem);
      font-weight: 800;
      line-height: 1.15;
      margin-bottom: 14px;
    }

    .hero h1 span {
      color: var(--primary);
    }

    .hero p {
      font-size: 1.05rem;
      color: #d1d5db;
      margin-bottom: 28px;
      max-width: 600px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 13px 24px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.95rem;
      transition: var(--transition);
    }

    .btn-shopee {
      background: var(--shopee);
      color: var(--white);
      box-shadow: 0 8px 20px rgba(238, 77, 45, 0.35);
    }

    .btn-shopee:hover {
      background: #d83f20;
      transform: translateY(-2px);
    }

    .btn-tiktok {
      background: var(--white);
      color: var(--dark);
    }

    .btn-tiktok:hover {
      background: var(--gray-light);
      transform: translateY(-2px);
    }

    /* SEARCH & FILTER BAR */
    .search-section {
      margin-top: -28px;
      position: relative;
      z-index: 10;
    }

    .search-box {
      background: var(--white);
      padding: 16px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items: center;
      border: 1px solid var(--border);
    }

    .search-input-wrap {
      flex: 1;
      min-width: 240px;
      position: relative;
    }

    .search-input-wrap input {
      width: 100%;
      padding: 12px 16px 12px 42px;
      border: 1px solid var(--border);
      border-radius: 10px;
      font-size: 0.95rem;
      outline: none;
      transition: var(--transition);
    }

    .search-input-wrap input:focus {
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(255, 87, 34, 0.12);
    }

    .search-icon {
      position: absolute;
      left: 14px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--gray);
    }

    .sort-tabs {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }

    .tab-btn {
      padding: 10px 16px;
      border-radius: 10px;
      background: var(--gray-light);
      color: var(--dark-soft);
      font-weight: 600;
      font-size: 0.88rem;
      transition: var(--transition);
    }

    .tab-btn.active,
    .tab-btn:hover {
      background: var(--primary);
      color: var(--white);
    }

    /* SECTION GENERAL */
    section {
      padding: 56px 0;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 28px;
      gap: 16px;
      flex-wrap: wrap;
    }

    .section-title {
      font-size: 1.6rem;
      font-weight: 800;
      color: var(--dark);
    }

    .section-subtitle {
      font-size: 0.95rem;
      color: var(--gray);
      margin-top: 4px;
    }

    /* CATEGORIES */
    .categories-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(135px, 1fr));
      gap: 14px;
    }

    .category-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 18px 12px;
      text-align: center;
      transition: var(--transition);
      cursor: pointer;
    }

    .category-card:hover,
    .category-card.active {
      border-color: var(--primary);
      background: var(--primary-light);
      transform: translateY(-3px);
      box-shadow: var(--shadow);
    }

    .category-icon {
      font-size: 2rem;
      margin-bottom: 8px;
      display: block;
    }

    .category-name {
      font-size: 0.85rem;
      font-weight: 700;
      color: var(--dark);
    }

    /* PRODUCTS GRID */
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
      gap: 22px;
    }

    .product-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: var(--transition);
      animation: fadeUp 0.4s ease;
    }

    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow);
      border-color: #ffd0c2;
    }

    .product-img-wrap {
      position: relative;
      width: 100%;
      aspect-ratio: 4 / 3;
      background: var(--gray-light);
      overflow: hidden;
    }

    .product-img-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .product-card:hover .product-img-wrap img {
      transform: scale(1.05);
    }

    .product-badge {
      position: absolute;
      top: 12px;
      left: 12px;
      padding: 5px 11px;
      border-radius: 999px;
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--white);
      background: var(--primary);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
    }

    .product-badge.terlaris {
      background: #dc2626;
    }

    .product-badge.terbaru {
      background: #111827;
    }

    .product-body {
      padding: 18px;
      display: flex;
      flex-direction: column;
      flex: 1;
    }

    .product-cat {
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--primary);
      text-transform: uppercase;
      letter-spacing: 0.4px;
      margin-bottom: 6px;
    }

    .product-title {
      font-size: 1.05rem;
      font-weight: 700;
      color: var(--dark);
      margin-bottom: 8px;
      line-height: 1.35;
    }

    .product-desc {
      font-size: 0.87rem;
      color: var(--gray);
      margin-bottom: 14px;
      flex: 1;
    }

    .product-price {
      font-size: 1.2rem;
      font-weight: 800;
      color: var(--dark);
      margin-bottom: 14px;
    }

    .product-actions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }

    .btn-buy {
      padding: 10px 8px;
      border-radius: 8px;
      font-size: 0.78rem;
      font-weight: 700;
      text-align: center;
      color: var(--white);
      transition: var(--transition);
    }

    .btn-buy.shopee {
      background: var(--shopee);
    }

    .btn-buy.shopee:hover {
      background: #d83f20;
    }

    .btn-buy.tiktok {
      background: var(--tiktok);
    }

    .btn-buy.tiktok:hover {
      background: #2b2b2b;
    }

    .empty-state {
      grid-column: 1 / -1;
      text-align: center;
      padding: 48px 20px;
      background: var(--white);
      border-radius: var(--radius);
      border: 1px dashed var(--border);
      color: var(--gray);
    }

    /* ABOUT SECTION */
    .about-box {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 36px;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 32px;
      align-items: center;
    }

    .about-box h2 {
      font-size: 1.6rem;
      font-weight: 800;
      margin-bottom: 12px;
    }

    .about-box p {
      color: var(--gray);
      margin-bottom: 20px;
    }

    .social-links {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .social-btn {
      padding: 10px 16px;
      border-radius: 8px;
      font-size: 0.88rem;
      font-weight: 700;
      background: var(--gray-light);
      color: var(--dark);
      transition: var(--transition);
    }

    .social-btn:hover {
      background: var(--dark);
      color: var(--white);
    }

    .wa-card {
      background: var(--primary-light);
      border: 1px solid #ffd0c2;
      padding: 24px;
      border-radius: var(--radius);
      text-align: center;
    }

    .wa-card h3 {
      font-size: 1.15rem;
      margin-bottom: 8px;
    }

    .wa-card p {
      font-size: 0.88rem;
      margin-bottom: 16px;
    }

    .btn-wa {
      background: var(--whatsapp);
      color: var(--white);
      width: 100%;
    }

    .btn-wa:hover {
      background: #1eb956;
    }

    /* FOOTER */
    footer {
      background: var(--dark);
      color: var(--white);
      padding: 44px 0 28px;
      margin-top: 40px;
    }

    .footer-content {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 12px;
    }

    .footer-logo {
      font-size: 1.5rem;
      font-weight: 800;
    }

    .footer-logo span {
      color: var(--primary);
    }

    .footer-tagline {
      font-size: 1rem;
      color: #e5e7eb;
      font-weight: 600;
    }

    .footer-disclaimer {
      max-width: 650px;
      font-size: 0.85rem;
      color: #9ca3af;
      margin-top: 8px;
      padding-top: 16px;
      border-top: 1px solid #374151;
    }

    /* FLOATING WHATSAPP */
    .floating-wa {
      position: fixed;
      bottom: 22px;
      right: 22px;
      background: var(--whatsapp);
      color: var(--white);
      width: 56px;
      height: 56px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.6rem;
      box-shadow: 0 8px 20px rgba(37, 211, 102, 0.4);
      z-index: 999;
      transition: var(--transition);
    }

    .floating-wa:hover {
      transform: scale(1.08);
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(14px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* RESPONSIVE */
    @media (max-width: 860px) {
      .about-box {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 768px) {
      .menu-toggle {
        display: block;
      }

      nav {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: var(--white);
        border-bottom: 1px solid var(--border);
        display: none;
        padding: 16px 20px;
      }

      nav.open {
        display: block;
      }

      nav ul {
        flex-direction: column;
        align-items: flex-start;
        gap: 14px;
      }

      .hero {
        padding: 52px 0;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <div class="container nav-wrapper">
      <a href="#beranda" class="brand">
        <div class="brand-logo">GUDANG <span>PILIHAN</span></div>
        <div class="brand-slogan">Temukan Produk Favoritmu, Harga Terbaik Pilihanmu!</div>
      </a>

      <button class="menu-toggle" id="menuToggle" aria-label="Buka Menu">☰</button>

      <nav id="mainNav">
        <ul>
          <li><a href="#beranda" class="nav-link active">Beranda</a></li>
          <li><a href="#produk" class="nav-link" data-filter="Terbaru">Produk Terbaru</a></li>
          <li><a href="#produk" class="nav-link" data-filter="Terlaris">Produk Terlaris</a></li>
          <li><a href="#kategori" class="nav-link">Kategori</a></li>
          <li><a href="#tentang" class="nav-link">Tentang Kami</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- HERO BANNER -->
  <section class="hero" id="beranda">
    <div class="container">
      <div class="hero-content">
        <span class="hero-badge" id="bannerBadge">GUDANG PILIHAN</span>
        <h1 id="bannerTitle">Belanja Cerdas, <span>Pilihan Berkualitas!</span></h1>
        <p id="bannerSubtitle">Temukan berbagai produk menarik dengan harga terbaik dari Shopee dan TikTok Shop.</p>
        <div class="hero-buttons">
          <a href="#produk" class="btn btn-shopee" id="btnHeroShopee">🛍️ Lihat Produk Shopee</a>
          <a href="#produk" class="btn btn-tiktok" id="btnHeroTiktok">🎵 Lihat Produk TikTok</a>
        </div>
      </div>
    </div>
  </section>

  <!-- SEARCH & FILTER -->
  <div class="container search-section">
    <div class="search-box">
      <div class="search-input-wrap">
        <span class="search-icon">🔍</span>
        <input type="text" id="searchInput" placeholder="Cari produk, kategori, atau kata kunci..." />
      </div>
      <div class="sort-tabs">
        <button class="tab-btn active" data-tab="Semua">Semua</button>
        <button class="tab-btn" data-tab="Rekomendasi">Rekomendasi</button>
        <button class="tab-btn" data-tab="Terlaris">Terlaris</button>
        <button class="tab-btn" data-tab="Terbaru">Terbaru</button>
      </div>
    </div>
  </div>

  <!-- KATEGORI PRODUK -->
  <section id="kategori">
    <div class="container">
      <div class="section-header">
        <div>
          <h2 class="section-title">Kategori Pilihan</h2>
          <p class="section-subtitle">Pilih kategori untuk menyaring produk sesuai kebutuhan Anda</p>
        </div>
        <button class="tab-btn" id="resetCategoryBtn">Tampilkan Semua Kategori</button>
      </div>
      <div class="categories-grid" id="categoriesGrid"></div>
    </div>
  </section>

  <!-- DAFTAR PRODUK -->
  <section id="produk" style="padding-top: 10px;">
    <div class="container">
      <div class="section-header">
        <div>
          <h2 class="section-title" id="productSectionTitle">Semua Produk Pilihan</h2>
          <p class="section-subtitle" id="productCountInfo">Menampilkan produk terbaik dari Shopee & TikTok Shop</p>
        </div>
      </div>
      <div class="products-grid" id="productsGrid"></div>
    </div>
  </section>

  <!-- TENTANG KAMI & KONTAK -->
  <section id="tentang">
    <div class="container">
      <div class="about-box">
        <div>
          <h2>Tentang GUDANG PILIHAN</h2>
          <p>
            GUDANG PILIHAN adalah portal kurasi produk terbaik dari Shopee dan TikTok Shop.
            Kami membantu Anda menemukan barang berkualitas, viral, dan terlaris dengan harga paling bersahabat tanpa harus bingung mencari satu per satu.
          </p>
          <div class="social-links" id="socialLinks"></div>
        </div>
        <div class="wa-card">
          <h3>Butuh Bantuan atau Rekomendasi?</h3>
          <p>Hubungi admin kami langsung melalui WhatsApp untuk tanya produk atau kerja sama.</p>
          <a href="#" target="_blank" rel="noopener noreferrer" class="btn btn-wa" id="waButton">
            💬 Hubungi Admin via WhatsApp
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="container footer-content">
      <div class="footer-logo">GUDANG <span>PILIHAN</span></div>
      <div class="footer-tagline">"Belanja Mudah, Pilihan Tepat."</div>
      <p class="footer-disclaimer">
        Website ini merupakan media rekomendasi produk affiliate. Kami dapat menerima komisi dari pembelian melalui tautan affiliate tanpa biaya tambahan bagi pembeli.
      </p>
    </div>
  </footer>

  <!-- FLOATING WHATSAPP -->
  <a href="#" target="_blank" rel="noopener noreferrer" class="floating-wa" id="floatingWa" title="Chat Admin di WhatsApp">💬</a>

  <!-- =========================================================
       PENGATURAN WEBSITE (MUDAH DIEDIT)
       Ubah data di bawah ini untuk mengganti produk, link, banner,
       kategori, nomor WhatsApp, dan media sosial.
  ========================================================== -->
  <script>
    const SITE_CONFIG = {
      banner: {
        badge: "GUDANG PILIHAN",
        title: 'Belanja Cerdas, <span>Pilihan Berkualitas!</span>',
        subtitle: "Temukan berbagai produk menarik dengan harga terbaik dari Shopee dan TikTok Shop."
      },
      whatsappNumber: "6281234567890", // Gunakan format 628... tanpa tanda +
      whatsappMessage: "Halo Admin Gudang Pilihan, saya ingin bertanya tentang rekomendasi produk.",
      socials: [
        { name: "TikTok", url: "https://www.tiktok.com/@gudangpilihan" },
        { name: "Instagram", url: "https://www.instagram.com/gudangpilihan" },
        { name: "Facebook", url: "https://www.facebook.com/gudangpilihan" }
      ],
      categories: [
        { name: "Elektronik dan Gadget", icon: "📱" },
        { name: "Fashion Pria", icon: "👔" },
        { name: "Fashion Wanita", icon: "👗" },
        { name: "Peralatan Rumah Tangga", icon: "🏠" },
        { name: "Kecantikan dan Perawatan", icon: "✨" },
        { name: "Perlengkapan Dapur", icon: "🍳" },
        { name: "Aksesoris HP", icon: "🎧" },
        { name: "Produk Viral dan Trending", icon: "🔥" }
      ]
    };

    const PRODUCTS_DATA = [
      {
        id: 1,
        name: "TWS Earbuds Wireless Pro Bass",
        category: "Elektronik dan Gadget",
        price: "Rp 129.000",
        description: "Suara jernih, bass bertenaga, tahan hingga 24 jam pemakaian dengan casing pengisi daya.",
        image: "https://images.unsplash.com/photo-1590658268037-6bf12165a8df?auto=format&fit=crop&w=600&q=80",
        label: "Terlaris", // Pilihan: "Terlaris", "Rekomendasi", "Terbaru"
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-1",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-1"
      },
      {
        id: 2,
        name: "Kemeja Flanel Pria Premium",
        category: "Fashion Pria",
        price: "Rp 145.000",
        description: "Bahan katun lembut, adem dipakai seharian, cocok untuk gaya kasual maupun semi-formal.",
        image: "https://images.unsplash.com/photo-1596755094514-f87e34085b2c?auto=format&fit=crop&w=600&q=80",
        label: "Rekomendasi",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-2",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-2"
      },
      {
        id: 3,
        name: "Tas Selempang Wanita Minimalis",
        category: "Fashion Wanita",
        price: "Rp 165.000",
        description: "Desain elegan dengan kulit sintetis premium, muat HP, dompet, dan makeup harian.",
        image: "https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=600&q=80",
        label: "Terlaris",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-3",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-3"
      },
      {
        id: 4,
        name: "Air Fryer Digital 4.5 Liter",
        category: "Perlengkapan Dapur",
        price: "Rp 499.000",
        description: "Masak lebih sehat tanpa banyak minyak. Dilengkapi layar sentuh dan pengatur suhu otomatis.",
        image: "https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?auto=format&fit=crop&w=600&q=80",
        label: "Rekomendasi",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-4",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-4"
      },
      {
        id: 5,
        name: "Serum Vitamin C Glowing Skin",
        category: "Kecantikan dan Perawatan",
        price: "Rp 79.000",
        description: "Membantu mencerahkan wajah, menyamarkan noda hitam, dan melembapkan kulit.",
        image: "https://images.unsplash.com/photo-1620916566398-39f1143ab7be?auto=format&fit=crop&w=600&q=80",
        label: "Terbaru",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-5",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-5"
      },
      {
        id: 6,
        name: "Vacuum Cleaner Portable Mobil & Rumah",
        category: "Peralatan Rumah Tangga",
        price: "Rp 189.000",
        description: "Daya hisap kuat, ringan, tanpa kabel, praktis membersihkan debu di sudut sempit.",
        image: "https://images.unsplash.com/photo-1558317374-067fb5f30001?auto=format&fit=crop&w=600&q=80",
        label: "Terlaris",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-6",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-6"
      },
      {
        id: 7,
        name: "Holder HP Meja Lipat Aluminium",
        category: "Aksesoris HP",
        price: "Rp 45.000",
        description: "Kokoh, anti slip, ketinggian dan sudut kemiringan bisa diatur sesuka hati.",
        image: "https://images.unsplash.com/photo-1586953208448-b95a79798f07?auto=format&fit=crop&w=600&q=80",
        label: "Terbaru",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-7",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-7"
      },
      {
        id: 8,
        name: "Lampu Tidur Proyektor Bintang Viral",
        category: "Produk Viral dan Trending",
        price: "Rp 95.000",
        description: "Menciptakan suasana kamar estetik dengan efek galaksi dan warna lampu yang bisa diganti.",
        image: "https://images.unsplash.com/photo-1513506003901-1e6a229e2d15?auto=format&fit=crop&w=600&q=80",
        label: "Rekomendasi",
        shopeeUrl: "https://shopee.co.id/contoh-link-affiliate-8",
        tiktokUrl: "https://www.tiktok.com/contoh-link-affiliate-8"
      }
    ];

    // =========================================================
    // LOGIKA APLIKASI (TIDAK PERLU DIUBAH)
    // =========================================================
    let activeCategory = "Semua";
    let activeTab = "Semua";
    let searchQuery = "";

    const categoriesGrid = document.getElementById("categoriesGrid");
    const productsGrid = document.getElementById("productsGrid");
    const searchInput = document.getElementById("searchInput");
    const productSectionTitle = document.getElementById("productSectionTitle");
    const productCountInfo = document.getElementById("productCountInfo");

    // Inisialisasi Banner & Kontak
    document.getElementById("bannerBadge").textContent = SITE_CONFIG.banner.badge;
    document.getElementById("bannerTitle").innerHTML = SITE_CONFIG.banner.title;
    document.getElementById("bannerSubtitle").textContent = SITE_CONFIG.banner.subtitle;

    const waUrl = `https://wa.me/${SITE_CONFIG.whatsappNumber}?text=${encodeURIComponent(SITE_CONFIG.whatsappMessage)}`;
    document.getElementById("waButton").href = waUrl;
    document.getElementById("floatingWa").href = waUrl;

    // Render Media Sosial
    const socialLinksEl = document.getElementById("socialLinks");
    SITE_CONFIG.socials.forEach(soc => {
      const a = document.createElement("a");
      a.href = soc.url;
      a.target = "_blank";
      a.rel = "noopener noreferrer";
      a.className = "social-btn";
      a.textContent = soc.name;
      socialLinksEl.appendChild(a);
    });

    // Render Kategori
    function renderCategories() {
      categoriesGrid.innerHTML = "";
      SITE_CONFIG.categories.forEach(cat => {
        const card = document.createElement("div");
        card.className = `category-card ${activeCategory === cat.name ? "active" : ""}`;
        card.innerHTML = `
          <span class="category-icon">${cat.icon}</span>
          <div class="category-name">${cat.name}</div>
        `;
        card.addEventListener("click", () => {
          activeCategory = activeCategory === cat.name ? "Semua" : cat.name;
          renderCategories();
          renderProducts();
          document.getElementById("produk").scrollIntoView({ behavior: "smooth" });
        });
        categoriesGrid.appendChild(card);
      });
    }

    // Render Produk
    function renderProducts() {
      const filtered = PRODUCTS_DATA.filter(item => {
        const matchCategory = activeCategory === "Semua" || item.category === activeCategory;
        const matchTab = activeTab === "Semua" || item.label === activeTab;
        const q = searchQuery.toLowerCase();
        const matchSearch =
          item.name.toLowerCase().includes(q) ||
          item.description.toLowerCase().includes(q) ||
          item.category.toLowerCase().includes(q);
        return matchCategory && matchTab && matchSearch;
      });

      productSectionTitle.textContent =
        activeCategory !== "Semua"
          ? `Kategori: ${activeCategory}`
          : activeTab !== "Semua"
          ? `Produk ${activeTab}`
          : "Semua Produk Pilihan";

      productCountInfo.textContent = `Menampilkan ${filtered.length} produk terbaik`;

      productsGrid.innerHTML = "";

      if (filtered.length === 0) {
        productsGrid.innerHTML = `
          <div class="empty-state">
            <h3>Produk tidak ditemukan</h3>
            <p>Coba gunakan kata kunci lain atau pilih kategori lainnya.</p>
          </div>
        `;
        return;
      }

      filtered.forEach(product => {
        const badgeClass =
          product.label === "Terlaris"
            ? "terlaris"
            : product.label === "Terbaru"
            ? "terbaru"
            : "";

        const card = document.createElement("div");
        card.className = "product-card";
        card.innerHTML = `
          <div class="product-img-wrap">
            <img src="${product.image}" alt="${product.name}" loading="lazy" />
            <span class="product-badge ${badgeClass}">${product.label}</span>
          </div>
          <div class="product-body">
            <div class="product-cat">${product.category}</div>
            <h3 class="product-title">${product.name}</h3>
            <p class="product-desc">${product.description}</p>
            <div class="product-price">${product.price}</div>
            <div class="product-actions">
              <a href="${product.shopeeUrl}" target="_blank" rel="noopener noreferrer" class="btn-buy shopee">BELI DI SHOPEE</a>
              <a href="${product.tiktokUrl}" target="_blank" rel="noopener noreferrer" class="btn-buy tiktok">BELI DI TIKTOK SHOP</a>
            </div>
          </div>
        `;
        productsGrid.appendChild(card);
      });
    }

    // Event Pencarian
    searchInput.addEventListener("input", e => {
      searchQuery = e.target.value;
      renderProducts();
    });

    // Event Tab Filter (Semua, Rekomendasi, Terlaris, Terbaru)
    document.querySelectorAll(".sort-tabs .tab-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        document.querySelectorAll(".sort-tabs .tab-btn").forEach(b => b.classList.remove("active"));
        btn.classList.add("active");
        activeTab = btn.dataset.tab;
        renderProducts();
      });
    });

    // Reset Kategori
    document.getElementById("resetCategoryBtn").addEventListener("click", () => {
      activeCategory = "Semua";
      renderCategories();
      renderProducts();
    });

    // Tombol Menu Navigasi (termasuk filter Produk Terbaru & Terlaris)
    document.querySelectorAll("nav a[data-filter]").forEach(link => {
      link.addEventListener("click", () => {
        const filterVal = link.dataset.filter;
        activeTab = filterVal;
        document.querySelectorAll(".sort-tabs .tab-btn").forEach(b => {
          b.classList.toggle("active", b.dataset.tab === filterVal);
        });
        renderProducts();
      });
    });

    // Toggle Menu Mobile
    const menuToggle = document.getElementById("menuToggle");
    const mainNav = document.getElementById("mainNav");
    menuToggle.addEventListener("click", () => {
      mainNav.classList.toggle("open");
    });

    document.querySelectorAll("nav a").forEach(a => {
      a.addEventListener("click", () => {
        mainNav.classList.remove("open");
      });
    });

    // Jalankan Render Awal
    renderCategories();
    renderProducts();
  </script>
</body>
</html>
