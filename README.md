
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Anime Profile</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #101014;
      color: white;
      font-family: Arial, sans-serif;
      min-height: 100vh;
    }

    header {
      padding: 25px;
      text-align: center;
      background: #1c1c24;
      border-bottom: 1px solid #333;
    }

    header h1 {
      color: #b9b9c9;
      letter-spacing: 3px;
    }

    .container {
      max-width: 900px;
      margin: 40px auto;
      padding: 20px;
    }

    .profile {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 30px;
      background: #1c1c24;
      padding: 25px;
      border-radius: 15px;
      border: 1px solid #333;
    }

    .profile img {
      width: 230px;
      height: 300px;
      object-fit: cover;
      border-radius: 12px;
      border: 2px solid #666;
    }

    .info {
      flex: 1;
      min-width: 200px;
    }

    .info h2 {
      font-size: 30px;
      margin-bottom: 10px;
    }

    .info p {
      color: #bdbdc7;
      margin: 12px 0;
      line-height: 1.6;
    }

    .section {
      background: #1c1c24;
      margin-top: 25px;
      padding: 25px;
      border-radius: 15px;
      border: 1px solid #333;
    }

    h3 {
      color: #c5c5d3;
      margin-bottom: 15px;
    }

    .music {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 15px;
    }

    button {
      background: #555566;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 15px;
    }

    button:hover {
      background: #77778c;
    }

    audio {
      width: 100%;
      margin-top: 15px;
    }

    footer {
      text-align: center;
      padding: 25px;
      color: #777;
    }

    @media (max-width: 600px) {
      .profile {
        justify-content: center;
        text-align: center;
      }

      .profile img {
        width: 100%;
        max-width: 280px;
      }
    }
  </style>
</head>

<body>

  <header>
    <h1>MY PROFILE</h1>
    <p>Welcome to my anime world</p>
  </header>

  <main class="container">

    <div class="profile">

      <img
        src="Waifu gua.jpg"
        alt="Foto waifu">

      <div class="info">
        <h2>Halo, Saya Aditya!</h2>
        <p>
          Selamat datang di website pribadi saya.
          Saya seorang pecinta anime, gamer,
          dan penggemar musik.
        </p>

        <p><b>Nama:</b> Aditya</p>
        <p><b>Hobi:</b> Gaming, Anime, Musik</p>
        <p><b>Waifu:</b> Sistine Fibel</p>
        <p><b>Genre favorit:</b> Action, Fantasy</p>
      </div>

    </div>

    <div class="section">
      <h3>Tentang Saya</h3>
      <p>
        Saya suka menghabiskan waktu dengan bermain game,
        menonton anime, dan mendengarkan musik.
        Ini adalah website pribadi saya dengan
        tema anime yang simpel dan elegan.
      </p>
    </div>

    <div class="section">
      <h3>My Favorite Music</h3>

      <div class="music">
        <p>🎵 Musik favorit saya</p>

        <button onclick="toggleMusic()" id="musicBtn">
          ▶ Putar Musik
        </button>
      </div>

      <audio id="music" loop>
        <source src="18.mp3" type="audio/mpeg">
        Browser kamu tidak mendukung audio.
      </audio>
    </div>

  </main>

  <footer>
    <p>© 2026 Aditya | Made with ❤️</p>
  </footer>

  <script>
    const music = document.getElementById("music");
    const btn = document.getElementById("musicBtn");

    function toggleMusic() {
      if (music.paused) {
        music.play().then(() => {
          btn.textContent = "⏸ Hentikan Musik";
        }).catch(() => {
          alert("File musik belum tersedia!");
        });
      } else {
        music.pause();
        btn.textContent = "▶ Putar Musik";
      }
    }
  </script>

</body>
</html>
