<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mustafa Kayacıoğlu | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --neon-mor: #9d00ff;
            --mor-efekt: #d400ff;
            --siyah: #0a0a0a;
            --koyu-mor: #2a0a35;
            --text-renk: #ffffff;
        }

        body {
            background: var(--siyah);
            color: var(--text-renk);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        header {
            text-align: center;
            margin-bottom: 3rem;
            padding: 8rem 2rem 4rem; /* Extend the height */
            border-radius: 15px;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, 
                var(--neon-mor) 0%, 
                var(--mor-efekt) 50%, 
                var(--neon-mor) 100%);
            opacity: 0.3;
            z-index: -1;
        }

        header h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 0 0 10px var(--mor-efekt);
            background: linear-gradient(45deg, #ff00ff, #9d00ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: -120px auto 2rem; /* Adjust margin */
            border: 3px solid var(--neon-mor);
            box-shadow: 0 0 30px var(--mor-efekt);
            position: relative;
            overflow: hidden;
            background-image: url('https://media.licdn.com/dms/image/v2/D4E03AQHJkgRSXF_zIw/profile-displayphoto-shrink_400_400/0/1720232201715?e=1744848000&v=beta&t=WIXDyHyrFUAjrO4D6VvGE_cp-lYWjwqJK7tPS83w1KA');
            background-size: cover;
            background-position: center;
        }

        section {
            background: rgba(157, 0, 255, 0.05);
            padding: 2rem;
            margin-bottom: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(157, 0, 255, 0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 30px rgba(157, 0, 255, 0.2);
        }

        h2 {
            color: var(--neon-mor);
            margin-bottom: 1.5rem;
            font-size: 2.2rem;
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--mor-efekt);
            box-shadow: 0 0 10px var(--mor-efekt);
        }

        .yetenekler ul {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            list-style: none;
        }

        .yetenekler li {
            background: var(--koyu-mor);
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            border: 1px solid var(--neon-mor);
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .yetenekler li:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 30px rgba(157, 0, 255, 0.2);
        }

        .badge {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .badge img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
        }

        .projeler ul {
            list-style: none;
        }

        .projeler li {
            margin-bottom: 1.5rem;
            padding: 1.5rem;
            background: rgba(157, 0, 255, 0.1);
            border-radius: 10px;
            border: 1px solid rgba(157, 0, 255, 0.3);
            transition: all 0.3s ease;
        }

        .projeler li:hover {
            background: rgba(157, 0, 255, 0.2);
        }

        .projeler a {
            color: var(--text-renk);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 1rem;
            font-size: 1.1rem;
        }

        .projeler i {
            color: var(--neon-mor);
            font-size: 1.5rem;
        }

        .egitim {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .egitim-item {
            display: flex;
            align-items: center;
            gap: 1.5rem;
            background: rgba(157, 0, 255, 0.05);
            padding: 1.5rem;
            border-radius: 10px;
            border: 1px solid rgba(157, 0, 255, 0.2);
        }

        .egitim-item img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            border: 2px solid var(--neon-mor);
            box-shadow: 0 0 10px var (--mor-efekt);
        }

        .egitim-item h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .egitim-item p {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.8);
        }

        .diller {
            margin-top: 1.5rem;
        }

        .diller ul {
            list-style: none;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .diller li {
            background: rgba(157, 0, 255, 0.1);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            border: 1px solid rgba(157, 0, 255, 0.3);
            font-size: 0.9rem;
        }

        .yazilim-dilleri {
            margin-top: 1.5rem;
        }

        .yazilim-dilleri ul {
            list-style: none;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .yazilim-dilleri li {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(157, 0, 255, 0.1);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            border: 1px solid rgba(157, 0, 255, 0.3);
            font-size: 0.9rem;
        }

        .yazilim-dilleri img {
            width: 20px;
            height: 20px;
        }

        .iletisim {
            background: rgba(157, 0, 255, 0.05);
            padding: 2rem;
            margin-bottom: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(157, 0, 255, 0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            text-align: left;
        }

        .iletisim h2 {
            color: var(--neon-mor);
            margin-bottom: 1.5rem;
            font-size: 2.2rem;
            position: relative;
            display: inline-block;
        }

        .iletisim h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--mor-efekt);
            box-shadow: 0 0 10px var(--mor-efekt);
        }

        .iletisim p {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            font-size: 1.1rem;
        }

        .iletisim p i {
            margin-right: 10px;
            color: var(--neon-mor);
            font-size: 1.5rem;
        }

        .iletisim a {
            color: var(--text-renk);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .iletisim a:hover {
            color: var(--mor-efekt);
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            header h1 {
                font-size: 2.5rem;
            }
            
            .profile-img {
                width: 120px;
                height: 120px;
                margin-top: -80px; /* Adjust margin for mobile */            }

            .egitim-item {
                flex-direction: column;
                text-align: center;
            }

            .iletisim {
                text-align: center;
            }

            .iletisim p {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-img" style="background-image: url('https://media.licdn.com/dms/image/v2/D4E03AQHJkgRSXF_zIw/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1720232201715?e=1744848000&v=beta&t=WIXDyHyrFUAjrO4D6VvGE_cp-lYWjwqJK7tPS83w1KA');"></div>
            <h1>Mustafa Kayacıoğlu</h1>
            <p>Full Stack Geliştirici</p>
        </header>
        
        <section class="hakkimda">
            <h2>Hakkımda</h2>
            <p>Merhaba, ben Mustafa Kayacıoğlu. Yazılım geliştirme ve web tasarımı alanında kendimi geliştirmekteyim. AppTasarım.com.tr'nin kurucusuyum ve bireyler ile şirketler için yenilikçi ve etkileyici dijital çözümler sunmaktayız.</p>


        </section>

        <section class="yetenekler">
            <h2>Yetenekler</h2>
            <ul>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968292.png" alt="JavaScript"></span>JavaScript</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/919/919825.png" alt="Node.js"></span>Node.js</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968350.png" alt="Python"></span>Python</li>
                <li><span class="badge"><img src="https://go.dev/blog/go-brand/Go-Logo/SVG/Go-Logo_Aqua.svg" alt="Go"></span>Go</li>
                <li><span class="badge"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Arduino_Logo.svg/1080px-Arduino_Logo.svg.png?20200922062315" alt="Arduino"></span>Arduino</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968332.png" alt="PHP"></span>PHP</li>
                <li><span class="badge"><img src="https://img.icons8.com/?size=48&id=13443&format=png" alt="Raspberry Pi"></span>Raspberry Pi</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968267.png" alt="HTML5"></span>HTML5</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968242.png" alt="CSS3"></span>CSS3</li>
                <li><span class="badge"><img src="https://www.vectorlogo.zone/logos/cloudflare/cloudflare-icon.svg" alt="Cloudflare"></span>Cloudflare</li>
                <li><span class="badge"><img src="https://www.svgrepo.com/show/448266/aws.svg" alt="AWS"></span>AWS</li>
                <li><span class="badge"><img src="https://img.icons8.com/?size=80&id=9Gfx4Dfxl0JK&format=png" alt="Express.js"></span>Express.js</li>
                <li><span class="badge"><img src="https://www.svgrepo.com/show/354128/npm.svg" alt="NPM"></span>NPM</li>
                <li><span class="badge"><img src="https://img.icons8.com/color/512/vue-js.png" alt="Vue.js"></span>Vue.js</li>
                <li><span class="badge"><img src="https://www.vectorlogo.zone/logos/sequelizejs/sequelizejs-icon.svg" alt="Sequelize"></span>Sequelize</li>
                <li><span class="badge"><img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="SQLite"></span>SQLite</li>
                <li><span class="badge"><img src="https://www.svgrepo.com/show/331488/mongodb.svg" alt="MongoDB"></span>MongoDB</li>
                <li><span class="badge"><img src="https://www.vectorlogo.zone/logos/mysql/mysql-official.svg" alt="MySQL"></span>MySQL</li>
                <li><span class="badge"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968520.png" alt="Adobe Photoshop"></span>Adobe Photoshop</li>
            </ul>

            <div class="diller">
                <h3>Diller</h3>
                <ul>
                    <li>Türkçe (Ana Dil)</li>
                    <li>İngilizce (Orta Seviye)</li>
                </ul>
            </div>
        </section>

        <section class="projeler">
            <h2>Projeler</h2>
            <ul>
                <li>
                    <a href="https://github.com/Iahmacun/FilmVeSohbet">
                        <i class="fas fa-rocket"></i>
                        <span>Film ve Sohbet Uygulaması</span>
                    </a>
                </li>
                <li>
                    <a href="https://github.com/Iahmacun/HATAP-HastaTakipProgrami-HBYS-">
                        <i class="fas fa-robot"></i>
                        <span>HATAP - Hasta Takip Programı (HBYS)</span>
                    </a>
                </li>
            </ul>
        </section>

        <section class="egitim">
            <h2>Eğitim</h2>
            <div class="egitim-item">
                <img src="data:image/jpeg;base64,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" alt="Kapadokya Üniversitesi">
                <div>
                    <h3>Yönetim Bilişim Sistemleri</h3>
                    <p>2024-Başlangıç (Devam Ediyor)</p>
                </div>
            </div>
            <div class="egitim-item">
                <img src="data:image/jpeg;base64,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" alt="Anadolu Üniversitesi">
                <div>
                    <h3>Bilgisayar Programcılığı</h3>
                    <p>Anadolu Üniversitesi</p>
                </div>
            </div>
        </section>

        <section class="iletisim">
            <h2>İletişim</h2>
            <p>
                <i class="fas fa-envelope"></i>
                <a href="mailto:mustafa@example.com">mustafa@example.com</a>
            </p>
            <p>
                <i class="fab fa-linkedin"></i>
                <a href="https://www.linkedin.com/in/mustafa-kayac%C4%B1o%C4%9Flu/">linkedin.com/in/mustafa-kayacıoğlu</a>
            </p>
            <p>
                <i class="fab fa-github"></i>
                <a href="https://github.com/Iahmacun">github.com/Iahmacun</a>
            </p>
            <p>
                <i class="fas fa-globe"></i>
                <a href="https://apptasarım.com.tr">apptasarım.com.tr</a>
            </p>
        </section>
    </div>
</body>
</html>
