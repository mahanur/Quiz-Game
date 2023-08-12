# Quiz-Game
<!DOCTYPE html>
<html>
<head>
	<title>Quiz Game</title>
	<style>
		body {
			background-color: skyblue;
			font-family: Arial, sans-serif;
		}
		h1 {
			text-align: center;
			color: #333;
		}
		form {
			margin: auto;
			width: 50%;
			padding: 20px;
			background-color: #fff;
			border-radius: 5px;
			box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
		}
		label {
			font-size: 18px;
			font-weight: bold;
			display: block;
			margin-bottom: 10px;
			color: #333;
		}
		input[type="submit"] {
			background-color: #4CAF50;
			color: #fff;
			padding: 10px 20px;
			border: none;
			border-radius: 3px;
			cursor: pointer;
			font-size: 16px;
			margin-top: 20px;
		}
		input[type="submit"]:hover {
			background-color: #3e8e41;
		}
	</style>
</head>
<body>
	<h1>Quiz Game with Maha</h1>
	<form>
		<label>******Who will be gainer?*******</label>
		<label>Enter your name:</label>
		<input type="text" name="name" required><br><br>
		<label>1. Which one is mutable?</label>
		<input type="radio" name="q1" value="a" required> a. list<br>
		<input type="radio" name="q1" value="b"> b. tuple<br>
		<input type="radio" name="q1" value="c"> c. string<br><br>
		<input type="submit" value="Submit">
    


</form>


		
	
	<script>
		// Get the form element
		const form = document.querySelector('form');

		// Add a submit event listener to the form
		form.addEventListener('submit', function(event) {
			// Prevent the form from submitting and reloading the page
			event.preventDefault();

			// Get the values of the form inputs
			const name = form.elements['name'].value;
			const q1 = form.elements['q1'].value;

			// Define the correct answers
			const correctAnswers = {
				'q1': 'a',
			};

			// Calculate the score
			let score = 0;
			if (q1 === correctAnswers['q1']) {
				score += 5000;
			}

		// Show the result to the user

	// Show the result to the user
			if (score > 0) {
				alert(`Congratulations ${name}, you won ${score} tk!`);
			} else {
				alert(`Sorry ${name}, you didn't win anything.`);
			}
		});  



	</script>

</body>
</html>

