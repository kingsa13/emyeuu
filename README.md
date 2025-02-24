# emyeuu
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang Tình Yêu</title>
    <style>
        body {
            background-color: #ffebf2;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
            margin: 0;
        }
        h1 {
            color: #ff4081;
            font-size: 40px;
            margin-top: 100px;
        }
        .message {
            font-size: 24px;
            color: #d81b60;
            display: none;
            margin-top: 20px;
        }
        button {
            background-color: #ff4081;
            color: white;
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 30px;
        }
        button:hover {
            background-color: #d81b60;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 30px;
            animation: float 5s infinite;
        }
        @keyframes float {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            50% { transform: translateY(-300px) scale(1.5); opacity: 0.6; }
            100% { transform: translateY(-600px) scale(2); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Chào em yêu! ❤️</h1>
    <button onclick="showMessage()">Nhấn vào đây để xem lời nhắn</button>
    <p class="message">Anh yêu em rất nhiều! 💖</p>

    <script>
        function showMessage() {
            document.querySelector('.message').style.display = 'block';
        }

        // Tạo trái tim bay lên
        function createHeart() {
            let heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            document.body.appendChild(heart);

            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.top = '100vh';
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's';

            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        setInterval(createHeart, 500);
    </script>
</body>
</html>
