---
title: Testing
published_at: 2024-05-09
snippet: Wahoo
disable_html_sanitization: true
---

<!doctype html>
<head>
    <title> b l a n k </title>
<style>
    body, html {
        margin: 0;
        padding: 0;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }

    #colorSquare {
        width: 100px;
        height: 100px;
        background-color: red;
        position: absolute;
    }
</style>
</head>

<body>
    test
<canvas id="recursive_squares"></canvas>


<div id="colorSquare"></div>

<script type="module">
function changeColorAndMove() {
    var square = document.getElementById("colorSquare");
    var randomColor = '#' + Math.floor(Math.random()*16777215).toString(16); // Generates a random hex color
    square.style.backgroundColor = randomColor;

    // Get viewport dimensions
    var viewportWidth = document.documentElement.clientWidth;
    var viewportHeight = document.documentElement.clientHeight;

    // Generate random coordinates within the viewport
    var randomX = Math.floor(Math.random() * (viewportWidth - 100)); // Subtracting square width
    var randomY = Math.floor(Math.random() * (viewportHeight - 100)); // Subtracting square height

    // Set square position
    square.style.left = randomX + 'px';
    square.style.top = randomY + 'px';

    // Generate random velocity for x and y directions
    var vx = Math.random() * 10 - 5; // Random horizontal velocity between -5 and 5
    var vy = Math.random() * 10 - 5; // Random vertical velocity between -5 and 5

    // Update square position continuously
    function moveSquare() {
        // Get current square position
        var currentX = parseFloat(square.style.left);
        var currentY = parseFloat(square.style.top);

        // Calculate new position
        var newX = currentX + vx;
        var newY = currentY + vy;

        // Check if the square hits the boundaries
        if (newX < 0 || newX + 100 > viewportWidth) {
            vx = -vx; // Reverse horizontal velocity
        }
        if (newY < 0 || newY + 100 > viewportHeight) {
            vy = -vy; // Reverse vertical velocity
        }

        // Update square position
        square.style.left = newX + 'px';
        square.style.top = newY + 'px';
    }

    // Move the square every 50 milliseconds
    var moveInterval = setInterval(moveSquare, 50);

    // Stop moving after 5 seconds
    setTimeout(function() {
        clearInterval(moveInterval);
    }, 5000);
}

// Change color, move, and bounce every 5 seconds
setInterval(changeColorAndMove, 5000);
</script>
    
</body>


<!-- <script type="module">
    const cnv = document.getElementById (`recursive_squares`)
    cnv.width = cnv.parentNode.scrollWidth
    cnv.height = cnv.width
    
    const ctx = cnv.getContext (`2d`)

    function rand_col () {
        return `hsl(${ Math.random () * 360 }, 100%, 66%)`
    }

    function draw_square (size) {
        const x = (cnv.width - size) / 2
        const y = (cnv.height - size) / 2

        ctx.fillStyle = rand_col ()
        ctx.fillRect (x, y, size, size)
    }

    function draw_squares (start_size) {
        draw_square (start_size)

        if (start_size > 0) {
            draw_squares (start_size - 20)
        }
    }

    draw_squares (cnv.height)

</script> -->
