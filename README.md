<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Subhi Arjaria - AI/ML Researcher</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 80px 0;
            background: rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 30px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            animation: slideInDown 1s ease-out;
        }

        .tagline {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 30px;
            animation: slideInUp 1s ease-out 0.3s both;
        }

        @keyframes slideInDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            animation: fadeIn 1s ease-out 0.6s both;
        }

        .social-link {
            padding: 12px 24px;
            background: rgba(255,255,255,0.1);
            border: 2px solid rgba(255,255,255,0.3);
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }

        .social-link:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Section Styles */
        .section {
            padding: 80px 0;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
        }

        /* Timeline Styles */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, #ff6b6b, #4ecdc4);
            transform: translateX(-50%);
        }

        .timeline-item {
            position: relative;
            width: 50%;
            padding: 30px;
            animation: slideInLeft 0.8s ease-out;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
            animation: slideInRight 0.8s ease-out;
        }

        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .timeline-content {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border: 2px solid rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
        }

        .timeline-content:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            background: rgba(255,255,255,0.15);
        }

        .timeline-dot {
            position: absolute;
            top: 50%;
            right: -25px;
            width: 20px;
            height: 20px;
            background: #ff6b6b;
            border-radius: 50%;
            transform: translateY(-50%);
            border: 4px solid white;
            box-shadow: 0 0 20px rgba(255,107,107,0.5);
        }

        .timeline-item:nth-child(even) .timeline-dot {
            left: -25px;
            right: auto;
            background: #4ecdc4;
            box-shadow: 0 0 20px rgba(78,205,196,0.5);
        }

        .timeline-year {
            font-size: 1.1rem;
            color: #4ecdc4;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .timeline-title {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .timeline-desc {
            opacity: 0.9;
            line-height: 1.6;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 40px;
        }

        .skill-category {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border: 2px solid rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        .skill-category h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #4ecdc4;
        }

        .skill-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            gap: 15px;
        }

        .skill-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 0.9rem;
        }

        .skill-info {
            flex: 1;
        }

        .skill-name {
            font-weight: 600;
            margin-bottom: 5px;
        }

        .skill-bar {
            height: 8px;
            background: rgba(255,255,255,0.2);
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 4px;
            transition: width 2s ease-out;
            width: 0%;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .project-card {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border: 2px solid rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            transition: left 0.5s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        .project-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: #4ecdc4;
        }

        .project-tech {
            font-style: italic;
            opacity: 0.8;
            margin-bottom: 15px;
        }

        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .stat-card {
            text-align: center;
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border: 2px solid rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            color: #4ecdc4;
            margin-bottom: 10px;
            counter-reset: stat-counter;
        }

        .stat-label {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .timeline::before {
                left: 30px;
            }

            .timeline-item {
                width: 100%;
                left: 0;
                padding-left: 60px;
            }

            .timeline-item:nth-child(even) {
                left: 0;
            }

            .timeline-dot {
                left: 20px !important;
                right: auto !important;
            }

            .name {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <section class="header">
        <div class="container">
            <div class="profile-img">👨‍💻</div>
            <h1 class="name">Subhi Arjaria</h1>
            <p class="tagline">AI/ML Researcher & Data Scientist</p>
            <div class="social-links">
                <a href="https://github.com/SubhiArjaria" class="social-link" target="_blank">GitHub</a>
                <a href="https://www.linkedin.com/in/subhi18082002/" class="social-link" target="_blank">LinkedIn</a>
                <a href="https://www.kaggle.com/" class="social-link" target="_blank">Kaggle</a>
                <a href="https://huggingface.co/Subhi09" class="social-link" target="_blank">HuggingFace</a>
                <a href="https://x.com/SubhiArjaria09" class="social-link" target="_blank">X (Twitter)</a>
                <a href="#" class="social-link" target="_blank">Resume</a>
            </div>
        </div>
    </section>

    <!-- Experience Timeline -->
    <section class="section">
        <div class="container">
            <h2 class="section-title fade-in">Professional Experience</h2>
            <div class="timeline">
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">Feb 2025 – Present</div>
                        <h3 class="timeline-title">AI Research Intern @ ZySec AI</h3>
                        <p class="timeline-desc">Optimizing large-scale AI models using CDE embeddings for security applications.</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2024</div>
                        <h3 class="timeline-title">ML Intern @ Feynn Lab</h3>
                        <p class="timeline-desc">Built AI-driven financial models leveraging deep learning & computer vision.</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2024</div>
                        <h3 class="timeline-title">Research Analyst @ Igurus Consultancy Service LLP</h3>
                        <p class="timeline-desc">Worked on Hindi NER and translation models.</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2023</div>
                        <h3 class="timeline-title">Data Analyst @ Psyliq</h3>
                        <p class="timeline-desc">Delivered insights using Power BI, Excel, Tableau, R & SQL across 5 projects.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Timeline -->
    <section class="section">
        <div class="container">
            <h2 class="section-title fade-in">Education Journey</h2>
            <div class="timeline">
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2025</div>
                        <h3 class="timeline-title">MSc AI & ML @ IIIT Lucknow</h3>
                        <p class="timeline-desc">CGPA: 9.22 - Specializing in Advanced AI/ML techniques</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2024</div>
                        <h3 class="timeline-title">Diploma in Data Science @ IIT Madras</h3>
                        <p class="timeline-desc">Grade A - Comprehensive Data Science Program</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2023</div>
                        <h3 class="timeline-title">BSc Mathematics @ Bipin Bihari Degree College</h3>
                        <p class="timeline-desc">75% - Strong mathematical foundation</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-dot"></div>
                        <div class="timeline-year">2020</div>
                        <h3 class="timeline-title">Class XII @ Sheer Wood College</h3>
                        <p class="timeline-desc">92.8% - Science Stream</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title fade-in">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category fade-in">
                    <h3>Programming Languages</h3>
                    <div class="skill-item">
                        <div class="skill-icon">🐍</div>
                        <div class="skill-info">
                            <div class="skill-name">Python</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="95"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">⚡</div>
                        <div class="skill-info">
                            <div class="skill-name">C++</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="85"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🗃️</div>
                        <div class="skill-info">
                            <div class="skill-name">SQL</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="90"></div></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category fade-in">
                    <h3>AI/ML Frameworks</h3>
                    <div class="skill-item">
                        <div class="skill-icon">🤗</div>
                        <div class="skill-info">
                            <div class="skill-name">Hugging Face</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="90"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🔗</div>
                        <div class="skill-info">
                            <div class="skill-name">LangChain</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="85"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🧠</div>
                        <div class="skill-info">
                            <div class="skill-name">TensorFlow</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="80"></div></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category fade-in">
                    <h3>Cloud & DevOps</h3>
                    <div class="skill-item">
                        <div class="skill-icon">☁️</div>
                        <div class="skill-info">
                            <div class="skill-name">AWS</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="75"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🐳</div>
                        <div class="skill-info">
                            <div class="skill-name">Docker</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="70"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🔧</div>
                        <div class="skill-info">
                            <div class="skill-name">MLflow</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="80"></div></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category fade-in">
                    <h3>Data Analytics</h3>
                    <div class="skill-item">
                        <div class="skill-icon">📊</div>
                        <div class="skill-info">
                            <div class="skill-name">Power BI</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="90"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🔢</div>
                        <div class="skill-info">
                            <div class="skill-name">Pandas</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="95"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">📈</div>
                        <div class="skill-info">
                            <div class="skill-name">Tableau</div>
                            <div class="skill-bar"><div class="skill-progress" data-width="85"></div></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title fade-in">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-icon">🪙</div>
                    <h3 class="project-title">Crypto Agent</h3>
                    <p class="project-tech">LLaMA 3.1 + Coingecko API + Streamlit</p>
                    <p>Created a real-time crypto agent powered by Together.AI and live APIs for cryptocurrency analysis and insights.</p>
                </div>
                
                <div class="project-card fade-in">
                    <div class="project-icon">📄</div>
                    <h3 class="project-title">AskPDF</h3>
                    <p class="project-tech">LangChain + Streamlit + Hugging Face</p>
                    <p>Built a GenAI app for analyzing large PDFs (up to 200MB) with natural language queries and intelligent responses.</p>
                </div>
                
                <div class="project-card fade-in">
                    <div class="project-icon">🎯</div>
                    <h3 class="project-title">Fine-tuning Idefics 9B</h3>
                    <p class="project-tech">Multimodal LLM fine-tuning with PEFT</p>
                    <p>Trained a 9B parameter multimodal model for QA and vision-language tasks using parameter-efficient fine-tuning.</p>
                </div>
                
                <div class="project-card fade-in">
                    <div class="project-icon">📊</div>
                    <h3 class="project-title">Credit Risk Analysis</h3>
                    <p class="project-tech">XGBoost, Decision Tree, Random Forest</p>
                    <p>Built comprehensive scoring models on 50k+ credit records for accurate risk prediction and assessment.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Achievements Stats -->
    <section class="section">
        <div class="container">
            <h2 class="section-title fade-in">Achievements & Stats</h2>
            <div class="stats-grid">
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="785">0</div>
                    <div class="stat-label">AIR in IIT JAM 2023</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="4">0</div>
                    <div class="stat-label">Top % Kaggle Expert</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="100">0</div>
                    <div class="stat-label">Coding Problems Solved</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="5">0</div>
                    <div class="stat-label">Industry Projects</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="9.22">0</div>
                    <div class="stat-label">Current CGPA</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number" data-target="3">0</div>
                    <div class="stat-label">Certifications</div>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    
                    // Animate skill bars
                    if (entry.target.classList.contains('skill-category')) {
                        animateSkillBars(entry.target);
                    }
                    
                    // Animate stat counters
                    if (entry.target.classList.contains('stat-card')) {
                        animateStatCounter(entry.target);
                    }
                }
            });
        }, observerOptions);

        // Observe all fade-in elements
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Animate skill bars
        function animateSkillBars(skillCategory) {
            const progressBars = skillCategory.querySelectorAll('.skill-progress');
            progressBars.forEach(bar => {
                setTimeout(() => {
                    const width = bar.getAttribute('data-width');
                    bar.style.width = width + '%';
                }, Math.random() * 500);
            });
        }

        // Animate stat counters
        function animateStatCounter(statCard) {
            const numberElement = statCard.querySelector('.stat-number');
            const target = parseFloat(numberElement.getAttribute('data-target'));
            const duration = 2000;
            const increment = target / (duration / 16);
            let current = 0;

            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    current = target;
                    clearInterval(timer);
                }
                
                if (target === 9.22) {
                    numberElement.textContent = current.toFixed(2);
                } else {
                    numberElement.textContent = Math.floor(current);
                }
            }, 16);
        }

        // Add parallax effect to header
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.header');
            const speed = scrolled * 0.5;
            parallax.style.transform = `translateY(${speed}px)`;
        });

        // Add hover effects to timeline items
        document.querySelectorAll('.timeline-content').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-10px) scale(1.02)';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Add click effects to project cards
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = 'scale(1)';
                }, 150);
            });
        });
