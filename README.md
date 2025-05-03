# Birthday
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nature Greeting Card</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb') no-repeat center center fixed;
      background-size: cover;
      font-family: 'Segoe UI', sans-serif;
      color: white;
      text-align: center;
      overflow: hidden;
    }

    .card {
      padding: 30px;
      margin: 50px auto;
      background: rgba(0, 0, 0, 0.5);
      border-radius: 20px;
      max-width: 600px;
    }

    h1 {
      font-size: 2.5em;
      margin-bottom: 10px;
    }

    .flower {
      display: inline-block;
      margin: 10px;
      padding: 15px;
      background: rgba(255, 255, 255, 0.2);
      border: 2px solid white;
      border-radius: 50%;
      width: 100px;
      height: 100px;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .flower:hover {
      transform: scale(1.1);
    }

    .message-box {
      margin-top: 20px;
      font-size: 1.2em;
      background: rgba(0, 0, 0, 0.6);
      padding: 15px;
      border-radius: 10px;
    }

    .butterfly {
      position: absolute;
      width: 60px;
      top: 50%;
      left: -80px;
      animation: fly 12s linear infinite;
    }

    @keyframes fly {
      0% {
        transform: translateY(0) rotate(0deg);
      }
      50% {
        transform: translateY(-100px) rotate(180deg);
      }
      100% {
        left: 100%;
        transform: translateY(0) rotate(360deg);
      }
    }
  </style>
</head>
<body>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Papilio_machaon_Linnaeus_1758_Machaon.jpg/2560px-Papilio_machaon_Linnaeus_1758_Machaon.jpg" alt="butterfly" class="butterfly" />

  <div class="card">
    <h1>Happy Nature Day, Friend! 🌼</h1>
    <p>Click a flower to reveal a surprise message!</p>

    <div class="flower" onclick="showMessage('Wishing you peace and sunshine today! ☀️')">🌸</div>
    <div class="flower" onclick="showMessage('May your path be filled with wildflowers! 🌿')">🌼</div>
    <div class="flower" onclick="showMessage('Breathe in nature, exhale joy 🌳')">🌺</div>

    <div class="message-box" id="messageBox"></div>
  </div>

  <script>
    function showMessage(msg) {
      document.getElementById("messageBox").textContent = msg;
    }
  </script>
</body>
</html>
