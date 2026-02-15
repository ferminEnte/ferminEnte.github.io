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
  <h1 id="phrase">felis 14 de febrero mi princesita <3  </h1>
</div>


<script>
  const phrases = [
   "te amo demasiado avrii",
    "felis 14 divina",
    "te amo y te voy a amar por siempre, eres el amor de mi vida",
    "eres mi 11:11 para toda la vida",
    "El Destino, hechizado, te sigue tus pisadas; tu siembras a tu paso desgracias y alegrias, tu lo gobiernas todo sin responder de nada."
    "ha pasado ya seis meses y sigo queriendote y amandote como la primera vez, aun recuerdo la primera vez que te vi, me pareciste tan hermosa que te presumi con el unico amigo que tenia en ese momento, y al pasar los dias te veo incluso mas preciosa que nunca, eres y siempre seras el amor de mi vida avri. quiero estar contigo para siempre"
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
