<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For You ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }
    header {
      padding: 60px 20px;
    }
    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }
    p {
      font-size: 1.2rem;
      max-width: 700px;
      margin: auto;
    }
    .heart {
      font-size: 2rem;
      animation: float 2s infinite ease-in-out;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      padding: 40px;
    }
    .gallery img {
      width: 100%;
      height: 280px;
      object-fit: cover;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      transition: transform 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }
    .btn {
      background: #fff;
      color: #ff4d6d;
      border: none;
      padding: 15px 30px;
      font-size: 1.1rem;
      border-radius: 30px;
      cursor: pointer;
      margin-top: 30px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .btn:hover {
      background: #ffe6ec;
    }
    #secret {
      display: none;
      padding: 40px 20px;
      font-size: 1.4rem;
    }
    footer {
      padding: 20px;
      font-size: 0.9rem;
      opacity: 0.8;
    }
  </style>
</head>
<body>
  <header>
    <h1>Hey You ❤️</h1>
    <p>
      From the moment you entered my life, everything felt a little brighter,
      a little warmer, and a lot more special.
    </p>
    <div class="heart">💖</div>
  </header>

  <section class="gallery">
    <!-- Replace these image files with her real photos -->
    <img src="photo1.jpg" alt="Her Photo 1" />
    <img src="photo2.jpg" alt="Her Photo 2" />
    <img src="photo3.jpg" alt="Her Photo 3" />
    <img src="photo4.jpg" alt="Her Photo 4" />
  </section>

  <button class="btn" onclick="showSecret()">Click for a surprise 💌</button>

  <section id="secret">
    <p>
      I don’t know what the future holds,
      but I do know this —
      every smile of yours makes my day better.
      <br /><br />
      Will you be my Valentine? 🌹
    </p>
  </section>

  <footer>
    Made with ❤️ just for you
  </footer>

  <script>
    function showSecret() {
      const secret = document.getElementById('secret');
      secret.style.display = 'block';
      secret.scrollIntoView({ behavior: 'smooth' });
    }

    // Floating hearts effect
    setInterval(() => {
      const heart = document.createElement('div');
      heart.innerText = '❤️';
      heart.style.position = 'fixed';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.bottom = '0';
      heart.style.fontSize = Math.random() * 20 + 20 + 'px';
      heart.style.animation = 'rise 4s linear';
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 4000);
    }, 600);

    const style = document.createElement('style');
    style.innerHTML = `
      @keyframes rise {
        to {
          transform: translateY(-100vh);
          opacity: 0;
        }
      }
    `;
    document.head.appendChild(style);
  </script>
</body>
</html>
