<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
    }

    #heart {
      width: 100px;
      height: 100px;
      background-color: red;
      position: relative;
      transform: rotate(-45deg);
      cursor: pointer;
      transition: transform 0.5s ease-out;
    }

    #heart::before,
    #heart::after {
      content: '';
      width: 100px;
      height: 100px;
      background-color: red;
      border-radius: 50%;
      position: absolute;
    }

    #heart::before {
      top: -50px;
      left: 0;
    }

    #heart::after {
      top: 0;
      left: 50px;
    }

    #heart.clicked {
      transform: scale(1.5) rotate(-45deg);
      transition: transform 0.5s ease-in;
    }
  </style>
</head>
<body>

<div id="heart"></div>

<script>
  document.getElementById('heart').addEventListener('click', function() {
    this.classList.add('clicked');
  });
</script>

</body>
</html>
