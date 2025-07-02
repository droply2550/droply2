<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>เว็บไซต์ทันสมัย</title>
  <style>
    :root {
      --main-bg-color: #f5f5f5;
      --text-color: #333;
      --footer-bg: #222;
      --footer-text: #eee;
      --highlight: #007bff;
    }

    [data-theme="dark"] {
      --main-bg-color: #1e1e1e;
      --text-color: #ffffff;
      --footer-bg: #111;
      --footer-text: #ccc;
      --highlight: #66ccff;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--main-bg-color);
      color: var(--text-color);
      transition: background-color 0.3s, color 0.3s;
    }

    header {
      background-color: var(--highlight);
      color: white;
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      margin: 0;
      font-size: 20px;
    }

    .top-bar {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      position: relative;
    }

    .menu-dropdown {
      position: relative;
    }

    .menu-button {
      background: none;
      border: none;
      font-size: 16px;
      cursor: pointer;
      padding: 8px 12px;
      color: white;
    }

    .menu-list {
      position: absolute;
      top: 100%;
      right: 0;
      background: var(--main-bg-color);
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      border-radius: 8px;
      display: none;
      flex-direction: column;
      min-width: 200px;
      z-index: 10;
    }

    .menu-list button {
      background: none;
      border: none;
      padding: 10px 15px;
      text-align: left;
      font-size: 14px;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 8px;
      color: var(--text-color);
      transition: transform 0.2s ease;
    }

    .menu-list button:hover {
      background-color: var(--highlight);
      color: white;
      transform: translateX(5px);
    }

    .menu-dropdown:hover .menu-list {
      display: flex;
    }

    .divider {
      height: 2px;
      background-color: #ddd;
      margin: 0;
    }

    .carousel {
      width: 100%;
      max-width: 1000px;
      margin: auto;
      overflow: hidden;
    }
    .carousel .slides {
      display: flex;
      transition: transform 0.6s ease-in-out;
      width: 300%;
    }
    .carousel img {
      width: 100%;
      height: 400px;
      object-fit: cover;
      flex-shrink: 0;
    }

    .gallery-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 15px;
      padding: 40px;
      max-width: 1000px;
      margin: auto;
    }
    .gallery-container img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 8px;
      transition: transform 0.3s ease;
    }
    .gallery-container img:hover {
      transform: scale(1.05);
    }

    footer {
      background-color: var(--footer-bg);
      color: var(--footer-text);
      padding: 40px 20px;
    }
    .footer-container {
      max-width: 1000px;
      margin: auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .footer-column {
      flex: 1 1 250px;
      padding: 10px;
    }
    .footer-column h4 {
      margin-bottom: 15px;
      color: var(--highlight);
    }
    .footer-column a {
      display: block;
      color: var(--footer-text);
      text-decoration: none;
      margin-bottom: 8px;
    }
    .footer-column a:hover {
      text-decoration: underline;
    }

    .social-icons {
      display: flex;
      gap: 10px;
    }
    .social-icons a {
      text-align: center;
      transition: transform 0.3s;
    }
    .social-icons a:hover {
      transform: scale(1.2);
    }
    .social-icons img {
      width: 32px;
      height: 32px;
    }

    .copyright {
      text-align: center;
      margin-top: 30px;
      font-size: 14px;
      color: #aaa;
    }
  </style>
</head>
<body>
  <header>
    <h1>เว็บไซต์ทันสมัย</h1>
    <div class="top-bar">
      <div class="menu-dropdown">
        <button class="menu-button">☰ เมนู</button>
        <div class="menu-list">
          <button onclick="toggleLanguage()">🌐 แปลภาษา</button>
          <button onclick="toggleTheme()">🌓 ธีมสีอัตโนมัติ</button>
        </div>
      </div>
    </div>
  </header>

  <div class="divider"></div>

  <div class="carousel">
    <div class="slides" id="carouselSlides">
      <img src="https://source.unsplash.com/1000x400/?japan,tokyo" alt="Banner 1">
      <img src="https://source.unsplash.com/1000x400/?kyoto,night" alt="Banner 2">
      <img src="https://source.unsplash.com/1000x400/?japan,shrine" alt="Banner 3">
    </div>
  </div>

  <div class="gallery-container">
    <img src="https://cdn.visitgifu.com/wp/2020/03/c2d0da73-new25_1.jpg" alt="Gallery 1">
    <img src="https://www.jnto.or.th/wp-content/uploads/2019/11/NOV19-Chubu-12.jpg" alt="Gallery 2">
    <img src="https://www.wonderfulpackage.com/uploads/moxie/Article/%E0%B8%8D%E0%B8%B5%E0%B9%88%E0%B8%9B%E0%B8%B8%E0%B9%88%E0%B8%99/sanmachisuji/1.jpg" alt="Gallery 3">
    <img src="https://source.unsplash.com/600x400/?kyoto,river" alt="Gallery 4">
    <img src="https://source.unsplash.com/600x400/?osaka,night" alt="Gallery 5">
    <img src="https://source.unsplash.com/600x400/?tokyo,tower" alt="Gallery 6">
  </div>

  <footer>
    <div class="footer-container">
      <div class="footer-column">
        <h4 id="footer-title">ชื่อเว็บไซต์</h4>
        <p id="footer-description">เว็บไซต์ตัวอย่างที่แสดงภาพแกลเลอรี่ และข้อมูลพื้นฐาน</p>
      </div>
      <div class="footer-column">
        <h4 id="menu-title">เมนู</h4>
        <a href="#" id="menu-about">เกี่ยวกับเรา</a>
        <a href="#" id="menu-faq">คำถามพบบ่อย</a>
        <a href="#" id="menu-privacy">นโยบายความเป็นส่วนตัว</a>
      </div>
      <div class="footer-column">
        <h4 id="follow-title">ช่องทางติดตามข่าวสาร</h4>
        <div class="social-icons">
          <div>
            <div id="social-fb-label">Facebook</div>
            <a href="#"><img src="facebook-icon.png" alt="Facebook"></a>
          </div>
          <div>
            <div id="social-ig-label">Instagram</div>
            <a href="#"><img src="instagram-icon.png" alt="Instagram"></a>
          </div>
        </div>
      </div>
    </div>
    <div class="copyright" id="copyright-text">
      © 2025 เว็บไซต์ตัวอย่าง. สงวนลิขสิทธิ์.
    </div>
  </footer>

  <script>
    const slides = document.getElementById("carouselSlides");
    const total = slides.children.length;
    let index = 0;
    setInterval(() => {
      index = (index + 1) % total;
      slides.style.transform = `translateX(-${index * 100}%)`;
    }, 3000);

    let currentLang = 'th';

    const translations = {
      th: {
        "footer-title": "ชื่อเว็บไซต์",
        "footer-description": "เว็บไซต์ตัวอย่างที่แสดงภาพแกลเลอรี่ และข้อมูลพื้นฐาน",
        "menu-title": "เมนู",
        "menu-about": "เกี่ยวกับเรา",
        "menu-faq": "คำถามพบบ่อย",
        "menu-privacy": "นโยบายความเป็นส่วนตัว",
        "follow-title": "ช่องทางติดตามข่าวสาร",
        "social-fb-label": "Facebook",
        "social-ig-label": "Instagram",
        "copyright-text": "© 2025 เว็บไซต์ตัวอย่าง. สงวนลิขสิทธิ์."
      },
      en: {
        "footer-title": "Website Name",
        "footer-description": "Sample website showcasing gallery and basic information",
        "menu-title": "Menu",
        "menu-about": "About Us",
        "menu-faq": "FAQ",
        "menu-privacy": "Privacy Policy",
        "follow-title": "Follow Us",
        "social-fb-label": "Facebook",
        "social-ig-label": "Instagram",
        "copyright-text": "© 2025 Sample Website. All rights reserved."
      }
    };

    function toggleLanguage() {
      currentLang = currentLang === 'th' ? 'en' : 'th';
      const textMap = translations[currentLang];
      for (const id in textMap) {
        const el = document.getElementById(id);
        if (el) el.textContent = textMap[id];
      }
    }

    function toggleTheme() {
      const html = document.documentElement;
      if (html.getAttribute('data-theme') === 'dark') {
        html.removeAttribute('data-theme');
      } else {
        html.setAttribute('data-theme', 'dark');
      }
    }
  </script>
</body>
</html>
