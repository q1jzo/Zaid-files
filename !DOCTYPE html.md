<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <title>Zaid files</title>  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <style>  
    body {  
      margin: 0;  
      height: 100vh;  
      background: black;  
      display: flex;  
      flex-direction: column;  
      justify-content: center;  
      align-items: center;  
      font-family: Arial, Helvetica, sans-serif;  
    }  
  
    h1 {  
      color: white;  
      font-size: 3rem;  
      margin-bottom: 30px;  
      letter-spacing: 2px;  
    }  
  
    #timer {  
      color: red;  
      font-size: 6rem;  
      font-weight: bold;  
      letter-spacing: 4px;  
    }  
  </style>  
</head>  
<body>  
  
  <h1>Zaid files</h1>  
  <div id="timer">24:00:00</div>  
  
  <script>  
    let timeLeft = 24 * 60 * 60; // 24 hours in seconds  
  
    function updateTimer() {  
      const hours = String(Math.floor(timeLeft / 3600)).padStart(2, '0');  
      const minutes = String(Math.floor((timeLeft % 3600) / 60)).padStart(2, '0');  
      const seconds = String(timeLeft % 60).padStart(2, '0');  
  
      document.getElementById("timer").textContent =  
        `${hours}:${minutes}:${seconds}`;  
  
      if (timeLeft > 0) {  
        timeLeft--;  
      }  
    }  
  
    updateTimer();  
    setInterval(updateTimer, 1000);  
  </script>  
  
</body>  
</html>  
