# -Eira-apology-page
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To My Kawaii Friend, Eira</title>
  <link href="https://fonts.googleapis.com/css2?family=Indie+Flower&family=Patrick+Hand&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Patrick Hand', cursive;
      background: linear-gradient(to bottom, #ffd6f6, #ffe4ec);
      overflow-x: hidden;
      position: relative;
    }

    .sakura {
      position: absolute;
      top: -50px;
      width: 100%;
      height: 100%;
      background-image: url('https://i.ibb.co/zZhdPkp/sakura.png');
      background-repeat: repeat;
      background-size: contain;
      animation: fall 20s linear infinite;
      z-index: 0;
    }

    @keyframes fall {
      0% {background-position: 0 -1000px;}
      100% {background-position: 0 1000px;}
    }

    .container {
      text-align: center;
      padding: 50px 20px;
      z-index: 2;
      position: relative;
    }

    h1 {
      font-size: 3em;
      color: #ff79c6;
      font-family: 'Indie Flower', cursive;
    }

    .chibi {
      width: 150px;
      margin-bottom: 20px;
    }

    .message {
      font-size: 1.4em;
      color: #333;
      max-width: 600px;
      margin: 0 auto;
    }

    .button {
      margin-top: 30px;
      padding: 12px 30px;
      background: #ff95d3;
      color: white;
      border: none;
      border-radius: 30px;
      font-size: 1.2em;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .button:hover {
      background: #ff60b7;
      transform: scale(1.05);
    }

    .popup {
      display: none;
      font-size: 1.5em;
      color: #ff5d8f;
      margin-top: 20px;
    }

    .cat-mascot {
      position: fixed;
      width: 60px;
      pointer-events: none;
      z-index: 999;
      transition: transform 0.1s ease;
    }
  </style>
</head>
<body>
  <div class="sakura"></div>
  <div class="container">
    <img class="chibi" src="https://i.ibb.co/FVxmt0M/sad-chibi-girl.png" alt="Chibi Girl">
    <h1>Gomenasai, Eira-chan...</h1>
    <p class="message">
      I’m really sorry if I made you sad. It was never my intention, and I miss your smile more than words can say.
      You're like the sunshine in my anime world — and without you, everything feels a little less sparkly.
    </p>
    <button class="button" onclick="showPopup()">Forgive Me?</button>
    <div class="popup" id="popup">Thank you, Eira! You’re the best friend anyone could wish for!</div>
  </div>
  <img src="https://i.ibb.co/YcZKNrg/cat-cursor.png" alt="Cat Mascot" class="cat-mascot" id="cat">
  <audio id="bg-music" loop>
    <source src="https://cdn.pixabay.com/audio/2022/03/23/audio_10f2fcf39e.mp3" type="audio/mpeg">
  </audio>
  <script>
    const popup = document.getElementById('popup');
    function showPopup() {
      popup.style.display = 'block';
    }

    const cat = document.getElementById("cat");
    document.addEventListener("mousemove", (e) => {
      cat.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
    });

    // Auto-play background music
    window.addEventListener("click", () => {
      document.getElementById("bg-music").play();
    }, { once: true });
  </script>
</body>
</html>
