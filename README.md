<!DOCTYPE html>
<html lang="cs">
<head>
  <meta charset="UTF-8">
  <title>Tade Server</title>
  <style>
    body {
      font-family: 'Courier New', monospace;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #2a2a2a;
      color: #fff;
    }

    .main {
      background: url('https://i.imgur.com/3ZQ3mHb.png') no-repeat center center fixed;
      background-size: cover;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    .map {
      background-color: #1e1e1e;
      padding: 20px;
    }

    h1 {
      font-size: 3em;
      color: #4CAF50;
      text-shadow: 2px 2px #000;
    }

    .button {
      display: inline-block;
      padding: 15px 25px;
      margin-top: 20px;
      font-size: 1.2em;
      background-color: #4CAF50;
      color: white;
      text-decoration: none;
      border-radius: 5px;
      box-shadow: 2px 2px 5px #000;
    }

    iframe {
      border: none;
      width: 100%;
      height: 80vh;
    }
  </style>
</head>
<body>
  <div id="content" class="main">
    <h1>Tade Server</h1>
    <a href="#dynmap" class="button">Zobrazit DynMapu</a>
  </div>

  <div id="dynmap" class="map" style="display:none;">
    <h1>DynMapa</h1>
    <iframe src="https://tvujserver.cz:8123"></iframe>
    <br>
    <a href="#" class="button">Zpět</a>
  </div>

  <script>
    const link = document.querySelector('a[href="#dynmap"]');
    const back = document.querySelector('a[href="#"]');
    const main = document.getElementById('content');
    const map = document.getElementById('dynmap');

    link.addEventListener('click', () => {
      main.style.display = 'none';
      map.style.display = 'block';
    });

    back.addEventListener('click', () => {
      map.style.display = 'none';
      main.style.display = 'flex';
    });
  </script>
</body>
</html>
