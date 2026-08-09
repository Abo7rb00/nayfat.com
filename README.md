# nayfat.com <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نايفات | للبناء والتطوير العقاري الفاخر</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #121A24;
            --secondary-color: #C5A880;
            --accent-color: #E6C594;
            --bg-light: #F9F9FB;
            --card-bg: #FFFFFF;
            --text-main: #2C3539;
            --text-muted: #6C7A89;
            --whatsapp-color: #25D366;
            --transition: all 0.4s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-main);
            overflow-x: hidden;
        }

        /* Header / Navbar */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            background: rgba(18, 26, 36, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(197, 168, 128, 0.2);
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            color: #FFFFFF;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--secondary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: #FFFFFF;
            text-decoration: none;
            font-size: 16px;
            font-weight: 500;
            transition: var(--transition);
        }

        nav a:hover {
            color: var(--secondary-color);
        }

        .cta-btn {
            background: linear-gradient(135deg, var(--secondary-color), var(--accent-color));
            color: var(--primary-color);
            padding: 10px 24px;
            border-radius: 6px;
            font-weight: 700;
            text-decoration: none;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(197, 168, 128, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .cta-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(197, 168, 128, 0.5);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(18, 26, 36, 0.7), rgba(18, 26, 36, 0.85)), 
                        url('https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
            display: flex;
            align-items: center;
            padding: 0 8%;
            position: relative;
        }

        .hero-content {
            max-width: 650px;
            color: #FFFFFF;
            animation: fadeIn 1.2s ease;
        }

        .hero-subtitle {
            color: var(--secondary-color);
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 12px;
            letter-spacing: 1px;
        }

        .hero-title {
            font-size: 52px;
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-desc {
            font-size: 18px;
            color: #D1D5DB;
            margin-bottom: 35px;
            line-height: 1.6;
        }

        .hero-btns {
            display: flex;
            gap: 15px;
        }

        .secondary-btn {
            border: 2px solid var(--secondary-color);
            color: #FFFFFF;
            padding: 10px 24px;
            border-radius: 6px;
            font-weight: 700;
            text-decoration: none;
            transition: var(--transition);
        }

        .secondary-btn:hover {
            background: var(--secondary-color);
            color: var(--primary-color);
        }

        /* Services Section */
        .section {
            padding: 100px 8%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 36px;
            color: var(--primary-color);
            font-weight: 800;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            width: 50%;
            height: 3px;
            background: var(--secondary-color);
            position: absolute;
            bottom: -10px;
            left: 25%;
        }

        .section-desc {
            color: var(--text-muted);
            margin-top: 15px;
            font-size: 16px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--card-bg);
            padding: 40px 30px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: var(--transition);
            border-top: 4px solid transparent;
        }

        .service-card:hover {
            transform: translateY(-8px);
            border-top-color: var(--secondary-color);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .service-icon {
            font-size: 40px;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        .service-title {
            font-size: 22px;
            color: var(--primary-color);
            margin-bottom: 12px;
        }

        .service-text {
            color: var(--text-muted);
            line-height: 1.6;
        }

        /* Interactive Cost Calculator Section */
        .calculator-section {
            background: var(--primary-color);
            color: #FFFFFF;
            border-radius: 20px;
            padding: 60px 40px;
            margin: 0 8% 100px 8%;
        }

        .calc-wrapper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .calc-info h3 {
            font-size: 32px;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        .calc-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid rgba(197, 168, 128, 0.2);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #E5E7EB;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            border-radius: 6px;
            border: 1px solid rgba(255,255,255,0.2);
            background: rgba(0,0,0,0.2);
            color: #FFFFFF;
            font-size: 16px;
        }

        .calc-result {
            font-size: 24px;
            font-weight: 700;
            color: var(--accent-color);
            margin-top: 15px;
            text-align: center;
        }

        /* Contact Section */
        .contact-section {
            background: #FFFFFF;
            border-radius: 16px;
            padding: 60px 40px;
            margin: 0 8% 100px 8%;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            border: 1px solid rgba(197, 168, 128, 0.3);
        }

        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background-color: var(--whatsapp-color);
            color: #FFFFFF;
            padding: 16px 36px;
            border-radius: 50px;
            font-size: 20px;
            font-weight: 700;
            text-decoration: none;
            margin-top: 25px;
            transition: var(--transition);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.3);
        }

        .whatsapp-btn:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 12px 30px rgba(37, 211, 102, 0.4);
            background-color: #20bd5a;
        }

        /* Footer */
        footer {
            background: var(--primary-color);
            color: #FFFFFF;
            padding: 40px 8% 20px 8%;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        footer p {
            color: var(--text-muted);
            font-size: 14px;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 768px) {
            .hero-title { font-size: 36px; }
            .calc-wrapper { grid-template-columns: 1fr; }
            nav ul { display: none; }
        }
    </style>
</head>
<body>

    <!-- الهيدر -->
    <header>
        <div class="logo">نايفات<span>.</span></div>
        <nav>
            <ul>
                <li><a href="#home">الرئيسية</a></li>
                <li><a href="#services">خدماتنا</a></li>
                <li><a href="#calculator">حاسبة البناء</a></li>
                <li><a href="#contact">تواصل معنا</a></li>
            </ul>
        </nav>
        <!-- رابط واتساب مباشر في الهيدر -->
        <a href="https://wa.me/966549331981" target="_blank" class="cta-btn">
            تواصل معنا عبر الواتساب
        </a>
    </header>

    <!-- قسم البداية -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-subtitle">شركة نايفات للتطوير العقاري</div>
            <h1 class="hero-title">نُجسد رؤيتك في بناء منزل معبّر عن الفخامة</h1>
            <p class="hero-desc">نحن نبتكر المساحات المعمارية الحديثة بتصاميم متطورة، تنفيذ عالي الدقة، ومعايير جودة لا تضاهى لتشييد منازل أحلامك.</p>
            <div class="hero-btns">
                <a href="#calculator" class="cta-btn">احسب تكلفة بيتك</a>
                <a href="https://wa.me/966549331981" target="_blank" class="secondary-btn">استشارة واتساب</a>
            </div>
        </div>
    </section>

    <!-- قسم الخدمات -->
    <section class="section" id="services">
        <div class="section-header">
            <h2 class="section-title">خدماتنا المتميزة</h2>
            <p class="section-desc">حلول متكاملة تبدأ من الفكرة الأولى وحتى تسليم المفتاح</p>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🏛️</div>
                <h3 class="service-title">التصميم المعماري</h3>
                <p class="service-text">مخططات هندسية حديثة واستغلال ذكي للمساحات يجمع بين الجمالية والوظيفة.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🏗️</div>
                <h3 class="service-title">البناء والتشييد</h3>
                <p class="service-text">تنفيذ المشاريع بأعلى معايير السلامة والجودة وبإشراف نخبة من المهندسين.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">✨</div>
                <h3 class="service-title">التشطيبات الفاخرة</h3>
                <p class="service-text">لمسات داخلية وخارجية راقية باستخدام أجود المواد المقاومة والديكورات الحديثة.</p>
            </div>
        </div>
    </section>

    <!-- حاسبة تكلفة تقريبية -->
    <section class="calculator-section" id="calculator">
        <div class="calc-wrapper">
            <div class="calc-info">
                <h3>حاسبة البناء التقديرية</h3>
                <p>احصل على تقدير أولي لتكلفة بناء مسكنك الخاص بناءً على مساحة الأرض ونوع التشطيب المطلوب.</p>
            </div>
            <div class="calc-form">
                <div class="form-group">
                    <label>مساحة البناء الإجمالية (م²)</label>
                    <input type="number" id="area" placeholder="مثال: 400" oninput="calculateCost()">
                </div>
                <div class="form-group">
                    <label>مستوى التشطيب</label>
                    <select id="quality" onchange="calculateCost()">
                        <option value="1200">عظم مع المواد (أساسي)</option>
                        <option value="2000">تشطيب مودرن فاخر</option>
                        <option value="2800">تشطيب VIP ذكي</option>
                    </select>
                </div>
                <div class="calc-result" id="result">
                    التكلفة التقديرية: 0 ريال
                </div>
            </div>
        </div>
    </section>

    <!-- قسم تواصل معنا المخصص للواتساب -->
    <section class="contact-section" id="contact">
        <h2 class="section-title">تواصل معنا</h2>
        <p class="section-desc" style="margin-top: 20px;">يسعدنا الإجابة على جميع استفساراتك وبدء تخطيط مشروعك القادم عبر الواتساب</p>
        
        <!-- زر الواتساب -->
        <a href="https://wa.me/966549331981" target="_blank" class="whatsapp-btn">
            <span>محادثة مباشرة عبر الواتساب (+966 54 933 1981)</span>
        </a>
    </section>

    <!-- الفوتر -->
    <footer>
        <p>جميع الحقوق محفوظة &copy; 2026 شركة نايفات للبناء والتطوير العقاري</p>
    </footer>

    <!-- سكربت الحساب التفاعلي -->
    <script>
        function calculateCost() {
            const area = document.getElementById('area').value;
            const rate = document.getElementById('quality').value;
            const resultDiv = document.getElementById('result');

            if (area > 0) {
                const total = area * rate;
                resultDiv.innerText = `التكلفة التقديرية: ${total.toLocaleString()} ريال سعودي`;
            } else {
                resultDiv.innerText = 'التكلفة التقديرية: 0 ريال';
            }
        }
    </script>
</body>
</html>
