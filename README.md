<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ошибка</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #000;
      color: white;
      font-family: Arial, sans-serif;
    }

    .error {
      text-align: center;
    }

    .error h1 {
      font-size: 50px;
      margin-bottom: 30px;
    }

    button {
      padding: 15px 35px;
      border: none;
      border-radius: 10px;
      background: white;
      color: black;
      font-size: 18px;
      cursor: pointer;
    }

    button:hover {
      opacity: 0.8;
    }

    .loading {
      display: none;
      text-align: center;
    }

    .loading h1 {
      font-size: 35px;
      margin-bottom: 25px;
    }

    .spinner {
      width: 60px;
      height: 60px;
      margin: auto;
      border: 5px solid #333;
      border-top: 5px solid white;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }
  </style>
</head>

<body>

  <div class="error" id="error">
    <h1>Ошибка</h1>

    <button onclick="startLoading()">
      Перейти на сайт
    </button>
  </div>

  <div class="loading" id="loading">
    <h1>Загрузка...</h1>

    <div class="spinner"></div>
  </div>

  <script>
    function startLoading() {
      document.getElementById("error").style.display = "none";
      document.getElementById("loading").style.display = "block";

      setTimeout(function() {
        window.location.href = "https://example.com";
      }, 5000);
    }
  </script>

</body>
</html>
