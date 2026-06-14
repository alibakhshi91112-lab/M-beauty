[index.html](https://github.com/user-attachments/files/28925733/index.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>beautyM | لوازم آرایشی اورجینال</title>
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --rose: #C5527A;
    --rose-light: #F7E8EF;
    --rose-dark: #8B3055;
    --blush: #F2C4D0;
    --nude: #F9F4F0;
    --charcoal: #2A2A2A;
    --gray: #6B6B6B;
    --gray-light: #E8E4E0;
    --white: #FFFFFF;
    --gold: #C9A84C;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body { font-family: 'Vazirmatn', sans-serif; background: var(--white); color: var(--charcoal); direction: rtl; }

  /* NAV */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(255,255,255,0.96); backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--gray-light);
    padding: 0 5%;
  }
  .nav-inner { max-width: 1200px; margin: 0 auto; display: flex; align-items: center; justify-content: space-between; height: 64px; }
  .logo { font-size: 22px; font-weight: 700; color: var(--rose-dark); letter-spacing: -0.5px; }
  .logo span { color: var(--rose); }
  .nav-links { display: flex; gap: 28px; list-style: none; }
  .nav-links a { text-decoration: none; font-size: 14px; color: var(--gray); transition: color 0.2s; }
  .nav-links a:hover { color: var(--rose); }
  .nav-actions { display: flex; align-items: center; gap: 14px; }
  .btn-nav { background: var(--rose); color: white; border: none; padding: 9px 20px; border-radius: 50px; font-size: 13px; font-family: inherit; cursor: pointer; transition: background 0.2s; }
  .btn-nav:hover { background: var(--rose-dark); }
  .cart-icon { position: relative; cursor: pointer; font-size: 20px; color: var(--charcoal); }
  .cart-badge { position: absolute; top: -6px; left: -6px; background: var(--rose); color: white; font-size: 10px; width: 16px; height: 16px; border-radius: 50%; display: flex; align-items: center; justify-content: center; }

  /* HERO */
  .hero {
    min-height: 100vh; padding-top: 64px;
    background: linear-gradient(135deg, var(--nude) 0%, var(--rose-light) 100%);
    display: flex; align-items: center; justify-content: center;
    text-align: center; padding-left: 5%; padding-right: 5%;
  }
  .hero-content { max-width: 700px; }
  .hero-badge { display: inline-block; background: var(--white); color: var(--rose); font-size: 12px; padding: 6px 16px; border-radius: 50px; border: 1px solid var(--blush); margin-bottom: 24px; }
  .hero-title { font-size: clamp(36px, 6vw, 64px); font-weight: 700; color: var(--charcoal); line-height: 1.2; margin-bottom: 16px; }
  .hero-title em { font-style: normal; color: var(--rose); }
  .hero-sub { font-size: 16px; color: var(--gray); line-height: 1.8; margin-bottom: 36px; max-width: 500px; margin-left: auto; margin-right: auto; }
  .hero-btns { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; }
  .btn-primary { background: var(--rose); color: white; border: none; padding: 14px 32px; border-radius: 50px; font-size: 15px; font-family: inherit; cursor: pointer; transition: all 0.2s; }
  .btn-primary:hover { background: var(--rose-dark); transform: translateY(-1px); }
  .btn-outline { background: transparent; color: var(--rose); border: 1.5px solid var(--rose); padding: 14px 32px; border-radius: 50px; font-size: 15px; font-family: inherit; cursor: pointer; transition: all 0.2s; }
  .btn-outline:hover { background: var(--rose-light); }
  .hero-stats { display: flex; gap: 40px; justify-content: center; margin-top: 56px; flex-wrap: wrap; }
  .stat-item { text-align: center; }
  .stat-num { font-size: 28px; font-weight: 700; color: var(--rose-dark); }
  .stat-lbl { font-size: 12px; color: var(--gray); margin-top: 4px; }

  /* SECTIONS */
  section { padding: 80px 5%; }
  .section-inner { max-width: 1200px; margin: 0 auto; }
  .section-header { text-align: center; margin-bottom: 56px; }
  .section-eyebrow { font-size: 12px; font-weight: 500; color: var(--rose); letter-spacing: 2px; text-transform: uppercase; margin-bottom: 12px; }
  .section-title { font-size: clamp(24px, 3.5vw, 36px); font-weight: 700; color: var(--charcoal); }
  .section-sub { font-size: 15px; color: var(--gray); margin-top: 10px; }

  /* BRANDS */
  .brands-section { background: var(--charcoal); }
  .brands-section .section-eyebrow { color: var(--blush); }
  .brands-section .section-title { color: var(--white); }
  .brands-section .section-sub { color: #aaa; }
  .brands-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 16px; }
  .brand-card {
    background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px; padding: 28px 20px; text-align: center;
    transition: all 0.25s; cursor: pointer; position: relative; overflow: hidden;
  }
  .brand-card::before { content: ''; position: absolute; inset: 0; background: linear-gradient(135deg, rgba(197,82,122,0.15), transparent); opacity: 0; transition: opacity 0.25s; }
  .brand-card:hover { transform: translateY(-4px); border-color: rgba(197,82,122,0.5); }
  .brand-card:hover::before { opacity: 1; }
  .brand-logo { font-size: 22px; font-weight: 700; color: var(--white); letter-spacing: -0.5px; margin-bottom: 6px; }
  .brand-origin { font-size: 11px; color: #888; margin-bottom: 10px; }
  .brand-specialty { font-size: 12px; color: var(--blush); background: rgba(197,82,122,0.15); padding: 4px 12px; border-radius: 50px; display: inline-block; }

  /* CATEGORIES */
  .cats-section { background: var(--nude); }
  .cats-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(160px, 1fr)); gap: 14px; }
  .cat-card {
    background: var(--white); border-radius: 20px; padding: 28px 16px;
    text-align: center; border: 1px solid var(--gray-light);
    transition: all 0.2s; cursor: pointer;
  }
  .cat-card:hover { border-color: var(--rose); transform: translateY(-3px); box-shadow: 0 8px 24px rgba(197,82,122,0.1); }
  .cat-emoji { font-size: 32px; margin-bottom: 12px; display: block; }
  .cat-name { font-size: 14px; font-weight: 500; color: var(--charcoal); }
  .cat-count { font-size: 12px; color: var(--gray); margin-top: 4px; }

  /* PRODUCTS */
  .products-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 20px; }
  .product-card { background: var(--white); border-radius: 20px; overflow: hidden; border: 1px solid var(--gray-light); transition: all 0.25s; cursor: pointer; }
  .product-card:hover { transform: translateY(-4px); box-shadow: 0 16px 40px rgba(0,0,0,0.08); border-color: var(--blush); }
  .product-img { height: 200px; display: flex; align-items: center; justify-content: center; font-size: 56px; }
  .product-info { padding: 16px; }
  .product-brand { font-size: 11px; color: var(--rose); font-weight: 500; letter-spacing: 1px; text-transform: uppercase; }
  .product-name { font-size: 14px; font-weight: 500; color: var(--charcoal); margin: 6px 0; line-height: 1.4; }
  .product-price { font-size: 16px; font-weight: 700; color: var(--rose-dark); }
  .product-old-price { font-size: 13px; color: var(--gray); text-decoration: line-through; margin-right: 8px; }
  .product-footer { display: flex; align-items: center; justify-content: space-between; margin-top: 14px; }
  .stars { color: var(--gold); font-size: 13px; }
  .btn-add { background: var(--rose); color: white; border: none; padding: 8px 16px; border-radius: 50px; font-size: 12px; font-family: inherit; cursor: pointer; transition: background 0.2s; }
  .btn-add:hover { background: var(--rose-dark); }
  .badge-sale { background: var(--rose); color: white; font-size: 10px; padding: 3px 8px; border-radius: 50px; position: absolute; top: 12px; right: 12px; }
  .badge-new { background: var(--gold); color: white; font-size: 10px; padding: 3px 8px; border-radius: 50px; position: absolute; top: 12px; right: 12px; }
  .product-card { position: relative; }

  /* TRUST */
  .trust-section { background: var(--rose-light); }
  .trust-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; }
  .trust-card { background: var(--white); border-radius: 20px; padding: 32px 24px; text-align: center; }
  .trust-icon { font-size: 36px; margin-bottom: 16px; }
  .trust-title { font-size: 15px; font-weight: 600; color: var(--charcoal); margin-bottom: 8px; }
  .trust-text { font-size: 13px; color: var(--gray); line-height: 1.7; }

  /* ABOUT */
  .about-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: center; }
  .about-visual { background: linear-gradient(135deg, var(--rose-light), var(--blush)); border-radius: 32px; height: 400px; display: flex; align-items: center; justify-content: center; font-size: 80px; }
  .about-text h2 { font-size: 32px; font-weight: 700; margin-bottom: 20px; }
  .about-text p { font-size: 15px; color: var(--gray); line-height: 1.9; margin-bottom: 16px; }
  .about-points { list-style: none; margin-top: 24px; }
  .about-points li { font-size: 14px; padding: 8px 0; border-bottom: 1px solid var(--gray-light); display: flex; align-items: center; gap: 10px; }
  .about-points li::before { content: '✓'; color: var(--rose); font-weight: 700; }

  /* FAQ */
  .faq-section { background: var(--nude); }
  .faq-list { max-width: 720px; margin: 0 auto; }
  .faq-item { border-bottom: 1px solid var(--gray-light); }
  .faq-q { padding: 20px 0; font-size: 15px; font-weight: 500; cursor: pointer; display: flex; justify-content: space-between; align-items: center; color: var(--charcoal); }
  .faq-q:hover { color: var(--rose); }
  .faq-a { font-size: 14px; color: var(--gray); line-height: 1.8; padding-bottom: 20px; display: none; }
  .faq-item.open .faq-a { display: block; }
  .faq-item.open .faq-q { color: var(--rose); }
  .faq-arrow { transition: transform 0.2s; font-size: 18px; color: var(--rose); }
  .faq-item.open .faq-arrow { transform: rotate(180deg); }

  /* NEWSLETTER */
  .newsletter { background: var(--charcoal); padding: 60px 5%; text-align: center; }
  .newsletter h2 { font-size: 28px; font-weight: 700; color: var(--white); margin-bottom: 12px; }
  .newsletter p { font-size: 15px; color: #aaa; margin-bottom: 28px; }
  .newsletter-form { display: flex; gap: 12px; justify-content: center; max-width: 460px; margin: 0 auto; }
  .newsletter-form input { flex: 1; padding: 14px 20px; border-radius: 50px; border: none; font-family: inherit; font-size: 14px; direction: rtl; outline: none; }
  .newsletter-form button { background: var(--rose); color: white; border: none; padding: 14px 28px; border-radius: 50px; font-size: 14px; font-family: inherit; cursor: pointer; white-space: nowrap; transition: background 0.2s; }
  .newsletter-form button:hover { background: var(--rose-dark); }

  /* FOOTER */
  footer { background: #1a1a1a; color: #aaa; padding: 56px 5% 24px; }
  .footer-inner { max-width: 1200px; margin: 0 auto; }
  .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 40px; margin-bottom: 48px; }
  .footer-brand .logo { display: block; margin-bottom: 14px; }
  .footer-brand p { font-size: 13px; line-height: 1.8; }
  .footer-col h4 { color: var(--white); font-size: 13px; font-weight: 600; margin-bottom: 16px; letter-spacing: 0.5px; }
  .footer-col ul { list-style: none; }
  .footer-col li { margin-bottom: 10px; }
  .footer-col a { color: #888; text-decoration: none; font-size: 13px; transition: color 0.2s; }
  .footer-col a:hover { color: var(--rose); }
  .footer-bottom { border-top: 1px solid #333; padding-top: 20px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }
  .footer-bottom p { font-size: 12px; color: #555; }
  .social-links { display: flex; gap: 12px; }
  .social-links a { width: 36px; height: 36px; border-radius: 50%; background: #333; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 16px; transition: background 0.2s; }
  .social-links a:hover { background: var(--rose); }

  /* TOAST */
  .toast { position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%) translateY(80px); background: var(--charcoal); color: white; padding: 14px 24px; border-radius: 50px; font-size: 14px; z-index: 999; transition: transform 0.3s; pointer-events: none; }
  .toast.show { transform: translateX(-50%) translateY(0); }

  @media (max-width: 768px) {
    .nav-links { display: none; }
    .about-inner { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .hero-stats { gap: 24px; }
    .newsletter-form { flex-direction: column; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <div class="logo">beauty<span>M</span></div>
    <ul class="nav-links">
      <li><a href="#brands">برندها</a></li>
      <li><a href="#categories">دسته‌بندی</a></li>
      <li><a href="#products">محصولات</a></li>
      <li><a href="#about">درباره ما</a></li>
      <li><a href="#faq">سوالات</a></li>
    </ul>
    <div class="nav-actions">
      <div class="cart-icon" onclick="showToast('🛒 سبد خرید خالی است')">🛒<span class="cart-badge" id="cart-count">0</span></div>
      <button class="btn-nav">ورود</button>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <div class="hero-badge">✨ ۱۰۰٪ اورجینال — ارسال سریع</div>
    <h1 class="hero-title">بهترین برندهای<br><em>آرایشی دنیا</em><br>یک‌جا برای شما</h1>
    <p class="hero-sub">از MAC تا Charlotte Tilbury، از Dior تا Fenty Beauty — همه محصولات اصل با گارانتی اصالت کالا</p>
    <div class="hero-btns">
      <button class="btn-primary" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">خرید کن</button>
      <button class="btn-outline" onclick="document.getElementById('brands').scrollIntoView({behavior:'smooth'})">مشاهده برندها</button>
    </div>
    <div class="hero-stats">
      <div class="stat-item"><div class="stat-num">+1200</div><div class="stat-lbl">محصول اورجینال</div></div>
      <div class="stat-item"><div class="stat-num">+15</div><div class="stat-lbl">برند معتبر</div></div>
      <div class="stat-item"><div class="stat-num">+8000</div><div class="stat-lbl">مشتری راضی</div></div>
      <div class="stat-item"><div class="stat-num">7</div><div class="stat-lbl">روز ضمانت بازگشت</div></div>
    </div>
  </div>
</section>

<!-- BRANDS -->
<section class="brands-section" id="brands">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">INTERNATIONAL BRANDS</div>
      <h2 class="section-title" style="color:white">برندهای معتبر جهانی</h2>
      <p class="section-sub">مستقیم از نمایندگی رسمی — بدون واسطه</p>
    </div>
    <div class="brands-grid">
      <div class="brand-card" onclick="showToast('MAC Cosmetics — محصولات در دسترس ✨')">
        <div class="brand-logo">MAC</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">رنگی · حرفه‌ای</div>
      </div>
      <div class="brand-card" onclick="showToast('Zara Beauty — محصولات در دسترس ✨')">
        <div class="brand-logo">Zara Beauty</div>
        <div class="brand-origin">🇪🇸 اسپانیا</div>
        <div class="brand-specialty">مدرن · مقرون‌به‌صرفه</div>
      </div>
      <div class="brand-card" onclick="showToast('Charlotte Tilbury — محصولات در دسترس ✨')">
        <div class="brand-logo">Charlotte Tilbury</div>
        <div class="brand-origin">🇬🇧 انگلستان</div>
        <div class="brand-specialty">لوکس · جادویی</div>
      </div>
      <div class="brand-card" onclick="showToast('NARS — محصولات در دسترس ✨')">
        <div class="brand-logo">NARS</div>
        <div class="brand-origin">🇫🇷 فرانسه</div>
        <div class="brand-specialty">چشم · لب</div>
      </div>
      <div class="brand-card" onclick="showToast('Dior Beauty — محصولات در دسترس ✨')">
        <div class="brand-logo">Dior</div>
        <div class="brand-origin">🇫🇷 فرانسه</div>
        <div class="brand-specialty">اشرافی · کلاسیک</div>
      </div>
      <div class="brand-card" onclick="showToast('YSL Beauty — محصولات در دسترس ✨')">
        <div class="brand-logo">YSL</div>
        <div class="brand-origin">🇫🇷 فرانسه</div>
        <div class="brand-specialty">مدرن · جسورانه</div>
      </div>
      <div class="brand-card" onclick="showToast('Fenty Beauty — محصولات در دسترس ✨')">
        <div class="brand-logo">Fenty</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">متنوع · همه‌رنگه</div>
      </div>
      <div class="brand-card" onclick="showToast('Huda Beauty — محصولات در دسترس ✨')">
        <div class="brand-logo">Huda Beauty</div>
        <div class="brand-origin">🇦🇪 امارات</div>
        <div class="brand-specialty">درامتیک · اورینتال</div>
      </div>
      <div class="brand-card" onclick="showToast('Too Faced — محصولات در دسترس ✨')">
        <div class="brand-logo">Too Faced</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">فانتزی · جذاب</div>
      </div>
      <div class="brand-card" onclick="showToast('Urban Decay — محصولات در دسترس ✨')">
        <div class="brand-logo">Urban Decay</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">خلاق · رنگارنگ</div>
      </div>
      <div class="brand-card" onclick="showToast('Benefit — محصولات در دسترس ✨')">
        <div class="brand-logo">Benefit</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">شاد · خلاقانه</div>
      </div>
      <div class="brand-card" onclick="showToast('Estée Lauder — محصولات در دسترس ✨')">
        <div class="brand-logo">Estée Lauder</div>
        <div class="brand-origin">🇺🇸 آمریکا</div>
        <div class="brand-specialty">مراقبت · کلاسیک</div>
      </div>
    </div>
  </div>
</section>

<!-- CATEGORIES -->
<section class="cats-section" id="categories">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">CATEGORIES</div>
      <h2 class="section-title">دسته‌بندی محصولات</h2>
      <p class="section-sub">هر چیزی که برای آرایش کامل نیاز داری</p>
    </div>
    <div class="cats-grid">
      <div class="cat-card"><span class="cat-emoji">💋</span><div class="cat-name">رژ لب</div><div class="cat-count">+۱۸۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">👁️</span><div class="cat-name">آرایش چشم</div><div class="cat-count">+۲۴۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">🌟</span><div class="cat-name">کرم پودر</div><div class="cat-count">+۱۲۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">✨</span><div class="cat-name">هایلایتر</div><div class="cat-count">+۸۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">🧴</span><div class="cat-name">مراقبت پوست</div><div class="cat-count">+۲۰۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">💅</span><div class="cat-name">ناخن</div><div class="cat-count">+۹۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">🌸</span><div class="cat-name">عطر</div><div class="cat-count">+۶۰ محصول</div></div>
      <div class="cat-card"><span class="cat-emoji">🎨</span><div class="cat-name">ابزار آرایش</div><div class="cat-count">+۱۵۰ محصول</div></div>
    </div>
  </div>
</section>

<!-- PRODUCTS -->
<section id="products">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">BEST SELLERS</div>
      <h2 class="section-title">پرفروش‌ترین‌ها</h2>
      <p class="section-sub">محصولاتی که مشتریان ما عاشقشانند</p>
    </div>
    <div class="products-grid">
      <div class="product-card">
        <span class="badge-sale">٪۱۵ تخفیف</span>
        <div class="product-img" style="background:#FDE8EE">💄</div>
        <div class="product-info">
          <div class="product-brand">MAC</div>
          <div class="product-name">رژ لب مات Ruby Woo</div>
          <div class="product-footer">
            <div><span class="product-old-price">۵۸۰,۰۰۰</span><span class="product-price">۴۹۳,۰۰۰ تومان</span></div>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★★ <span style="color:#aaa;font-size:12px">(۲۴۸)</span></div>
        </div>
      </div>
      <div class="product-card">
        <span class="badge-new">جدید</span>
        <div class="product-img" style="background:#F0EEF8">🌟</div>
        <div class="product-info">
          <div class="product-brand">Charlotte Tilbury</div>
          <div class="product-name">فاندیشن Magic Skin</div>
          <div class="product-footer">
            <span class="product-price">۱,۲۵۰,۰۰۰ تومان</span>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★★ <span style="color:#aaa;font-size:12px">(۱۸۷)</span></div>
        </div>
      </div>
      <div class="product-card">
        <span class="badge-sale">٪۲۰ تخفیف</span>
        <div class="product-img" style="background:#E8F4E8">👁️</div>
        <div class="product-info">
          <div class="product-brand">NARS</div>
          <div class="product-name">پالت سایه Narsissist</div>
          <div class="product-footer">
            <div><span class="product-old-price">۱,۸۰۰,۰۰۰</span><span class="product-price">۱,۴۴۰,۰۰۰ تومان</span></div>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★☆ <span style="color:#aaa;font-size:12px">(۳۱۲)</span></div>
        </div>
      </div>
      <div class="product-card">
        <div class="product-img" style="background:#FEF3E2">✨</div>
        <div class="product-info">
          <div class="product-brand">Fenty Beauty</div>
          <div class="product-name">هایلایتر Killawatt</div>
          <div class="product-footer">
            <span class="product-price">۸۹۰,۰۰۰ تومان</span>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★★ <span style="color:#aaa;font-size:12px">(۴۲۱)</span></div>
        </div>
      </div>
      <div class="product-card">
        <span class="badge-new">جدید</span>
        <div class="product-img" style="background:#F8E8EE">💋</div>
        <div class="product-info">
          <div class="product-brand">Zara Beauty</div>
          <div class="product-name">ست رژ لب Velvet Nude</div>
          <div class="product-footer">
            <span class="product-price">۳۸۰,۰۰۰ تومان</span>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★☆ <span style="color:#aaa;font-size:12px">(۹۶)</span></div>
        </div>
      </div>
      <div class="product-card">
        <div class="product-img" style="background:#EEF0F8">🌸</div>
        <div class="product-info">
          <div class="product-brand">Dior</div>
          <div class="product-name">عطر Miss Dior Rose</div>
          <div class="product-footer">
            <span class="product-price">۳,۲۰۰,۰۰۰ تومان</span>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★★ <span style="color:#aaa;font-size:12px">(۵۳۸)</span></div>
        </div>
      </div>
      <div class="product-card">
        <span class="badge-sale">٪۱۰ تخفیف</span>
        <div class="product-img" style="background:#F0F8F0">🧴</div>
        <div class="product-info">
          <div class="product-brand">Huda Beauty</div>
          <div class="product-name">پرایمر Easy Bake</div>
          <div class="product-footer">
            <div><span class="product-old-price">۱,۱۰۰,۰۰۰</span><span class="product-price">۹۹۰,۰۰۰ تومان</span></div>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★☆ <span style="color:#aaa;font-size:12px">(۲۰۳)</span></div>
        </div>
      </div>
      <div class="product-card">
        <div class="product-img" style="background:#F8EEF4">💅</div>
        <div class="product-info">
          <div class="product-brand">YSL</div>
          <div class="product-name">رژ لب Tatouage Couture</div>
          <div class="product-footer">
            <span class="product-price">۱,۴۵۰,۰۰۰ تومان</span>
            <button class="btn-add" onclick="addToCart()">افزودن</button>
          </div>
          <div class="stars" style="margin-top:8px">★★★★★ <span style="color:#aaa;font-size:12px">(۱۶۴)</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TRUST -->
<section class="trust-section">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">WHY BEAUTYM</div>
      <h2 class="section-title">چرا beautyM؟</h2>
    </div>
    <div class="trust-grid">
      <div class="trust-card">
        <div class="trust-icon">🏆</div>
        <div class="trust-title">۱۰۰٪ اورجینال</div>
        <div class="trust-text">همه محصولات مستقیم از نمایندگی رسمی برند تامین می‌شوند. کد رهگیری اصالت برای هر سفارش</div>
      </div>
      <div class="trust-card">
        <div class="trust-icon">🚀</div>
        <div class="trust-title">ارسال سریع</div>
        <div class="trust-text">ارسال اکسپرس به سراسر کشور در بسته‌بندی مخصوص برای حفظ کیفیت محصول</div>
      </div>
      <div class="trust-card">
        <div class="trust-icon">🔄</div>
        <div class="trust-title">۷ روز بازگشت</div>
        <div class="trust-text">اگر از خریدت راضی نبودی، ظرف ۷ روز بدون سوال برگردون و پول کاملت برگرده</div>
      </div>
      <div class="trust-card">
        <div class="trust-icon">💬</div>
        <div class="trust-title">مشاوره آرایشی</div>
        <div class="trust-text">تیم متخصص ما آماده‌ست تا بهترین محصول متناسب با نوع پوست و سلیقه‌ات رو بهت معرفی کنه</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <div class="about-inner">
      <div class="about-visual">💄</div>
      <div class="about-text">
        <div class="section-eyebrow">ABOUT BEAUTYM</div>
        <h2>داستان ما</h2>
        <p>beautyM از سال ۱۴۰۰ با یک هدف ساده شروع کرد: دسترسی آسان به بهترین لوازم آرایشی دنیا برای همه. ما باور داریم که هر کسی حق داره از محصولات اورجینال و باکیفیت استفاده کنه.</p>
        <p>با بیش از ۸ هزار مشتری راضی و ۱۵ برند معتبر بین‌المللی در سبد محصولاتمون، امروز یکی از معتبرترین فروشگاه‌های آنلاین لوازم آرایشی خارجی در ایران هستیم.</p>
        <ul class="about-points">
          <li>قرارداد مستقیم با نمایندگی رسمی برندها</li>
          <li>آزمایش اصالت هر محصول قبل از ارسال</li>
          <li>تیم مشاوره متخصص آرایش</li>
          <li>بسته‌بندی اختصاصی و زیبا</li>
          <li>پشتیبانی ۲۴ ساعته واتساپ</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- FAQ -->
<section class="faq-section" id="faq">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">FAQ</div>
      <h2 class="section-title">سوالات متداول</h2>
    </div>
    <div class="faq-list">
      <div class="faq-item open">
        <div class="faq-q" onclick="toggleFaq(this)">چطور مطمئن بشم محصول اورجینال‌ه؟<span class="faq-arrow">⌄</span></div>
        <div class="faq-a">هر محصول دارای کد رهگیری اصالت ۱۶ رقمی‌ه که می‌تونی روی سایت رسمی برند تاییدش کنی. علاوه بر این، بارکد و هولوگرام اصالت روی بسته‌بندی هست.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">زمان ارسال چقدره؟<span class="faq-arrow">⌄</span></div>
        <div class="faq-a">ارسال معمولی ۳ تا ۵ روز کاری. ارسال اکسپرس تهران ۲۴ ساعته، و اکسپرس شهرستان ۲ تا ۳ روز.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">آیا امکان مرجوعی وجود داره؟<span class="faq-arrow">⌄</span></div>
        <div class="faq-a">بله، تا ۷ روز پس از دریافت می‌تونی محصول رو برگردونی — مشروط به اینکه استفاده نشده باشه. پول کامل ظرف ۴۸ ساعت بازگشت داده می‌شه.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">روش‌های پرداخت چیه؟<span class="faq-arrow">⌄</span></div>
        <div class="faq-a">پرداخت آنلاین با تمام کارت‌های بانکی، پرداخت در محل، و اقساط ۳ تا ۱۲ ماهه بدون بهره از طریق اعتبار خرید.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">چطور با شما تماس بگیرم؟<span class="faq-arrow">⌄</span></div>
        <div class="faq-a">از طریق واتساپ ۰۹۱۲-XXX-XXXX، ایمیل info@beautym.ir، یا چت آنلاین سایت. پاسخگویی ۹ صبح تا ۱۱ شب.</div>
      </div>
    </div>
  </div>
</section>

<!-- NEWSLETTER -->
<div class="newsletter">
  <h2>اول باش، بهتر باش 💄</h2>
  <p>خبرنامه ما رو عضو شو — ۱۰٪ تخفیف اول خریدت هدیه می‌گیری</p>
  <div class="newsletter-form">
    <input type="email" placeholder="ایمیل شما" id="email-input">
    <button onclick="subscribeEmail()">عضویت</button>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="logo">beauty<span>M</span></div>
        <p>بهترین برندهای آرایشی دنیا، اورجینال و با ضمانت. از ۱۴۰۰ تا امروز، ۸ هزار مشتری راضی.</p>
      </div>
      <div class="footer-col">
        <h4>دسترسی سریع</h4>
        <ul>
          <li><a href="#brands">برندها</a></li>
          <li><a href="#categories">دسته‌بندی</a></li>
          <li><a href="#products">محصولات</a></li>
          <li><a href="#about">درباره ما</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>پشتیبانی</h4>
        <ul>
          <li><a href="#faq">سوالات متداول</a></li>
          <li><a href="#">راهنمای خرید</a></li>
          <li><a href="#">پیگیری سفارش</a></li>
          <li><a href="#">تماس با ما</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>قوانین</h4>
        <ul>
          <li><a href="#">شرایط استفاده</a></li>
          <li><a href="#">حریم خصوصی</a></li>
          <li><a href="#">سیاست بازگشت</a></li>
          <li><a href="#">ضمانت اصالت</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© ۱۴۰۳ beautyM — تمام حقوق محفوظ است</p>
      <div class="social-links">
        <a href="#" title="اینستاگرام">📸</a>
        <a href="#" title="تلگرام">✈️</a>
        <a href="#" title="واتساپ">💬</a>
      </div>
    </div>
  </div>
</footer>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2500);
}

function addToCart() {
  const el = document.getElementById('cart-count');
  el.textContent = parseInt(el.textContent) + 1;
  showToast('✅ محصول به سبد خرید اضافه شد');
}

function toggleFaq(el) {
  const item = el.parentElement;
  const isOpen = item.classList.contains('open');
  document.querySelectorAll('.faq-item').forEach(i => i.classList.remove('open'));
  if (!isOpen) item.classList.add('open');
}

function subscribeEmail() {
  const v = document.getElementById('email-input').value;
  if (v && v.includes('@')) {
    showToast('🎉 عضویت موفق! کد تخفیف ۱۰٪ به ایمیلت ارسال شد');
    document.getElementById('email-input').value = '';
  } else {
    showToast('⚠️ لطفاً ایمیل معتبر وارد کن');
  }
}
</script>
</body>
</html>
