<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>HERO WOLFS Team</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: url('https://images.unsplash.com/photo-1600132806158-7b2dc7bce6c5?auto=format&fit=crop&w=1600&q=80') no-repeat center center fixed;
      background-size: cover;
      color: white;
      text-align: center;
      padding: 2rem;
    }

    h1 {
      font-size: 3rem;
      text-shadow: 2px 2px 8px #ff4e00;
    }

    #logo {
      width: 150px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    #logo:hover {
      transform: scale(1.1);
      animation: firePulse 1.5s infinite ease-in-out;
    }

    @keyframes firePulse {
      0% { filter: drop-shadow(0 0 8px orange); }
      50% { filter: drop-shadow(0 0 16px red); }
      100% { filter: drop-shadow(0 0 8px orange); }
    }

    .player-cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      margin-top: 1rem;
    }

    .player-card {
      background: rgba(0, 0, 0, 0.6);
      border: 2px solid #ff9f1c;
      border-radius: 12px;
      padding: 1rem;
      width: 200px;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .player-card:hover {
      transform: scale(1.05);
    }

    .player-info {
      display: none;
      margin-top: 0.5rem;
      font-size: 0.9rem;
      color: #ffd8a8;
    }

    #team-info {
      display: none;
      margin-top: 2rem;
      padding: 1rem;
      background: rgba(0, 0, 0, 0.6);
      border-radius: 12px;
    }

    .discord-btn {
      display: inline-block;
      padding: 12px 24px;
      margin-top: 10px;
      background: linear-gradient(45deg, #ff4e00, #ff9f1c);
      color: #fff;
      font-weight: bold;
      text-decoration: none;
      border-radius: 12px;
      box-shadow: 0 0 12px #ff4e00aa;
      transition: transform 0.3s, box-shadow 0.3s;
      animation: glowPulse 1.5s infinite ease-in-out;
    }

    .discord-btn:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #ff9f1cdd;
    }

    @keyframes glowPulse {
      0%   { box-shadow: 0 0 10px #ff4e00aa; }
      50%  { box-shadow: 0 0 20px #ff9f1cdd; }
      100% { box-shadow: 0 0 10px #ff4e00aa; }
    }
  </style>
</head>
<body>

  <h1>🔥 HERO WOLFS 🔥</h1>
  <img id="logo" src="logo.png" alt="Team Logo" onclick="toggleTeamInfo()">

  <div id="team-info">
    <h2>About Us</h2>
    <p>We are a newly made team (HERO WOLFS). Founder SILWER WOLF made the team at 2025.03.04.</p>
    <p><strong>📱 Where you can contact us:</strong></p>
    <a href="https://discord.gg/4UXmkYtC" target="_blank" class="discord-btn">🔥 Join Our Discord 🔥</a>

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

    <h3 style="margin-top: 2rem;">🏆 Achievements</h3>
    <p style="animation: glowPulse 2s infinite; font-style: italic;">Nothing for now... 🔥 <em>Coming Soon</em>!</p>
  </div>

  <script>
    function toggleTeamInfo() {
      const info = document.getElementById('team-info');
      info.style.display = (info.style.display === 'none' || info.style.display === '') ? 'block' : 'none';
    }

    function toggleDetails(card) {
      const info = card.querySelector('.player-info');
      info.style.display = (info.style.display === 'none' || info.style.display === '') ? 'block' : 'none';
    }
  </script>

</body>
</html>
