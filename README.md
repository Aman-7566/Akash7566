
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Akash Kourav Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
    }

    html{
      scroll-behavior:smooth;
    }

    body{
      font-family:'Poppins',sans-serif;
      background:linear-gradient(135deg,#f5f3ff,#ffe7f5);
      overflow-x:hidden;
      color:#111827;
    }

    img{
      max-width:100%;
      display:block;
    }

    .container{
      width:100%;
      max-width:1400px;
      margin:auto;
      padding:20px;
    }

    /* NAVBAR */

    .navbar{
      width:100%;
      background:#050b2e;
      border-radius:24px;
      padding:16px 24px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      flex-wrap:wrap;
      gap:20px;
      box-shadow:0 10px 40px rgba(0,0,0,0.15);
    }

    .logo-area{
      display:flex;
      align-items:center;
      gap:14px;
    }

    .logo-box{
      width:54px;
      height:54px;
      border-radius:16px;
      background:linear-gradient(135deg,#8b5cf6,#d946ef);
      display:flex;
      align-items:center;
      justify-content:center;
      color:#fff;
      font-weight:700;
      font-size:24px;
    }

    .logo-text h2{
      color:#fff;
      font-size:24px;
    }

    .logo-text p{
      color:#cbd5e1;
      font-size:14px;
    }

    .nav-links{
      display:flex;
      gap:28px;
      flex-wrap:wrap;
      justify-content:center;
    }

    .nav-links a{
      text-decoration:none;
      color:#fff;
      font-weight:500;
      transition:.3s;
    }

    .nav-links a:hover{
      color:#a855f7;
    }

    .resume-btn{
      background:linear-gradient(90deg,#8b5cf6,#60a5fa);
      color:#fff;
      padding:12px 22px;
      border-radius:14px;
      text-decoration:none;
      font-weight:600;
    }

    /* HERO SECTION */

    .hero-wrapper{
      display:grid;
      grid-template-columns:340px 1fr;
      gap:22px;
      margin-top:22px;
    }

    .card{
      background:rgba(255,255,255,.9);
      border-radius:28px;
      padding:24px;
      backdrop-filter:blur(10px);
      box-shadow:0 10px 30px rgba(0,0,0,.08);
    }

    .profile-card{
      text-align:center;
    }

    .profile-img{
      width:180px;
      height:180px;
      margin:auto;
      border-radius:50%;
      overflow:hidden;
      border:6px solid #d8b4fe;
    }

    .profile-img img{
      width:100%;
      height:100%;
      object-fit:cover;
    }

    .profile-card h1{
      margin-top:20px;
      font-size:36px;
      color:#111827;
    }

    .profile-card p{
      color:#4b5563;
      margin-top:8px;
      font-weight:500;
    }

    .tagline{
      margin-top:18px;
      background:#eef2ff;
      color:#4f46e5;
      padding:12px;
      border-radius:14px;
      font-size:14px;
      font-weight:600;
    }

    .mini-stats{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:12px;
      margin-top:22px;
    }

    .mini-box{
      background:#fff;
      border-radius:18px;
      padding:16px;
      box-shadow:0 4px 14px rgba(0,0,0,.05);
    }

    .mini-box h3{
      font-size:28px;
      color:#4f46e5;
    }

    .mini-box span{
      font-size:13px;
      color:#6b7280;
    }

    .social-icons{
      margin-top:20px;
      display:flex;
      justify-content:center;
      gap:12px;
      flex-wrap:wrap;
    }

    .social-icons a{
      width:44px;
      height:44px;
      background:#fff;
      border-radius:14px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:#4f46e5;
      text-decoration:none;
      box-shadow:0 4px 14px rgba(0,0,0,.06);
    }

    /* RIGHT HERO */

    .hero-section{
      background:linear-gradient(135deg,#0f2ac9,#7c3aed);
      border-radius:30px;
      padding:42px;
      position:relative;
      overflow:hidden;
      color:#fff;
    }

    .hero-content{
      display:grid;
      grid-template-columns:1.1fr .9fr;
      align-items:center;
      gap:30px;
    }

    .hello{
      font-size:22px;
      font-weight:600;
      margin-bottom:12px;
    }

    .hero-title{
      font-size:74px;
      line-height:1.1;
      font-weight:800;
    }

    .hero-title span{
      color:#e879f9;
    }

    .hero-subtitle{
      font-size:32px;
      font-weight:600;
      margin-top:12px;
    }

    .hero-description{
      margin-top:24px;
      line-height:1.9;
      color:#dbeafe;
      max-width:620px;
    }

    .hero-buttons{
      margin-top:32px;
      display:flex;
      gap:18px;
      flex-wrap:wrap;
    }

    .primary-btn,
    .secondary-btn{
      padding:15px 26px;
      border:none;
      border-radius:16px;
      font-weight:600;
      cursor:pointer;
      font-size:15px;
    }

    .primary-btn{
      background:linear-gradient(90deg,#60a5fa,#d946ef);
      color:#fff;
    }

    .secondary-btn{
      background:#fff;
      color:#1e40af;
    }

    .hero-image img{
      width:100%;
      max-width:450px;
      margin:auto;
    }

    /* STATS */

    .stats-grid{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
      margin-top:26px;
    }

    .stat-card{
      background:rgba(255,255,255,.96);
      border-radius:20px;
      padding:22px;
      text-align:center;
      color:#111827;
    }

    .stat-card h2{
      font-size:36px;
      color:#2563eb;
    }

    .stat-card p{
      margin-top:6px;
      color:#6b7280;
    }

    /* SKILLS */

    .section-title{
      font-size:28px;
      margin:36px 0 20px;
      color:#111827;
    }

    .skills-grid{
      display:grid;
      grid-template-columns:repeat(6,1fr);
      gap:16px;
    }

    .skill-card{
      background:#fff;
      padding:18px;
      border-radius:22px;
      text-align:center;
      box-shadow:0 6px 20px rgba(0,0,0,.05);
      transition:.3s;
    }

    .skill-card:hover{
      transform:translateY(-8px);
    }

    .skill-card i{
      font-size:34px;
      margin-bottom:14px;
      color:#7c3aed;
    }

    .skill-card h4{
      margin-bottom:8px;
    }

    .skill-card p{
      font-size:14px;
      color:#6b7280;
    }

    /* SERVICES */

    .services-grid{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
      margin-top:20px;
    }

    .service-card{
      background:#fff;
      padding:24px;
      border-radius:22px;
      box-shadow:0 6px 20px rgba(0,0,0,.05);
    }

    .service-card i{
      font-size:36px;
      color:#8b5cf6;
      margin-bottom:16px;
    }

    .service-card h3{
      margin-bottom:10px;
    }

    .service-card p{
      color:#6b7280;
      line-height:1.7;
    }

    /* RESPONSIVE */

    @media(max-width:1200px){

      .skills-grid{
        grid-template-columns:repeat(3,1fr);
      }

      .services-grid{
        grid-template-columns:repeat(2,1fr);
      }

      .hero-content{
        grid-template-columns:1fr;
        text-align:center;
      }

      .hero-description{
        margin:auto;
        margin-top:24px;
      }

      .hero-buttons{
        justify-content:center;
      }

    }

    @media(max-width:1024px){

      .hero-wrapper{
        grid-template-columns:1fr;
      }

      .stats-grid{
        grid-template-columns:repeat(2,1fr);
      }

      .hero-title{
        font-size:58px;
      }

    }

    @media(max-width:768px){

      .navbar{
        flex-direction:column;
        align-items:flex-start;
      }

      .nav-links{
        width:100%;
        justify-content:center;
      }

      .hero-section{
        padding:28px;
      }

      .hero-title{
        font-size:46px;
      }

      .hero-subtitle{
        font-size:24px;
      }

      .hero-buttons{
        flex-direction:column;
      }

      .primary-btn,
      .secondary-btn{
        width:100%;
      }

      .skills-grid,
      .services-grid,
      .stats-grid{
        grid-template-columns:1fr;
      }

      .mini-stats{
        grid-template-columns:1fr;
      }

    }

    @media(max-width:480px){

      .container{
        padding:12px;
      }

      .hero-title{
        font-size:38px;
      }

      .profile-card h1{
        font-size:28px;
      }

      .logo-text h2{
        font-size:20px;
      }

    }

  </style>
</head>
<body>

  <div class="container">

    <!-- NAVBAR -->

    <nav class="navbar">

      <div class="logo-area">
        <div class="logo-box">AK</div>

        <div class="logo-text">
          <h2>Akash Kourav</h2>
          <p>Power BI Developer & BI Analyst</p>
        </div>
      </div>

      <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Skills</a>
        <a href="#">Projects</a>
        <a href="#">Experience</a>
        <a href="#">Certifications</a>
        <a href="#">Awards</a>
      </div>

      <a href="#" class="resume-btn">Resume</a>

    </nav>

    <!-- HERO -->

    <section class="hero-wrapper">

      <!-- LEFT PROFILE -->

      <div class="card profile-card">

        <div class="profile-img">
          <img src="https://i.imgur.com/uIgDDDd.png" alt="profile">
        </div>

        <h1>Akash Kourav</h1>

        <p>Power BI Developer & BI Analyst</p>

        <div class="tagline">
          Turning Data Into Powerful Insights
        </div>

        <div class="mini-stats">

          <div class="mini-box">
            <h3>50+</h3>
            <span>Dashboards</span>
          </div>

          <div class="mini-box">
            <h3>2+</h3>
            <span>Years Exp.</span>
          </div>

          <div class="mini-box">
            <h3>5★</h3>
            <span>Rating</span>
          </div>

        </div>

        <div class="social-icons">
          <a href="#"><i class="fab fa-linkedin-in"></i></a>
          <a href="#"><i class="fab fa-github"></i></a>
          <a href="#"><i class="fas fa-envelope"></i></a>
          <a href="#"><i class="fas fa-briefcase"></i></a>
        </div>

      </div>

      <!-- RIGHT HERO -->

      <div class="hero-section">

        <div class="hero-content">

          <div>

            <div class="hello">👋 Hello, I'm</div>

            <h1 class="hero-title">
              Akash <span>Kourav</span>
            </h1>

            <h2 class="hero-subtitle">
              Power BI Developer & BI Analyst
            </h2>

            <p class="hero-description">
              Transforming raw data into powerful insights that drive smarter business decisions. Specialized in interactive dashboards, ETL pipelines, Power Platform, Azure and data storytelling across industries.
            </p>

            <div class="hero-buttons">
              <button class="primary-btn">View My Work →</button>
              <button class="secondary-btn">Hire Me</button>
            </div>

          </div>

          <div class="hero-image">
            <img src="https://i.imgur.com/qf9m6Vf.png" alt="dashboard image">
          </div>

        </div>

        <div class="stats-grid">

          <div class="stat-card">
            <h2>50+</h2>
            <p>Power BI Dashboards</p>
          </div>

          <div class="stat-card">
            <h2>25+</h2>
            <p>Happy Clients</p>
          </div>

          <div class="stat-card">
            <h2>100%</h2>
            <p>Client Satisfaction</p>
          </div>

          <div class="stat-card">
            <h2>10+</h2>
            <p>Industries Served</p>
          </div>

        </div>

      </div>

    </section>

    <!-- SKILLS -->

    <h2 class="section-title">Core Technologies</h2>

    <section class="skills-grid">

      <div class="skill-card">
        <i class="fas fa-chart-bar"></i>
        <h4>Power BI</h4>
        <p>Expert • 95%</p>
      </div>

      <div class="skill-card">
        <i class="fas fa-database"></i>
        <h4>SQL</h4>
        <p>Advanced • 90%</p>
      </div>

      <div class="skill-card">
        <i class="fab fa-python"></i>
        <h4>Python</h4>
        <p>Intermediate • 80%</p>
      </div>

      <div class="skill-card">
        <i class="fab fa-microsoft"></i>
        <h4>Azure</h4>
        <p>Intermediate • 70%</p>
      </div>

      <div class="skill-card">
        <i class="fas fa-chart-line"></i>
        <h4>Tableau</h4>
        <p>Advanced • 85%</p>
      </div>

      <div class="skill-card">
        <i class="fas fa-cogs"></i>
        <h4>ETL / DAX</h4>
        <p>Advanced • 88%</p>
      </div>

    </section>

    <!-- SERVICES -->

    <h2 class="section-title">What I Do</h2>

    <section class="services-grid">

      <div class="service-card">
        <i class="fas fa-chart-pie"></i>
        <h3>Data Analysis</h3>
        <p>Extract meaningful insights from complex business data.</p>
      </div>

      <div class="service-card">
        <i class="fas fa-laptop-code"></i>
        <h3>Dashboard Development</h3>
        <p>Build interactive dashboards that improve decisions.</p>
      </div>

      <div class="service-card">
        <i class="fas fa-server"></i>
        <h3>ETL & Data Modeling</h3>
        <p>Design efficient data pipelines and scalable models.</p>
      </div>

      <div class="service-card">
        <i class="fas fa-robot"></i>
        <h3>Automation</h3>
        <p>Automate business workflows using Power Platform.</p>
      </div>

    </section>

  </div>

</body>
</html>


✅ Optimized Spacing
