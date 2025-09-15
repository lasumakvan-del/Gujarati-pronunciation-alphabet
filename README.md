# Gujarati-pronunciation-alphabet
અંગ્રેજી આલ્ફાબેટ ના ગુજરાતી ઉચ્ચારણ
<!DOCTYPE html>
<html lang="gu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ઇંગ્લીશ આલ્ફાબેટ ના ગુજરાતી ઉચ્ચારણ</title>
    <link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Baloo 2', cursive;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: #2d3748;
        }
        
        .container {
            max-width: 1200px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 24px;
            padding: 35px;
            box-shadow: 0 20px 35px rgba(0, 0, 0, 0.1);
            border: 1px solid #e2e8f0;
        }
        
        .header {
            text-align: center;
            margin-bottom: 35px;
            position: relative;
        }
        
        .header::after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #4299e1, #48bb78);
            margin: 15px auto;
            border-radius: 2px;
        }
        
        h1 {
            color: #2b6cb0;
            margin-bottom: 12px;
            font-size: 2.8rem;
            font-weight: 700;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        }
        
        .subtitle {
            color: #4a5568;
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto;
            line-height: 1.5;
        }
        
        .alphabet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .letter-card {
            height: 160px;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            position: relative;
            overflow: hidden;
            border: 2px solid transparent;
        }
        
        .letter-card:hover {
            transform: translateY(-8px) scale(1.03);
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.15);
        }
        
        .letter-card:active {
            transform: translateY(2px);
        }
        
        .letter {
            font-size: 42px;
            font-weight: 800;
            margin-bottom: 10px;
            z-index: 2;
            color: #2d3748;
        }
        
        .gujarati {
            font-size: 18px;
            margin-bottom: 8px;
            z-index: 2;
            text-align: center;
            color: #4a5568;
            font-weight: 500;
        }
        
        .example {
            font-size: 16px;
            font-style: italic;
            z-index: 2;
            text-align: center;
            color: #48bb78;
            font-weight: 500;
        }
        
        .pattern {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.05;
            background-size: 40px 40px;
            background-image: 
                linear-gradient(45deg, #4299e1 25%, transparent 25%, transparent 75%, #4299e1 75%, #4299e1),
                linear-gradient(45deg, #4299e1 25%, transparent 25%, transparent 75%, #4299e1 75%, #4299e1);
        }
        
        .instructions {
            text-align: center;
            background: linear-gradient(135deg, #ebf4ff 0%, #c3dafe 100%);
            color: #2b6cb0;
            padding: 20px;
            border-radius: 18px;
            margin-top: 30px;
            font-size: 1.2rem;
            border: 1px solid #90cdf4;
            font-weight: 500;
            box-shadow: 0 5px 15px rgba(66, 153, 225, 0.15);
        }
        
        .footer {
            text-align: center;
            margin-top: 30px;
            color: #4a5568;
            font-size: 1.1rem;
            font-weight: 500;
        }
        
        @media (max-width: 768px) {
            .alphabet-grid {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
                gap: 16px;
            }
            
            .letter-card {
                height: 145px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .container {
                padding: 25px 20px;
            }
            
            .subtitle {
                font-size: 1.1rem;
            }
        }
        
        @media (max-width: 480px) {
            .alphabet-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
                gap: 14px;
            }
            
            .letter-card {
                height: 130px;
            }
            
            h1 {
                font-size: 1.9rem;
            }
            
            .subtitle {
                font-size: 1rem;
            }
        }
        
        /* Animation for cards */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .letter-card {
            animation: fadeIn 0.5s ease-out;
            animation-fill-mode: both;
        }
        
        /* Sequential animation for cards */
        .letter-card:nth-child(1) { animation-delay: 0.05s; }
        .letter-card:nth-child(2) { animation-delay: 0.1s; }
        .letter-card:nth-child(3) { animation-delay: 0.15s; }
        .letter-card:nth-child(4) { animation-delay: 0.2s; }
        .letter-card:nth-child(5) { animation-delay: 0.25s; }
        .letter-card:nth-child(6) { animation-delay: 0.3s; }
        .letter-card:nth-child(7) { animation-delay: 0.35s; }
        .letter-card:nth-child(8) { animation-delay: 0.4s; }
        .letter-card:nth-child(9) { animation-delay: 0.45s; }
        .letter-card:nth-child(10) { animation-delay: 0.5s; }
        .letter-card:nth-child(11) { animation-delay: 0.55s; }
        .letter-card:nth-child(12) { animation-delay: 0.6s; }
        .letter-card:nth-child(13) { animation-delay: 0.65s; }
        .letter-card:nth-child(14) { animation-delay: 0.7s; }
        .letter-card:nth-child(15) { animation-delay: 0.75s; }
        .letter-card:nth-child(16) { animation-delay: 0.8s; }
        .letter-card:nth-child(17) { animation-delay: 0.85s; }
        .letter-card:nth-child(18) { animation-delay: 0.9s; }
        .letter-card:nth-child(19) { animation-delay: 0.95s; }
        .letter-card:nth-child(20) { animation-delay: 1s; }
        .letter-card:nth-child(21) { animation-delay: 1.05s; }
        .letter-card:nth-child(22) { animation-delay: 1.1s; }
        .letter-card:nth-child(23) { animation-delay: 1.15s; }
        .letter-card:nth-child(24) { animation-delay: 1.2s; }
        .letter-card:nth-child(25) { animation-delay: 1.25s; }
        .letter-card:nth-child(26) { animation-delay: 1.3s; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>રંગીન અક્ષરમાળા</h1>
            <div class="subtitle">આલ્ફાબેટ પર ટચ કરી તેનો ગુજરાતી ઉચ્ચારણ જાણો</div>
        </div>
        
        <div class="alphabet-grid" id="alphabetGrid">
            <!-- Alphabet cards will be generated by JavaScript -->
        </div>
        
        <div class="instructions">
            Makwana Sanjaybhai, Shri Pipardi-2 Primary School
        </div>
    </div>
    
    <div class="footer">
        આનંદ સાથે અક્ષરો શીખો! | Enjoy learning letters!
    </div>

    <script>
        // Alphabet data with Gujarati pronunciations and examples
        const alphabetData = [
            { letter: "A", gujarati: "એ, અ, આ, ઓ", example: "Apple", color: "#ffcdd2" },
            { letter: "B", gujarati: "બ", example: "Ball", color: "#f8bbd0" },
            { letter: "C", gujarati: "ક", example: "Cat", color: "#e1bee7" },
            { letter: "D", gujarati: "ડ", example: "Dog", color: "#d1c4e9" },
            { letter: "E", gujarati: "એ", example: "Elephant", color: "#c5cae9" },
            { letter: "F", gujarati: "ફ", example: "Fish", color: "#bbdefb" },
            { letter: "G", gujarati: "ગ", example: "Goat", color: "#b3e5fc" },
            { letter: "H", gujarati: "હ", example: "Hat", color: "#b2ebf2" },
            { letter: "I", gujarati: "ઇ, આઈ", example: "Ice", color: "#b2dfdb" },
            { letter: "J", gujarati: "જ", example: "Jug", color: "#c8e6c9" },
            { letter: "K", gujarati: "ક", example: "Kite", color: "#dcedc8" },
            { letter: "L", gujarati: "લ", example: "Lion", color: "#f0f4c3" },
            { letter: "M", gujarati: "મ", example: "Monkey", color: "#fff9c4" },
            { letter: "N", gujarati: "ન", example: "Nest", color: "#ffecb3" },
            { letter: "O", gujarati: "ઓ", example: "Orange", color: "#ffe0b2" },
            { letter: "P", gujarati: "પ", example: "Parrot", color: "#ffccbc" },
            { letter: "Q", gujarati: "ક્યુ", example: "Queen", color: "#ffcdd2" },
            { letter: "R", gujarati: "ર", example: "Rat", color: "#f8bbd0" },
            { letter: "S", gujarati: "સ", example: "Sun", color: "#e1bee7" },
            { letter: "T", gujarati: "ટ", example: "Tree", color: "#d1c4e9" },
            { letter: "U", gujarati: "યુ, અ", example: "Umbrella", color: "#c5cae9" },
            { letter: "V", gujarati: "વ", example: "Van", color: "#bbdefb" },
            { letter: "W", gujarati: "વ", example: "Watch", color: "#b3e5fc" },
            { letter: "X", gujarati: "ક્ષ", example: "Box", color: "#b2ebf2" },
            { letter: "Y", gujarati: "ય", example: "Yak", color: "#b2dfdb" },
            { letter: "Z", gujarati: "ઝ", example: "Zoo", color: "#c8e6c9" }
        ];

        // Generate alphabet cards
        const grid = document.getElementById('alphabetGrid');
        
        alphabetData.forEach((item, index) => {
            const card = document.createElement('div');
            card.className = 'letter-card';
            card.style.background = `linear-gradient(135deg, ${item.color} 0%, ${lightenColor(item.color, 30)} 100%)`;
            card.innerHTML = `
                <div class="pattern"></div>
                <div class="letter">${item.letter}</div>
                <div class="gujarati">${item.gujarati}</div>
                <div class="example">${item.example}</div>
            `;
            
            card.addEventListener('click', () => {
                playAudio(item.letter, item.gujarati, item.example);
                // Add click animation
                card.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    card.style.transform = '';
                }, 100);
            });
            
            grid.appendChild(card);
        });

        // Function to lighten a color
        function lightenColor(color, percent) {
            const num = parseInt(color.replace('#', ''), 16);
            const amt = Math.round(2.55 * percent);
            const R = (num >> 16) + amt;
            const G = (num >> 8 & 0x00FF) + amt;
            const B = (num & 0x0000FF) + amt;
            return '#' + (
                0x1000000 +
                (R < 255 ? (R < 0 ? 0 : R) : 255) * 0x10000 +
                (G < 255 ? (G < 0 ? 0 : G) : 255) * 0x100 +
                (B < 255 ? (B < 0 ? 0 : B) : 255)
            ).toString(16).slice(1);
        }

        // Function to play audio using SpeechSynthesis API
        function playAudio(letter, gujarati, example) {
            // Stop any ongoing speech
            window.speechSynthesis.cancel();
            
            // Create utterances
            const letterSpeech = new SpeechSynthesisUtterance(letter);
            letterSpeech.lang = 'en-US';
            letterSpeech.rate = 0.8;
            
            const gujSpeech = new SpeechSynthesisUtterance(gujarati);
            gujSpeech.lang = 'gu-IN';
            gujSpeech.rate = 0.8;
            
            const exSpeech = new SpeechSynthesisUtterance(example);
            exSpeech.lang = 'en-US';
            exSpeech.rate = 0.8;
            
            // Play in sequence
            letterSpeech.onend = function() {
                setTimeout(() => {
                    window.speechSynthesis.speak(gujSpeech);
                }, 300);
            };
            
            gujSpeech.onend = function() {
                setTimeout(() => {
                    window.speechSynthesis.speak(exSpeech);
                }, 300);
            };
            
            // Start with the letter
            window.speechSynthesis.speak(letterSpeech);
        }
    </script>
</body>
</html>
