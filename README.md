# RandomQuoteGeneratorApp
//index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Quote Generator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Random Quote Generator</h1>
        <div id="quoteDisplay" class="quote">"Click the button to generate a quote!"</div>
        <button id="newQuoteButton">New Quote</button>
    </div>

    <script src="script.js"></script>
</body>
</html>

//style.css

body {
    font-family: Arial, sans-serif;
    background-color: #5e0234;
    margin: 0;
    padding: 20px;
}

.container {
    max-width: 600px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    text-align: center;
}

h1 {
    margin-bottom: 20px;
}

.quote {
    font-size: 1.5em;
    margin: 20px 0;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: lch(81.12% 34.58 237.34);
}

button {
    padding: 10px 20px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #f0f35b;
    color: rgb(0, 0, 0);
    font-size: 1em;
}

button:hover {
    background-color: #e7e7e7;
}

//script.js

const quotes = [
    "The best way to predict the future is to create it. - Peter Drucker",
    "Life is 10% what happens to us and 90% how we react to it. - Charles R. Swindoll",
    "The only way to do great work is to love what you do. - Steve Jobs",
    "Success is not how high you have climbed, but how you make a positive difference to the world. - Roy T. Bennett",
    "You only live once, but if you do it right, once is enough. - Mae West",
    "In the end, we will remember not the words of our enemies, but the silence of our friends. - Martin Luther King Jr.",
    "The purpose of our lives is to be happy. - Dalai Lama",
    "Get busy living or get busy dying. - Stephen King",
    "You have within you right now, everything you need to deal with whatever the world can throw at you. - Brian Tracy",
    "Believe you can and you're halfway there. - Theodore Roosevelt"
];

function generateRandomQuote() {
    const randomIndex = Math.floor(Math.random() * quotes.length);
    document.getElementById('quoteDisplay').innerText = quotes[randomIndex];
}

document.getElementById('newQuoteButton').addEventListener('click', generateRandomQuote);
document.getElementById('shareButton').addEventListener('click', shareQuote);

generateRandomQuote();
