<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover">
    <meta name="theme-color" content="#060a17">
    <title>Digital Hub Club - DH CLUB</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts (Inter & Outfit) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Outfit:wght@400;600;700;800&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            950: '#060a17',
                            900: '#080d1a',
                            850: '#0c1427',
                            800: '#0f172a',
                            700: '#1e293b',
                        },
                        cyanGlow: {
                            300: '#7dd3fc',
                            400: '#38bdf8',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            accent: '#00e5ff',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Outfit', 'sans-serif'],
                    },
                    boxShadow: {
                        'glass-sm': '0 4px 30px rgba(0, 0, 0, 0.25)',
                        'glass-md': '0 8px 32px 0 rgba(0, 229, 255, 0.12)',
                        'glass-glow': '0 0 30px rgba(56, 189, 248, 0.35)',
                    }
                }
            }
        }
    </script>
    <style>
        /* Deep Navy & Light Blue Glassmorphism Styling */
        * {
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: #060a17;
            background-attachment: fixed;
            color: #f8fafc;
        }

        /* Fixed Blurred Background DH HUB Logo Effect */
        .bg-logo-blur {
            position: fixed;
            inset: 0;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            z-index: -20;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .bg-logo-img {
            width: clamp(320px, 60vw, 750px);
            height: auto;
            opacity: 0.18;
            filter: blur(28px) brightness(1.1);
            transform: scale(1.1);
            animation: pulseSlow 10s ease-in-out infinite alternate;
        }

        @keyframes pulseSlow {
            0% { transform: scale(1.05) rotate(0deg); opacity: 0.15; }
            100% { transform: scale(1.15) rotate(2deg); opacity: 0.22; }
        }

        .glass-panel {
            background: rgba(12, 20, 39, 0.65);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.12);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.035);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.09);
            transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-card:hover {
            background: rgba(255, 255, 255, 0.07);
            border-color: rgba(56, 189, 248, 0.45);
            transform: translateY(-6px);
            box-shadow: 0 15px 35px -10px rgba(56, 189, 248, 0.28);
        }

        .glass-input {
            background: rgba(8, 13, 26, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.14);
            backdrop-filter: blur(10px);
            transition: all 0.25s ease;
        }

        .glass-input:focus {
            outline: none;
            border-color: #38bdf8;
            box-shadow: 0 0 18px rgba(56, 189, 248, 0.35);
            background: rgba(8, 13, 26, 0.85);
        }

        .badge-glass {
            background: rgba(56, 189, 248, 0.12);
            border: 1px solid rgba(56, 189, 248, 0.35);
            color: #7dd3fc;
        }

        /* Float animations */
        @keyframes floatSlow {
            0%, 100% { transform: translateY(0px) scale(1); }
            50% { transform: translateY(-15px) scale(1.05); }
        }
        .animate-float-slow {
            animation: floatSlow 8s ease-in-out infinite;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #060a17;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(56, 189, 248, 0.3);
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(56, 189, 248, 0.6);
        }
    </style>
</head>
<body class="font-sans antialiased min-h-screen flex flex-col justify-between selection:bg-cyanGlow-400 selection:text-navy-950">

    <!-- Fixed Blurred DH HUB Logo Background -->
    <div class="bg-logo-blur">
        <!-- SVG Graphic matching DH HUB Logo for crisp rendering -->
        <svg class="bg-logo-img" viewBox="0 0 800 600" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="400" cy="260" r="210" stroke="#38bdf8" stroke-width="6" stroke-dasharray="14 10" opacity="0.8"/>
            <path d="M 230 250 A 170 170 0 0 1 570 250" stroke="#00e5ff" stroke-width="8" stroke-linecap="round"/>
            <path d="M 250 280 A 170 170 0 0 0 550 280" stroke="#0ea5e9" stroke-width="8" stroke-linecap="round"/>
            <!-- DH Text -->
            <text x="400" y="275" font-family="'Outfit', sans-serif" font-weight="900" font-size="140" fill="#38bdf8" text-anchor="middle">DH</text>
            <text x="400" y="440" font-family="'Outfit', sans-serif" font-weight="800" font-size="52" fill="#ffffff" letter-spacing="12" text-anchor="middle">DIGITAL HUB</text>
        </svg>
    </div>

    <!-- Glowing Background Ambient Glass Orbs -->
    <div class="fixed top-16 left-8 w-80 h-80 bg-cyanGlow-500/20 rounded-full blur-3xl pointer-events-none -z-10 animate-float-slow"></div>
    <div class="fixed bottom-16 right-8 w-96 h-96 bg-cyanGlow-400/15 rounded-full blur-3xl pointer-events-none -z-10 animate-pulse"></div>

    <!-- Header / Sticky Glass Navigation -->
    <header class="sticky top-0 z-50 px-4 lg:px-8 py-4">
        <nav class="max-w-7xl mx-auto glass-panel rounded-2xl px-6 py-3.5 flex items-center justify-between shadow-glass-sm">
            <!-- Brand Logo / Title -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-cyanGlow-600 via-cyanGlow-400 to-cyanGlow-accent p-0.5 shadow-lg shadow-cyanGlow-500/25 group-hover:shadow-cyanGlow-400/50 transition-all">
                    <div class="w-full h-full bg-navy-950 rounded-[10px] flex items-center justify-center">
                        <i data-lucide="cpu" class="w-5 h-5 text-cyanGlow-300"></i>
                    </div>
                </div>
                <div class="flex flex-col">
                    <span class="font-display font-extrabold text-xl tracking-tight bg-gradient-to-r from-white via-slate-100 to-cyanGlow-300 bg-clip-text text-transparent">
                        DH CLUB
                    </span>
                    <span class="text-[10px] text-cyanGlow-300/80 tracking-widest uppercase font-semibold">Digital Hub Club</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <div class="hidden md:flex items-center gap-8 font-medium text-sm text-slate-300">
                <a href="#intro" class="hover:text-cyanGlow-300 transition-colors flex items-center gap-1.5 py-1">
                    <i data-lucide="zap" class="w-4 h-4 text-cyanGlow-400"></i> Intro
                </a>
                <a href="#specialites" class="hover:text-cyanGlow-300 transition-colors flex items-center gap-1.5 py-1">
                    <i data-lucide="bar-chart-2" class="w-4 h-4 text-cyanGlow-400"></i> Spécialités
                </a>
                <a href="#poles" class="hover:text-cyanGlow-300 transition-colors flex items-center gap-1.5 py-1">
                    <i data-lucide="graduation-cap" class="w-4 h-4 text-cyanGlow-400"></i> Nos Pôles
                </a>
                <a href="#contact" class="hover:text-cyanGlow-300 transition-colors flex items-center gap-1.5 py-1">
                    <i data-lucide="mail" class="w-4 h-4 text-cyanGlow-400"></i> Contact
                </a>
            </div>

            <!-- Glowing CTA Button -->
            <div class="hidden sm:block">
                <a href="#contact" class="relative group inline-flex items-center gap-2 px-5 py-2.5 rounded-xl font-semibold text-sm text-navy-950 bg-gradient-to-r from-cyanGlow-300 via-cyanGlow-400 to-cyanGlow-accent hover:brightness-110 transition-all shadow-md shadow-cyanGlow-500/25 active:scale-95">
                    <span>Rejoindre</span>
                    <i data-lucide="arrow-right" class="w-4 h-4 group-hover:translate-x-0.5 transition-transform"></i>
                </a>
            </div>

            <!-- Mobile Menu Toggle Button -->
            <button id="mobileMenuBtn" aria-label="Ouvrir le menu" class="md:hidden text-slate-300 hover:text-white p-2 rounded-lg glass-card">
                <i data-lucide="menu" class="w-6 h-6"></i>
            </button>
        </nav>

        <!-- Mobile Menu Dropdown -->
        <div id="mobileMenu" class="hidden md:hidden max-w-7xl mx-auto mt-2 glass-panel rounded-2xl p-5 shadow-2xl flex flex-col gap-4 text-slate-200">
            <a href="#intro" class="mobile-link flex items-center gap-3 p-2 rounded-lg hover:bg-white/5">
                <i data-lucide="zap" class="w-5 h-5 text-cyanGlow-400"></i> Intro
            </a>
            <a href="#specialites" class="mobile-link flex items-center gap-3 p-2 rounded-lg hover:bg-white/5">
                <i data-lucide="bar-chart-2" class="w-5 h-5 text-cyanGlow-400"></i> Spécialités
            </a>
            <a href="#poles" class="mobile-link flex items-center gap-3 p-2 rounded-lg hover:bg-white/5">
                <i data-lucide="graduation-cap" class="w-5 h-5 text-cyanGlow-400"></i> Nos Pôles
            </a>
            <a href="#contact" class="mobile-link flex items-center gap-3 p-2 rounded-lg hover:bg-white/5">
                <i data-lucide="mail" class="w-5 h-5 text-cyanGlow-400"></i> Contact
            </a>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="max-w-7xl mx-auto px-4 lg:px-8 py-8 w-full flex-grow flex flex-col gap-16">

        <!-- 1. Hero / Introduction Section -->
        <section id="intro" class="relative">
            <div class="glass-panel rounded-3xl p-8 lg:p-14 relative overflow-hidden shadow-2xl border border-white/10">
                <!-- Inner Glow effect -->
                <div class="absolute -top-24 -right-24 w-80 h-80 bg-cyanGlow-400/20 rounded-full blur-3xl pointer-events-none"></div>

                <div class="max-w-3xl flex flex-col items-start gap-6 relative z-10">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full badge-glass text-xs font-semibold uppercase tracking-wider">
                        <i data-lucide="zap" class="w-3.5 h-3.5 text-cyanGlow-300"></i>
                        <span>⚡ INTRODUCTION</span>
                    </div>

                    <h1 class="font-display text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight text-white leading-tight">
                        DH CLUB
                    </h1>

                    <p class="text-slate-300 text-lg sm:text-xl leading-relaxed font-light">
                        Bienvenue au club informatique et digital <strong class="text-white font-medium">Digital Hub Club</strong>. Notre plateforme rassemble les esprits passionnés par l'innovation, la création visuelle et le développement moderne pour construire le monde numérique de demain.
                    </p>

                    <div class="pt-4 flex flex-wrap gap-4 items-center">
                        <a href="#poles" class="px-6 py-3.5 rounded-xl bg-gradient-to-r from-cyanGlow-400 to-cyanGlow-500 text-navy-950 font-semibold hover:brightness-110 transition-all shadow-lg shadow-cyanGlow-500/25 flex items-center gap-2">
                            <span>Découvrir nos pôles</span>
                            <i data-lucide="chevron-right" class="w-4 h-4"></i>
                        </a>
                        <a href="#specialites" class="px-6 py-3.5 rounded-xl glass-card hover:bg-white/10 text-slate-200 font-medium transition-all flex items-center gap-2">
                            <span>Voir le savoir-faire</span>
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- 2. Compétences / Spécialités Section -->
        <section id="specialites" class="scroll-mt-24">
            <div class="flex flex-col items-start gap-2 mb-8">
                <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full badge-glass text-xs font-semibold uppercase tracking-wider">
                    <i data-lucide="bar-chart-2" class="w-3.5 h-3.5 text-cyanGlow-300"></i>
                    <span>📊 Compétences</span>
                </div>
                <h2 class="font-display text-3xl sm:text-4xl font-bold text-white">Notre savoir-faire</h2>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                
                <!-- Card 1: Programmation -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-cyanGlow-500/10 border border-cyanGlow-400/30 flex items-center justify-center text-3xl mb-6 group-hover:scale-110 group-hover:border-cyanGlow-400 transition-all">
                            💻
                        </div>
                        <h3 class="font-display text-xl font-bold text-white mb-2 group-hover:text-cyanGlow-300 transition-colors">Programmation</h3>
                        <p class="text-slate-400 text-sm mb-4 leading-relaxed">
                            Maîtrise des langages et technologies fondamentales du web et du développement logiciel.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-white/10 flex items-center gap-2 font-medium text-cyanGlow-300 text-sm">
                        <span>HTML, CSS, Python, JS</span>
                    </div>
                </div>

                <!-- Card 2: Design Graphique -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-cyanGlow-500/10 border border-cyanGlow-400/30 flex items-center justify-center text-3xl mb-6 group-hover:scale-110 group-hover:border-cyanGlow-400 transition-all">
                            🎨
                        </div>
                        <h3 class="font-display text-xl font-bold text-white mb-2 group-hover:text-cyanGlow-300 transition-colors">Design Graphique</h3>
                        <p class="text-slate-400 text-sm mb-4 leading-relaxed">
                            Création visuelle percutante, logos, affiches et identités visuelles sur-mesure.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-white/10 flex items-center gap-2 font-medium text-cyanGlow-300 text-sm">
                        <span>Photoshop, Illustrator</span>
                    </div>
                </div>

                <!-- Card 3: Graphisme 3D -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-cyanGlow-500/10 border border-cyanGlow-400/30 flex items-center justify-center text-3xl mb-6 group-hover:scale-110 group-hover:border-cyanGlow-400 transition-all">
                            🌐
                        </div>
                        <h3 class="font-display text-xl font-bold text-white mb-2 group-hover:text-cyanGlow-300 transition-colors">3D et Animation</h3>
                        <p class="text-slate-400 text-sm mb-4 leading-relaxed">
                            Modélisation d'espaces 3D, création d'environnements et animations immersives.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-white/10 flex items-center gap-2 font-medium text-cyanGlow-300 text-sm">
                        <span>Blender et Animation</span>
                    </div>
                </div>

                <!-- Card 4: Gestion de projets -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-cyanGlow-500/10 border border-cyanGlow-400/30 flex items-center justify-center text-3xl mb-6 group-hover:scale-110 group-hover:border-cyanGlow-400 transition-all">
                            📊
                        </div>
                        <h3 class="font-display text-xl font-bold text-white mb-2 group-hover:text-cyanGlow-300 transition-colors">Gestion de projets</h3>
                        <p class="text-slate-400 text-sm mb-4 leading-relaxed">
                            Planification stratégique, organisation des tâches et gestion d'équipe collaborative.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-white/10 flex items-center gap-2 font-medium text-cyanGlow-300 text-sm">
                        <span>Agile, SCRUM, Coordination</span>
                    </div>
                </div>

                <!-- Card 5: Histoire de l'art -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between group sm:col-span-2 lg:col-span-1">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-cyanGlow-500/10 border border-cyanGlow-400/30 flex items-center justify-center text-3xl mb-6 group-hover:scale-110 group-hover:border-cyanGlow-400 transition-all">
                            🏛️
                        </div>
                        <h3 class="font-display text-xl font-bold text-white mb-2 group-hover:text-cyanGlow-300 transition-colors">Histoire de l'art</h3>
                        <p class="text-slate-400 text-sm mb-4 leading-relaxed">
                            Étude approfondie des courants artistiques, esthétiques visuelles et culture artistique.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-white/10 flex items-center gap-2 font-medium text-cyanGlow-300 text-sm">
                        <span>Culture Visuelle & Esthétique</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- 3. Dashboard / Nos Pôles Section -->
        <section id="poles" class="scroll-mt-24">
            <div class="flex flex-col items-start gap-2 mb-8">
                <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full badge-glass text-xs font-semibold uppercase tracking-wider">
                    <i data-lucide="graduation-cap" class="w-3.5 h-3.5 text-cyanGlow-300"></i>
                    <span>🎓 NOS PÔLES</span>
                </div>
                <h2 class="font-display text-3xl sm:text-4xl font-bold text-white">Nos différents groupes</h2>
            </div>

            <!-- Pôles Glass Dashboard Cards -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">

                <!-- Pôle 1 -->
                <div class="glass-card rounded-2xl p-8 flex flex-col justify-between relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-28 h-28 bg-cyanGlow-400/10 rounded-bl-full pointer-events-none"></div>
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-bold uppercase tracking-wider text-cyanGlow-400">Pôle Programmation</span>
                            <span class="text-[11px] font-mono px-2 py-0.5 rounded badge-glass">Web / Code</span>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">Développement Web</h3>
                        <p class="text-slate-300 text-sm leading-relaxed mb-6">
                            Création de sites web fluides et rapides, dotés d'interfaces UI/UX uniques.
                        </p>
                    </div>
                    
                    <div>
                        <!-- Progress indicator -->
                        <div class="w-full bg-navy-950/80 rounded-full h-1.5 mb-4 overflow-hidden border border-white/5">
                            <div class="bg-gradient-to-r from-cyanGlow-500 to-cyanGlow-accent h-full w-[85%] rounded-full"></div>
                        </div>
                        <a href="#contact" class="inline-flex items-center gap-2 text-sm font-semibold text-cyanGlow-300 hover:text-white transition-colors group-hover:translate-x-1 transition-transform">
                            <span>Contactez-nous</span>
                            <i data-lucide="arrow-right" class="w-4 h-4"></i>
                        </a>
                    </div>
                </div>

                <!-- Pôle 2 -->
                <div class="glass-card rounded-2xl p-8 flex flex-col justify-between relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-28 h-28 bg-cyanGlow-400/10 rounded-bl-full pointer-events-none"></div>
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-bold uppercase tracking-wider text-cyanGlow-400">Pôle Design</span>
                            <span class="text-[11px] font-mono px-2 py-0.5 rounded badge-glass">Branding / 2D</span>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">Création 2D</h3>
                        <p class="text-slate-300 text-sm leading-relaxed mb-6">
                            Conception graphique de cartes de visite, logos, identités visuelles, etc.
                        </p>
                    </div>

                    <div>
                        <!-- Progress indicator -->
                        <div class="w-full bg-navy-950/80 rounded-full h-1.5 mb-4 overflow-hidden border border-white/5">
                            <div class="bg-gradient-to-r from-cyanGlow-500 to-cyanGlow-accent h-full w-[90%] rounded-full"></div>
                        </div>
                        <a href="#contact" class="inline-flex items-center gap-2 text-sm font-semibold text-cyanGlow-300 hover:text-white transition-colors group-hover:translate-x-1 transition-transform">
                            <span>Contactez-nous</span>
                            <i data-lucide="arrow-right" class="w-4 h-4"></i>
                        </a>
                    </div>
                </div>

                <!-- Pôle 3 -->
                <div class="glass-card rounded-2xl p-8 flex flex-col justify-between relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-28 h-28 bg-cyanGlow-400/10 rounded-bl-full pointer-events-none"></div>
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-bold uppercase tracking-wider text-cyanGlow-400">Pôle Graphisme 3D</span>
                            <span class="text-[11px] font-mono px-2 py-0.5 rounded badge-glass">3D / Blender</span>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">Modélisation Blender</h3>
                        <p class="text-slate-300 text-sm leading-relaxed mb-6">
                            Création de décors et d'architectures (maisons, paysages futuristes, intérieurs design).
                        </p>
                    </div>

                    <div>
                        <!-- Progress indicator -->
                        <div class="w-full bg-navy-950/80 rounded-full h-1.5 mb-4 overflow-hidden border border-white/5">
                            <div class="bg-gradient-to-r from-cyanGlow-500 to-cyanGlow-accent h-full w-[78%] rounded-full"></div>
                        </div>
                        <a href="#contact" class="inline-flex items-center gap-2 text-sm font-semibold text-cyanGlow-300 hover:text-white transition-colors group-hover:translate-x-1 transition-transform">
                            <span>Contactez-nous</span>
                            <i data-lucide="arrow-right" class="w-4 h-4"></i>
                        </a>
                    </div>
                </div>

            </div>
        </section>

        <!-- 4. Contact Section -->
        <section id="contact" class="scroll-mt-24 mb-12">
            <div class="glass-panel rounded-3xl p-8 lg:p-12 relative overflow-hidden shadow-2xl border border-white/10">
                
                <div class="max-w-2xl mx-auto flex flex-col items-center text-center gap-3 mb-10">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full badge-glass text-xs font-semibold uppercase tracking-wider">
                        <i data-lucide="mail" class="w-3.5 h-3.5 text-cyanGlow-300"></i>
                        <span>📬 CONTACT</span>
                    </div>
                    <h2 class="font-display text-3xl sm:text-4xl font-bold text-white">Démarrer un projet avec notre club</h2>
                    <p class="text-slate-400 text-sm sm:text-base max-w-lg">
                        Remplissez le formulaire ci-dessous pour nous envoyer votre message ou demande d'adhésion.
                    </p>
                </div>

                <!-- Glassmorphic Form linked to Formspree -->
                <form id="contactForm" action="https://formspree.io/f/xeewnkek" method="POST" class="max-w-2xl mx-auto flex flex-col gap-5">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
                        <div class="flex flex-col gap-2 text-left">
                            <label for="name" class="text-xs font-semibold uppercase tracking-wider text-slate-300">Nom Complet</label>
                            <input type="text" name="name" id="name" required placeholder="Votre nom" class="glass-input rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 w-full">
                        </div>
                        <div class="flex flex-col gap-2 text-left">
                            <label for="email" class="text-xs font-semibold uppercase tracking-wider text-slate-300">Adresse Email</label>
                            <input type="email" name="email" id="email" required placeholder="nom@exemple.com" class="glass-input rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 w-full">
                        </div>
                    </div>

                    <div class="flex flex-col gap-2 text-left">
                        <label for="subject" class="text-xs font-semibold uppercase tracking-wider text-slate-300">Sujet / Pôle</label>
                        <select name="subject" id="subject" class="glass-input rounded-xl px-4 py-3 text-sm text-white w-full bg-navy-900 cursor-pointer">
                            <option value="Programmation">Pôle Programmation (Développement Web)</option>
                            <option value="Design">Pôle Design (Création 2D)</option>
                            <option value="Graphisme 3D">Pôle Graphisme 3D (Modélisation Blender)</option>
                            <option value="Autre">Autre demande</option>
                        </select>
                    </div>

                    <div class="flex flex-col gap-2 text-left">
                        <label for="message" class="text-xs font-semibold uppercase tracking-wider text-slate-300">Votre Message</label>
                        <textarea name="message" id="message" rows="4" required placeholder="Décrivez votre projet ou votre question..." class="glass-input rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 w-full resize-none"></textarea>
                    </div>

                    <button type="submit" id="submitBtn" class="mt-2 w-full py-3.5 px-6 rounded-xl font-semibold text-navy-950 bg-gradient-to-r from-cyanGlow-300 via-cyanGlow-400 to-cyanGlow-accent hover:brightness-110 transition-all shadow-lg shadow-cyanGlow-500/25 active:scale-[0.99] flex items-center justify-center gap-2">
                        <i data-lucide="send" class="w-4 h-4"></i>
                        <span>Envoyer le message</span>
                    </button>
                </form>

            </div>
        </section>

    </main>

    <!-- Interactive Glass Toast Notification -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="glass-panel bg-navy-900/90 border-cyanGlow-400/40 rounded-2xl p-4 shadow-glass-glow flex items-center gap-3 text-white max-w-md">
            <div class="w-9 h-9 rounded-xl bg-cyanGlow-500/20 flex items-center justify-center text-cyanGlow-300 shrink-0">
                <i data-lucide="check-circle-2" class="w-5 h-5"></i>
            </div>
            <div>
                <h4 class="text-sm font-bold text-white">Message envoyé !</h4>
                <p class="text-xs text-slate-300">Merci de nous avoir contactés. Nous vous répondrons sous peu.</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-white/10 glass-panel py-8 mt-12">
        <div class="max-w-7xl mx-auto px-4 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-400">
            <div class="flex items-center gap-2">
                <span class="font-bold text-white tracking-wide">DH CLUB</span>
                <span>• Digital Hub Club © 2026</span>
            </div>
            <p>Conçu avec une interface زجاجية (Glassmorphic) & fluide en bleu royal/cyan.</p>
        </div>
    </footer>

    <!-- Scripts -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Async Formspree Handling
        const contactForm = document.getElementById('contactForm');
        const toast = document.getElementById('toast');
        const submitBtn = document.getElementById('submitBtn');

        contactForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            
            submitBtn.disabled = true;
            submitBtn.classList.add('opacity-75');

            const formData = new FormData(contactForm);

            try {
                const response = await fetch(contactForm.action, {
                    method: 'POST',
                    body: formData,
                    headers: {
                        'Accept': 'application/json'
                    }
                });

                if (response.ok) {
                    // Show toast
                    toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');
                    toast.classList.add('translate-y-0', 'opacity-100');

                    // Reset form
                    contactForm.reset();

                    // Hide toast after 4 seconds
                    setTimeout(() => {
                        toast.classList.remove('translate-y-0', 'opacity-100');
                        toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
                    }, 4000);
                } else {
                    alert("Erreur lors de l'envoi du message. Veuillez réessayer.");
                }
            } catch (err) {
                alert("Erreur de connexion. Veuillez réessayer.");
            } finally {
                submitBtn.disabled = false;
                submitBtn.classList.remove('opacity-75');
            }
        });
    </script>
</body>
</html>
