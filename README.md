<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🎂 Happy Birthday Dhea 🎉</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/@tsparticles/confetti@3.0.3/tsparticles.confetti.bundle.min.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>

  <style>
    * {
      transition: all 0.6s ease-in-out;
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive;
      background: radial-gradient(circle at top, #000000, #0a0a0a);
      color: #8ecae6;
      overflow: hidden;
      text-align: center;
    }

    /* ===== TEKS PELANGI ===== */
    .rainbow-text {
      background: linear-gradient(90deg, #00ffff, #ff00ff, #ffcc00, #00ff66, #00ffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-size: 400%;
      animation: rainbowMove 6s linear infinite;
    }
    @keyframes rainbowMove {
      0% { background-position: 0% }
      100% { background-position: 400% }
    }

    /* ===== SLIDE STYLE ===== */
    .slide {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transform: scale(0.9);
      transition: opacity 1s ease, transform 1s ease;
    }
    .active {
      opacity: 1;
      transform: scale(1);
      z-index: 10;
    }

    button {
      background: linear-gradient(90deg, #0077ff, #00ccff);
      color: white;
      padding: 10px 25px;
      border: none;
      border-radius: 25px;
      margin-top: 25px;
      cursor: pointer;
      font-weight: bold;
      box-shadow: 0 0 20px rgba(0,150,255,0.7);
      transition: transform 0.3s ease, background 0.3s ease;
    }
    button:hover {
      background: linear-gradient(90deg, #00ccff, #33ffff);
      transform: scale(1.1);
    }

    /* ===== CAKE ANIMATION ===== */
    .cake {
      position: relative;
      width: 180px;
      height: 120px;
      margin: 20px auto;
      animation: float 3s ease-in-out infinite alternate;
      transform-origin: center;
    }
    @keyframes float {
      from { transform: translateY(0); }
      to { transform: translateY(-12px); }
    }

    .plate {
      position: absolute;
      bottom: -10px;
      left: -15px;
      width: 210px;
      height: 20px;
      background: #3d3d3d;
      border-radius: 50%;
      box-shadow: 0 8px 18px rgba(0,0,0,0.25);
    }
    .layer {
      position: absolute;
      left: 10px;
      width: 160px;
      border-radius: 20px;
    }
    .layer1 { top: 70px; height: 50px; background: linear-gradient(to bottom, #0077ff, #0044cc); }
    .layer2 { top: 30px; height: 40px; width: 140px; left: 20px; background: linear-gradient(to bottom, #33aaff, #0077ff); }
    .layer3 { top: 0; height: 30px; width: 120px; left: 30px; background: linear-gradient(to bottom, #99ddff, #33aaff); }

    .candle {
      position: absolute;
      top: -45px;
      left: 85px;
      width: 15px;
      height: 45px;
      background: repeating-linear-gradient(45deg, #00ccff, #00ccff 5px, #ffffff 5px, #ffffff 10px);
      border-radius: 5px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .candle:hover { transform: scale(1.1); }

    .flame {
      position: absolute;
      top: -25px;
      left: 91px;
      width: 10px;
      height: 15px;
      background: radial-gradient(circle, gold 40%, orange 80%, transparent);
      border-radius: 50%;
      box-shadow: 0 0 20px gold;
      animation: flicker 0.25s infinite alternate;
    }
    @keyframes flicker {
      from { transform: scale(1); opacity: 0.9; }
      to { transform: scale(1.2); opacity: 1; }
    }

    h1, h2, p { animation: fadeInUp 1s ease; }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>

<body>
  <!-- ===== SLIDE 1 ===== -->
  <section class="slide active">
    <h1 class="text-5xl font-bold mb-4 rainbow-text">🎉 Selamat Ulang Tahun, Dhea! 🎉</h1>
    <p class="text-lg mb-4 text-blue-300">Hari ini dunia lebih berkilau... karena kamu lahir 💖</p>
    <button onclick="nextSlide()">Lanjut ➡️</button>
  </section>

  <!-- ===== SLIDE 2 ===== -->
  <section class="slide">
    <div class="cake">
      <div class="plate"></div>
      <div class="layer layer1"></div>
      <div class="layer layer2"></div>
      <div class="layer layer3"></div>
      <div class="candle" id="candle"></div>
      <div class="flame" id="flame"></div>
    </div>
    <p id="ucapan" class="text-blue-300">Klik lilin buat tiup ya 🎂</p>
    <button onclick="nextSlide()">➡️ Selanjutnya</button>
  </section>

  <!-- ===== SLIDE 3–10 ===== -->
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">🌈 Harapan untukmu 🌈</h2><p class="text-lg w-80 text-blue-300">Semoga setiap langkahmu penuh cahaya dan tawa. Dunia butuh senyum seindah punyamu 💕</p><button onclick="confettiEffect()">🎊 Rayakan!</button><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">🍰 Kamu Spesial 🍰</h2><p class="text-lg w-80 text-blue-300">Kamu bukan cuma bertambah umur, tapi juga makin berharga di hati banyak orang 💫</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">💌 Pesan Rahasia 💌</h2><p class="text-lg w-80 text-blue-300">Kalau kamu merasa lelah, ingat... ada banyak doa diam-diam yang ingin kamu bahagia 🤍</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">✨ Mimpi yang Indah ✨</h2><p class="text-lg w-80 text-blue-300">Terus kejar mimpimu, tapi jangan lupa nikmati langkah-langkah kecilnya 🌸</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">🌷 Dhea yang Hebat 🌷</h2><p class="text-lg w-80 text-blue-300">Jangan pernah ragu sama diri sendiri, karena kamu lebih kuat dari yang kamu kira 💪</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">🌸 Canda, Tawa, dan Bahagia 🌸</h2><p class="text-lg w-80 text-blue-300">Tahun baru ini bukan cuma tentang lilin dan kue, tapi tentang cerita baru yang siap kamu tulis 📖</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h2 class="text-3xl font-bold mb-2 rainbow-text">💖 Terima Kasih 💖</h2><p class="text-lg w-80 text-blue-300">Terima kasih sudah jadi sosok yang ceria, baik, dan selalu menebar energi positif 🌞</p><button onclick="nextSlide()">➡️</button></section>
  <section class="slide"><h1 class="text-4xl font-bold mb-4 rainbow-text">🎀 Dari Temanmu 🎀</h1><p class="text-lg w-80 text-blue-300">Dhea, semoga semua hal indah selalu berpihak padamu. Dunia lebih indah karena kamu ada 💐</p><button onclick="restart()">🔁 Ulangi dari Awal</button></section>

  <!-- ===== AUDIO ===== -->
  <audio id="lagu" src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.mp3"></audio>

  <script>
    let currentSlide = 1;
    const slides = document.querySelectorAll('.slide');
    const totalSlides = slides.length;
    const flame = document.getElementById('flame');
    const candle = document.getElementById('candle');
    const ucapan = document.getElementById('ucapan');
    const lagu = document.getElementById('lagu');

    function nextSlide() {
      if (currentSlide < totalSlides) {
        slides[currentSlide - 1].classList.remove('active');
        slides[currentSlide].classList.add('active');
        currentSlide++;
        if (currentSlide === 2) lagu.play();
      }
    }

    function restart() {
      slides.forEach(s => s.classList.remove('active'));
      slides[0].classList.add('active');
      currentSlide = 1;
    }

    let mati = false;
    candle.onclick = () => {
      if (!mati) {
        flame.style.display = 'none';
        ucapan.innerText = "💨 Lilinnya padam! Klik lagi buat nyalain 🔥";
        mati = true;
      } else {
        flame.style.display = 'block';
        ucapan.innerText = "🔥 Lilin menyala lagi! Semoga semua harapanmu terkabul ✨";
        mati = false;
      }
    };

    function confettiEffect() {
      confetti({
        particleCount: 250,
        spread: 160,
        origin: { y: 0.6 },
        colors: ["#33ccff", "#00ffff", "#ff00ff", "#ffff00", "#00ff66"]
      });
    }
  </script>
</body>
</html>

