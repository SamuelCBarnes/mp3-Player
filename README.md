# mp3-Player
mp3 player using HTML5 and Javascript


<!DOCTYPE html>

<html>
<head>
    <title>Using the Audio Tag</title>
    <script>
        var player;
        
        //Init
        //
        ////////////////////////////
        window.onload = function()
        {
            document.getElementById('btnPlay').addEventListener('click', playMusic, false);
            document.getElementById('btnPause').addEventListener('click', pauseMusic, false);
            document.getElementById('btnStop').addEventListener('click', stopMusic, false);
            player = document.getElementById('player');
        }
        
        //Music Play Controls
        //
        ///////////////////////////
        function playMusic()
        {
            player.play();
        }
        
        function pauseMusic()
        {
            player.pause();
        }
        
        function stopMusic()
        {
            player.pause();
            player.currentTime = 0;
        }
    </script>
</head>

<body>
<audio id="player">
    <source src="miab.mp3.mp3" />
</audio>
<button id="btnPlay">Play</button>
<button id="btnPause">Pause</button>
<button id="btnStop">Stop</button>
</body>
</html>
