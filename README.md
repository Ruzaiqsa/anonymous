<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>for rania</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Caveat:wght@400;700&family=Montserrat:wght@300;400&display=swap');
        
        body {
            margin: 0;
            padding: 0;
            background-color: #D2B48C; /* Lighter brown (tan) background */
            background-image: url('data:image/svg+xml,%3Csvg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"%3E%3Cg fill="%23A0522D" fill-opacity="0.3" fill-rule="evenodd"%3E%3Cpath d="M0 0h60v60H0z"/%3E%3Ctext x="30" y="40" font-size="30" text-anchor="middle" fill="%23A0522D" font-family="Arial"%3E%F0%9F%90%%3C/text%3E%3C/g%3E%3C/svg%3E'); /* Slightly larger bear emojis */
            background-size: 60px 60px;
            background-attachment: fixed;
            font-family: 'Montserrat', sans-serif;
            color: #5a3d4e;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }
        
        /* Side bear decorations with animation */
        .side-bears-left,
        .side-bears-right {
            position: fixed;
            top: 0;
            height: 100%;
            width: 80px;
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            font-size: 2.5rem;
            color: #8B4513;
            opacity: 0.6;
            pointer-events: none;
            animation: bounce 3s ease-in-out infinite;
        }
        
        .side-bears-left {
            left: 15px;
        }
        
        .side-bears-right {
            right: 15px;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        .container {
            max-width: 600px;
            padding: 20px;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(8px);
            z-index: 1;
        }
        
        h1 {
            font-family: 'Caveat', cursive;
            font-size: 2.5rem;
            color: #9d6b84;
            margin-bottom: 30px;
            text-transform: lowercase;
        }
        
        .heart {
            font-size: 5rem;
            color: #e88ba7;
            cursor: pointer;
            margin: 40px 0;
            transition: all 0.3s ease;
            position: relative;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .heart:hover {
            transform: scale(1.2);
            color: #d45d7d;
        }
        
        .message {
            font-family: 'Caveat', cursive;
            font-size: 1.5rem;
            line-height: 1.6;
            opacity: 0;
            max-height: 0;
            overflow: hidden;
            transition: opacity 1s ease, max-height 1s ease;
            padding: 0 20px;
            text-align: left;
            background-color: rgba(255, 255, 255, 0.7);
            border-radius: 10px;
            margin: 20px 0;
        }
        
        .message.show {
            opacity: 1;
            max-height: 1000px;
            padding: 20px;
        }
        
        .footer {
            margin-top: 40px;
            font-size: 0.9rem;
            color: #9d6b84;
            font-style: italic;
        }
        
        .music-control {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: rgba(232, 139, 167, 0.3);
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            font-size: 1.5rem;
            border: 2px solid #e88ba7;
        }
        
        .music-control:hover {
            background-color: rgba(232, 139, 167, 0.5);
            transform: scale(1.1);
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 2rem;
            }
            
            .heart {
                font-size: 4rem;
            }
            
            .message {
                font-size: 1.3rem;
            }
            
            .music-control {
                width: 50px;
                height: 50px;
                font-size: 1.2rem;
            }
            
            .side-bears-left,
            .side-bears-right {
                width: 60px;
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="side-bears-left">
        <div>🧸</div>
        <div>🐻‍❄️</div>
        <div>🧸</div>
    </div>
    <div class="side-bears-right">
        <div>🐻‍❄️</div>
        <div>🧸</div>
        <div>🐻‍❄️</div>
    </div>
    <div class="container">
        <h1>for rania</h1>
        
        <div class="heart" id="heart">❤️</div>
        
        <div class="message" id="message">
            <p>hey rania,</p>
            
            <p>just wanted to say i'm sorry. for everything.</p>
            
            <p>i miss you more than i should probably admit. it hits me at random times - when i see something you'd laugh at, or hear a song we both liked.</p>
            
            <p>i know i messed up. didn't mean to make things weird between us. just wanted you to know that i care, even if i didn't always show it right.</p>
            
            <p>hope you're doing okay. really mean that.</p>
            
            <p>- anonymous</p>
        </div>
        
        <div class="footer">
            sent with love
        </div>
    </div>
    
    <div class="music-control" id="musicControl">
        🎵
    </div>
    
    <audio id="bgMusic" loop muted>
        <source src="https://d340.d2mefast.net/tb/2/44/tubidy_mp3_75963.mp3?play" type="audio/mpeg" />
        Your browser does not support the audio element.
    </audio>
    
    <script>
        const heart = document.getElementById('heart');
        const message = document.getElementById('message');
        const musicControl = document.getElementById('musicControl');
        const bgMusic = document.getElementById('bgMusic');

        let musicPlaying = false;

        heart.addEventListener('click', () => {
            message.classList.toggle('show');
            
            // Pulse animation reset
            heart.style.animation = 'none';
            void heart.offsetWidth; // Trigger reflow
            heart.style.animation = 'pulse 0.7s ease';
            
            // Play and unmute music on first heart click
            if (bgMusic.paused) {
                bgMusic.muted = false;
                bgMusic.play();
                musicPlaying = true;
                musicControl.innerHTML = '❚❚'; // pause icon
                musicControl.style.backgroundColor = 'rgba(232, 139, 167, 0.5)';
            }
        });

        musicControl.addEventListener('click', () => {
            if (musicPlaying) {
                bgMusic.pause();
                musicControl.innerHTML = '🎵';
                musicControl.style.backgroundColor = 'rgba(232, 139, 167, 0.3)';
            } else {
                bgMusic.play();
                musicControl.innerHTML = '❚❚';
                musicControl.style.backgroundColor = 'rgba(232, 139, 167, 0.5)';
            }
            musicPlaying = !musicPlaying;
        });
    </script>
</body>
</html>
