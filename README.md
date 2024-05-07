<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hacked</title>
<style>
  body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: red;
    animation: blinkBackground 1s infinite;
  }

  @keyframes blinkBackground {
    0% {
      background-color: red;
    }
    50% {
      background-color: black;
    }
    100% {
      background-color: red;
    }
  }

  .message {
    font-size: 30px;
    color: white;
    text-align: center;
    margin-bottom: 20px;
  }

  .info {
    font-size: 16px;
    color: white;
    text-align: center;
    margin-bottom: 20px;
  }

  .pay-now-button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 20px 40px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 20px;
    cursor: pointer;
    border-radius: 10px;
    transition: background-color 0.3s;
    position: fixed;
    bottom: 20px;
  }

  .pay-now-button:hover {
    background-color: #45a049;
  }

  /* Modifie le style du body lorsque le lien est ouvert en plein écran */
  body.fullscreen {
    justify-content: flex-start;
    height: 100vh;
  }

  /* Modifie le style du message lorsque le lien est ouvert en plein écran */
  .fullscreen .message {
    margin-top: 100px;
  }

  /* Modifie le style du bouton lorsque le lien est ouvert en plein écran */
  .fullscreen .pay-now-button {
    bottom: 40px;
  }
</style>
</head>
<body onclick="openFullscreen()">
<div class="message">You've been hacked</div>
<div class="info">Your computer has been infected with a virus. Your operating system, all your files, passwords are lost. This is the only screen you can access, even if you restart your device.<br>We are sorry for the inconvenience and damage this may have caused.</div>
<a href="https://pranx.com/" class="pay-now-button">Pay now</a>
<script>
  function openFullscreen() {
    var elem = document.documentElement;
    if (elem.requestFullscreen) {
      elem.requestFullscreen();
    } else if (elem.webkitRequestFullscreen) { /* Safari */
      elem.webkitRequestFullscreen();
    } else if (elem.msRequestFullscreen) { /* IE11 */
      elem.msRequestFullscreen();
    }

    // Ajoute la classe "fullscreen" au body lorsqu'il est en plein écran
    document.body.classList.add('fullscreen');
  }
</script>
</body>
</html>
