<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KEV Live Board - Audio & Animation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:ital,wght@0,900;1,900&display=swap');

        :root {
            --kev-yellow: #ffed00;
            --kev-gold: #ffaa00;
            --kev-yellow-glow: rgba(255, 237, 0, 0.8);
            --away-color: #ff0000;
            --bg-dark: #000000;
        }

        body {
            background-color: var(--bg-dark);
            color: #fff;
            overflow: hidden;
            font-family: 'Inter', sans-serif;
            height: 100vh;
            margin: 0;
            display: flex;
            flex-direction: column;
        }

        /* --- STANDARDBILD --- */
        .bg-rivalry {
            background: linear-gradient(90deg, #000 0%, var(--kev-yellow) 20%, #000 50%, var(--away-color) 80%, #000 100%);
            background-size: 200% 100%;
            animation: rivalry-flow 20s ease-in-out infinite alternate;
            position: relative;
        }
        .bg-rivalry::after {
            content: "";
            position: absolute;
            inset: 0;
            background: rgba(0, 0, 0, 0.88);
            pointer-events: none;
            z-index: 1;
        }

        @keyframes rivalry-flow {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        /* --- PHASE 1: STROBO --- */
        @keyframes strobe-gradient {
            0% { background: linear-gradient(90deg, var(--kev-yellow) 0%, #000 50%, var(--kev-yellow) 100%); background-size: 200% 100%; background-position: 0% 0%; }
            100% { background: linear-gradient(90deg, var(--kev-yellow) 0%, #000 50%, var(--kev-yellow) 100%); background-size: 200% 100%; background-position: 200% 0%; }
        }
        .strobe-active { 
            animation: strobe-gradient 0.08s linear infinite !important; 
        }

        /* --- PHASE 2: GOLD PULSE --- */
        @keyframes gold-pulse {
            0% { background: #000; }
            50% { background: #332d00; }
            100% { background: #000; }
        }
        .gold-celebration {
            animation: gold-pulse 2s ease-in-out infinite;
        }

        /* --- SHAKE EFFEKT --- */
        @keyframes earthquake {
            0%, 100% { transform: translate(0, 0) scale(1); }
            25% { transform: translate(-8px, -8px) scale(1.02); }
            50% { transform: translate(8px, 8px) scale(0.98); }
            75% { transform: translate(-8px, 8px) scale(1.02); }
        }
        .shake { animation: earthquake 0.07s infinite; }

        /* --- UI ELEMENTE --- */
        #home-logo-container {
            filter: drop-shadow(0 0 40px var(--kev-yellow));
            z-index: 100;
            transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        /* Gast Logo Container - Schatten entfernt für volle Sichtbarkeit */
        #away-logo-container {
            z-index: 100;
            transition: all 0.5s ease;
        }

        .team-logo { height: 28vh; width: auto; object-fit: contain; }

        .score-number {
            font-size: 32vh;
            font-weight: 900;
            font-style: italic;
            text-shadow: 0 20px 60px rgba(0,0,0,1);
            z-index: 10;
            transition: all 0.5s ease;
        }

        /* --- FOCUS MODE (Nur KEV sichtbar) --- */
        .celebration-active #away-logo-container,
        .celebration-active #away-score,
        .celebration-active #away-name-display,
        .celebration-active #period-display,
        .celebration-active #quick-action-bar,
        .celebration-active #core-trigger,
        .celebration-active .score-divider,
        .celebration-active #home-name-display {
            opacity: 0 !important;
            pointer-events: none;
        }

        .celebration-active #board-content {
            flex-direction: row;
            justify-content: center;
            gap: 50px;
        }

        .celebration-active #home-logo-container {
            transform: scale(1.4);
        }

        .celebration-active #home-score {
            font-size: 45vh;
            opacity: 1;
            transform: translateX(-20px);
            color: var(--kev-yellow);
            text-shadow: 0 0 50px rgba(255, 237, 0, 0.5);
        }

        /* --- CHANT OVERLAY (Abspann) --- */
        #chant-overlay {
            display: none;
            position: fixed;
            inset: 0;
            z-index: 600;
            background: #000;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        #chant-overlay.visible { display: flex; }
        .chant-text {
            font-size: 10vw;
            font-weight: 900;
            font-style: italic;
            text-transform: uppercase;
            color: #fff;
            animation: chant-pop 0.3s forwards;
        }
        @keyframes chant-pop {
            0% { transform: scale(0.8); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        /* --- GOAL OVERLAY --- */
        #goal-overlay {
            display: none;
            position: fixed;
            inset: 0;
            z-index: 500;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background: rgba(0,0,0,0.4);
            backdrop-filter: blur(5px);
        }
        #goal-overlay.visible { display: flex; }

        .goal-text-main {
            font-size: 10vw;
            font-weight: 900;
            font-style: italic;
            color: var(--kev-yellow);
            text-transform: uppercase;
            line-height: 0.8;
            text-align: center;
            text-shadow: 0 0 50px #000, 0 0 100px var(--kev-yellow);
            transform: skewX(-10deg);
            margin-top: -15vh;
            animation: text-pop 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @keyframes text-pop {
            0% { transform: scale(0.5) skewX(-10deg); opacity: 0; }
            100% { transform: scale(1) skewX(-10deg); opacity: 1; }
        }

        .period-badge {
            font-size: 2.8vh;
            color: var(--kev-yellow);
            font-weight: 900;
            text-transform: uppercase;
            border: 2px solid var(--kev-yellow);
            padding: 10px 40px;
            margin-top: 20px;
            z-index: 10;
            transition: opacity 0.3s;
        }

        /* --- ADMIN SIDEBAR --- */
        #admin-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background: rgba(0, 0, 0, 0.95);
            border-left: 2px solid #333;
            z-index: 1000;
            transition: right 0.3s ease-in-out;
            overflow-y: auto;
            color: #fff;
            padding: 20px;
            box-shadow: -10px 0 30px rgba(0,0,0,0.8);
            backdrop-filter: blur(10px);
        }
        #admin-sidebar.open { right: 0; }

        .admin-group { background:#111; padding:15px; border-radius:12px; margin-bottom:15px; border: 1px solid #333; text-align: center; }
        .admin-group h3 { color:var(--kev-yellow); margin-top:0; text-transform:uppercase; font-size:14px; letter-spacing:1px; }
        .admin-btn { width:100%; padding:15px; margin:5px 0; border:none; border-radius:8px; font-weight:bold; cursor:pointer; text-transform:uppercase; transition: transform 0.1s, filter 0.2s;}
        .admin-btn:active { transform: scale(0.98); }
        .admin-btn:hover { filter: brightness(1.2); }
        .btn-kev { background:var(--kev-yellow); color:#000; }
        .btn-away { background:var(--away-color); color:#fff; }
        .btn-kill { background:#444; color:#fff; font-size:11px; padding:8px; }
        .btn-reset { background:#22c55e; color:#000; }
        .btn-close { background: #333; color: #fff; margin-bottom: 20px; font-size: 12px; padding: 10px;}
        .admin-input, .admin-select { width:100%; padding:12px; margin:8px 0; background:#222; color:#fff; border:1px solid #444; border-radius:6px; box-sizing:border-box; outline: none;}
        .admin-input:focus, .admin-select:focus { border-color: var(--kev-yellow); }
        .admin-label { font-size:11px; opacity:0.5; display:block; text-align:left; text-transform:uppercase; margin-top:10px; }

        #core-trigger {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(255,255,255,0.1);
            color: #fff;
            border: 1px solid rgba(255,255,255,0.2);
            padding: 8px 15px;
            border-radius: 8px;
            cursor: pointer;
            z-index: 999;
            font-size: 12px;
            font-weight: bold;
            transition: opacity 0.3s, background 0.2s;
        }
        #core-trigger:hover { background: rgba(255,255,255,0.3); }

        #quick-action-bar {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 20px;
            z-index: 900;
            background: rgba(0,0,0,0.6);
            padding: 15px 25px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: opacity 0.3s;
        }
        .quick-btn {
            padding: 15px 30px;
            font-size: 2.5vh;
            font-weight: 900;
            font-style: italic;
            text-transform: uppercase;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.1s, filter 0.2s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
        }
        .quick-btn:active { transform: scale(0.95); }
        .quick-btn:hover { filter: brightness(1.2); }
        .quick-btn-kev { background: var(--kev-yellow); color: #000; }
        .quick-btn-away { background: var(--away-color); color: #fff; }
    </style>
</head>
<body id="main-body" class="bg-rivalry">

    <!-- Gast Tor Indikator wurde gelöscht -->

    <div id="goal-overlay">
        <div class="goal-text-main">TOR FÜR<br>KREFELD</div>
    </div>

    <div id="chant-overlay">
        <div id="chant-content" class="chant-text"></div>
    </div>

    <div id="board-container" class="flex-1 flex flex-col items-center justify-between py-16">
        <div id="period-display" class="period-badge">1. Drittel</div>

        <div id="board-content" class="flex w-full items-center justify-around px-20 flex-1">
            <!-- HEIM (LINKS) -->
            <div class="flex flex-col items-center flex-1">
                <div id="home-logo-container">
                    <img src="https://assets.holema.de/core/image/G43DSNK7GIYDAX27MM4TMNTFHE" alt="KEV Logo" class="team-logo">
                </div>
                <div id="home-score" class="score-number text-[#ffed00]">0</div>
                <div id="home-name-display" class="text-4xl font-black italic uppercase text-[#ffed00]">Krefeld</div>
            </div>

            <div class="score-number opacity-10 italic score-divider">:</div>

            <!-- GAST (RECHTS) - Logo nun voll sichtbar -->
            <div class="flex flex-col items-center flex-1">
                <div id="away-logo-container">
                    <img src="https://www.eisloewen.de/wp-content/uploads/2022/05/Logo-Regensburg.png" alt="Gast Logo" class="team-logo" id="away-logo-ui">
                </div>
                <div id="away-score" class="score-number text-white">0</div>
                <div id="away-name-display" class="text-4xl font-black italic uppercase text-white">Gegner</div>
            </div>
        </div>
    </div>

    <!-- QUICK ACTION BAR -->
    <div id="quick-action-bar">
        <button class="quick-btn quick-btn-kev" onclick="changeScore('home', 1)">TOR KREFELD</button>
        <button class="quick-btn quick-btn-away" onclick="changeScore('away', 1)">TOR GAST</button>
    </div>

    <button id="core-trigger" onclick="toggleSidebar()">⚙️ PANEL</button>

    <!-- ADMIN SIDEBAR -->
    <div id="admin-sidebar">
        <button class="admin-btn btn-close" onclick="toggleSidebar()">X Panel einklappen</button>

        <div class="admin-group">
            <h3>HEIMMANNSCHAFT</h3>
            <button class="admin-btn btn-kev" onclick="changeScore('home', 1)">TOR KREFELD (39s)</button>
            <button class="admin-btn btn-kill" onclick="changeScore('home', -1)">PUNKT ABZIEHEN KEV</button>
        </div>

        <div class="admin-group">
            <h3>GASTMANNSCHAFT</h3>
            <button class="admin-btn btn-away" onclick="changeScore('away', 1)">TOR GAST</button>
            <button class="admin-btn btn-kill" onclick="changeScore('away', -1)">PUNKT ABZIEHEN GAST</button>
            
            <label class="admin-label">Gegner Name:</label>
            <input type="text" class="admin-input" placeholder="Name (z.B. DEG)" oninput="updateGegner(this.value)">
            
            <label class="admin-label">Farbe Gast (Hintergrund):</label>
            <input type="color" class="admin-input" value="#ff0000" onchange="updateAwayColor(this.value)">
        </div>

        <div class="admin-group">
            <h3>AUDIO & DRITTEL</h3>
            <label class="admin-label">Torhymne KEV hochladen (MP3):</label>
            <input type="file" class="admin-input" accept="audio/*" onchange="uploadAudio(this)">
            
            <label class="admin-label">Spielabschnitt:</label>
            <select class="admin-select" onchange="setPeriod(this.value)">
                <option>1. Drittel</option>
                <option>2. Drittel</option>
                <option>3. Drittel</option>
                <option>Overtime</option>
                <option>Spiel beginnt bald</option>
                <option>Penaltyschießen</option>
            </select>
        </div>

        <button class="admin-btn btn-reset" onclick="stopAllEffects()">ANIMATION ABBRECHEN</button>
    </div>

    <audio id="goal-horn"></audio>

    <script>
        let homeScore = 0;
        let awayScore = 0;
        let animationTimer;

        const body = document.getElementById('main-body');
        const board = document.getElementById('board-container');
        const goalOverlay = document.getElementById('goal-overlay');
        const chantOverlay = document.getElementById('chant-overlay');
        const chantContent = document.getElementById('chant-content');
        const audioPlayer = document.getElementById('goal-horn');
        const sidebar = document.getElementById('admin-sidebar');

        function toggleSidebar() {
            sidebar.classList.toggle('open');
        }

        function changeScore(team, delta) {
            if (team === 'home') {
                if (delta > 0) { 
                    homeScore += delta; 
                    triggerKevGoal(); 
                } else { 
                    homeScore = Math.max(0, homeScore + delta); 
                    stopAllEffects(); 
                }
            } else {
                if (delta > 0) { 
                    awayScore += delta; 
                    // Nur Score Update, keine visuelle Benachrichtigung mehr
                } else { 
                    awayScore = Math.max(0, awayScore + delta); 
                }
            }
            updateDisplay();
        }

        function updateDisplay() {
            document.getElementById('home-score').innerText = homeScore;
            document.getElementById('away-score').innerText = awayScore;
        }

        function triggerKevGoal() {
            stopAllEffects();
            
            body.classList.add('celebration-active');
            body.classList.remove('bg-rivalry');
            body.classList.add('strobe-active');
            board.classList.add('shake');
            goalOverlay.classList.add('visible');
            
            if (audioPlayer.src) {
                audioPlayer.currentTime = 0;
                audioPlayer.play().catch(e => { console.log("Audio Error:", e) });
            }

            // Phase 1 (10s): Strobo & Goal Text
            animationTimer = setTimeout(() => {
                body.classList.remove('strobe-active');
                goalOverlay.classList.remove('visible');
                body.classList.add('gold-celebration');
                
                // Phase 2 (Restliche 29s): Gold Puls
                animationTimer = setTimeout(() => {
                    startChantSequence();
                }, 29000);

            }, 10000);
        }

        function startChantSequence() {
            body.classList.remove('gold-celebration');
            board.classList.remove('shake');
            chantOverlay.classList.add('visible');

            const chants = [
                "SCHEIẞ KÖLNER HAIE",
                "SCHEIẞ DEG",
                "SCHMUTZIGE PREUẞEN",
                "HU HU HU"
            ];

            let index = 0;
            const displayNextChant = () => {
                if (index < chants.length) {
                    chantContent.innerText = chants[index];
                    chantContent.style.animation = 'none';
                    void chantContent.offsetWidth; 
                    chantContent.style.animation = 'chant-pop 0.3s forwards';
                    index++;
                    setTimeout(displayNextChant, 2000); 
                } else {
                    stopAllEffects();
                }
            };
            displayNextChant();
        }

        function stopAllEffects() {
            if (animationTimer) clearTimeout(animationTimer);
            if (audioPlayer) { audioPlayer.pause(); audioPlayer.currentTime = 0; }
            
            body.classList.remove('celebration-active');
            chantOverlay.classList.remove('visible');
            body.className = 'bg-rivalry';
            board.classList.remove('shake');
            goalOverlay.classList.remove('visible');
            chantContent.innerText = "";
        }

        function updateAwayColor(color) {
            document.documentElement.style.setProperty('--away-color', color);
            // Schatten/Filter am Gast Logo entfernt für bessere Sichtbarkeit
        }

        function updateGegner(n) { 
            const name = n || "GEGNER";
            document.getElementById('away-name-display').innerText = name; 
        }

        function setPeriod(p) { 
            document.getElementById('period-display').innerText = p; 
        }

        function uploadAudio(input) { 
            if(input.files && input.files[0]) {
                const url = URL.createObjectURL(input.files[0]);
                audioPlayer.src = url;
            }
        }
    </script>
</body>
</html>
