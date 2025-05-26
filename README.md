
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Joyeux Anniversaire !</title>
    <style>
        body {
            background: url('https://source.unsplash.com/random/1920x1080/?celebration,gold,party') no-repeat center center fixed;
            background-size: cover;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            margin: 0;
            padding: 20px;
            height: auto;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff;
            overflow: hidden;
        }

        .card {
            background: rgba(0, 0, 0, 0.75);
            border-radius: 25px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
            max-width: 800px;
            width: 90%;
            max-height: 90vh;
            backdrop-filter: blur(10px);
            border: 3px solid #FFD700;
            position: relative;
            overflow: hidden;
            overflow-y: auto;
        }

        h1 {
            font-size: 3.5rem;
            margin: 0 0 25px 0;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.8);
            position: relative;
            z-index: 2;
            background: linear-gradient(90deg, #FF69B4, #FFB6C1, #FFC0CB);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .message {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 30px;
            position: relative;
            z-index: 2;
        }

        .music-container {
            background: rgba(20, 20, 20, 0.7);
            border-radius: 15px;
            padding: 20px;
            margin: 15px 0;
            border: 1px solid #FFD700;
            position: relative;
            z-index: 2;
        }

        .music-player {
            width: 100%;
            margin-top: 15px;
        }

        audio {
            width: 100%;
            border-radius: 10px;
            outline: none;
        }

        button {
            background: linear-gradient(45deg, #FF8C00, #FF1493);
            color: white;
            border: none;
            padding: 10px 25px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            margin: 15px;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 2;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.5);
        }

        .hidden {
            display: none;
            animation: zoomIn 0.5s ease-out;
        }

        @keyframes zoomIn {
            0% {
                transform: scale(0.8);
                opacity: 0;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }

        .emoji {
            font-size: 2rem;
            animation: float 4s ease-in-out infinite;
            display: inline-block;
            filter: drop-shadow(0 0 5px rgba(255, 215, 0, 0.7));
            color: #FFD700; /* Couleur fixe pour les émojis */
        }

        @keyframes float {
            0% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-15px) rotate(5deg); }
            100% { transform: translateY(0px) rotate(0deg); }
        }

        .gold-text {
            color: #FFD700;
            font-weight: bold;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            font-size: 1.2rem;
        }

        /* Effets de particules */
        .particle {
            position: absolute;
            background: #FFD700;
            border-radius: 50%;
            pointer-events: none;
            z-index: 1;
        }

        /* Styles pour les ballons */
        .balloon {
            position: absolute;
            width: 50px;
            height: 70px;
            background: linear-gradient(45deg, #FF1493, #FFD700);
            border-radius: 50%;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            animation: floatUp 5s ease-in-out infinite;
            z-index: 3;
        }

        .balloon::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            width: 2px;
            height: 20px;
            background: #fff;
            transform: translateX(-50%);
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) scale(1);
                opacity: 1;
            }
            100% {
                transform: translateY(-200vh) scale(0.8);
                opacity: 0;
            }
        }

        /* Effet d'étoiles scintillantes */
        .star {
            position: absolute;
            width: 5px;
            height: 5px;
            background: #FFD700;
            border-radius: 50%;
            animation: twinkle 2s infinite ease-in-out;
            opacity: 0.8;
        }

        @keyframes twinkle {
            0%, 100% {
                opacity: 0.5;
                transform: scale(1);
            }
            50% {
                opacity: 1;
                transform: scale(1.5);
            }
        }

        /* Styles responsives pour les téléphones */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }

            .card {
                padding: 20px;
                max-width: 100%;
                border-radius: 15px;
            }

            h1 {
                font-size: 2.5rem;
            }

            .message {
                font-size: 1rem;
                line-height: 1.5;
            }

            button {
                padding: 8px 20px;
                font-size: 0.9rem;
            }

            .music-container {
                padding: 15px;
                margin: 10px 0;
            }

            .emoji {
                font-size: 1.5rem;
            }

            .gold-text {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <h1><span class="emoji">🎉</span> JOYEUX ANNIVERSAIRE AMI  <span class="emoji">🎂</span></h1>
        
        <div class="message">
            <p>En ce jour spécial,j'aimerais souhaiter un Joyeuxanniversaire à une personne incroyable  !</p>
            <p>Si la joie était une personne,elle porterait ton nom! Merci d'illuminer le monde juste en existant.
            Que cette annéé t'apporte autant de bonheur que tu en distribue autour de toi!</p>
            <p>Désolé j'aurais aimer mettre une musique de <span class="gold-text">NINHO</span>.</p>
        </div>

        <!-- Section Musique -->
        <div class="music-container">
            <h3>Naza - " Happy Birthday"</h3>
            <p><em>"C'est ton jour"</em></p>
            
            <div class="music-player">
                <!-- Remplacez ceci par votre propre fichier audio légal -->
                <audio controls autoplay loop>
                    <source src="C:\Users\HP\Documents\Mon premier site en HTML\mes_essais\Diamountene\Happy_Birthday(256k).mp3" type="audio/mpeg">
                    Votre navigateur ne supporte pas l'élément audio.
                </audio>
            </div>
            
            <p style="font-size: 0.9rem; margin-top: 10px;">
                <i>Pour une expérience optimale, activez le son</i> 🔈
            </p>
        </div>

        <button id="showBtn">Voir mes vœux spéciaux</button>
        
        <div id="moreWishes" class="hidden">
            <p class="gold-text">💰 Prospérité et réussite à ton image</p>
            <p class="gold-text">❤️ Beaucoup d'amour et de moments inoubliables</p>
            <p class="gold-text">🎁 Tous tes souhaits réalisés</p>
            <p class="gold-text">😉 Reste comme tu es</p>
            <p class="gold-text">🌈 Que la vie te réserve de belles surprises</p>
            <p class="gold-text">🎊 Que chaque instant soit rempli de joie</p>
            <p class="gold-text">🎈 Que la santé et le bonheur t'accompagnent</p>
            <p class="gold-text">🎶 Que la musique de la vie soit douce à ton oreille</p>
            <p class="gold-text">🤣 J'oubliais si tu casse un truc tu vas remboursé avec bon coeur!</p>
            <p style="margin-top: 20px;"> Profite aux max de ta journée !</p>
        </div>
    </div>

    <!-- Confettis et animations -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <script>
        // Effets de particules dorées
        function createParticles() {
            const particles = 50;
            for (let i = 0; i < particles; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Position aléatoire
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                
                // Taille aléatoire
                const size = Math.random() * 10 + 5;
                
                // Animation aléatoire
                const duration = Math.random() * 10 + 10;
                const delay = Math.random() * 5;
                
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.opacity = Math.random() * 0.5 + 0.5;
                particle.style.animation = `float ${duration}s ease-in-out ${delay}s infinite`;
                
                document.body.appendChild(particle);
            }
        }

        // Confettis dorés et roses
        function fireConfetti() {
            // Confettis depuis le haut
            confetti({
                particleCount: 150,
                spread: 70,
                origin: { y: 0 },
                colors: ['#FFD700', '#FF1493', '#FFFFFF'],
                shapes: ['circle', 'star'],
                scalar: 1.2
            });
            
            // Confettis depuis les côtés
            setTimeout(() => {
                confetti({
                    particleCount: 100,
                    angle: 60,
                    spread: 55,
                    origin: { x: 0 }
                });
                
                confetti({
                    particleCount: 100,
                    angle: 120,
                    spread: 55,
                    origin: { x: 1 }
                });
            }, 300);
        }

        // Fonction pour créer des étoiles scintillantes
        function createStars() {
            const starCount = 100;
            for (let i = 0; i < starCount; i++) {
                const star = document.createElement('div');
                star.classList.add('star');

                // Position aléatoire
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;

                star.style.left = `${posX}%`;
                star.style.top = `${posY}%`;

                // Taille aléatoire
                const size = Math.random() * 3 + 2;
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;

                // Durée d'animation aléatoire
                const duration = Math.random() * 2 + 1;
                star.style.animationDuration = `${duration}s`;

                document.body.appendChild(star);
            }
        }

        // Lancement automatique au chargement
        window.onload = function() {
            createParticles();
            fireConfetti();
            createStars();
            
            // Confettis toutes les 20 secondes
            setInterval(fireConfetti, 20000);
            
            // Essayer de lancer la musique automatiquement (peut être bloqué par le navigateur)
            const audio = document.querySelector('audio');
            audio.volume = 0.7;
            audio.play().catch(e => console.log("Lecture automatique bloquée - cliquez pour jouer"));
        };

        // Confettis au clic n'importe où
        document.addEventListener('click', function() {
            confetti({
                particleCount: 50,
                spread: 50,
                origin: { y: 0.7 },
                colors: ['#FFD700', '#FF1493']
            });
        });

        // Fonction pour créer un ballon
        function createBalloon() {
            const balloon = document.createElement('div');
            balloon.classList.add('balloon');

            // Position aléatoire horizontale
            const posX = Math.random() * 100;
            balloon.style.left = `${posX}%`;

            // Couleur aléatoire
            const colors = ['#FF1493', '#FFD700', '#00FFFF', '#FF4500', '#ADFF2F'];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            balloon.style.background = `linear-gradient(45deg, ${randomColor}, #FFFFFF)`;

            document.body.appendChild(balloon);

            // Supprimer le ballon après l'animation
            setTimeout(() => {
                balloon.remove();
            }, 5000);
        }

        // Ajouter des ballons au clic sur le bouton
        document.getElementById('showBtn').addEventListener('click', function() {
            document.getElementById('moreWishes').classList.remove('hidden');
            this.style.display = 'none';

            // Lancer l'animation des ballons
            for (let i = 0; i < 20; i++) {
                setTimeout(createBalloon, i * 200);
            }

            // Mega confettis
            for (let i = 0; i < 8; i++) {
                setTimeout(() => {
                    confetti({
                        particleCount: 100,
                        angle: 45 + (i * 15),
                        spread: 60,
                        origin: { x: 0 },
                        colors: ['#FFD700', '#FF1493', '#00FFFF']
                    });
                }, i * 150);
            }

            // Confettis en éventail
            setTimeout(() => {
                for (let i = 0; i < 5; i++) {
                    confetti({
                        particleCount: 80,
                        angle: 90,
                        spread: 100,
                        startVelocity: 45,
                        origin: { y: 0.5 }
                    });
                }
            }, 1200);
        });
    </script>
</body>
</html>
