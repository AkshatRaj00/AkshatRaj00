<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Akshat Raj - AI Engineer & Full-Stack Developer</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #3081F7;
            --secondary: #7C3AED;
            --accent: #06FFA5;
            --bg-dark: #0D1117;
            --bg-card: #161B22;
            --text-primary: #F0F6FC;
            --text-secondary: #8B949E;
            --gradient: linear-gradient(135deg, #3081F7 0%, #7C3AED 50%, #06FFA5 100%);
            --glow: 0 0 20px rgba(48, 129, 247, 0.3);
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: var(--bg-dark);
            color: var(--text-primary);
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        /* Animated Background */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }
        
        .floating-shapes {
            position: absolute;
            width: 100%;
            height: 100%;
        }
        
        .shape {
            position: absolute;
            border-radius: 50%;
            animation: float 20s infinite linear;
        }
        
        .shape:nth-child(1) { background: var(--primary); width: 80px; height: 80px; top: 20%; left: 10%; animation-duration: 25s; }
        .shape:nth-child(2) { background: var(--secondary); width: 60px; height: 60px; top: 60%; left: 80%; animation-duration: 30s; }
        .shape:nth-child(3) { background: var(--accent); width: 40px; height: 40px; top: 80%; left: 20%; animation-duration: 20s; }
        .shape:nth-child(4) { background: var(--primary); width: 100px; height: 100px; top: 40%; left: 70%; animation-duration: 35s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            25% { transform: translateY(-20px) rotate(90deg); }
            50% { transform: translateY(-40px) rotate(180deg); }
            75% { transform: translateY(-20px) rotate(270deg); }
        }
        
        /* Header Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: radial-gradient(ellipse at center, rgba(48, 129, 247, 0.1) 0%, transparent 70%);
        }
        
        .hero-content {
            text-align: center;
            max-width: 1200px;
            padding: 2rem;
            animation: fadeInUp 1s ease-out;
        }
        
        .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: var(--gradient);
            margin: 0 auto 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            box-shadow: var(--glow);
            animation: pulse 3s infinite;
        }
        
        .typing-text {
            font-size: 3.5rem;
            font-weight: 800;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
            opacity: 0;
            animation: fadeIn 1s ease-out 0.5s forwards;
        }
        
        .hero-badges {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }
        
        .badge {
            padding: 0.8rem 1.5rem;
            background: var(--bg-card);
            border: 1px solid var(--primary);
            border-radius: 50px;
            text-decoration: none;
            color: var(--text-primary);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .badge:hover {
            transform: translateY(-5px);
            box-shadow: var(--glow);
            border-color: var(--accent);
        }
        
        .badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            transition: left 0.5s;
        }
        
        .badge:hover::before {
            left: 100%;
        }
        
        /* Tech Stack Grid */
        .tech-stack {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }
        
        .tech-card {
            background: var(--bg-card);
            border: 1px solid rgba(48, 129, 247, 0.2);
            border-radius: 20px;
            padding: 2rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .tech-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: var(--gradient);
        }
        
        .tech-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(48, 129, 247, 0.2);
            border-color: var(--primary);
        }
        
        .tech-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
            animation: bounce 2s infinite;
        }
        
        .tech-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }
        
        .tech-tag {
            background: rgba(48, 129, 247, 0.1);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid rgba(48, 129, 247, 0.3);
        }
        
        /* Projects Section */
        .projects {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .project-card {
            background: var(--bg-card);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid rgba(124, 58, 237, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
        }
        
        .project-card:hover {
            transform: scale(1.02);
            box-shadow: 0 25px 50px rgba(124, 58, 237, 0.2);
        }
        
        .project-header {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .project-icon {
            font-size: 2rem;
            margin-right: 1rem;
            animation: rotate 10s linear infinite;
        }
        
        .project-title {
            font-size: 1.8rem;
            color: var(--secondary);
            margin: 0;
        }
        
        .project-description {
            color: var(--text-secondary);
            margin-bottom: 1rem;
            line-height: 1.8;
        }
        
        .project-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
            margin: 1rem 0;
        }
        
        .feature {
            background: rgba(6, 255, 165, 0.1);
            padding: 1rem;
            border-radius: 10px;
            border-left: 3px solid var(--accent);
        }
        
        /* Interactive Console */
        .console-section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .console {
            background: #1a1a1a;
            border-radius: 15px;
            padding: 1rem;
            font-family: 'JetBrains Mono', monospace;
            border: 1px solid var(--primary);
            position: relative;
            overflow: hidden;
        }
        
        .console-header {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 1px solid #333;
        }
        
        .console-dots {
            display: flex;
            gap: 0.5rem;
            margin-right: 1rem;
        }
        
        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .dot.red { background: #ff5f56; }
        .dot.yellow { background: #ffbd2e; }
        .dot.green { background: #27ca3f; }
        
        .console-content {
            color: var(--accent);
            font-size: 0.9rem;
            line-height: 1.8;
        }
        
        .prompt {
            color: var(--primary);
        }
        
        .typing-cursor {
            animation: blink 1s infinite;
        }
        
        /* Stats Section */
        .stats {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(48, 129, 247, 0.2);
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--glow);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary);
            display: block;
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }
        
        /* Contact Section */
        .contact {
            padding: 4rem 2rem;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            background: radial-gradient(ellipse at center, rgba(124, 58, 237, 0.1) 0%, transparent 70%);
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-item {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid var(--secondary);
            transition: all 0.3s ease;
            text-decoration: none;
            color: var(--text-primary);
        }
        
        .contact-item:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(124, 58, 237, 0.3);
            border-color: var(--accent);
        }
        
        .contact-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            display: block;
            color: var(--secondary);
        }
        
        /* Animations */
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
        
        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                box-shadow: var(--glow);
            }
            50% {
                transform: scale(1.05);
                box-shadow: 0 0 40px rgba(48, 129, 247, 0.5);
            }
        }
        
        @keyframes glow {
            from {
                text-shadow: 0 0 20px rgba(48, 129, 247, 0.5);
            }
            to {
                text-shadow: 0 0 30px rgba(48, 129, 247, 0.8), 0 0 40px rgba(124, 58, 237, 0.5);
            }
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .typing-text {
                font-size: 2.5rem;
            }
            
            .hero-badges {
                flex-direction: column;
                align-items: center;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
            
            .project-features {
                grid-template-columns: 1fr;
            }
        }
        
        /* Scroll animations */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease;
        }
        
        .animate-on-scroll.animated {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: var(--bg-dark);
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--secondary);
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="bg-animation">
        <div class="floating-shapes">
            <div class="shape"></div>
            <div class="shape"></div>
            <div class="shape"></div>
            <div class="shape"></div>
        </div>
    </div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="profile-image">
                🤖
            </div>
            <h1 class="typing-text" id="typing-text">Akshat Raj</h1>
            <p class="subtitle">AI Engineer & Full-Stack Developer | Building Emotion-Aware Intelligence</p>
            
            <div class="hero-badges">
                <a href="https://onepersonai-website.vercel.app/" class="badge">🌐 Website</a>
                <a href="https://linkedin.com/in/akshatraj00" class="badge">💼 LinkedIn</a>
                <a href="https://akshatraj00.github.io/AkshatRaj-portfolio/" class="badge">📂 Portfolio</a>
                <a href="https://orcid.org/0009-0005-8565-0145" class="badge">🔬 ORCID</a>
            </div>
        </div>
    </section>

    <!-- Tech Stack Section -->
    <section class="tech-stack animate-on-scroll">
        <h2 class="section-title">🛠️ Core Competencies & Tech Stack</h2>
        <div class="tech-grid">
            <div class="tech-card">
                <span class="tech-icon">⚡</span>
                <h3>Frontend Development</h3>
                <p>Creating stunning, responsive user interfaces with modern frameworks and cutting-edge design principles.</p>
                <div class="tech-list">
                    <span class="tech-tag">React</span>
                    <span class="tech-tag">Next.js</span>
                    <span class="tech-tag">TypeScript</span>
                    <span class="tech-tag">JavaScript</span>
                    <span class="tech-tag">HTML5</span>
                    <span class="tech-tag">CSS3</span>
                </div>
            </div>
            
            <div class="tech-card">
                <span class="tech-icon">🔧</span>
                <h3>Backend & Database</h3>
                <p>Building scalable, secure server architectures and efficient database solutions for enterprise applications.</p>
                <div class="tech-list">
                    <span class="tech-tag">Node.js</span>
                    <span class="tech-tag">Express.js</span>
                    <span class="tech-tag">Python Flask</span>
                    <span class="tech-tag">MongoDB</span>
                    <span class="tech-tag">REST APIs</span>
                </div>
            </div>
            
            <div class="tech-card">
                <span class="tech-icon">🧠</span>
                <h3>AI & Machine Learning</h3>
                <p>Developing intelligent systems with deep learning, computer vision, and natural language processing capabilities.</p>
                <div class="tech-list">
                    <span class="tech-tag">TensorFlow</span>
                    <span class="tech-tag">PyTorch</span>
                    <span class="tech-tag">Scikit-learn</span>
                    <span class="tech-tag">OpenCV</span>
                    <span class="tech-tag">NLTK</span>
                    <span class="tech-tag">Computer Vision</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Console -->
    <section class="console-section animate-on-scroll">
        <h2 class="section-title">💻 Interactive Development Console</h2>
        <div class="console">
            <div class="console-header">
                <div class="console-dots">
                    <div class="dot red"></div>
                    <div class="dot yellow"></div>
                    <div class="dot green"></div>
                </div>
                <span>akshat@ai-terminal ~ %</span>
            </div>
            <div class="console-content" id="console-content">
                <div><span class="prompt">akshat@ai-terminal:~$</span> whoami</div>
                <div>AI Engineer & Full-Stack Developer</div>
                <div><span class="prompt">akshat@ai-terminal:~$</span> cat skills.json</div>
                <div>{</div>
                <div>  "languages": ["Python", "JavaScript", "TypeScript", "C++"],</div>
                <div>  "frameworks": ["React", "Next.js", "TensorFlow", "PyTorch"],</div>
                <div>  "specialization": "Emotion-Aware AI Systems",</div>
                <div>  "passion": "Human-Centered Technology"</div>
                <div>}</div>
                <div><span class="prompt">akshat@ai-terminal:~$</span> <span class="typing-cursor">_</span></div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects animate-on-scroll">
        <h2 class="section-title">🚀 Featured Projects</h2>
        
        <div class="project-card">
            <div class="project-header">
                <span class="project-icon">🧠</span>
                <h3 class="project-title">NeuroBreak-AI | Emotion-Aware Mental Wellness AI</h3>
            </div>
            <p class="project-description">
                A revolutionary 24/7 AI-powered companion designed to promote mindfulness and mental wellness. 
                Uses advanced NLP to detect user emotions from text in real-time, offering supportive and human-like conversations.
            </p>
            <div class="project-features">
                <div class="feature">
                    <strong>Real-time Emotion Detection</strong><br>
                    Advanced sentiment analysis using deep learning
                </div>
                <div class="feature">
                    <strong>Mood Analysis & Patterns</strong><br>
                    ML-powered insights into emotional well-being
                </div>
                <div class="feature">
                    <strong>Interactive UI</strong><br>
                    Beautiful, responsive interface built with Streamlit
                </div>
                <div class="feature">
                    <strong>Tech Stack</strong><br>
                    Python, Streamlit, TensorFlow, NLTK, Scikit-learn
                </div>
            </div>
        </div>
        
        <div class="project-card">
            <div class="project-header">
                <span class="project-icon">🤖</span>
                <h3 class="project-title">AkshaBot-Pro | Advanced AI Chatbot System</h3>
            </div>
            <p class="project-description">
                An enterprise-grade, scalable chatbot built for professional applications. 
                Leverages robust backend architecture and advanced context understanding for sophisticated conversational AI.
            </p>
            <div class="project-features">
                <div class="feature">
                    <strong>Scalable Architecture</strong><br>
                    Built with Flask for enterprise-grade performance
                </div>
                <div class="feature">
                    <strong>Advanced NLP</strong><br>
                    Context-aware conversations with memory retention
                </div>
                <div class="feature">
                    <strong>RESTful APIs</strong><br>
                    Easy integration with existing systems
                </div>
                <div class="feature">
                    <strong>Tech Stack</strong><br>
                    Python, Flask, JavaScript, TensorFlow, REST APIs
                </div>
            </div>
        </div>
        
        <div class="project-card">
            <div class="project-header">
                <span class="project-icon">🎬</span>
                <h3 class="project-title">MultimodalAI-Assistant | Next-Gen AI Interface</h3>
            </div>
            <p class="project-description">
                A cutting-edge AI assistant capable of processing multiple input types simultaneously, including voice, text, and images. 
                This project explores the future of human-computer interaction through multimodal AI.
            </p>
            <div class="project-features">
                <div class="feature">
                    <strong>Voice Recognition</strong><br>
                    Advanced speech-to-text processing
                </div>
                <div class="feature">
                    <strong>Image Processing</strong><br>
                    Computer vision with OpenCV integration
                </div>
                <div class="feature">
                    <strong>Text Analysis</strong><br>
                    Natural language understanding and generation
                </div>
                <div class="feature">
                    <strong>Tech Stack</strong><br>
                    Python, OpenCV, SpeechRecognition, PyTorch, NLTK
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats animate-on-scroll">
        <h2 class="section-title">📊 GitHub Statistics & Achievements</h2>
        <div class="stats-grid">
            <div class="stat-card">
                <span class="stat-number" id="projects-count">15+</span>
                <span class="stat-label">Projects Completed</span>
            </div>
            <div class="stat-card">
                <span class="stat-number" id="commits-count">500+</span>
                <span class="stat-label">Commits This Year</span>
            </div>
            <div class="stat-card">
                <span class="stat-number" id="languages-count">8</span>
                <span class="stat-label">Programming Languages</span>
            </div>
            <div class="stat-card">
                <span class="stat-number" id="contributions-count">365</span>
                <span class="stat-label">Days Active</span>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact animate-on-scroll">
        <h2 class="section-title">📫 Let's Connect & Collaborate!</h2>
        <p class="subtitle">Always open to discussing new projects, collaborations, or opportunities in AI and tech.</p>
        
        <div class="contact-grid">
            <a href="mailto:akshat@onepersonai.com" class="contact-item">
                <span class="contact-icon">📧</span>
                <h3>Email</h3>
                <p>akshat@onepersonai.com</p>
            </a>
            
            <a href="https://linkedin.com/in/akshatraj00" class="contact-item">
                <span class="contact-icon">💼</span>
                <h3>LinkedIn</h3>
                <p>Professional Network</p>
            </a>
            
            <a href="https://github.com/AkshatRaj00" class="contact-item">
                <span class="contact-icon">💻</span>
                <h3>GitHub</h3>
                <p>Code Repository</p>
            </a>
        </div>
        
        <div style="margin-top: 4rem; padding: 2rem; background: rgba(48, 129, 247, 0.1); border-radius: 15px; border: 1px solid var(--primary);">
            <h3 style="color: var(--primary); margin-bottom: 1rem;">🚀 Mission Statement</h3>
            <p style="font-size: 1.1rem; font-style: italic;">
                "Leveraging AI and software development to build technologies that are not just intelligent, 
                but also empathetic and beneficial to society. Passionate about creating harmonious 
                interactions between humans and technology."
            </p>
        </div>
        
        <div style="margin-top: 2rem; font-size: 1.2rem; font-weight: 600;">
            <span style="background: var(--gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">
                "Building the Future, One Line of Code at a Time"
            </span>
        </div>
    </section>

    <script>
        // Typing animation for hero text
        const texts = [
            "Akshat Raj",
            "AI Engineer",
            "Full-Stack Developer",
            "Innovation Creator",
            "Tech Enthusiast"
        ];
        
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');
        
        function typeWriter() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            let typingSpeed = isDeleting ? 50 : 100;
            
            if (!isDeleting && charIndex === currentText.length) {
                typingSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
                typingSpeed = 500;
            }
            
            setTimeout(typeWriter, typingSpeed);
        }
        
        // Start typing animation
        setTimeout(typeWriter, 1000);
        
        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);
        
        // Observe all elements with animate-on-scroll class
        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            observer.observe(el);
        });
        
        // Animated counter for stats
        function animateCounter(elementId, finalValue, duration = 2000) {
            const element = document.getElementById(elementId);
            const startValue = 0;
            const increment = finalValue / (duration / 16);
            let currentValue = startValue;
            
            const timer = setInterval(() => {
                currentValue += increment;
                if (currentValue >= finalValue) {
                    element.textContent = finalValue.toString().includes('+') ? finalValue : finalValue + '+';
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(currentValue).toString();
                }
            }, 16);
        }
        
        // Trigger counter animations when stats section is visible
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateCounter('projects-count', 15);
                    animateCounter('commits-count', 500);
                    animateCounter('languages-count', 8);
                    animateCounter('contributions-count', 365);
                    statsObserver.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        const statsSection = document.querySelector('.stats');
        if (statsSection) {
            statsObserver.observe(statsSection);
        }
        
        // Interactive console typing effect
        const consoleCommands = [
            { command: 'ls -la', output: ['drwxr-xr-x  8 akshat  staff   256 Sep  3 10:30 .', 'drwxr-xr-x 15 akshat  staff   480 Sep  3 10:29 ..', 'drwxr-xr-x  3 akshat  staff    96 Sep  3 10:25 ai-projects/', 'drwxr-xr-x  5 akshat  staff   160 Sep  3 10:28 web-apps/', '-rw-r--r--  1 akshat  staff  1024 Sep  3 10:30 README.md'] },
            { command: 'cd ai-projects && ls', output: ['neurobreak-ai/', 'akshabot-pro/', 'multimodal-assistant/', 'emotion-detector/'] },
            { command: 'python -c "print(\'Hello, AI World!\')"', output: ['Hello, AI World!'] },
            { command: 'git status', output: ['On branch main', 'Your branch is up to date with \'origin/main\'.', 'nothing to commit, working tree clean'] }
        ];
        
        let consoleCommandIndex = 0;
        
        function typeConsoleCommand() {
            if (consoleCommandIndex < consoleCommands.length) {
                const cmd = consoleCommands[consoleCommandIndex];
                const consoleContent = document.getElementById('console-content');
                
                // Add command line
                const commandLine = document.createElement('div');
                commandLine.innerHTML = `<span class="prompt">akshat@ai-terminal:~$</span> ${cmd.command}`;
                consoleContent.appendChild(commandLine);
                
                // Add output
                setTimeout(() => {
                    cmd.output.forEach((line, index) => {
                        setTimeout(() => {
                            const outputLine = document.createElement('div');
                            outputLine.textContent = line;
                            consoleContent.appendChild(outputLine);
                        }, index * 100);
                    });
                    
                    // Add prompt for next command
                    setTimeout(() => {
                        consoleCommandIndex++;
                        if (consoleCommandIndex < consoleCommands.length) {
                            setTimeout(typeConsoleCommand, 2000);
                        } else {
                            // Add final prompt
                            const finalPrompt = document.createElement('div');
                            finalPrompt.innerHTML = '<span class="prompt">akshat@ai-terminal:~$</span> <span class="typing-cursor">_</span>';
                            consoleContent.appendChild(finalPrompt);
                        }
                    }, cmd.output.length * 100 + 500);
                }, 500);
            }
        }
        
        // Start console animation when section is visible
        const consoleObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    setTimeout(typeConsoleCommand, 1000);
                    consoleObserver.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        const consoleSection = document.querySelector('.console-section');
        if (consoleSection) {
            consoleObserver.observe(consoleSection);
        }
        
        // Particle system for hero background
        class Particle {
            constructor(canvas) {
                this.canvas = canvas;
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.vx = (Math.random() - 0.5) * 0.5;
                this.vy = (Math.random() - 0.5) * 0.5;
                this.size = Math.random() * 2 + 1;
                this.opacity = Math.random() * 0.5 + 0.2;
            }
            
            update() {
                this.x += this.vx;
                this.y += this.vy;
                
                if (this.x < 0 || this.x > this.canvas.width) this.vx = -this.vx;
                if (this.y < 0 || this.y > this.canvas.height) this.vy = -this.vy;
            }
            
            draw(ctx) {
                ctx.save();
                ctx.globalAlpha = this.opacity;
                ctx.fillStyle = '#3081F7';
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
                ctx.restore();
            }
        }
        
        // Create particle canvas
        function createParticleSystem() {
            const hero = document.querySelector('.hero');
            const canvas = document.createElement('canvas');
            const ctx = canvas.getContext('2d');
            
            canvas.style.position = 'absolute';
            canvas.style.top = '0';
            canvas.style.left = '0';
            canvas.style.width = '100%';
            canvas.style.height = '100%';
            canvas.style.pointerEvents = 'none';
            canvas.style.zIndex = '-1';
            
            hero.appendChild(canvas);
            
            function resize() {
                canvas.width = hero.offsetWidth;
                canvas.height = hero.offsetHeight;
            }
            
            const particles = [];
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                particles.push(new Particle(canvas));
            }
            
            function animate() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                particles.forEach(particle => {
                    particle.update();
                    particle.draw(ctx);
                });
                
                // Draw connections
                for (let i = 0; i < particles.length; i++) {
                    for (let j = i + 1; j < particles.length; j++) {
                        const dx = particles[i].x - particles[j].x;
                        const dy = particles[i].y - particles[j].y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 100) {
                            ctx.save();
                            ctx.globalAlpha = (100 - distance) / 100 * 0.2;
                            ctx.strokeStyle = '#3081F7';
                            ctx.lineWidth = 0.5;
                            ctx.beginPath();
                            ctx.moveTo(particles[i].x, particles[i].y);
                            ctx.lineTo(particles[j].x, particles[j].y);
                            ctx.stroke();
                            ctx.restore();
                        }
                    }
                }
                
                requestAnimationFrame(animate);
            }
            
            resize();
            animate();
            
            window.addEventListener('resize', resize);
        }
        
        // Initialize particle system
        setTimeout(createParticleSystem, 1000);
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
        
        // Add cursor trail effect
        let mouseTrail = [];
        
        document.addEventListener('mousemove', (e) => {
            mouseTrail.push({ x: e.clientX, y: e.clientY, age: 0 });
            
            if (mouseTrail.length > 20) {
                mouseTrail.shift();
            }
        });
        
        function animateMouseTrail() {
            const existingTrails = document.querySelectorAll('.mouse-trail');
            existingTrails.forEach(trail => trail.remove());
            
            mouseTrail.forEach((point, index) => {
                const trail = document.createElement('div');
                trail.className = 'mouse-trail';
                trail.style.position = 'fixed';
                trail.style.left = point.x + 'px';
                trail.style.top = point.y + 'px';
                trail.style.width = '6px';
                trail.style.height = '6px';
                trail.style.borderRadius = '50%';
                trail.style.background = `rgba(48, 129, 247, ${(1 - index / 20) * 0.5})`;
                trail.style.pointerEvents = 'none';
                trail.style.zIndex = '1000';
                trail.style.transform = 'translate(-50%, -50%)';
                
                document.body.appendChild(trail);
                
                point.age++;
                if (point.age > 30) {
                    trail.style.opacity = '0';
                    setTimeout(() => trail.remove(), 300);
                }
            });
            
            mouseTrail = mouseTrail.filter(point => point.age <= 30);
            requestAnimationFrame(animateMouseTrail);
        }
        
        // Start mouse trail animation
        animateMouseTrail();
        
        // Add page load animation
        window.addEventListener('load', () => {
            document.body.style.opacity = '1';
            document.body.style.transform = 'translateY(0)';
        });
        
        // Add dynamic theme colors based on time
        function updateThemeColors() {
            const hour = new Date().getHours();
            const root = document.documentElement;
            
            if (hour >= 6 && hour < 12) {
                // Morning theme
                root.style.setProperty('--primary', '#3081F7');
                root.style.setProperty('--secondary', '#7C3AED');
                root.style.setProperty('--accent', '#06FFA5');
            } else if (hour >= 12 && hour < 18) {
                // Afternoon theme
                root.style.setProperty('--primary', '#FF6B6B');
                root.style.setProperty('--secondary', '#4ECDC4');
                root.style.setProperty('--accent', '#FFE66D');
            } else {
                // Evening/Night theme
                root.style.setProperty('--primary', '#8B5CF6');
                root.style.setProperty('--secondary', '#06D6A0');
                root.style.setProperty('--accent', '#F72585');
            }
        }
        
        // Update theme colors on load and every hour
        updateThemeColors();
        setInterval(updateThemeColors, 3600000);
        
        // Add Easter egg - Konami code
        let konamiCode = [];
        const konami = [38, 38, 40, 40, 37, 39, 37, 39, 66, 65];
        
        document.addEventListener('keydown', (e) => {
            konamiCode.push(e.keyCode);
            if (konamiCode.length > konami.length) {
                konamiCode.shift();
            }
            
            if (JSON.stringify(konamiCode) === JSON.stringify(konami)) {
                // Easter egg activated!
                document.body.style.animation = 'rainbow 2s infinite';
                setTimeout(() => {
                    document.body.style.animation = '';
                    alert('🎉 Easter Egg Activated! You found the secret code!');
                }, 2000);
                konamiCode = [];
            }
        });
        
        // Add rainbow animation for easter egg
        const style = document.createElement('style');
        style.textContent = `
            @keyframes rainbow {
                0% { filter: hue-rotate(0deg); }
                25% { filter: hue-rotate(90deg); }
                50% { filter: hue-rotate(180deg); }
                75% { filter: hue-rotate(270deg); }
                100% { filter: hue-rotate(360deg); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
