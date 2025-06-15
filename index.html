<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Three Strikers</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #000; /* Black background */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            overflow: hidden;
        }
        .game-container {
            background-color: #1a1a1a;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 90%;
            max-width: 800px;
            box-sizing: border-box;
            position: relative;
        }
        .strikers-area {
            display: flex;
            justify-content: space-around;
            width: 100%;
            padding: 20px 0;
            position: relative;
            z-index: 10;
        }
        .striker-wrapper {
            position: relative;
            cursor: pointer;
            width: 140px; /* Increased wrapper width to accommodate larger striker */
            height: 160px; /* Increased wrapper height to accommodate larger striker and label */
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            border-radius: 50%;
            transition: transform 0.2s ease-in-out, border 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
            border: 3px solid transparent;
            padding-top: 10px;
        }
        .striker-wrapper.selected {
            transform: scale(1.1);
            border: 5px solid #00FFFF; /* Thicker, bright cyan border for clearer selection */
            box-shadow: 0 8px 30px rgba(0, 255, 255, 0.7), 0 0 15px rgba(0, 255, 255, 0.5);
            z-index: 11;
        }
        .striker {
            width: 120px; /* Increased striker size */
            height: 120px; /* Increased striker size */
            background-color: #e74c3c; /* A solid, vibrant red */
            border-radius: 50%;
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
            position: relative;
            z-index: 5;
            transition: transform 0.3s ease-in-out;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.5), /* Subtle inner shadow */
                        0 3px 8px rgba(0,0,0,0.3); /* Subtle outer shadow */
            border: 2px solid #c0392b; /* Slightly darker red border */
            margin-bottom: 5px; /* Space between striker and label */
        }
        .striker-label {
            position: relative;
            margin-top: 5px;
            font-size: 0.9rem;
            color: #ccc;
            font-weight: bold;
            background-color: rgba(0, 0, 0, 0.6);
            padding: 3px 8px;
            border-radius: 5px;
            white-space: nowrap;
            z-index: 7;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        .hidden-image {
            position: absolute;
            top: calc(50% + 25px); /* Adjusted position for larger striker */
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: #FFD700;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 45px;
            color: #fff;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.7);
            box-shadow: 0 4px 10px rgba(0,0,0,0.5);
            z-index: 1;
            opacity: 0;
            transition: opacity 0.5s ease-out, transform 0.5s ease-out;
        }
        .hidden-image.visible {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
            z-index: 6;
        }
        @keyframes bounce {
            0% { transform: translate(-50%, -50%) scale(0); }
            50% { transform: translate(-50%, -50%) scale(1.2); }
            100% { transform: translate(-50%, -50%) scale(1); }
        }

        .betting-panel {
            background-color: #2a2a2a;
            border-radius: 10px;
            padding: 15px;
            margin-top: 20px;
            width: 100%;
            max-width: 400px;
            text-align: center;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.4);
        }
        .game-messages {
            color: #fff;
            font-size: 1.2rem;
            margin-bottom: 15px;
            min-height: 30px;
        }
        .game-button {
            background-image: linear-gradient(to right, #FF416C 0%, #FF4B2B 100%);
            color: white;
            padding: 10px 25px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            box-shadow: 0 5px 15px rgba(255, 75, 43, 0.4);
            margin: 10px;
        }
        .game-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 75, 43, 0.6);
        }
        .game-button:disabled {
            background-image: linear-gradient(to right, #555 0%, #777 100%);
            cursor: not-allowed;
            box-shadow: none;
        }

        @keyframes shuffleMove {
            0% { transform: translate(0, 0); }
            25% { transform: translate(var(--dx), var(--dy)); }
            50% { transform: translate(var(--dx2), var(--dy2)); }
            75% { transform: translate(var(--dx3), var(--dy3)); }
            100% { transform: translate(0, 0); } /* Reset to original position */
        }

        .shuffling {
            animation: shuffleMove 1.5s ease-in-out forwards;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .striker-wrapper {
                width: 120px; /* Adjusted for mobile */
                height: 140px; /* Adjusted for mobile */
            }
            .striker {
                width: 100px; /* Adjusted for mobile */
                height: 100px; /* Adjusted for mobile */
            }
            .hidden-image {
                width: 70px;
                height: 70px;
                font-size: 40px;
                top: calc(50% + 15px); /* Adjusted for mobile */
            }
        }

        @media (max-width: 480px) {
            .striker-wrapper {
                width: 100px; /* Adjusted for mobile */
                height: 120px; /* Adjusted for mobile */
            }
            .striker {
                width: 80px; /* Adjusted for mobile */
                height: 80px; /* Adjusted for mobile */
            }
            .hidden-image {
                width: 60px;
                height: 60px;
                font-size: 35px;
                top: calc(50% + 10px); /* Adjusted for mobile */
            }
            .game-container {
                padding: 15px;
            }
            .game-messages {
                font-size: 1rem;
            }
            .game-button {
                padding: 8px 20px;
                font-size: 1rem;
            }
        }
    </style>
    <!-- Howler.js for robust audio playback -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/howler/2.2.3/howler.min.js"></script>
</head>
<body class="bg-black text-white">

    <div class="game-container">
        <h1 class="text-3xl font-bold mb-5 text-red-500">Three Strikers</h1>
        <div class="game-messages" id="gameMessage">Place your bet!</div>

        <div class="strikers-area" id="strikersArea">
            <!-- Strikers will be dynamically generated here -->
        </div>

        <div class="betting-panel">
            <h2 class="text-xl font-semibold mb-3 text-red-400">Your Winnings: <span id="winnings">100</span></h2>
            <div class="flex justify-center items-center space-x-4 mb-4">
                <label for="betAmount" class="text-lg">Bet Amount:</label>
                <input type="number" id="betAmount" value="10" min="5" max="50" step="5" class="p-2 rounded-md bg-gray-700 text-white w-24 text-center">
            </div>
            <button id="shuffleButton" class="game-button">Shuffle & Bet</button>
            <button id="revealButton" class="game-button" disabled>Reveal</button>
            <button id="resetButton" class="game-button" disabled>Play Again</button>
        </div>
    </div>

    <script>
        const strikerImage = "Carrom-Board-Striker-Tournament-Carrom-Board-Striker-Splay-Red.webp"; // Provided striker image
        const strikersArea = document.getElementById('strikersArea');
        const gameMessage = document.getElementById('gameMessage');
        const shuffleButton = document.getElementById('shuffleButton');
        const revealButton = document.getElementById('revealButton');
        const resetButton = document.getElementById('resetButton');
        const betAmountInput = document.getElementById('betAmount');
        const winningsDisplay = document.getElementById('winnings');

        let strikers = [];
        let hiddenStrikerIndex = -1;
        let selectedStrikerIndex = -1;
        let winnings = 100;
        let isShuffling = false;

        const shuffleSound = new Howl({
            src: ['https://assets.mixkit.co/sfx/preview/mixkit-card-shuffle-656.mp3'],
            volume: 0.5
        });
        const winSound = new Howl({
            src: ['https://assets.mixkit.co/sfx/preview/mixkit-achievement-bell-600.mp3'],
            volume: 0.5
        });
        const loseSound = new Howl({
            src: ['https://assets.mixkit.co/sfx/preview/mixkit-negative-tone-866.mp3'],
            volume: 0.5
        });

        function initializeGame() {
            strikersArea.innerHTML = '';
            strikers = [];
            hiddenStrikerIndex = Math.floor(Math.random() * 3);
            selectedStrikerIndex = -1;

            for (let i = 0; i < 3; i++) {
                const strikerWrapper = document.createElement('div');
                strikerWrapper.className = 'striker-wrapper rounded-full';
                strikerWrapper.dataset.originalIndex = i;

                const strikerDiv = document.createElement('div');
                strikerDiv.className = 'striker rounded-full';
                // No background image set here; CSS will handle the simple red background
                strikerDiv.onerror = () => {
                    console.error('Striker image failed to load, using CSS fallback color.');
                };

                const hiddenImageDiv = document.createElement('div');
                hiddenImageDiv.className = 'hidden-image';
                hiddenImageDiv.textContent = '🌟';

                const strikerLabel = document.createElement('div');
                strikerLabel.className = 'striker-label';
                strikerLabel.textContent = `Striker ${i + 1}`;

                strikerWrapper.appendChild(strikerDiv);
                strikerWrapper.appendChild(hiddenImageDiv);
                strikerWrapper.appendChild(strikerLabel);
                strikers.push({ wrapper: strikerWrapper, element: strikerDiv, hiddenImage: hiddenImageDiv, label: strikerLabel });

                strikerWrapper.addEventListener('click', (event) => {
                    const clickedOriginalIndex = parseInt(event.currentTarget.dataset.originalIndex);
                    selectStriker(clickedOriginalIndex);
                });
                strikersArea.appendChild(strikerWrapper);
            }
            updateUI();
        }

        function updateUI() {
            console.log('UpdateUI called. selectedStrikerIndex:', selectedStrikerIndex, 'Reveal button disabled:', revealButton.disabled);
            winningsDisplay.textContent = winnings;
            if (winnings <= 0) {
                gameMessage.textContent = "Game Over! You've run out of winnings.";
                shuffleButton.disabled = true;
                betAmountInput.disabled = true;
                revealButton.disabled = true;
                resetButton.disabled = false;
                return;
            }

            shuffleButton.disabled = isShuffling || selectedStrikerIndex !== -1;
            revealButton.disabled = isShuffling || selectedStrikerIndex === -1;
            resetButton.disabled = true;
            betAmountInput.disabled = isShuffling || selectedStrikerIndex !== -1;

            strikers.forEach((s) => {
                s.wrapper.classList.remove('selected');
                s.hiddenImage.classList.remove('visible', 'bounced');
                s.hiddenImage.style.opacity = 0;
                s.hiddenImage.style.transform = 'translate(-50%, -50%) scale(0)';
                s.label.textContent = `Striker ${parseInt(s.wrapper.dataset.originalIndex) + 1}`;
                s.label.style.backgroundColor = 'rgba(0, 0, 0, 0.6)';
                s.label.style.color = '#ccc';
            });

            if (selectedStrikerIndex !== -1 && strikers[selectedStrikerIndex]) {
                strikers[selectedStrikerIndex].wrapper.classList.add('selected');
            }
            gameMessage.textContent = "Place your bet and click Shuffle & Bet!";
        }

        function selectStriker(clickedOriginalIndex) {
            if (isShuffling || !shuffleButton.disabled) {
                gameMessage.textContent = "Please wait for shuffling to complete or click Shuffle & Bet first!";
                return;
            }

            const actualIndexInStrikersArray = strikers.findIndex(s => parseInt(s.wrapper.dataset.originalIndex) === clickedOriginalIndex);

            if (actualIndexInStrikersArray === -1 || selectedStrikerIndex === actualIndexInStrikersArray) {
                return;
            }

            if (selectedStrikerIndex !== -1 && strikers[selectedStrikerIndex]) {
                strikers[selectedStrikerIndex].wrapper.classList.remove('selected');
            }

            selectedStrikerIndex = actualIndexInStrikersArray;
            strikers[selectedStrikerIndex].wrapper.classList.add('selected');

            gameMessage.textContent = `You selected Striker ${clickedOriginalIndex + 1}. Now click Reveal!`;

            revealButton.disabled = false;
            shuffleButton.disabled = true;
            betAmountInput.disabled = true;
            console.log('Striker selected (data-originalIndex):', clickedOriginalIndex, 'Actual array index:', actualIndexInStrikersArray, 'Reveal button disabled (after setting):', revealButton.disabled);
        }

        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
            return array;
        }

        async function shuffleStrikers() {
            if (isShuffling) return;

            const bet = parseInt(betAmountInput.value);
            if (isNaN(bet) || bet <= 0 || bet > winnings) {
                gameMessage.textContent = "Invalid bet amount. Please enter a valid amount.";
                return;
            }

            isShuffling = true;
            shuffleButton.disabled = true;
            revealButton.disabled = true;
            betAmountInput.disabled = true;
            gameMessage.textContent = "Shuffling... Keep your eyes on the star!";
            shuffleSound.play();

            const initialRects = strikers.map(s => s.wrapper.getBoundingClientRect());
            const containerRect = strikersArea.getBoundingClientRect();

            strikers.forEach((s, i) => {
                s.wrapper.style.position = 'absolute';
                s.wrapper.style.left = `${initialRects[i].left - containerRect.left}px`;
                s.wrapper.style.top = `${initialRects[i].top - containerRect.top}px`;
            });

            const animationDuration = 1500;
            const numSteps = 8;

            for (let step = 0; step < numSteps; step++) {
                strikers.forEach((s, i) => {
                    s.wrapper.style.transition = 'transform 0.2s ease-in-out';
                    const dx = (Math.random() - 0.5) * 150;
                    const dy = (Math.random() - 0.5) * 70;
                    const rotation = (Math.random() - 0.5) * 360;
                    s.wrapper.style.transform = `translate(${dx}px, ${dy}px) rotate(${rotation}deg)`;
                });
                await new Promise(resolve => setTimeout(resolve, animationDuration / numSteps));
            }

            strikers.forEach(s => {
                s.wrapper.style.transition = '';
                s.wrapper.style.transform = '';
                s.wrapper.style.position = 'relative';
                s.wrapper.style.left = '';
                s.wrapper.style.top = '';
            });

            shuffleArray(strikers);
            hiddenStrikerIndex = Math.floor(Math.random() * strikers.length);

            strikersArea.innerHTML = '';
            strikers.forEach(s => {
                strikersArea.appendChild(s.wrapper);
            });

            isShuffling = false;
            selectedStrikerIndex = -1;
            gameMessage.textContent = "Shuffling complete! Choose a striker.";
            shuffleButton.disabled = true;
            betAmountInput.disabled = true;
            revealButton.disabled = true;
        }

        function revealStrikers() {
            if (selectedStrikerIndex === -1) {
                gameMessage.textContent = "Please select a striker first!";
                return;
            }

            const revealedImage = strikers[hiddenStrikerIndex].hiddenImage;
            revealedImage.classList.add('visible', 'bounced');

            const bet = parseInt(betAmountInput.value);
            const selectedStrikerLabel = strikers[selectedStrikerIndex].label;

            if (selectedStrikerIndex === hiddenStrikerIndex) {
                winnings += bet;
                gameMessage.textContent = `Congratulations! You won ${bet}!`;
                winSound.play();
                strikers[selectedStrikerIndex].wrapper.style.borderColor = '#66bb6a';
                selectedStrikerLabel.textContent = "You Won!";
                selectedStrikerLabel.style.backgroundColor = '#66bb6a';
                selectedStrikerLabel.style.color = '#FFFFFF';
            } else {
                winnings -= bet;
                gameMessage.textContent = `Sorry, you lost ${bet}. The star was under Striker ${strikers[hiddenStrikerIndex].wrapper.dataset.originalIndex + 1}.`;
                loseSound.play();
                strikers[selectedStrikerIndex].wrapper.style.borderColor = '#ef5350';
                selectedStrikerLabel.textContent = "You Lost!";
                selectedStrikerLabel.style.backgroundColor = '#ef5350';
                selectedStrikerLabel.style.color = '#FFFFFF';
            }

            winningsDisplay.textContent = winnings;
            revealButton.disabled = true;
            resetButton.disabled = false;
            shuffleButton.disabled = true;
            if (winnings <= 0) {
                gameMessage.textContent = "Game Over! You've run out of winnings.";
                shuffleButton.disabled = true;
                betAmountInput.disabled = true;
                resetButton.disabled = false;
            }
        }

        function resetGame() {
            initializeGame();
            updateUI();
            gameMessage.textContent = "New round! Place your bet and click Shuffle & Bet.";
            betAmountInput.value = 10;
        }

        shuffleButton.addEventListener('click', shuffleStrikers);
        revealButton.addEventListener('click', revealStrikers);
        resetButton.addEventListener('click', resetGame);

        initializeGame();
        updateUI();
    </script>
</body>
</html>
