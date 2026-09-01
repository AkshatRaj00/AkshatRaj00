<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Akshat Raj · AI Engineer</title>
    <style>
        /* ── reset & base ── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0b0f1a;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            line-height: 1.6;
            color: #e8edf5;
        }

        .readme {
            max-width: 820px;
            width: 100%;
            background: #0f1629;
            background-image: radial-gradient(ellipse at 20% 50%, rgba(14, 165, 233, 0.04) 0%, transparent 70%),
                radial-gradient(ellipse at 80% 20%, rgba(139, 92, 246, 0.04) 0%, transparent 60%);
            border-radius: 32px;
            padding: 2.5rem 2.2rem;
            box-shadow: 0 25px 60px -15px rgba(0, 0, 0, 0.8), inset 0 1px 0 rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.03);
            position: relative;
            overflow: hidden;
        }

        .readme::before {
            content: '';
            position: absolute;
            inset: 0;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.015'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            pointer-events: none;
        }

        /* ── typography ── */
        h1,
        h2,
        h3,
        h4 {
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .glow-text {
            background: linear-gradient(135deg, #38bdf8 0%, #818cf8 50%, #c084fc 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .badge {
            display: inline-block;
            padding: 0.2rem 0.9rem;
            border-radius: 100px;
            font-size: 0.7rem;
            font-weight: 600;
            letter-spacing: 0.03em;
            text-transform: uppercase;
            background: rgba(56, 189, 248, 0.10);
            color: #7dd3fc;
            border: 1px solid rgba(56, 189, 248, 0.12);
        }

        /* ── header ── */
        .header {
            text-align: center;
            padding-bottom: 2rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 2.2rem;
            position: relative;
        }

        .header h1 {
            font-size: 4rem;
            font-weight: 700;
            letter-spacing: -0.04em;
            background: linear-gradient(135deg, #f0f9ff 0%, #7dd3fc 50%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.2rem;
            line-height: 1.1;
        }

        .header .sub {
            font-size: 1rem;
            color: #94a3b8;
            letter-spacing: 0.2em;
            text-transform: uppercase;
            font-weight: 400;
            margin-top: 0.2rem;
        }

        .header .sub span {
            color: #38bdf8;
            font-weight: 500;
        }

        .header .tagline {
            margin-top: 1rem;
            font-size: 1.05rem;
            color: #cbd5e1;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .header .tagline strong {
            color: #f0f9ff;
            font-weight: 600;
        }

        .header-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.6rem;
            margin-top: 1.5rem;
        }

        .header-links a {
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            padding: 0.55rem 1.4rem;
            border-radius: 100px;
            font-size: 0.8rem;
            font-weight: 500;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.2s ease;
            color: #e2e8f0;
        }

        .header-links a:hover {
            background: rgba(56, 189, 248, 0.10);
            border-color: rgba(56, 189, 248, 0.20);
            transform: translateY(-1px);
            box-shadow: 0 8px 25px -8px rgba(56, 189, 248, 0.08);
        }

        .header-links a .icon {
            font-size: 1.1rem;
        }

        /* ── status bar ── */
        .status-bar {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
            padding: 0.8rem 1.2rem;
            background: rgba(255, 255, 255, 0.02);
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 2.2rem;
            font-size: 0.8rem;
            color: #94a3b8;
        }

        .status-bar .dot {
            display: inline-block;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            margin-right: 0.4rem;
            background: #22c55e;
            box-shadow: 0 0 12px rgba(34, 197, 94, 0.3);
            animation: pulse-dot 2s ease-in-out infinite;
        }

        @keyframes pulse-dot {
            0%,
            100% {
                opacity: 1;
                transform: scale(1);
            }
            50% {
                opacity: 0.5;
                transform: scale(0.9);
            }
        }

        .status-bar span {
            color: #e2e8f0;
        }

        /* ── grid sections ── */
        .section-title {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            font-size: 1.1rem;
            font-weight: 600;
            color: #f0f9ff;
            margin-bottom: 1.2rem;
            letter-spacing: -0.01em;
        }

        .section-title .line {
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, rgba(56, 189, 248, 0.20), transparent);
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-bottom: 2.2rem;
        }

        .card {
            background: rgba(255, 255, 255, 0.02);
            border-radius: 20px;
            padding: 1.5rem 1.5rem 1.8rem;
            border: 1px solid rgba(255, 255, 255, 0.04);
            transition: all 0.2s ease;
        }

        .card:hover {
            border-color: rgba(56, 189, 248, 0.08);
            background: rgba(255, 255, 255, 0.025);
        }

        .card h3 {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.12em;
            color: #64748b;
            margin-bottom: 0.8rem;
            font-weight: 600;
        }

        .card .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .card .tech-icons img {
            height: 32px;
            width: auto;
            filter: brightness(0.9) saturate(0.8);
            transition: filter 0.2s;
        }

        .card .tech-icons img:hover {
            filter: brightness(1.1) saturate(1.1);
        }

        .card p {
            font-size: 0.92rem;
            color: #cbd5e1;
            line-height: 1.7;
        }

        .card p strong {
            color: #f0f9ff;
            font-weight: 500;
        }

        /* ── philosophy ── */
        .philosophy {
            text-align: center;
            padding: 1.8rem 1.5rem;
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.04), rgba(139, 92, 246, 0.04));
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 2.2rem;
        }

        .philosophy blockquote {
            font-size: 1.25rem;
            font-weight: 400;
            color: #e2e8f0;
            letter-spacing: -0.01em;
            line-height: 1.6;
        }

        .philosophy blockquote em {
            font-style: normal;
            color: #7dd3fc;
            font-weight: 500;
        }

        .philosophy .attribution {
            margin-top: 0.4rem;
            font-size: 0.8rem;
            color: #64748b;
            letter-spacing: 0.05em;
        }

        /* ── builds ── */
        .builds {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin-bottom: 2.2rem;
        }

        .build-item {
            background: rgba(255, 255, 255, 0.015);
            border-radius: 16px;
            padding: 1.2rem 1.4rem;
            border: 1px solid rgba(255, 255, 255, 0.04);
            transition: all 0.2s ease;
        }

        .build-item:hover {
            border-color: rgba(56, 189, 248, 0.08);
            background: rgba(255, 255, 255, 0.025);
        }

        .build-item h4 {
            font-size: 1rem;
            font-weight: 600;
            color: #f0f9ff;
            margin-bottom: 0.15rem;
        }

        .build-item .desc {
            font-size: 0.82rem;
            color: #94a3b8;
            margin-bottom: 0.6rem;
        }

        .build-item .link {
            font-size: 0.75rem;
            font-weight: 500;
            color: #38bdf8;
            display: inline-flex;
            align-items: center;
            gap: 0.3rem;
            transition: color 0.2s;
        }

        .build-item .link:hover {
            color: #7dd3fc;
        }

        /* ── terminal ── */
        .terminal {
            background: #0a0e1a;
            border-radius: 16px;
            padding: 1.2rem 1.5rem;
            font-family: 'JetBrains Mono', 'Fira Code', monospace;
            font-size: 0.82rem;
            border: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 2.2rem;
            position: relative;
            overflow: hidden;
        }

        .terminal .line {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: #94a3b8;
            padding: 0.1rem 0;
        }

        .terminal .line .prompt {
            color: #22c55e;
            font-weight: 500;
        }

        .terminal .line .cmd {
            color: #e2e8f0;
        }

        .terminal .line .output {
            color: #7dd3fc;
        }

        .terminal .cursor {
            display: inline-block;
            width: 8px;
            height: 16px;
            background: #22c55e;
            animation: blink 1s step-end infinite;
            vertical-align: text-bottom;
            margin-left: 2px;
        }

        @keyframes blink {
            0%,
            100% {
                opacity: 1;
            }
            50% {
                opacity: 0;
            }
        }

        /* ── stats ── */
        .stats {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            padding: 1.2rem 0;
            border-top: 1px solid rgba(255, 255, 255, 0.04);
            border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 2.2rem;
        }

        .stats .stat {
            text-align: center;
        }

        .stats .stat .num {
            font-size: 1.6rem;
            font-weight: 700;
            color: #f0f9ff;
            letter-spacing: -0.02em;
        }

        .stats .stat .label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.08em;
            color: #64748b;
        }

        /* ── connect ── */
        .connect {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.5rem;
            margin-top: 1.2rem;
        }

        .connect a {
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            padding: 0.4rem 1rem;
            border-radius: 100px;
            font-size: 0.75rem;
            font-weight: 500;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            color: #cbd5e1;
            transition: all 0.2s ease;
        }

        .connect a:hover {
            background: rgba(56, 189, 248, 0.06);
            border-color: rgba(56, 189, 248, 0.12);
            color: #f0f9ff;
        }

        /* ── footer ── */
        .footer {
            text-align: center;
            font-size: 0.75rem;
            color: #475569;
            margin-top: 1.8rem;
            padding-top: 1.2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
            letter-spacing: 0.02em;
        }

        .footer span {
            color: #64748b;
        }

        /* ── responsive ── */
        @media (max-width: 640px) {
            .readme {
                padding: 1.5rem 1rem;
                border-radius: 20px;
            }
            .header h1 {
                font-size: 2.6rem;
            }
            .grid-2 {
                grid-template-columns: 1fr;
            }
            .builds {
                grid-template-columns: 1fr;
            }
            .stats {
                gap: 1.2rem;
            }
            .header-links a {
                padding: 0.4rem 1rem;
                font-size: 0.7rem;
            }
            .status-bar {
                font-size: 0.7rem;
                gap: 0.8rem;
                padding: 0.6rem 0.8rem;
            }
            .philosophy blockquote {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .header h1 {
                font-size: 2rem;
            }
            .header .sub {
                font-size: 0.7rem;
                letter-spacing: 0.1em;
            }
            .card {
                padding: 1rem;
            }
            .terminal {
                font-size: 0.7rem;
                padding: 0.8rem 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="readme">

        <!-- ─── HEADER ─── -->
        <div class="header">
            <h1>AKSHAT RAJ</h1>
            <div class="sub">AI <span>·</span> Automation <span>·</span> Cloud</div>
            <div class="tagline">
                <strong>Founder @ OnePersonAI</strong> &nbsp;·&nbsp; Building autonomous digital systems
                <br />from first principles to production.
            </div>
            <div class="header-links">
                <a href="https://onepersonai.in"><span class="icon">✦</span> OnePersonAI</a>
                <a href="https://akshat-raj-portfolio-lfy7.vercel.app/"><span class="icon">◈</span> Portfolio</a>
                <a href="mailto:akshatgyan2004@gmail.com"><span class="icon">✉</span> Contact</a>
            </div>
        </div>

        <!-- ─── STATUS BAR ─── -->
        <div class="status-bar">
            <span><span class="dot"></span> System · <span>Online</span></span>
            <span>⚡ Mode · <span>Building</span></span>
            <span>📡 Uptime · <span>99.9%</span></span>
            <span>🧩 Stack · <span>Rust · Go · Python</span></span>
        </div>

        <!-- ─── RUNTIME + INTELLIGENCE ─── -->
        <div class="grid-2">
            <div class="card">
                <h3>⚙️ Runtime &amp; Interface</h3>
                <div class="tech-icons">
                    <img src="https://skillicons.dev/icons?i=rust,go,py&theme=dark" alt="Rust Go Python" />
                    <img src="https://skillicons.dev/icons?i=react,nextjs,flutter&theme=dark" alt="React Next.js Flutter" />
                </div>
                <p style="margin-top:0.8rem;">
                    Systems that <strong>perform</strong> — low-latency cores, clean UIs,
                    and mobile experiences that ship.
                </p>
            </div>
            <div class="card">
                <h3>🧠 Intelligence &amp; Infra</h3>
                <div class="tech-icons">
                    <img src="https://skillicons.dev/icons?i=tensorflow,pytorch,py&theme=dark" alt="TensorFlow PyTorch" />
                    <img src="https://skillicons.dev/icons?i=aws,docker,linux&theme=dark" alt="AWS Docker Linux" />
                </div>
                <p style="margin-top:0.8rem;">
                    LLM agents, automation pipelines, and cloud-native infrastructure
                    built to <strong>scale</strong>.
                </p>
            </div>
        </div>

        <!-- ─── PHILOSOPHY ─── -->
        <div class="philosophy">
            <blockquote>
                “Build less noise. <em>Ship more signal.</em>”
            </blockquote>
            <div class="attribution">— full‑stack engineering · AI · automation · security</div>
        </div>

        <!-- ─── BUILD IN MOTION ─── -->
        <div class="section-title">
            <span>🎬 Build in Motion</span>
            <span class="line"></span>
        </div>
        <div class="card" style="margin-bottom:2.2rem; padding:1.5rem 1.8rem;">
            <div style="display:grid; grid-template-columns: 1fr 1fr; gap:1.2rem;">
                <div>
                    <p style="font-size:0.9rem;">
                        <strong>🤖 Autonomous AI workflows</strong><br />
                        <span style="color:#94a3b8;">Agents that plan, call tools, and recover from failure.</span>
                    </p>
                    <p style="font-size:0.9rem; margin-top:0.6rem;">
                        <strong>⚙️ High‑performance backends</strong><br />
                        <span style="color:#94a3b8;">Rust + Go services built for throughput, not demos.</span>
                    </p>
                    <p style="font-size:0.9rem; margin-top:0.6rem;">
                        <strong>🎨 3D interactive interfaces</strong><br />
                        <span style="color:#94a3b8;">Three.js experiences that feel alive.</span>
                    </p>
                </div>
                <div>
                    <p style="font-size:0.9rem;">
                        <strong>🔐 Security engineering</strong><br />
                        <span style="color:#94a3b8;">Scanners and bots that catch real threats in real time.</span>
                    </p>
                    <p style="font-size:0.9rem; margin-top:0.6rem;">
                        <strong>☁️ Cloud‑native infrastructure</strong><br />
                        <span style="color:#94a3b8;">Dockerized, CI/CD‑driven, production‑ready.</span>
                    </p>
                    <p style="font-size:0.9rem; margin-top:0.6rem;">
                        <strong>📱 Production mobile apps</strong><br />
                        <span style="color:#94a3b8;">Flutter builds shipped to real users.</span>
                    </p>
                </div>
            </div>
            <div style="margin-top:1rem; font-size:0.8rem; color:#64748b; text-align:center; border-top:1px solid rgba(255,255,255,0.04); padding-top:0.8rem;">
                One person, full stack, end to end — from first line to deployed release.
            </div>
        </div>

        <!-- ─── TECH UNIVERSE ─── -->
        <div class="section-title">
            <span>🧩 Technology Universe</span>
            <span class="line"></span>
        </div>
        <div style="display:flex; flex-wrap:wrap; gap:0.8rem 1.2rem; justify-content:center; margin-bottom:2.2rem;">
            <img src="https://skillicons.dev/icons?i=rust,go,py,cpp,c&theme=dark" alt="Languages" />
            <img src="https://skillicons.dev/icons?i=ts,js,react,nextjs,nodejs,express&theme=dark" alt="Web" />
            <img src="https://skillicons.dev/icons?i=threejs,flutter,dart,php,laravel&theme=dark" alt="UI & Mobile" />
            <img src="https://skillicons.dev/icons?i=aws,docker,linux,kali,git,githubactions&theme=dark" alt="Infra" />
            <img src="https://skillicons.dev/icons?i=firebase,supabase,postgres&theme=dark" alt="Data" />
        </div>

        <!-- ─── TERMINAL ─── -->
        <div class="terminal">
            <div class="line"><span class="prompt">➜</span> <span class="cmd">~ whoami</span></div>
            <div class="line"><span class="output">akshat · founder @ OnePersonAI</span></div>
            <div class="line" style="margin-top:0.3rem;"><span class="prompt">➜</span> <span class="cmd">~ ls projects/</span></div>
            <div class="line"><span class="output">onepersonai &nbsp; kbfixer &nbsp; onemusic &nbsp; jeev-sahay</span></div>
            <div class="line" style="margin-top:0.3rem;"><span class="prompt">➜</span> <span class="cmd">~ status --check</span></div>
            <div class="line"><span class="output">[OK] mode: BUILDING · uptime: 99.9%</span><span class="cursor"></span></div>
        </div>

        <!-- ─── FEATURED BUILDS ─── -->
        <div class="section-title">
            <span>🚀 Featured Builds</span>
            <span class="line"></span>
        </div>
        <div class="builds">
            <div class="build-item">
                <h4>🧠 OnePersonAI</h4>
                <div class="desc">AI + automation ecosystem · intelligent products &amp; workflows</div>
                <a href="https://onepersonai.in" class="link">Open Product →</a>
            </div>
            <div class="build-item">
                <h4>📄 KBFixer</h4>
                <div class="desc">Document processing engine · fast PDF &amp; presentation workflows</div>
                <a href="https://kbfixer.onepersonai.in" class="link">Open Product →</a>
            </div>
            <div class="build-item">
                <h4>🎵 OneMusic</h4>
                <div class="desc">Flutter music platform · clean Android listening experience</div>
                <a href="https://github.com/AkshatRaj00" class="link">View Source →</a>
            </div>
            <div class="build-item">
                <h4>🚑 Jeev Sahay</h4>
                <div class="desc">Emergency assistance · digital workflows for support &amp; accessibility</div>
                <a href="https://jeevsahay.in" class="link">Open Product →</a>
            </div>
        </div>

        <!-- ─── STATS ─── -->
        <div class="stats">
            <div class="stat"><div class="num">∞</div><div class="label">Always Building</div></div>
            <div class="stat"><div class="num">99.9%</div><div class="label">Uptime</div></div>
            <div class="stat"><div class="num">⚡</div><div class="label">Ship Fast</div></div>
            <div class="stat"><div class="num">🔐</div><div class="label">Secure by Design</div></div>
        </div>

        <!-- ─── CONNECT ─── -->
        <div class="section-title" style="margin-bottom:0.8rem;">
            <span>📡 Connect</span>
            <span class="line"></span>
        </div>
        <div class="connect">
            <a href="https://github.com/AkshatRaj00">GitHub</a>
            <a href="https://akshat-raj-portfolio-lfy7.vercel.app/">Portfolio</a>
            <a href="mailto:akshatgyan2004@gmail.com">Email</a>
            <a href="https://x.com/AkshatRaj00_">X</a>
            <a href="https://dev.to/akshatraj00">DEV.to</a>
            <a href="https://nest.owasp.org/members/AkshatRaj00">OWASP</a>
            <a href="https://www.kaggle.com/akshatraj12">Kaggle</a>
        </div>

        <!-- ─── FOOTER ─── -->
        <div class="footer">
            <span>✦</span> Engineering intelligent systems, one idea at a time. <span>✦</span>
        </div>

    </div>
</body>
</html>
