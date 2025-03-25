<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anime Style Profile</title>
    <link href="https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #FF6B6B;
            --secondary: #4ECDC4;
            --background: #2D2D2D;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, var(--background), #1A1A1A);
            color: white;
            font-family: 'Chakra Petch', sans-serif;
            min-height: 100vh;
            line-height: 1.6;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 3rem 2rem;
            position: relative;
        }

        /* Efecto de brillo dinámico */
        .glow {
            animation: glowEffect 2s ease-in-out infinite alternate;
        }

        @keyframes glowEffect {
            from {
                filter: drop-shadow(0 0 5px var(--primary));
            }
            to {
                filter: drop-shadow(0 0 20px var(--secondary));
            }
        }

        .profile-section {
            text-align: center;
            margin-bottom: 4rem;
        }

        .anime-avatar {
            width: 220px;
            height: 220px;
            border-radius: 50%;
            border: 4px solid var(--primary);
            clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
            margin-bottom: 1.5rem;
            transition: transform 0.4s;
        }

        .anime-avatar:hover {
            transform: rotate(5deg) scale(1.05);
        }

        .title {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .title::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--secondary), transparent);
            bottom: -10px;
            left: 0;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 1.8rem;
            border-radius: 15px;
            border: 1px solid var(--primary);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .project-card:hover {
            transform: translateY(-8px);
            background: rgba(255, 255, 255, 0.1);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, var(--secondary), transparent);
            animation: shine 4s infinite;
        }

        @keyframes shine {
            100% {
                transform: rotate(360deg);
            }
        }

        .social-links {
            margin-top: 4rem;
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        .social-icon {
            font-size: 2rem;
            color: white;
            transition: all 0.3s;
            position: relative;
        }

        .social-icon:hover {
            color: var(--primary);
            transform: scale(1.2);
        }

        .tech-badge {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            background: rgba(78, 205, 196, 0.2);
            border-radius: 20px;
            margin: 0.5rem 0.3rem;
            font-size: 0.9rem;
            border: 1px solid var(--secondary);
        }
    </style>
</head>
<body>
    <div class="container">
        <section class="profile-section">
            <img src="https://example.com/your-avatar.jpg" alt="Anime Style Avatar" class="anime-avatar glow">
            <h1 class="title">Creative Developer</h1>
            <p>🌟 Passionate about visual design and interactive experiences</p>
        </section>

        <section class="projects">
            <h2 class="title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>Character Database</h3>
                    <p>Interactive character showcase with dynamic UI</p>
                    <div class="tech-stack">
                        <span class="tech-badge">UI Design</span>
                        <span class="tech-badge">React</span>
                        <span class="tech-badge">API</span>
                    </div>
                </div>
                <!-- Añadir más proyectos -->
            </div>
        </section>

        <div class="social-links">
            <a href="#" class="social-icon"><i class="fab fa-github"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-linkedin"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-codepen"></i></a>
        </div>
    </div>
</body>
</html>
