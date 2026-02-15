<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   <link rel="icon" type="image/png" href="img/1.JPG">
  <title>unclick+</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      background: #0049F7;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: "Tahoma";
      font-style: normal;
      color: #FFA6E7;
      cursor: pointer;
      padding: 20px;
    }

    .container {
      text-align: center;
      width: 100%;
      max-width: 500px;
      padding: 24px;
      border-radius: 20px;
      backdrop-filter: blur(10px);
    }

    img {
      width: 100%;
      max-height: 300px;
      object-fit: cover;
      border-radius: 16px;
      margin-bottom: 18px;
    }

    h1 {
      font-size: 1.4rem;
      line-height: 1.4;
      margin: 0;
    }

    p {
      margin-top: 10px;
      opacity: 0.6;
      font-size: 0.8rem;
    }
  </style>
</head>

<body onclick="changeVibe()">
  <div class="container">
  <img id="vibeImage" src="img/1.jpeg" alt="vibe image" />
  <h1 id="phrase">FELIZ 14 DE FEBRERO AMORA <3 </h1>
</div>


<script>
  const phrases = [
    "Yo conozco tu locura porque también es la mía\n\n Somos locas rebeldes\nlocas del estar vivas\nlocas maravillosas\nestrafalarias, floridas",
    "Te amo amora",
    "Feliz 14 de febrero guapa👩🏻‍❤️‍💋‍👩🏽",
    "´Después de todo, qué gusto estar vivas, y juntas´",
    "Te quiero con la eternidad que concede la brevedad de un momento inolvidable.",
    "¡Ay, Amora! No cabe duda: ¡el amor es una cosa esplendorosa!",
    "Eres mi 11:11 de toda la vida"
  ];

  const images = [
    "img/1.JPG",
    "img/2.jpeg",
    "img/3.jpeg",
    "img/4.jpeg",
    "img/5.jpeg",
    "img/6.jpg",
    "img/7.JPG",
    "img/8.jpeg"

  ];

  const phraseEl = document.getElementById("phrase");
  const imageEl = document.getElementById("vibeImage");

  // ESTADO INICIAL ESTÁ MOSTRANDO EL TEXTO
  let showing = "text";
  imageEl.style.display = "none";

  function changeVibe() {
    if (showing === "text") {
      // ocultar el texto
      phraseEl.style.display = "none";

      // mostrar imagen
      imageEl.src = images[Math.floor(Math.random() * images.length)];
      imageEl.style.display = "block";

      showing = "image";
    } else {
      // ocultar imagen
      imageEl.style.display = "none";

      // mostrar texto
      phraseEl.textContent =
        phrases[Math.floor(Math.random() * phrases.length)];
      phraseEl.style.display = "block";

      showing = "text";
    }
  }
</script>

</body>
</html>
