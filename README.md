<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dãy Màu Quang Phổ Lấp Lánh Galaxy</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            height: 100vh;
            overflow: hidden;
            background: radial-gradient(circle at center, #0a001f 0%, #000000 70%);
            position: relative;
        }

        /* Nền galaxy + rainbow spectrum chuyển động */
        .galaxy {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, 
                #ff0000, #ff7f00, #ffff00, #00ff00, 
                #00ffff, #0000ff, #8b00ff, #ff0000);
            background-size: 400% 400%;
            animation: rainbowShift 15s linear infinite;
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
