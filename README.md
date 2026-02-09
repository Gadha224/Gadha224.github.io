<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Be My Valentine 🤍</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: "Comic Sans MS", cursive, sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
    }

    h1 {
      margin-bottom: 30px;
      color: #ff4d6d;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    #yesBtn {
      background-color: #ff4d6d;
      color: white;
      margin-right: 20px;
    }

    #yesBtn:hover {
      transform: scale(1.1);
    }

    #noBtn {
      background-color: #ccc;
      color: #333;
      position: absolute;
    }

    #message {
      margin-top: 20px;
      font-size: 18px;
      color: #ff4d6d;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Will you be my Valentine, Motiii? 🤍</h1>
    <button id="yesBtn">Yes 💕</button>
    <button id="noBtn">No 💔</button>
    <div id="message"></div>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const message = document.getElementById("message");
    const yesBtn = document.getElementById("yesBtn");

    const messages = [
      "Nice try 😏",
      "I know that's your fav. word",
      "You can't escape 😘",
      "Almost had it 😂",
      "Just say yes 💕"
    ];

    noBtn.addEventListener("mouseenter", () => {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);

      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;

      message.textContent =
        messages[Math.floor(Math.random() * messages.length)];

    yesBtn.addEventListener("click", () => {
      document.body.innerHTML = `
        <div style="
          height:100vh;
          display:flex;
          align-items:center;
          justify-content:center;
          background:linear-gradient(135deg,#ff9a9e,#fad0c4);
          font-family:'Comic Sans MS', cursive;
          text-align:center;
        ">
          <h1 style="color:#ff4d6d;">
            YAYYY 🤍🥰<br>
            I knew you'd say yes!
          </h1>
        </div>
      `;
    });
  </script>

</body>
</html>
