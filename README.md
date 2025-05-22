# Poema-codificado
<!DOCTYPE html><html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Poema em Código</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Courier New', monospace;
      background: linear-gradient(to bottom, #f5f5f5, #e0e0e0);
      color: #333;
      text-align: center;
    }
    .container {
      padding: 20px;
      max-width: 800px;
      margin: auto;
    }
    .typing {
      border-right: .1em solid #666;
      white-space: pre-wrap;
      overflow: hidden;
      font-size: 1.2em;
      margin-bottom: 20px;
      min-height: 150px;
    }
    button {
      background-color: #444;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1em;
      margin: 10px;
    }
    .photo {
      width: 100%;
      max-width: 500px;
      border-radius: 16px;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="foto1_estilizada.jpg" alt="Foto Estilizada" class="photo" />
    <img src="foto2_romantica.jpg" alt="Foto Romântica" class="photo" /><div class="typing" id="typing"></div>
<button onclick="revealNext()">Revelar próximo verso</button>

<audio id="bgmusic" controls autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/10/26/audio_f25a0b59f3.mp3?filename=memories-122009.mp3" type="audio/mpeg">
  Seu navegador não suporta áudio.
</audio>

  </div>  <script>
    const versos = [
      'if (vida.te_provar()) {',
      '  console.log("Deus sempre sustentou.");',
      '  while (fé > medo) {',
      '    coragem++;',
      '    amor.continua();',
      '  }',
      '}',
      '',
      'if (meta == alcançada) {',
      '  console.log("Eu sempre soube da sua capacidade.");',
      '  console.log("Orgulho define.");',
      '}',
      '',
      '// Com amor, da sua eterna apoiadora.'
    ];

    let index = 0;
    const typingDiv = document.getElementById("typing");

    function revealNext() {
      if (index < versos.length) {
        let line = versos[index];
        let i = 0;
        const interval = setInterval(() => {
          if (i < line.length) {
            typingDiv.innerHTML += line.charAt(i);
            i++;
          } else {
            typingDiv.innerHTML += "\n";
            clearInterval(interval);
            index++;
          }
        }, 40);
      }
    }
  </script></body>
</html>
