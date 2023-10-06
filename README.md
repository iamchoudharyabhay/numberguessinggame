<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Number Guessing Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }

    #container {
      max-width: 400px;
      margin: 0 auto;
    }

    #guessInput {
      width: 60px;
    }

    #result {
      font-weight: bold;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div id="container">
    <h1>Number Guessing Game</h1>
    <p>Guess a number between 1 and 10:</p>
    <input type="number" id="guessInput" min="1" max="10">
    <button onclick="checkGuess()">Submit Guess</button>
    <p id="result"></p>
  </div>

  <script>
    function checkGuess() {
      var secretNumber = 7; // Change this to set the secret number
      var userGuess = document.getElementById("guessInput").value;

      if (userGuess == secretNumber) {
        document.getElementById("result").innerHTML = "Congratulations! You guessed it!";
      } else {
        document.getElementById("result").innerHTML = "Wrong guess. Try again!";
      }
    }
  </script>
</body>
</html>
