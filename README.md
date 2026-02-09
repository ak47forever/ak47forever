<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Our Little Universe ✨</title>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: radial-gradient(circle at top, #2b1d4d, #0b061a);
      color: #f5f3ff;
      overflow-x: hidden;
    }

    section {
      min-height: 100vh;
      padding: 60px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .card {
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(10px);
      border-radius: 22px;
      padding: 35px;
      max-width: 800px;
      box-shadow: 0 0 40px rgba(255, 192, 203, 0.15);
    }

    h1, h2 {
      font-family: 'Playfair Display', serif;
    }

    button {
      background: linear-gradient(135deg, #ff9aa2, #c77dff);
      border: none;
      color: #1b102f;
      padding: 12px 30px;
      border-radius: 30px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 25px;
      transition: transform 0.2s ease;
    }

    button:hover {
      transform: scale(1.05);
    }

    .stars::before {
      content: "";
      position: fixed;
      inset: 0;
      background-image:
        radial-gradient(1px 1px at 20% 30%, white, transparent),
        radial-gradient(1px 1px at 80% 70%, white, transparent),
        radial-gradient(1px 1px at 50% 50%, white, transparent);
      background-size: 200px 200px;
      opacity: 0.3;
      z-index: -1;
      animation: twinkle 8s infinite alternate;
    }

    @keyframes twinkle {
      from { opacity: 0.2; }
      to { opacity: 0.4; }
    }
  </style>
</head>

<body class="stars">

<!-- 🎶 MUSIC (loops forever, starts on first click) -->
<iframe
  id="musicPlayer"
  width="0"
  height="0"
  src="https://www.youtube.com/embed/4yZ-mn0u8NE?autoplay=0&loop=1&playlist=4yZ-mn0u8NE"
  frameborder="0"
  allow="autoplay">
</iframe>

<!-- LANDING -->
<section>
  <div class="card">
    <h1>
      Out of billions of people,<br>
      somehow… the universe paused for you ✨
    </h1>
    <button onclick="goTo('letter')">Enter our little universe 💫</button>
  </div>
</section>

<!-- LOVE LETTER -->
<section id="letter">
  <div class="card">
    <p>
      I don’t know when it happened exactly. There wasn’t one loud moment or a dramatic sign.
      Bas ek din, it felt like my heart knew you.<br><br>

      In a world that’s always rushing, you felt calm — familiar in a way that’s hard to explain.
      Somewhere between conversations, silences, and thoughts I never said out loud,
      I realised how grateful I am for you.<br><br>

      Grateful for the way you exist, for the comfort you bring without trying,
      for how easily you became important to me.
      And oh God, how I miss you every single day.
      Life has humbled me enough to understand that what’s the point of a whole garden
      when the only flower I love is missing.Some days the distance feels unbearable and I want you right next to me. I miss you constantly , in everyday moments where I wish you were here. Counting days has somehow become my favourite habit, not because I want to, but because it’s the only thing that makes the waiting feel survivable. Loving you from here isn’t easy, but it’s still you who I want, every single day.
And no matter how far you are, you are always the place my heart comes back to.<br><br>

      I love you — silently, calmly, loudly, dramatically — in every possible way.
      You literally mean the world to me, in the soft everyday sense that actually lasts.<br><br>

      And if choosing you feels this natural, maybe it was destiny all along.
    </p>
    <button onclick="goTo('timeline')">Keep going 🌙</button>
  </div>
</section>

<!-- TIMELINE -->
<section id="timeline">
  <div class="card">
    <h2>🌌 How the universe slowly wrote us</h2>
    <p>🌟 Thank you ma'am Deepanjali</p>
    <p>🌙 Physics Lab built the Chemistry</p>
    <p>💫 When choosing you started feeling natural</p>
    <p>💖 Now — where love feels so sure that I fear the void</p>
    <p>🔮 What the future is gently promising us…</p>
    <button onclick="goTo('feels')">One more thing ✨</button>
  </div>
</section>

<!-- FEELS -->
<section id="feels">
  <div class="card">
    <p>Some souls don’t feel new. They feel remembered.</p>
    <p>If comfort had a name, it would sound like yours.</p>
    <p>Loving you doesn’t feel heavy. It feels right.</p>
    <button onclick="goTo('question')">Almost there 💗</button>
  </div>
</section>

<!-- QUESTION -->
<section id="question">
  <div class="card">
    <h2>If the universe really did plan us…</h2>
    <h1>Will you be my Valentine? 💘</h1>
    <button onclick="goTo('yes')">Yes 💕</button>
    <button onclick="goTo('yes')">Obviously yes 😌</button>
  </div>
</section>

<!-- RESPONSE -->
<section id="yes">
  <div class="card">
    <h1>And of course.</h1>
    <p>Destiny doesn’t get things like this wrong.</p>
    <button onclick="goTo('secret')">One last thing 🌙</button>
  </div>
</section>

<!-- SECRET -->
<section id="secret">
  <div class="card">
    <p>
      If loving you feels this easy,<br>
      if choosing you feels this natural,<br>
      then maybe it was always written.<br><br>

      You are chosen.<br>
      You are loved.<br>
      And somehow, against all odds —<br>
      you are meant to be ✨
    </p>
    <p style="margin-top:20px;">— always, yours. I love you honey🧿❤️</p>
  </div>
</section>

<script>
  let musicStarted = false;

  function goTo(id) {
    if (!musicStarted) {
      const player = document.getElementById("musicPlayer");
      player.src = player.src.replace("autoplay=0", "autoplay=1");
      musicStarted = true;
    }
    document.getElementById(id).scrollIntoView({ behavior: "smooth" });
  }
</script>

</body>
</html>
