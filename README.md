<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Marry Me, Mahi?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffe4e1;
            padding: 50px;
        }
        h1 {
            color: #d63384;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        .yes {
            background-color: #28a745;
            color: white;
        }
        .no {
            background-color: #dc3545;
            color: white;
            position: absolute;
        }
        #message {
            display: none;
            font-size: 24px;
            color: #d63384;
            margin-top: 20px;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <h1>Mahi, Will You Marry Me? 💍</h1>
    <div class="buttons">
        <button class="yes" onclick="showLove()">YES 💖</button>
        <button class="no" onmouseover="moveNo()">NO 😢</button>
    </div>
    <p id="message">
        "From the moment our eyes met, my heart knew it found home in you. Every smile, every laugh, every moment with you is a piece of forever I never want to lose. Mahi, you are my sunshine on the darkest days, my heartbeat in the silence. No matter the distance, no matter the time, my love for you only grows stronger. I want to wake up to your laughter, hold your hand through every storm, and dance through life with you. Will you be mine, now and forever?" ❤️
    </p>
    
    <audio id="loveSong" src="https://www.mfiles.co.uk/mp3-downloads/Ed-Sheeran-Perfect.mp3"></audio>
    
    <script>
        function showLove() {
            document.getElementById("message").style.display = "block";
            let song = document.getElementById("loveSong");
            song.play();
            confettiEffect();
        }
        
        function moveNo() {
            let button = document.querySelector('.no');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
        
        function confettiEffect() {
            let confetti = document.createElement("div");
            confetti.innerHTML = "🎉";
            confetti.style.position = "fixed";
            confetti.style.left = "50%";
            confetti.style.top = "50%";
            confetti.style.fontSize = "50px";
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 3000);
        }
    </script>
</body>
</html>
