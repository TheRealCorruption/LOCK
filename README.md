
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Screen Locked</title>
    <style>
        body {
            background-color: black;
            color: #00FF00;
            font-family: monospace;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }

        .skull-emoji {
            font-size: 100px;
        }

        .locked-text {
            font-size: 32px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="skull-emoji">
            ☠️
        </div>
        <div class="locked-text">
            YOUR SCREEN IS NOW LOCKED.
        </div>
    </div>

    <script>
        // Function to request fullscreen mode
        function goFullScreen() {
            let elem = document.documentElement;
            if (elem.requestFullscreen) {
                elem.requestFullscreen();
            } else if (elem.mozRequestFullScreen) { // Firefox
                elem.mozRequestFullScreen();
            } else if (elem.webkitRequestFullscreen) { // Chrome, Safari and Opera
                elem.webkitRequestFullscreen();
            } else if (elem.msRequestFullscreen) { // IE/Edge
                elem.msRequestFullscreen();
            }
        }

        // Trigger fullscreen on page load
        window.onload = function() {
            goFullScreen();
        };
    </script>
</body>
</html>
