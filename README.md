# Beyza-LOVE.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>For You ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      font-family: 'Georgia', serif;
      background: #fff;
      text-align: center;
    }

    .screen {
      display: none;
      padding: 20px;
      min-height: 100vh;
      box-sizing: border-box;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    .active {
      display: flex;
    }

    img {
      max-width: 90%;
      cursor: pointer;
      transition: transform 0.4s ease;
    }

    img:hover {
      transform: scale(1.05);
    }

    .letter {
      width: 200px;
    }

    .page {
      background: #ffffff;
      border: 1px solid #eee;
      padding: 30px;
      max-width: 600px;
    }

    .address {
      text-align: left;
      margin-bottom: 40px;
      font-size: 16px;
    }

    .message {
      color: #9bbcff; /* light blue */
      font-size: 18px;
      line-height: 1.6;
    }

    .flowers {
      margin: 20px 0;
      font-size: 24px;
    }
  </style>
</head>
<body>

  <!-- Screen 1: Bouquet -->
  <div id="screen1" class="screen active">
    <img src="https://i.imgur.com/0Z8FQYF.png" alt="Bouquet" onclick="goTo(2)" />
    <p>Tap the bouquet 💐</p>
  </div>

  <!-- Screen 2: Letter -->
  <div id="screen2" class="screen">
    <img class="letter" src="https://i.imgur.com/YZ6X9mS.png" alt="Letter" onclick="goTo(3)" />
    <p>Tap the letter ✉️</p>
  </div>

  <!-- Screen 3: Open Letter -->
  <div id="screen3" class="screen">
    <div class="page" onclick="goTo(4)">
      <div class="address">
        <strong>To:</strong> Her Name<br />
        Her Address<br />
        City, Country
      </div>
      <p>(Tap to open)</p>
    </div>
  </div>

  <!-- Screen 4: Message -->
  <div id="screen4" class="screen">
    <div class="page">
      <div class="flowers">🌸🌹🌸🌹🌸</div>
      <div class="message">
        Your text goes here.
        <br /><br />
        Write your love letter exactly how you want it ❤️
      </div>
      <div class="flowers">🌸🌹🌸🌹🌸</div>
    </div>
  </div>

  <script>
    function goTo(n) {
      document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
      document.getElementById('screen' + n).classList.add('active');
    }
  </script>

</body>
</html>
