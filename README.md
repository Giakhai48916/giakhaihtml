                #ff0000, #ff7f00, #ffff00, #00ff00, 
                #00ffff, #0000ff, #8b00ff, #ff0000);
            background-size: 400% 400%;
            animation: rainbowShift 15s linear infinite;/* ====================== HÌNH NỀN GALAXY LẤP LÁNH ====================== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    background: radial-gradient(circle at center, #0a001f 0%, #000011 60%, #000000 100%);
    position: relative;
    overflow: hidden;
    font-family: Arial, sans-serif;
    color: #ffffff;
}

/* Layer 1: Dải màu quang phổ (rainbow) nhẹ nhàng chuyển động */
.galaxy-rainbow {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, 
        #ff0080, #ff00ff, #8000ff, #0080ff, 
        #00ffff, #00ff80, #80ff00, #ffff00, #ff8000, #ff0080);
    background-size: 500% 500%;
    animation: rainbowMove 25s linear infinite;
    opacity: 0.18;
    mix-blend-mode: screen;
    z-index: -3;
}

@keyframes rainbowMove {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

/* Layer 2: Các ngôi sao lấp lánh (twinkling) */
.stars {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: transparent;
    box-shadow: 
        50px 80px 2px #fff,
        180px 150px 1px #fff,
        320px 90px 2px #fff,
        480px 380px 1px #fff,
        650px 120px 2px #fff,
        820px 450px 1px #fff,
        950px 200px 2px #fff,
        1100px 320px 1px #fff,
        120px 520px 2px #fff,
        750px 580px 1px #fff,
        280px 680px 2px #fff,
        1050px 80px 1px #fff,
        420px 620px 2px #fff,
        1250px 410px 1px #fff,
        30px 350px 2px #fff,
        600px 250px 1px #fff;
    animation: twinkle 4s infinite alternate ease-in-out;
    z-index: -2;
    opacity: 0.85;
}

.stars2 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    box-shadow: 
        90px 280px 3px rgba(220,255,255,0.9),
        260px 480px 2px rgba(255,220,255,0.8),
        520px 140px 3px rgba(255,255,200,0.9),
        710px 520px 2px rgba(200,255,255,0.8),
        980px 260px 3px rgba(255,200,255,0.9),
        1150px 610px 2px rgba(220,255,220,0.8),
        150px 650px 3px rgba(255,255,255,0.9);
    animation: twinkle 7s infinite alternate ease-in-out;
    z-index: -2;
    opacity: 0.7;
}

@keyframes twinkle {
    0%   { opacity: 0.5; }
    100% { opacity: 1; }
}

/* Layer 3: Điểm sáng nhỏ hơn, dày đặc hơn (tăng cảm giác galaxy) */
.stars3 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, rgba(255,255,255,0.9) 1px, transparent 1px);
    background-size: 80px 80px;
    opacity: 0.25;
    animation: twinkle 3s infinite alternate;
    z-index: -2;
}

/* Đảm bảo nội dung của bạn nằm trên nền */
table, h1, h2, h3, ul, a {
    position: relative;
    z-index: 10;
}

/* Tăng độ tương phản cho chữ nếu cần */
h1, h2, h3 {
    text-shadow: 0 0 15px rgba(255, 255, 255, 0.7);
}
            opacity: 0.25;
            mix-blend-mode: screen;
        }

        /* Hiệu ứng lấp lánh sparkle (nhiều lớp sao nhỏ nhấp nháy) */
        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: transparent;
            box-shadow: 
                /* Nhiều điểm sáng nhỏ ngẫu nhiên */
                50px 80px 2px #fff,
                150px 200px 1px #fff,
                300px 120px 2px #fff,
                450px 350px 1px #fff,
                600px 80px 2px #fff,
                750px 450px 1px #fff,
                900px 150px 2px #fff,
                1200px 300px 1px #fff,
                200px 500px 2px #fff,
                800px 600px 1px #fff,
                100px 700px 2px #fff,
                1100px 50px 1px #fff,
                400px 650px 2px #fff,
                1300px 400px 1px #fff;
            animation: twinkle 4s infinite alternate ease-in-out;
        }

        /* Layer thứ 2 sparkle chậm hơn, màu galaxy hơn */
        .stars2 {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            box-shadow: 
                80px 300px 3px rgba(255,255,255,0.9),
                250px 450px 2px rgba(200,255,255,0.8),
                500px 150px 3px rgba(255,200,255,0.9),
                700px 500px 2px rgba(255,255,200,0.8),
                950px 250px 3px rgba(200,255,255,0.9),
                1100px 600px 2px rgba(255,200,255,0.8);
            animation: twinkle 6s infinite alternate ease-in-out;
            opacity: 0.7;
        }

        @keyframes rainbowShift {
            0%   { background-position: 0% 50%; }
            50%  { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes twinkle {
            0%   { opacity: 0.4; }
            100% { opacity: 1; }
        }

        /* Nội dung ở giữa (bạn có thể thay bằng text hoặc gì cũng được) */
        .content {
            position: relative;
            z-index: 10;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            text-shadow: 0 0 20px rgba(255,255,255,0.8);
        }
    </style>
</head>
<body>

    <div class="galaxy"></div>
    <div class="stars"></div>
    <div class="stars2"></div>

    <div class="content">
        <h1>Dãy Màu Quang Phổ Lấp Lánh Như Galaxy ✨</h1>
        <p>Code này chạy mượt trên mọi trình duyệt</p>
    </div>

</body>
</html>
