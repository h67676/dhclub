<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Hub Club - DH CLUB</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts (Inter & Outfit) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Outfit:wght@500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navyBg: '#050a18',
                        cardBg: 'rgba(10, 24, 48, 0.65)',
                        cardBorder: 'rgba(0, 183, 255, 0.25)',
                        cyanAccent: '#00bdff',
                        cyanGlow: '#00d5ff',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Outfit', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #060a17;
            color: #ffffff;
        }

        .card-custom {
            background-color: #0d1527;
            border: 1px solid rgba(0, 183, 255, 0.2);
            transition: all 0.3s ease;
        }

        .card-custom:hover {
            border-color: rgba(0, 213, 255, 0.6);
            box-shadow: 0 4px 20px rgba(0, 175, 255, 0.15);
            transform: translateY(-4px);
        }

        .input-box {
            background-color: #09101f;
            border: 1px solid rgba(0, 150, 255, 0.25);
            transition: all 0.25s ease;
        }

        .input-box:focus-within {
            border-color: #00d5ff;
            box-shadow: 0 0 10px rgba(0, 213, 255, 0.25);
        }

        .section-title::after {
            content: '';
            display: block;
            width: 48px;
            height: 3px;
            background: #00bdff;
            margin: 10px auto 0;
            border-radius: 2px;
        }
    </style>
</head>
<body class="font-sans antialiased min-h-screen flex flex-col justify-between selection:bg-cyanAccent selection:text-black relative overflow-x-hidden">

    <!-- Header Navigation -->
    <header class="w-full max-w-6xl mx-auto px-6 py-6 flex items-center justify-between relative z-10">
        <!-- Logo -->
        <a href="#" class="font-display font-extrabold text-2xl tracking-tight flex items-center gap-1.5 text-white">
            <span>DH</span>
            <span class="text-cyanAccent">CLUB</span>
        </a>

        <!-- Menu -->
        <nav class="hidden sm:flex items-center gap-8 font-medium text-sm text-slate-300">
            <a href="#intro" class="text-cyanAccent border-b-2 border-cyanAccent pb-1">Intro</a>
            <a href="#specialites" class="hover:text-cyanAccent transition-colors">Spécialités</a>
            <a href="#projets" class="hover:text-cyanAccent transition-colors">Projets</a>
            <a href="#contact" class="hover:text-cyanAccent transition-colors">Contact</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="w-full max-w-5xl mx-auto px-6 pt-12 pb-20 relative z-10 flex flex-col gap-24 text-center">

        <!-- Hero Section -->
        <section id="intro" class="flex flex-col items-center pt-8">
            <h1 class="font-display text-5xl sm:text-7xl font-extrabold tracking-tight text-white mb-4">
                Digital <span class="text-cyanAccent">Hub</span>
            </h1>
            <p class="text-slate-300 text-lg sm:text-xl font-normal mb-8 max-w-lg">
                Créativité, technologie et innovation.
            </p>
            <a href="#specialites" class="px-8 py-3 rounded-full bg-cyanAccent hover:bg-cyanGlow text-black font-semibold text-sm transition-all shadow-lg shadow-cyanAccent/30 hover:shadow-cyanAccent/50 active:scale-95 flex items-center gap-2">
                <span>Découvrir</span>
                <i data-lucide="arrow-down" class="w-4 h-4"></i>
            </a>
        </section>

        <!-- Nos Spécialités -->
        <section id="specialites" class="scroll-mt-20">
            <h2 class="font-display text-3xl font-bold text-white mb-10 section-title">
                Nos spécialités
            </h2>

            <!-- Grid 4 Top + 1 Bottom Centered -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5 mb-5">
                <!-- Programmation -->
                <div class="card-custom rounded-2xl p-6 flex flex-col items-center text-center">
                    <i data-lucide="code" class="w-10 h-10 text-cyanAccent mb-4"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Programmation</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        HTML, CSS, JavaScript et création de sites web.
                    </p>
                </div>

                <!-- Design Graphique -->
                <div class="card-custom rounded-2xl p-6 flex flex-col items-center text-center">
                    <i data-lucide="palette" class="w-10 h-10 text-cyanAccent mb-4"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Design Graphique</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Création de logos, affiches et identités visuelles.
                    </p>
                </div>

                <!-- 3D et Animation -->
                <div class="card-custom rounded-2xl p-6 flex flex-col items-center text-center">
                    <i data-lucide="box" class="w-10 h-10 text-cyanAccent mb-4"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">3D et Animation</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Modélisation 3D et création avec Blender.
                    </p>
                </div>

                <!-- Gestion de projets -->
                <div class="card-custom rounded-2xl p-6 flex flex-col items-center text-center">
                    <i data-lucide="clipboard-check" class="w-10 h-10 text-cyanAccent mb-4"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Gestion de projets</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Planification, suivi et organisation des projets.
                    </p>
                </div>
            </div>

            <!-- Centered 5th Card -->
            <div class="flex justify-center">
                <div class="card-custom rounded-2xl p-6 flex flex-col items-center text-center w-full sm:w-1/2 lg:w-1/3">
                    <i data-lucide="landmark" class="w-10 h-10 text-cyanAccent mb-4"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Histoire de l'art</h3>
                    <p class="text-slate-400 text-xs leading-relaxed">
                        Culture, patrimoine et analyse artistique.
                    </p>
                </div>
            </div>
        </section>

        <!-- Nos Projets -->
        <section id="projets" class="scroll-mt-20">
            <h2 class="font-display text-3xl font-bold text-white mb-10 section-title">
                Nos projets
            </h2>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Développement Web -->
                <div class="card-custom rounded-2xl p-8 flex flex-col items-center text-center">
                    <i data-lucide="globe" class="w-12 h-12 text-cyanAccent mb-5"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Développement Web</h3>
                    <p class="text-slate-400 text-xs">
                        Sites modernes et performants.
                    </p>
                </div>

                <!-- Création 2D -->
                <div class="card-custom rounded-2xl p-8 flex flex-col items-center text-center">
                    <i data-lucide="image" class="w-12 h-12 text-cyanAccent mb-5"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Création 2D</h3>
                    <p class="text-slate-400 text-xs">
                        Logos & affiches.
                    </p>
                </div>

                <!-- Modélisation 3D -->
                <div class="card-custom rounded-2xl p-8 flex flex-col items-center text-center">
                    <i data-lucide="box" class="w-12 h-12 text-cyanAccent mb-5"></i>
                    <h3 class="font-display text-lg font-bold text-white mb-2">Modélisation 3D</h3>
                    <p class="text-slate-400 text-xs">
                        Décors & environnements.
                    </p>
                </div>
            </div>
        </section>

        <!-- Contactez-nous -->
        <section id="contact" class="scroll-mt-20 max-w-3xl mx-auto w-full">
            <h2 class="font-display text-3xl font-bold text-white mb-10 section-title">
                Contactez-nous
            </h2>

            <div class="card-custom rounded-2xl p-6 sm:p-8 text-left">
                <form id="contactForm" action="https://formspree.io/f/xeewnkek" method="POST" class="flex flex-col gap-4">
                    
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <!-- Name Input -->
                        <div class="input-box rounded-xl px-4 py-3 flex items-center gap-3">
                            <i data-lucide="user" class="w-5 h-5 text-slate-400 shrink-0"></i>
                            <input type="text" name="name" required placeholder="Votre nom" class="bg-transparent border-none outline-none w-full text-sm text-white placeholder-slate-500">
                        </div>

                        <!-- Email Input -->
                        <div class="input-box rounded-xl px-4 py-3 flex items-center gap-3">
                            <i data-lucide="mail" class="w-5 h-5 text-slate-400 shrink-0"></i>
                            <input type="email" name="email" required placeholder="Votre email" class="bg-transparent border-none outline-none w-full text-sm text-white placeholder-slate-500">
                        </div>
                    </div>

                    <!-- Message Area -->
                    <div class="input-box rounded-xl px-4 py-3 flex items-start gap-3">
                        <i data-lucide="message-square" class="w-5 h-5 text-slate-400 shrink-0 mt-0.5"></i>
                        <textarea name="message" rows="4" required placeholder="Votre message" class="bg-transparent border-none outline-none w-full text-sm text-white placeholder-slate-500 resize-none"></textarea>
                    </div>

                    <!-- Submit Button -->
                    <button type="submit" id="submitBtn" class="mt-2 w-full py-3.5 rounded-xl bg-cyanAccent hover:bg-cyanGlow text-black font-semibold text-sm transition-all shadow-md shadow-cyanAccent/30 active:scale-[0.99] flex items-center justify-center gap-2">
                        <i data-lucide="send" class="w-4 h-4"></i>
                        <span>Envoyer le message</span>
                    </button>
                </form>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="w-full max-w-6xl mx-auto px-6 py-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-400 border-t border-slate-800/60 relative z-10">
        <p>© 2026 Digital Hub Club (DH CLUB). Tous droits réservés.</p>
        
        <!-- Social Icons -->
        <div class="flex items-center gap-5 text-slate-300">
            <a href="#" aria-label="YouTube" class="hover:text-cyanAccent transition-colors">
                <i data-lucide="youtube" class="w-5 h-5"></i>
            </a>
            <a href="#" aria-label="Discord" class="hover:text-cyanAccent transition-colors">
                <i data-lucide="disc" class="w-5 h-5"></i>
            </a>
            <a href="#" aria-label="Instagram" class="hover:text-cyanAccent transition-colors">
                <i data-lucide="instagram" class="w-5 h-5"></i>
            </a>
            <a href="#" aria-label="LinkedIn" class="hover:text-cyanAccent transition-colors">
                <i data-lucide="linkedin" class="w-5 h-5"></i>
            </a>
        </div>
    </footer>

    <!-- Lucide Init & Form Script -->
    <script>
        lucide.createIcons();

        const contactForm = document.getElementById('contactForm');
        const submitBtn = document.getElementById('submitBtn');

        contactForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            const originalText = submitBtn.innerHTML;
            submitBtn.disabled = true;
            submitBtn.innerHTML = `<span>Envoi en cours...</span>`;

            try {
                const response = await fetch(contactForm.action, {
                    method: 'POST',
                    body: new FormData(contactForm),
                    headers: { 'Accept': 'application/json' }
                });

                if (response.ok) {
                    contactForm.reset();
                    submitBtn.innerHTML = `<i data-lucide="check" class="w-4 h-4"></i> Message envoyé !`;
                    lucide.createIcons();
                    setTimeout(() => {
                        submitBtn.disabled = false;
                        submitBtn.innerHTML = originalText;
                        lucide.createIcons();
                    }, 4000);
                } else {
                    submitBtn.disabled = false;
                    submitBtn.innerHTML = originalText;
                    lucide.createIcons();
                }
            } catch (err) {
                submitBtn.disabled = false;
                submitBtn.innerHTML = originalText;
                lucide.createIcons();
            }
        });
    </script>
</body>
</html>
