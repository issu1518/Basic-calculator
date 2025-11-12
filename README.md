# Basic-calculator
<!DOCTYPE html>
<html>
<head>
  <title>Basic Calculator</title>
  
</head>
<body>

  <h2>Basic Calculator</h2>

  <input type="number" id="num1" placeholder="Enter first number">
  <input type="number" id="num2" placeholder="Enter second number"><br>

  <button onclick="calculate('add')">Add</button>
  <button onclick="calculate('subtract')">Subtract</button>
  <button onclick="calculate('multiply')">Multiply</button>
  <button onclick="calculate('divide')">Divide</button>

  <h3>Result: <span id="result">---</span></h3>

  <script>
    function calculate(operation) {
      const num1 = parseFloat(document.getElementById('num1').value);
      const num2 = parseFloat(document.getElementById('num2').value);
      let result;

      if (isNaN(num1) || isNaN(num2)) {
        result = 'Please enter valid numbers';
      } else {
        switch (operation) {
          case 'add':
            result = num1 + num2;
            break;
          case 'subtract':
            result = num1 - num2;
            break;
          case 'multiply':
            result = num1 * num2;
            break;
          case 'divide':
            result = num2 !== 0 ? num1 / num2 : 'Cannot divide by zero';
            break;
        }
      }

      document.getElementById('result').textContent = result;
    }
  </script>

</body>
</html>
