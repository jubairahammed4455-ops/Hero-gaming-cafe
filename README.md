<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Hero Gaming Cafe</title>
  <style>
    :root{
      --accent-start: #d83b2b;
      --accent-end:   #ff7a00;
      --text: #fff;
      --pill-height: 68px;
      --max-width: 1100px;
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:"Helvetica Neue", Arial, sans-serif;
      background: linear-gradient(90deg,var(--accent-start), var(--accent-end));
      display:flex;
      align-items:center;
      justify-content:center;
      min-height:100vh;
      padding:24px;
      color:var(--text);
    }

    .hero {
      width:100%;
      max-width:var(--max-width);
      background: linear-gradient(90deg, rgba(0,0,0,0.04) 0%, rgba(0,0,0,0.02) 100%);
      border-radius:14px;
      overflow:hidden;
      display:grid;
      grid-template-columns: 1fr 420px;
      box-shadow:0 12px 40px rgba(0,0,0,0.25);
      align-items:center;
    }

    .hero-left{
      padding:48px 42px;
      display:flex;
      flex-direction:column;
      gap:26px;
    }

    .headline{
      margin:0;
      line-height:0.9;
      font-weight:800;
      font-size:88px;
      letter-spacing:-2px;
      text-transform:uppercase;
    }

    .cta-wrap{ margin-top:-6px; }

    .pill{
      display:inline-block;
      background: linear-gradient(90deg, rgba(255,80,20,0.98), rgba(255,120,40,0.98));
      color:#fff;
      padding: 0 34px;
      height: var(--pill-height);
      border-radius:999px;
      font-size:32px;
      font-weight:800;
      line-height:var(--pill-height);
      text-decoration:none;
      box-shadow:0 8px 22px rgba(0,0,0,0.25);
      transition:transform 0.15s ease-in-out;
    }

    .pill:hover{ transform:scale(1.05); }
    .pill:active{ transform:translateY(1px); }

    .hero-right{
      min-height:360px;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:28px;
      background:linear-gradient(90deg, rgba(0,0,0,0.02), rgba(0,0,0,0.02));
    }

    .hero-bg {
      width:100%;
      height:100%;
      border-radius:12px;
      background-image:url('hero-gaming-cafe.jpg');
      background-size:cover;
      background-position:center;
      position:relative;
    }

    .controller{
      position:absolute;
      top:22px;
      right:22px;
      width:94px;
      height:58px;
      opacity:0.98;
      filter:drop-shadow(0 6px 12px rgba(0,0,0,0.35));
    }

    @media (max-width:980px){
      .hero{ grid-template-columns:1fr; }
      .hero-left{ padding:28px; text-align:center; }
      .headline{ font-size:56px; }
      .hero-right{ padding:18px; }
      .controller{ top:14px; right:14px; width:80px; height:48px; }
      .pill{ font-size:22px; padding:0 20px; height:56px; line-height:56px;}
    }

    @media (max-width:460px){
      .headline{ font-size:40px; }
      .pill{ font-size:18px; height:48px; line-height:48px; }
    }
  </style>
</head>
<body>
  <main class="hero">
    <section class="hero-left">
      <h1 class="headline">Visit<br>Hero<br>Gaming<br>Cafe</h1>

      <div class="cta-wrap">
        <!-- Facebook link -->
        <a class="pill"
           href="https://m.facebook.com/story.php?story_fbid=pfbid02hyXVzEN7xN9iP4XUDbykwcMmfWR2bsBN9HKVQUowvRRbDjF8YXgGDoM3H4CB18zxl&id=61567183790159&mibextid=Nif5oz"
           target="_blank"
           rel="noopener noreferrer">
          CLICK THE LINK!
        </a>
      </div>
    </section>

    <aside class="hero-right">
      <div class="hero-bg">
        <svg class="controller" viewBox="0 0 64 40" xmlns="http://www.w3.org/2000/svg">
          <rect width="64" height="40" rx="8" fill="#0e0e0e"/>
          <g transform="translate(7,6)" fill="#fde9d6">
            <circle cx="42" cy="6" r="2.8"/>
            <circle cx="46" cy="11" r="2.8"/>
            <circle cx="38" cy="11" r="2.8"/>
            <path d="M6 6h6v6H6zM2 10h6v6H2z" />
          </g>
        </svg>
      </div>
    </aside>
  </main>
</body>
</html>
.hero {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #d62828, #ff6600);
  color: #fff;
  padding: 20px;
}

.hero-left {
  flex: 1;
  min-width: 280px;
  max-width: 500px;
  text-align: center;
  padding: 20px;
}

.hero-left h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
  font-weight: 700;
}

.hero-left p {
  font-size: 1.1rem;
  margin-bottom: 25px;
}

.cta-wrap .pill {
  display: inline-block;
  padding: 14px 28px;
  background: #ff4500;
  color: white;
  border-radius: 50px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.3s ease, background 0.3s ease;
}

.cta-wrap .pill:hover {
  background: #ff6600;
  transform: scale(1.05);
}

.hero-right {
  flex: 1;
  min-width: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-bg .controller {
  width: 120px;
  height: auto;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
