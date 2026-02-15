<DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   <link rel="icon" type="image/png" href="img/1.JPG">
  <title>sanvalentinjjj</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      <audio controls autoplay="true" loop="true"> 
         <source src="teamo.mp3" type="audio"> 
      </audio>
      margin: 0;
      min-height: 100vh;
      background: #0049f7;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: "Tahoma";
      font-style: normal;
      color: #f4cbe5;
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
  <img id="vibeImage" src="ktorc.png" alt="vibe image" />
  <h1 id="phrase">felis 14 de febrero mi princesita <3 </h1>
</div>


<script>
  const phrases = [
    "te amo demasiado avrii",
    "felis 14 divina",
    "te amo y te voy a amar por siempre, eres el amor de mi vida",
    "eres mi 11:11 para toda la vida",
    "El Destino, hechizado, te sigue tus pisadas; tú siembras a tu paso desgracias y alegrías, tú lo gobiernas todo sin responder de nada."
    "ha pasado ya medio año y sigo queriendote y amandote como la primera vez, aún recuerdo la primera vez que te ví, me         pareciste tan hermosa que te presumí con el único amigo que tenía en ese momento, y al pasar los días te veo incluso        más preciosa que nunca, eres y siempre serás el amor de mi vida avri. quiero estar contigo para siempre"
  ];

  const images = [
    "ktorc.png",
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
