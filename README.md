<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RapidBrainwave</title>
    <link rel="icon" href="https://yt3.googleusercontent.com/dnBJtL6OpEPnfeIfXrAz7QCp0PL3uw4AARWyWM2g59vu6ctGab6sYnnAmJi9sCVHxmP_GvQlNYQ=s160-c-k-c0x00ffffff-no-rj">
    <style>
        body {  background-color: #f9dd16;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            min-height: 100vh; }
        header { background-color: #333;
            color: #fff;
            padding: 15px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); }
        header h1 { margin: 0;
            font-size: 2rem;
            font-family: 'Arial Black', sans-serif; }
        .container {display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            grid-gap: 20px;
            padding: 20px;
            flex: 1; }
        .box {background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); }
        .box h2 {  margin: 0 0 15px;
            font-size: 1.5rem; }
        .box canvas {max-width: 100%;
            border: 2px solid #000;
            border-radius: 4px; }
        .menu-button {  padding: 10px 20px;
            background-color: #444;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s ease; }
        .menu-button:hover 
        { background-color: #555;  }
        .statistics {position: fixed;
            top: 20px;
            right: 20px;
            background-color: #fff;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            z-index: 1000; }
        .statistics h3 {
            margin: 0 0 10px;
            font-size: 1.2rem; }
        footer { text-align: center;
            padding: 20px;
            background-color: #333;
            color: #fff;
            border-top: 1px solid #444;  }
        footer p {
            margin: 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .statistics {
                top: 10px;
                right: 10px;
                padding: 10px;
            }
            header h1 {
                font-size: 1.5rem;
            }
            .box h2 {
                font-size: 1.25rem;
            }
            .menu-button {
                font-size: 14px;
            }
        }

        @media (max-width: 480px) {
            .statistics {
                width: calc(100% - 20px);
                position: static;
                margin: 10px auto;
            }
            header h1 {
                font-size: 1.25rem;
            }
            .box h2 {
                font-size: 1rem;
            }
            .menu-button {
                width: 100%;
                padding: 15px;
                font-size: 14px;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>RapidBrainwave</h1>
    </header>

    <div class="statistics">
        <h3>Site Statistics</h3>
        <p>Daily Visits: <span id="dailyVisits">0</span></p>
        <p>Weekly Visits: <span id="weeklyVisits">0</span></p>
        <p>Total Visits: <span id="totalVisits">0</span></p>
    </div>

    <div class="container">
        <div class="box">
            <h2>Game 1</h2>
            <canvas id="gameCanvas" width="300" height="200"></canvas>
            <button class="menu-button">Play</button>
        </div>
        <div class="box">
            <h2>Game 2</h2>
            <canvas id="gameCanvas2" width="300" height="200"></canvas>
            <button class="menu-button">Play</button>
        </div>
    </div>

    <footer>
        <p>&copy; 2024 RapidBrainwave. All rights reserved.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Simulate fetching statistics data
            const dailyVisits = Math.floor(Math.random() * 1000);
            const weeklyVisits = Math.floor(Math.random() * 7000);
            const totalVisits = Math.floor(Math.random() * 50000);

            // Update statistics in DOM
            document.getElementById('dailyVisits').textContent = dailyVisits;
            document.getElementById('weeklyVisits').textContent = weeklyVisits;
            document.getElementById('totalVisits').textContent = totalVisits;
        });
    </script>

</body>
</html>


    <header>
        <h1>RapidBrainwave</h1>
    </header>

    <div class="container">
        <!-- Εγκυκλοπαίδεια -->
        <div class="box" id="encyclopedia">
            <h2>ENCYCLOPEDIA</h2>
            <p>Προσθέστε το περιεχόμενο της εγκυκλοπαίδειας εδώ...</p>
        </div>

        <!-- Sites You Should Know -->
        <div class="box" id="sites">
            <h2>SITES YOU SHOULD KNOW</h2>
            <ul>
                <li><a href="https://www.example1.com" target="_blank">Example Site 1</a></li>
                <li><a href="https://www.example2.com" target="_blank">Example Site 2</a></li>
                <!-- Προσθέστε περισσότερα sites εδώ -->
            </ul>
        </div>

        <!-- Πρώτο Παιχνίδι -->
        <div class="box" id="game-1">
            <h2>2D Game - Adventure Runner</h2>
            <canvas id="gameCanvas" width="800" height="600"></canvas>

            <div id="menu">
                <button class="menu-button" onclick="startGame()">Start Game</button>
                <button class="menu-button" onclick="restartGame()">Reset Game</button>
                <button class="menu-button" onclick="nextStage()">Next Stage</button>
                <div class="controls">
                    <label for="music-volume">Music Volume:</label>
                    <input type="range" id="music-volume" min="0" max="1" step="0.1" value="0.5" onchange="adjustVolume()">
                    <br>
                    <label for="sfx-volume">SFX Volume:</label>
                    <input type="range" id="sfx-volume" min="0" max="1" step="0.1" value="0.5" onchange="adjustSfxVolume()">
                </div>
            </div>
        </div>

        <!-- Δεύτερο Παιχνίδι -->
        <div class="box" id="game-2">
            <h2>Advanced Game - Space Explorer</h2>
            <canvas id="gameCanvas2" width="800" height="600"></canvas>

            <div id="advanced-menu">
                <button class="menu-button" onclick="startAdvancedGame()">Start Game</button>
                <button class="menu-button" onclick="restartAdvancedGame()">Reset Game</button>
                <div class="controls">
                    <label for="adv-music-volume">Music Volume:</label>
                    <input type="range" id="adv-music-volume" min="0" max="1" step="0.1" value="0.5" onchange="adjustAdvVolume()">
                    <br>
                    <label for="adv-sfx-volume">SFX Volume:</label>
                    <input type="range" id="adv-sfx-volume" min="0" max="1" step="0.1" value="0.5" onchange="adjustAdvSfxVolume()">
                </div>
            </div>
        </div>

        <!-- Quiz -->
        <div class="box" id="quiz-section">
            <h2>QUIZ</h2>
            <p>Προσθέστε τα quiz σας εδώ...</p>
        </div>

        <!-- YouTube Channel -->
        <div class="box" id="youtube-section">
            <h2>YOUTUBE</h2>
            <a href="https://www.youtube.com/@rapidbrainwave" target="_blank">
                <img src="https://yt3.googleusercontent.com/dnBJtL6OpEPnfeIfXrAz7QCp0PL3uw4AARWyWM2g59vu6ctGab6sYnnAmJi9sCVHxmP_GvQlNYQ=s160-c-k-c0x00ffffff-no-rj" alt="RapidBrainwave" width="100">
                <p>Visit my channel - RapidBrainwave</p>
            </a>
        </div>
    </div>

    <footer>
        <p>Created by Marios D. Tasoulas</p>
        <p>Code written by ChatGPT</p>
    </footer>

    <!-- Αρχεία ήχου για το πρώτο παιχνίδι -->
    <audio id="backgroundMusic" loop>
        <source src="background-music.mp3" type="audio/mp3">
    </audio>
    <audio id="jumpSound">
        <source src="jump-sound.mp3" type="audio/mp3">
    </audio>
    <audio id="winSound">
        <source src="win-sound.mp3" type="audio/mp3">
    </audio>
    <audio id="loseSound">
        <source src="lose-sound.mp3" type="audio/mp3">
    </audio>

    <!-- Αρχεία ήχου για το δεύτερο παιχνίδι -->
    <audio id="adv-backgroundMusic" loop>
        <source src="adv-background-music.mp3" type="audio/mp3">
    </audio>
    <audio id="adv-actionSound">
        <source src="adv-action-sound.mp3" type="audio/mp3">
    </audio>

    <script>
        // Πρώτο Παιχνίδι
        let canvas = document.getElementById("gameCanvas");
        let ctx = canvas.getContext("2d");
        let score = 0;
        let level = 1;
        let gameRunning = false;
        let player = { x: 50, y: 550, width: 40, height: 40, color: 'blue', speed: 5 };

        let backgroundMusic = document.getElementById('backgroundMusic');
        let jumpSound = document.getElementById('jumpSound');
        let winSound = document.getElementById('winSound');
        let loseSound = document.getElementById('loseSound');

        let musicVolume = document.getElementById('music-volume').value;
        backgroundMusic.volume = musicVolume;

        let sfxVolume = document.getElementById('sfx-volume').value;

        function startGame() {
            backgroundMusic.play();
            gameRunning = true;
            score = 0;
            level = 1;
            player.x = 50;
            player.y = 550;
            gameLoop();
        }

        function restartGame() {
            score = 0;
            player.x = 50;
            player.y = 550;
            gameRunning = true;
            gameLoop();
        }

        function nextStage() {
            level++;
            player.x = 50;
            player.y = 550;
            score = 0;
            gameLoop();
        }

        function adjustVolume() {
            backgroundMusic.volume = document.getElementById('music-volume').value;
        }

        function adjustSfxVolume() {
            sfxVolume = document.getElementById('sfx-volume').value;
        }

        function gameLoop() {
            if (!gameRunning) return;

            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Σχεδίαση παίκτη
            ctx.fillStyle = player.color;
            ctx.fillRect(player.x, player.y, player.width, player.height);

            // Ενημέρωση και εμφάνιση σκορ και επιπέδου
            score++;
            ctx.fillStyle = 'black';
            ctx.font = '20px Arial';
            ctx.fillText(`Score: ${score}`, 10, 30);
            ctx.fillText(`Level: ${level}`, 10, 60);

            // Έλεγχος νίκης/ήττας
            if (score >= 500) {
                ctx.font = '40px Arial Black';
                ctx.fillStyle = 'green';
                ctx.fillText('CONGRATULATIONS!', canvas.width / 2 - 200, canvas.height / 2);
                winSound.volume = sfxVolume;
                winSound.play();
                gameRunning = false;
                return;
            }

            // Κίνηση παίκτη
            document.addEventListener('keydown', function(event) {
                if (event.code === 'ArrowUp') {
                    player.y -= player.speed;
                    jumpSound.volume = sfxVolume;
                    jumpSound.play();
                } else if (event.code === 'ArrowDown') {
                    player.y += player.speed;
                } else if (event.code === 'ArrowLeft') {
                    player.x -= player.speed;
                } else if (event.code === 'ArrowRight') {
                    player.x += player.speed;
                }
            });

            requestAnimationFrame(gameLoop);
        }

        // Δεύτερο Παιχνίδι (Πιο Πολύπλοκο)
        let canvas2 = document.getElementById("gameCanvas2");
        let ctx2 = canvas2.getContext("2d");
        let advGameRunning = false;
        let advPlayer = { x: 400, y: 550, width: 50, height: 50, color: 'red', speed: 7 };
        let advBackgroundMusic = document.getElementById('adv-backgroundMusic');
        let advActionSound = document.getElementById('adv-actionSound');

        let advMusicVolume = document.getElementById('adv-music-volume').value;
        advBackgroundMusic.volume = advMusicVolume;

        let advSfxVolume = document.getElementById('adv-sfx-volume').value;

        function startAdvancedGame() {
            advBackgroundMusic.play();
            advGameRunning = true;
            advPlayer.x = 400;
            advPlayer.y = 550;
            advancedGameLoop();
        }

        function restartAdvancedGame() {
            advPlayer.x = 400;
            advPlayer.y = 550;
            advGameRunning = true;
            advancedGameLoop();
        }

        function adjustAdvVolume() {
            advBackgroundMusic.volume = document.getElementById('adv-music-volume').value;
        }

        function adjustAdvSfxVolume() {
            advSfxVolume = document.getElementById('adv-sfx-volume').value;
        }

        function advancedGameLoop() {
            if (!advGameRunning) return;

            ctx2.clearRect(0, 0, canvas2.width, canvas2.height);

            // Σχεδίαση παίκτη
            ctx2.fillStyle = advPlayer.color;
            ctx2.fillRect(advPlayer.x, advPlayer.y, advPlayer.width, advPlayer.height);

            // Κίνηση παίκτη
            document.addEventListener('keydown', function(event) {
                if (event.code === 'KeyW') {
                    advPlayer.y -= advPlayer.speed;
                    advActionSound.volume = advSfxVolume;
                    advActionSound.play();
                } else if (event.code === 'KeyS') {
                    advPlayer.y += advPlayer.speed;
                } else if (event.code === 'KeyA') {
                    advPlayer.x -= advPlayer.speed;
                } else if (event.code === 'KeyD') {
                    advPlayer.x += advPlayer.speed;
                }
            });

            // Προσθέστε επιπλέον λειτουργικότητα εδώ (π.χ. εχθρούς, εμπόδια)

            requestAnimationFrame(advancedGameLoop);
        }

        // Αρχικοποίηση
        window.onload = function() {
            // Μπορείτε να προσθέσετε οποιεσδήποτε αρχικές ρυθμίσεις εδώ
        };
    </script>

</body>
</html>
