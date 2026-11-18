# Karla-Dakshinpara-Football-Academy10
All of us
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>করড়া দক্ষিণপাড়া ফুটবল একাডেমি (KARRA)</title>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0B4F28;
            --primary-dark: #062E17;
            --accent: #D91E26;
            --gold: #D4AF37;
            --light: #F4F7F6;
            --dark: #1A1A1A;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Hind Siliguri', sans-serif;
        }
        body {
            background-color: var(--light);
            color: var(--dark);
            padding-bottom: 50px;
        }
        header {
            background: linear-gradient(135deg, var(--primary-dark), var(--primary));
            color: white;
            text-align: center;
            padding: 20px 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .logo-container {
            width: 80px;
            height: 80px;
            margin: 0 auto 10px;
            border-radius: 50%;
            overflow: hidden;
            border: 3px solid white;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3);
            background: white;
        }
        .logo-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        header h1 {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 2px;
        }
        header p {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        /* Banner Slider Section */
        .slider-section {
            width: 100%;
            max-width: 800px;
            margin: 15px auto;
            padding: 0 10px;
        }
        .slider-container {
            position: relative;
            width: 100%;
            height: 200px;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            background: #ddd;
        }
        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 0.8s ease-in-out;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .slide.active {
            opacity: 1;
        }
        .slide img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .slider-btns {
            text-align: center;
            margin-top: 8px;
        }
        .btn-custom {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            transition: 0.2s;
            margin: 3px;
        }
        .btn-custom:active {
            transform: scale(0.95);
        }

        /* Main Container */
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 10px;
        }
        section {
            background: white;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }
        h2.section-title {
            font-size: 1.2rem;
            color: var(--primary-dark);
            border-bottom: 2px solid var(--primary);
            padding-bottom: 5px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Squad Grid */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
        }
        .player-card {
            background: #fafafa;
            border-radius: 10px;
            overflow: hidden;
            text-align: center;
            border: 1px solid #eee;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            position: relative;
        }
        .player-img {
            width: 100%;
            height: 120px;
            object-fit: cover;
            background: #ccc;
        }
        .player-number {
            background: var(--primary);
            color: white;
            font-weight: 700;
            padding: 4px;
            font-size: 1rem;
        }
        .delete-btn {
            position: absolute;
            top: 5px;
            right: 5px;
            background: rgba(217, 30, 38, 0.8);
            color: white;
            border: none;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            font-size: 0.75rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Legends Section */
        .legend-card {
            background: linear-gradient(135deg, #fff9e6, #fff);
            border: 1px solid var(--gold);
        }
        .legend-card .player-number {
            background: var(--gold);
            color: #000;
        }

        /* Executive Committee */
        .committee-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        .committee-card {
            background: #f9f9f9;
            border-radius: 8px;
            padding: 10px;
            text-align: center;
            border-left: 4px solid var(--primary);
        }
        .committee-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto 5px;
            border: 2px solid var(--primary);
        }
        .committee-card h4 {
            font-size: 0.95rem;
            color: var(--primary-dark);
        }
        .committee-card p {
            font-size: 0.8rem;
            color: #555;
        }
        .committee-card a {
            display: inline-block;
            margin-top: 5px;
            font-size: 0.8rem;
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
        }

        /* Location & Contact */
        .info-box {
            background: #eef7f2;
            border-left: 5px solid var(--primary);
            padding: 12px;
            border-radius: 6px;
            font-size: 0.95rem;
            line-height: 1.6;
        }
        .info-box i {
            color: var(--primary);
            margin-right: 8px;
        }

        /* Hidden file input */
        input[type="file"] {
            display: none;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-container">
            <img src="65951.jpg" alt="Logo">
        </div>
        <h1>করড়া দক্ষিণপাড়া ফুটবল একাডেমি</h1>
        <p>KARRA SOUTH PARA FOOTBALL ACADEMY</p>
    </header>

    <!-- Multi-Banner Slider -->
    <div class="slider-section">
        <div class="slider-container" id="sliderContainer">
            <!-- Default Slide -->
            <div class="slide active">
                <img src="65951.jpg" alt="Banner">
            </div>
        </div>
        <div class="slider-btns">
            <button class="btn-custom" onclick="document.getElementById('bannerUpload').click()"><i class="fa fa-plus"></i> ব্যানার যোগ করুন</button>
            <input type="file" id="bannerUpload" accept="image/*" onchange="addBanner(event)">
        </div>
    </div>

    <div class="container">

        <!-- Executive Committee -->
        <section>
            <h2 class="section-title"><span><i class="fa fa-users"></i> পরিচালনা পর্ষদ</span></h2>
            <div class="committee-grid" id="committeeGrid">
                <div class="committee-card">
                    <img src="65951.jpg" class="committee-img" alt="President">
                    <h4>মোঃ আকাশ</h4>
                    <p>সভাপতি</p>
                    <a href="tel:01700000000"><i class="fa fa-phone"></i> কল করুন</a>
                </div>
                <div class="committee-card">
                    <img src="65951.jpg" class="committee-img" alt="Cashier">
                    <h4>ক্যাশিয়ার নাম</h4>
                    <p>কোষাধ্যক্ষ</p>
                    <a href="tel:01700000000"><i class="fa fa-phone"></i> কল করুন</a>
                </div>
            </div>
        </section>

        <!-- Current Squad -->
        <section>
            <h2 class="section-title">
                <span><i class="fa fa-shield-alt"></i> বর্তমান স্কোয়াড</span>
                <button class="btn-custom" style="padding: 4px 10px; font-size: 0.75rem;" onclick="document.getElementById('playerUpload').click()">+ প্লেয়ার</button>
                <input type="file" id="playerUpload" accept="image/*" onchange="addPlayer(event, 'current')">
            </h2>
            <div class="grid-container" id="currentSquadGrid">
                <!-- Sample Player -->
                <div class="player-card">
                    <button class="delete-btn" onclick="this.parentElement.remove()">&times;</button>
                    <img src="65951.jpg" class="player-img" alt="Player">
                    <div class="player-number">17</div>
                </div>
            </div>
        </section>

        <!-- Legendary Players -->
        <section>
            <h2 class="section-title">
                <span><i class="fa fa-star text-warning"></i> সম্মানীয় লিজেন্ড</span>
                <button class="btn-custom" style="padding: 4px 10px; font-size: 0.75rem; background: var(--gold); color: #000;" onclick="document.getElementById('legendUpload').click()">+ লিজেন্ড</button>
                <input type="file" id="legendUpload" accept="image/*" onchange="addPlayer(event, 'legend')">
            </h2>
            <div class="grid-container" id="legendSquadGrid">
                <!-- Sample Legend -->
                <div class="player-card legend-card">
                    <button class="delete-btn" onclick="this.parentElement.remove()">&times;</button>
                    <img src="65951.jpg" class="player-img" alt="Legend">
                    <div class="player-number">10</div>
                </div>
            </div>
        </section>

        <!-- Trophy Cabinet -->
        <section>
            <h2 class="section-title"><span><i class="fa fa-trophy"></i> ট্রফি ক্যাবিনেট</span></h2>
            <div style="text-align: center; padding: 10px; font-weight: 600; color: #555;">
                🏆 চ্যাম্পিয়ন - করড়া টুর্নামেন্ট (২০২৫)
            </div>
        </section>

        <!-- Location & Contact Info -->
        <section>
            <h2 class="section-title"><span><i class="fa fa-map-marker-alt"></i> লোকেশন ও যোগাযোগ</span></h2>
            <div class="info-box">
                <p><i class="fa fa-map-pin"></i> **ঠিকানা:** কররা দক্ষিণপাড়া, আজিম নগর ইউনিয়ন, ভাঙ্গা, ফরিদপুর।</p>
                <p style="margin-top: 8px;"><i class="fa fa-phone-alt"></i> **মোবাইল:** ০১৭০০-০০০০০০</p>
            </div>
        </section>

    </div>

    <script>
        // Banner Slider Logic
        let slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        function nextSlide() {
            slides = document.querySelectorAll('.slide');
            if(slides.length === 0) return;
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }
        setInterval(nextSlide, 4000);

        function addBanner(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const sliderContainer = document.getElementById('sliderContainer');
                    slides.forEach(s => s.classList.remove('active'));
                    
                    const newDiv = document.createElement('div');
                    newDiv.classList.add('slide', 'active');
                    newDiv.innerHTML = `<img src="${e.target.result}" alt="Banner">`;
                    sliderContainer.appendChild(newDiv);
                    slides = document.querySelectorAll('.slide');
                    currentSlide = slides.length - 1;
                }
                reader.readAsDataURL(file);
            }
        }

        // Add Player / Legend Logic
        function addPlayer(event, type) {
            const file = event.target.files[0];
            if (file) {
                let jerseyNum = prompt("খেলোয়াড়ের জার্সি নম্বর দিন:", "৭");
                if(jerseyNum === null) return;

                const reader = new FileReader();
                reader.onload = function(e) {
                    const gridId = type === 'current' ? 'currentSquadGrid' : 'legendSquadGrid';
                    const cardClass = type === 'current' ? 'player-card' : 'player-card legend-card';
                    
                    const grid = document.getElementById(gridId);
                    const card = document.createElement('div');
                    card.className = cardClass;
                    card.innerHTML = `
                        <button class="delete-btn" onclick="this.parentElement.remove()">&times;</button>
                        <img src="${e.target.result}" class="player-img" alt="Player">
                        <div class="player-number">${jerseyNum}</div>
                    `;
                    grid.appendChild(card);
                }
                reader.readAsDataURL(file);
            }
        }
    </script>
</body>
</html>
