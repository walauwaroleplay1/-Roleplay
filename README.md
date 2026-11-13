# -Roleplay
සාදරයෙන් පිලිගන්නවා වලව්ව Roleplay
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>වලව්ව Roleplay | Sri Lanka's Premier FiveM RP</title>
    
    <!-- Google Fonts: Sinhala (Noto Sans Sinhala) & English (Cinzel for Royal feel, Plus Jakarta Sans for clean UI) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Noto+Sans+Sinhala:wght@500;700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Custom Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        royal: {
                            dark: '#09090b',
                            card: '#121216',
                            border: '#27272a',
                            gold: '#eab308',
                            goldLight: '#fde047',
                            goldDark: '#a16207',
                            crimson: '#991b1b',
                            crimsonBright: '#dc2626'
                        }
                    },
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', '"Noto Sans Sinhala"', 'sans-serif'],
                        royal: ['"Cinzel"', '"Noto Sans Sinhala"', 'serif'],
                        sinhala: ['"Noto Sans Sinhala"', 'sans-serif']
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #09090b;
        }
        ::-webkit-scrollbar-thumb {
            background: #a16207;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #eab308;
        }

        /* Hero Background Pattern & Gradient */
        .hero-bg {
            background-color: #09090b;
            background-image: 
                radial-gradient(circle at 50% 0%, rgba(153, 27, 27, 0.25) 0%, transparent 60%),
                radial-gradient(circle at 85% 30%, rgba(234, 179, 8, 0.12) 0%, transparent 50%),
                linear-gradient(to bottom, rgba(9, 9, 11, 0.7), #09090b);
        }

        /* Subtle Gold Glow */
        .gold-glow {
            box-shadow: 0 0 25px rgba(234, 179, 8, 0.15);
        }
        .gold-glow-hover:hover {
            box-shadow: 0 0 30px rgba(234, 179, 8, 0.3);
        }

        /* Traditional Sri Lankan Motif Divider */
        .motif-divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, #991b1b, #eab308, #991b1b, transparent);
        }
    </style>
</head>
<body class="bg-royal-dark text-gray-200 font-sans antialiased selection:bg-royal-gold selection:text-black">

    <!-- Toast Notification for IP Copy (Replaces alert) -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-24 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="bg-royal-card border border-royal-gold text-white px-5 py-3.5 rounded-xl shadow-2xl flex items-center gap-3 gold-glow">
            <div class="w-8 h-8 rounded-full bg-royal-gold/20 flex items-center justify-center text-royal-gold">
                <i class="fa-solid fa-check"></i>
            </div>
            <div>
                <p class="font-semibold text-sm text-royal-gold">Server IP Copied!</p>
                <p class="text-xs text-gray-300">Open FiveM, press F8 & paste to join.</p>
            </div>
        </div>
    </div>

    <!-- 1. STICKY NAVIGATION BAR -->
    <nav class="sticky top-0 z-40 bg-royal-dark/85 backdrop-blur-md border-b border-royal-border/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Brand Logo -->
                <a href="#home" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-royal-crimson to-royal-goldDark p-0.5 shadow-lg group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-royal-dark rounded-[10px] flex items-center justify-center">
                            <i class="fa-solid fa-crown text-royal-gold text-lg"></i>
                        </div>
                    </div>
                    <div class="flex flex-col">
                        <span class="font-sinhala font-extrabold text-xl tracking-wide text-white group-hover:text-royal-gold transition-colors">
                            වලව්ව <span class="text-royal-gold font-royal">RP</span>
                        </span>
                        <span class="text-[10px] uppercase tracking-widest text-gray-400">Sri Lanka FiveM</span>
                    </div>
                </a>

                <!-- Desktop Navigation Links -->
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="text-sm font-medium text-gray-300 hover:text-royal-gold transition-colors">Home</a>
                    <a href="#features" class="text-sm font-medium text-gray-300 hover:text-royal-gold transition-colors">Features</a>
                    <a href="#rules" class="text-sm font-medium text-gray-300 hover:text-royal-gold transition-colors">Rules</a>
                    <a href="#join" class="text-sm font-medium text-gray-300 hover:text-royal-gold transition-colors">Join Us</a>
                    <a href="#staff" class="text-sm font-medium text-gray-300 hover:text-royal-gold transition-colors">Community</a>
                </div>

                <!-- Desktop Discord CTA -->
                <div class="hidden md:flex items-center">
                    <a href="https://discord.gg/your-invite-link" target="_blank" rel="noopener noreferrer" 
                       class="inline-flex items-center gap-2 bg-gradient-to-r from-royal-crimson to-red-800 hover:from-red-700 hover:to-royal-crimson text-white text-sm font-semibold px-5 py-2.5 rounded-xl border border-red-500/30 shadow-lg transition-all duration-200 hover:scale-105">
                        <i class="fa-brands fa-discord text-lg"></i>
                        <span>Discord</span>
                    </a>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" aria-label="Toggle Menu" class="p-2.5 rounded-xl bg-royal-card border border-royal-border text-gray-300 hover:text-royal-gold focus:outline-none">
                        <i class="fa-solid fa-bars text-xl" id="menu-icon"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Dropdown Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-royal-card border-b border-royal-border px-4 pt-2 pb-6 space-y-2">
            <a href="#home" class="mobile-link block px-4 py-3 rounded-xl text-base font-medium text-gray-200 hover:bg-royal-dark hover:text-royal-gold">Home</a>
            <a href="#features" class="mobile-link block px-4 py-3 rounded-xl text-base font-medium text-gray-200 hover:bg-royal-dark hover:text-royal-gold">Features</a>
            <a href="#rules" class="mobile-link block px-4 py-3 rounded-xl text-base font-medium text-gray-200 hover:bg-royal-dark hover:text-royal-gold">Server Rules</a>
            <a href="#join" class="mobile-link block px-4 py-3 rounded-xl text-base font-medium text-gray-200 hover:bg-royal-dark hover:text-royal-gold">How to Join</a>
            <a href="#staff" class="mobile-link block px-4 py-3 rounded-xl text-base font-medium text-gray-200 hover:bg-royal-dark hover:text-royal-gold">Staff & Community</a>
            <div class="pt-2">
                <a href="https://discord.gg/your-invite-link" target="_blank" rel="noopener noreferrer" 
                   class="w-full flex items-center justify-center gap-2 bg-gradient-to-r from-royal-crimson to-red-800 text-white font-semibold px-5 py-3.5 rounded-xl">
                    <i class="fa-brands fa-discord text-xl"></i>
                    <span>Join Official Discord</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- 2. HERO SECTION -->
    <section id="home" class="relative hero-bg pt-16 pb-24 lg:pt-28 lg:pb-36 overflow-hidden">
        <!-- Decorative Background Elements -->
        <div class="absolute top-20 left-10 w-64 h-64 bg-royal-crimson/10 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute bottom-10 right-10 w-80 h-80 bg-royal-gold/10 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
            <!-- Live Status Badge -->
            <div class="inline-flex items-center gap-2.5 px-4 py-1.5 rounded-full bg-royal-card/90 border border-royal-gold/40 mb-8 shadow-md">
                <span class="relative flex h-2.5 w-2.5">
                    <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                    <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-emerald-500"></span>
                </span>
                <span class="text-xs font-semibold tracking-wider uppercase text-royal-gold">Server Online • Whitelist Open</span>
            </div>

            <!-- Main Title -->
            <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight mb-4">
                <span class="block font-sinhala text-white drop-shadow-md mb-2">වලව්ව</span>
                <span class="font-royal bg-gradient-to-r from-royal-goldLight via-royal-gold to-amber-600 bg-clip-text text-transparent">
                    ROLEPLAY
                </span>
            </h1>

            <!-- Tagline -->
            <p class="text-lg sm:text-2xl font-royal text-gray-300 tracking-wide mb-4">
                Sri Lanka's Premier Roleplay Experience
            </p>
            <p class="max-w-2xl mx-auto text-sm sm:text-base text-gray-400 mb-10 leading-relaxed">
                Step into a realistic Sri Lankan inspired GTA V world. Build your legacy, rule the streets, uphold the law, or run a business empire in the most optimized FiveM community in Sri Lanka.
            </p>

            <!-- Action Buttons: Live IP Copy & Discord -->
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 max-w-xl mx-auto">
                <!-- Copy IP Button -->
                <button onclick="copyServerIP()" 
                        class="w-full sm:w-auto flex-1 group flex items-center justify-between gap-4 bg-royal-card hover:bg-zinc-900 border border-royal-gold/60 px-5 py-4 rounded-2xl transition-all duration-200 gold-glow gold-glow-hover cursor-pointer">
                    <div class="flex items-center gap-3 text-left">
                        <div class="w-10 h-10 rounded-xl bg-royal-gold/15 flex items-center justify-center text-royal-gold group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-server"></i>
                        </div>
                        <div>
                            <span class="block text-[11px] uppercase tracking-wider text-gray-400">Click to Copy IP</span>
                            <code id="server-ip" class="text-sm sm:text-base font-bold text-white">connect play.walawwarp.lk</code>
                        </div>
                    </div>
                    <div class="w-9 h-9 rounded-lg bg-royal-dark flex items-center justify-center text-gray-400 group-hover:text-royal-gold transition-colors">
                        <i class="fa-regular fa-copy" id="copy-icon"></i>
                    </div>
                </button>

                <!-- Join Discord Button -->
                <a href="https://discord.gg/your-invite-link" target="_blank" rel="noopener noreferrer" 
                   class="w-full sm:w-auto flex items-center justify-center gap-3 bg-gradient-to-r from-royal-crimson to-red-800 hover:from-red-700 hover:to-royal-crimson text-white font-bold px-8 py-4 rounded-2xl border border-red-500/40 shadow-xl transition-all duration-200 hover:scale-105">
                    <i class="fa-brands fa-discord text-2xl"></i>
                    <span>Join Discord</span>
                </a>
            </div>

            <!-- Quick Stats Bar -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 max-w-4xl mx-auto mt-16 pt-8 border-t border-royal-border/60">
                <div class="p-3">
                    <p class="text-2xl sm:text-3xl font-extrabold text-royal-gold font-royal">60+ FPS</p>
                    <p class="text-xs text-gray-400 mt-1">Optimized City</p>
                </div>
                <div class="p-3">
                    <p class="text-2xl sm:text-3xl font-extrabold text-white font-royal">150+</p>
                    <p class="text-xs text-gray-400 mt-1">Custom SL Vehicles</p>
                </div>
                <div class="p-3">
                    <p class="text-2xl sm:text-3xl font-extrabold text-royal-gold font-royal">24/7</p>
                    <p class="text-xs text-gray-400 mt-1">Active Staff Support</p>
                </div>
                <div class="p-3">
                    <p class="text-2xl sm:text-3xl font-extrabold text-white font-royal">100%</p>
                    <p class="text-xs text-gray-400 mt-1">Serious & Fun RP</p>
                </div>
            </div>
        </div>
    </section>

    <div class="motif-divider"></div>

    <!-- 3. SERVER FEATURES SECTION -->
    <section id="features" class="py-20 lg:py-28 bg-royal-dark">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header -->
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs font-bold uppercase tracking-widest text-royal-gold">Why Choose Walawwa RP</span>
                <h2 class="text-3xl sm:text-4xl font-royal font-bold text-white mt-2 mb-4">Exclusive Server Features</h2>
                <p class="text-gray-400 text-sm sm:text-base">
                    Crafted with custom scripts and Sri Lankan cultural touches to give you an unforgettable FiveM roleplay adventure.
                </p>
            </div>

            <!-- Feature Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Feature 1 -->
                <div class="bg-royal-card border border-royal-border hover:border-royal-gold/50 rounded-2xl p-6 transition-all duration-300 hover:-translate-y-1 group">
                    <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-royal-crimson/30 to-royal-gold/20 border border-royal-gold/30 flex items-center justify-center text-royal-gold text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-car-side"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-royal-gold transition-colors">Custom SL Vehicles & Map</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Drive iconic Sri Lankan vehicles including Three-Wheelers (Tuk-Tuks), Leyland buses, Defenders, and explore custom local landmarks & Walawwa mansions.
                    </p>
                </div>

                <!-- Feature 2 -->
                <div class="bg-royal-card border border-royal-border hover:border-royal-gold/50 rounded-2xl p-6 transition-all duration-300 hover:-translate-y-1 group">
                    <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-royal-crimson/30 to-royal-gold/20 border border-royal-gold/30 flex items-center justify-center text-royal-gold text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-coins"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-royal-gold transition-colors">Balanced Economy</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Realistic LKR-inspired economy. Start with legal jobs like tea plucking, gem mining, or fishing, and work your way up to owning businesses & luxury properties.
                    </p>
                </div>

                <!-- Feature 3 -->
                <div class="bg-royal-card border border-royal-border hover:border-royal-gold/50 rounded-2xl p-6 transition-all duration-300 hover:-translate-y-1 group">
                    <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-royal-crimson/30 to-royal-gold/20 border border-royal-gold/30 flex items-center justify-center text-royal-gold text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-shield-halved"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-royal-gold transition-colors">Active Police & EMS</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Dedicated Sri Lanka Police (SLPD) and Suwaseriya EMS departments with custom uniforms, realistic MDT dispatch systems, and advanced medical scripts.
                    </p>
                </div>

                <!-- Feature 4 -->
                <div class="bg-royal-card border border-royal-border hover:border-royal-gold/50 rounded-2xl p-6 transition-all duration-300 hover:-translate-y-1 group">
                    <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-royal-crimson/30 to-royal-gold/20 border border-royal-gold/30 flex items-center justify-center text-royal-gold text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-mask"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-royal-gold transition-colors">Custom Gangs & Heists</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Form registered gangs, claim turf, craft black-market weapons, and plan multi-stage bank, jewelry, and armored truck heists with thrilling police chases.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. SERVER RULES QUICK-VIEW TABS -->
    <section id="rules" class="py-20 lg:py-28 bg-zinc-950/70 border-y border-royal-border/60">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header -->
            <div class="text-center max-w-2xl mx-auto mb-12">
                <span class="text-xs font-bold uppercase tracking-widest text-royal-gold">Fair & Fun Gameplay</span>
                <h2 class="text-3xl sm:text-4xl font-royal font-bold text-white mt-2 mb-4">Server Rules Quick-View</h2>
                <p class="text-gray-400 text-sm sm:text-base">
                    හැමෝටම හොඳ RP අත්දැකීමක් ලබාගන්න පහත නීති රීති අනිවාර්යයෙන්ම පිළිපදින්න. Full rules are available on our Discord.
                </p>
            </div>

            <!-- Interactive Rule Category Tabs -->
            <div class="flex flex-wrap justify-center gap-2 sm:gap-3 mb-8" role="tablist">
                <button onclick="switchRuleTab('general')" id="tab-general" 
                        class="rule-tab active px-5 py-3 rounded-xl text-sm font-semibold transition-all bg-royal-gold text-black shadow-lg">
                    <i class="fa-solid fa-book mr-2"></i>General Rules
                </button>
                <button onclick="switchRuleTab('rdmvdm')" id="tab-rdmvdm" 
                        class="rule-tab px-5 py-3 rounded-xl text-sm font-semibold transition-all bg-royal-card text-gray-300 border border-royal-border hover:border-royal-gold/50">
                    <i class="fa-solid fa-skull-crossbones mr-2"></i>RDM & VDM
                </button>
                <button onclick="switchRuleTab('failrp')" id="tab-failrp" 
                        class="rule-tab px-5 py-3 rounded-xl text-sm font-semibold transition-all bg-royal-card text-gray-300 border border-royal-border hover:border-royal-gold/50">
                    <i class="fa-solid fa-ban mr-2"></i>FailRP & Meta
                </button>
                <button onclick="switchRuleTab('crime')" id="tab-crime" 
                        class="rule-tab px-5 py-3 rounded-xl text-sm font-semibold transition-all bg-royal-card text-gray-300 border border-royal-border hover:border-royal-gold/50">
                    <i class="fa-solid fa-handcuffs mr-2"></i>Police & Crime
                </button>
            </div>

            <!-- Rules Content Card -->
            <div class="bg-royal-card border border-royal-border rounded-2xl p-6 sm:p-8 shadow-2xl">
                
                <!-- Tab 1: General Rules -->
                <div id="content-general" class="rule-content space-y-5">
                    <div class="flex items-center justify-between border-b border-royal-border pb-4">
                        <h3 class="text-xl font-bold text-royal-gold">1. General Community Rules</h3>
                        <span class="text-xs bg-royal-crimson/20 text-red-400 border border-red-500/30 px-3 py-1 rounded-full">Mandatory</span>
                    </div>
                    <ul class="space-y-4 text-sm sm:text-base text-gray-300">
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Respect Everyone:</strong> Toxic behavior, racism, religion insults, or OOC (Out of Character) harassment will result in an immediate ban. හැමෝටම ගරු කරන්න.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Working Microphone Required:</strong> Clear voice communication is essential for Roleplay. Use Push-to-Talk to avoid background noise.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">No Exploiting / Cheating:</strong> Using mod menus, third-party cheats, or abusing game bugs/glitches is strictly prohibited.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Stay In Character (IC):</strong> Never break character during an active RP scene. If there is a rule break, finish the scene and report on Discord with a clip.
                            </div>
                        </li>
                    </ul>
                </div>

                <!-- Tab 2: RDM & VDM -->
                <div id="content-rdmvdm" class="rule-content hidden space-y-5">
                    <div class="flex items-center justify-between border-b border-royal-border pb-4">
                        <h3 class="text-xl font-bold text-royal-gold">2. RDM & VDM Policies</h3>
                        <span class="text-xs bg-royal-crimson/20 text-red-400 border border-red-500/30 px-3 py-1 rounded-full">Zero Tolerance</span>
                    </div>
                    <ul class="space-y-4 text-sm sm:text-base text-gray-300">
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-triangle-exclamation text-red-500 mt-1"></i>
                            <div>
                                <strong class="text-white">RDM (Random Deathmatch):</strong> කිසිම RP හේතුවක් හෝ කතාබහක් නැතුව වෙනත් Player කෙනෙක්ට වෙඩි තැබීම හෝ මරා දැමීම සම්පූර්ණයෙන් තහනම්. You must initiate valid RP before attacking.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-triangle-exclamation text-red-500 mt-1"></i>
                            <div>
                                <strong class="text-white">VDM (Vehicle Deathmatch):</strong> වාහන පාවිච්චි කරලා හිතාමතාම මිනිසුන්ව හප්පලා මරන්න උත්සාහ කිරීම තහනම්. Vehicles are not weapons.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Revenge Killing:</strong> If you are downed and respawn at the hospital, you forget the events leading to your death (New Life Rule). Do not return to the scene to take revenge.
                            </div>
                        </li>
                    </ul>
                </div>

                <!-- Tab 3: FailRP & Metagaming -->
                <div id="content-failrp" class="rule-content hidden space-y-5">
                    <div class="flex items-center justify-between border-b border-royal-border pb-4">
                        <h3 class="text-xl font-bold text-royal-gold">3. FailRP, Metagaming & Powergaming</h3>
                        <span class="text-xs bg-royal-gold/20 text-royal-gold border border-royal-gold/30 px-3 py-1 rounded-full">RP Quality</span>
                    </div>
                    <ul class="space-y-4 text-sm sm:text-base text-gray-300">
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Value of Life (NVL):</strong> තුවක්කුවක් පෙන්නලා තර්ජනය කරද්දී (Gunpoint) ඔයාගේ ජීවිතයට බය වෙලා ඒ අය කියන විදියට වැඩ කරන්න ඕනේ. Acting fearless at gunpoint is FailRP.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Metagaming:</strong> Discord calls, Facebook/YouTube Live streams වලින් දකින දේවල් Game එක ඇතුලේ ඔයාගේ Character එක දන්නවා වගේ පාවිච්චි කිරීම තහනම්.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Combat Logging:</strong> Police chase එකක් හෝ RP scene එකක් මැදදී Game එකෙන් Quit වෙලා (Alt+F4) පැනලා යාම තහනම්.
                            </div>
                        </li>
                    </ul>
                </div>

                <!-- Tab 4: Police & Crime Rules -->
                <div id="content-crime" class="rule-content hidden space-y-5">
                    <div class="flex items-center justify-between border-b border-royal-border pb-4">
                        <h3 class="text-xl font-bold text-royal-gold">4. Police, Heists & Gang Rules</h3>
                        <span class="text-xs bg-royal-crimson/20 text-red-400 border border-red-500/30 px-3 py-1 rounded-full">Action RP</span>
                    </div>
                    <ul class="space-y-4 text-sm sm:text-base text-gray-300">
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Safe Zones:</strong> Hospital, Police Station, Garages, and Spawn areas are strict Green Zones. No kidnapping, robbing, or shooting allowed here.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Heist Limits & Hostages:</strong> Do not use fake hostages (your own friends) for robberies. Respect the maximum criminal/police limits set for each heist.
                            </div>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-circle-check text-royal-gold mt-1"></i>
                            <div>
                                <strong class="text-white">Cop Baiting:</strong> පොලිසිය ඉස්සරහා හිතාමතාම නීති කඩලා Police chase ගන්න උත්සාහ කිරීම (Cop Baiting) තහනම්.
                            </div>
                        </li>
                    </ul>
                </div>

            </div>
        </div>
    </section>

    <!-- 5. HOW TO JOIN STEP-BY-STEP SECTION -->
    <section id="join" class="py-20 bg-royal-dark">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-xs font-bold uppercase tracking-widest text-royal-gold">Start Your Journey</span>
                <h2 class="text-3xl sm:text-4xl font-royal font-bold text-white mt-2 mb-4">How to Join Walawwa RP</h2>
                <p class="text-gray-400 text-sm sm:text-base">පියවර 3කින් ලේසියෙන්ම අපේ Server එකට සම්බන්ධ වෙන්න.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Step 1 -->
                <div class="relative bg-royal-card border border-royal-border rounded-2xl p-8 text-center">
                    <div class="w-12 h-12 rounded-full bg-royal-gold text-black font-extrabold text-xl flex items-center justify-center mx-auto mb-5 shadow-lg">1</div>
                    <h3 class="text-lg font-bold text-white mb-2">Install GTA V & FiveM</h3>
                    <p class="text-sm text-gray-400">Make sure you have a legal copy of Grand Theft Auto V installed on your PC, then download and install the FiveM client.</p>
                </div>

                <!-- Step 2 -->
                <div class="relative bg-royal-card border border-royal-border rounded-2xl p-8 text-center">
                    <div class="w-12 h-12 rounded-full bg-royal-gold text-black font-extrabold text-xl flex items-center justify-center mx-auto mb-5 shadow-lg">2</div>
                    <h3 class="text-lg font-bold text-white mb-2">Join Our Discord</h3>
                    <p class="text-sm text-gray-400">Join the official Walawwa RP Discord server, read the rules, and get your Citizen / Whitelist role verified.</p>
                </div>

                <!-- Step 3 -->
                <div class="relative bg-royal-card border border-royal-border rounded-2xl p-8 text-center">
                    <div class="w-12 h-12 rounded-full bg-royal-gold text-black font-extrabold text-xl flex items-center justify-center mx-auto mb-5 shadow-lg">3</div>
                    <h3 class="text-lg font-bold text-white mb-2">Connect & Play</h3>
                    <p class="text-sm text-gray-400">Open FiveM, press <kbd class="px-2 py-0.5 bg-zinc-800 rounded text-royal-gold text-xs">F8</kbd>, type <code class="text-royal-gold text-xs">connect play.walawwarp.lk</code> and create your character!</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 6. STAFF & COMMUNITY SECTION -->
    <section id="staff" class="py-20 bg-zinc-950/70 border-t border-royal-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-xs font-bold uppercase tracking-widest text-royal-gold">Leadership & Support</span>
                <h2 class="text-3xl sm:text-4xl font-royal font-bold text-white mt-2 mb-4">Walawwa Management</h2>
                <p class="text-gray-400 text-sm sm:text-base">Dedicated team working behind the scenes to ensure smooth gameplay and fair moderation.</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Staff Card 1 -->
                <div class="bg-royal-card border border-royal-border rounded-2xl p-6 text-center hover:border-royal-gold/40 transition-colors">
                    <div class="w-20 h-20 rounded-full bg-gradient-to-tr from-royal-crimson to-royal-gold p-1 mx-auto mb-4">
                        <div class="w-full h-full rounded-full bg-royal-dark flex items-center justify-center text-royal-gold text-2xl">
                            <i class="fa-solid fa-crown"></i>
                        </div>
                    </div>
                    <h4 class="text-lg font-bold text-white">Dulhan (Founder)</h4>
                    <span class="inline-block text-xs font-semibold text-royal-gold bg-royal-gold/10 px-3 py-1 rounded-full mt-1">Server Owner</span>
                    <p class="text-xs text-gray-400 mt-3">Visionary & Head of Community Direction</p>
                </div>

                <!-- Staff Card 2 -->
                <div class="bg-royal-card border border-royal-border rounded-2xl p-6 text-center hover:border-royal-gold/40 transition-colors">
                    <div class="w-20 h-20 rounded-full bg-gradient-to-tr from-royal-crimson to-royal-gold p-1 mx-auto mb-4">
                        <div class="w-full h-full rounded-full bg-royal-dark flex items-center justify-center text-royal-gold text-2xl">
                            <i class="fa-solid fa-code"></i>
                        </div>
                    </div>
                    <h4 class="text-lg font-bold text-white">Lead Developer</h4>
                    <span class="inline-block text-xs font-semibold text-red-400 bg-royal-crimson/20 px-3 py-1 rounded-full mt-1">Core Dev</span>
                    <p class="text-xs text-gray-400 mt-3">Custom Scripts, Vehicles & Server Optimization</p>
                </div>

                <!-- Staff Card 3 -->
                <div class="bg-royal-card border border-royal-border rounded-2xl p-6 text-center hover:border-royal-gold/40 transition-colors">
                    <div class="w-20 h-20 rounded-full bg-gradient-to-tr from-royal-crimson to-royal-gold p-1 mx-auto mb-4">
                        <div class="w-full h-full rounded-full bg-royal-dark flex items-center justify-center text-royal-gold text-2xl">
                            <i class="fa-solid fa-gavel"></i>
                        </div>
                    </div>
                    <h4 class="text-lg font-bold text-white">Head Admin</h4>
                    <span class="inline-block text-xs font-semibold text-royal-gold bg-royal-gold/10 px-3 py-1 rounded-full mt-1">Administration</span>
                    <p class="text-xs text-gray-400 mt-3">RP Quality Control & Staff Management</p>
                </div>

                <!-- Staff Card 4 -->
                <div class="bg-royal-card border border-royal-border rounded-2xl p-6 text-center hover:border-royal-gold/40 transition-colors">
                    <div class="w-20 h-20 rounded-full bg-gradient-to-tr from-royal-crimson to-royal-gold p-1 mx-auto mb-4">
                        <div class="w-full h-full rounded-full bg-royal-dark flex items-center justify-center text-royal-gold text-2xl">
                            <i class="fa-solid fa-headset"></i>
                        </div>
                    </div>
                    <h4 class="text-lg font-bold text-white">Support Team</h4>
                    <span class="inline-block text-xs font-semibold text-emerald-400 bg-emerald-500/10 px-3 py-1 rounded-full mt-1">24/7 Support</span>
                    <p class="text-xs text-gray-400 mt-3">Whitelist Interviews & Player Tickets</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 7. FOOTER -->
    <footer class="bg-royal-dark border-t border-royal-border pt-14 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center justify-between gap-8 pb-10 border-b border-royal-border/60">
                <!-- Brand -->
                <div class="text-center md:text-left">
                    <div class="flex items-center justify-center md:justify-start gap-2.5 mb-2">
                        <i class="fa-solid fa-crown text-royal-gold text-xl"></i>
                        <span class="font-sinhala font-extrabold text-2xl text-white">වලව්ව <span class="text-royal-gold font-royal">RP</span></span>
                    </div>
                    <p class="text-sm text-gray-400 max-w-md">
                        Sri Lanka's Premier GTA V FiveM Roleplay Community. Not affiliated with Rockstar Games or Take-Two Interactive.
                    </p>
                </div>

                <!-- Social Links -->
                <div class="flex items-center gap-4">
                    <a href="https://discord.gg/your-invite-link" target="_blank" rel="noopener noreferrer" aria-label="Discord" 
                       class="w-11 h-11 rounded-xl bg-royal-card border border-royal-border hover:border-royal-gold text-gray-300 hover:text-royal-gold flex items-center justify-center text-xl transition-all">
                        <i class="fa-brands fa-discord"></i>
                    </a>
                    <a href="#" target="_blank" rel="noopener noreferrer" aria-label="YouTube" 
                       class="w-11 h-11 rounded-xl bg-royal-card border border-royal-border hover:border-royal-gold text-gray-300 hover:text-royal-gold flex items-center justify-center text-xl transition-all">
                        <i class="fa-brands fa-youtube"></i>
                    </a>
                    <a href="#" target="_blank" rel="noopener noreferrer" aria-label="TikTok" 
                       class="w-11 h-11 rounded-xl bg-royal-card border border-royal-border hover:border-royal-gold text-gray-300 hover:text-royal-gold flex items-center justify-center text-xl transition-all">
                        <i class="fa-brands fa-tiktok"></i>
                    </a>
                    <a href="#" target="_blank" rel="noopener noreferrer" aria-label="Facebook" 
                       class="w-11 h-11 rounded-xl bg-royal-card border border-royal-border hover:border-royal-gold text-gray-300 hover:text-royal-gold flex items-center justify-center text-xl transition-all">
                        <i class="fa-brands fa-facebook"></i>
                    </a>
                </div>
            </div>

            <div class="pt-8 flex flex-col sm:flex-row items-center justify-between text-xs text-gray-500 gap-4">
                <p>&copy; <span id="year"></span> වලව්ව Roleplay (Walawwa RP). All rights reserved.</p>
                <p>Designed for Sri Lankan FiveM Community <span class="text-royal-crimson">♥</span></p>
            </div>
        </div>
    </footer>

    <!-- JAVASCRIPT FOR INTERACTIVITY -->
    <script>
        // Set dynamic current year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle Logic
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuIcon = document.getElementById('menu-icon');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
            if (mobileMenu.classList.contains('hidden')) {
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            } else {
                menuIcon.classList.remove('fa-bars');
                menuIcon.classList.add('fa-xmark');
            }
        });

        // Close mobile menu when clicking a link
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            });
        });

        // Copy Server IP Function (Iframe & Mobile Safe using execCommand)
        function copyServerIP() {
            const ipText = document.getElementById('server-ip').innerText;
            const tempInput = document.createElement('input');
            tempInput.value = ipText;
            document.body.appendChild(tempInput);
            tempInput.select();
            tempInput.setSelectionRange(0, 99999);
            
            try {
                document.execCommand('copy');
                showToast();
                
                // Temporary icon feedback
                const copyIcon = document.getElementById('copy-icon');
                copyIcon.classList.remove('fa-regular', 'fa-copy');
                copyIcon.classList.add('fa-solid', 'fa-check', 'text-emerald-400');
                setTimeout(() => {
                    copyIcon.classList.remove('fa-solid', 'fa-check', 'text-emerald-400');
                    copyIcon.classList.add('fa-regular', 'fa-copy');
                }, 2500);
            } catch (err) {
                console.error('Copy failed', err);
            }
            
            document.body.removeChild(tempInput);
        }

        // Show Custom Toast Notification
        let toastTimeout;
        function showToast() {
            const toast = document.getElementById('toast');
            toast.classList.remove('translate-y-24', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');

            clearTimeout(toastTimeout);
            toastTimeout = setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-24', 'opacity-0');
            }, 3500);
        }

        // Rules Tab Switcher
        function switchRuleTab(tabName) {
            // Hide all rule contents
            document.querySelectorAll('.rule-content').forEach(content => {
                content.classList.add('hidden');
            });

            // Reset all tab buttons styling
            document.querySelectorAll('.rule-tab').forEach(tab => {
                tab.classList.remove('bg-royal-gold', 'text-black', 'shadow-lg');
                tab.classList.add('bg-royal-card', 'text-gray-300', 'border', 'border-royal-border');
            });

            // Show selected content
            document.getElementById('content-' + tabName).classList.remove('hidden');

            // Highlight active tab button
            const activeTab = document.getElementById('tab-' + tabName);
            activeTab.classList.remove('bg-royal-card', 'text-gray-300', 'border', 'border-royal-border');
            activeTab.classList.add('bg-royal-gold', 'text-black', 'shadow-lg');
        }
    </script>
</body>
</html>
