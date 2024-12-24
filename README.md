# Jos20006-beep.githup.io
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun!</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #d50000;
            text-align: center;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        h1 {
            color: #f8399f;
            font-size: 3em;
            margin-bottom: 20px;
        }

        .message-options button {
            margin: 10px;
            padding: 15px 30px;
            font-size: 1.2em;
            background-color: #032cf7;
            color: rgb(38, 211, 223);
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .message-options button:hover {
            transform: scale(1.1);
        }

        .selected-message {
            font-size: 1.5em;
            color: #0a0908;
            margin-top: 20px;
            opacity: 0;
            animation: fadeIn 1s forwards;
        }

        .animation-container {
            position: relative;
            margin-top: 30px;
            display: none;
        }

        .balloon {
            font-size: 3em;
            animation: float 4s infinite ease-in-out;
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        .heart  {
            front-size: 4em;
            animation: pop 3s alternate-reverse;
            position:absolute;
            top: 0%;
            left: 50%;
            transform: translateX(-50%);
        }
        .confetti {
            font-size: 2em;
            animation: pop 5s ease-in-out;
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
        }

      .cake {
          font-size: 5em;
          animation: pop 1s forwards;
          position:absolute;
          top: 0%;
          left: 50%;
          transform: translateX(-50%);
      }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-30px); }
            100% { transform: translateY(0); }
        }

        @keyframes pop {
            0% { transform: scale(1); opacity: 1; }
            100% { transform: scale(2); opacity: 0; }
        }

        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>

    <h1>🎉 Selamat Ulang Tahun! 🎂</h1>

    <div class="message-options">
        <button onclick="showMessage('Selamat ulang tahun! Semoga tahun ini kamu lebih sering tertawa, biar dunia lebih cerah! 🎉')">Pilihan 1</button>
        <button onclick="showMessage('Para bintang ucapin ulang tahun tuh,karena sang perinya lagi bertambah umur😂')">Pilihan 2</button>
        <button onclick="showMessage('Happy birthday!,ingat jangan terlalu manis.. ntar kopiku jadi tambah manis nihh😩')">Pilihan 3</button>
        <button onclick="showMessage('Ulang tahunmu bikin aku mikir, kapan ya aku bisa jadi pemenang di hatimu? 💖')">Pilihan 4</button>
        <button onclick="showMessage('Ulang tahun ini lagi mikirin apa??,umur atau taro tuhh🤔')">pilihsn 5</button>
    </div>

    <p id="selected-message" class="selected-message"></p>

    <div id="animation-container" class="animation-container">
        <div class="balloon">🎈</div>
        <div class="heart">💖🌸</div>
        <div class="confetti">🎊🎉✨</div>
        <div class="cake">🎂</div>
    </div>

    <script>
        function showMessage(message) {
            // Menampilkan pesan lucu
            const messageElement = document.getElementById('selected-message');
            messageElement.textContent = message;

            // Menampilkan animasi
            const animationContainer = document.getElementById('animation-container');
            animationContainer.style.display = 'block';

            // Menghilangkan animasi setelah 10 detik
            setTimeout(function() {
                animationContainer.style.display = 'none';
            }, 3000);

            // Fade-in pesan setelah klik
            messageElement.style.opacity = '0';
            setTimeout(function() {
                messageElement.style.opacity = '1';
            }, 50);
        }
    </script>

</body>
</html>
