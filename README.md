<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abhilasha Kapadnis - Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #21262d 100%);
            color: #e6edf3;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            text-align: center;
            margin-bottom: 3rem;
            animation: fadeInUp 1s ease-out;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid #58a6ff;
            margin: 0 auto 2rem;
            background: linear-gradient(45deg, #58a6ff, #bc8cff);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            animation: float 3s ease-in-out infinite;
        }

        .name {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, #58a6ff, #bc8cff, #f85149);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 2s ease-in-out infinite alternate;
        }

        .title {
            font-size: 1.5rem;
            color: #7d8590;
            margin-bottom: 2rem;
            animation: typewriter 3s steps(40) 1s both;
            overflow: hidden;
            border-right: 2px solid #58a6ff;
            white-space: nowrap;
            width: 0;
            margin: 0 auto 2rem;
        }

        .stats-container {
            display: flex;
            justify-content: center;
            margin-bottom: 3rem;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .trophy-section {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .trophy-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.3);
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .info-card {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out;
        }

        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.2);
            border-color: #58a6ff;
        }

        .info-card h3 {
            color: #58a6ff;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 0.8rem;
            transition: transform 0.3s ease;
        }

        .info-item:hover {
            transform: translateX(10px);
        }

        .info-icon {
            margin-right: 0.8rem;
            color: #58a6ff;
            font-size: 1.2rem;
        }

        .technologies {
            margin-top: 3rem;
            animation: fadeInUp 1s ease-out 1s both;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .tech-item {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 15px 30px rgba(88, 166, 255, 0.3);
            border-color: #58a6ff;
        }

        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            display: block;
        }

        .tech-name {
            font-size: 0.9rem;
            color: #7d8590;
        }

        .contact-section {
            text-align: center;
            margin-top: 3rem;
            padding: 2rem;
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 12px;
            animation: fadeInUp 1s ease-out 1.5s both;
        }

        .email-link {
            color: #58a6ff;
            text-decoration: none;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .email-link:hover {
            color: #bc8cff;
            text-shadow: 0 0 10px rgba(188, 140, 255, 0.5);
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            background: #58a6ff;
            border-radius: 50%;
            animation: float-particle 15s linear infinite;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        @keyframes glow {
            from { text-shadow: 0 0 20px rgba(88, 166, 255, 0.5); }
            to { text-shadow: 0 0 30px rgba(188, 140, 255, 0.8), 0 0 40px rgba(248, 81, 73, 0.3); }
        }

        @keyframes typewriter {
            to { width: 100%; }
        }

        @keyframes float-particle {
            0% {
                transform: translateY(100vh) translateX(-10px);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) translateX(10px);
                opacity: 0;
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .name {
                font-size: 2.5rem;
            }
            
            .title {
                font-size: 1.2rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <header class="header">
            <div class="profile-img">👋</div>
            <h1 class="name">Abhilasha Kapadnis</h1>
            <p class="title">A passionate frontend developer from India</p>
        </header>

        <div class="stats-container">
            <div class="trophy-section">
                <h3>🏆 GitHub Achievements</h3>
                <p>Building amazing projects with code and creativity</p>
            </div>
        </div>

        <div class="info-grid">
            <div class="info-card">
                <h3>🚀 Currently Working On</h3>
                <div class="info-item">
                    <span class="info-icon">🌱</span>
                    <span>Learning <strong>GitOps</strong> for modern DevOps workflows</span>
                </div>
            </div>

            <div class="info-card">
                <h3>💡 Ask Me About</h3>
                <div class="info-item">
                    <span class="info-icon">🔧</span>
                    <span><strong>Git</strong> - Version control mastery</span>
                </div>
                <div class="info-item">
                    <span class="info-icon">🐙</span>
                    <span><strong>GitHub</strong> - Collaboration & workflows</span>
                </div>
                <div class="info-item">
                    <span class="info-icon">⚙️</span>
                    <span><strong>GitOps</strong> - Modern deployment strategies</span>
                </div>
            </div>
        </div>

        <div class="contact-section">
            <h3>📫 Let's Connect!</h3>
            <p>Ready to collaborate on exciting projects?</p>
            <a href="mailto:abhilashakapdnis@gmail.com" class="email-link">abhilashakapdnis@gmail.com</a>
        </div>

        <div class="technologies">
            <h2 style="text-align: center; color: #58a6ff; margin-bottom: 1rem;">🛠️ Technologies & Tools</h2>
            
            <div class="tech-grid">
                <div class="tech-item" data-tech="Android">
                    <span class="tech-icon">🤖</span>
                    <div class="tech-name">Android</div>
                </div>
                <div class="tech-item" data-tech="Arduino">
                    <span class="tech-icon">🔌</span>
                    <div class="tech-name">Arduino</div>
                </div>
                <div class="tech-item" data-tech="AWS">
                    <span class="tech-icon">☁️</span>
                    <div class="tech-name">AWS</div>
                </div>
                <div class="tech-item" data-tech="Blender">
                    <span class="tech-icon">🎨</span>
                    <div class="tech-name">Blender</div>
                </div>
                <div class="tech-item" data-tech="C">
                    <span class="tech-icon">⚡</span>
                    <div class="tech-name">C</div>
                </div>
                <div class="tech-item" data-tech="Chart.js">
                    <span class="tech-icon">📊</span>
                    <div class="tech-name">Chart.js</div>
                </div>
                <div class="tech-item" data-tech="C++">
                    <span class="tech-icon">🔥</span>
                    <div class="tech-name">C++</div>
                </div>
                <div class="tech-item" data-tech="CSS3">
                    <span class="tech-icon">🎨</span>
                    <div class="tech-name">CSS3</div>
                </div>
                <div class="tech-item" data-tech=".NET">
                    <span class="tech-icon">🔷</span>
                    <div class="tech-name">.NET</div>
                </div>
                <div class="tech-item" data-tech="Firebase">
                    <span class="tech-icon">🔥</span>
                    <div class="tech-name">Firebase</div>
                </div>
                <div class="tech-item" data-tech="Gatsby">
                    <span class="tech-icon">🚀</span>
                    <div class="tech-name">Gatsby</div>
                </div>
                <div class="tech-item" data-tech="GCP">
                    <span class="tech-icon">🌐</span>
                    <div class="tech-name">GCP</div>
                </div>
                <div class="tech-item" data-tech="Git">
                    <span class="tech-icon">📚</span>
                    <div class="tech-name">Git</div>
                </div>
                <div class="tech-item" data-tech="HTML5">
                    <span class="tech-icon">🌐</span>
                    <div class="tech-name">HTML5</div>
                </div>
                <div class="tech-item" data-tech="Java">
                    <span class="tech-icon">☕</span>
                    <div class="tech-name">Java</div>
                </div>
                <div class="tech-item" data-tech="Jest">
                    <span class="tech-icon">🃏</span>
                    <div class="tech-name">Jest</div>
                </div>
                <div class="tech-item" data-tech="MongoDB">
                    <span class="tech-icon">🍃</span>
                    <div class="tech-name">MongoDB</div>
                </div>
                <div class="tech-item" data-tech="Node.js">
                    <span class="tech-icon">💚</span>
                    <div class="tech-name">Node.js</div>
                </div>
                <div class="tech-item" data-tech="Pandas">
                    <span class="tech-icon">🐼</span>
                    <div class="tech-name">Pandas</div>
                </div>
                <div class="tech-item" data-tech="Photoshop">
                    <span class="tech-icon">🖼️</span>
                    <div class="tech-name">Photoshop</div>
                </div>
                <div class="tech-item" data-tech="Python">
                    <span class="tech-icon">🐍</span>
                    <div class="tech-name">Python</div>
                </div>
                <div class="tech-item" data-tech="Sass">
                    <span class="tech-icon">💅</span>
                    <div class="tech-name">Sass</div>
                </div>
                <div class="tech-item" data-tech="Spring">
                    <span class="tech-icon">🌱</span>
                    <div class="tech-name">Spring</div>
                </div>
                <div class="tech-item" data-tech="Unity">
                    <span class="tech-icon">🎮</span>
                    <div class="tech-name">Unity</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.width = Math.random() * 4 + 2 + 'px';
                particle.style.height = particle.style.width;
                particle.style.animationDuration = Math.random() * 10 + 10 + 's';
                particle.style.animationDelay = Math.random() * 15 + 's';
                particlesContainer.appendChild(particle);
            }
        }

        // Add hover effects to tech items
        document.querySelectorAll('.tech-item').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.background = 'linear-gradient(45deg, rgba(88, 166, 255, 0.2), rgba(188, 140, 255, 0.2))';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.background = 'rgba(22, 27, 34, 0.8)';
            });
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all animated elements
        document.querySelectorAll('.info-card, .tech-item').forEach(el => {
            observer.observe(el);
        });

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Add stagger animation to tech items
            const techItems = document.querySelectorAll('.tech-item');
            techItems.forEach((item, index) => {
                item.style.animationDelay = (index * 0.1) + 's';
            });
        });

        // Add typing animation completion
        const titleElement = document.querySelector('.title');
        titleElement.addEventListener('animationend', function() {
            this.style.borderRight = 'none';
        });
    </script>
</body>
</html>
