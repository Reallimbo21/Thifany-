<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thifany</title>
    <style>
        body {
            background-color: pink;
            text-align: center;
            font-family: Arial, sans-serif;
            color: white;
        }
        h1 {
            font-size: 50px;
            margin-top: 50px;
            text-shadow: 2px 2px 5px red;
        }
        .hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            overflow: hidden;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 30px;
            animation: float 5s linear infinite;
        }
        @keyframes float {
            from { transform: translateY(100vh); opacity: 1; }
            to { transform: translateY(-10vh); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Thifany ❤️</h1>
    <div class="hearts">
        <!-- Corações animados -->
        <script>
            function createHeart() {
                const heart = document.createElement("div");
                heart.classList.add("heart");
                heart.innerHTML = "❤️";
                heart.style.left = Math.random() * 100 + "vw";
                heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
                document.querySelector(".hearts").appendChild(heart);
                setTimeout(() => heart.remove(), 5000);
            }
            setInterval(createHeart, 300);
        </script>
    </div>
</body>
</html>
