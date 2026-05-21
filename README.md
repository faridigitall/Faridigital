# Faridigital
<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Farid Shirinov — Digital Marketoloq</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --gold: #C8963E;
    --gold-light: #F5E6C8;
    --gold-dark: #8A6520;
    --ink: #0F0E0C;
    --ink-mid: #3A3630;
    --ink-soft: #7A746A;
    --cream: #FAF7F2;
    --cream-dark: #F0EBE0;
    --white: #FFFFFF;
    --border: rgba(200,150,62,0.2);
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1.25rem 5%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(250,247,242,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .logo {
    font-family: 'DM Serif Display', serif;
    font-size: 1.25rem;
    color: var(--ink);
    letter-spacing: -0.02em;
  }

  .logo span { color: var(--gold); }

  nav ul {
    list-style: none;
    display: flex;
    gap: 2.5rem;
  }

  nav a {
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 400;
    color: var(--ink-soft);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    transition: color 0.2s;
  }

  nav a:hover { color: var(--gold); }

  .nav-cta {
    background: var(--ink) !important;
    color: var(--cream) !important;
    padding: 0.6rem 1.4rem;
    border-radius: 2rem;
    font-size: 0.82rem !important;
    transition: background 0.2s !important;
  }

  .nav-cta:hover { background: var(--gold) !important; }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 8rem 5% 4rem;
    position: relative;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute;
    top: -10%;
    right: -5%;
    width: 55%;
    height: 120%;
    background: linear-gradient(135deg, var(--gold-light) 0%, var(--cream-dark) 100%);
    border-radius: 40% 0 0 60%;
    z-index: 0;
  }

  .hero-content {
    position: relative;
    z-index: 1;
    max-width: 560px;
  }

  .hero-tag {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold-dark);
    background: var(--gold-light);
    border: 1px solid var(--gold);
    padding: 0.4rem 1rem;
    border-radius: 2rem;
    margin-bottom: 2rem;
  }

  .hero-tag::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--gold);
    border-radius: 50%;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(3rem, 6vw, 5rem);
    line-height: 1.05;
    letter-spacing: -0.03em;
    color: var(--ink);
    margin-bottom: 1.5rem;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold);
  }

  .hero p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: var(--ink-soft);
    margin-bottom: 2.5rem;
    max-width: 440px;
  }

  .hero-actions {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn-primary {
    background: var(--ink);
    color: var(--cream);
    padding: 0.9rem 2.2rem;
    border-radius: 3rem;
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }

  .btn-primary:hover { background: var(--gold); transform: translateY(-2px); }

  .btn-outline {
    border: 1.5px solid var(--ink);
    color: var(--ink);
    padding: 0.9rem 2.2rem;
    border-radius: 3rem;
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    transition: all 0.2s;
    display: inline-block;
  }

  .btn-outline:hover { border-color: var(--gold); color: var(--gold); transform: translateY(-2px); }

  .hero-stats {
    position: relative;
    z-index: 1;
    margin-left: auto;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding-right: 5%;
  }

  .stat-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.5rem 2rem;
    min-width: 180px;
    box-shadow: 0 4px 24px rgba(15,14,12,0.06);
  }

  .stat-card .num {
    font-family: 'DM Serif Display', serif;
    font-size: 2.5rem;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 0.3rem;
  }

  .stat-card .label {
    font-size: 0.82rem;
    color: var(--ink-soft);
    text-transform: uppercase;
    letter-spacing: 0.06em;
  }

  /* SERVICES */
  .services {
    padding: 7rem 5%;
    background: var(--white);
  }

  .section-header {
    text-align: center;
    margin-bottom: 4rem;
  }

  .section-tag {
    display: inline-block;
    font-size: 0.75rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold-dark);
    margin-bottom: 1rem;
  }

  .section-header h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    letter-spacing: -0.025em;
    color: var(--ink);
    margin-bottom: 1rem;
  }

  .section-header p {
    color: var(--ink-soft);
    font-size: 1rem;
    max-width: 480px;
    margin: 0 auto;
    line-height: 1.7;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
    max-width: 1100px;
    margin: 0 auto;
  }

  .service-card {
    background: var(--cream);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 2.2rem;
    transition: transform 0.2s, box-shadow 0.2s;
    position: relative;
    overflow: hidden;
  }

  .service-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    background: var(--gold);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }

  .service-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(15,14,12,0.09); }
  .service-card:hover::after { transform: scaleX(1); }

  .service-icon {
    width: 52px; height: 52px;
    background: var(--gold-light);
    border-radius: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .service-card h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.3rem;
    color: var(--ink);
    margin-bottom: 0.75rem;
    letter-spacing: -0.01em;
  }

  .service-card p {
    font-size: 0.9rem;
    color: var(--ink-soft);
    line-height: 1.65;
  }

  /* RESULTS */
  .results {
    padding: 7rem 5%;
    background: var(--ink);
    color: var(--cream);
  }

  .results .section-tag { color: var(--gold); }
  .results h2 { color: var(--cream); }
  .results .section-header p { color: rgba(250,247,242,0.6); }

  .results-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.5rem;
    max-width: 900px;
    margin: 0 auto;
  }

  .result-card {
    border: 1px solid rgba(200,150,62,0.3);
    border-radius: 20px;
    padding: 2rem;
    text-align: center;
  }

  .result-card .big {
    font-family: 'DM Serif Display', serif;
    font-size: 3.5rem;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 0.5rem;
  }

  .result-card p {
    font-size: 0.88rem;
    color: rgba(250,247,242,0.65);
    line-height: 1.5;
  }

  /* PORTFOLIO */
  .portfolio {
    padding: 7rem 5%;
    background: var(--cream);
  }

  .portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1100px;
    margin: 0 auto;
  }

  .portfolio-card {
    border-radius: 20px;
    overflow: hidden;
    background: var(--white);
    border: 1px solid var(--border);
    transition: transform 0.2s, box-shadow 0.2s;
  }

  .portfolio-card:hover { transform: translateY(-4px); box-shadow: 0 16px 48px rgba(15,14,12,0.1); }

  .portfolio-img {
    height: 180px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
    position: relative;
  }

  .portfolio-img.bg1 { background: #1a1a2e; }
  .portfolio-img.bg2 { background: #16213e; }
  .portfolio-img.bg3 { background: #0f3460; }

  .portfolio-body { padding: 1.5rem; }

  .portfolio-tag {
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold-dark);
    background: var(--gold-light);
    padding: 0.25rem 0.7rem;
    border-radius: 2rem;
    display: inline-block;
    margin-bottom: 0.8rem;
  }

  .portfolio-card h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.2rem;
    color: var(--ink);
    margin-bottom: 0.5rem;
    letter-spacing: -0.01em;
  }

  .portfolio-card p {
    font-size: 0.88rem;
    color: var(--ink-soft);
    line-height: 1.6;
    margin-bottom: 1rem;
  }

  .portfolio-metric {
    display: flex;
    gap: 1rem;
  }

  .metric {
    font-size: 0.82rem;
    color: var(--gold-dark);
    font-weight: 500;
  }

  /* TESTIMONIALS */
  .testimonials {
    padding: 7rem 5%;
    background: var(--white);
  }

  .testimonials-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1000px;
    margin: 0 auto;
  }

  .testimonial-card {
    background: var(--cream);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 2rem;
  }

  .stars {
    color: var(--gold);
    font-size: 1rem;
    margin-bottom: 1rem;
    letter-spacing: 2px;
  }

  .testimonial-card blockquote {
    font-size: 0.95rem;
    color: var(--ink-mid);
    line-height: 1.7;
    margin-bottom: 1.5rem;
    font-style: italic;
  }

  .testimonial-author {
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .avatar {
    width: 42px; height: 42px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--white);
  }

  .testimonial-author .name {
    font-weight: 500;
    font-size: 0.9rem;
    color: var(--ink);
  }

  .testimonial-author .role {
    font-size: 0.78rem;
    color: var(--ink-soft);
  }

  /* CONTACT */
  .contact {
    padding: 7rem 5%;
    background: var(--ink);
    text-align: center;
  }

  .contact h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3.5rem);
    color: var(--cream);
    letter-spacing: -0.03em;
    margin-bottom: 1rem;
  }

  .contact h2 em { color: var(--gold); font-style: italic; }

  .contact p {
    color: rgba(250,247,242,0.6);
    font-size: 1rem;
    margin-bottom: 2.5rem;
    line-height: 1.7;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 1.2rem;
    flex-wrap: wrap;
    margin-bottom: 3rem;
  }

  .contact-links a {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    text-decoration: none;
    font-size: 0.88rem;
    color: rgba(250,247,242,0.8);
    border: 1px solid rgba(200,150,62,0.3);
    padding: 0.75rem 1.5rem;
    border-radius: 3rem;
    transition: all 0.2s;
  }

  .contact-links a:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  .contact-cta {
    background: var(--gold);
    color: var(--ink);
    padding: 1rem 3rem;
    border-radius: 3rem;
    text-decoration: none;
    font-size: 1rem;
    font-weight: 500;
    display: inline-block;
    transition: transform 0.2s, background 0.2s;
  }

  .contact-cta:hover { transform: translateY(-2px); background: #E8AE4E; }

  /* FOOTER */
  footer {
    background: #0A0908;
    color: rgba(250,247,242,0.4);
    text-align: center;
    padding: 2rem 5%;
    font-size: 0.82rem;
  }

  footer span { color: var(--gold); }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-content > * {
    animation: fadeUp 0.7s ease both;
  }

  .hero-content > *:nth-child(1) { animation-delay: 0.1s; }
  .hero-content > *:nth-child(2) { animation-delay: 0.2s; }
  .hero-content > *:nth-child(3) { animation-delay: 0.35s; }
  .hero-content > *:nth-child(4) { animation-delay: 0.5s; }

  .hero-stats {
    animation: fadeUp 0.8s 0.4s ease both;
  }

  @media (max-width: 768px) {
    .hero { flex-direction: column; gap: 3rem; }
    .hero-stats { flex-direction: row; flex-wrap: wrap; margin-left: 0; padding-right: 0; }
    .hero-bg { width: 100%; height: 50%; top: 50%; right: 0; border-radius: 0; }
    nav ul { display: none; }
  }
</style>
</head>
<body>

<nav>
  <div class="logo">Farid<span>.</span>Shirinov</div>
  <ul>
    <li><a href="#xidmetler">Xidmətlər</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#haqqimda">Haqqımda</a></li>
    <li><a href="#elaqe" class="nav-cta">Əlaqə</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>

  <div class="hero-content">
    <div class="hero-tag">Digital Marketoloq & Brendinq Eksperti</div>
    <h1>Brendinizi<br><em>rəqəmsal</em><br>dünyada ucaldın</h1>
    <p>Azərbaycan və beynəlxalq bazarlarda SEO, sosial media, ödənişli reklamlar və brendinq strategiyası ilə biznesinizi böyüdürəm.</p>
    <div class="hero-actions">
      <a href="#elaqe" class="btn-primary">Əməkdaşlığa başlayaq</a>
      <a href="#portfolio" class="btn-outline">İşlərimi gör</a>
    </div>
  </div>

  <div class="hero-stats">
    <div class="stat-card">
      <div class="num">85+</div>
      <div class="label">Tamamlanmış<br>layihə</div>
    </div>
    <div class="stat-card">
      <div class="num">5x</div>
      <div class="label">Ortalama<br>ROI artımı</div>
    </div>
    <div class="stat-card">
      <div class="num">6 il</div>
      <div class="label">Sahə<br>təcrübəsi</div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="xidmetler">
  <div class="section-header">
    <div class="section-tag">— Xidmətlər</div>
    <h2>Nə təklif edirəm?</h2>
    <p>Biznesinizin onlayn görünürlüğünü artırmaq üçün hərtərəfli rəqəmsal marketinq həlləri.</p>
  </div>

  <div class="services-grid">
    <div class="service-card">
      <div class="service-icon">🔍</div>
      <h3>SEO Optimallaşdırma</h3>
      <p>Google-da ilk sıralara çıxmaq üçün texniki SEO, məzmun strategiyası və keykəlimə tədqiqatı ilə saytınızı optimizasiya edirəm.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📱</div>
      <h3>Sosial Media İdarəsi</h3>
      <p>Instagram, Facebook, LinkedIn — hər platforma üçün xüsusi məzmun strategiyası, icma idarəçiliyi və rəqib analizi.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🎯</div>
      <h3>Ödənişli Reklamlar (PPC)</h3>
      <p>Google Ads, Meta Ads, TikTok Ads — büdcənizi ən yüksək ROI ilə idarə edən kampaniyalar qururam.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">✉️</div>
      <h3>E-poçt Marketinqi</h3>
      <p>Avtomatik e-poçt axınları, A/B testlər və şəxsiləşdirilmiş kampaniyalarla müştəri saxlama nisbətini artırın.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📊</div>
      <h3>Analitika & Hesabat</h3>
      <p>GA4, Hotjar, SEMrush kimi alətlər vasitəsilə dərin data analizi və aylıq performans hesabatları.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">💡</div>
      <h3>Brendinq Strategiyası</h3>
      <p>Brendinizin sesini, tonunu, vizual kimliyini və bazar mövqeləndirməsini birlikdə formalaşdırırıq.</p>
    </div>
  </div>
</section>

<!-- RESULTS -->
<section class="results" id="haqqimda">
  <div class="section-header">
    <div class="section-tag">— Nəticələr</div>
    <h2 style="color:#FAF7F2">Rəqəmlərlə danışır</h2>
    <p>Müştərilərimizin bizneslərinə gətirdiyimiz ölçülə bilən dəyişikliklər.</p>
  </div>

  <div class="results-grid">
    <div class="result-card">
      <div class="big">320%</div>
      <p>Ortalama üzvi trafik artımı ilk 6 ay ərzində</p>
    </div>
    <div class="result-card">
      <div class="big">4.8×</div>
      <p>Reklam xərclərindən gəlir nisbəti (ROAS)</p>
    </div>
    <div class="result-card">
      <div class="big">60%</div>
      <p>Sosial media izləyici artımı ortalama</p>
    </div>
    <div class="result-card">
      <div class="big">92%</div>
      <p>Müştəri məmnuniyyəti skoru</p>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section class="portfolio" id="portfolio">
  <div class="section-header">
    <div class="section-tag">— Portfolio</div>
    <h2>Seçilmiş işlər</h2>
    <p>Müxtəlif sahələrdə tamamladığım uğurlu layihələrdən bir seçki.</p>
  </div>

  <div class="portfolio-grid">
    <div class="portfolio-card">
      <div class="portfolio-img bg1">🛍️</div>
      <div class="portfolio-body">
        <div class="portfolio-tag">E-ticarət</div>
        <h3>Moda Brendinin Böyüməsi</h3>
        <p>Azərbaycan moda brendinin Meta Ads və SEO kampaniyası ilə 8 ayda satışları 4x artırdıq.</p>
        <div class="portfolio-metric">
          <span class="metric">+420% satış</span>
          <span class="metric">ROAS: 5.2x</span>
        </div>
      </div>
    </div>

    <div class="portfolio-card">
      <div class="portfolio-img bg2">🏥</div>
      <div class="portfolio-body">
        <div class="portfolio-tag">Sağlamlıq</div>
        <h3>Klinika Rəqəmsal Transformasiyası</h3>
        <p>Xüsusi tibb klinikası üçün Google Ads və SEO ilə aylıq müraciətləri 3x artırdıq.</p>
        <div class="portfolio-metric">
          <span class="metric">+280% müraciət</span>
          <span class="metric">CPC -40%</span>
        </div>
      </div>
    </div>

    <div class="portfolio-card">
      <div class="portfolio-img bg3">🏠</div>
      <div class="portfolio-body">
        <div class="portfolio-tag">Daşınmaz Əmlak</div>
        <h3>Əmlak Agentliyinin Brendinqi</h3>
        <p>Sosial media idarəsi və məzmun marketinqi ilə brend fərqindəliyi 6 ayda 200% artdı.</p>
        <div class="portfolio-metric">
          <span class="metric">+200% fərqindəlik</span>
          <span class="metric">12K yeni izləyici</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="testimonials">
  <div class="section-header">
    <div class="section-tag">— Rəylər</div>
    <h2>Müştərilər nə deyir?</h2>
    <p>Birlikdə çalışdığımız müştərilər öz təcrübələrini bölüşürlər.</p>
  </div>

  <div class="testimonials-grid">
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <blockquote>"Anar ilə işləmək biznesimizi tamamilə dəyişdirdi. SEO kampaniyası sayəsində Google-da ilk sıraları tutduq və satışlarımız rekord qırdı."</blockquote>
      <div class="testimonial-author">
        <div class="avatar" style="background: #C8963E;">NK</div>
        <div>
          <div class="name">Nərmin Kərimova</div>
          <div class="role">CEO, StyleAZ</div>
        </div>
      </div>
    </div>

    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <blockquote>"Reklam büdcəmizi 3x azaldıb eyni zamanda müraciətlərimizi 2.5x artırdı. Peşəkar yanaşma, şəffaf hesabatlar — tövsiyə edirəm!"</blockquote>
      <div class="testimonial-author">
        <div class="avatar" style="background: #3A8A6E;">RA</div>
        <div>
          <div class="name">Rauf Abdullayev</div>
          <div class="role">Həkim-Direktor, MedCenter</div>
        </div>
      </div>
    </div>

    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <blockquote>"Instagram hesabımız 2 000-dən 45 000 izləyiciyə çatdı. Məzmun keyfiyyəti, strategiya və nəticələr — hamısı üstün səviyyəlidir."</blockquote>
      <div class="testimonial-author">
        <div class="avatar" style="background: #5A6DB0;">EH</div>
        <div>
          <div class="name">Elçin Həsənli</div>
          <div class="role">Kurucu, EmlakPro</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="elaqe">
  <div class="section-tag">— Əlaqə</div>
  <h2>Layihənizi<br><em>birgə</em> böyüdək</h2>
  <p>Məqsədlərinizi, büdcənizi və gözləntilərinizi müzakirə etmək üçün<br>pulsuz məsləhət sessiyası üçün əlaqə saxlayın.</p>

  <div class="contact-links">
    <a href="mailto:farid@example.az">📧 farid@example.az</a>
    <a href="tel:+994501234567">📞 +994 50 123 45 67</a>
    <a href="#">💼 LinkedIn</a>
    <a href="#">📸 Instagram</a>
  </div>

  <a href="mailto:farid@example.az" class="contact-cta">Pulsuz məsləhət al →</a>
</section>

<footer>
  <p>© 2024 Farid Shirinov. Bütün hüquqlar qorunur. Bakı, <span>Azərbaycan</span></p>
</footer>

</body>
</html>
