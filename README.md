<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>PiKIR | Praktisi Kewirausahaan Inovasi Riset</title>
    <meta
      name="description"
      content="PiKIR adalah organisasi yang bergerak di bidang kewirausahaan, inovasi, dan riset untuk menciptakan solusi nyata bagi masyarakat."
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <style>
      :root {
        --brand-blue: #0e2245;
        --brand-blue-2: #16375a;
        --brand-gold: #f3c54c;
        --brand-gold-2: #dca81f;
        --brand-cream: #fffaf1;
        --brand-cream-2: #fff3d4;
        --text: #1a2437;
        --muted: #58677b;
        --border: #e9dfbe;
        --shadow: 0 18px 40px rgba(14, 31, 58, 0.12);
      }

      * { box-sizing: border-box; }
      html { scroll-behavior: smooth; }
      body {
        margin: 0;
        font-family: "Plus Jakarta Sans", sans-serif;
        background:
          radial-gradient(circle at top left, rgba(243, 197, 76, 0.14), transparent 26%),
          linear-gradient(180deg, #fffdf9 0%, #fffaf1 100%);
        color: var(--text);
      }

      a { color: inherit; text-decoration: none; }
      img { max-width: 100%; display: block; }

      .container {
        width: min(1120px, 92%);
        margin: 0 auto;
      }

      .header {
        position: sticky;
        top: 0;
        z-index: 1000;
        background: rgba(255, 250, 241, 0.86);
        backdrop-filter: blur(10px);
        border-bottom: 1px solid rgba(14, 34, 69, 0.08);
      }

      .navbar {
        display: flex;
        align-items: center;
        justify-content: space-between;
        min-height: 78px;
        gap: 20px;
      }

      .logo {
        display: flex;
        align-items: center;
        gap: 10px;
        min-height: 52px;
      }

      .logo-mark {
        width: 58px;
        height: 58px;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        overflow: hidden;
        flex-shrink: 0;
      }

      .logo-mark svg {
        width: 100%;
        height: 100%;
        display: block;
      }

      .logo-text {
        display: inline-flex;
        align-items: center;
        gap: 0;
        font-weight: 900;
        letter-spacing: -0.05em;
        font-size: clamp(1.5rem, 2vw, 2rem);
        line-height: 1;
      }

      .logo-text .pi,
      .logo-text .kir {
        color: var(--brand-blue);
      }

      .nav-menu {
        display: flex;
        align-items: center;
        gap: 22px;
      }

      .nav-menu a {
        color: var(--muted);
        font-size: 0.96rem;
        font-weight: 600;
      }

      .nav-menu a:hover { color: var(--brand-blue); }

      .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 0.92rem 1.5rem;
        border-radius: 14px;
        font-weight: 700;
        transition: transform 0.2s ease, box-shadow 0.2s ease;
      }

      .btn:hover { transform: translateY(-1px); }

      .btn-primary {
        background: linear-gradient(135deg, var(--brand-gold), var(--brand-gold-2));
        color: var(--brand-blue);
        box-shadow: 0 12px 26px rgba(220, 168, 31, 0.28);
      }

      .btn-secondary {
        background: #fff;
        color: var(--brand-blue);
        border: 1px solid rgba(14, 34, 69, 0.14);
      }

      .btn-light {
        background: #fff;
        color: var(--brand-blue);
        border: 1px solid rgba(255,255,255,0.2);
      }

      .hero {
        padding: 72px 0 44px;
      }

      .hero-content {
        display: grid;
        grid-template-columns: 1.1fr 0.9fr;
        align-items: center;
        gap: 40px;
      }

      .hero-copy h1 {
        margin: 0 0 18px;
        font-size: clamp(2.4rem, 4vw, 4.2rem);
        letter-spacing: -0.06em;
        line-height: 1.08;
        color: var(--text);
      }

      .eyebrow {
        display: inline-block;
        margin: 0 0 18px;
        padding: 8px 14px;
        border-radius: 999px;
        background: var(--brand-cream-2);
        color: var(--brand-blue);
        font-weight: 700;
        font-size: 0.76rem;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      .subtitle {
        margin: 0 0 28px;
        color: var(--muted);
        line-height: 1.8;
        font-size: 1.04rem;
        max-width: 640px;
      }

      .hero-actions {
        display: flex;
        flex-wrap: wrap;
        gap: 16px;
        margin-bottom: 28px;
      }

      .stats {
        display: flex;
        flex-wrap: wrap;
        gap: 28px;
        padding-top: 8px;
      }

      .stats div {
        min-width: 120px;
      }

      .stats strong {
        display: block;
        font-size: clamp(1.6rem, 2vw, 2.2rem);
        color: var(--brand-blue);
        margin-bottom: 8px;
      }

      .stats span {
        color: var(--muted);
        font-size: 0.9rem;
      }

      .hero-visual {
        position: relative;
        min-height: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .main-card {
        width: min(480px, 100%);
        background: linear-gradient(135deg, var(--brand-blue) 0%, var(--brand-blue-2) 100%);
        color: #fff;
        border-radius: 28px;
        padding: 32px 28px;
        box-shadow: 0 30px 60px rgba(14, 34, 69, 0.24);
        position: relative;
        z-index: 2;
      }

      .main-card::before {
        content: "";
        position: absolute;
        inset: -50px auto auto -40px;
        width: 160px;
        height: 160px;
        background: rgba(255,255,255,0.06);
        border-radius: 50%;
      }

      .badge {
        display: inline-flex;
        align-items: center;
        background: rgba(255,255,255,0.12);
        border: 1px solid rgba(255,255,255,0.12);
        color: #fff;
        padding: 8px 12px;
        border-radius: 999px;
        font-size: 0.72rem;
        font-weight: 700;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      .main-card h3 {
        margin: 22px 0 18px;
        font-size: clamp(1.5rem, 2vw, 2rem);
        line-height: 1.35;
        letter-spacing: -0.04em;
      }

      .main-card ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: grid;
        gap: 12px;
      }

      .main-card li {
        position: relative;
        padding-left: 26px;
        color: rgba(255,255,255,0.92);
        font-weight: 500;
      }

      .main-card li::before {
        content: "✓";
        position: absolute;
        left: 0;
        color: var(--brand-gold);
        font-weight: 800;
      }

      .floating-card {
        position: absolute;
        right: 10px;
        bottom: 30px;
        display: flex;
        align-items: center;
        gap: 14px;
        background: rgba(255,255,255,0.8);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(14,34,69,0.08);
        border-radius: 18px;
        box-shadow: var(--shadow);
        padding: 16px 18px;
        min-width: 200px;
        z-index: 3;
      }

      .floating-card .icon {
        width: 52px;
        height: 52px;
        border-radius: 14px;
        background: linear-gradient(135deg, #fff4d3, #f5d77c);
        display: grid;
        place-items: center;
        font-size: 1.5rem;
      }

      .floating-card strong {
        display: block;
        font-size: 1.5rem;
        color: var(--brand-blue);
        margin-bottom: 4px;
      }

      .floating-card p {
        margin: 0;
        color: var(--muted);
        font-size: 0.8rem;
        line-height: 1.4;
      }

      .section {
        padding: 88px 0;
      }

      .section.alt {
        background: rgba(243,197,76,0.04);
      }

      .section-heading {
        text-align: center;
        margin-bottom: 36px;
      }

      .section-heading h2 {
        margin: 0;
        font-size: clamp(2rem, 3vw, 2.7rem);
        letter-spacing: -0.05em;
        color: var(--text);
      }

      .about-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .about-card {
        background: rgba(255,255,255,0.96);
        border: 1px solid var(--border);
        border-radius: 22px;
        padding: 28px 24px;
        box-shadow: var(--shadow);
      }

      .about-card h3 {
        margin: 0 0 14px;
        font-size: 1.3rem;
        color: var(--brand-blue);
      }

      .about-card p {
        margin: 0;
        color: var(--muted);
        line-height: 1.8;
      }

      .program-grid {
        display: grid;
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 24px;
      }

      .program-card {
        background: #fff;
        border: 1px solid var(--border);
        border-radius: 22px;
        padding: 26px 20px;
        box-shadow: var(--shadow);
        transition: transform 0.2s ease, box-shadow 0.2s ease;
      }

      .program-card:hover {
        transform: translateY(-4px);
        box-shadow: 0 24px 42px rgba(14,34,69,0.12);
      }

      .icon-box {
        width: 58px;
        height: 58px;
        display: grid;
        place-items: center;
        background: linear-gradient(135deg, #fff4d3, #f5d77c);
        border-radius: 16px;
        font-size: 1.8rem;
        margin-bottom: 18px;
      }

      .program-card h3 {
        margin: 0 0 12px;
        font-size: 1.28rem;
      }

      .program-card p {
        margin: 0;
        color: var(--muted);
        line-height: 1.8;
      }

      .activity-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 26px;
      }

      .activity-item {
        background: #fff;
        border: 1px solid var(--border);
        border-radius: 24px;
        overflow: hidden;
        box-shadow: var(--shadow);
      }

      .activity-image {
        height: 220px;
        background-size: cover;
        background-position: center;
      }

      .image-one {
        background-image: url("https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=1200&q=80");
      }
      .image-two {
        background-image: url("https://images.unsplash.com/photo-1517048676732-d65bc937f952?auto=format&fit=crop&w=1200&q=80");
      }
      .image-three {
        background-image: url("https://images.unsplash.com/photo-1532012197267-da84d127e765?auto=format&fit=crop&w=1200&q=80");
      }
      .image-four {
        background-image: url("https://images.unsplash.com/photo-1523240795612-9a054b0db644?auto=format&fit=crop&w=1200&q=80");
      }
      .image-five {
        background-image: url("https://images.unsplash.com/photo-1552664730-d307ca884978?auto=format&fit=crop&w=1200&q=80");
      }
      .image-six {
        background-image: url("https://images.unsplash.com/photo-1497633762265-9d179a990aa6?auto=format&fit=crop&w=1200&q=80");
      }

      .activity-content {
        padding: 22px 20px 26px;
      }

      .tag {
        display: inline-block;
        background: #fff4d3;
        color: var(--brand-blue);
        border-radius: 999px;
        padding: 7px 10px;
        font-size: 0.72rem;
        font-weight: 700;
        letter-spacing: 0.05em;
        text-transform: uppercase;
        margin-bottom: 12px;
      }

      .activity-content h3 {
        margin: 0 0 10px;
        font-size: 1.25rem;
      }

      .activity-content p {
        margin: 0;
        color: var(--muted);
        line-height: 1.8;
      }

      .portfolio-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .portfolio-card {
        background: linear-gradient(135deg, #fffdf8 0%, #fff5d9 100%);
        border: 1px solid var(--border);
        border-radius: 24px;
        padding: 26px 22px;
        box-shadow: var(--shadow);
      }

      .portfolio-badge {
        display: inline-block;
        background: #fff1b0;
        color: var(--brand-blue);
        padding: 8px 12px;
        border-radius: 999px;
        font-size: 0.72rem;
        font-weight: 700;
        letter-spacing: 0.06em;
        text-transform: uppercase;
        margin-bottom: 18px;
      }

      .portfolio-card h3 {
        margin: 0 0 14px;
        font-size: 1.28rem;
        line-height: 1.4;
      }

      .portfolio-card p {
        margin: 0;
        color: var(--muted);
        line-height: 1.8;
      }

      .team-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .team-card {
        background: #fff;
        border: 1px solid var(--border);
        border-radius: 24px;
        padding: 20px;
        text-align: center;
        box-shadow: var(--shadow);
      }

      .avatar {
        width: 130px;
        height: 130px;
        margin: 0 auto 18px;
        border-radius: 50%;
        background-size: cover;
        background-position: center;
        border: 4px solid #fdf1c8;
      }

      .avatar-one {
        background-image: url("https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=800&q=80");
      }
      .avatar-two {
        background-image: url("https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&w=800&q=80");
      }
      .avatar-three {
        background-image: url("https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?auto=format&fit=crop&w=800&q=80");
      }

      .team-card h3 {
        margin: 0 0 6px;
        font-size: 1.2rem;
      }

      .team-card p {
        margin: 0;
        color: var(--muted);
        font-weight: 600;
      }

      .cta {
        padding: 30px 0 70px;
      }

      .cta-box {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 24px;
        background: linear-gradient(135deg, var(--brand-blue) 0%, var(--brand-blue-2) 100%);
        color: #fff;
        border-radius: 28px;
        padding: 32px 36px;
        box-shadow: 0 28px 50px rgba(14, 34, 69, 0.25);
      }

      .cta-box h2 {
        margin: 0;
        font-size: clamp(1.8rem, 3vw, 2.5rem);
        letter-spacing: -0.05em;
      }

      .footer {
        background: #0d1d36;
        color: rgba(255,255,255,0.8);
        padding-top: 30px;
      }

      .footer-grid {
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr;
        gap: 30px;
        padding-bottom: 25px;
      }

      .footer-logo {
        margin-bottom: 14px;
        color: white;
      }

      .footer p, .footer li, .footer a {
        color: rgba(255,255,255,0.78);
      }

      .footer h4 {
        margin-top: 0;
        margin-bottom: 16px;
        color: #fff;
      }

      .footer ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: grid;
        gap: 10px;
      }

      .copyright {
        border-top: 1px solid rgba(255,255,255,0.08);
        padding: 14px 0 22px;
        text-align: center;
      }

      @media (max-width: 980px) {
        .hero-content,
        .about-grid,
        .program-grid,
        .activity-grid,
        .portfolio-grid,
        .team-grid,
        .footer-grid,
        .cta-box {
          display: grid;
          grid-template-columns: 1fr;
        }
        .nav-menu {
          display: none;
        }
      }

      @media (max-width: 620px) {
        .hero {
          padding-top: 52px;
        }

        .hero-actions {
          flex-direction: column;
          align-items: stretch;
        }

        .btn {
          width: 100%;
        }

        .stats {
          gap: 18px;
        }
      }
    </style>
  </head>
  <body>
    <header class="header">
      <nav class="navbar container">
        <div class="logo">
          <div class="logo-mark" aria-label="PiKIR logo">
            <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="PiKIR">
              <defs>
                <path id="ringTextPath" d="M 100,100 m -72,0 a 72,72 0 1,1 144,0 a 72,72 0 1,1 -144,0" />
              </defs>

              <circle cx="100" cy="100" r="82" fill="#0e2245" />
              <circle cx="100" cy="100" r="74" fill="#f5d24a" stroke="#0e2245" stroke-width="4" />

              <g fill="#0e2245">
                <circle cx="100" cy="18" r="4.5" />
                <circle cx="100" cy="182" r="4.5" />
                <circle cx="18" cy="100" r="4.5" />
                <circle cx="182" cy="100" r="4.5" />
                <circle cx="36" cy="36" r="4.5" />
                <circle cx="164" cy="36" r="4.5" />
                <circle cx="36" cy="164" r="4.5" />
                <circle cx="164" cy="164" r="4.5" />
                <circle cx="26" cy="63" r="4.5" />
                <circle cx="174" cy="63" r="4.5" />
                <circle cx="26" cy="137" r="4.5" />
                <circle cx="174" cy="137" r="4.5" />
              </g>

              <text
                fill="#0e2245"
                font-size="9.5"
                font-weight="800"
                letter-spacing="2"
                font-family="Verdana, sans-serif">
                <textPath href="#ringTextPath" startOffset="50%" text-anchor="middle">
                  PRAKTISI KEWIRAUSAHAAN INOVASI RISET
                </textPath>
              </text>

              <circle cx="100" cy="100" r="48" fill="#fffaf0" stroke="#0e2245" stroke-width="4" />

              <path
                d="M72 66 V136 H82 V100 H114 C126 100 133 94 133 84 C133 72 126 66 114 66 H72 Z
                   M82 76 H111 C118 76 122 79 122 84 C122 89 118 92 111 92 H82 V76 Z"
                fill="#0e2245"
              />
              <circle cx="100" cy="100" r="5" fill="#f5d24a" />

              <text
                x="100"
                y="156"
                text-anchor="middle"
                font-size="26"
                font-family="Verdana, sans-serif"
                font-weight="900"
                fill="#0e2245">
                KIR
              </text>
            </svg>
          </div>

          <div class="logo-text">
            <span class="pi">Pi</span><span class="kir">KIR</span>
          </div>
        </div>

        <div class="nav-menu">
          <a href="#beranda">Beranda</a>
          <a href="#tentang">Tentang</a>
          <a href="#program">Program</a>
          <a href="#kegiatan">Kegiatan</a>
          <a href="#portfolio">Portofolio</a>
          <a href="#tim">Pembina</a>
          <a href="#kontak">Kontak</a>
          <a href="#kontak" class="btn btn-primary nav-cta">Kolaborasi</a>
        </div>
      </nav>
    </header>

    <main>
      <section id="beranda" class="hero">
        <div class="container hero-content">
          <div class="hero-copy">
            <p class="eyebrow">Praktisi Kewirausahaan Inovasi Riset</p>
            <h1>Menghubungkan riset, inovasi, dan kewirausahaan untuk perubahan nyata.</h1>
            <p class="subtitle">
              PiKIR hadir sebagai wadah bagi para praktisi, akademisi, dan pelaku
              inovasi untuk mengembangkan ide, membangun solusi berbasis riset,
              serta mendorong ekosistem kewirausahaan yang berdampak.
            </p>

            <div class="hero-actions">
              <a href="#kontak" class="btn btn-primary">Bergabung</a>
              <a href="#program" class="btn btn-secondary">Lihat Program</a>
            </div>

            <div class="stats">
              <div>
                <strong>14th</strong>
                <span>tahun pengalaman</span>
              </div>
              <div>
                <strong>40+</strong>
                <span>program inovasi</span>
              </div>
              <div>
                <strong>2000+</strong>
                <span>pelaku terlibat</span>
              </div>
            </div>
          </div>

          <div class="hero-visual">
            <div class="main-card">
              <div class="badge">Research to Venture</div>
              <h3>Inovasi yang lahir dari riset dan siap diimplementasikan.</h3>
              <ul>
                <li>Riset kebutuhan masyarakat</li>
                <li>Pengembangan solusi inovatif</li>
                <li>Inkubasi kewirausahaan</li>
              </ul>
            </div>

            <div class="floating-card">
              <div class="icon">📈</div>
              <div>
                <strong>85%</strong>
                <p>inovasi siap dikembangkan</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="tentang" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Tentang PiKIR</p>
            <h2>Memberdayakan ide menjadi solusi yang berdampak.</h2>
          </div>

          <div class="about-grid">
            <div class="about-card">
              <h3>Visi</h3>
              <p>
                Menjadi pelopor ekosistem inovasi riset dan kewirausahaan yang
                mendorong kualitas hidup masyarakat melalui solusi nyata.
              </p>
            </div>
            <div class="about-card">
              <h3>Misi</h3>
              <p>
                Mengembangkan kemampuan riset, membangun inovasi yang aplikatif,
                dan mendorong kemandirian usaha berbasis pengetahuan.
              </p>
            </div>
            <div class="about-card">
              <h3>Nilai</h3>
              <p>
                Kreativitas, kolaborasi, integritas, dan kebermanfaatan menjadi
                fondasi utama dalam setiap langkah PiKIR.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="program" class="section alt">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Program</p>
            <h2>Lintasan pengembangan inovasi dan kewirausahaan.</h2>
          </div>

          <div class="program-grid">
            <article class="program-card">
              <div class="icon-box">🔬</div>
              <h3>Riset & Analisis</h3>
              <p>
                Mengidentifikasi kebutuhan nyata dan membangun dasar data untuk
                solusi inovatif yang relevan.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">💡</div>
              <h3>Inovasi</h3>
              <p>
                Mengembangkan konsep, prototipe, dan model solusi baru yang
                teruji dan aplikatif.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">🚀</div>
              <h3>Inkubasi Kewirausahaan</h3>
              <p>
                Menyediakan pendampingan, strategi bisnis, dan jaringan
                pengembangan usaha berbasis inovasi.
              </p>
            </article>

            <article class="program-card">
              <div class="icon-box">🤝</div>
              <h3>Kolaborasi</h3>
              <p>
                Menjalin kemitraan dengan berbagai pihak untuk memperluas
                dampak dan akses terhadap inovasi.
              </p>
            </article>
          </div>
        </div>
      </section>

      <section id="kegiatan" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Kegiatan</p>
            <h2>Aktivitas yang mendorong ide berkembang menjadi solusi.</h2>
          </div>

          <div class="activity-grid">
            <div class="activity-item">
              <div class="activity-image image-one"></div>
              <div class="activity-content">
                <span class="tag">Informasi</span>
                <h3>Info PiKIR Day</h3>
                <p>
                  Serangkaian sosialisasi, pengenalan program, dan informasi
                  penting seputar inovasi, riset, serta peluang kewirausahaan
                  bagi siswa dan komunitas.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-two"></div>
              <div class="activity-content">
                <span class="tag">Festival</span>
                <h3>FIKSA (Festival Kewirausahaan SMASA)</h3>
                <p>
                  Festival kewirausahaan yang menampilkan ide kreatif, bisnis
                  inovatif, serta semangat berwirausaha siswa SMA/SMK dalam
                  wadah yang inspiratif dan kompetitif.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-three"></div>
              <div class="activity-content">
                <span class="tag">Eksperimen</span>
                <h3>Roket Air</h3>
                <p>
                  Kegiatan eksperimen dan kreativitas siswa yang menggabungkan
                  konsep sains, teknik, dan inovasi melalui pembuatan roket air
                  yang menarik dan edukatif.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-four"></div>
              <div class="activity-content">
                <span class="tag">Pengajaran</span>
                <h3>PiJAR (PiKIR Mengajar)</h3>
                <p>
                  Program berbagi ilmu dan pendampingan belajar melalui kegiatan
                  mengajar, pembinaan, serta transfer pengetahuan untuk membangun
                  karakter dan kemampuan siswa.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-five"></div>
              <div class="activity-content">
                <span class="tag">Kunjungan</span>
                <h3>Studi Visit</h3>
                <p>
                  Kegiatan kunjungan belajar ke berbagai instansi, lembaga, atau
                  komunitas untuk menambah wawasan, inspirasi, dan jaringan
                  kolaborasi.
                </p>
              </div>
            </div>

            <div class="activity-item">
              <div class="activity-image image-six"></div>
              <div class="activity-content">
                <span class="tag">Riset</span>
                <h3>Penamaan Ilmiah</h3>
                <p>
                  Kegiatan yang menumbuhkan kreativitas siswa dalam mengembangkan
                  ide-ide ilmiah, inovatif, dan aplikatif melalui proses penamaan
                  produk, karya, atau inovasi dengan pendekatan yang terarah dan
                  edukatif.
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="portfolio" class="section alt">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Portofolio</p>
            <h2>Proyek yang menunjukkan dampak nyata PiKIR.</h2>
          </div>

          <div class="portfolio-grid">
            <div class="portfolio-card">
              <div class="portfolio-badge">Inovasi Sosial</div>
              <h3>Program solusi berbasis kebutuhan masyarakat</h3>
              <p>
                Menciptakan model inovasi yang menjawab permasalahan nyata di
                komunitas dengan pendekatan riset yang terukur.
              </p>
            </div>

            <div class="portfolio-card">
              <div class="portfolio-badge">Startup</div>
              <h3>Pendampingan ide bisnis berbasis riset</h3>
              <p>
                Membantu pelaku usaha menghadapi tantangan pasar dengan strategi
                serta data yang lebih kuat dan terarah.
              </p>
            </div>

            <div class="portfolio-card">
              <div class="portfolio-badge">Teknologi</div>
              <h3>Pengembangan produk inovatif berbasis data</h3>
              <p>
                Menghasilkan prototype dan pengembangan karya yang siap diuji,
                dipelajari, dan diterapkan.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="tim" class="section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Pembina Organisasi</p>
            <h2>Para pembina yang membimbing dan mengarahkan organisasi.</h2>
          </div>

          <div class="team-grid">
            <div class="team-card">
              <div class="avatar avatar-one"></div>
              <h3>A. Chizam Baihaqy M.Pd</h3>
              <p>Pembina</p>
            </div>

            <div class="team-card">
              <div class="avatar avatar-two"></div>
              <h3>Ainun Tazkia S.Pd</h3>
              <p>Pembina</p>
            </div>

            <div class="team-card">
              <div class="avatar avatar-three"></div>
              <h3>Rizki Yudha Sentika M.Pd</h3>
              <p>Pembina</p>
            </div>
          </div>
        </div>
      </section>

      <section class="cta">
        <div class="container cta-box">
          <div>
            <p class="eyebrow">Bersama kita membangun ekosistem inovasi yang memberi manfaat.</p>
            <h2>Jadikan ide Anda bermakna dan siap berdaya.</h2>
          </div>
          <a href="#kontak" class="btn btn-light">Hubungi Kami</a>
        </div>
      </section>
    </main>

    <footer id="kontak" class="footer">
      <div class="container footer-grid">
        <div>
          <div class="logo footer-logo">
            <div class="logo-mark" aria-label="PiKIR logo">
              <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="PiKIR">
                <defs>
                  <path id="ringTextPathFooter" d="M 100,100 m -72,0 a 72,72 0 1,1 144,0 a 72,72 0 1,1 -144,0" />
                </defs>

                <circle cx="100" cy="100" r="82" fill="#0e2245" />
                <circle cx="100" cy="100" r="74" fill="#f5d24a" stroke="#0e2245" stroke-width="4" />

                <g fill="#0e2245">
                  <circle cx="100" cy="18" r="4.5" />
                  <circle cx="100" cy="182" r="4.5" />
                  <circle cx="18" cy="100" r="4.5" />
                  <circle cx="182" cy="100" r="4.5" />
                  <circle cx="36" cy="36" r="4.5" />
                  <circle cx="164" cy="36" r="4.5" />
                  <circle cx="36" cy="164" r="4.5" />
                  <circle cx="164" cy="164" r="4.5" />
                  <circle cx="26" cy="63" r="4.5" />
                  <circle cx="174" cy="63" r="4.5" />
                  <circle cx="26" cy="137" r="4.5" />
                  <circle cx="174" cy="137" r="4.5" />
                </g>

                <text fill="#0e2245" font-size="9.5" font-weight="800" letter-spacing="2" font-family="Verdana, sans-serif">
                  <textPath href="#ringTextPathFooter" startOffset="50%" text-anchor="middle">
                    PRAKTISI KEWIRAUSAHAAN INOVASI RISET
                  </textPath>
                </text>

                <circle cx="100" cy="100" r="48" fill="#fffaf0" stroke="#0e2245" stroke-width="4" />

                <path
                  d="M72 66 V136 H82 V100 H114 C126 100 133 94 133 84 C133 72 126 66 114 66 H72 Z
                     M82 76 H111 C118 76 122 79 122 84 C122 89 118 92 111 92 H82 V76 Z"
                  fill="#0e2245"
                />
                <circle cx="100" cy="100" r="5" fill="#f5d24a" />

                <text
                  x="100"
                  y="156"
                  text-anchor="middle"
                  font-size="26"
                  font-family="Verdana, sans-serif"
                  font-weight="900"
                  fill="#0e2245">
                  KIR
                </text>
              </svg>
            </div>
          </div>

          <p>
            PiKIR adalah wadah inovasi yang menghubungkan riset, teknologi,
            dan kewirausahaan untuk menghasilkan solusi yang berdampak.
          </p>
        </div>

        <div>
          <h4>Kontak</h4>
          <ul>
            <li>Jl. Inovasi No. 25, Bandung</li>
            <li>hello@pikir.or.id</li>
            <li>+62 812-3456-7890</li>
          </ul>
        </div>

        <div>
          <h4>Menu</h4>
          <ul>
            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#tentang">Tentang</a></li>
            <li><a href="#program">Program</a></li>
            <li><a href="#kontak">Kontak</a></li>
          </ul>
        </div>
      </div>

      <div class="copyright">
        <div class="container">
          <p>© <span id="year"></span> PiKIR. Semua hak dilindungi.</p>
        </div>
      </div>
    </footer>

    <script>
      document.getElementById("year").textContent = new Date().getFullYear();
    </script>
  </body>
</html>
