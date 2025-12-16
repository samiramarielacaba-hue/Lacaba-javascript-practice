<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JavaScript Practice</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
        }

        header, footer {
            padding: 20px;
            text-align: center;
            background-color: #e0e0e0;
        }

        section {
            padding: 20px;
        }

        button {
            margin: 5px 0;
        }
    </style>

    <script>
        function highlightHeader() {
            document.querySelector("header").style.backgroundColor = "#ffeb3b";
        }

        function highlightFooter() {
            document.querySelector("footer").style.backgroundColor = "#90caf9";
        }

        function clearHighlight() {
            document.querySelector("header").style.backgroundColor = "#e0e0e0";
            document.querySelector("footer").style.backgroundColor = "#e0e0e0";
        }

        function showDay() {
            const days = [
                "Sunday", "Monday", "Tuesday",
                "Wednesday", "Thursday", "Friday", "Saturday"
            ];

            const today = new Date();
            const dayName = days[today.getDay()];

            document.getElementById("dayText").innerHTML =
                "Today is a " + dayName + "!";
        }

        function getSum() {
            const num1 = Number(document.getElementById("num1").value);
            const num2 = Number(document.getElementById("num2").value);

            const sum = num1 + num2;

            document.getElementById("sumResult").innerHTML =
                "The sum of " + num1 + " and " + num2 + " is " + sum + ".";
        }
    </script>
</head>

<body onload="showDay()">

    <header>
        <h1>Welcome to my Webpage!</h1>
        <button onclick="highlightHeader()">Highlight header</button>
    </header>

    <section>
        <h2>Section Content</h2>

        <p id="dayText"></p>

        <h3>Add Two Numbers</h3>

        <input type="text" id="num1" placeholder="Enter first number">
        <br>
        <input type="text" id="num2" placeholder="Enter second number">
        <br>
        <button onclick="getSum()">Get sum</button>

        <p id="sumResult"></p>

        <br>

        <button onclick="clearHighlight()">Clear highlight</button>
    </section>

    <footer>
        <p>Thank ou for visiting my webpage!</p>
        <button onclick="highlightFooter()">Highlight footer</button>
    </footer>

</body>
</html>
