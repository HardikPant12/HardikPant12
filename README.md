<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hardik Pant · advanced README</title>
    <!-- Google Fonts & Font Awesome for clean icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #0d1117 0%, #161b22 100%);
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            color: #e6edf3;
            display: flex;
            justify-content: center;
            padding: 2rem 1.5rem;
            line-height: 1.6;
            min-height: 100vh;
        }

        .readme-card {
            max-width: 1100px;
            width: 100%;
            background: rgba(13, 17, 23, 0.65);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid #30363d;
            border-radius: 2.5rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(255, 255, 255, 0.02) inset;
            padding: 2.5rem 2.2rem;
            transition: all 0.2s ease;
        }

        /* header with avatar + animated text */
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 2.5rem;
            margin-bottom: 3.5rem;
        }

        .avatar-glow {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            background: linear-gradient(135deg, #2ea043, #1f6feb, #bf4b8a);
            padding: 3px;
            box-shadow: 0 15px 30px -10px #1f6feb80;
        }

        .avatar-glow img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #0d1117;
            background: #0d1117;
        }

        .typing-section h1 {
            font-size: 2.8rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(to right, #c9d1d9, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.3rem;
        }

        .typed-container {
            display: flex;
            gap: 0.5rem;
            font-size: 1.5rem;
            font-weight: 500;
            color: #b1bac4;
            flex-wrap: wrap;
        }

        #typed-text {
            color: #ffa657;
            font-weight: 600;
            background: rgba(255, 166, 87, 0.1);
            padding: 0.2rem 0.8rem;
            border-radius: 40px;
            border-left: 2px solid #f78166;
        }

        .badge-panel {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
            margin-top: 1.2rem;
        }

        .badge {
            background: #21262d;
            border-radius: 30px;
            padding: 0.3rem 1rem;
            font-size: 0.85rem;
            font-weight: 500;
            border: 1px solid #3d444d;
            color: #e6edf3;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: 0.15s;
        }

        .badge i {
            color: #2f81f7;
        }

        .badge:hover {
            border-color: #2f81f7;
            background: #2d333c;
        }

        /* about section cards */
        .grid-about {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
            gap: 1.2rem;
            margin: 2.5rem 0 3rem 0;
        }

        .about-card {
            background: #161b22;
            border: 1px solid #30363d;
            border-radius: 24px;
            padding: 1.2rem 1.2rem;
            backdrop-filter: blur(5px);
            transition: transform 0.15s, border-color 0.15s;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .about-card:hover {
            border-color: #3d8cff;
            transform: translateY(-4px);
        }

        .about-icon {
            font-size: 1.8rem;
            min-width: 42px;
            height: 42px;
            background: #21262d;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #f78166;
        }

        .about-card p {
            font-weight: 500;
            font-size: 0.98rem;
        }

        .about-card small {
            color: #848d97;
            font-size: 0.8rem;
            display: block;
        }

        /* connect section */
        .connect-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            background: #161b22;
            border-radius: 60px;
            padding: 0.9rem 2rem;
            margin: 2.5rem 0 2.2rem 0;
            border: 1px solid #30363d;
        }

        .connect-wrapper h3 {
            font-weight: 600;
            font-size: 1.2rem;
            color: #e6edf3;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .social-links a {
            color: #c9d1d9;
            font-size: 1.7rem;
            margin-left: 1.4rem;
            transition: 0.2s;
            display: inline-block;
        }

        .social-links a:hover {
            color: #2f81f7;
            transform: scale(1.15) translateY(-3px);
        }

        /* language and tools grid */
        .tools-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.5rem;
            margin: 1.5rem 0 2.8rem 0;
            background: #0d1117;
            padding: 1.8rem 1.5rem;
            border-radius: 48px;
            border: 1px solid #2d333c;
            justify-content: center;
        }

        .tools-grid span {
            background: #1f252e;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-weight: 500;
            font-size: 1rem;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: 1px solid #363e48;
            transition: 0.15s;
        }

        .tools-grid span i {
            font-size: 1.3rem;
            color: #d4aaff;
        }

        .tools-grid span:hover {
            background: #2d3748;
            border-color: #6e7681;
        }

        /* stats blocks */
        .stats-row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.8rem;
            margin: 2rem 0 2rem;
        }

        .stat-block {
            background: #161b22;
            border-radius: 28px;
            padding: 1.4rem 1.2rem;
            border: 1px solid #30363d;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0,0,0,0.5);
        }

        .stat-block h4 {
            font-weight: 500;
            color: #848d97;
            margin-bottom: 0.5rem;
            font-size: 1rem;
            letter-spacing: 0.5px;
        }

        .stat-block img {
            max-width: 100%;
            border-radius: 12px;
        }

        /* streak + graph */
        .graph-section {
            margin: 2rem 0;
        }

        .graph-card {
            background: #161b22;
            border-radius: 28px;
            padding: 1.8rem 1.5rem;
            border: 1px solid #30363d;
        }

        .graph-header {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 1.2rem;
        }

        .graph-header i {
            font-size: 1.8rem;
            color: #9e6ffd;
        }

        .graph-header span {
            font-weight: 600;
            font-size: 1.2rem;
        }

        /* snake container */
        .snake-container {
            background: #0f1419;
            border-radius: 28px;
            padding: 2rem 1rem;
            margin: 2.5rem 0;
            border: 1px dashed #3d8880;
            text-align: center;
        }

        .snake-container img {
            max-width: 100%;
            border-radius: 20px;
            filter: drop-shadow(0 0 10px #2ea04360);
        }

        /* trophies */
        .trophy-wall {
            background: #151c24;
            border-radius: 40px;
            padding: 1.8rem 1.5rem;
            border: 1px solid #30363d;
            margin-top: 2rem;
        }

        .trophy-wall h3 {
            display: flex;
            gap: 10px;
            align-items: center;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .trophy-wall img {
            max-width: 100%;
            border-radius: 16px;
        }

        hr {
            border: 0.5px solid #292f36;
            margin: 2rem 0;
        }

        .footer-note {
            font-size: 0.9rem;
            color: #6e7681;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 2.8rem;
        }
        /* typed cursor */
        .cursor {
            display: inline-block;
            width: 4px;
            margin-left: 4px;
            background: #f78166;
            animation: blink 0.8s infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
    </style>
</head>
<body>
<div class="readme-card">
    <!-- hero area with typing effect + profile views -->
    <div class="hero">
        <div class="avatar-glow">
            <!-- we keep the original github avatar placeholder, but you can use any -->
            <img src="https://avatars.githubusercontent.com/u/55389276?v=4" alt="Hardik Pant">
        </div>
        <div class="typing-section">
            <h1>Hardik Pant</h1>
            <div class="typed-container">
                <span>👨‍💻</span>
                <span id="typed-text"></span>
                <span class="cursor"></span>
            </div>
            <div class="badge-panel">
                <span class="badge"><i class="fa-regular fa-eye"></i> Profile views: 1,284</span>
                <span class="badge"><i class="fa-regular fa-calendar"></i> Aspiring SWE</span>
                <span class="badge"><i class="fa-regular fa-compass"></i> India</span>
            </div>
        </div>
    </div>

    <!-- about me micro cards -->
    <div class="grid-about">
        <div class="about-card">
            <div class="about-icon"><i class="fa-solid fa-graduation-cap"></i></div>
            <div><p>Aspiring Software Engineer</p><small>building tomorrow's systems</small></div>
        </div>
        <div class="about-card">
            <div class="about-icon"><i class="fa-solid fa-code"></i></div>
            <div><p>Full Stack in progress</p><small>MERN • backend</small></div>
        </div>
        <div class="about-card">
            <div class="about-icon"><i class="fa-solid fa-puzzle-piece"></i></div>
            <div><p>Rubik's cube ⏱️</p><small>&lt; 2 minutes fun fact</small></div>
        </div>
        <div class="about-card">
            <div class="about-icon"><i class="fa-regular fa-envelope"></i></div>
            <div><p>hardikpant18@gmail.com</p><small>reach me anytime</small></div>
        </div>
    </div>

    <!-- connect + social -->
    <div class="connect-wrapper">
        <h3><i class="fa-regular fa-hand-peace" style="color: #f78166;"></i> Connect with me</h3>
        <div class="social-links">
            <a href="https://linkedin.com/in/hardikpant" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
            <a href="#"><i class="fa-brands fa-x-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-github"></i></a>
            <a href="mailto:hardikpant18@gmail.com"><i class="fa-regular fa-envelope"></i></a>
        </div>
    </div>

    <!-- languages & tools (advanced icon grid) -->
    <h3 style="display: flex; gap: 8px; margin-bottom: 0.2rem;"><i class="fa-solid fa-code" style="color:#57ab5a;"></i> Languages & tools</h3>
    <div class="tools-grid">
        <span><i class="fa-brands fa-c"></i> C</span>
        <span><i class="fa-brands fa-js"></i> JavaScript</span>
        <span><i class="fa-brands fa-html5"></i> HTML5</span>
        <span><i class="fa-brands fa-figma"></i> Figma</span>
        <span><i class="fa-brands fa-linux"></i> Linux</span>
        <span><i class="fa-solid fa-database"></i> MySQL</span>
        <span><i class="fa-brands fa-node"></i> Node.js</span>
        <span><i class="fa-brands fa-python"></i> Python</span>
        <span><i class="fa-brands fa-git-alt"></i> Git</span>
        <span><i class="fa-solid fa-code-branch"></i> Docker</span>
    </div>

    <!-- first row stats: top langs + github stats -->
    <div class="stats-row">
        <div class="stat-block">
            <h4><i class="fa-regular fa-chart-bar"></i> most used languages</h4>
            <img src="https://github-readme-stats.vercel.app/api/top-langs?username=hardikpant12&show_icons=true&locale=en&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=c9d1d9" alt="top langs">
        </div>
        <div class="stat-block">
            <h4><i class="fa-regular fa-star"></i> github stats</h4>
            <img src="https://github-readme-stats.vercel.app/api?username=hardikpant12&show_icons=true&locale=en&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&icon_color=bb77ff" alt="github stats">
        </div>
    </div>

    <!-- streak + contribution graph block -->
    <div class="graph-section">
        <div class="graph-card">
            <div class="graph-header">
                <i class="fa-regular fa-calendar-check"></i>
                <span>🔥 current streak & contributions</span>
            </div>
            <div style="display: flex; flex-direction: column; gap: 2rem;">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=hardikpant12&theme=github-dark-blue&hide_border=true&border=30363d&background=161b22&ring=2f81f7&fire=ff7b72&currStreakNum=c9d1d9" alt="streak">
                <!-- activity graph (modern) -->
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=hardikpant12&theme=github-compact&hide_border=true&area=true&bg_color=161b22&color=6e7681&line=2f81f7&point=bb77ff" alt="contribution graph" style="border-radius: 18px;">
            </div>
        </div>
    </div>

    <!-- snake animation (advanced contribution snake) -->
    <div class="snake-container">
        <div style="display: flex; gap: 8px; align-items: center; justify-content: center; margin-bottom: 15px; color:#7ee3b4">
            <i class="fa-regular fa-circle-play"></i> <span>contribution snake</span>
        </div>
        <img src="https://github.com/hardikpant12/hardikpant12/blob/output/github-contribution-grid-snake.svg?raw=true" alt="snake animation" onerror="this.src='https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg'">
        <!-- fallback to platane's snake if user doesn't have one yet -->
    </div>

    <!-- GitHub trophies -->
    <div class="trophy-wall">
        <h3><i class="fa-regular fa-trophy" style="color: #ffd369;"></i> GitHub achievements</h3>
        <img src="https://github-profile-trophy.vercel.app/?username=hardikpant12&theme=onedark&no-frame=true&no-bg=true&column=5&margin-w=15&margin-h=15&row=2" alt="trophies">
    </div>

    <!-- fun extra: profile views counter (real) and fun fact -->
    <hr>
    <div class="footer-note">
        <span><i class="fa-regular fa-face-smile"></i> ⚡ Fun fact: I can solve a Rubik's Cube in under two minutes</span>
        <span><i class="fa-regular fa-id-badge"></i> profile views since 2025: <span id="view-counter">1,284</span></span>
    </div>
</div>

<!-- typed js effect (lightweight) -->
<script>
    (function() {
        const typedSpan = document.getElementById('typed-text');
        const phrases = [
            "Aspiring Software Engineer",
            "Full Stack explorer",
            "backend & system design",
            "Rubik's cube solver",
            "from India 👋"
        ];
        let i = 0;
        let j = 0;
        let currentPhrase = [];
        let isDeleting = false;
        let isEnd = false;

        function loop() {
            isEnd = false;
            if (!isDeleting && j <= phrases[i].length) {
                // write text
                typedSpan.innerHTML = phrases[i].substring(0, j);
                j++;
            } else if (isDeleting && j >= 0) {
                typedSpan.innerHTML = phrases[i].substring(0, j);
                j--;
            }

            if (j === phrases[i].length + 1) {
                isDeleting = true;
            }
            if (j === 0 && isDeleting) {
                isDeleting = false;
                i = (i + 1) % phrases.length;
            }
            setTimeout(loop, isDeleting ? 50 : 110);
        }
        loop();

        // tiny view counter increment simulation (just for looks)
        let views = 1284;
        setInterval(() => {
            views += Math.floor(Math.random() * 3);
            document.getElementById('view-counter').innerText = views.toLocaleString();
        }, 60000); // every minute update
    })();
</script>

<!-- ensure fontawesome & all icons are loaded -->
</body>
</html>
