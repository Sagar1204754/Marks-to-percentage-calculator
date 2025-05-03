# Marks-to-percentage-calculator
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Marks to Percentage Calculator</title>
  <style>
    body {
      background-color: #f0f8ff;
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    input, button {
      padding: 10px;
      margin: 10px;
      font-size: 16px;
    }
    .result {
      font-weight: bold;
      margin-top: 20px;
      color: #007BFF;
    }
  </style>
</head>
<body>

  <h1>Marks to Percentage Calculator</h1>

  <input type="number" id="obtained" placeholder="Obtained Marks">
  <input type="number" id="total" placeholder="Total Marks">
  <br>
  <button onclick="calculate()">Calculate Percentage</button>

  <div class="result" id="output"></div>

  <script>
    function calculate() {
      const obtained = parseFloat(document.getElementById("obtained").value);
      const total = parseFloat(document.getElementById("total").value);
      const output = document.getElementById("output");

      if (isNaN(obtained) || isNaN(total) || total === 0) {
        output.textContent = "Please enter valid numbers.";
        return;
      }

      const percentage = (obtained / total) * 100;
      output.textContent = "Percentage: " + percentage.toFixed(2) + "%";
    }
  </script>

</body>
</html>
