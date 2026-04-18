#Happy birthday Prachuuu 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Prachuuu!</title>
    <style>
        body {
            background: #0f0c29;
            background: linear-gradient(to bottom, #24243e, #302b63, #0f0c29);
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Arial', sans-serif;
            color: white;
            overflow-x: hidden;
            padding: 20px;
        }

        .birthday-container {
            text-align: center;
            z-index: 10;
            max-width: 90%;
        }

        .greeting {
            font-size: 2.2rem;
            margin-bottom: 20px;
            text-shadow: 0 0 20px #ff00de;
            animation: pulse 2s infinite;
        }

        .letter-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 25px;
            border-radius: 20px;
            max-width: 450px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            margin: 0 auto 30px auto;
            line-height: 1.5;
            position: relative;
        }

        .letter-text {
            font-size: 1rem;
            color: #fce4ec;
            text-align: left;
        }

        .warning {
            display: block;
            margin-top: 15px;
            color: #ff4d4d;
            font-weight: bold;
            text-align: center;
        }

        /* Floating Elements Container */
        .animation-container {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
        }

        /* Balloons & Hearts (Floating UP) */
        .balloon, .heart {
            position: absolute;
            bottom: -150px;
            animation: floatUp 8s linear infinite;
        }

        .balloon {
            width: 50px;
            height: 70px;
            border-radius: 50%;
        }

        .heart {
            color: #ff4d4d;
            font-size: 25px;
        }

        /* Confetti (Falling DOWN) */
        .confetti {
            position: absolute;
            top: -50px;
            width: 10px;
            height: 10px;
            animation: fallDown 5s linear infinite;
        }

        /* Animation Keyframes */
        @keyframes floatUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-120vh) rotate(20deg); opacity: 0; }
        }

        @keyframes fallDown {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(120vh) rotate(360deg); opacity: 0; }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Cake Styling */
        .cake { position: relative; width: 100px; margin: 0 auto; }
        .layer { height: 20px; border-radius: 5px; margin: 2px auto; background: #f06292; }
        .top { width: 50px; } .mid { width: 80px; } .bot { width: 100px; }
        .candle { width: 6px; height: 15px; background: gold; margin: 0 auto; position: relative; }
        .candle::after { content: '🔥'; position: absolute; top: -15px; left: -5px; }

    </style>
</head>
<body>

    <div class="animation-container" id="visuals">
        </div>

    <div class="birthday-container">
        <h1 class="greeting">Happy Birthday, Prachuuu! 🎂</h1>
        
        <div class="letter-card">
            <div class="letter-text">
                🌸 <strong>Dear Bestie,</strong> 🌸<br><br>
                You are not just my friend, you are my favorite person, my partner in crime, 
                and the one who makes my life so much more beautiful 💕<br><br>
                On your special day, I wish you:<br>
                ✨ Endless smiles | 🎁 Sweet surprises<br>
                🌈 Dreams coming true | 💫 Happiness that never ends<br><br>
                Thank you for being <strong>YOU</strong>—kind, crazy, caring, and absolutely amazing 💖<br><br>
                🍰 Let’s make more memories, laugh louder, and stay best friends forever ♾️.<br><br>
                Thank you for being born and not leaving me alone in this world. You are the strongest person I know. Always be happy 😊 and healthy 💖.<br><br>
                <span class="warning">And don't ever make another best friend 🔪 instead of me!</span>
            </div>
        </div>

        <div class="cake">
            <div class="candle"></div>
            <div class="layer top"></div>
            <div class="layer mid"></div>
            <div class="layer bot"></div>
        </div>
    </div>

    <script>
        const container = document.getElementById('visuals');
        const colors = ['#ff00de', '#7b2cbf', '#00d4ff', '#ffbd00', '#ff4d4d', '#ffffff'];

        function createElements() {
            // Create 15 Confetti
            for(let i=0; i<15; i++) {
                let c = document.createElement('div');
                c.className = 'confetti';
                c.style.left = Math.random() * 100 + '%';
                c.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                c.style.animationDelay = Math.random() * 5 + 's';
                container.appendChild(c);
            }

            // Create 8 Balloons
            for(let i=0; i<8; i++) {
                let b = document.createElement('div');
                b.className = 'balloon';
                b.style.left = Math.random() * 100 + '%';
                b.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                b.style.animationDelay = Math.random() * 8 + 's';
                container.appendChild(b);
            }

            // Create 10 Hearts
            for(let i=0; i<10; i++) {
                let h = document.createElement('div');
                h.className = 'heart';
                h.innerHTML = '❤️';
                h.style.left = Math.random() * 100 + '%';
                h.style.animationDelay = Math.random() * 8 + 's';
                container.appendChild(h);
            }
        }
        createElements();
    </script>
</body>
</html>
