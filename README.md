<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shonel.base.eth Coin Dashboard</title>
<style>
  body {
    margin: 0;
    font-family: 'Arial', sans-serif;
    background: #0a0f25;
    color: #00bfff;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .dashboard {
    background: linear-gradient(145deg, #00142a, #002c5c);
    border-radius: 20px;
    padding: 30px;
    text-align: center;
    width: 320px;
    box-shadow: 0 0 30px rgba(0, 191, 255, 0.5);
    transition: transform 0.3s ease;
  }

  .dashboard:hover {
    transform: scale(1.05);
  }

  .coin-img {
    width: 120px;
    margin-bottom: 20px;
    animation: rotate 10s linear infinite;
  }

  @keyframes rotate {
    0% { transform: rotateY(0deg); }
    100% { transform: rotateY(360deg); }
  }

  h2 {
    margin-bottom: 10px;
  }

  .stats {
    margin: 15px 0;
    font-size: 0.95rem;
  }

  .btn {
    display: inline-block;
    padding: 10px 20px;
    background: #00bfff;
    color: #00142a;
    font-weight: bold;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
  }

  .btn:hover {
    background: #0095cc;
    transform: translateY(-3px);
  }
</style>
</head>
<body>

<div class="dashboard">
  <img class="coin-img" src="https://i.ibb.co/7Q7zjBp/A-promotional-digital-digital-image-features-a-blu.png" alt="Shonel.base.eth Coin">
  <h2>Shonel.base.eth Coin</h2>
  <div class="stats">
    💎 Holders: <span id="holders">1,245</span><br>
    🔄 Circulating: <span id="circulating">50,000</span><br>
    ⚡ Recent TX: <span id="tx">23</span>
  </div>
  <a href="https://base.org/" class="btn" target="_blank">Claim / Tip</a>
</div>

<script>
  // Simple dynamic stats animation
  function randomizeStats() {
    document.getElementById('holders').textContent = Math.floor(1200 + Math.random() * 100);
    document.getElementById('circulating').textContent = Math.floor(50000 + Math.random() * 2000);
    document.getElementById('tx').textContent = Math.floor(10 + Math.random() * 20);
  }

  setInterval(randomizeStats, 3000);
</script>

</body>
</html>
