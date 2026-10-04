<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>FL!P</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: #071525;
      color: white;
      min-height: 100vh;
      transition: 0.6s ease;
    }

    body.flipped {
      background: #d9f4f7;
      color: #071525;
    }

    .page {
      width: 100%;
      max-width: 430px;
      min-height: 100vh;
      margin: auto;
      padding: 45px 22px 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    /* LOGO */

    .logo-container {
      width: 170px;
      height: 170px;
      perspective: 1000px;
      cursor: pointer;
      margin-top: 20px;
      margin-bottom: 28px;
    }

    .logo {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.7s ease;
    }

    .logo.flipped {
      transform: rotateY(180deg);
    }

    .logo-side {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .logo-side img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }

    .logo-back {
      transform: rotateY(180deg);
      font-size: 55px;
      font-weight: 900;
      letter-spacing: -5px;
    }

    /* TEXT */

    .headline {
      text-align: center;
      margin-bottom: 8px;
      font-size: 13px;
      letter-spacing: 4px;
      opacity: 0.7;
    }

    .title {
      text-align: center;
      font-size: 25px;
      font-weight: 800;
      margin-bottom: 7px;
    }

    .subtitle {
      text-align: center;
      font-size: 12px;
      opacity: 0.6;
      margin-bottom: 30px;
    }

    /* LINKS */

    .links {
      width: 100%;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .link {
      width: 100%;
      padding: 17px 20px;
      border: 1px solid rgba(255,255,255,0.25);
      color: white;
      text-decoration: none;
      text-align: center;
      font-size: 13px;
      font-weight: bold;
      letter-spacing: 2px;
      transition: 0.3s ease;
      background: rgba(255,255,255,0.03);
    }

    .link:hover {
      transform: translateY(-3px);
      background: white;
      color: #071525;
    }

    body.flipped .link {
      color: #071525;
      border-color: rgba(7,21,37,0.25);
      background: rgba(7,21,37,0.04);
    }

    body.flipped .link:hover {
      background: #071525;
      color: white;
    }

    /* DISCOUNT */

    .discount {
      width: 100%;
      margin-top: 25px;
      padding: 20px;
      border: 1px dashed rgba(255,255,255,0.3);
      text-align: center;
    }

    body.flipped .discount {
      border-color: rgba(7,21,37,0.3);
    }

    .discount-small {
      font-size: 10px;
      letter-spacing: 2px;
      opacity: 0.6;
      margin-bottom: 8px;
    }

    .discount-code {
      font-size: 22px;
      font-weight: 900;
      letter-spacing: 4px;
    }

    /* FOOTER */

    .footer {
      margin-top: auto;
      padding-top: 40px;
      font-size: 9px;
      letter-spacing: 3px;
      opacity: 0.45;
      text-align: center;
    }

    .flip-hint {
      margin-top: 15px;
      font-size: 9px;
      letter-spacing: 2px;
      opacity: 0.45;
      text-align: center;
    }

    @media (max-width: 360px) {
      .logo-container {
        width: 145px;
        height: 145px;
      }

      .title {
        font-size: 22px;
      }
    }
  </style>
</head>

<body>

  <div class="page">

    <!-- LOGO -->
    <div class="logo-container" onclick="flipLogo()">

      <div class="logo" id="logo">

        <!-- FRONT -->
        <div class="logo-side">
          <img src="logo.png" alt="FL!P Logo">
        </div>

        <!-- BACK -->
        <div class="logo-side logo-back">
          FL!P
        </div>

      </div>

    </div>


    <!-- TEXT -->

    <div class="headline">
      YOU'VE REACHED
    </div>

    <div class="title">
      FL!P
    </div>

    <div class="subtitle">
      YOUR DESTINATION
    </div>


    <!-- LINKS -->

    <div class="links">

      <a class="link" href="YOUR-SHOP-LINK" target="_blank">
        SHOP FL!P
      </a>

      <a class="link" href="YOUR-INSTAGRAM-LINK" target="_blank">
        INSTAGRAM
      </a>

      <a class="link" href="YOUR-TIKTOK-LINK" target="_blank">
        TIKTOK
      </a>

      <a class="link" href="YOUR-CONTACT-LINK" target="_blank">
        CONTACT
      </a>

    </div>


    <!-- DISCOUNT -->

    <div class="discount">

      <div class="discount-small">
        FL!P CODE
      </div>

      <div class="discount-code">
        FLIP10
      </div>

    </div>


    <div class="flip-hint">
      TAP THE LOGO TO FLIP
    </div>


    <!-- FOOTER -->

    <div class="footer">
      FLIP THE SCRIPT.
    </div>

  </div>


  <script>

    function flipLogo() {

      const logo = document.getElementById("logo");

      logo.classList.toggle("flipped");

      document.body.classList.toggle("flipped");

    }

  </script>

</body>
</html>
