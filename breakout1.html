<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Breakout Game</title>
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100vh;
      background-color: #1d1d1d;
      color: #fff;
      text-align: center;
    }

    h1 {
      position: absolute;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 2.5rem;
      color: #f3f3f3;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
    }

    canvas {
      border: 2px solid #f3f3f3;
      background-color: #222;
      border-radius: 10px;
    }

    #score, #lives {
      font-size: 1.2rem;
      font-weight: bold;
      color: #00e5ff;
      position: absolute;
      top: 20px;
      font-family: 'Roboto', sans-serif;
    }

    #score {
      left: 20px;
    }

    #lives {
      right: 20px;
    }

    .button {
      padding: 10px 20px;
      margin-top: 20px;
      background-color: #00e5ff;
      border: none;
      border-radius: 5px;
      font-size: 1.2rem;
      color: #1d1d1d;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .button:hover {
      background-color: #0091c7;
    }

    /* Button container for left and right controls */
    .control-buttons {
      display: flex;
      justify-content: center;
      margin-top: 20px;
    }

    .control-buttons button {
      width: 70px;
      height: 70px;
      font-size: 1.5rem;
      margin: 0 15px;
      background-color: #00e5ff;
      border: none;
      border-radius: 50%;
      color: #1d1d1d;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .control-buttons button:hover {
      background-color: #0091c7;
    }
  </style>
</head>
<body>

<h1>Breakout Game</h1>
<canvas id="gameCanvas" width="480" height="320"></canvas>
<div id="score">Punteggio: 0</div>
<div id="lives">Vite: 3</div>

<!-- Game Start Button -->
<button class="button" id="startBtn">Inizia Gioco</button>

<!-- Control Buttons -->
<div class="control-buttons">
  <button id="leftBtn">←</button>
  <button id="rightBtn">→</button>
</div>

<script>
  const canvas = document.getElementById("gameCanvas");
  const ctx = canvas.getContext("2d");

  let ballRadius = 10;
  let x = canvas.width / 2;
  let y = canvas.height - 30;
  let dx = 2;
  let dy = -2;

  let paddleHeight = 10;
  let paddleWidth = 75;
  let paddleX = (canvas.width - paddleWidth) / 2;
  let rightPressed = false;
  let leftPressed = false;

  let brickRowCount = 3;
  let brickColumnCount = 5;
  let brickWidth = 70;
  let brickHeight = 20;
  let brickPadding = 10;
  let brickOffsetTop = 30;
  let brickOffsetLeft = 30;

  let bricks = [];
  for (let c = 0; c < brickColumnCount; c++) {
    bricks[c] = [];
    for (let r = 0; r < brickRowCount; r++) {
      bricks[c][r] = { x: 0, y: 0, status: 1 };
    }
  }

  let score = 0;
  let lives = 3;

  // Hide the start button after game start
  document.getElementById('startBtn').addEventListener('click', startGame);

  document.addEventListener("keydown", keyDownHandler, false);
  document.addEventListener("keyup", keyUpHandler, false);

  // Control buttons functionality
  document.getElementById('leftBtn').addEventListener('click', () => movePaddle('left'));
  document.getElementById('rightBtn').addEventListener('click', () => movePaddle('right'));

  function startGame() {
    document.getElementById('startBtn').style.display = "none"; // Hide button on start
    draw();
  }

  function keyDownHandler(e) {
    if (e.key == "Right" || e.key == "ArrowRight") {
      rightPressed = true;
    } else if (e.key == "Left" || e.key == "ArrowLeft") {
      leftPressed = true;
    }
  }

  function keyUpHandler(e) {
    if (e.key == "Right" || e.key == "ArrowRight") {
      rightPressed = false;
    } else if (e.key == "Left" || e.key == "ArrowLeft") {
      leftPressed = false;
    }
  }

  function movePaddle(direction) {
    if (direction === 'left' && paddleX > 0) {
      paddleX -= 7;
    } else if (direction === 'right' && paddleX < canvas.width - paddleWidth) {
      paddleX += 7;
    }
  }

  function collisionDetection() {
    for (let c = 0; c < brickColumnCount; c++) {
      for (let r = 0; r < brickRowCount; r++) {
        let b = bricks[c][r];
        if (b.status == 1) {
          if (x > b.x && x < b.x + brickWidth && y > b.y && y < b.y + brickHeight) {
            dy = -dy;
            b.status = 0;
            score++;
            if (score == brickRowCount * brickColumnCount) {
              alert("Hai vinto! Premi OK per continuare a giocare.");
              document.location.reload();
            }
          }
        }
      }
    }
  }

  function drawBall() {
    ctx.beginPath();
    ctx.arc(x, y, ballRadius, 0, Math.PI * 2);
    ctx.fillStyle = "#00e5ff";
    ctx.fill();
    ctx.closePath();
  }

  function drawPaddle() {
    ctx.beginPath();
    ctx.rect(paddleX, canvas.height - paddleHeight, paddleWidth, paddleHeight);
    ctx.fillStyle = "#00e5ff";
    ctx.fill();
    ctx.closePath();
  }

  function drawBricks() {
    for (let c = 0; c < brickColumnCount; c++) {
      for (let r = 0; r < brickRowCount; r++) {
        if (bricks[c][r].status == 1) {
          let brickX = c * (brickWidth + brickPadding) + brickOffsetLeft;
          let brickY = r * (brickHeight + brickPadding) + brickOffsetTop;
          bricks[c][r].x = brickX;
          bricks[c][r].y = brickY;
          ctx.beginPath();
          ctx.rect(brickX, brickY, brickWidth, brickHeight);
          ctx.fillStyle = "#ff4081";
          ctx.fill();
          ctx.closePath();
        }
      }
    }
  }

  function drawScore() {
    document.getElementById('score').textContent = "Punteggio: " + score;
  }

  function drawLives() {
    document.getElementById('lives').textContent = "Vite: " + lives;
  }

  function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    drawBricks();
    drawBall();
    drawPaddle();
    drawScore();
    drawLives();
    collisionDetection();

    if (x + dx > canvas.width - ballRadius || x + dx < ballRadius) {
      dx = -dx;
    }
    if (y + dy < ballRadius) {
      dy = -dy;
    } else if (y + dy > canvas.height - ballRadius) {
      if (x > paddleX && x < paddleX + paddleWidth) {
        dy = -dy;
      } else {
        lives--;
        if (lives == 0) {
          alert("GAME OVER");
          document.location.reload();
        } else {
          x = canvas.width / 2;
          y = canvas.height - 30;
          dx = 2;
          dy = -2;
          paddleX = (canvas.width - paddleWidth) / 2;
        }
      }
    }

    x += dx;
    y += dy;
    requestAnimationFrame(draw);
  }
</script>

</body>
</html>