<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>🔥 Team Roles</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: radial-gradient(ellipse at top, #1b1b1b, #000000);
      color: white;
      padding: 20px;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px;
    }

    .logo {
      height: 60px;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .logo:hover {
      transform: scale(1.05);
      filter: drop-shadow(0 0 10px #ff4e00);
    }

    .intro-section {
      text-align: center;
      margin: 40px 0;
    }

    .intro-section h1 {
      font-size: 2.5em;
      color: #ffe156;
      animation: flicker 2s infinite;
    }

    .intro-section p {
      font-size: 1.1em;
      color: #ddd;
    }

    .achievements-section {
      margin-top: 60px;
      padding: 30px;
      background: rgba(20, 20, 20, 0.8);
      border-radius: 16px;
      box-shadow: 0 0 30px rgba(255, 107, 107, 0.4);
      text-align: center;
      animation: fadeIn 1s ease-in-out;
    }

    .achievements-section h2 {
      color: #ffe156;
      font-size: 2em;
      margin-bottom: 20px;
      text-shadow: 0 0 10px #ffe15655;
    }

    .achievements-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .achievements-list li {
      font-size: 1.2em;
      margin: 12px 0;
      color: #f1f1f1;
      text-shadow: 0 0 5px rgba(255,255,255,0.2);
    }

    #team-info {
      text-align: center;
      margin-top: 40px;
      animation: fadeIn 0.5s ease-in-out;
    }

    .player-cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }

    .player-card {
      background: #222;
      border-radius: 16px;
      padding: 20px;
      width: 200px;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
      box-shadow: 0 0 10px #ff9f1c66;
      animation: pulse 2s infinite;
    }

    .player-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #ff9f1caa;
    }

    .player-info {
      display: none;
      margin-top: 10px;
      color: #ccc;
      font-size: 0.95em;
      animation: fadeIn 0.5s ease-in-out;
    }

    footer {
      margin-top: 80px;
      text-align: center;
      font-size: 0.9em;
      color: #888;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0% { box-shadow: 0 0 10px #ff9f1c66; }
      50% { box-shadow: 0 0 20px #ff9f1caa; }
      100% { box-shadow: 0 0 10px #ff9f1c66; }
    }

    @keyframes flicker {
      0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% {
        opacity: 1;
      }
      20%, 24%, 55% {
        opacity: 0.4;
      }
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="Team Logo" class="logo" onclick="toggleInfo()">
  </header>

  <div class="intro-section">
    <h1>Welcome to Our Fire Team 🔥</h1>
    <p>We are a competitive CS2 team dominating the servers and breaking records.</p>
  </div>

  <div class="achievements-section">
    <h2>🔥 Our Achievements</h2>
    <ul class="achievements-list">
      <li>🏆 Winners of Dust II Showdown 2024</li>
      <li>🥇 Top 3 in Inferno Cup - Winter Edition</li>
      <li>💥 Most Clutches in Mirage Masters League</li>
    </ul>
  </div>

  <div id="team-info" style="display:none;">
    <h2>About Us</h2>
    <p>We are a passionate group of players with a fiery spirit, great teamwork, and a goal to conquer every tournament we enter.</p>
    <h3>🔥 Team Roster</h3>
    <div class="player-cards">
      <div class="player-card" onclick="toggleDetails(this)">
        🔥 <strong>Doxiest</strong><br>In-Game Leader
        <div class="player-info">Strategic mastermind, clutch caller, and team captain. Leads with experience and fire.</div>
      </div>
      <div class="player-card" onclick="toggleDetails(this)">
        💥 <strong>donk666</strong><br>Entry Fragger
        <div class="player-info">Fearless frontliner known for explosive plays and first bloods. Breaks through every defense.</div>
      </div>
      <div class="player-card" onclick="toggleDetails(this)">
        🎯 <strong>SILWER WOLF</strong><br>AWPer
        <div class="player-info">Sharp-eyed sniper who never misses a flick. Controls the map with deadly precision.</div>
      </div>
      <div class="player-card" onclick="toggleDetails(this)">
        🛡️ <strong>mearxz</strong><br>Support
        <div class="player-info">Reliable backbone of the team. Sets up plays, throws perfect nades, and covers every angle.</div>
      </div>
      <div class="player-card" onclick="toggleDetails(this)">
        🧠 <strong>Nex1k</strong><br>Lurker
        <div class="player-info">Master of the shadows. Sneaks behind lines, gathers intel, and outsmarts the enemy.</div>
      </div>
    </div>
  </div>

  <footer>
    &copy; 2025 Your Team Name. All rights reserved.
  </footer>

  <script>
    function toggleInfo() {
      const info = document.getElementById("team-info");
      info.style.display = info.style.display === "none" ? "block" : "none";
    }

    function toggleDetails(card) {
      const info = card.querySelector(".player-info");
      info.style.display = info.style.display === "block" ? "none" : "block";
    }
  </script>
</body>
</html>
