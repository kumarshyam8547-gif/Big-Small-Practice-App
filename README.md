DOCTYPE html>
<html>
<head>
<title>Color Prediction</title>
<style>
body { text-align: center; font-family: Arial; }
.box { width: 100px; height: 100px; margin: 20px auto; display: inline-block; }
.red { background-color: red; }
.green { background-color: green; }
</style>
</head>
<body>
<h1>Color Prediction Game</h1>
<div id="colorBox" class="box red"></div>
<p>Guess the next color!</p>
<button onclick="predict('red')">Red</button>
<button onclick="predict('green')">Green</button>
<p id="result"></p>
<script>
function predict(choice) {
const colors = ['red', 'green'];
const randomColor = colors[Math.floor(Math.random() * colors.length)];
const box = document.getElementById('colorBox');
box.className = 'box ' + randomColor;
if (choice === randomColor) {
document.getElementById('result').innerText = 'You Win!';
} else {
document.getElementById('result').innerText = 'Try Again!';
}
}
</script>
</body>
</
