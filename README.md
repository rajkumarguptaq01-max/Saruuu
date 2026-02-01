<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💖</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      background: #f8c8dc;
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .card {
      background: #fff;
      padding: 30px;
      border-radius: 16px;
      text-align: center;
      width: 320px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    .emoji {
      font-size: 50px;
    }

    h2 {
      margin: 15px 0 25px;
    }

    button {
      padding: 10px 25px;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      cursor: pointer;
      margin: 10px;
    }

    #yesBtn {
      background: #ff4d6d;
      color: white;
    }

    #noBtn {
      background: #ddd;
      position: absolute;
    }

    img {
      width: 100%;
      border-radius: 12px;
      margin-top: 15px;
    }
  </style>
</head>

<body>

  <div class="card" id="card">
    <div class="emoji">🐶💗</div>
    <h2><span id="name">Saruuu</span>, will you be my Valentine?</h2>

    <button id="yesBtn">Yes</button>
    <button id="noBtn">No</button>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const card = document.getElementById("card");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    yesBtn.addEventListener("click", () => {
      card.innerHTML = `
        <h2>YAY!! 🎉💖</h2>
        <p>You just made my day 🥹</p>
        <img src="https://media.giphy.com/media/26ufdipQqU2lhNA4g/giphy.gif">
      `;
    });
  </script>

</body>
</html>
