
<html>
<head>
<title>Temperature degree Conversions</title>
<link rel="icon" href="C:\Users\manik\Downloads\tfavi.ico">
</head>
<style>
	* {
		margin: 0;
		padding: 0;
		font-family: Verdana, Geneva, Tahoma, sans-serif;
	   }
	   .bimage{
	   background-image: linear-gradient(rgba(0,0,0,0.5),rgba(0, 0, 0, 0.5)),url("https://wallpapercave.com/wp/wp6946084.jpg");
      /background-image: url();/
      background-repeat: no-repeat;
      background-size: cover;
      height:100vh;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      font-style:oblique;
      font-size:40px;
	}
	.ground {
		width: 100%;
		height: 100vh;
		background-color:
		linear-gradient(rgb(140, 219, 140), rgb(20, 141, 20));
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	
	.ground h1 {
		color: black;
		font-weight: 800;
		font-size: 30px;
		text-align: center;
	}
	
	.converter-row {
		display: flex;
		width: 30%;
		justify-content: space-between;
		align-items: center;
		border-radius: 10px;
		padding: 50px 20px;
	}
	.converter-roww {
		display: flex;
		width: 30%;
		justify-content: space-between;
		align-items: center;
		border-radius: 10px;
		padding: 50px 20px;
	}
	
	.col {
		flex-basis: 32%;
		text-align: center;
	}
	
	.col label {
		font-size: 15px;
		font-weight: 500;
		margin-bottom: 10px;
		color: #fff;
	}
	
	.col input {
		width: 150px;
		height: 30px;
		background: #CAE7DF;
		border-radius: 5px;
		text-align: center;
	}
</style>
<body>
<div class="bimage">
    <div class="ground">
		<bold>Temperature degree Conversions</bold></h1>
	<div class="converter-row">
		<div class="col">
			<label>Fahrenheit</label>
			<input type="number" id="fahrenheit">
		</div>
		<div class="col">
			<label>Celsius</label>
			<input type="number" id="celsius"></br>
		</div>
		<div class="col">
			<label>Kelvin</label>
			<input type="number" id="kelvin">
		</div>

	</div>
	</div>
</div>

<script>
	let celsius = document.getElementById('celsius');
	let fahrenheit = document.getElementById('fahrenheit');
	let kelvin = document.getElementById('kelvin');
	celsius.oninput = function () {
		let f = (parseFloat(celsius.value) * 9) / 5 + 32;
		fahrenheit.value = parseFloat(f.toFixed(2));
	
		let k = (parseFloat(celsius.value) + 273.15);
		kelvin.value = parseFloat(k.toFixed(2));
	}
	fahrenheit.oninput = function () {
		let c = ((parseFloat(
			fahrenheit.value) - 32) * 5) / 9;
		celsius.value = parseFloat(c.toFixed(2));
	
		let k = (parseFloat(
			fahrenheit.value) - 32) * 5 / 9 + 273.15;
		kelvin.value = parseFloat(k.toFixed(2));
     }
	kelvin.oninput = function () {
		let f = (parseFloat(
			kelvin.value) - 273.15) * 9 / 5 + 32;
		fahrenheit.value = parseFloat(f.toFixed(2));
	
		let c = (parseFloat(kelvin.value) - 273.15);
		celsius.value = parseFloat(c.toFixed(2));
	}
	 
</script>
</body>
</html>
