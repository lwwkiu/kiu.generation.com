# kiu.generation.com
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
    <style>
        * {
            font-family: 'Libre Baskerville', serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body,
        html {
            height: 100%;
            font-family: 'Libre Baskerville', serif;
        }
        
        .background {
            position: relative;
            height: 100%;
            background: url('https://asiamountains.net/assets/cache_image/assets/lib/resized/308/1600x1066_0x0_d0b.jpg') no-repeat center center/cover;
        }
        
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(3px);
            z-index: 1;
        }
        
        header {
            position: absolute;
            top: 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            z-index: 2;
        }
        
        header .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            color: white;
        }
        
        header .logo img {
            height: 55px;
            width: 55px;
        }
        
        header nav a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            font-size: 24px;
        }
        
        header nav a:hover {
            color: #32b544;
            text-decoration: underline;
        }
        /* Контейнер для выпадающего меню */
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        /* Выпадающее меню */
        
        .dropdown-menu {
            display: none;
            position: absolute;
            top: 100%;
            left: 0;
            background-color: white;
            padding: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 10;
            border-radius: 5px;
        }
        /* Кнопки внутри выпадающего меню */
        
        .dropdown-menu .btn {
            display: block;
            margin: 5px 0;
            padding: 10px 35px;
            text-decoration: none;
            background-color: #1e6c29;
            color: white;
            border-radius: 5px;
            text-align: center;
            font-size: 16px;
        }
        /* Эффект наведения на кнопки */
        
        .dropdown-menu .btn:hover {
            background-color: #32b544;
        }
        /* Показываем меню при наведении на ссылку */
        
        .dropdown:hover .dropdown-menu {
            display: block;
        }
        
        main {
            position: relative;
            z-index: 2;
            text-align: center;
            color: white;
            top: 50%;
            transform: translateY(-50%);
        }
        
        h1 {
            font-size: 48px;
        }
        
        p {
            font-size: 24px;
        }
        
        .content-container {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            text-align: center;
            padding: 30px;
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            display: none;
        }
        
        .content {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .content img {
            max-width: 40%;
            margin-right: 20px;
            border-radius: 10px;
        }
        
        .content .description {
            max-width: 50%;
        }
        
        .back-btn {
            margin-top: 20px;
        }
        
        .btn {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #1e6c29;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-size: 18px;
        }
        
        .text-and-images-container {
            margin: 80px auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
        }
        
        .text-left {
            color: white;
            text-align: center;
            font-size: 20px;
            max-width: 800px;
        }
        
        .container {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 30px;
        }
        
        .container-title {
            font-size: 48px;
            color: rgb(26, 79, 28);
            /* Цвет заголовка */
            margin-bottom: 20px;
            /* Отступ под заголовком */
            text-align: center;
            width: 100%;
            margin-top: -10%;
        }
        
        .photo-container {
            width: 300px;
            height: 400px;
            text-align: center;
            background-color: #fff;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            margin-bottom: 30px;
            margin-top: -60px;
        }
        
        .photo-container:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
        }
        
        .photo-container img {
            width: 100%;
            height: 300px;
            transition: box-shadow 0.3s;
            object-fit: fill;
        }
        
        .photo-container img:hover {
            box-shadow: 0 0 0 10px rgba(50, 181, 67, 0.737);
        }
        
        .photo-container p {
            padding: 10px;
            font-size: 24px;
            color: #185119;
        }
        
        .bottom-section {
            background-color: #012207ec;
            padding: 50px 20px;
        }
        
        .bottom-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-between;
            align-items: center;
        }
        
        .rect-container {
            position: relative;
            width: 300px;
            height: 500px;
            background-color: #1d8734;
            margin-bottom: 20%;
        }
        
        .rect-container img {
            position: absolute;
            top: 60px;
            left: 80px;
            width: 500px;
            height: 300px;
            object-fit: cover;
        }
        
        .text-right {
            flex: 1;
            font-size: 12px;
            margin-top: 25%;
            color: #eaeaea;
        }
        
        .text-right h2 {
            font-size: 30px;
            margin-bottom: 10px;
            margin-left: 20%;
            color: #24d146;
        }
        
        .text-below {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: flex-start;
            align-items: center;
            margin-top: 20px;
            color: #6be583;
            /* Ограничивает ширину текста */
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            font-size: 14px;
        }
        
        .text-below img {
            width: 500px;
            height: 500px;
            object-fit: cover;
        }
        
        .collage {
            display: grid;
            grid-template-rows: repeat(2, 1fr);
            grid-template-columns: repeat(4, 1fr);
            width: 100%;
            height: 500px;
            gap: 0;
        }
        
        .collage .large-img {
            grid-row: span 2;
            grid-column: span 2;
            background-image: url('https://balthazar.club/uploads/posts/2023-01/1674371371_balthazar-club-p-kartinki-estetika-puteshestvie-vkontakte-1.jpg');
            background-size: cover;
            background-position: center;
        }
        
        .collage .small-img {
            background-size: cover;
            background-position: center;
        }
        
        .collage .img1 {
            background-image: url('https://scontent.ffru4-1.fna.fbcdn.net/v/t39.30808-6/292449043_5213150065387013_49415713687159736_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=127cfc&_nc_ohc=_urwY7RKt24Q7kNvgGOvJTs&_nc_zt=23&_nc_ht=scontent.ffru4-1.fna&_nc_gid=AIzTBpNev8K_PwHtQVJRjZ8&oh=00_AYDxZUdVxpHAlsd72t1IHa9IUSmvABebtfDcOdAZcnbJYA&oe=6760B2B2');
        }
        
        .collage .img2 {
            background-image: url("C:/Users/Lenovo/OneDrive/Resimler/Снимки экрана/Снимок экрана 2024-12-14 190040.png");
        }
        
        .collage .img3 {
            background-image: url("C:/Users/Lenovo/OneDrive/Resimler/Снимки экрана/Снимок экрана 2024-12-14 190452.png");
        }
        
        .collage .img4 {
            background-image: url('https://gdb.rferl.org/777c4431-c718-4090-81fc-121ef37fdc14_cx0_cy2_cw0_w1200_r1.jpg');
        }
        
        footer {
            background-color: #1e6c29;
            color: white;
            text-align: center;
            padding: 15px;
        }
        
        .popup {
            position: absolute;
            background-color: white;
            color: rgb(5, 46, 14);
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            display: none;
            z-index: 10;
            max-width: 200px;
            font-size: 18px;
        }
    </style>
</head>

<body>
    <div class="background">
        <div class="overlay"></div>
        <header>
            <div class="logo img">
                <img src="c:\Users\Lenovo\OneDrive\Resimler\free-png.ru-352.png" alt="Логотип">
                <p>Welcome!</p>
            </div>
            <nav>
                <a href="big pr.html">Home</a>
                <a href="big.about.html">About us</a>
                <div class="dropdown">
                    <a href="big.dost.html" class="dropdown-link">Tours</a>
                    <div class="dropdown-menu">
                        <a href="big.dost.html" class="btn">Tour 1</a>
                        <a href="big past 2.html" class="btn">Tour 2</a>
                    </div>
                </div>
                <a href="big.cont.html">Contacts</a>
            </nav>

        </header>
        <main id="mainContent">
            <h1>Let's plan the journey of your dreams together!</h1>
            <p>Explore the world with our company KiU Generation</p>
            <a href="javascript:void(0);" class="btn" onclick="showContent()">Learn more</a>
        </main>
    </div>

    <div class="text-and-images-container">
        <div class="text-left">
            <p>Чуйская область — это одно из самых живописных мест, расположенных в северной части Кыргызстана. Она известна своими красивыми горами, реками и долинами. Путешествуя по Чуйской области, можно насладиться красивыми пейзажами и узнать много
                интересных историй.</p>
        </div>
    </div>

    <div id="info" class="content-container">
        <div class="content">
            <img src="https://sdc-eu.info/2-kg/images/5-0003.png" alt="Фото">
            <div class="description">
                <h2>Chui Region</h2>
                <p>The Chui region is located in the northern part of Kyrgyzstan. It borders Kazakhstan to the north and west, the Talas and Jalal-Abad regions to the southwest, and the Issyk-Kul region to the southeast. The Chui region consists of several
                    districts: Chon-Kemin, Kichi-Kemin, the Suusamyr Valley, the slopes of the Kyrgyz Ala-Too, and the Kungey Ala-Too. The lowest point of the valley is at 550 meters above sea level, and the highest point is at 4,895 meters. The city
                    of Bishkek (the capital of Kyrgyzstan) is located in the northern part of the Chui region. The Chui region is not only known for its beautiful landscapes but also for its historical sites that will interest every tourist.</p>
            </div>
        </div>
        <a href="javascript:void(0);" class="btn back-btn" onclick="hideContent()">Close</a>
    </div>

    <div class="container">
        <h2 class="container-title">The attractions of the city of Tokmok.</h2>
        <!-- Добавлен класс для заголовка -->
        <div class="photo-container" data-description="The Chuy Valley is one of the most fertile and picturesque places in Kyrgyzstan, surrounded by mountains and green meadows. The Chu River flows here, providing water for agriculture and giving the landscape a unique appearance.">
            <img src="https://ybis.ru/wp-content/uploads/2023/09/chuiskaia-dolina-kirgiziia-1-1.webp" alt="Фото 1">
            <p>The Chuy Valley</p>
        </div>
        <div class="photo-container" data-description="The Ketmen-Tube mountain range is located in the eastern part of the Chuy region. It is known for its breathtaking views, clean air, and unique flora and fauna, making it popular among tourists and mountaineers.

        ">
            <img src="https://чунджа.kz/image/img-4b44ymf97" alt="Фото 2">
            <p>The Ketmen-Tube Mountains</p>
        </div>
        <div class="photo-container" data-description="The Chu River flows through the Chuy region and holds significant importance for the area. It is an ideal spot for fishing, outdoor recreation, and photography due to its clear water and picturesque shores.

        ">
            <img src="https://oreke.ru/wp-content/uploads/2023/03/reka-CHu-Kazahstan.jpg" alt="Фото 3">
            <p>The Chu River</p>
        </div>
        <div class="photo-container" data-description="The Burana Tower is an ancient architectural monument built in the 10th-11th centuries. It is part of the ruins of the city of Balasagun, once an important center on the Silk Road. Today, the Burana Tower is a symbol of Kyrgyzstan's historical heritage.">
            <img src="https://concept.kg/media/redactor/10_Iqw2Ngt.jpg" alt="Фото 4">
            <p>Burana Tower</p>
        </div>

    </div>

    <div class="bottom-section">
        <div class="bottom-content">
            <div class="rect-container">
                <img src="https://e-cis.info/upload/iblock/908/d4i3x2ff324fkye2rkxx0mou0divragg.png" alt="Фото">
            </div>
            <div class="text-right">
                <h2>Tokmok city</h2>
                <p>Tokmok is a small yet significant city in the Chuy region of Kyrgyzstan, located approximately 60 km east of Bishkek, on the banks of the Chu River. The city has a rich history, being close to the ruins of the ancient city of Balasagun
                    and the famous Burana Tower. Today, Tokmok is an important industrial and agricultural center in the region. Surrounded by the picturesque plains of the Chuy Valley and mountain ranges, the city attracts tourists with its culture,
                    natural beauty, and peaceful atmosphere.
                </p>
            </div>
            <div class="text-below">
                <img src="https://trikky.ru/wp-content/blogs.dir/1/files/2019/05/30/6063889_xlarge.jpg" alt="Фото ниже">
                <p>A journey through Kyrgyzstan.</p>
            </div>
        </div>
    </div>

    <div class="collage">
        <div class="large-img"></div>
        <div class="small-img img1"></div>
        <div class="small-img img2"></div>
        <div class="small-img img3"></div>
        <div class="small-img img4"></div>
    </div>

    <footer>
        <p>&copy; 2024 Kyrgyzstan Guide. All rights reserved.</p>
    </footer>

    <script>
        function showContent() {
            document.getElementById('mainContent').style.display = 'none';
            document.getElementById('info').style.display = 'block';
        }

        function hideContent() {
            document.getElementById('mainContent').style.display = 'block';
            document.getElementById('info').style.display = 'none';
        }
        document.addEventListener('DOMContentLoaded', () => {
            const photoContainers = document.querySelectorAll('.photo-container');
            const popup = document.createElement('div');
            popup.classList.add('popup');
            document.body.appendChild(popup);

            photoContainers.forEach(card => {
                card.addEventListener('click', (e) => {
                    const description = card.getAttribute('data-description');
                    const rect = card.getBoundingClientRect();

                    popup.textContent = description;
                    popup.style.display = 'block';
                    popup.style.left = `${rect.left + window.scrollX + rect.width / 2 - popup.offsetWidth / 2}px`;
                    popup.style.top = `${rect.top + window.scrollY - popup.offsetHeight - 10}px`;
                });
            });

            document.addEventListener('click', (e) => {
                if (!e.target.closest('.photo-container')) {
                    popup.style.display = 'none';
                }
            });
        });
    </script>
</body>

</html>
