<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mars Transfer Program</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: black;
      color: #00ffcc;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      text-align: center;
      max-width: 500px;
    }
    button {
      padding: 12px 20px;
      font-size: 16px;
      border: none;
      background: #00ffcc;
      color: black;
      cursor: pointer;
      margin-top: 20px;
      border-radius: 6px;
    }
    #progress {
      width: 100%;
      background: #222;
      margin-top: 20px;
      height: 20px;
      border-radius: 10px;
      overflow: hidden;
      display: none;
    }
    #bar {
      height: 100%;
      width: 0%;
      background: #00ffcc;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🚀 Mars Transfer Program</h1>
    <p>Congratulations! You've been randomly selected for a one-way trip to Mars.</p>
    <button onclick="startPrank()">Accept Mission</button><div id="progress">
  <div id="bar"></div>
</div>

<p id="status"></p>

  </div>  <script>
    function startPrank() {
      document.querySelector("button").style.display = "none";
      document.getElementById("progress").style.display = "block";
      let bar = document.getElementById("bar");
      let status = document.getElementById("status");
      let width = 0;

      let messages = [
        "Scanning DNA...",
        "Packing your belongings...",
        "Saying goodbye to Earth...",
        "Calculating trajectory...",
        "Uploading consciousness...",
        "Finalizing transfer..."
      ];

      let i = 0;

      let interval = setInterval(() => {
        if (width >= 100) {
          clearInterval(interval);
          status.innerHTML = "🚨 ERROR: You are too broke to go to Mars. Mission canceled.";
          document.body.style.background = "darkred";
        } else {
          width++;
          bar.style.width = width + "%";

          if (width % 15 === 0 && i < messages.length) {
            status.innerHTML = messages[i];
            i++;
          }
        }
      }, 50);
    }
  </script></body>
</html># MARS-1
MARS BY ANGELO
