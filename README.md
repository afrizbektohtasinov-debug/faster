<!DOCTYPE html>
<html lang="uz">

<head>
    <meta charset="UTF-8">
    <title>Malikaga Sevgi</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            font-family: 'Segoe UI', sans-serif;
        }

        h1 {
            font-size: 60px;
            color: #fff;
            text-shadow: 0 0 15px #ff0055, 0 0 30px #ff3399;
            animation: glow 2s infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 15px #ff0055;
            }

            to {
                text-shadow: 0 0 30px #ff66aa, 0 0 50px #ff99cc;
            }
        }

        p {
            font-size: 22px;
            color: #fff;
            margin-top: 20px;
            text-align: center;
            width: 80%;
            line-height: 1.5em;
        }

        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background: red;
            transform: rotate(45deg);
            animation: floatUp 6s linear infinite;
            opacity: 0.7;
        }

        .heart::before,
        .heart::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: red;
            border-radius: 50%;
        }

        .heart::before {
            top: -10px;
            left: 0;
        }

        .heart::after {
            left: -10px;
            top: 0;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(45deg);
                opacity: 1;
            }

            100% {
                transform: translateY(-800px) rotate(45deg);
                opacity: 0;
            }
        }
    </style>
</head>

<body>

    <h1>💖 Malika 💖</h1>

    <p>
        Sen mening orzularim yulduzi,<br>
        Dilimdagi eng go‘zal qo‘shiq so‘zi.<br>
        Har bir nafasimda sening isming,<br>
        Malika, sen – sevgi quvonchim!
    </p>

    <script>
        // Yurakchalar hosil qilish
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.style.left = Math.random() * window.innerWidth + 'px';
            heart.style.top = window.innerHeight + 'px';
            heart.style.animationDuration = (3 + Math.random() * 3) + 's';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 6000);
        }
        setInterval(createHeart, 300);
    </script>

</body>

</html># faster
