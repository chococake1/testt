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
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');

    // Set canvas width and height
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    // Square properties
    let squareSize = 30;
    let squareX = canvas.width / 2 - squareSize / 2;
    let squareY = canvas.height / 2 - squareSize / 2;
    let dx = 2;
    let dy = 2;

    // Function to generate a random color
    function randomColor() {
        return '#' + Math.floor(Math.random() * 16777215).toString(16);
    }

    // Function to draw a square
    function drawSquare(x, y, size, color) {
        ctx.fillStyle = color;
        ctx.fillRect(x, y, size, size);
    }

    function animate() {
        // Clear canvas
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Generate a random color for the square
        const color = randomColor();

        // Draw the square
        drawSquare(squareX, squareY, squareSize, color);

        // Move the square
        squareX += dx;
        squareY += dy;

        // Reverse direction if hitting the canvas edges
        if (squareX + squareSize > canvas.width || squareX < 0) {
            dx = -dx;
        }
        if (squareY + squareSize > canvas.height || squareY < 0) {
            dy = -dy;
        }

        requestAnimationFrame(animate);
    }

    animate();
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
