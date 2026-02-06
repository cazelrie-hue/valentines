# valentines
asking someone to be my valentine
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Day Fun</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #ffafbd, #ffc3a0);
            min-height: 100vh;
            overflow: hidden;
            position: relative;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
            position: relative;
            z-index: 10;
        }
        
        header {
            padding: 30px 0;
            color: #b33951;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            font-family: 'Brush Script MT', cursive;
            color: #d63031;
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: #a83232;
            margin-bottom: 30px;
        }
        
        .message-box {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 30px;
            margin: 30px auto;
            max-width: 800px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border: 5px solid #ff6b81;
            position: relative;
            z-index: 10;
        }
        
        .message-box p {
            font-size: 1.4rem;
            line-height: 1.6;
            color: #555;
            margin-bottom: 20px;
        }
        
        .buttons-container {
            display: flex;
            justify-content: center;
            gap: 100px;
            margin: 50px 0;
            position: relative;
            z-index: 10;
        }
        
        .valentine-button {
            padding: 20px 40px;
            font-size: 1.8rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
            position: absolute;
        }
        
        #yesButton {
            background-color: #ff6b81;
            color: white;
            left: 35%;
        }
        
        #noButton {
            background-color: #a29bfe;
            color: white;
            right: 35%;
        }
        
        .valentine-button:hover {
            transform: scale(1.05);
        }
        
        .instructions {
            margin-top: 30px;
            color: #a83232;
            font-size: 1.2rem;
            font-style: italic;
            background-color: rgba(255, 255, 255, 0.7);
            padding: 15px;
            border-radius: 10px;
            display: inline-block;
        }
        
        /* Balloons */
        .balloon {
            position: absolute;
            width: 60px;
            height: 70px;
            border-radius: 50%;
            z-index: 1;
            animation: float 8s ease-in-out infinite;
        }
        
        .balloon:before {
            content: "";
            position: absolute;
            width: 2px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.7);
            top: 70px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .balloon.red {
            background: radial-gradient(circle at 30% 30%, #ff7675, #d63031);
        }
        
        .balloon.pink {
            background: radial-gradient(circle at 30% 30%, #fd79a8, #a83232);
        }
        
        .balloon.purple {
            background: radial-gradient(circle at 30% 30%, #a29bfe, #6c5ce7);
        }
        
        .balloon.heart {
            background: none;
            font-size: 40px;
            color: #ff6b81;
            animation: float-heart 10s ease-in-out infinite;
        }
        
        /* Hearts */
        .heart {
            position: absolute;
            color: #ff6b81;
            font-size: 24px;
            opacity: 0.7;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }
        
        /* Floating animation */
        @keyframes float {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(5deg);
            }
        }
        
        @keyframes float-heart {
            0%, 100% {
                transform: translateY(0) rotate(0deg) scale(1);
            }
            33% {
                transform: translateY(-15px) rotate(5deg) scale(1.1);
            }
            66% {
                transform: translateY(-10px) rotate(-5deg) scale(0.9);
            }
        }
        
        /* Footer */
        footer {
            position: fixed;
            bottom: 20px;
            width: 100%;
            text-align: center;
            color: #a83232;
            font-size: 1rem;
            z-index: 10;
        }
        
        .counter {
            font-size: 1.5rem;
            color: #d63031;
            font-weight: bold;
            margin-top: 20px;
            background-color: rgba(255, 255, 255, 0.7);
            padding: 10px 20px;
            border-radius: 50px;
            display: inline-block;
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .buttons-container {
                flex-direction: column;
                align-items: center;
                gap: 50px;
            }
            
            .valentine-button {
                position: relative;
                left: auto !important;
                right: auto !important;
                margin: 10px 0;
            }
            
            .message-box p {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Balloons -->
    <div class="balloon red" style="top: 10%; left: 5%; animation-delay: 0s;"></div>
    <div class="balloon pink" style="top: 15%; left: 15%; animation-delay: 1s;"></div>
    <div class="balloon purple" style="top: 5%; right: 10%; animation-delay: 2s;"></div>
    <div class="balloon red" style="top: 20%; right: 20%; animation-delay: 3s;"></div>
    <div class="balloon heart" style="top: 25%; left: 20%; animation-delay: 4s;">❤️</div>
    <div class="balloon pink" style="bottom: 30%; left: 10%; animation-delay: 5s;"></div>
    <div class="balloon purple" style="bottom: 20%; right: 15%; animation-delay: 6s;"></div>
    <div class="balloon heart" style="bottom: 25%; right: 5%; animation-delay: 7s;">❤️</div>
    
    <!-- Floating Hearts -->
    <div class="heart" style="top: 40%; left: 8%; animation-delay: 0.5s;">❤️</div>
    <div class="heart" style="top: 60%; left: 12%; animation-delay: 1.5s;">❤️</div>
    <div class="heart" style="top: 30%; right: 8%; animation-delay: 2.5s;">❤️</div>
    <div class="heart" style="top: 50%; right: 12%; animation-delay: 3.5s;">❤️</div>
    <div class="heart" style="bottom: 40%; left: 20%; animation-delay: 4.5s;">❤️</div>
    <div class="heart" style="bottom: 60%; right: 25%; animation-delay: 5.5s;">❤️</div>
    
    <div class="container">
        <header>
            <h1>Valentine's Day Fun</h1>
            <div class="subtitle">A playful Valentine's experience with tricky buttons!</div>
        </header>
        
        <div class="message-box">
            <p>💖 Welcome to this special Valentine's Day website! 💖</p>
            <p>I have two buttons for you, but they're a bit shy... They'll move around when you try to click them!</p>
            <p>See if you can catch the "YES" button to accept this virtual Valentine, or try your luck with the "NO" button (but we all know you want to say yes!).</p>
            <p>Good luck and Happy Valentine's Day! ❤️</p>
        </div>
        
        <div class="buttons-container">
            <!-- Buttons will be positioned by JavaScript -->
        </div>
        
        <div class="counter">
            Attempts: <span id="attemptCount">0</span>
        </div>
        
        <div class="instructions">
            <i class="fas fa-lightbulb"></i> Hint: Try to anticipate where the button will move!
        </div>
    </div>
    
    <footer>
        Made with <span style="color: #ff6b81;">❤️</span> for Valentine's Day | All buttons are uncooperative by design!
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const buttonsContainer = document.querySelector('.buttons-container');
            const attemptCountElement = document.getElementById('attemptCount');
            let attemptCount = 0;
            
            // Create the buttons
            const yesButton = document.createElement('button');
            yesButton.id = 'yesButton';
            yesButton.className = 'valentine-button';
            yesButton.textContent = 'YES 💖';
            
            const noButton = document.createElement('button');
            noButton.id = 'noButton';
            noButton.className = 'valentine-button';
            noButton.textContent = 'NO 😢';
            
            buttonsContainer.appendChild(yesButton);
            buttonsContainer.appendChild(noButton);
            
            // Set initial positions
            positionButtons();
            
            // Function to position buttons
            function positionButtons() {
                const containerRect = buttonsContainer.getBoundingClientRect();
                
                // Position YES button
                const yesX = containerRect.width * 0.35 - yesButton.offsetWidth / 2;
                const yesY = containerRect.height / 2 - yesButton.offsetHeight / 2;
                yesButton.style.left = `${yesX}px`;
                yesButton.style.top = `${yesY}px`;
                
                // Position NO button
                const noX = containerRect.width * 0.65 - noButton.offsetWidth / 2;
                const noY = containerRect.height / 2 - noButton.offsetHeight / 2;
                noButton.style.left = `${noX}px`;
                noButton.style.top = `${noY}px`;
            }
            
            // Function to move button away from cursor
            function moveButton(button, event) {
                attemptCount++;
                attemptCountElement.textContent = attemptCount;
                
                const containerRect = buttonsContainer.getBoundingClientRect();
                const buttonRect = button.getBoundingClientRect();
                
                // Calculate cursor position relative to button
                const cursorX = event.clientX - containerRect.left;
                const cursorY = event.clientY - containerRect.top;
                
                // Calculate button center
                const buttonCenterX = buttonRect.left - containerRect.left + buttonRect.width / 2;
                const buttonCenterY = buttonRect.top - containerRect.top + buttonRect.height / 2;
                
                // Calculate distance from cursor to button center
                const deltaX = cursorX - buttonCenterX;
                const deltaY = cursorY - buttonCenterY;
                
                // Move button in opposite direction
                let newX = parseFloat(button.style.left) - deltaX * 0.8;
                let newY = parseFloat(button.style.top) - deltaY * 0.8;
                
                // Keep button within container bounds
                newX = Math.max(10, Math.min(containerRect.width - buttonRect.width - 10, newX));
                newY = Math.max(10, Math.min(containerRect.height - buttonRect.height - 10, newY));
                
                // Apply new position with smooth transition
                button.style.transition = 'all 0.5s ease';
                button.style.left = `${newX}px`;
                button.style.top = `${newY}px`;
                
                // Remove transition after movement to prepare for next move
                setTimeout(() => {
                    button.style.transition = '';
                }, 500);
                
                // If user manages to click the YES button
                if (button.id === 'yesButton' && attemptCount > 5) {
                    // Small chance to allow clicking after many attempts
                    if (Math.random() > 0.7) {
                        setTimeout(() => {
                            alert("🎉 You caught me! Happy Valentine's Day! 💝\nThanks for playing! ❤️");
                            // Reset counter
                            attemptCount = 0;
                            attemptCountElement.textContent = attemptCount;
                        }, 100);
                        return true;
                    }
                }
                
                return false;
            }
            
            // Add event listeners to buttons
            yesButton.addEventListener('mouseover', function(event) {
                moveButton(yesButton, event);
            });
            
            yesButton.addEventListener('click', function(event) {
                if (!moveButton(yesButton, event)) {
                    event.preventDefault();
                    event.stopPropagation();
                }
            });
            
            noButton.addEventListener('mouseover', function(event) {
                moveButton(noButton, event);
            });
            
            noButton.addEventListener('click', function(event) {
                if (!moveButton(noButton, event)) {
                    event.preventDefault();
                    event.stopPropagation();
                    // Special message for NO button
                    if (attemptCount % 5 === 0) {
                        alert("The NO button is extra tricky! Try the YES button instead! 💖");
                    }
                }
            });
            
            // Reposition buttons on window resize
            window.addEventListener('resize', positionButtons);
            
            // Create more floating hearts dynamically
            function createFloatingHearts() {
                const body = document.body;
                for (let i = 0; i < 10; i++) {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.innerHTML = '❤️';
                    heart.style.left = `${Math.random() * 100}%`;
                    heart.style.top = `${Math.random() * 100}%`;
                    heart.style.fontSize = `${Math.random() * 20 + 15}px`;
                    heart.style.opacity = `${Math.random() * 0.5 + 0.3}`;
                    heart.style.animationDuration = `${Math.random() * 4 + 4}s`;
                    heart.style.animationDelay = `${Math.random() * 5}s`;
                    body.appendChild(heart);
                }
            }
            
            createFloatingHearts();
        });
    </script>
</body>
</html>
