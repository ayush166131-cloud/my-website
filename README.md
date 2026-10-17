<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EDU AI - Next-Gen Cognitive Learning & Exam Mastery</title>
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>⚡</text></svg>">
  
  <!-- Google Fonts: Outfit (Cyberpunk headings) & Inter (Clean UI) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Outfit:wght@400;500;600;700;800;900&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            pitch: '#07080D',
            pitchDark: '#0B0E14',
            surface: 'rgba(15, 20, 31, 0.75)',
            surfaceBorder: 'rgba(255, 255, 255, 0.08)',
            neonGreen: '#00FF88',
            neonCyan: '#00E5FF',
            neonPurple: '#A855F7',
            neonPink: '#FF2A6D',
            neonYellow: '#FACC15'
          },
          fontFamily: {
            outfit: ['Outfit', 'sans-serif'],
            inter: ['Inter', 'sans-serif'],
            mono: ['JetBrains Mono', 'monospace']
          },
          boxShadow: {
            'glow-green': '0 0 25px rgba(0, 255, 136, 0.35)',
            'glow-cyan': '0 0 25px rgba(0, 229, 255, 0.35)',
            'glow-purple': '0 0 25px rgba(168, 85, 247, 0.35)',
            'glow-pink': '0 0 25px rgba(255, 42, 109, 0.35)',
            'neon-box': '0 0 35px -5px rgba(0, 229, 255, 0.25)'
          }
        }
      }
    }
  </script>

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    /* Cyberpunk Custom Scrollbar */
    ::-webkit-scrollbar { width: 8px; height: 8px; }
    ::-webkit-scrollbar-track { background: #07080D; }
    ::-webkit-scrollbar-thumb { background: #1a2234; border-radius: 4px; border: 1px solid rgba(0, 229, 255, 0.2); }
    ::-webkit-scrollbar-thumb:hover { background: #00e5ff; }

    /* Custom Glass & Glow Utilities */
    .glass-card {
      background: rgba(14, 18, 28, 0.82);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }
    .glass-panel {
      background: rgba(11, 14, 20, 0.92);
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
    }
    .text-glow-cyan {
      text-shadow: 0 0 16px rgba(0, 229, 255, 0.65), 0 0 32px rgba(0, 229, 255, 0.3);
    }
    .text-glow-green {
      text-shadow: 0 0 16px rgba(0, 255, 136, 0.65), 0 0 32px rgba(0, 255, 136, 0.3);
    }
    .text-glow-purple {
      text-shadow: 0 0 16px rgba(168, 85, 247, 0.65), 0 0 32px rgba(168, 85, 247, 0.3);
    }
    .gradient-brand {
      background: linear-gradient(135deg, #00FF88 0%, #00E5FF 50%, #A855F7 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .border-glow-cyan {
      box-shadow: 0 0 20px rgba(0, 229, 255, 0.35);
      border-color: #00E5FF;
    }

    /* Scanline Background & Subtle Cyber Grid */
    .cyber-bg {
      background-color: #07080D;
      background-image: 
        radial-gradient(circle at 10% 20%, rgba(168, 85, 247, 0.12) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(0, 229, 255, 0.12) 0%, transparent 40%),
        radial-gradient(circle at 50% 50%, rgba(0, 255, 136, 0.06) 0%, transparent 60%),
        linear-gradient(rgba(255, 255, 255, 0.02) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
      background-size: 100% 100%, 100% 100%, 100% 100%, 48px 48px, 48px 48px;
    }

    /* Shimmer & Pulse Animations */
    @keyframes pulseGlow {
      0%, 100% { filter: drop-shadow(0 0 15px rgba(0, 229, 255, 0.6)); transform: scale(1); }
      50% { filter: drop-shadow(0 0 32px rgba(168, 85, 247, 0.9)); transform: scale(1.02); }
    }
    .animate-logo-pulse {
      animation: pulseGlow 2s ease-in-out infinite;
    }

    @keyframes scan {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(1000%); }
    }
    .scanner-line {
      animation: scan 3s linear infinite;
    }

    /* Print Formatting for Super Notes */
    @media print {
      body { background: #fff !important; color: #000 !important; }
      .no-print { display: none !important; }
      .print-show { display: block !important; }
      .glass-card, .glass-panel { background: #fff !important; border: 1px solid #ddd !important; box-shadow: none !important; color: #000 !important; }
      .gradient-brand { -webkit-text-fill-color: #000 !important; color: #000 !important; }
      * { text-shadow: none !important; filter: none !important; }
    }

    /* Presentation Full Screen Mode for Concept Mind Map */
    .mindmap-fullscreen {
      position: fixed !important;
      inset: 0 !important;
      width: 100vw !important;
      height: 100vh !important;
      max-width: 100vw !important;
      max-height: 100vh !important;
      z-index: 9999 !important;
      border-radius: 0 !important;
      border: none !important;
      margin: 0 !important;
    }
  </style>
</head>
<body class="cyber-bg text-gray-200 font-inter min-h-screen antialiased flex flex-col selection:bg-neonCyan/30 selection:text-neonCyan">

  <!-- ========================================== -->
  <!-- 1. SPLASH SCREEN (Strict 2-Second Transition) -->
  <!-- ========================================== -->
  <div id="splash-screen" class="fixed inset-0 z-50 flex flex-col items-center justify-center bg-[#07080D] transition-all duration-700">
    <div class="relative flex flex-col items-center">
      <!-- Cyber Orbit Rings -->
      <div class="absolute -inset-16 rounded-full border border-neonCyan/20 animate-spin" style="animation-duration: 16s;"></div>
      <div class="absolute -inset-24 rounded-full border border-dashed border-neonPurple/20 animate-spin" style="animation-duration: 24s; animation-direction: reverse;"></div>
      <div class="absolute -inset-8 rounded-full bg-gradient-to-r from-neonGreen/20 via-neonCyan/20 to-neonPurple/20 blur-2xl"></div>

      <!-- Glowing Centered Logo -->
      <div class="relative z-10 flex flex-col items-center text-center">
        <div class="w-24 h-24 mb-6 rounded-2xl bg-gradient-to-br from-neonGreen via-neonCyan to-neonPurple p-0.5 shadow-glow-cyan animate-logo-pulse">
          <div class="w-full h-full bg-[#0B0E14] rounded-2xl flex items-center justify-center">
            <span class="font-outfit font-black text-4xl text-neonCyan">⚡</span>
          </div>
        </div>
        
        <h1 class="font-outfit font-black text-6xl md:text-7xl tracking-wider gradient-brand uppercase drop-shadow-[0_0_25px_rgba(0,229,255,0.7)]">
          EDU AI
        </h1>
        <p class="mt-3 font-outfit text-sm md:text-base uppercase tracking-[0.25em] text-gray-400">
          Cognitive AI for Exam Mastery
        </p>

        <!-- Dynamic Timer Bar (2000ms countdown) -->
        <div class="w-56 h-1.5 mt-8 bg-gray-800/80 rounded-full overflow-hidden p-0.5 border border-white/10">
          <div id="splash-progress" class="h-full bg-gradient-to-r from-neonGreen via-neonCyan to-neonPurple rounded-full w-0 transition-all duration-[2000ms] ease-out shadow-glow-cyan"></div>
        </div>
        
        <span class="mt-4 text-xs font-mono text-gray-500">Initializing Neural Parser...</span>
      </div>
    </div>
    
    <button id="skip-splash-btn" class="absolute bottom-8 text-xs font-mono text-gray-500 hover:text-neonCyan transition-colors">
      Press [Space] or Click to skip
    </button>
  </div>

  <!-- ========================================== -->
  <!-- 2. EDUCATION LEVEL SELECTOR MODAL / SCREEN -->
  <!-- ========================================== -->
  <div id="level-screen" class="hidden fixed inset-0 z-40 flex items-center justify-center p-4 bg-[#07080D]/95 backdrop-blur-xl overflow-y-auto">
    <div class="relative w-full max-w-5xl p-6 md:p-10 rounded-3xl glass-card border border-white/10 shadow-[0_0_50px_rgba(0,229,255,0.15)] my-8">
      
      <!-- Close button (if already selected a level previously) -->
      <button id="level-close-btn" onclick="closeLevelScreen()" class="hidden absolute top-6 right-6 text-gray-400 hover:text-white p-2 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono transition-all">
        ✕ Close
      </button>

      <!-- Ambient Glow Accents -->
      <div class="absolute -top-24 -left-24 w-64 h-64 bg-neonPurple/20 rounded-full blur-3xl pointer-events-none"></div>
      <div class="absolute -bottom-24 -right-24 w-64 h-64 bg-neonCyan/20 rounded-full blur-3xl pointer-events-none"></div>

      <!-- STEP 1: CATEGORY SELECTION (POSTGRADUATE, UNDERGRADUATE, SCHOOL) -->
      <div id="level-step-categories" class="space-y-8 animate-fade">
        <div class="text-center max-w-2xl mx-auto">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/5 border border-white/10 text-xs font-mono text-neonCyan mb-3">
            <span class="w-2 h-2 rounded-full bg-neonCyan animate-ping"></span>
            STEP 1: CHOOSE EDUCATION LEVEL
          </div>
          <h2 class="font-outfit font-extrabold text-3xl md:text-4xl text-white tracking-wide">
            What level of education are you <span class="gradient-brand">pursuing?</span>
          </h2>
          <p class="mt-2 text-gray-400 text-sm md:text-base">
            Select your primary educational phase to calibrate cognitive depth, exam traps, and question rigor.
          </p>
        </div>

        <!-- 3 Primary Sections: Undergraduate, Postgraduate, School -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          
          <!-- Section 1: Undergraduate -->
          <div class="category-card group relative p-6 rounded-3xl glass-card border border-white/10 hover:border-neonCyan hover:shadow-glow-cyan text-left transition-all duration-300 transform hover:-translate-y-2 cursor-pointer flex flex-col justify-between"
            onclick="selectCategory('Undergraduate')">
            <div>
              <div class="flex items-start justify-between">
                <div class="w-14 h-14 rounded-2xl bg-neonCyan/10 border border-neonCyan/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
                  🎓
                </div>
                <span class="px-2.5 py-1 rounded-full text-[10px] font-mono font-medium tracking-wide bg-neonCyan/10 text-neonCyan border border-neonCyan/30">
                  DEGREE
                </span>
              </div>
              <h3 class="font-outfit font-extrabold text-2xl text-white mt-5 group-hover:text-neonCyan transition-colors">
                Undergraduate
              </h3>
              <p class="text-xs text-gray-400 mt-2 leading-relaxed">
                Bachelor's degree courses — Engineering, Medicine, Science, Commerce, Law, Management &amp; Architecture.
              </p>
            </div>
            <div class="mt-6 pt-4 border-t border-white/5 flex items-center justify-between text-xs font-mono text-neonCyan font-semibold">
              <span>11 Specific Courses →</span>
              <span class="text-base group-hover:translate-x-1 transition-transform">➔</span>
            </div>
          </div>

          <!-- Section 2: Postgraduate -->
          <div class="category-card group relative p-6 rounded-3xl glass-card border border-white/10 hover:border-neonPurple hover:shadow-glow-purple text-left transition-all duration-300 transform hover:-translate-y-2 cursor-pointer flex flex-col justify-between"
            onclick="selectCategory('Postgraduate')">
            <div>
              <div class="flex items-start justify-between">
                <div class="w-14 h-14 rounded-2xl bg-neonPurple/10 border border-neonPurple/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
                  🔬
                </div>
                <span class="px-2.5 py-1 rounded-full text-[10px] font-mono font-medium tracking-wide bg-neonPurple/10 text-neonPurple border border-neonPurple/30">
                  MASTERS &amp; PH.D
                </span>
              </div>
              <h3 class="font-outfit font-extrabold text-2xl text-white mt-5 group-hover:text-neonPurple transition-colors">
                Postgraduate
              </h3>
              <p class="text-xs text-gray-400 mt-2 leading-relaxed">
                Master's programs, medical/surgical doctorate, MBA, advanced sciences, research &amp; Ph.D dissertation.
              </p>
            </div>
            <div class="mt-6 pt-4 border-t border-white/5 flex items-center justify-between text-xs font-mono text-neonPurple font-semibold">
              <span>11 Specializations →</span>
              <span class="text-base group-hover:translate-x-1 transition-transform">➔</span>
            </div>
          </div>

          <!-- Section 3: School -->
          <div class="category-card group relative p-6 rounded-3xl glass-card border border-white/10 hover:border-neonGreen hover:shadow-glow-green text-left transition-all duration-300 transform hover:-translate-y-2 cursor-pointer flex flex-col justify-between"
            onclick="selectCategory('School')">
            <div>
              <div class="flex items-start justify-between">
                <div class="w-14 h-14 rounded-2xl bg-neonGreen/10 border border-neonGreen/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
                  🎒
                </div>
                <span class="px-2.5 py-1 rounded-full text-[10px] font-mono font-medium tracking-wide bg-neonGreen/10 text-neonGreen border border-neonGreen/30">
                  K-12 &amp; BOARDS
                </span>
              </div>
              <h3 class="font-outfit font-extrabold text-2xl text-white mt-5 group-hover:text-neonGreen transition-colors">
                School
              </h3>
              <p class="text-xs text-gray-400 mt-2 leading-relaxed">
                Classes 6 through 12 — Senior Secondary Boards, Secondary Exams, JEE/NEET entrance &amp; foundational science.
              </p>
            </div>
            <div class="mt-6 pt-4 border-t border-white/5 flex items-center justify-between text-xs font-mono text-neonGreen font-semibold">
              <span>7 Classes (12 to 6) →</span>
              <span class="text-base group-hover:translate-x-1 transition-transform">➔</span>
            </div>
          </div>

        </div>

        <div class="text-center text-xs text-gray-500 font-mono">
          Click any section above to reveal specific courses or classes. You can switch anytime.
        </div>
      </div>

      <!-- STEP 2: SUB-OPTION DRILLDOWN (POPULATED DYNAMICALLY) -->
      <div id="level-step-suboptions" class="hidden space-y-6 animate-fade">
        <div class="flex flex-wrap items-center justify-between gap-4 pb-4 border-b border-white/10">
          <button onclick="backToCategories()" class="flex items-center gap-2 px-4 py-2 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-gray-300 hover:text-white transition-all">
            <span class="text-neonCyan">←</span> Back to Categories
          </button>
          <div class="flex items-center gap-2">
            <span id="suboption-badge" class="px-3 py-1 rounded-full text-xs font-mono bg-neonCyan/10 text-neonCyan border border-neonCyan/30">
              🎓 Undergraduate
            </span>
          </div>
        </div>

        <div class="text-left">
          <h3 id="suboption-heading" class="font-outfit font-extrabold text-2xl md:text-3xl text-white">
            Choose your exact course
          </h3>
          <p id="suboption-subtext" class="text-xs md:text-sm text-gray-400 mt-1">
            We will calibrate question rigor, formulas, and terminology to this selection.
          </p>
        </div>

        <!-- Dynamic Grid of Sub-Cards -->
        <div id="suboptions-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3.5 max-h-[60vh] overflow-y-auto pr-1">
          <!-- Rendered dynamically -->
        </div>
      </div>

    </div>
  </div>

  <!-- ========================================== -->
  <!-- 3. TOP NAVIGATION BAR -->
  <!-- ========================================== -->
  <header class="no-print sticky top-0 z-30 w-full border-b border-white/10 bg-[#07080D]/80 backdrop-blur-xl">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      
      <!-- Left: Profile Logo / Settings Button & Brand -->
      <div class="flex items-center gap-3">
        <!-- Top-Left Profile & Settings Button with Anime Avatar -->
        <button id="nav-profile-btn" onclick="openProfileSettingsModal()" class="group relative flex items-center gap-2 p-1 pr-2.5 rounded-2xl bg-white/5 hover:bg-white/10 border border-neonCyan/40 hover:border-neonCyan transition-all shadow-[0_0_15px_rgba(0,229,255,0.25)] focus:outline-none" title="Profile, Anime Avatars & Settings">
          <div id="nav-avatar-icon-wrap" class="w-9 h-9 rounded-xl overflow-hidden bg-black/80 flex items-center justify-center p-0.5 border border-white/20 group-hover:scale-105 transition-transform">
            <!-- Dynamic Avatar SVG or Image -->
          </div>
          <div class="hidden sm:flex flex-col text-left">
            <span id="nav-user-name" class="font-outfit font-bold text-xs text-white group-hover:text-neonCyan transition-colors leading-tight">Naruto U.</span>
            <span class="text-[9px] font-mono text-neonCyan tracking-wider uppercase leading-none">⚙️ SETTINGS</span>
          </div>
          <span class="absolute -top-1 -right-1 w-2.5 h-2.5 bg-neonGreen rounded-full ring-2 ring-[#07080D] animate-pulse"></span>
        </button>

        <div class="w-px h-6 bg-white/10 hidden sm:block"></div>

        <!-- Brand Logo -->
        <div class="flex items-center gap-2.5 cursor-pointer" onclick="navigateHome()">
          <div class="w-8 h-8 rounded-xl bg-gradient-to-tr from-neonGreen via-neonCyan to-neonPurple p-0.5 shadow-glow-cyan">
            <div class="w-full h-full bg-[#0B0E14] rounded-xl flex items-center justify-center font-outfit font-black text-neonCyan text-base">
              ⚡
            </div>
          </div>
          <div class="font-outfit font-black text-xl tracking-wider gradient-brand">
            EDU AI
          </div>
        </div>
      </div>

      <!-- Center & Right Stats and Badges -->
      <div class="flex items-center gap-3">
        
        <!-- Active Grade Badge (Clickable to switch level) -->
        <button id="nav-grade-badge" class="group flex items-center gap-2 px-3 py-1.5 rounded-full bg-white/5 hover:bg-white/10 border border-neonCyan/40 hover:border-neonCyan text-xs font-mono text-neonCyan transition-all shadow-[0_0_12px_rgba(0,229,255,0.2)]" title="Click to change education level">
          <span id="nav-grade-text">🎓 Undergraduate</span>
          <span class="text-[10px] text-gray-400 group-hover:text-white transition-colors">✎ Change</span>
        </button>

        <!-- Quick Stats Pill (Desktop) -->
        <div class="hidden md:flex items-center gap-4 px-3 py-1.5 rounded-full bg-white/5 border border-white/10 text-xs font-mono text-gray-400">
          <div class="flex items-center gap-1.5" title="Documents Analyzed">
            <span class="text-neonGreen">📄</span>
            <span id="stat-docs">0 Docs</span>
          </div>
          <div class="w-px h-3 bg-white/10"></div>
          <div class="flex items-center gap-1.5" title="Weak Concepts Cleared">
            <span class="text-neonPink">🛡️</span>
            <span id="stat-weak">0 Weak Spots</span>
          </div>
          <div class="w-px h-3 bg-white/10"></div>
          <div class="flex items-center gap-1.5" title="Diagnostic Quiz Score">
            <span class="text-neonCyan">🎯</span>
            <span id="stat-accuracy">--% Mastery</span>
          </div>
        </div>

        <!-- AI Engine Status Indicator / Settings -->
        <button id="open-settings-btn" class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-gray-300 transition-colors" title="Settings & Gemini API Config">
          <span id="ai-status-dot" class="w-2 h-2 rounded-full bg-neonGreen animate-pulse"></span>
          <span id="ai-status-label" class="hidden sm:inline">Mock AI Active</span>
          <span>⚙️</span>
        </button>
      </div>
    </div>
  </header>

  <!-- ========================================== -->
  <!-- MAIN CONTAINER (PAGE WRAPPER) -->
  <!-- ========================================== -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8">

    <!-- ========================================== -->
    <!-- SCREEN A: DASHBOARD & DOCUMENT INGESTION -->
    <!-- ========================================== -->
    <section id="screen-dashboard" class="space-y-8 animate-fade">
      
      <!-- Welcome Hero Header -->
      <div class="relative overflow-hidden rounded-3xl p-6 sm:p-8 glass-card border border-white/10 shadow-[0_0_40px_rgba(0,0,0,0.5)]">
        <div class="absolute -top-12 -right-12 w-48 h-48 bg-gradient-to-br from-neonCyan/20 to-neonPurple/20 rounded-full blur-2xl pointer-events-none"></div>
        
        <div class="relative max-w-3xl">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-neonGreen/10 border border-neonGreen/30 text-neonGreen text-xs font-mono mb-3">
            <span>●</span>
            MULTI-MODAL INGESTION ENGINE
          </div>
          <h1 class="font-outfit font-black text-3xl sm:text-4xl text-white tracking-wide">
            Turn your study material into <span class="gradient-brand">Adaptive Super Notes</span>
          </h1>
          <p class="mt-2 text-gray-400 text-sm sm:text-base leading-relaxed">
            Upload lecture PDFs, snap camera photos of textbook pages, or paste raw notes. EDU AI synthesizes crisp summaries, builds adaptive weakness-targeting quizzes, and crafts exam cheat sheets.
          </p>
        </div>
      </div>

      <!-- Multi-Modal Input Tabs -->
      <div class="glass-card rounded-3xl border border-white/10 overflow-hidden shadow-2xl">
        
        <!-- Tab Navigation -->
        <div class="flex border-b border-white/10 bg-[#0B0E14]/70 p-2 gap-2 overflow-x-auto">
          <button id="tab-btn-file" class="tab-trigger active flex-1 min-w-[140px] flex items-center justify-center gap-2 py-3 px-4 rounded-xl text-xs sm:text-sm font-outfit font-semibold transition-all bg-neonCyan/15 text-neonCyan border border-neonCyan/40 shadow-glow-cyan" onclick="switchInputTab('file')">
            <span>📁</span> File Upload
          </button>
          <button id="tab-btn-camera" class="tab-trigger flex-1 min-w-[140px] flex items-center justify-center gap-2 py-3 px-4 rounded-xl text-xs sm:text-sm font-outfit font-semibold transition-all text-gray-400 hover:text-white hover:bg-white/5 border border-transparent" onclick="switchInputTab('camera')">
            <span>📷</span> Camera / Photo
          </button>
          <button id="tab-btn-paste" class="tab-trigger flex-1 min-w-[140px] flex items-center justify-center gap-2 py-3 px-4 rounded-xl text-xs sm:text-sm font-outfit font-semibold transition-all text-gray-400 hover:text-white hover:bg-white/5 border border-transparent" onclick="switchInputTab('paste')">
            <span>✍️</span> Paste Text / Notes
          </button>
        </div>

        <!-- TAB CONTENT 1: FILE UPLOAD (DRAG & DROP) -->
        <div id="tab-pane-file" class="p-6 sm:p-8 space-y-6">
          <div id="drop-zone" class="relative group border-2 border-dashed border-white/20 hover:border-neonCyan rounded-2xl p-8 sm:p-12 text-center transition-all duration-300 bg-white/[0.02] hover:bg-neonCyan/[0.04] cursor-pointer">
            <input type="file" id="file-input" class="hidden" multiple accept=".pdf,.docx,.txt,.md,image/*">
            
            <div class="flex flex-col items-center justify-center space-y-4">
              <div class="w-16 h-16 rounded-2xl bg-neonCyan/10 border border-neonCyan/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform shadow-glow-cyan">
                📄
              </div>
              <div>
                <p class="font-outfit font-bold text-lg text-white">
                  Drag & Drop your study documents here
                </p>
                <p class="text-xs sm:text-sm text-gray-400 mt-1">
                  Supports <strong class="text-neonCyan">PDFs, Word (.docx), TXT, Markdown</strong>, and Images
                </p>
              </div>
              <div class="flex items-center gap-3">
                <button type="button" class="px-5 py-2.5 rounded-xl bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan border border-neonCyan/40 text-xs font-mono font-medium transition-all shadow-[0_0_15px_rgba(0,229,255,0.2)]">
                  Browse Files from Device
                </button>
                <span class="text-xs text-gray-500">or drop them anywhere</span>
              </div>
            </div>
          </div>

          <!-- Uploaded Files List -->
          <div id="file-queue-container" class="hidden space-y-3">
            <div class="flex items-center justify-between text-xs font-mono text-gray-400 px-1">
              <span>ATTACHED DOCUMENTS (<span id="queue-count">0</span>)</span>
              <button onclick="clearFiles()" class="text-neonPink hover:underline">Clear all</button>
            </div>
            <div id="file-queue-list" class="space-y-2"></div>
          </div>
        </div>

        <!-- TAB CONTENT 2: CAMERA / WEBCAM PHOTO CAPTURE -->
        <div id="tab-pane-camera" class="hidden p-6 sm:p-8 space-y-6">
          <div class="max-w-xl mx-auto space-y-4">
            <div class="relative overflow-hidden rounded-2xl border border-neonPurple/40 bg-black aspect-video flex items-center justify-center shadow-glow-purple">
              <!-- Live Video Feed -->
              <video id="webcam-feed" autoplay playsinline muted class="w-full h-full object-cover hidden"></video>
              
              <!-- Placeholder when camera idle -->
              <div id="camera-idle-view" class="text-center p-6 space-y-3">
                <div class="w-16 h-16 mx-auto rounded-full bg-neonPurple/10 border border-neonPurple/30 flex items-center justify-center text-3xl">
                  📸
                </div>
                <h4 class="font-outfit font-bold text-white text-base">Physical Notes & Textbook Scanner</h4>
                <p class="text-xs text-gray-400 max-w-sm">
                  Position your camera over notes or blackboard equations. Our OCR engine extracts readable text automatically.
                </p>
                <div class="flex items-center justify-center gap-3 pt-2">
                  <button id="start-camera-btn" onclick="initCamera()" class="px-5 py-2.5 rounded-xl bg-neonPurple/20 hover:bg-neonPurple/30 text-neonPurple border border-neonPurple/50 text-xs font-mono font-semibold transition-all shadow-glow-purple">
                    ▶ Activate Webcam
                  </button>
                  <label class="px-5 py-2.5 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 border border-white/10 text-xs font-mono cursor-pointer transition-all">
                    Upload Photo
                    <input type="file" id="camera-file-fallback" accept="image/*" class="hidden" onchange="handleImageFile(this)">
                  </label>
                </div>
              </div>

              <!-- Live HUD Scanner Overlay (visible when active) -->
              <div id="camera-hud" class="hidden absolute inset-0 pointer-events-none p-4 flex flex-col justify-between">
                <div class="flex justify-between items-center text-[10px] font-mono text-neonCyan bg-black/60 px-3 py-1 rounded backdrop-blur">
                  <span>● LIVE SENSOR HUD</span>
                  <span id="camera-mode-label">ENVIRONMENT MODE</span>
                </div>
                <!-- Reticle Corners -->
                <div class="w-full h-full border-2 border-dashed border-neonCyan/40 rounded-xl relative">
                  <div class="absolute -top-1 -left-1 w-4 h-4 border-t-2 border-l-2 border-neonCyan"></div>
                  <div class="absolute -top-1 -right-1 w-4 h-4 border-t-2 border-r-2 border-neonCyan"></div>
                  <div class="absolute -bottom-1 -left-1 w-4 h-4 border-b-2 border-l-2 border-neonCyan"></div>
                  <div class="absolute -bottom-1 -right-1 w-4 h-4 border-b-2 border-r-2 border-neonCyan"></div>
                </div>
              </div>

              <!-- Canvas for frame snapshot (hidden) -->
              <canvas id="snapshot-canvas" class="hidden"></canvas>
            </div>

            <!-- Camera Control Buttons -->
            <div id="camera-controls" class="hidden flex items-center justify-center gap-4">
              <button onclick="captureSnapshot()" class="flex items-center gap-2 px-6 py-3 rounded-xl bg-gradient-to-r from-neonCyan to-neonPurple text-black font-outfit font-bold text-sm shadow-glow-cyan hover:opacity-90 transition-all">
                <span>📸</span> Capture Snapshot
              </button>
              <button onclick="toggleCameraFacing()" class="px-4 py-3 rounded-xl bg-white/10 hover:bg-white/15 text-white text-xs font-mono border border-white/15 transition-all">
                🔄 Flip Lens
              </button>
              <button onclick="stopCamera()" class="px-4 py-3 rounded-xl bg-neonPink/10 hover:bg-neonPink/20 text-neonPink text-xs font-mono border border-neonPink/30 transition-all">
                ✕ Stop
              </button>
            </div>
          </div>
        </div>

        <!-- TAB CONTENT 3: PASTE TEXT & SAMPLE DATASETS -->
        <div id="tab-pane-paste" class="hidden p-6 sm:p-8 space-y-5">
          <div class="flex flex-wrap items-center justify-between gap-3">
            <label class="text-xs font-mono text-gray-400">PASTE LECTURE NOTES OR SYLLABUS TEXT:</label>
            <div class="flex items-center gap-2">
              <span class="text-xs text-gray-500">Quick Demo Presets:</span>
              <button onclick="loadSamplePreset('bio')" class="px-2.5 py-1 rounded-lg bg-neonGreen/10 hover:bg-neonGreen/20 text-neonGreen border border-neonGreen/30 text-[11px] font-mono transition-all">
                🌱 Photosynthesis
              </button>
              <button onclick="loadSamplePreset('physics')" class="px-2.5 py-1 rounded-lg bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan border border-neonCyan/30 text-[11px] font-mono transition-all">
                🚀 Mechanics & Gravity
              </button>
              <button onclick="loadSamplePreset('cs')" class="px-2.5 py-1 rounded-lg bg-neonPurple/10 hover:bg-neonPurple/20 text-neonPurple border border-neonPurple/30 text-[11px] font-mono transition-all">
                💻 Database & ACID
              </button>
            </div>
          </div>

          <div class="relative">
            <textarea id="paste-input" rows="8" class="w-full rounded-2xl bg-[#07080D]/90 border border-white/10 focus:border-neonCyan p-4 text-sm font-mono text-gray-200 placeholder-gray-600 focus:outline-none focus:ring-1 focus:ring-neonCyan transition-all"
              placeholder="Paste lecture excerpts, chapter notes, definitions, chemical formulas, or textbook paragraphs here..."></textarea>
            
            <div class="absolute bottom-3 right-4 flex items-center gap-3 text-[11px] font-mono text-gray-500 pointer-events-none">
              <span id="word-count-badge">0 words</span>
              <span>·</span>
              <span id="char-count-badge">0 chars</span>
            </div>
          </div>
        </div>

        <!-- Document Preview & Analysis Action Banner -->
        <div id="doc-summary-bar" class="p-6 border-t border-white/10 bg-[#0B0E14]/80 flex flex-col sm:flex-row items-center justify-between gap-4">
          <div class="flex items-center gap-3 w-full sm:w-auto">
            <div id="doc-status-indicator" class="w-3 h-3 rounded-full bg-gray-600"></div>
            <div>
              <div id="doc-summary-title" class="text-sm font-outfit font-semibold text-white">
                No Document Loaded Yet
              </div>
              <div id="doc-summary-meta" class="text-xs text-gray-400">
                Upload files, snap a photo, or load a sample preset above.
              </div>
            </div>
          </div>

          <button id="analyze-doc-btn" disabled onclick="analyzeDocument()" class="w-full sm:w-auto px-8 py-3.5 rounded-xl font-outfit font-bold text-sm tracking-wide text-black bg-gradient-to-r from-neonGreen via-neonCyan to-neonPurple disabled:opacity-40 disabled:cursor-not-allowed hover:opacity-95 shadow-glow-cyan transition-all transform hover:-translate-y-0.5 active:translate-y-0 flex items-center justify-center gap-2">
            <span id="analyze-spinner" class="hidden w-4 h-4 border-2 border-black border-t-transparent rounded-full animate-spin"></span>
            <span id="analyze-btn-text">⚡ Analyze Document</span>
          </button>
        </div>

      </div>

    </section>

    <!-- ========================================== -->
    <!-- SCREEN B: ACTION MODE SELECTOR (POST-UPLOAD) -->
    <!-- ========================================== -->
    <section id="screen-modes" class="hidden space-y-8 animate-fade">
      
      <!-- Document Context Breadcrumb -->
      <div class="flex flex-wrap items-center justify-between gap-4 p-4 rounded-2xl glass-card border border-white/10">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-xl bg-neonCyan/10 border border-neonCyan/30 flex items-center justify-center text-xl">
            📑
          </div>
          <div>
            <div class="flex items-center gap-2">
              <span class="text-xs font-mono text-neonCyan">PARSED DOCUMENT</span>
              <span class="text-xs text-gray-500">•</span>
              <span id="active-doc-words" class="text-xs font-mono text-gray-400">420 Words</span>
            </div>
            <h3 id="active-doc-title" class="font-outfit font-bold text-white text-base">
              Photosynthesis & Chemical Energy Notes
            </h3>
          </div>
        </div>

        <button onclick="navigateDashboard()" class="px-3.5 py-1.5 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-gray-300 hover:text-white transition-all">
          ← Upload Another Document
        </button>
      </div>

      <div class="text-center max-w-2xl mx-auto space-y-2">
        <h2 class="font-outfit font-extrabold text-3xl sm:text-4xl text-white">
          Select Your <span class="gradient-brand">Learning Mode</span>
        </h2>
        <p class="text-sm text-gray-400">
          Synthesized specifically for your target academic stage: <strong id="mode-grade-label" class="text-neonCyan">Undergraduate</strong>.
        </p>
      </div>

      <!-- 4 Feature Cards (Summary, Quiz, Super Notes, Mind Map) -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">

        <!-- Mode 1: Smart Summary -->
        <div class="group relative rounded-3xl p-6 glass-card border border-white/10 hover:border-neonGreen hover:shadow-glow-green transition-all duration-300 flex flex-col justify-between transform hover:-translate-y-2">
          <div class="space-y-4">
            <div class="w-14 h-14 rounded-2xl bg-neonGreen/10 border border-neonGreen/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
              📝
            </div>
            <span class="inline-block px-2.5 py-0.5 rounded-full text-[10px] font-mono tracking-wider bg-neonGreen/10 text-neonGreen border border-neonGreen/30">
              SYNTHESIS
            </span>
            <h3 class="font-outfit font-bold text-xl text-white group-hover:text-neonGreen transition-colors">
              Smart Summary
            </h3>
            <p class="text-xs text-gray-400 leading-relaxed">
              Executive brief, core bullet takeaways, extracted chemical/mathematical formulas, and essential definitions.
            </p>
            <ul class="space-y-2 text-xs font-mono text-gray-400 pt-2 border-t border-white/5">
              <li class="flex items-center gap-2">
                <span class="text-neonGreen">✓</span> Executive TL;DR
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonGreen">✓</span> High-Yield Bullets
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonGreen">✓</span> Equations &amp; Glossary
              </li>
            </ul>
          </div>

          <button onclick="openSmartSummary()" class="mt-8 w-full py-3 rounded-xl bg-neonGreen/10 hover:bg-neonGreen/20 text-neonGreen border border-neonGreen/40 font-outfit font-bold text-xs uppercase tracking-wider transition-all shadow-[0_0_15px_rgba(0,255,136,0.2)]">
            Open Summary →
          </button>
        </div>

        <!-- Mode 2: Adaptive Diagnostic Quiz -->
        <div class="group relative rounded-3xl p-6 glass-card border border-white/10 hover:border-neonCyan hover:shadow-glow-cyan transition-all duration-300 flex flex-col justify-between transform hover:-translate-y-2">
          <div class="space-y-4">
            <div class="w-14 h-14 rounded-2xl bg-neonCyan/10 border border-neonCyan/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
              🎯
            </div>
            <span class="inline-block px-2.5 py-0.5 rounded-full text-[10px] font-mono tracking-wider bg-neonCyan/10 text-neonCyan border border-neonCyan/30">
              WEAKNESS REMEDIATION
            </span>
            <h3 class="font-outfit font-bold text-xl text-white group-hover:text-neonCyan transition-colors">
              Adaptive Quiz
            </h3>
            <p class="text-xs text-gray-400 leading-relaxed">
              Interactive diagnostic test with instant scoring, video tutorials and dynamic reinforcement questions.
            </p>
            <ul class="space-y-2 text-xs font-mono text-gray-400 pt-2 border-t border-white/5">
              <li class="flex items-center gap-2">
                <span class="text-neonCyan">✓</span> Instant Score &amp; Explanations
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonCyan">✓</span> YouTube Video Links
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonCyan">✓</span> Weakness Detection
              </li>
            </ul>
          </div>

          <div class="mt-8 flex flex-col sm:flex-row gap-2">
            <button onclick="openQuizConfigModal()" class="flex-1 py-3 px-3 rounded-xl bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan border border-neonCyan/40 font-outfit font-bold text-xs uppercase tracking-wider transition-all shadow-[0_0_15px_rgba(0,229,255,0.2)] flex items-center justify-center gap-1.5">
              <span>⚙️</span> Customize
            </button>
            <button onclick="openAdaptiveQuiz()" title="Quick start with current settings" class="py-3 px-3 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 hover:text-white border border-white/10 font-mono text-xs transition-all flex items-center justify-center">
              ⚡ Quick
            </button>
          </div>
        </div>

        <!-- Mode 3: Simplified Exam-Oriented Notes ("Super Notes") -->
        <div class="group relative rounded-3xl p-6 glass-card border border-white/10 hover:border-neonPurple hover:shadow-glow-purple transition-all duration-300 flex flex-col justify-between transform hover:-translate-y-2">
          <div class="space-y-4">
            <div class="w-14 h-14 rounded-2xl bg-neonPurple/10 border border-neonPurple/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
              🌈
            </div>
            <span class="inline-block px-2.5 py-0.5 rounded-full text-[10px] font-mono tracking-wider bg-neonPurple/10 text-neonPurple border border-neonPurple/30">
              HIGH-YIELD CHEAT SHEET
            </span>
            <h3 class="font-outfit font-bold text-xl text-white group-hover:text-neonPurple transition-colors">
              Super Notes
            </h3>
            <p class="text-xs text-gray-400 leading-relaxed">
              Converts dense, dry notes into high-retention exam cheat sheets with color-coded callouts and examiner traps.
            </p>
            <ul class="space-y-2 text-xs font-mono text-gray-400 pt-2 border-t border-white/5">
              <li class="flex items-center gap-2">
                <span class="text-neonPurple">✓</span> 💡 Mnemonics &amp; Traps
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonPurple">✓</span> ⚡ 60-Sec Cram Bullets
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonPurple">✓</span> 📐 Step-Marked Q&amp;A
              </li>
            </ul>
          </div>

          <button onclick="openSuperNotes()" class="mt-8 w-full py-3 rounded-xl bg-neonPurple/10 hover:bg-neonPurple/20 text-neonPurple border border-neonPurple/40 font-outfit font-bold text-xs uppercase tracking-wider transition-all shadow-[0_0_15px_rgba(168,85,247,0.2)]">
            Super Notes →
          </button>
        </div>

        <!-- Mode 4: Interactive Concept Mind Map (NEW) -->
        <div class="group relative rounded-3xl p-6 glass-card border border-white/10 hover:border-neonYellow hover:shadow-[0_0_30px_rgba(255,230,0,0.25)] transition-all duration-300 flex flex-col justify-between transform hover:-translate-y-2">
          <div class="space-y-4">
            <div class="w-14 h-14 rounded-2xl bg-neonYellow/10 border border-neonYellow/30 flex items-center justify-center text-3xl group-hover:scale-110 transition-transform">
              🧠
            </div>
            <span class="inline-block px-2.5 py-0.5 rounded-full text-[10px] font-mono tracking-wider bg-neonYellow/10 text-neonYellow border border-neonYellow/30">
              VISUAL KNOWLEDGE GRAPH
            </span>
            <h3 class="font-outfit font-bold text-xl text-white group-hover:text-neonYellow transition-colors">
              Concept Mind Map
            </h3>
            <p class="text-xs text-gray-400 leading-relaxed">
              Radial &amp; dual-loop knowledge graph mapping key concepts, relationships, and detailed branch takeaways from your PDF.
            </p>
            <ul class="space-y-2 text-xs font-mono text-gray-400 pt-2 border-t border-white/5">
              <li class="flex items-center gap-2">
                <span class="text-neonYellow">✓</span> 🕸️ Dual-Loop Radial Nodes
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonYellow">✓</span> 🔍 Interactive Node Inspector
              </li>
              <li class="flex items-center gap-2">
                <span class="text-neonYellow">✓</span> 📥 Zoom &amp; SVG/PNG Export
              </li>
            </ul>
          </div>

          <button onclick="openMindMap()" class="mt-8 w-full py-3 rounded-xl bg-neonYellow/10 hover:bg-neonYellow/20 text-neonYellow border border-neonYellow/40 font-outfit font-bold text-xs uppercase tracking-wider transition-all shadow-[0_0_15px_rgba(255,230,0,0.2)]">
            Explore Mind Map →
          </button>
        </div>

      </div>

    </section>

    <!-- ========================================== -->
    <!-- SCREEN C: SMART SUMMARY VIEW -->
    <!-- ========================================== -->
    <section id="screen-summary" class="hidden space-y-6 animate-fade">
      
      <!-- Top Action Bar -->
      <div class="no-print flex flex-wrap items-center justify-between gap-4 p-4 rounded-2xl glass-card border border-white/10">
        <button onclick="navigateModes()" class="flex items-center gap-2 text-xs font-mono text-gray-400 hover:text-white transition-colors">
          <span>←</span> Back to Learning Modes
        </button>

        <div class="flex items-center gap-3">
          <button id="tts-btn" onclick="toggleAudioSpeech()" class="px-3.5 py-1.5 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-neonCyan flex items-center gap-2 transition-all">
            <span id="tts-icon">🔊</span> <span id="tts-text">Read Aloud</span>
          </button>
          <button onclick="copySummaryText()" class="px-3.5 py-1.5 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-gray-300 hover:text-white flex items-center gap-2 transition-all">
            <span>📋</span> <span id="copy-btn-label">Copy Text</span>
          </button>
          <button onclick="window.print()" class="px-3.5 py-1.5 rounded-xl bg-neonGreen/10 hover:bg-neonGreen/20 text-neonGreen border border-neonGreen/40 text-xs font-mono flex items-center gap-2 transition-all">
            <span>⬇️</span> Print / Save PDF
          </button>
        </div>
      </div>

      <!-- Main Summary Paper -->
      <div class="glass-card rounded-3xl p-6 sm:p-10 border border-white/10 shadow-2xl space-y-8">
        
        <!-- Header -->
        <div class="border-b border-white/10 pb-6">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-neonGreen/10 border border-neonGreen/30 text-neonGreen text-xs font-mono mb-2">
            <span>📝</span> SMART EXECUTIVE SUMMARY
          </div>
          <h2 id="summary-doc-title" class="font-outfit font-black text-2xl sm:text-3xl text-white">
            Document Summary
          </h2>
          <p id="summary-grade-badge" class="text-xs font-mono text-gray-400 mt-1">
            Calibrated for Undergraduate
          </p>
        </div>

        <!-- 1. Executive Brief -->
        <div class="space-y-3">
          <h3 class="font-outfit font-bold text-lg text-neonCyan flex items-center gap-2">
            <span>📌</span> Executive Brief
          </h3>
          <div id="summary-executive-body" class="p-4 sm:p-6 rounded-2xl bg-white/[0.02] border border-white/5 text-sm sm:text-base text-gray-300 leading-relaxed font-inter">
            <!-- Dynamic Executive Summary -->
          </div>
        </div>

        <!-- 2. Core Bullet Points -->
        <div class="space-y-3">
          <h3 class="font-outfit font-bold text-lg text-neonGreen flex items-center gap-2">
            <span>⚡</span> Core Takeaways & High-Yield Bullets
          </h3>
          <ul id="summary-bullets-list" class="space-y-3 text-sm text-gray-300">
            <!-- Dynamic bullets -->
          </ul>
        </div>

        <!-- 3. Essential Formulas & Chemical Reactions -->
        <div class="space-y-3">
          <h3 class="font-outfit font-bold text-lg text-neonCyan flex items-center gap-2">
            <span>📐</span> Essential Formulas & Key Reactions
          </h3>
          <div id="summary-formulas-grid" class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <!-- Dynamic formula cards -->
          </div>
        </div>

        <!-- 4. Key Terminology Glossary -->
        <div class="space-y-3">
          <h3 class="font-outfit font-bold text-lg text-neonPurple flex items-center gap-2">
            <span>📖</span> Essential Terminology Glossary
          </h3>
          <div id="summary-glossary-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3">
            <!-- Dynamic terms -->
          </div>
        </div>

      </div>

    </section>

    <!-- ========================================== -->
    <!-- SCREEN D: ADAPTIVE DIAGNOSTIC QUIZ -->
    <!-- ========================================== -->
    <section id="screen-quiz" class="hidden space-y-6 animate-fade">
      
      <!-- Quiz Header HUD -->
      <div class="flex flex-wrap items-center justify-between gap-4 p-4 rounded-2xl glass-card border border-white/10">
        <div class="flex items-center gap-3">
          <span class="text-2xl">🎯</span>
          <div>
            <div class="text-[10px] font-mono text-neonCyan tracking-wider uppercase">
              ADAPTIVE DIAGNOSTIC QUIZ
            </div>
            <div id="quiz-hud-progress" class="text-xs font-mono text-gray-400">
              Question 1 of 5
            </div>
          </div>
        </div>

        <!-- Live Score, Difficulty Badge & Weaknesses Counter -->
        <div class="flex items-center gap-3 sm:gap-4 text-xs font-mono">
          <div id="quiz-hud-diff-badge" class="px-2.5 py-1 rounded-full bg-neonPurple/10 border border-neonPurple/30 text-neonPurple flex items-center gap-1.5 font-bold uppercase tracking-wider text-[11px]">
            <span>⚡</span> <span id="quiz-hud-diff-text">Medium</span>
          </div>
          <div class="px-3 py-1 rounded-full bg-neonGreen/10 border border-neonGreen/30 text-neonGreen">
            Score: <span id="quiz-live-score" class="font-bold">0</span>
          </div>
          <div id="quiz-weak-counter-badge" class="px-3 py-1 rounded-full bg-neonPink/10 border border-neonPink/30 text-neonPink hidden">
            Weak Spots: <span id="quiz-weak-count" class="font-bold">0</span>
          </div>
          <button onclick="openQuizConfigModal()" title="Customize Quiz Settings" class="text-xs font-mono text-neonCyan hover:text-white px-2.5 py-1 rounded-lg bg-neonCyan/10 border border-neonCyan/30 transition-all flex items-center gap-1">
            <span>⚙️</span> <span class="hidden sm:inline">Settings</span>
          </button>
          <button onclick="exitQuizPrompt()" class="text-gray-400 hover:text-white px-2 py-1">
            ✕ Exit
          </button>
        </div>
      </div>

      <!-- Question Progress Bar -->
      <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden border border-white/10">
        <div id="quiz-progress-bar" class="h-full bg-gradient-to-r from-neonCyan via-neonPurple to-neonGreen rounded-full transition-all duration-300 w-0"></div>
      </div>

      <!-- Dynamic Weakness Detection Alert Banner -->
      <div id="weakness-banner" class="hidden p-4 rounded-2xl bg-neonPink/10 border border-neonPink/40 text-neonPink flex items-center justify-between gap-3 animate-bounce">
        <div class="flex items-center gap-3 text-xs sm:text-sm font-mono">
          <span class="text-xl">⚠️</span>
          <div>
            <strong>Weak Spot Detected:</strong> <span id="weak-concept-name">Calvin Cycle Kinetics</span>
            <div class="text-[11px] text-gray-300 font-sans">
              Dynamic Reinforcement Question spawned in your queue to solidify mastery!
            </div>
          </div>
        </div>
        <span class="text-xs font-mono bg-neonPink/20 px-2 py-1 rounded text-white">REINFORCING</span>
      </div>

      <!-- Active Question Box -->
      <div id="quiz-question-box" class="glass-card rounded-3xl p-6 sm:p-10 border border-white/10 shadow-2xl space-y-8">
        
        <div>
          <div class="flex items-center gap-2 mb-3">
            <span id="quiz-topic-tag" class="px-2.5 py-0.5 rounded-full text-[11px] font-mono bg-neonCyan/10 text-neonCyan border border-neonCyan/30">
              Photosynthesis
            </span>
            <span id="quiz-reinforce-tag" class="hidden px-2.5 py-0.5 rounded-full text-[11px] font-mono bg-neonPink/10 text-neonPink border border-neonPink/30">
              🎯 Reinforcement Question
            </span>
          </div>
          <h3 id="quiz-question-text" class="font-outfit font-bold text-xl sm:text-2xl text-white leading-relaxed">
            What is the primary role of chlorophyll in the light-dependent reactions?
          </h3>
        </div>

        <!-- Options Grid -->
        <div id="quiz-options-grid" class="grid grid-cols-1 gap-3.5">
          <!-- Dynamic Buttons A, B, C, D -->
        </div>

        <!-- In-Depth Student-Friendly Explanation Drawer with YouTube & Internet Sources -->
        <div id="quiz-explanation-box" class="hidden p-6 sm:p-8 rounded-3xl border border-white/10 bg-[#0B0E14]/95 backdrop-blur-xl shadow-2xl space-y-6 animate-fade">
          
          <!-- Banner: Correct / Incorrect -->
          <div id="quiz-feedback-title" class="p-4 rounded-2xl font-outfit font-bold text-base sm:text-lg flex items-center justify-between gap-3">
            <!-- Correct / Incorrect banner -->
          </div>

          <!-- Section 1: In Plain English (Student-Friendly Explanation) -->
          <div class="space-y-2">
            <div class="flex items-center gap-2 text-xs font-mono text-neonCyan font-bold uppercase tracking-wider">
              <span>💡</span> In Plain English (The Core Concept)
            </div>
            <div id="quiz-feedback-simple" class="p-4 sm:p-5 rounded-2xl bg-white/[0.03] border border-neonCyan/30 text-sm text-gray-200 leading-relaxed font-inter">
              <!-- Clear, simple 2-3 sentence breakdown -->
            </div>
          </div>

          <!-- Section 2: Why Your Answer Was Tricky (Misconception Buster) -->
          <div id="quiz-feedback-trap-container" class="hidden space-y-2">
            <div class="flex items-center gap-2 text-xs font-mono text-neonPink font-bold uppercase tracking-wider">
              <span>⚠️</span> Why Your Choice Was Tricky (Common Misconception)
            </div>
            <div id="quiz-feedback-trap" class="p-4 rounded-2xl bg-neonPink/[0.05] border border-neonPink/30 text-xs sm:text-sm text-gray-300 leading-relaxed font-inter">
              <!-- Misconception explanation -->
            </div>
          </div>

          <!-- Section 3: YouTube Educational Video Lesson -->
          <div class="space-y-3 p-5 rounded-2xl bg-red-950/20 border border-red-500/30">
            <div class="flex flex-wrap items-center justify-between gap-2">
              <div class="flex items-center gap-2">
                <span class="w-7 h-7 rounded-lg bg-red-600/20 border border-red-500/40 flex items-center justify-center text-red-400 text-sm">
                  ▶
                </span>
                <div>
                  <div class="text-xs font-mono text-red-400 font-bold uppercase tracking-wider flex items-center gap-2">
                    <span>YouTube Curated Video Lesson</span>
                    <span id="quiz-yt-topic-badge" class="px-2 py-0.5 rounded-full text-[10px] font-mono bg-red-500/10 text-red-300 border border-red-500/30">
                      Topic Breakdown
                    </span>
                  </div>
                  <div class="text-[11px] text-gray-400">
                    Watch this student-friendly video explanation to clearly visualize the concept
                  </div>
                </div>
              </div>
              <a id="quiz-youtube-direct-link" href="#" target="_blank" rel="noopener noreferrer" class="px-3.5 py-1.5 rounded-xl bg-red-600/20 hover:bg-red-600/30 border border-red-500/50 text-xs font-mono text-red-300 hover:text-white flex items-center gap-1.5 transition-all shadow-[0_0_12px_rgba(239,68,68,0.2)]">
                <span>🔗</span> <span>Open Direct Video on YouTube</span> <span>↗</span>
              </a>
            </div>
            
            <!-- Video Player -->
            <div class="relative overflow-hidden rounded-2xl border border-red-500/30 bg-black aspect-video shadow-[0_0_25px_rgba(239,68,68,0.2)]">
              <iframe id="quiz-youtube-iframe" class="w-full h-full" src="" title="YouTube Educational Lesson" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>

            <!-- Fallback Search Link & Topic Summary -->
            <div class="flex flex-wrap items-center justify-between gap-2 pt-1 text-[11px] font-mono text-gray-400">
              <span id="quiz-yt-channel-hint">📺 Recommended channels: Khan Academy, CrashCourse &amp; Amoeba Sisters</span>
              <a id="quiz-youtube-search-link" href="#" target="_blank" rel="noopener noreferrer" class="text-neonCyan hover:underline">
                Search more videos on this topic ↗
              </a>
            </div>
          </div>

          <!-- Section 4: Verified Internet Reference Sources (Wikipedia & Academic Citations) -->
          <div class="space-y-2.5">
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-2 text-xs font-mono text-neonGreen font-bold uppercase tracking-wider">
                <span>🌐</span> Verified Internet Sources &amp; Citations
              </div>
              <span id="quiz-source-tag" class="text-[10px] font-mono px-2 py-0.5 rounded bg-neonGreen/10 text-neonGreen border border-neonGreen/30">
                WIKIPEDIA ENCYCLOPEDIC SOURCE
              </span>
            </div>
            <div id="quiz-internet-source-card" class="p-4 rounded-2xl bg-white/[0.02] border border-neonGreen/30 space-y-2 text-xs text-gray-300">
              <div class="flex items-center justify-between">
                <strong id="quiz-source-title" class="text-sm font-outfit text-white">Concept Citation</strong>
                <a id="quiz-source-link" href="#" target="_blank" rel="noopener noreferrer" class="text-neonGreen hover:underline font-mono text-[11px]">Read Full Article ↗</a>
              </div>
              <p id="quiz-source-extract" class="text-gray-400 leading-relaxed font-inter">
                Loading verified internet citation...
              </p>
            </div>
          </div>

          <!-- Action Buttons -->
          <div class="pt-4 border-t border-white/10 flex items-center justify-between">
            <div class="text-[11px] font-mono text-gray-500">
              Review explanation before continuing
            </div>
            <button id="quiz-next-btn" onclick="nextQuizQuestion()" class="px-7 py-3 rounded-xl font-outfit font-bold text-xs uppercase tracking-wider text-black bg-gradient-to-r from-neonGreen via-neonCyan to-neonPurple hover:opacity-95 shadow-glow-cyan transition-all transform hover:-translate-y-0.5">
              Next Question →
            </button>
          </div>

        </div>

      </div>

      <!-- Quiz Results View (Shown at completion) -->
      <div id="quiz-results-box" class="hidden glass-card rounded-3xl p-6 sm:p-10 border border-white/10 shadow-2xl text-center space-y-8">
        
        <div class="w-20 h-20 mx-auto rounded-3xl bg-gradient-to-tr from-neonGreen via-neonCyan to-neonPurple p-0.5 shadow-glow-cyan">
          <div class="w-full h-full bg-[#0B0E14] rounded-3xl flex items-center justify-center text-4xl">
            🏆
          </div>
        </div>

        <div>
          <h2 class="font-outfit font-black text-3xl sm:text-4xl text-white">
            Diagnostic Test <span class="gradient-brand">Completed</span>
          </h2>
          <p class="text-gray-400 text-sm mt-1">
            Here is your concept mastery breakdown for this session.
          </p>
        </div>

        <!-- Big Score Dial -->
        <div class="inline-flex flex-col items-center justify-center p-6 rounded-3xl bg-white/[0.02] border border-white/10 min-w-[200px]">
          <div id="final-score-text" class="font-outfit font-black text-6xl text-neonCyan">
            4 / 5
          </div>
          <div id="final-percentage-badge" class="mt-2 px-3 py-1 rounded-full text-xs font-mono bg-neonGreen/10 text-neonGreen border border-neonGreen/30">
            80% Mastery Rate
          </div>
        </div>

        <!-- Mastered vs Weak Spots Cards -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-left max-w-3xl mx-auto">
          
          <!-- Mastered Concepts -->
          <div class="p-5 rounded-2xl bg-neonGreen/5 border border-neonGreen/20 space-y-3">
            <div class="flex items-center gap-2 text-neonGreen font-outfit font-bold text-sm">
              <span>✓</span> Mastered Concepts
            </div>
            <ul id="mastered-concepts-list" class="space-y-1.5 text-xs font-mono text-gray-300">
              <li>• Chlorophyll Absorption Spectra</li>
              <li>• Photolysis of Water</li>
            </ul>
          </div>

          <!-- Weak Spots Flagged -->
          <div class="p-5 rounded-2xl bg-neonPink/5 border border-neonPink/20 space-y-3">
            <div class="flex items-center gap-2 text-neonPink font-outfit font-bold text-sm">
              <span>⚠️</span> Concepts Needing Reinforcement
            </div>
            <ul id="flagged-weak-list" class="space-y-1.5 text-xs font-mono text-gray-300">
              <li>• Calvin Cycle Rubisco Kinetics</li>
            </ul>
          </div>

        </div>

        <!-- Action Buttons -->
        <div class="flex flex-wrap items-center justify-center gap-4 pt-4">
          <button id="remediate-weak-btn" onclick="startTargetedRemediation()" class="px-6 py-3 rounded-xl bg-neonPink/20 hover:bg-neonPink/30 text-neonPink border border-neonPink/50 font-outfit font-bold text-xs uppercase tracking-wider shadow-glow-pink transition-all">
            🎯 Remediate Weak Concepts
          </button>
          <button onclick="openQuizConfigModal()" class="px-6 py-3 rounded-xl bg-neonCyan/20 hover:bg-neonCyan/30 text-neonCyan border border-neonCyan/50 font-outfit font-bold text-xs uppercase tracking-wider shadow-glow-cyan transition-all flex items-center gap-2">
            <span>⚙️</span> Customize &amp; Retake
          </button>
          <button onclick="openAdaptiveQuiz()" class="px-5 py-3 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 hover:text-white border border-white/10 font-outfit font-semibold text-xs transition-all">
            🔄 Retake Same Settings
          </button>
          <button onclick="navigateModes()" class="px-5 py-3 rounded-xl bg-white/5 hover:bg-white/10 text-white border border-white/15 font-outfit font-semibold text-xs transition-all">
            Back to Learning Modes
          </button>
        </div>

      </div>

    </section>

    <!-- ========================================== -->
    <!-- SCREEN E: SIMPLIFIED SUPER NOTES (EXAM CHEAT SHEET) -->
    <!-- ========================================== -->
    <section id="screen-supernotes" class="hidden space-y-6 animate-fade">
      
      <!-- Top Action Bar -->
      <div class="no-print flex flex-wrap items-center justify-between gap-4 p-4 rounded-2xl glass-card border border-white/10">
        <button onclick="navigateModes()" class="flex items-center gap-2 text-xs font-mono text-gray-400 hover:text-white transition-colors">
          <span>←</span> Back to Learning Modes
        </button>

        <div class="flex items-center gap-3">
          <button onclick="window.print()" class="px-4 py-2 rounded-xl bg-gradient-to-r from-neonGreen to-neonCyan text-black font-outfit font-bold text-xs uppercase tracking-wider shadow-glow-green transition-all flex items-center gap-2">
            <span>⬇️</span> Export Printable Cheat Sheet
          </button>
        </div>
      </div>

      <!-- Super Notes Content -->
      <div class="glass-card rounded-3xl p-6 sm:p-10 border border-white/10 shadow-2xl space-y-10">
        
        <!-- Header -->
        <div class="border-b border-white/10 pb-6 flex flex-col md:flex-row md:items-center justify-between gap-4">
          <div>
            <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-neonPurple/10 border border-neonPurple/30 text-neonPurple text-xs font-mono mb-2">
              <span>🌈</span> EXAM-ORIENTED SUPER NOTES
            </div>
            <h2 id="supernotes-doc-title" class="font-outfit font-black text-2xl sm:text-3xl text-white">
              High-Yield Exam Cheat Sheet
            </h2>
            <p id="supernotes-grade-tag" class="text-xs font-mono text-gray-400 mt-1">
              Calibrated for Undergraduate
            </p>
          </div>
          <div class="no-print text-right text-xs font-mono text-gray-500">
            <div>EST. REVISION TIME: <strong class="text-neonGreen">3 MINS</strong></div>
            <div>EXAM YIELD: <strong class="text-neonCyan">HIGH</strong></div>
          </div>
        </div>

        <!-- CALLOUT 1: 💡 MNEMONICS & MEMORY HACKS (NEON PURPLE) -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-lg bg-neonPurple/10 border border-neonPurple/30 flex items-center justify-center text-lg">
              💡
            </div>
            <h3 class="font-outfit font-bold text-xl text-white">
              Mnemonics &amp; Memory Hooks
            </h3>
            <span class="text-xs font-mono px-2 py-0.5 rounded bg-neonPurple/10 text-neonPurple border border-neonPurple/30">
              RETENTION
            </span>
          </div>
          <div id="supernotes-mnemonics-grid" class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <!-- Dynamic Mnemonics Cards -->
          </div>
        </div>

        <!-- CALLOUT 2: ⚠️ COMMON EXAM TRAPS (NEON PINK/RED) -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-lg bg-neonPink/10 border border-neonPink/30 flex items-center justify-center text-lg">
              ⚠️
            </div>
            <h3 class="font-outfit font-bold text-xl text-white">
              Common Exam Traps &amp; Pitfalls
            </h3>
            <span class="text-xs font-mono px-2 py-0.5 rounded bg-neonPink/10 text-neonPink border border-neonPink/30">
              AVOID -1 DEDUCTIONS
            </span>
          </div>
          <div id="supernotes-traps-grid" class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <!-- Dynamic Exam Traps Cards -->
          </div>
        </div>

        <!-- CALLOUT 3: ⚡ 60-SECOND QUICK REVISION BULLETS (NEON GREEN) -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-lg bg-neonGreen/10 border border-neonGreen/30 flex items-center justify-center text-lg">
              ⚡
            </div>
            <h3 class="font-outfit font-bold text-xl text-white">
              60-Second Cram Revision
            </h3>
            <span class="text-xs font-mono px-2 py-0.5 rounded bg-neonGreen/10 text-neonGreen border border-neonGreen/30">
              RAPID RECALL
            </span>
          </div>
          <div id="supernotes-bullets-box" class="p-6 rounded-2xl bg-neonGreen/[0.04] border border-neonGreen/30 space-y-3">
            <!-- Dynamic rapid bullets -->
          </div>
        </div>

        <!-- CALLOUT 4: 📐 ESSENTIAL FORMULAS & EQUATIONS (NEON CYAN) -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-lg bg-neonCyan/10 border border-neonCyan/30 flex items-center justify-center text-lg">
              📐
            </div>
            <h3 class="font-outfit font-bold text-xl text-white">
              Core Formulas &amp; Equations Sheet
            </h3>
            <span class="text-xs font-mono px-2 py-0.5 rounded bg-neonCyan/10 text-neonCyan border border-neonCyan/30">
              NUMERICALS &amp; DERIVATIONS
            </span>
          </div>
          <div id="supernotes-formulas-grid" class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <!-- Dynamic formula cards -->
          </div>
        </div>

        <!-- CALLOUT 5: 🎯 HIGH-PROBABILITY EXAM QUESTIONS (1, 3 & 5 MARKS) -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-lg bg-neonYellow/10 border border-neonYellow/30 flex items-center justify-center text-lg">
              🎯
            </div>
            <h3 class="font-outfit font-bold text-xl text-white">
              Mark-Graded Exam Practice Questions
            </h3>
            <span class="text-xs font-mono px-2 py-0.5 rounded bg-neonYellow/10 text-neonYellow border border-neonYellow/30">
              STEP-MARKING READY
            </span>
          </div>
          <div id="supernotes-qa-list" class="space-y-3">
            <!-- Dynamic Accordion Q&A -->
          </div>
        </div>

      </div>

    </section>

    <!-- ========================================== -->
    <!-- SCREEN F: INTERACTIVE CONCEPT MIND MAP (Dual-Loop Knowledge Graph) -->
    <!-- ========================================== -->
    <section id="screen-mindmap" class="hidden space-y-6 animate-fade">
      
      <!-- Top Action Bar -->
      <div class="no-print flex flex-wrap items-center justify-between gap-4 p-4 rounded-2xl glass-card border border-white/10">
        <div class="flex items-center gap-3">
          <button onclick="navigateModes()" class="flex items-center gap-2 text-xs font-mono text-gray-400 hover:text-white transition-colors">
            <span>←</span> Back to Learning Modes
          </button>
          <div class="h-4 w-px bg-white/10 hidden sm:block"></div>
          <span class="text-xs font-mono px-2.5 py-0.5 rounded-full bg-neonYellow/10 text-neonYellow border border-neonYellow/30 hidden sm:inline-flex items-center gap-1.5">
            <span>🧠</span> <span id="mindmap-grade-badge">Calibrated Knowledge Graph</span>
          </span>
        </div>

        <!-- Controls: Layout Switch, Zoom In/Out, Full Screen Presentation -->
        <div class="flex items-center gap-2 sm:gap-3 text-xs font-mono">
          <div class="flex items-center rounded-xl bg-white/5 border border-white/10 p-1">
            <button onclick="setMindmapLayout('dual-loop')" id="mm-layout-dual" class="px-3 py-1 rounded-lg bg-neonYellow/20 text-neonYellow font-bold transition-all">
              Dual-Loop
            </button>
            <button onclick="setMindmapLayout('radial')" id="mm-layout-radial" class="px-3 py-1 rounded-lg text-gray-400 hover:text-white transition-all">
              Radial Star
            </button>
          </div>

          <!-- Centered Zoom Controls -->
          <div class="flex items-center rounded-xl bg-white/5 border border-white/10 p-0.5">
            <button onclick="zoomMindMap(0.85)" title="Zoom Out" class="w-8 h-8 rounded-lg hover:bg-white/10 text-gray-300 hover:text-white flex items-center justify-center font-bold text-sm transition-colors">
              −
            </button>
            <button onclick="resetMindMapZoom()" title="Reset to 100%" id="mm-zoom-level" class="px-2.5 py-0.5 text-[11px] font-mono font-bold text-neonYellow hover:bg-white/5 rounded transition-all">
              100%
            </button>
            <button onclick="zoomMindMap(1.15)" title="Zoom In" class="w-8 h-8 rounded-lg hover:bg-white/10 text-gray-300 hover:text-white flex items-center justify-center font-bold text-sm transition-colors">
              +
            </button>
          </div>

          <!-- Presentation Full Screen Toggle -->
          <button onclick="toggleMindMapFullscreen()" title="Present Full Screen" id="mm-fs-btn" class="px-3 py-1.5 rounded-xl bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan border border-neonCyan/40 flex items-center gap-1.5 transition-all">
            <span>⛶</span> <span id="mm-fs-label">Full Screen</span>
          </button>

          <button onclick="exportMindMapSVG()" title="Export Vector SVG" class="px-3 py-1.5 rounded-xl bg-neonYellow/10 hover:bg-neonYellow/20 text-neonYellow border border-neonYellow/40 flex items-center gap-1.5 transition-all">
            <span>⬇️</span> <span class="hidden md:inline">Export SVG</span>
          </button>
        </div>
      </div>

      <!-- Main Interactive Mind Map Workspace Card -->
      <div class="glass-card rounded-3xl p-4 sm:p-8 border border-white/10 shadow-2xl space-y-6">
        
        <!-- Header & Breadcrumbs -->
        <div class="flex flex-wrap items-center justify-between gap-4 border-b border-white/10 pb-4">
          <div>
            <div class="inline-flex items-center gap-2 text-xs font-mono text-neonYellow mb-1">
              <span>🕸️</span> <span>KNOWLEDGE TOPOLOGY &amp; CONCEPT PATHWAYS</span>
            </div>
            <h2 id="mindmap-doc-title" class="font-outfit font-black text-2xl sm:text-3xl text-white">
              Visual Concept Mind Map
            </h2>
            <p class="text-xs text-gray-400 mt-1">
              Click any colored node to inspect core definitions, exam significance, and connected sub-topics.
            </p>
          </div>

          <div class="flex items-center gap-3 text-xs font-mono">
            <span class="flex items-center gap-1.5 text-gray-400">
              <span class="w-2.5 h-2.5 rounded-full bg-neonCyan"></span> Core
            </span>
            <span class="flex items-center gap-1.5 text-gray-400">
              <span class="w-2.5 h-2.5 rounded-full bg-neonGreen"></span> Inputs
            </span>
            <span class="flex items-center gap-1.5 text-gray-400">
              <span class="w-2.5 h-2.5 rounded-full bg-neonPurple"></span> Mechanism
            </span>
            <span class="flex items-center gap-1.5 text-gray-400">
              <span class="w-2.5 h-2.5 rounded-full bg-neonPink"></span> Outputs
            </span>
            <span class="flex items-center gap-1.5 text-gray-400">
              <span class="w-2.5 h-2.5 rounded-full bg-neonYellow"></span> Law
            </span>
          </div>
        </div>

        <!-- Full-Screen Interactive Mind Map Presentation Canvas -->
        <div id="mindmap-canvas-container" class="relative w-full h-[78vh] min-h-[640px] rounded-3xl bg-[#05060A] border border-white/10 overflow-hidden select-none transition-all duration-300">
          
          <!-- Subtle Cyber Grid Background -->
          <div class="absolute inset-0 opacity-15 pointer-events-none" style="background-image: radial-gradient(rgba(0, 229, 255, 0.4) 1px, transparent 1px); background-size: 24px 24px;"></div>

          <!-- Helper Overlay Tip -->
          <div class="absolute top-4 left-4 z-10 px-3 py-1.5 rounded-xl bg-black/70 backdrop-blur-md border border-white/10 text-[11px] font-mono text-gray-300 flex items-center gap-2 pointer-events-none shadow-lg">
            <span>💡</span> <span>Click any orb or pill to view details • Zoom with + / −</span>
          </div>

          <!-- Floating On-Canvas Quick Zoom Controls (Bottom Left) -->
          <div class="absolute bottom-4 left-4 z-10 flex items-center gap-1.5 p-1.5 rounded-2xl bg-black/80 backdrop-blur-md border border-white/10 shadow-2xl font-mono text-xs">
            <button onclick="zoomMindMap(0.85)" title="Zoom Out" class="w-8 h-8 rounded-xl bg-white/5 hover:bg-white/15 text-gray-200 hover:text-white flex items-center justify-center font-bold text-sm transition-all">
              −
            </button>
            <button onclick="resetMindMapZoom()" title="Reset to 100%" id="mm-canvas-zoom-badge" class="px-2.5 py-1 rounded-xl bg-white/5 hover:bg-white/10 text-neonYellow font-bold text-[11px] transition-all">
              100%
            </button>
            <button onclick="zoomMindMap(1.15)" title="Zoom In" class="w-8 h-8 rounded-xl bg-white/5 hover:bg-white/15 text-gray-200 hover:text-white flex items-center justify-center font-bold text-sm transition-all">
              +
            </button>
            <div class="h-4 w-px bg-white/10 mx-0.5"></div>
            <button onclick="toggleMindMapFullscreen()" title="Toggle Full Screen Mode" class="px-2.5 py-1 rounded-xl bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan font-medium flex items-center gap-1 text-[11px] transition-all">
              <span>⛶</span> Full Screen
            </button>
          </div>

          <!-- Exit Full Screen button (Visible when presented in full screen) -->
          <button id="mm-fs-close-btn" onclick="toggleMindMapFullscreen(false)" class="hidden absolute top-4 right-4 z-30 px-3.5 py-2 rounded-xl bg-red-500/20 hover:bg-red-500/30 text-red-300 border border-red-500/40 text-xs font-mono font-bold flex items-center gap-1.5 shadow-2xl transition-all">
            <span>✕</span> Exit Full Screen
          </button>

          <!-- The SVG Element -->
          <svg id="mindmap-svg" class="w-full h-full block select-none" viewBox="0 0 1000 650" width="100%" height="100%" preserveAspectRatio="xMidYMid meet" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <!-- Glowing Filters -->
              <filter id="glow-cyan" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="glow-blue" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="glow-purple" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="glow-green" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="glow-pink" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="glow-yellow" x="-30%" y="-30%" width="160%" height="160%">
                <feGaussianBlur stdDeviation="4" result="blur" />
                <feMerge>
                  <feMergeNode in="blur" />
                  <feMergeNode in="SourceGraphic" />
                </feMerge>
              </filter>
              <filter id="orb-shadow" x="-30%" y="-30%" width="160%" height="160%">
                <feDropShadow dx="0" dy="6" stdDeviation="6" flood-color="#000000" flood-opacity="0.7" />
              </filter>

              <!-- Node Gradients (Rich 3D Spherical Effect) -->
              <radialGradient id="grad-center" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#FFFFFF" />
                <stop offset="40%" stop-color="#E2E8F0" />
                <stop offset="75%" stop-color="#94A3B8" />
                <stop offset="100%" stop-color="#334155" />
              </radialGradient>
              <linearGradient id="grad-ruby" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#FF2A6D" />
                <stop offset="50%" stop-color="#E11D48" />
                <stop offset="100%" stop-color="#881337" />
              </linearGradient>
              <radialGradient id="grad-cyan" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#A5F3FC" />
                <stop offset="45%" stop-color="#00E5FF" />
                <stop offset="100%" stop-color="#0891B2" />
              </radialGradient>
              <radialGradient id="grad-blue" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#BAE6FD" />
                <stop offset="45%" stop-color="#0284C7" />
                <stop offset="100%" stop-color="#0369A1" />
              </radialGradient>
              <radialGradient id="grad-green" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#BBF7D0" />
                <stop offset="45%" stop-color="#10B981" />
                <stop offset="100%" stop-color="#047857" />
              </radialGradient>
              <radialGradient id="grad-purple" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#F3E8FF" />
                <stop offset="45%" stop-color="#A855F7" />
                <stop offset="100%" stop-color="#6B21A8" />
              </radialGradient>
              <radialGradient id="grad-pink" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#FFE4E6" />
                <stop offset="45%" stop-color="#FF2A6D" />
                <stop offset="100%" stop-color="#9F1239" />
              </radialGradient>
              <radialGradient id="grad-yellow" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#FEF9C3" />
                <stop offset="45%" stop-color="#F59E0B" />
                <stop offset="100%" stop-color="#92400E" />
              </radialGradient>
              <radialGradient id="grad-amber" cx="35%" cy="35%" r="65%">
                <stop offset="0%" stop-color="#FED7AA" />
                <stop offset="45%" stop-color="#F97316" />
                <stop offset="100%" stop-color="#C2410C" />
              </radialGradient>
            </defs>

            <!-- Dynamic SVG Content: Connectors, Paths, Central Ring, Orbs & Text Tags -->
            <g id="mindmap-svg-viewport" transform="translate(0, 0) scale(1)">
              <!-- Populated dynamically via renderMindMap() -->
            </g>
          </svg>

          <!-- Floating Inspector Drawer (Opens on Node Click) -->
          <div id="mindmap-inspector" class="hidden absolute right-4 bottom-4 top-4 w-full max-w-sm rounded-2xl bg-[#0B0E14]/95 backdrop-blur-xl border border-neonYellow/40 p-5 shadow-2xl flex flex-col justify-between z-20 animate-slide-left">
            <div class="space-y-4 overflow-y-auto pr-1">
              <div class="flex items-center justify-between border-b border-white/10 pb-3">
                <div class="flex items-center gap-2">
                  <span id="inspector-icon" class="text-2xl">💡</span>
                  <div>
                    <span id="inspector-badge" class="px-2 py-0.5 rounded text-[10px] font-mono bg-neonYellow/20 text-neonYellow border border-neonYellow/30">
                      CORE CONCEPT
                    </span>
                    <h4 id="inspector-title" class="font-outfit font-bold text-lg text-white mt-0.5">
                      Concept Node
                    </h4>
                  </div>
                </div>
                <button onclick="closeMindMapInspector()" class="text-gray-400 hover:text-white p-1">
                  ✕
                </button>
              </div>

              <div>
                <label class="text-[10px] font-mono uppercase text-gray-400">Definition &amp; Role</label>
                <p id="inspector-desc" class="text-xs text-gray-300 font-inter leading-relaxed mt-1 p-3 rounded-xl bg-white/[0.03] border border-white/5">
                  Node definition here...
                </p>
              </div>

              <div>
                <label class="text-[10px] font-mono uppercase text-neonYellow">Exam &amp; Syllabus High-Yield Takeaway</label>
                <div id="inspector-takeaway" class="text-xs text-neonYellow/90 font-mono leading-relaxed mt-1 p-3 rounded-xl bg-neonYellow/[0.05] border border-neonYellow/20">
                  Exam significance note...
                </div>
              </div>

              <div>
                <label class="text-[10px] font-mono uppercase text-neonCyan">Directly Connected Nodes</label>
                <ul id="inspector-connections" class="space-y-1.5 mt-1 text-xs font-mono text-gray-300">
                  <!-- Dynamic connected nodes -->
                </ul>
              </div>
            </div>

            <div class="pt-3 border-t border-white/10 flex items-center justify-between">
              <span class="text-[10px] font-mono text-gray-500">Interactive Node Inspector</span>
              <button onclick="openQuizForConcept(activeMindmapNodeTopic)" class="px-3 py-1.5 rounded-xl bg-neonCyan/15 hover:bg-neonCyan/25 text-neonCyan border border-neonCyan/30 text-xs font-mono flex items-center gap-1.5 transition-all">
                <span>🎯 Quiz On This</span>
              </button>
            </div>
          </div>

        </div>

        <!-- Node Legend Cards (6 Concepts Breakdown from PDF) -->
        <div class="space-y-3 pt-2">
          <div class="flex items-center justify-between">
            <h4 class="font-outfit font-bold text-base text-white flex items-center gap-2">
              <span>📑</span> <span>Concept Nodes Extracted from PDF</span>
            </h4>
            <span class="text-xs font-mono text-gray-500">Click any card to focus on map</span>
          </div>
          <div id="mindmap-nodes-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3">
            <!-- Dynamic 6 node cards -->
          </div>
        </div>

      </div>

    </section>

  </main>

  <!-- ========================================== -->
  <!-- PROFILE & SETTINGS COMPREHENSIVE MODAL -->
  <!-- ========================================== -->
  <div id="profile-settings-modal" class="hidden fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/85 backdrop-blur-xl overflow-y-auto">
    <div class="relative w-full max-w-2xl p-6 sm:p-8 rounded-3xl glass-card border border-white/10 shadow-[0_0_60px_rgba(0,229,255,0.2)] my-6 space-y-6">
      
      <!-- Modal Header -->
      <div class="flex items-center justify-between pb-4 border-b border-white/10">
        <div class="flex items-center gap-3">
          <div id="modal-header-avatar" class="w-12 h-12 rounded-2xl overflow-hidden bg-black/90 p-1 border-2 border-neonCyan shadow-glow-cyan flex items-center justify-center">
            <!-- Dynamic Avatar preview -->
          </div>
          <div>
            <h3 class="font-outfit font-extrabold text-xl sm:text-2xl text-white flex items-center gap-2">
              <span id="modal-user-title">Profile &amp; Settings</span>
            </h3>
            <p class="text-xs font-mono text-gray-400">
              Customize your anime avatar, appearance, audio, and AI settings
            </p>
          </div>
        </div>
        <button onclick="closeProfileSettingsModal()" class="w-8 h-8 rounded-xl bg-white/5 hover:bg-white/10 text-gray-400 hover:text-white flex items-center justify-center transition-colors">
          ✕
        </button>
      </div>

      <!-- Navigation Tabs inside Settings -->
      <div class="flex border-b border-white/10 gap-2 overflow-x-auto pb-2 text-xs font-mono">
        <button id="pmodal-tab-avatar" onclick="switchProfileModalTab('avatar')" class="px-4 py-2 rounded-xl bg-neonCyan/15 text-neonCyan border border-neonCyan/40 font-bold transition-all">
          🍥 Avatar &amp; Profile
        </button>
        <button id="pmodal-tab-general" onclick="switchProfileModalTab('general')" class="px-4 py-2 rounded-xl text-gray-400 hover:text-white hover:bg-white/5 border border-transparent transition-all">
          ⚙️ Website Settings
        </button>
        <button id="pmodal-tab-ai" onclick="switchProfileModalTab('ai')" class="px-4 py-2 rounded-xl text-gray-400 hover:text-white hover:bg-white/5 border border-transparent transition-all">
          🤖 AI Engine &amp; API
        </button>
        <button id="pmodal-tab-stats" onclick="switchProfileModalTab('stats')" class="px-4 py-2 rounded-xl text-gray-400 hover:text-white hover:bg-white/5 border border-transparent transition-all">
          📊 Data &amp; Stats
        </button>
      </div>

      <!-- TAB 1: AVATAR & PROFILE -->
      <div id="pmodal-pane-avatar" class="space-y-6">
        
        <!-- Display Name & Active Education Level -->
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-xs font-mono text-gray-300 mb-1.5">DISPLAY NAME / CODENAME:</label>
            <input type="text" id="profile-name-input" value="Naruto Uzumaki" class="w-full rounded-xl bg-[#07080D] border border-white/10 focus:border-neonCyan p-3 text-xs font-mono text-white focus:outline-none focus:ring-1 focus:ring-neonCyan">
          </div>
          <div>
            <label class="block text-xs font-mono text-gray-300 mb-1.5">CURRENT EDUCATION LEVEL:</label>
            <div class="flex items-center justify-between p-2.5 rounded-xl bg-[#07080D] border border-white/10 text-xs font-mono">
              <span id="profile-current-level" class="text-neonCyan truncate max-w-[180px]">🎓 Undergraduate</span>
              <button onclick="closeProfileSettingsModal(); openLevelScreen();" class="text-[11px] text-gray-400 hover:text-white underline">Change</button>
            </div>
          </div>
        </div>

        <!-- Custom Upload or Randomize Row -->
        <div class="flex flex-wrap items-center justify-between gap-3 p-3.5 rounded-2xl bg-white/[0.02] border border-white/5">
          <div class="text-xs text-gray-300">
            <strong class="text-white">Custom Profile Photo:</strong> Upload any picture from your device
          </div>
          <div class="flex items-center gap-2">
            <label class="px-3.5 py-1.5 rounded-xl bg-neonCyan/10 hover:bg-neonCyan/20 text-neonCyan border border-neonCyan/40 text-xs font-mono cursor-pointer transition-all shadow-[0_0_10px_rgba(0,229,255,0.2)]">
              📁 Choose Photo
              <input type="file" id="custom-avatar-file" accept="image/*" class="hidden" onchange="handleCustomAvatarUpload(this)">
            </label>
            <button onclick="randomizeAnimeAvatar()" class="px-3.5 py-1.5 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 text-xs font-mono border border-white/10 transition-all">
              🎲 Randomize
            </button>
          </div>
        </div>

        <!-- Default Anime & Cartoon Characters Avatar Grid -->
        <div>
          <label class="block text-xs font-mono text-neonCyan mb-2">
            CHOOSE ANIME &amp; CARTOON CHARACTER AVATAR:
          </label>
          <div id="anime-avatars-grid" class="grid grid-cols-2 sm:grid-cols-5 gap-3 max-h-60 overflow-y-auto pr-1">
            <!-- Dynamic Avatar Cards -->
          </div>
        </div>

      </div>

      <!-- TAB 2: WEBSITE SETTINGS (Basic everyday website controls) -->
      <div id="pmodal-pane-general" class="hidden space-y-6">
        
        <!-- Appearance & Accent Color -->
        <div class="space-y-3">
          <label class="block text-xs font-mono text-gray-300">THEME ACCENT GLOW COLOR:</label>
          <div class="flex items-center gap-3">
            <button onclick="setThemeAccent('cyan', '#00E5FF')" class="w-8 h-8 rounded-full bg-[#00E5FF] shadow-[0_0_15px_#00E5FF] border-2 border-white focus:outline-none" title="Neon Cyan"></button>
            <button onclick="setThemeAccent('green', '#00FF88')" class="w-8 h-8 rounded-full bg-[#00FF88] shadow-[0_0_15px_#00FF88] border-2 border-transparent hover:border-white focus:outline-none" title="Neon Green"></button>
            <button onclick="setThemeAccent('purple', '#A855F7')" class="w-8 h-8 rounded-full bg-[#A855F7] shadow-[0_0_15px_#A855F7] border-2 border-transparent hover:border-white focus:outline-none" title="Neon Purple"></button>
            <button onclick="setThemeAccent('pink', '#FF2A6D')" class="w-8 h-8 rounded-full bg-[#FF2A6D] shadow-[0_0_15px_#FF2A6D] border-2 border-transparent hover:border-white focus:outline-none" title="Neon Pink"></button>
            <button onclick="setThemeAccent('yellow', '#FACC15')" class="w-8 h-8 rounded-full bg-[#FACC15] shadow-[0_0_15px_#FACC15] border-2 border-transparent hover:border-white focus:outline-none" title="Cyber Gold"></button>
          </div>
        </div>

        <!-- UI Sound Effects Toggle -->
        <div class="flex items-center justify-between p-4 rounded-2xl bg-white/[0.02] border border-white/5">
          <div>
            <div class="text-xs font-bold text-white">Cyber Synthesizer Sound Effects</div>
            <div class="text-[11px] text-gray-400">Plays futuristic audio feedback during clicks, quiz answers, and camera snapshots.</div>
          </div>
          <input type="checkbox" id="settings-sound-toggle" checked class="w-5 h-5 accent-neonCyan">
        </div>

        <!-- Text-to-Speech Speed -->
        <div class="space-y-2 p-4 rounded-2xl bg-white/[0.02] border border-white/5">
          <div class="flex justify-between items-center">
            <span class="text-xs font-bold text-white">Smart Summary Voice Speed (TTS):</span>
            <span id="tts-rate-label" class="text-xs font-mono text-neonCyan">1.0x</span>
          </div>
          <input type="range" id="tts-rate-slider" min="0.75" max="1.5" step="0.25" value="1.0" class="w-full accent-neonCyan" oninput="document.getElementById('tts-rate-label').textContent = this.value + 'x'">
        </div>

        <!-- Keyboard Shortcuts Legend -->
        <div class="p-4 rounded-2xl bg-white/[0.02] border border-white/5 space-y-2 text-xs font-mono text-gray-400">
          <div class="font-bold text-gray-300">KEYBOARD SHORTCUTS:</div>
          <div class="grid grid-cols-2 gap-2 text-[11px]">
            <div><kbd class="px-1.5 py-0.5 rounded bg-white/10 text-white">[Space]</kbd> Skip Splash Screen</div>
            <div><kbd class="px-1.5 py-0.5 rounded bg-white/10 text-white">[Esc]</kbd> Close Active Dialogs</div>
            <div><kbd class="px-1.5 py-0.5 rounded bg-white/10 text-white">[1-4 / A-D]</kbd> Select Quiz Options</div>
            <div><kbd class="px-1.5 py-0.5 rounded bg-white/10 text-white">[Enter]</kbd> Next Question</div>
          </div>
        </div>

      </div>

      <!-- TAB 3: AI ENGINE & API CONFIG -->
      <div id="pmodal-pane-ai" class="hidden space-y-5">
        <div>
          <label class="block text-xs font-mono text-gray-300 mb-1">GOOGLE GEMINI API KEY (OPTIONAL):</label>
          <input type="password" id="settings-gemini-key" placeholder="AIzaSy..." class="w-full rounded-xl bg-[#07080D] border border-white/10 focus:border-neonCyan p-3 text-xs font-mono text-white focus:outline-none focus:ring-1 focus:ring-neonCyan">
          <p class="text-[11px] text-gray-500 mt-1">
            Leave blank to use the built-in Intelligent Local Mock Engine (100% demo-ready for judges immediately).
          </p>
        </div>

        <div>
          <label class="block text-xs font-mono text-gray-300 mb-1">GEMINI MODEL TARGET:</label>
          <select id="settings-gemini-model" class="w-full rounded-xl bg-[#07080D] border border-white/10 focus:border-neonCyan p-3 text-xs font-mono text-white focus:outline-none">
            <option value="gemini-2.5-flash">gemini-2.5-flash (Fast &amp; Recommended)</option>
            <option value="gemini-1.5-flash">gemini-1.5-flash</option>
            <option value="gemini-1.5-pro">gemini-1.5-pro</option>
          </select>
        </div>

        <div class="p-3.5 rounded-xl bg-neonGreen/10 border border-neonGreen/30 text-xs font-mono text-neonGreen flex items-center gap-2">
          <span>●</span>
          <span>Dual Intelligence Architecture: Automatic fallback to Local Engine if network or API key is absent.</span>
        </div>
      </div>

      <!-- TAB 4: STATS & DATA MANAGEMENT -->
      <div id="pmodal-pane-stats" class="hidden space-y-5">
        
        <!-- Lifetime Stats -->
        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 text-center">
          <div class="p-3 rounded-xl bg-white/[0.02] border border-white/5">
            <div id="pmodal-stat-docs" class="font-outfit font-black text-xl text-white">0</div>
            <div class="text-[10px] font-mono text-gray-500 uppercase">Docs Parsed</div>
          </div>
          <div class="p-3 rounded-xl bg-white/[0.02] border border-white/5">
            <div id="pmodal-stat-quizzes" class="font-outfit font-black text-xl text-neonCyan">0</div>
            <div class="text-[10px] font-mono text-gray-500 uppercase">Quizzes Taken</div>
          </div>
          <div class="p-3 rounded-xl bg-white/[0.02] border border-white/5">
            <div id="pmodal-stat-weak" class="font-outfit font-black text-xl text-neonPink">0</div>
            <div class="text-[10px] font-mono text-gray-500 uppercase">Weak Spots Cleared</div>
          </div>
          <div class="p-3 rounded-xl bg-white/[0.02] border border-white/5">
            <div id="pmodal-stat-acc" class="font-outfit font-black text-xl text-neonGreen">0%</div>
            <div class="text-[10px] font-mono text-gray-500 uppercase">Avg Mastery</div>
          </div>
        </div>

        <!-- Data Actions -->
        <div class="flex flex-wrap items-center justify-between gap-3 p-4 rounded-2xl bg-white/[0.02] border border-white/5">
          <div>
            <div class="text-xs font-bold text-white">Export Study Progress Data</div>
            <div class="text-[11px] text-gray-400">Download your study documents and quiz scores as JSON.</div>
          </div>
          <button onclick="exportStudyDataJSON()" class="px-4 py-2 rounded-xl bg-white/5 hover:bg-white/10 text-neonCyan border border-neonCyan/30 text-xs font-mono transition-all">
            📥 Export JSON
          </button>
        </div>

        <div class="flex flex-wrap items-center justify-between gap-3 p-4 rounded-2xl bg-neonPink/[0.03] border border-neonPink/20">
          <div>
            <div class="text-xs font-bold text-neonPink">Clear Cache &amp; Reset Study History</div>
            <div class="text-[11px] text-gray-400">Resets local storage history, weak points queue, and cached statistics.</div>
          </div>
          <button onclick="resetAllStudyData()" class="px-4 py-2 rounded-xl bg-neonPink/10 hover:bg-neonPink/20 text-neonPink border border-neonPink/30 text-xs font-mono transition-all">
            ⚠️ Reset All Data
          </button>
        </div>

      </div>

      <!-- Modal Footer -->
      <div class="pt-4 border-t border-white/10 flex items-center justify-between">
        <div class="text-[11px] font-mono text-gray-500">
          EDU AI v2.0 • Hackathon Edition
        </div>
        <div class="flex gap-3">
          <button onclick="closeProfileSettingsModal()" class="px-4 py-2 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 text-xs font-mono">
            Cancel
          </button>
          <button onclick="saveProfileSettings()" class="px-6 py-2 rounded-xl bg-gradient-to-r from-neonGreen via-neonCyan to-neonPurple text-black font-outfit font-bold text-xs uppercase tracking-wider shadow-glow-cyan">
            Save Changes
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- ========================================== -->
  <!-- QUIZ CUSTOMIZATION MODAL (Difficulty & Count) -->
  <!-- ========================================== -->
  <div id="quiz-config-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden flex items-center justify-center p-4" onclick="if(event.target === this) closeQuizConfigModal()">
    <div class="relative w-full max-w-lg rounded-3xl glass-card border border-neonCyan/40 p-6 sm:p-8 space-y-6 shadow-[0_0_50px_rgba(0,229,255,0.25)] animate-scale" onclick="event.stopPropagation()">
      
      <!-- Modal Header with Back / Close Navigation -->
      <div class="flex items-center justify-between border-b border-white/10 pb-4">
        <div class="flex items-center gap-3">
          <button type="button" onclick="closeQuizConfigModal()" title="Back to Learning Modes" class="px-3 py-1.5 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-xs font-mono text-gray-300 hover:text-white flex items-center gap-1.5 transition-all">
            <span>←</span> <span>Back</span>
          </button>
          <div class="h-6 w-px bg-white/10"></div>
          <div>
            <h3 class="font-outfit font-black text-xl text-white">
              Customize Quiz
            </h3>
            <p class="text-xs font-mono text-gray-400">
              Calibrate question quantity, difficulty &amp; topic focus
            </p>
          </div>
        </div>
        <button type="button" onclick="closeQuizConfigModal()" title="Close" class="w-8 h-8 rounded-full bg-white/5 hover:bg-white/10 text-gray-400 hover:text-white flex items-center justify-center transition-colors">
          ✕
        </button>
      </div>

      <!-- Config Options -->
      <div class="space-y-6">

        <!-- 1. Number of Questions: 5, 10, 15, 20 -->
        <div class="space-y-2.5">
          <div class="flex items-center justify-between">
            <label class="text-xs font-mono uppercase tracking-wider text-neonCyan font-bold flex items-center gap-2">
              <span>🔢</span> <span>Number of Questions</span>
            </label>
            <span id="quiz-count-display-val" class="px-2.5 py-0.5 rounded-full text-xs font-mono font-bold bg-neonCyan/15 text-neonCyan border border-neonCyan/30">
              5 Questions
            </span>
          </div>

          <!-- Quick Select Buttons (5, 10, 15, 20) -->
          <div class="grid grid-cols-4 gap-2">
            <button type="button" onclick="setQuizCount(5)" data-count="5" class="quiz-count-btn active py-2.5 rounded-xl border border-neonCyan bg-neonCyan/15 text-xs font-mono font-bold text-neonCyan shadow-glow-cyan transition-all">
              5 <span class="text-[10px] text-neonCyan/80 block">Quick Check</span>
            </button>
            <button type="button" onclick="setQuizCount(10)" data-count="10" class="quiz-count-btn py-2.5 rounded-xl border border-white/10 bg-white/[0.02] text-xs font-mono font-semibold text-gray-300 hover:border-neonCyan hover:text-white transition-all">
              10 <span class="text-[10px] text-gray-500 block">Standard</span>
            </button>
            <button type="button" onclick="setQuizCount(15)" data-count="15" class="quiz-count-btn py-2.5 rounded-xl border border-white/10 bg-white/[0.02] text-xs font-mono font-semibold text-gray-300 hover:border-neonCyan hover:text-white transition-all">
              15 <span class="text-[10px] text-gray-500 block">In-Depth</span>
            </button>
            <button type="button" onclick="setQuizCount(20)" data-count="20" class="quiz-count-btn py-2.5 rounded-xl border border-white/10 bg-white/[0.02] text-xs font-mono font-semibold text-gray-300 hover:border-neonCyan hover:text-white transition-all">
              20 <span class="text-[10px] text-gray-500 block">Mock Exam</span>
            </button>
          </div>
          <p class="text-[11px] text-gray-400">
            Select how many questions you want generated from your current study notes (5, 10, 15, or 20).
          </p>
        </div>

        <!-- 2. Difficulty Level Selector -->
        <div class="space-y-2.5">
          <div class="flex items-center justify-between">
            <label class="text-xs font-mono uppercase tracking-wider text-neonPurple font-bold flex items-center gap-2">
              <span>⚡</span> <span>Cognitive Rigor / Difficulty</span>
            </label>
            <span id="quiz-diff-display-val" class="px-2.5 py-0.5 rounded-full text-xs font-mono font-bold bg-neonPurple/15 text-neonPurple border border-neonPurple/30">
              Medium
            </span>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
            
            <!-- Easy -->
            <button type="button" onclick="setQuizDifficulty('easy')" data-diff="easy" class="quiz-diff-btn p-3.5 rounded-2xl border border-white/10 bg-white/[0.02] text-left hover:border-neonGreen transition-all group flex flex-col justify-between">
              <div>
                <div class="flex items-center justify-between mb-1">
                  <span class="text-base">🌱</span>
                  <span class="text-[10px] font-mono text-neonGreen font-bold">FOUNDATIONAL</span>
                </div>
                <div class="font-outfit font-bold text-sm text-white group-hover:text-neonGreen">
                  Easy
                </div>
                <div class="text-[11px] text-gray-400 mt-1 leading-snug">
                  Direct definitions, formula identification &amp; core terminology.
                </div>
              </div>
            </button>

            <!-- Medium -->
            <button type="button" onclick="setQuizDifficulty('medium')" data-diff="medium" class="quiz-diff-btn active p-3.5 rounded-2xl border-2 border-neonCyan bg-neonCyan/10 text-left shadow-glow-cyan transition-all group flex flex-col justify-between">
              <div>
                <div class="flex items-center justify-between mb-1">
                  <span class="text-base">⚡</span>
                  <span class="text-[10px] font-mono text-neonCyan font-bold">BALANCED</span>
                </div>
                <div class="font-outfit font-bold text-sm text-white text-neonCyan">
                  Medium
                </div>
                <div class="text-[11px] text-gray-300 mt-1 leading-snug">
                  Conceptual application, cause-and-effect &amp; diagnostic reasoning.
                </div>
              </div>
            </button>

            <!-- Hard -->
            <button type="button" onclick="setQuizDifficulty('hard')" data-diff="hard" class="quiz-diff-btn p-3.5 rounded-2xl border border-white/10 bg-white/[0.02] text-left hover:border-neonPink transition-all group flex flex-col justify-between">
              <div>
                <div class="flex items-center justify-between mb-1">
                  <span class="text-base">🔥</span>
                  <span class="text-[10px] font-mono text-neonPink font-bold">EXAM CHALLENGE</span>
                </div>
                <div class="font-outfit font-bold text-sm text-white group-hover:text-neonPink">
                  Hard
                </div>
                <div class="text-[11px] text-gray-400 mt-1 leading-snug">
                  Multi-step edge cases, tricky distractors &amp; examiner traps.
                </div>
              </div>
            </button>

          </div>
        </div>

        <!-- 3. Target Syllabus Calibration Notice -->
        <div class="p-3.5 rounded-2xl bg-white/[0.02] border border-white/5 flex items-center justify-between gap-3 text-xs font-mono">
          <div class="flex items-center gap-2 text-gray-400">
            <span>🎓</span> <span>Target Level:</span> <strong id="quiz-config-target-level" class="text-white">Undergraduate</strong>
          </div>
          <button onclick="closeQuizConfigModal(); openLevelScreen();" class="text-neonCyan hover:underline text-[11px]">
            Change Level ➔
          </button>
        </div>

      </div>

      <!-- Modal Footer -->
      <div class="pt-4 border-t border-white/10 flex items-center justify-between">
        <button onclick="closeQuizConfigModal()" class="px-5 py-2.5 rounded-xl bg-white/5 hover:bg-white/10 text-gray-300 hover:text-white text-xs font-mono flex items-center gap-2 transition-all">
          <span>←</span> <span>Back to Learning Modes</span>
        </button>
        <button onclick="applyQuizConfigAndLaunch()" class="px-6 py-2.5 rounded-xl bg-gradient-to-r from-neonCyan to-neonGreen text-black font-outfit font-bold text-xs uppercase tracking-wider shadow-glow-cyan hover:brightness-110 transition-all flex items-center gap-2">
          <span>🚀 Start Custom Quiz</span>
        </button>
      </div>

    </div>
  </div>

  <!-- Footer -->
  <footer class="no-print mt-auto border-t border-white/5 py-6 bg-[#07080D]/60 text-center text-xs font-mono text-gray-500">
    <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-3">
      <div>
        ⚡ <strong class="text-gray-400">EDU AI</strong> — Hackathon Prototype for AI in Education
      </div>
      <div>
        100% Client-Side Ready • Powered by Heuristic &amp; Generative Intelligence
      </div>
    </div>
  </footer>

  <!-- ========================================== -->
  <!-- JAVASCRIPT APPLICATION LOGIC -->
  <!-- ========================================== -->
  <script>
    /* ===================================================
       1. CORE STATE MANAGEMENT
       =================================================== */
    const state = {
      level: localStorage.getItem('eduai_grade_level') || '',
      levelDesc: localStorage.getItem('eduai_grade_desc') || '',
      levelBadge: localStorage.getItem('eduai_grade_badge') || '🎓 Undergraduate',
      userName: localStorage.getItem('eduai_user_name') || 'Naruto Uzumaki',
      userAvatar: localStorage.getItem('eduai_user_avatar') || 'naruto',
      userCustomAvatar: localStorage.getItem('eduai_user_custom_avatar') || '',
      accentColor: localStorage.getItem('eduai_accent_color') || 'cyan',
      ttsRate: parseFloat(localStorage.getItem('eduai_tts_rate') || '1.0'),
      currentTab: 'file',
      docs: [], // { name, size, type, text, status }
      activeText: '',
      activeDocTitle: '',
      analyzedData: null,
      soundEnabled: localStorage.getItem('eduai_sound_enabled') !== 'false',
      geminiKey: localStorage.getItem('eduai_gemini_key') || '',
      geminiModel: localStorage.getItem('eduai_gemini_model') || 'gemini-2.5-flash',
      // Quiz Customization Preferences
      quizCount: parseInt(localStorage.getItem('eduai_quiz_count') || '5', 10),
      quizDifficulty: localStorage.getItem('eduai_quiz_difficulty') || 'medium',
      // Quiz & Weakness Tracking
      quiz: {
        activeQuestions: [],
        currentIndex: 0,
        score: 0,
        weakQueue: [],
        mastered: [],
        flaggedWeak: [],
        totalAnswered: 0
      },
      stats: {
        docsAnalyzed: parseInt(localStorage.getItem('eduai_stat_docs') || '0', 10),
        weakCleared: parseInt(localStorage.getItem('eduai_stat_weak') || '0', 10),
        quizzesTaken: parseInt(localStorage.getItem('eduai_stat_quizzes') || '0', 10),
        totalAccuracy: parseInt(localStorage.getItem('eduai_stat_acc') || '0', 10)
      }
    };

    /* ===================================================
       2. SYNTHESIZED WEB AUDIO SOUND ENGINE
       =================================================== */
    let audioCtx = null;
    function playTone(freq = 440, type = 'sine', duration = 0.1, gain = 0.08) {
      if (!state.soundEnabled) return;
      try {
        if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        if (audioCtx.state === 'suspended') audioCtx.resume();
        const osc = audioCtx.createOscillator();
        const g = audioCtx.createGain();
        osc.type = type;
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
        g.gain.setValueAtTime(gain, audioCtx.currentTime);
        g.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + duration);
        osc.connect(g);
        g.connect(audioCtx.destination);
        osc.start();
        osc.stop(audioCtx.currentTime + duration);
      } catch (_) {}
    }
    const sfx = {
      click: () => playTone(600, 'triangle', 0.04, 0.04),
      success: () => { playTone(523, 'sine', 0.08, 0.08); setTimeout(() => playTone(659, 'sine', 0.08, 0.08), 80); setTimeout(() => playTone(783, 'sine', 0.15, 0.09), 160); },
      error: () => { playTone(240, 'sawtooth', 0.1, 0.08); setTimeout(() => playTone(180, 'sawtooth', 0.15, 0.08), 90); },
      camera: () => { playTone(900, 'square', 0.03, 0.06); setTimeout(() => playTone(1200, 'sine', 0.06, 0.05), 40); },
      chime: () => { playTone(440, 'sine', 0.08, 0.06); setTimeout(() => playTone(880, 'sine', 0.15, 0.06), 90); }
    };

    /* ===================================================
       3. SPLASH SCREEN LIFECYCLE (2 Seconds Exact)
       =================================================== */
    const splashEl = document.getElementById('splash-screen');
    const splashProgress = document.getElementById('splash-progress');
    const levelScreen = document.getElementById('level-screen');

    // Start progress bar animation
    setTimeout(() => {
      if (splashProgress) splashProgress.style.width = '100%';
    }, 50);

    let splashCompleted = false;
    function finishSplashScreen() {
      if (splashCompleted) return;
      splashCompleted = true;
      sfx.chime();
      splashEl.style.opacity = '0';
      splashEl.style.transform = 'scale(1.05)';
      setTimeout(() => {
        splashEl.classList.add('hidden');
        if (!state.level) {
          openLevelScreen();
        } else {
          updateNavBadge();
          showScreen('screen-dashboard');
        }
      }, 600);
    }

    // Exactly 2000ms transition
    const splashTimer = setTimeout(finishSplashScreen, 2000);

    // Skip on click or spacebar
    document.getElementById('skip-splash-btn').onclick = () => {
      clearTimeout(splashTimer);
      finishSplashScreen();
    };
    splashEl.onclick = () => {
      clearTimeout(splashTimer);
      finishSplashScreen();
    };
    window.addEventListener('keydown', (e) => {
      if (e.code === 'Space' && !splashCompleted) {
        clearTimeout(splashTimer);
        finishSplashScreen();
      }
    });

    /* ===================================================
       4. GRADE / EDUCATION LEVEL ONBOARDING (2-Step Drilldown)
       =================================================== */
    const EDUCATION_LEVELS = {
      Undergraduate: {
        title: 'Undergraduate',
        icon: '🎓',
        tag: 'BACHELORS DEGREE',
        badgeColor: 'bg-neonCyan/10 text-neonCyan border-neonCyan/30',
        glowHover: 'hover:border-neonCyan hover:shadow-glow-cyan',
        desc: "Bachelor's degree courses — Engineering, Medicine, Science, Commerce, Law & Management.",
        subHeading: "Choose your Undergraduate Course",
        subDesc: "Calibrates engineering mechanisms, clinical diagnostics, and degree-level marking schemes.",
        items: [
          { id: 'Engineering (B.Tech / B.E.)', icon: '⚙️', desc: 'Computer Science, AI, Mechanical, Electrical, Civil, Electronics & all branches.' },
          { id: 'Medical (MBBS)', icon: '🩺', desc: 'Clinical Medicine, Anatomy, Physiology, Pathology & NEET-UG preparation.' },
          { id: 'BDS (Dental Surgery)', icon: '🦷', desc: 'Dental Sciences, Oral Pathology & Maxillofacial Surgery.' },
          { id: 'B.Pharm (Pharmacy)', icon: '💊', desc: 'Pharmaceutical Chemistry, Pharmacology & Drug Formulations.' },
          { id: 'B.Sc (Science)', icon: '🔬', desc: 'Physics, Chemistry, Mathematics, Botany, Zoology & Biotechnology.' },
          { id: 'BCA / B.Sc Computer Science', icon: '💻', desc: 'Software Engineering, Algorithms, Databases & Web Architecture.' },
          { id: 'B.Com (Commerce & Finance)', icon: '📊', desc: 'Accounting, Corporate Law, Auditing, Direct Tax & Economics.' },
          { id: 'BBA / BMS (Management)', icon: '🧭', desc: 'Business Strategy, Marketing, Organizational Behavior & Finance.' },
          { id: 'B.A. (Arts & Humanities)', icon: '📜', desc: 'Economics, Political Science, History, Psychology & Literature.' },
          { id: 'LLB (Law)', icon: '⚖️', desc: 'Constitutional Law, Criminal Law, Jurisprudence & Corporate Law.' },
          { id: 'B.Arch (Architecture)', icon: '🏛️', desc: 'Architectural Design, Structural Systems & Urban Planning.' }
        ]
      },
      Postgraduate: {
        title: 'Postgraduate',
        icon: '🔬',
        tag: 'MASTERS & DOCTORAL',
        badgeColor: 'bg-neonPurple/10 text-neonPurple border-neonPurple/30',
        glowHover: 'hover:border-neonPurple hover:shadow-glow-purple',
        desc: "Master's degrees, research doctorates & clinical surgical specializations.",
        subHeading: "Choose your Postgraduate Specialization",
        subDesc: "Calibrates advanced thesis depth, critical comparative analysis, and high-level research questions.",
        items: [
          { id: 'M.Tech / M.E.', icon: '⚙️', desc: 'Advanced Engineering, VLSI, Machine Learning, Robotics & Systems.' },
          { id: 'MD (Doctor of Medicine)', icon: '🩺', desc: 'General Medicine, Pediatrics, Radiodiagnosis & Clinical Specialties.' },
          { id: 'MS (Master of Surgery)', icon: '🏥', desc: 'General Surgery, Orthopedics, Ophthalmology, ENT & Operative Procedures.' },
          { id: 'MDS (Dental Specialization)', icon: '🦷', desc: 'Orthodontics, Periodontics, Prosthodontics & Oral Surgery.' },
          { id: 'M.Sc (Science Masters)', icon: '🧪', desc: 'Advanced Physics, Chemistry, Molecular Biology & Applied Mathematics.' },
          { id: 'MCA (Computer Applications)', icon: '💻', desc: 'Enterprise Systems, Distributed Cloud Computing, Cybersecurity & AI.' },
          { id: 'MBA (Business Administration)', icon: '📈', desc: 'Strategic Management, Quantitative Finance, Operations & Leadership.' },
          { id: 'M.Com (Commerce Masters)', icon: '📊', desc: 'Advanced Accounting, Financial Markets, International Taxation.' },
          { id: 'M.A. (Arts & Humanities)', icon: '📜', desc: 'Advanced Macroeconomics, International Relations, Public Policy.' },
          { id: 'LLM (Master of Laws)', icon: '⚖️', desc: 'Corporate Governance, Intellectual Property Rights, Cyber & International Law.' },
          { id: 'Ph.D (Doctoral Research)', icon: '🎓', desc: 'Original Dissertation, Scientific Methodologies & Scholarly Publications.' }
        ]
      },
      School: {
        title: 'School',
        icon: '🎒',
        tag: 'K-12 & BOARD EXAMS',
        badgeColor: 'bg-neonGreen/10 text-neonGreen border-neonGreen/30',
        glowHover: 'hover:border-neonGreen hover:shadow-glow-green',
        desc: "Classes 6 to 12 — Secondary & Senior Secondary Board Exams, JEE/NEET prep & Core Foundations.",
        subHeading: "Choose your Class / Grade",
        subDesc: "Calibrates syllabus terminology, board-marking step points, and student-friendly analogies.",
        items: [
          { id: 'Class 12', icon: '📚', desc: 'Senior Secondary Board Exam (CBSE/ISC/State) & JEE/NEET Entrance Prep.' },
          { id: 'Class 11', icon: '📘', desc: 'Senior Secondary Foundation, Core Physics, Chemistry, Biology & Math.' },
          { id: 'Class 10', icon: '📗', desc: 'Secondary Board Examination Focus, Science, Math & Core Concepts.' },
          { id: 'Class 9', icon: '📙', desc: 'Secondary Foundation, Matter, Motion, Cell Structure & Algebraic Geometry.' },
          { id: 'Class 8', icon: '📕', desc: 'Middle School Advanced Foundation, Rational Numbers & Science.' },
          { id: 'Class 7', icon: '✏️', desc: 'Middle School Core, Nutrition, Heat, Motion & Algebraic Expressions.' },
          { id: 'Class 6', icon: '🖍️', desc: 'Middle School Basics, Food, Components, Basic Geometry & Integers.' }
        ]
      }
    };

    let activeSelectedCategory = '';

    function selectCategory(catKey) {
      sfx.click();
      activeSelectedCategory = catKey;
      const data = EDUCATION_LEVELS[catKey];
      if (!data) return;

      document.getElementById('level-step-categories').classList.add('hidden');
      const subScreen = document.getElementById('level-step-suboptions');
      subScreen.classList.remove('hidden');

      // Update badge, heading and description
      const badge = document.getElementById('suboption-badge');
      badge.className = `px-3 py-1 rounded-full text-xs font-mono border ${data.badgeColor}`;
      badge.textContent = `${data.icon} ${data.title}`;

      document.getElementById('suboption-heading').textContent = data.subHeading;
      document.getElementById('suboption-subtext').textContent = data.subDesc;

      // Populate suboptions grid
      const grid = document.getElementById('suboptions-grid');
      grid.innerHTML = data.items.map(item => `
        <button class="group p-4 rounded-2xl glass-card border border-white/10 ${data.glowHover} text-left transition-all duration-200 transform hover:-translate-y-1 focus:outline-none flex flex-col justify-between"
          onclick="selectSubLevel('${catKey}', '${escapeHTML(item.id)}', '${item.icon}', '${escapeHTML(item.desc)}')">
          <div>
            <div class="flex items-center justify-between mb-2">
              <span class="text-2xl">${item.icon}</span>
              <span class="text-[10px] font-mono text-gray-500 group-hover:text-white">SELECT</span>
            </div>
            <h4 class="font-outfit font-bold text-base text-white group-hover:text-neonCyan transition-colors">
              ${escapeHTML(item.id)}
            </h4>
            <p class="text-xs text-gray-400 mt-1 line-clamp-2 leading-relaxed">
              ${escapeHTML(item.desc)}
            </p>
          </div>
          <div class="mt-3 pt-2 border-t border-white/5 flex items-center justify-between text-[11px] font-mono text-gray-500 group-hover:text-neonCyan">
            <span>Calibrate Tone &amp; Rigor</span>
            <span>➔</span>
          </div>
        </button>
      `).join('');
    }

    function backToCategories() {
      sfx.click();
      document.getElementById('level-step-suboptions').classList.add('hidden');
      document.getElementById('level-step-categories').classList.remove('hidden');
    }

    function selectSubLevel(category, subId, icon, desc) {
      state.level = `${category} - ${subId}`;
      state.levelBadge = `${icon} ${subId}`;
      state.levelDesc = desc;

      localStorage.setItem('eduai_grade_level', state.level);
      localStorage.setItem('eduai_grade_badge', state.levelBadge);
      localStorage.setItem('eduai_grade_desc', state.levelDesc);
      localStorage.setItem('eduai_grade_category', category);

      updateNavBadge();
      closeLevelScreen();
      showScreen('screen-dashboard');
      sfx.success();
    }

    function openLevelScreen() {
      sfx.click();
      const closeBtn = document.getElementById('level-close-btn');
      if (state.level) {
        closeBtn.classList.remove('hidden');
      } else {
        closeBtn.classList.add('hidden');
      }
      document.getElementById('level-step-suboptions').classList.add('hidden');
      document.getElementById('level-step-categories').classList.remove('hidden');
      levelScreen.classList.remove('hidden');
    }

    function closeLevelScreen() {
      sfx.click();
      levelScreen.classList.add('hidden');
    }

    function updateNavBadge() {
      const badgeText = document.getElementById('nav-grade-text');
      if (badgeText) badgeText.textContent = state.levelBadge || '🎓 Undergraduate';
      const modeLabel = document.getElementById('mode-grade-label');
      if (modeLabel) modeLabel.textContent = state.level || 'Undergraduate';
      const summaryBadge = document.getElementById('summary-grade-badge');
      if (summaryBadge) summaryBadge.textContent = 'Calibrated for ' + (state.level || 'Undergraduate');
      const supernotesBadge = document.getElementById('supernotes-grade-tag');
      if (supernotesBadge) supernotesBadge.textContent = 'Calibrated for ' + (state.level || 'Undergraduate');
      const mindmapBadge = document.getElementById('mindmap-grade-badge');
      if (mindmapBadge) mindmapBadge.textContent = 'Calibrated for ' + (state.level || 'Undergraduate');
    }

    document.getElementById('nav-grade-badge').onclick = openLevelScreen;

    /* ===================================================
       5. NAVIGATION & SCREEN MANAGER
       =================================================== */
    const SCREENS = ['screen-dashboard', 'screen-modes', 'screen-summary', 'screen-quiz', 'screen-supernotes', 'screen-mindmap'];
    function showScreen(screenId) {
      SCREENS.forEach(id => {
        const el = document.getElementById(id);
        if (el) {
          if (id === screenId) {
            el.classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
          } else {
            el.classList.add('hidden');
          }
        }
      });
      // Stop TTS if navigating away from summary
      if (screenId !== 'screen-summary' && isSpeaking) {
        stopAudioSpeech();
      }
    }

    function navigateHome() {
      sfx.click();
      if (state.activeText) {
        showScreen('screen-modes');
      } else {
        showScreen('screen-dashboard');
      }
    }
    function navigateDashboard() { sfx.click(); showScreen('screen-dashboard'); }
    function navigateModes() { sfx.click(); showScreen('screen-modes'); }

    /* ===================================================
       6. MULTI-MODAL DOCUMENT INPUTS
       =================================================== */
    function switchInputTab(tab) {
      sfx.click();
      state.currentTab = tab;
      
      const tabFile = document.getElementById('tab-btn-file');
      const tabCam = document.getElementById('tab-btn-camera');
      const tabPaste = document.getElementById('tab-btn-paste');

      const paneFile = document.getElementById('tab-pane-file');
      const paneCam = document.getElementById('tab-pane-camera');
      const panePaste = document.getElementById('tab-pane-paste');

      [tabFile, tabCam, tabPaste].forEach(t => {
        t.className = 'tab-trigger flex-1 min-w-[140px] flex items-center justify-center gap-2 py-3 px-4 rounded-xl text-xs sm:text-sm font-outfit font-semibold transition-all text-gray-400 hover:text-white hover:bg-white/5 border border-transparent';
      });

      const activeClasses = 'tab-trigger active flex-1 min-w-[140px] flex items-center justify-center gap-2 py-3 px-4 rounded-xl text-xs sm:text-sm font-outfit font-semibold transition-all bg-neonCyan/15 text-neonCyan border border-neonCyan/40 shadow-glow-cyan';

      paneFile.classList.add('hidden');
      paneCam.classList.add('hidden');
      panePaste.classList.add('hidden');

      if (tab === 'file') {
        tabFile.className = activeClasses;
        paneFile.classList.remove('hidden');
      } else if (tab === 'camera') {
        tabCam.className = activeClasses;
        paneCam.classList.remove('hidden');
      } else if (tab === 'paste') {
        tabPaste.className = activeClasses;
        panePaste.classList.remove('hidden');
      }
    }

    // --- Tab 1: File Drag & Drop ---
    const dropZone = document.getElementById('drop-zone');
    const fileInput = document.getElementById('file-input');

    dropZone.onclick = () => fileInput.click();
    fileInput.onchange = () => { handleFiles(fileInput.files); fileInput.value = ''; };

    ['dragenter', 'dragover'].forEach(name => {
      dropZone.addEventListener(name, e => {
        e.preventDefault();
        dropZone.classList.add('border-neonCyan', 'bg-neonCyan/[0.08]');
      });
    });
    ['dragleave', 'drop'].forEach(name => {
      dropZone.addEventListener(name, e => {
        e.preventDefault();
        dropZone.classList.remove('border-neonCyan', 'bg-neonCyan/[0.08]');
      });
    });
    dropZone.addEventListener('drop', e => {
      if (e.dataTransfer && e.dataTransfer.files.length) {
        handleFiles(e.dataTransfer.files);
      }
    });

    async function handleFiles(fileList) {
      sfx.click();
      const files = Array.from(fileList);
      for (const file of files) {
        const docItem = {
          name: file.name,
          size: (file.size / 1024).toFixed(1) + ' KB',
          type: file.type || file.name.split('.').pop(),
          text: '',
          status: 'reading'
        };
        state.docs.push(docItem);
        renderFileQueue();

        try {
          const text = await extractFileText(file);
          docItem.text = text;
          docItem.status = text.trim().length > 10 ? 'ready' : 'empty';
        } catch (err) {
          console.error('File parsing error:', err);
          docItem.status = 'error';
        }
        renderFileQueue();
      }
      updateDocSummaryBar();
    }

    async function extractFileText(file) {
      const lower = file.name.toLowerCase();
      // Plain text / Markdown
      if (lower.endsWith('.txt') || lower.endsWith('.md')) {
        return await file.text();
      }
      // Word DOCX parser
      if (lower.endsWith('.docx')) {
        await loadDynamicScript('https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.6.0/mammoth.browser.min.js');
        const buffer = await file.arrayBuffer();
        const result = await window.mammoth.extractRawText({ arrayBuffer: buffer });
        return result.value || '';
      }
      // PDF.js parser
      if (lower.endsWith('.pdf')) {
        await loadDynamicScript('https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js');
        window.pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';
        const buffer = await file.arrayBuffer();
        const pdf = await window.pdfjsLib.getDocument({ data: buffer }).promise;
        let fullText = '';
        for (let i = 1; i <= pdf.numPages; i++) {
          const page = await pdf.getPage(i);
          const content = await page.getTextContent();
          fullText += content.items.map(it => it.str).join(' ') + '\n';
        }
        return fullText;
      }
      // Image fallback to OCR or raw name
      return await file.text().catch(() => 'Study material excerpt from: ' + file.name);
    }

    function renderFileQueue() {
      const container = document.getElementById('file-queue-container');
      const list = document.getElementById('file-queue-list');
      const count = document.getElementById('queue-count');
      if (!state.docs.length) {
        container.classList.add('hidden');
        return;
      }
      container.classList.remove('hidden');
      count.textContent = state.docs.length;

      list.innerHTML = state.docs.map((d, idx) => `
        <div class="flex items-center justify-between p-3 rounded-xl glass-card border border-white/5 text-xs">
          <div class="flex items-center gap-3">
            <span class="text-base">📄</span>
            <div>
              <div class="font-outfit font-bold text-white">${escapeHTML(d.name)}</div>
              <div class="text-[11px] text-gray-500 font-mono">${d.size} • ${
                d.status === 'ready' ? '<span class="text-neonGreen">✓ Ready</span>' :
                d.status === 'reading' ? '<span class="text-neonCyan animate-pulse">Reading...</span>' :
                '<span class="text-neonPink">⚠ Text minimal</span>'
              }</div>
            </div>
          </div>
          <button onclick="removeFile(${idx})" class="text-gray-500 hover:text-neonPink p-1 transition-colors">✕</button>
        </div>
      `).join('');
    }

    function removeFile(idx) {
      sfx.click();
      state.docs.splice(idx, 1);
      renderFileQueue();
      updateDocSummaryBar();
    }
    function clearFiles() {
      sfx.click();
      state.docs = [];
      renderFileQueue();
      updateDocSummaryBar();
    }

    // --- Tab 2: Live Camera & Snapshot ---
    let cameraStream = null;
    let cameraFacing = 'environment';
    const videoFeed = document.getElementById('webcam-feed');
    const cameraIdleView = document.getElementById('camera-idle-view');
    const cameraControls = document.getElementById('camera-controls');
    const cameraHud = document.getElementById('camera-hud');

    async function initCamera() {
      sfx.click();
      try {
        if (cameraStream) stopCamera();
        cameraStream = await navigator.mediaDevices.getUserMedia({
          video: { facingMode: cameraFacing, width: { ideal: 1280 }, height: { ideal: 720 } }
        });
        videoFeed.srcObject = cameraStream;
        videoFeed.classList.remove('hidden');
        cameraIdleView.classList.add('hidden');
        cameraControls.classList.remove('hidden');
        cameraHud.classList.remove('hidden');
        sfx.chime();
      } catch (err) {
        alert('Webcam permission not granted or device not supported. Falling back to file upload.');
        document.getElementById('camera-file-fallback').click();
      }
    }

    function stopCamera() {
      if (cameraStream) {
        cameraStream.getTracks().forEach(t => t.stop());
        cameraStream = null;
      }
      videoFeed.classList.add('hidden');
      cameraIdleView.classList.remove('hidden');
      cameraControls.classList.add('hidden');
      cameraHud.classList.remove('hidden');
      cameraHud.classList.add('hidden');
    }

    function toggleCameraFacing() {
      sfx.click();
      cameraFacing = cameraFacing === 'environment' ? 'user' : 'environment';
      document.getElementById('camera-mode-label').textContent = cameraFacing.toUpperCase() + ' MODE';
      initCamera();
    }

    function captureSnapshot() {
      sfx.camera();
      const canvas = document.getElementById('snapshot-canvas');
      canvas.width = videoFeed.videoWidth || 640;
      canvas.height = videoFeed.videoHeight || 480;
      const ctx = canvas.getContext('2d');
      ctx.drawImage(videoFeed, 0, 0, canvas.width, canvas.height);
      
      // Stop camera and attach as document
      stopCamera();
      const simulatedText = `[Camera Snapshot Analysis - ${new Date().toLocaleTimeString()}]
Key Notes on Reaction Kinetics and Energy Transformations:
1. Photosynthesis light reactions split water: 2H2O -> 4H+ + 4e- + O2.
2. ATP and NADPH are synthesized to drive the Calvin cycle in the stroma.
3. Rubisco fixes CO2 into 3-phosphoglycerate (3-PGA).
4. Limiting factors include light intensity, CO2 concentration, and optimal enzyme temperature.`;

      state.docs.push({
        name: 'Camera-Snapshot-' + Date.now() + '.jpg',
        size: 'Snapshot Image',
        type: 'image/jpeg',
        text: simulatedText,
        status: 'ready'
      });
      renderFileQueue();
      switchInputTab('file');
      updateDocSummaryBar();
      sfx.success();
    }

    function handleImageFile(input) {
      if (input.files && input.files[0]) {
        handleFiles([input.files[0]]);
        switchInputTab('file');
      }
    }

    // --- Tab 3: Paste Text & Presets ---
    const pasteInput = document.getElementById('paste-input');
    const wordCountBadge = document.getElementById('word-count-badge');
    const charCountBadge = document.getElementById('char-count-badge');

    pasteInput.addEventListener('input', () => {
      const text = pasteInput.value.trim();
      const words = text ? text.split(/\s+/).length : 0;
      wordCountBadge.textContent = words + ' words';
      charCountBadge.textContent = text.length + ' chars';
      updateDocSummaryBar();
    });

    const PRESETS = {
      bio: `Photosynthesis is the fundamental biological process through which green plants, algae, and cyanobacteria convert radiant solar energy into chemical energy stored in carbohydrates. The process predominantly occurs within the specialized thylakoid membranes and stroma of chloroplasts in plant leaf mesophyll cells.

The overall balanced chemical reaction is:
6CO2 + 6H2O + light energy -> C6H12O6 + 6O2

The mechanism comprises two interconnected phases:
1. Light-Dependent Reactions: Take place in the thylakoid membranes. Chlorophyll a and accessory pigments absorb photons, primarily in the blue (430 nm) and red (660 nm) wavelengths, exciting electrons. Water molecules undergo photolysis: 2H2O -> 4H+ + 4e- + O2, generating molecular oxygen as a crucial by-product. Excited electrons traverse an electron transport chain (ETC), establishing a proton gradient across the thylakoid lumen that drives ATP synthase to produce ATP, while ferredoxin-NADP+ reductase reduces NADP+ into NADPH.

2. Light-Independent Reactions (Calvin-Benson Cycle): Occur in the fluid stroma. Carbon fixation is catalyzed by the enzyme Ribulose-1,5-bisphosphate carboxylase-oxygenase (Rubisco), joining CO2 to a 5-carbon sugar (RuBP) to yield 3-phosphoglycerate (3-PGA). ATP and NADPH from the light stage reduce 3-PGA into glyceraldehyde-3-phosphate (G3P), which recombines to regenerate RuBP and synthesize glucose.

Limiting factors follow Blackman's Law of Limiting Factors: light saturation point, carbon dioxide concentration, and temperature-dependent enzymatic denaturations. Respiration is the reciprocal catabolic pathway: C6H12O6 + 6O2 -> 6CO2 + 6H2O + 36-38 ATP.`,

      physics: `Newtonian Mechanics and Universal Gravitation govern the kinematics and dynamics of macroscopic physical bodies under gravitational and mechanical forces.

Newton's Three Laws of Motion:
1. First Law (Inertia): An object remains at rest or in uniform motion along a straight line unless acted upon by a non-zero net external force: Sigma F = 0 => dv/dt = 0.
2. Second Law (Force and Acceleration): The net applied force equals the rate of change of linear momentum: F_net = dp/dt = m*a (for invariant mass).
3. Third Law (Action-Reaction): For every interaction, forces between two bodies are equal in magnitude and opposite in direction: F_AB = -F_BA.

Newton's Law of Universal Gravitation states that any two point masses attract each other with a force directly proportional to the product of their masses and inversely proportional to the square of their distance:
F_g = G * (m1 * m2) / r^2
where G is the Universal Gravitational Constant: G = 6.67430 x 10^-11 N m^2 kg^-2.

Gravitational potential energy between two spherical masses: U(r) = -G * (m1 * m2) / r.
Escape velocity from a celestial body of mass M and radius R: v_esc = sqrt(2 * G * M / R).
Centripetal force sustaining orbital motion: F_c = m * v^2 / r = G * M * m / r^2, yielding Kepler's Third Law: T^2 = (4 * pi^2 / (G * M)) * r^3.`,

      cs: `Relational Database Normalization and ACID Transaction Architecture ensure data integrity, eliminate anomalies, and support concurrent distributed operations.

Database Normalization Levels:
- First Normal Form (1NF): Requires atomic, indivisible column values with no repeating groups or composite arrays.
- Second Normal Form (2NF): Must satisfy 1NF, and all non-key attributes must be fully functionally dependent on the entire primary key, eliminating partial dependencies.
- Third Normal Form (3NF): Must satisfy 2NF, and no non-prime attribute may be transitively dependent on another non-prime attribute (X -> Y and Y -> Z disallowed).
- Boyce-Codd Normal Form (BCNF): For every functional dependency X -> Y, X must be a superkey.

ACID Transaction Principles:
1. Atomicity: Transactions are all-or-nothing units of work; any failure triggers an immediate ROLLBACK.
2. Consistency: Transactions must transition the database from one valid integrity state to another, upholding all constraints.
3. Isolation: Concurrent execution produces the same state as serial execution, managed through Two-Phase Locking (2PL) or Multi-Version Concurrency Control (MVCC).
4. Durability: Once a transaction issues a COMMIT, modifications persist permanently in Write-Ahead Logs (WAL) even through power failures.

Indexing Mechanisms: B+ Trees maintain balanced logarithmic search complexity O(log N) for range and equality scans, while Hash Indexes offer O(1) equality lookup.`
    };

    function loadSamplePreset(key) {
      sfx.click();
      switchInputTab('paste');
      pasteInput.value = PRESETS[key] || '';
      pasteInput.dispatchEvent(new Event('input'));
      sfx.success();
    }

    // --- Ingestion Status Checker ---
    function updateDocSummaryBar() {
      const pasteText = pasteInput.value.trim();
      const readyDocs = state.docs.filter(d => d.status === 'ready');
      const hasContent = pasteText.length > 20 || readyDocs.length > 0;

      const indicator = document.getElementById('doc-status-indicator');
      const title = document.getElementById('doc-summary-title');
      const meta = document.getElementById('doc-summary-meta');
      const btn = document.getElementById('analyze-doc-btn');

      if (hasContent) {
        indicator.className = 'w-3 h-3 rounded-full bg-neonGreen animate-pulse shadow-glow-green';
        btn.disabled = false;
        
        if (readyDocs.length > 0) {
          title.textContent = `${readyDocs.length} Document(s) Ready for AI Parsing`;
          meta.textContent = `Includes: ${readyDocs.map(d => d.name).slice(0, 2).join(', ')}${readyDocs.length > 2 ? '...' : ''}`;
        } else {
          const words = pasteText.split(/\s+/).length;
          title.textContent = `Pasted Study Text Ready (${words} Words)`;
          meta.textContent = `Estimated analysis time: < 1 second`;
        }
      } else {
        indicator.className = 'w-3 h-3 rounded-full bg-gray-600';
        title.textContent = 'No Document Loaded Yet';
        meta.textContent = 'Upload files, snap a photo, or load a sample preset above.';
        btn.disabled = true;
      }
    }

    /* ===================================================
       7. AI ANALYSIS ENGINE (Intelligent Local Heuristic + Gemini)
       =================================================== */
    async function analyzeDocument() {
      sfx.click();
      const btn = document.getElementById('analyze-doc-btn');
      const spinner = document.getElementById('analyze-spinner');
      const btnText = document.getElementById('analyze-btn-text');

      btn.disabled = true;
      spinner.classList.remove('hidden');
      btnText.textContent = 'Parsing Cognitive Nodes...';

      // Aggregate text
      let combinedText = '';
      if (pasteInput.value.trim().length > 20) {
        combinedText = pasteInput.value.trim();
        state.activeDocTitle = 'Pasted Lecture Notes';
      } else {
        const readyDocs = state.docs.filter(d => d.status === 'ready');
        combinedText = readyDocs.map(d => d.text).join('\n\n');
        state.activeDocTitle = readyDocs[0] ? readyDocs[0].name.replace(/\.[^/.]+$/, '') : 'Lecture Notes';
      }
      state.activeText = combinedText;

      try {
        // Run AI synthesis (Gemini if key exists, else intelligent deterministic local engine)
        state.analyzedData = await runAISynthesis(state.activeText, state.level);
        
        // Update stats
        state.stats.docsAnalyzed++;
        localStorage.setItem('eduai_stat_docs', state.stats.docsAnalyzed);
        document.getElementById('stat-docs').textContent = `${state.stats.docsAnalyzed} Docs`;

        // Update breadcrumb
        document.getElementById('active-doc-title').textContent = state.activeDocTitle;
        document.getElementById('active-doc-words').textContent = combinedText.split(/\s+/).length + ' Words';

        sfx.success();
        showScreen('screen-modes');
      } catch (err) {
        console.error('Analysis error:', err);
        alert('Analysis error: ' + err.message);
      } finally {
        spinner.classList.add('hidden');
        btnText.textContent = '⚡ Analyze Document';
        btn.disabled = false;
      }
    }

    async function runAISynthesis(text, grade) {
      // If user supplied Gemini API key, attempt live Gemini 2.5 Flash query
      if (state.geminiKey) {
        try {
          return await callGeminiAPI(text, grade);
        } catch (e) {
          console.warn('Gemini API call failed, falling back to Local Heuristic Engine:', e);
        }
      }
      // Built-in intelligent local heuristic parser
      return runLocalHeuristicEngine(text, grade);
    }

    async function callGeminiAPI(text, grade) {
      const prompt = `You are EDU AI, a world-class cognitive study assistant.
Target Education Level: ${grade}.
Study Text:
"""
${text.slice(0, 15000)}
"""

Generate a strictly valid JSON response containing structured study tools for this student:
{
  "executiveSummary": "3-4 crisp sentences summarizing the core thesis and practical significance.",
  "bullets": ["5-7 high-yield takeaways written with clear bullet items"],
  "formulas": [{"name": "Formula Name", "equation": "e.g. 6CO2 + 6H2O -> C6H12O6 + 6O2", "variables": "Explanation of terms/variables"}],
  "glossary": [{"term": "Term", "def": "Concise definition"}],
  "mnemonics": [{"hook": "Mnemonic Hook/Acronym", "meaning": "What each letter represents", "context": "How it helps"}],
  "examTraps": [{"trap": "Common Student Misconception", "correction": "Correct concept & examiner tip"}],
  "quickRevision": ["4 rapid 1-line cram points"],
  "quizQuestions": [
    {
      "difficulty": "easy | medium | hard",
      "question": "Clear multiple choice question calibrated to difficulty level",
      "options": ["Option A", "Option B", "Option C", "Option D"],
      "answer": 0,
      "topic": "Specific Sub-concept Name",
      "explanation": "In-depth rationale of why option A is correct and why B, C, D are misconceptions."
    }
  ],
  "examQA": [
    {"marks": 1, "q": "Short 1-mark definition question", "a": "Direct model answer"},
    {"marks": 3, "q": "3-mark conceptual question", "a": "Step-marked model answer points"},
    {"marks": 5, "q": "5-mark comprehensive question", "a": "Detailed structured answer"}
  ],
  "mindmap": {
    "central": {
      "title": "Central Subject Name",
      "subtitle": "Short 3-5 word core theme",
      "takeaway": "1-line synthesis of the entire system"
    },
    "branches": [
      {
        "id": "branch-1",
        "side": "left",
        "position": "top-left",
        "color": "cyan",
        "icon": "💬",
        "title": "Foundational Concept",
        "subtitle": "Core definition and prerequisites",
        "takeaway": "High-yield exam rule for this branch",
        "connections": ["Kinetics", "Derivations"]
      },
      {
        "id": "branch-2",
        "side": "left",
        "position": "mid-left",
        "color": "blue",
        "icon": "🧩",
        "title": "Kinetics & Dynamics",
        "subtitle": "Rates, thresholds and catalysts",
        "takeaway": "Key rate-limiting condition",
        "connections": ["Foundations", "Mechanisms"]
      },
      {
        "id": "branch-3",
        "side": "left",
        "position": "bottom-left",
        "color": "purple",
        "icon": "🎯",
        "title": "Mechanisms & Pathways",
        "subtitle": "Step-by-step transformations",
        "takeaway": "Intermediate states often tested",
        "connections": ["Kinetics", "Equilibrium"]
      },
      {
        "id": "branch-4",
        "side": "right",
        "position": "top-right",
        "color": "green",
        "icon": "🌿",
        "title": "Equations & Derivations",
        "subtitle": "Governing mathematical models",
        "takeaway": "Units and boundary values",
        "connections": ["Foundations", "Equilibrium"]
      },
      {
        "id": "branch-5",
        "side": "right",
        "position": "mid-right",
        "color": "pink",
        "icon": "🎯",
        "title": "Equilibrium & Stability",
        "subtitle": "Reversible states and laws",
        "takeaway": "Thermodynamic criterion",
        "connections": ["Mechanisms", "Applications"]
      },
      {
        "id": "branch-6",
        "side": "right",
        "position": "bottom-right",
        "color": "yellow",
        "icon": "⚖️",
        "title": "Applications & Cases",
        "subtitle": "Clinical, practical or lab uses",
        "takeaway": "Practical evaluation criteria",
        "connections": ["Equilibrium", "Foundations"]
      }
    ]
  }
}
Generate at least 8-10 diverse quiz questions spanning easy, medium, and hard difficulty, and the mindmap knowledge graph. Return ONLY valid JSON.`;

      const resp = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/${state.geminiModel}:generateContent?key=${state.geminiKey}`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
      });
      if (!resp.ok) throw new Error('Gemini API responded with status ' + resp.status);
      const json = await resp.json();
      const rawText = json.candidates[0].content.parts[0].text;
      const cleanJson = rawText.replace(/```json/gi, '').replace(/```/g, '').trim();
      return JSON.parse(cleanJson);
    }

    // --- Deterministic Intelligent Local Engine ---
    function runLocalHeuristicEngine(text, grade) {
      const sentences = text.match(/[^.!?]+[.!?]+/g) || [text];
      const cleanSentences = sentences.map(s => s.trim()).filter(s => s.length > 25);
      
      // Extract key terms
      const stopWords = new Set(['these','those','their','there','about','which','where','while','could','would','should','other','after','under','using','between','first','second','third','process','occurs','takes','place','water','energy','state']);
      const wordCounts = {};
      const words = (text.match(/[A-Za-z]{4,}/g) || []).map(w => w.toLowerCase());
      words.forEach(w => {
        if (!stopWords.has(w)) wordCounts[w] = (wordCounts[w] || 0) + 1;
      });
      const topKeywords = Object.keys(wordCounts).sort((a,b) => wordCounts[b] - wordCounts[a]).slice(0, 10);

      // Detect Equations / Reactions
      const formulaCandidates = cleanSentences.filter(s => /(=|->|<-|\+|x10|\^|sqrt|pi|\bforce\b|\brate\b)/i.test(s)).slice(0, 4);
      const formulas = formulaCandidates.length ? formulaCandidates.map((f, i) => ({
        name: `Key Relationship ${i + 1}`,
        equation: f.length > 90 ? f.slice(0, 85) + '...' : f,
        variables: `Variables calibrated for ${grade} syllabus and exam requirements.`
      })) : [
        { name: "Rate Constant Kinetics", equation: "k = A * e^(-Ea / (R*T))", variables: "A = Frequency factor, Ea = Activation energy, T = Absolute temperature" },
        { name: "Energy Conservation", equation: "Delta U = Q - W", variables: "Delta U = Internal energy change, Q = Heat added, W = Work done" }
      ];

      // Build Executive Summary
      const firstChunk = cleanSentences.slice(0, 3).join(' ');
      const executiveSummary = firstChunk.length > 60 ? firstChunk : text.slice(0, 240) + '...';

      // Build Bullets
      const bullets = cleanSentences.slice(1, 7).map(s => s.replace(/^\d+[\.\)]\s*/, ''));

      // Build Glossary
      const glossary = topKeywords.slice(0, 6).map(w => {
        const matchingSentence = cleanSentences.find(s => s.toLowerCase().includes(w)) || `Critical concept in ${grade} curriculum.`;
        return {
          term: capitalize(w),
          def: matchingSentence.slice(0, 110) + (matchingSentence.length > 110 ? '...' : '')
        };
      });

      // Build Mnemonics
      const acronymLetters = topKeywords.slice(0, 4).map(w => w[0].toUpperCase()).join('');
      const mnemonics = [
        {
          hook: acronymLetters || "FAST",
          meaning: topKeywords.slice(0, 4).map(w => `${w[0].toUpperCase()} = ${capitalize(w)}`).join(' • '),
          context: `Memory hook linking the 4 highest frequency concepts in your notes.`
        },
        {
          hook: "CORE-3",
          meaning: "Concept • Operation • Result",
          context: "Standard framework to write high-scoring answers without omitting step marks."
        }
      ];

      // Build Exam Traps
      const examTraps = [
        {
          trap: `Confusing ${capitalize(topKeywords[0] || 'primary mechanism')} with its reverse pathway.`,
          correction: `Always specify reaction conditions, directionality, and energetic requirements in board evaluations.`
        },
        {
          trap: "Missing units or omitting equilibrium arrows in final statements.",
          correction: "Examiners deduct 1/2 to 1 mark if state symbols or stoichiometric balancing is omitted."
        }
      ];

      // Build Quick Revision Cram Bullets
      const quickRevision = cleanSentences.slice(0, 4).map(s => {
        const parts = s.split(/[,;]/);
        return parts[0].trim();
      });

      // Build Adaptive Diagnostic Quiz Questions Pool (Categorized by Difficulty)
      const baseKeywords = topKeywords.length ? topKeywords : ['principles', 'systems', 'energy', 'equations', 'variables', 'pathways'];
      const kw0 = capitalize(baseKeywords[0] || 'Core Mechanism');
      const kw1 = capitalize(baseKeywords[1] || 'Kinetics & Factors');
      const kw2 = capitalize(baseKeywords[2] || 'Energy Transformations');
      const kw3 = capitalize(baseKeywords[3] || 'Analytical Derivations');
      const kw4 = capitalize(baseKeywords[4] || 'Systems Equilibrium');
      const kw5 = capitalize(baseKeywords[5] || 'Experimental Controls');

      const s0 = cleanSentences[0] || "It establishes direct conversion of input potential into observable systematic output.";
      const s1 = cleanSentences[1] || "The governing kinetics depend strictly on ambient state parameters and reaction thresholds.";
      const s2 = cleanSentences[2] || "Intermediate state transfers stabilize transient fluctuations across connected pathways.";
      const s3 = cleanSentences[3] || "Conserved quantities remain strictly invariant under isolated boundary conditions.";

      const quizQuestions = [
        // --- EASY / FOUNDATIONAL (Direct definitions, fundamental facts, core terms) ---
        {
          difficulty: 'easy',
          question: `[Foundational] What is the primary definition of ${kw0} based on your study material?`,
          options: [
            s0.length > 95 ? s0.slice(0, 92) + '...' : s0,
            `A purely hypothetical conjecture with no observable physical or biological consequence.`,
            `An irreversible decay into disorganized noise violating all known conservation laws.`,
            `An instantaneous step occurring without any time interval or intermediate mechanism.`
          ],
          answer: 0,
          topic: kw0,
          explanation: `Option A directly reflects the foundational definition given in your study material: "${s0.slice(0, 110)}". In basic examinations, identifying the exact definition yields instant marks without confusing it with non-physical distractors.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] Which term refers to the foundational regulatory factor influencing "${kw1}"?`,
          options: [
            `Substrate availability, state temperatures, and governing concentration limits.`,
            `Complete absence of external matter and total atmospheric vacuum.`,
            `Infinite constant acceleration requiring zero input energy.`,
            `Permanent random fluctuation with zero statistical predictability.`
          ],
          answer: 0,
          topic: kw1,
          explanation: `In ${grade} curriculums, ${kw1} is fundamentally regulated by concentrations, temperatures, and catalytic activity. Distractors represent physically impossible states.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] What is the role of key terminology such as "${kw2}" in this topic?`,
          options: [
            `It describes the active energy or structural transfer vehicle throughout the cycle.`,
            `It is an archaic symbol used exclusively in historical alchemy.`,
            `It signifies a state where all chemical and physical reactions cease permanently.`,
            `It represents an arbitrary constant that cancels out of every calculation.`
          ],
          answer: 0,
          topic: kw2,
          explanation: `Key terms like ${kw2} identify the active transfer pathway in your material. Remembering the core vocabulary is the easiest way to secure objective-type marks.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] In standard textbook notation, what do balance equations for "${kw3}" ensure?`,
          options: [
            `That mass, charge, and energy are conserved on both sides of the reaction/equality.`,
            `That product coefficients must always equal zero under all conditions.`,
            `That all state variables can be ignored without altering the final result.`,
            `That units and dimensions are purely optional and do not affect scoring.`
          ],
          answer: 0,
          topic: kw3,
          explanation: `Every governing equation must obey conservation of mass, charge, and energy. Balanced relationships are verified by checking atom and dimensional consistency on both sides.`
        },

        // --- MEDIUM / BALANCED (Conceptual application, limiting factors, cause-and-effect) ---
        {
          difficulty: 'medium',
          question: `[Conceptual] Which of the following statements regarding ${kw0} is scientifically accurate?`,
          options: [
            s0.length > 90 ? s0.slice(0, 88) + '...' : s0,
            "It requires zero external thermal energy and proceeds spontaneously without activation.",
            "It only occurs under extreme non-biological vacuum environments.",
            "It is completely independent of substrate concentration or catalyst presence."
          ],
          answer: 0,
          topic: `${kw0} Principles`,
          explanation: `Option A is directly derived from the foundational mechanism in your notes: "${s0.slice(0, 110)}". The other options are common misconceptions that ignore activation energy and environmental conditions.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] In an examination problem, if the reaction rate for "${kw1}" decreases abruptly, what is the most likely limiting factor?`,
          options: [
            "Enzymatic denaturation or depletion of substrate concentration beyond saturation.",
            "Excessive availability of photons with zero thermal degradation.",
            "Complete absence of non-participating inert spectator ions.",
            "Infinite rate acceleration according to Le Chatelier's equilibrium principle."
          ],
          answer: 0,
          topic: `${kw1} Kinetics`,
          explanation: `According to Blackman's Law and enzymatic kinetics, rate saturation or thermal denaturation halts reaction velocities. Distractors represent physically implausible scenarios.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] What distinguishes the primary energy storage and intermediate carriers in ${kw2}?`,
          options: [
            "They store high-energy chemical bonds synthesized via coupled electron and energy transport.",
            "They are completely inert and cannot be hydrolyzed or transferred to secondary acceptors.",
            "They violate the First Law of Thermodynamics by generating unbounded output.",
            "They are restricted exclusively to synthetic inorganic systems with zero organic presence."
          ],
          answer: 0,
          topic: `${kw2} Energetics`,
          explanation: `Biological and chemical energy carriers rely on transferable covalent and phosphoanhydride bonds to couple endergonic and exergonic reactions efficiently.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] How should an exam candidate approach analytical problems involving ${kw3}?`,
          options: [
            "State fundamental conservation laws, write boundary conditions, and balance all dimensions.",
            "Skip all intermediate mathematical steps and write arbitrary unitless values.",
            "Assume friction, gravity, and resistance are universally non-existent in every system.",
            "Treat all exponential factors as linear constants regardless of temperature."
          ],
          answer: 0,
          topic: `${kw3} Analysis`,
          explanation: `Full-credit exam marking keys award distinct marks for initial law statements, algebraic isolation, and dimensional validation.`
        },

        // --- HARD / EXAM CHALLENGE (Tricky distractors, multi-step edge cases, examiner traps) ---
        {
          difficulty: 'hard',
          question: `[Exam Challenge] Under extreme non-ideal conditions, which edge case disrupts the typical steady state of ${kw0}?`,
          options: [
            `Feedback inhibition or severe kinetic bottlenecks triggering non-linear pathway collapse.`,
            `Spontaneous infinite creation of mass in violation of the continuity equation.`,
            `Zero effect whatsoever because thermodynamic systems are universally immune to stress.`,
            `Immediate reversal of time arrow without any entropy generation.`
          ],
          answer: 0,
          topic: `${kw0} Edge Cases`,
          explanation: `In advanced ${grade} questions, examiners test whether students realize that feedback inhibition and allosteric bottlenecks disrupt linear pathways. Option A correctly identifies the non-linear response.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] A student claims that increasing temperature will indefinitely increase the yield of ${kw1}. Why is this reasoning flawed?`,
          options: [
            `Past the thermal optimum, enzyme denaturation and thermal breakdown drastically reduce reaction rates.`,
            `Temperature has absolutely zero thermodynamic relationship with molecular collision frequency.`,
            `Reactions can only accelerate if temperature is lowered to absolute zero (-273.15°C).`,
            `The Arrhenius pre-exponential factor collapses to zero whenever heat is applied.`
          ],
          answer: 0,
          topic: `${kw1} Temperature Traps`,
          explanation: `This is a classic examiner trap! While Arrhenius kinetics predict higher collision rates initially, real biological and chemical systems experience thermal denaturation or reverse equilibrium past the optimum.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] In a multi-step analytical derivation for ${kw4}, which constraint is most commonly omitted by candidates, resulting in lost marks?`,
          options: [
            `Failing to state the reference frame, boundary conditions, and dimensional balance of units.`,
            `Forgetting to randomly double the final answer to satisfy examiner discretion.`,
            `Assuming that all mathematical variables must be written in Roman numerals only.`,
            `Neglecting to state that energy and momentum can be freely destroyed when needed.`
          ],
          answer: 0,
          topic: `${kw4} Derivations`,
          explanation: `Marking rubrics deduct 1 to 2 marks when boundary conditions (such as T = 298K, standard pressure, or initial t=0 constraints) and SI units are omitted from derivations.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] How does coupling an exergonic reaction with an endergonic step in ${kw5} resolve the thermodynamic spontaneity constraint?`,
          options: [
            `The net Delta G of the combined reaction becomes negative, driving the unfavorable process forward.`,
            `The Second Law of Thermodynamics is temporarily suspended during intermediate phosphorylation.`,
            `Energy is created spontaneously from the void to satisfy the enthalpy deficit.`,
            `The activation energy barrier is increased to infinite resistance.`
          ],
          answer: 0,
          topic: `${kw5} Thermodynamics`,
          explanation: `Reaction coupling works because free energies (Delta G) are additive. As long as the overall net Gibbs free energy is negative, the combined reaction proceeds spontaneously.`
        },

        // --- ADDITIONAL TIER 2 & TIER 3 QUESTIONS (Supporting up to 20 questions) ---
        {
          difficulty: 'easy',
          question: `[Foundational] What unit or dimensional requirement applies when recording physical variables for ${kw3}?`,
          options: [
            `Standard SI units must be maintained consistently across all intermediate equations.`,
            `Any arbitrary unit can be used without conversion factors.`,
            `Units are completely irrelevant as long as the numbers match.`,
            `Dimensions only matter for qualitative exam questions.`
          ],
          answer: 0,
          topic: `${kw3} Units`,
          explanation: `In standard board and competitive grading, omitting SI unit conversions leads to an automatic deduction.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] Which statement best summarizes why students create notes on ${kw0}?`,
          options: [
            `To crystallize high-yield core definitions, reaction pathways, and exam rules.`,
            `To memorize verbatim paragraphs without understanding principles.`,
            `To replace standard textbooks with purely fictional assumptions.`,
            `To ignore teacher rubrics and exam marking guidelines.`
          ],
          answer: 0,
          topic: `${kw0} Summary`,
          explanation: `High-yield notes distill dense textbook chapters into actionable definitions and mnemonics for rapid recall.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] When reviewing ${kw1}, what is the quickest way to spot the rate-limiting step?`,
          options: [
            `Identify the slowest intermediate step with the highest activation energy barrier.`,
            `Pick the fastest step that releases the most thermal heat.`,
            `Assume the last step of the reaction is always the rate-determining step.`,
            `Choose the step with the shortest molecular lifetime.`
          ],
          answer: 0,
          topic: `${kw1} Rate Steps`,
          explanation: `The rate-determining step (RDS) in any multi-step reaction is always the slowest step with the highest barrier.`
        },
        {
          difficulty: 'easy',
          question: `[Foundational] What does an equilibrium constant greater than 1 (K > 1) indicate regarding ${kw4}?`,
          options: [
            `At equilibrium, products are favored over reactants.`,
            `The reaction can never proceed in the forward direction.`,
            `All reactants have vanished completely into non-existence.`,
            `The activation energy is equal to zero.`
          ],
          answer: 0,
          topic: `${kw4} Equilibrium`,
          explanation: `When K > 1, the equilibrium position favors product formation under standard conditions.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] How do catalysts alter the pathway kinetics of ${kw1} without shifting the final equilibrium?`,
          options: [
            `They lower activation energy by providing an alternative transition state, accelerating both forward and reverse rates equally.`,
            `They destroy reactant molecules so only product molecules can physically exist.`,
            `They permanently consume thermodynamic free energy from the surrounding universe.`,
            `They change the enthalpy of reaction Delta H to make endothermic reactions exothermic.`
          ],
          answer: 0,
          topic: `${kw1} Catalysis`,
          explanation: `Catalysts lower the activation energy barrier equally in both directions, speeding up the approach to equilibrium without altering the equilibrium constant K.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] If a student observes an endothermic temperature drop during ${kw2}, what does Le Chatelier's Principle predict if heat is added?`,
          options: [
            `The equilibrium shifts toward the endothermic direction to absorb added thermal energy, increasing yield.`,
            `The reaction ceases permanently due to thermal confusion.`,
            `The system shifts backward to generate additional heat.`,
            `The temperature drop will reverse instantly without any material shift.`
          ],
          answer: 0,
          topic: `${kw2} Le Chatelier`,
          explanation: `According to Le Chatelier's Principle, adding heat to an endothermic system shifts equilibrium toward the forward product side to absorb excess thermal stress.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] Why is the rate of diffusion or transport across membranes for ${kw0} proportional to concentration gradients?`,
          options: [
            `According to Fick's First Law, net flux moves down electrochemical potential gradients from high to low concentration.`,
            `Molecules possess conscious intent to avoid crowded environments.`,
            `Diffusion requires constant external mechanical agitation to occur.`,
            `Concentration differences generate electromagnetic repulsion fields.`
          ],
          answer: 0,
          topic: `${kw0} Transport`,
          explanation: `Fick's law dictates that passive diffusion flux is directly proportional to the magnitude of the concentration gradient.`
        },
        {
          difficulty: 'medium',
          question: `[Conceptual] How does feedback inhibition serve as a homeostatic control mechanism in ${kw5}?`,
          options: [
            `The end product allosterically binds to the first committed enzyme to halt excess metabolic expenditure.`,
            `The substrate destroys all incoming reactant molecules.`,
            `Feedback circuits permanently damage the genetic transcription machinery.`,
            `The process causes systemic metabolic collapse upon reaching threshold.`
          ],
          answer: 0,
          topic: `${kw5} Regulation`,
          explanation: `Feedback inhibition prevents cellular waste by allowing accumulated end products to inhibit upstream committed enzymes allosterically.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] A 5-mark university exam problem asks to calculate efficiency for ${kw2}. Which thermodynamic formula must be stated first?`,
          options: [
            `Carnot efficiency eta = 1 - (T_cold / T_hot), alongside First Law energy balance equations.`,
            `Random multiplication of input temperature by absolute zero.`,
            `Assuming 100% perpetual motion efficiency with zero frictional or heat losses.`,
            `Using Newton's Second Law F=ma in place of thermodynamic relations.`
          ],
          answer: 0,
          topic: `${kw2} Efficiency`,
          explanation: `Full-credit university marking keys require starting from Carnot efficiency bounds and fundamental energy conservation balances.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] What is the examiner's primary pitfall when asking questions about allosteric vs competitive inhibition in ${kw1}?`,
          options: [
            `Students confuse Vmax and Km changes: competitive increases Km without changing Vmax, while non-competitive lowers Vmax.`,
            `Students assume all inhibitors permanently disintegrate enzyme proteins.`,
            `Students forget that all inhibitors are exclusively gaseous elements.`,
            `Students believe enzymes only function in absolute zero environments.`
          ],
          answer: 0,
          topic: `${kw1} Enzyme Kinetics`,
          explanation: `This is the #1 exam trap in biochemistry and pharmacology! Competitive inhibitors increase apparent Km (can be overcome by excess substrate), whereas non-competitive inhibitors decrease Vmax.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] In a boundary-value differential formulation for ${kw3}, what happens if transient terms are neglected prematurely?`,
          options: [
            `The solution fails to capture dynamic oscillatory behavior or initial startup stresses.`,
            `The mathematics becomes invalid because time is physically prohibited from existing.`,
            `The steady state solution will automatically produce complex imaginary numbers.`,
            `The error cancels itself out completely under all conditions.`
          ],
          answer: 0,
          topic: `${kw3} Boundary Conditions`,
          explanation: `Neglecting time-dependent transient derivatives assumes immediate steady state, completely missing initial spike stresses and damping dynamics.`
        },
        {
          difficulty: 'hard',
          question: `[Exam Challenge] Under what conditions does the Gibbs Free Energy equation Delta G = Delta H - T*Delta S become zero?`,
          options: [
            `At dynamic thermodynamic equilibrium, where the forward and reverse reaction rates are perfectly balanced.`,
            `Only at infinite temperature where all molecular matter ceases to exist.`,
            `When all reactants are locked in an immovable crystalline state at boiling point.`,
            `Whenever pressure is decreased below standard atmospheric levels.`
          ],
          answer: 0,
          topic: `${kw5} Gibbs Equilibrium`,
          explanation: `At true equilibrium, Delta G = 0, meaning the system has no driving force to shift toward reactants or products without external disturbance.`
        }
      ];

      // Mark-Graded Questions
      const examQA = [
        {
          marks: 1,
          q: `Define ${capitalize(topKeywords[0] || 'the primary term')} in one concise sentence.`,
          a: `Model Answer: ${cleanSentences[0] || 'A fundamental process converting potential energy into kinetic or metabolic energy under defined conditions.'}`
        },
        {
          marks: 3,
          q: `Explain the step-by-step mechanism and role of limiting factors. (3 Marks)`,
          a: `Point 1: Define the primary input and activation threshold (1M).\nPoint 2: Outline the intermediate electron/energy transport phase (1M).\nPoint 3: State the limiting conditions according to Blackman's or Arrhenius's laws (1M).`
        },
        {
          marks: 5,
          q: `Give a comprehensive analytical breakdown with balanced equations and exam precautions. (5 Marks)`,
          a: `1. Overall balanced chemical/physical equation (1M).\n2. Detailed structural or mechanical steps with diagrams/derivation (2M).\n3. Practical significance and commercial/biological relevance (1M).\n4. Common experimental pitfalls and error sources (1M).`
        }
      ];

      // Build Mind Map Knowledge Graph (Dual-Loop Topology matching user template)
      const centralTopic = cleanSentences[0] ? cleanSentences[0].split(/[;:,]/)[0].slice(0, 36) : capitalize(topKeywords[0] || 'Core Subject');
      const mindmap = {
        central: {
          title: centralTopic,
          subtitle: `Calibrated for ${grade}`,
          takeaway: `Primary governing system unifying all 6 functional branches and conceptual dependencies in this document.`
        },
        branches: [
          {
            id: 'branch-1',
            side: 'left',
            position: 'top-left',
            color: 'cyan',
            icon: '💬',
            title: capitalize(topKeywords[0] || 'Foundations'),
            subtitle: cleanSentences[0] ? cleanSentences[0].slice(0, 75) + '...' : `Primary input mechanism and core definitions.`,
            takeaway: `Examiners test this as the fundamental prerequisite for solving all downstream numericals and essays.`,
            connections: [capitalize(topKeywords[1] || 'Kinetics'), capitalize(topKeywords[3] || 'Derivations')]
          },
          {
            id: 'branch-2',
            side: 'left',
            position: 'mid-left',
            color: 'blue',
            icon: '🧩',
            title: capitalize(topKeywords[1] || 'Kinetics'),
            subtitle: cleanSentences[1] ? cleanSentences[1].slice(0, 75) + '...' : `Dynamic reaction rates, intermediate thresholds, and limiting factors.`,
            takeaway: `Watch out for rate saturation and temperature shifts (Arrhenius and Blackman's constraints).`,
            connections: [capitalize(topKeywords[0] || 'Foundations'), capitalize(topKeywords[2] || 'Mechanisms')]
          },
          {
            id: 'branch-3',
            side: 'left',
            position: 'bottom-left',
            color: 'purple',
            icon: '🎯',
            title: capitalize(topKeywords[2] || 'Mechanisms'),
            subtitle: cleanSentences[2] ? cleanSentences[2].slice(0, 75) + '...' : `Step-by-step pathways, electron carriers, and intermediate state cycles.`,
            takeaway: `Step-marking rubrics allocate 2-3 marks specifically for listing intermediate state transformations.`,
            connections: [capitalize(topKeywords[1] || 'Kinetics'), capitalize(topKeywords[4] || 'Equilibrium')]
          },
          {
            id: 'branch-4',
            side: 'right',
            position: 'top-right',
            color: 'green',
            icon: '🌿',
            title: capitalize(topKeywords[3] || 'Derivations'),
            subtitle: cleanSentences[3] ? cleanSentences[3].slice(0, 75) + '...' : `Governing mathematical equalities, dimensional balances, and boundary constraints.`,
            takeaway: `Always state standard SI units and boundary initial conditions to prevent 1-mark deductions.`,
            connections: [capitalize(topKeywords[0] || 'Foundations'), capitalize(topKeywords[4] || 'Equilibrium')]
          },
          {
            id: 'branch-5',
            side: 'right',
            position: 'mid-right',
            color: 'pink',
            icon: '🎯',
            title: capitalize(topKeywords[4] || 'Equilibrium'),
            subtitle: cleanSentences[4] ? cleanSentences[4].slice(0, 75) + '...' : `Dynamic stability, reversible pathways, and Le Chatelier homeostatic shifts.`,
            takeaway: `When Delta G = 0, rates are balanced; adding stress causes predictable thermodynamic compensation.`,
            connections: [capitalize(topKeywords[2] || 'Mechanisms'), capitalize(topKeywords[5] || 'Applications')]
          },
          {
            id: 'branch-6',
            side: 'right',
            position: 'bottom-right',
            color: 'yellow',
            icon: '⚖️',
            title: capitalize(topKeywords[5] || 'Applications'),
            subtitle: cleanSentences[5] ? cleanSentences[5].slice(0, 75) + '...' : `Real-world clinical, commercial, or laboratory experimental applications.`,
            takeaway: `High-scoring essay answers conclude with practical use-cases and environmental safety caveats.`,
            connections: [capitalize(topKeywords[4] || 'Equilibrium'), capitalize(topKeywords[0] || 'Foundations')]
          }
        ]
      };

      return {
        executiveSummary,
        bullets,
        formulas,
        glossary,
        mnemonics,
        examTraps,
        quickRevision,
        quizQuestions,
        examQA,
        mindmap
      };
    }

    function capitalize(s) {
      if (!s) return '';
      return s.charAt(0).toUpperCase() + s.slice(1);
    }
    function escapeHTML(str) {
      return String(str).replace(/[&<>'"]/g, tag => ({
        '&': '&amp;', '<': '&lt;', '>': '&gt;', "'": '&#39;', '"': '&quot;'
      }[tag] || tag));
    }

    /* ===================================================
       8. FEATURE 1: SMART SUMMARY VIEW
       =================================================== */
    function openSmartSummary() {
      sfx.click();
      if (!state.analyzedData) return;
      const data = state.analyzedData;

      document.getElementById('summary-doc-title').textContent = state.activeDocTitle;
      document.getElementById('summary-grade-badge').textContent = `Calibrated for ${state.level || 'Undergraduate'}`;
      document.getElementById('summary-executive-body').textContent = data.executiveSummary || 'No executive summary generated.';

      // Bullets
      const bulletsList = document.getElementById('summary-bullets-list');
      bulletsList.innerHTML = (data.bullets || []).map(b => `
        <li class="flex items-start gap-3 p-3 rounded-xl bg-white/[0.02] border border-white/5">
          <span class="text-neonGreen text-base leading-none">●</span>
          <span class="leading-relaxed">${escapeHTML(b)}</span>
        </li>
      `).join('');

      // Formulas
      const formulasGrid = document.getElementById('summary-formulas-grid');
      formulasGrid.innerHTML = (data.formulas || []).map(f => `
        <div class="p-4 rounded-2xl bg-[#0B0E14] border border-neonCyan/30 shadow-[0_0_15px_rgba(0,229,255,0.1)] space-y-2">
          <div class="text-xs font-mono text-neonCyan uppercase tracking-wider">${escapeHTML(f.name)}</div>
          <div class="font-mono text-sm text-white font-bold bg-white/5 p-2 rounded-lg">${escapeHTML(f.equation)}</div>
          <div class="text-xs text-gray-400 font-inter">${escapeHTML(f.variables)}</div>
        </div>
      `).join('');

      // Glossary
      const glossaryGrid = document.getElementById('summary-glossary-grid');
      glossaryGrid.innerHTML = (data.glossary || []).map(g => `
        <div class="p-3.5 rounded-xl bg-white/[0.02] border border-white/5 hover:border-neonPurple/40 transition-colors">
          <div class="font-outfit font-bold text-sm text-neonPurple">${escapeHTML(g.term)}</div>
          <div class="text-xs text-gray-400 mt-1 line-clamp-3">${escapeHTML(g.def)}</div>
        </div>
      `).join('');

      showScreen('screen-summary');
    }

    // Text to Speech
    let isSpeaking = false;
    function toggleAudioSpeech() {
      sfx.click();
      if (!('speechSynthesis' in window)) {
        alert('Text to speech not supported by your browser.');
        return;
      }
      if (isSpeaking) {
        stopAudioSpeech();
      } else {
        startAudioSpeech();
      }
    }
    function startAudioSpeech() {
      window.speechSynthesis.cancel();
      const textToRead = `${document.getElementById('summary-doc-title').textContent}. Executive Summary: ${document.getElementById('summary-executive-body').textContent}. Core takeaways: ${(state.analyzedData.bullets || []).join('. ')}`;
      const utterance = new SpeechSynthesisUtterance(textToRead);
      utterance.rate = 1.0;
      utterance.pitch = 1.0;
      utterance.onend = stopAudioSpeech;
      utterance.onerror = stopAudioSpeech;

      window.speechSynthesis.speak(utterance);
      isSpeaking = true;
      document.getElementById('tts-icon').textContent = '⏹️';
      document.getElementById('tts-text').textContent = 'Stop Reading';
    }
    function stopAudioSpeech() {
      window.speechSynthesis.cancel();
      isSpeaking = false;
      document.getElementById('tts-icon').textContent = '🔊';
      document.getElementById('tts-text').textContent = 'Read Aloud';
    }

    function copySummaryText() {
      sfx.click();
      const text = `${document.getElementById('summary-doc-title').textContent}\n\nEXECUTIVE SUMMARY:\n${document.getElementById('summary-executive-body').textContent}\n\nCORE BULLETS:\n${(state.analyzedData.bullets || []).map(b => '- ' + b).join('\n')}`;
      navigator.clipboard.writeText(text).then(() => {
        const lbl = document.getElementById('copy-btn-label');
        lbl.textContent = 'Copied ✓';
        setTimeout(() => lbl.textContent = 'Copy Text', 1500);
      });
    }

    /* ===================================================
       9. FEATURE 2: ADAPTIVE DIAGNOSTIC QUIZ (Weakness Detection & Customization)
       =================================================== */
    function openQuizConfigModal() {
      sfx.click();
      if (!state.analyzedData) {
        alert('Please analyze a study document or paste notes first.');
        return;
      }
      // Sync UI with current state values
      const currentCount = state.quizCount || 5;
      const currentDiff = state.quizDifficulty || 'medium';

      setQuizCount(currentCount, false);
      setQuizDifficulty(currentDiff, false);

      const targetLevelLabel = document.getElementById('quiz-config-target-level');
      if (targetLevelLabel) {
        targetLevelLabel.textContent = state.level || 'Undergraduate';
      }

      document.getElementById('quiz-config-modal').classList.remove('hidden');
    }

    function closeQuizConfigModal() {
      sfx.click();
      document.getElementById('quiz-config-modal').classList.add('hidden');
    }

    function setQuizCount(count, triggerSfx = true) {
      if (triggerSfx) sfx.click();
      state.quizCount = parseInt(count, 10);
      localStorage.setItem('eduai_quiz_count', state.quizCount);

      const displayVal = document.getElementById('quiz-count-display-val');
      if (displayVal) displayVal.textContent = `${state.quizCount} Questions`;

      document.querySelectorAll('.quiz-count-btn').forEach(btn => {
        const btnCount = parseInt(btn.getAttribute('data-count'), 10);
        if (btnCount === state.quizCount) {
          btn.className = 'quiz-count-btn active py-2.5 rounded-xl border border-neonCyan bg-neonCyan/15 text-xs font-mono font-bold text-neonCyan shadow-glow-cyan transition-all';
        } else {
          btn.className = 'quiz-count-btn py-2.5 rounded-xl border border-white/10 bg-white/[0.02] text-xs font-mono font-semibold text-gray-300 hover:border-neonCyan hover:text-white transition-all';
        }
      });
    }

    function setQuizDifficulty(diff, triggerSfx = true) {
      if (triggerSfx) sfx.click();
      state.quizDifficulty = diff;
      localStorage.setItem('eduai_quiz_difficulty', diff);

      const displayVal = document.getElementById('quiz-diff-display-val');
      const capDiff = capitalize(diff);
      if (displayVal) {
        displayVal.textContent = capDiff;
        if (diff === 'easy') {
          displayVal.className = 'px-2.5 py-0.5 rounded-full text-xs font-mono font-bold bg-neonGreen/15 text-neonGreen border border-neonGreen/30';
        } else if (diff === 'hard') {
          displayVal.className = 'px-2.5 py-0.5 rounded-full text-xs font-mono font-bold bg-neonPink/15 text-neonPink border border-neonPink/30';
        } else {
          displayVal.className = 'px-2.5 py-0.5 rounded-full text-xs font-mono font-bold bg-neonCyan/15 text-neonCyan border border-neonCyan/30';
        }
      }

      document.querySelectorAll('.quiz-diff-btn').forEach(btn => {
        const btnDiff = btn.getAttribute('data-diff');
        if (btnDiff === diff) {
          if (diff === 'easy') {
            btn.className = 'quiz-diff-btn active p-3.5 rounded-2xl border-2 border-neonGreen bg-neonGreen/10 text-left shadow-glow-green transition-all group flex flex-col justify-between';
          } else if (diff === 'hard') {
            btn.className = 'quiz-diff-btn active p-3.5 rounded-2xl border-2 border-neonPink bg-neonPink/10 text-left shadow-glow-pink transition-all group flex flex-col justify-between';
          } else {
            btn.className = 'quiz-diff-btn active p-3.5 rounded-2xl border-2 border-neonCyan bg-neonCyan/10 text-left shadow-glow-cyan transition-all group flex flex-col justify-between';
          }
        } else {
          btn.className = 'quiz-diff-btn p-3.5 rounded-2xl border border-white/10 bg-white/[0.02] text-left hover:border-white/30 transition-all group flex flex-col justify-between';
        }
      });
    }

    function applyQuizConfigAndLaunch() {
      closeQuizConfigModal();
      openAdaptiveQuiz();
    }

    function openAdaptiveQuiz() {
      sfx.click();
      if (!state.analyzedData) return;
      
      const allQuestions = (state.analyzedData.quizQuestions || []).slice();
      const targetDiff = state.quizDifficulty || 'medium';
      const targetCount = state.quizCount || 5;

      // 1. Filter or sort questions prioritizing chosen difficulty level
      let filtered = allQuestions.filter(q => q.difficulty === targetDiff);
      
      // If not enough questions in this exact difficulty tier, complement with other tiers
      if (filtered.length < targetCount) {
        const remaining = allQuestions.filter(q => q.difficulty !== targetDiff);
        filtered = filtered.concat(remaining);
      }

      // If document had fewer questions than requested count (e.g. 15 or 20 requested from short text), cycle through cleanly with fresh IDs
      if (filtered.length < targetCount && filtered.length > 0) {
        const basePool = filtered.slice();
        while (filtered.length < targetCount) {
          const nextQ = { ...basePool[filtered.length % basePool.length] };
          filtered.push(nextQ);
        }
      }

      // Slice to selected question count
      const finalQuestions = filtered.slice(0, targetCount).map(q => ({ ...q }));

      state.quiz = {
        activeQuestions: finalQuestions,
        currentIndex: 0,
        score: 0,
        weakQueue: [],
        mastered: [],
        flaggedWeak: [],
        totalAnswered: 0
      };

      // Update Difficulty badge in HUD
      updateQuizHudDifficulty();

      document.getElementById('quiz-results-box').classList.add('hidden');
      document.getElementById('quiz-question-box').classList.remove('hidden');
      document.getElementById('weakness-banner').classList.add('hidden');
      document.getElementById('quiz-weak-counter-badge').classList.add('hidden');

      showScreen('screen-quiz');
      renderCurrentQuizQuestion();
    }

    function updateQuizHudDifficulty() {
      const diffText = document.getElementById('quiz-hud-diff-text');
      const diffBadge = document.getElementById('quiz-hud-diff-badge');
      if (!diffText || !diffBadge) return;

      const diff = state.quizDifficulty || 'medium';
      diffText.textContent = capitalize(diff);

      if (diff === 'easy') {
        diffBadge.className = 'px-2.5 py-1 rounded-full bg-neonGreen/10 border border-neonGreen/30 text-neonGreen flex items-center gap-1.5 font-bold uppercase tracking-wider text-[11px]';
        diffBadge.querySelector('span').textContent = '🌱';
      } else if (diff === 'hard') {
        diffBadge.className = 'px-2.5 py-1 rounded-full bg-neonPink/10 border border-neonPink/30 text-neonPink flex items-center gap-1.5 font-bold uppercase tracking-wider text-[11px]';
        diffBadge.querySelector('span').textContent = '🔥';
      } else {
        diffBadge.className = 'px-2.5 py-1 rounded-full bg-neonPurple/10 border border-neonPurple/30 text-neonPurple flex items-center gap-1.5 font-bold uppercase tracking-wider text-[11px]';
        diffBadge.querySelector('span').textContent = '⚡';
      }
    }

    function renderCurrentQuizQuestion() {
      const qz = state.quiz;
      const q = qz.activeQuestions[qz.currentIndex];

      if (!q) {
        finishQuiz();
        return;
      }

      // Progress HUD
      document.getElementById('quiz-hud-progress').textContent = `Question ${qz.currentIndex + 1} of ${qz.activeQuestions.length}`;
      document.getElementById('quiz-live-score').textContent = qz.score;
      const percent = (qz.currentIndex / qz.activeQuestions.length) * 100;
      document.getElementById('quiz-progress-bar').style.width = percent + '%';

      // Question Title & Tags
      document.getElementById('quiz-topic-tag').textContent = q.topic || 'Core Concept';
      document.getElementById('quiz-question-text').textContent = q.question;

      // Reinforcement Tag visibility
      const reinforceTag = document.getElementById('quiz-reinforce-tag');
      if (q.isReinforcement) {
        reinforceTag.classList.remove('hidden');
      } else {
        reinforceTag.classList.add('hidden');
      }

      // Hide explanation
      document.getElementById('quiz-explanation-box').classList.add('hidden');

      // Options
      const optionsGrid = document.getElementById('quiz-options-grid');
      const letters = ['A', 'B', 'C', 'D'];
      optionsGrid.innerHTML = q.options.map((opt, i) => `
        <button class="quiz-opt-btn group relative flex items-center justify-between p-4 rounded-2xl glass-card border border-white/10 hover:border-neonCyan hover:bg-neonCyan/[0.04] text-left transition-all duration-200 text-sm font-inter text-gray-200 focus:outline-none"
          onclick="handleQuizAnswer(${i})">
          <div class="flex items-center gap-3">
            <span class="w-7 h-7 rounded-lg bg-white/5 border border-white/10 flex items-center justify-center font-mono font-bold text-xs text-neonCyan group-hover:border-neonCyan transition-colors">
              ${letters[i]}
            </span>
            <span>${escapeHTML(opt)}</span>
          </div>
          <span class="opt-indicator hidden font-mono font-bold text-xs"></span>
        </button>
      `).join('');
    }

    function handleQuizAnswer(selectedIdx) {
      const qz = state.quiz;
      const q = qz.activeQuestions[qz.currentIndex];
      const buttons = document.querySelectorAll('.quiz-opt-btn');

      // Disable all options
      buttons.forEach(b => b.onclick = null);

      const isCorrect = selectedIdx === q.answer;
      qz.totalAnswered++;

      // Visual styling for correct and chosen options
      buttons.forEach((btn, idx) => {
        const ind = btn.querySelector('.opt-indicator');
        if (idx === q.answer) {
          btn.className = 'quiz-opt-btn flex items-center justify-between p-4 rounded-2xl bg-neonGreen/15 border-2 border-neonGreen text-white text-sm font-semibold shadow-glow-green';
          if (ind) { ind.classList.remove('hidden'); ind.textContent = '✓ CORRECT'; ind.className = 'text-neonGreen font-mono font-bold text-xs'; }
        } else if (idx === selectedIdx && !isCorrect) {
          btn.className = 'quiz-opt-btn flex items-center justify-between p-4 rounded-2xl bg-neonPink/15 border-2 border-neonPink text-white text-sm shadow-glow-pink';
          if (ind) { ind.classList.remove('hidden'); ind.textContent = '✕ INCORRECT'; ind.className = 'text-neonPink font-mono font-bold text-xs'; }
        } else {
          btn.classList.add('opacity-40');
        }
      });

      // Weakness Detection Logic
      if (isCorrect) {
        sfx.success();
        qz.score++;
        if (!qz.mastered.includes(q.topic)) qz.mastered.push(q.topic);
        // If it was a reinforcement question that passed, clear weak count
        if (q.isReinforcement) {
          state.stats.weakCleared++;
          localStorage.setItem('eduai_stat_weak', state.stats.weakCleared);
          document.getElementById('stat-weak').textContent = `${state.stats.weakCleared} Cleared`;
        }
      } else {
        sfx.error();
        if (!qz.flaggedWeak.includes(q.topic)) qz.flaggedWeak.push(q.topic);

        // Dynamically spawn Reinforcement Question targeting this specific weak spot!
        spawnReinforcementQuestion(q.topic);

        // Trigger visual weakness banner
        const banner = document.getElementById('weakness-banner');
        document.getElementById('weak-concept-name').textContent = q.topic;
        banner.classList.remove('hidden');

        // Update HUD weak count badge
        const badge = document.getElementById('quiz-weak-counter-badge');
        badge.classList.remove('hidden');
        document.getElementById('quiz-weak-count').textContent = qz.flaggedWeak.length;
      }

      // Show In-Depth Student-Friendly Explanation Drawer
      const expBox = document.getElementById('quiz-explanation-box');
      const expTitle = document.getElementById('quiz-feedback-title');
      const expSimple = document.getElementById('quiz-feedback-simple');
      const trapContainer = document.getElementById('quiz-feedback-trap-container');
      const trapText = document.getElementById('quiz-feedback-trap');

      const letters = ['A', 'B', 'C', 'D'];
      const correctOptText = q.options[q.answer];
      const selectedOptText = q.options[selectedIdx];

      if (isCorrect) {
        expTitle.className = 'p-4 rounded-2xl font-outfit font-bold text-base sm:text-lg flex items-center justify-between gap-3 bg-neonGreen/10 border border-neonGreen/30 text-neonGreen';
        expTitle.innerHTML = `
          <div class="flex items-center gap-2">
            <span>✓</span> <span>Spot on! Option ${letters[q.answer]} is correct.</span>
          </div>
          <span class="text-xs font-mono bg-neonGreen/20 px-3 py-1 rounded-full text-white">+1 POINT</span>
        `;
        trapContainer.classList.add('hidden');
      } else {
        expTitle.className = 'p-4 rounded-2xl font-outfit font-bold text-base sm:text-lg flex items-center justify-between gap-3 bg-neonPink/10 border border-neonPink/30 text-neonPink';
        expTitle.innerHTML = `
          <div class="flex items-center gap-2">
            <span>✕</span> <span>Incorrect choice — The correct answer is Option ${letters[q.answer]}.</span>
          </div>
          <span class="text-xs font-mono bg-neonPink/20 px-3 py-1 rounded-full text-white">LEARNING MOMENT</span>
        `;

        // Explain why the student's selected answer was a misconception
        trapContainer.classList.remove('hidden');
        trapText.innerHTML = `
          <p><strong class="text-neonPink">You chose Option ${letters[selectedIdx]}:</strong> "${escapeHTML(selectedOptText)}"</p>
          <p class="mt-2 text-gray-300">
            <strong>Why students pick this trap:</strong> This distractor is designed to sound plausible, but it conflicts with the core rules of <em>${escapeHTML(q.topic || 'this concept')}</em>. In examinations, questions frequently include inverted directions, false absolutes, or opposite reaction conditions to test if students truly understand the core mechanism.
          </p>
        `;
      }

      // Student-friendly core explanation
      expSimple.innerHTML = `
        <div class="space-y-2">
          <div class="flex items-center gap-2 text-neonGreen font-semibold text-xs font-mono">
            <span>✓ Correct Answer:</span> <span>Option ${letters[q.answer]} — "${escapeHTML(correctOptText)}"</span>
          </div>
          <p class="text-gray-200">
            ${escapeHTML(q.explanation || `The right answer is Option ${letters[q.answer]}. It represents the true governing mechanism described in your study material.`)}
          </p>
          <div class="p-3 rounded-xl bg-neonCyan/[0.05] border border-neonCyan/20 text-xs text-neonCyan font-mono mt-2">
            💡 <strong>Student Exam Tip:</strong> When evaluating <em>${escapeHTML(q.topic || 'this topic')}</em>, always check the fundamental cause-and-effect link rather than looking for quick buzzwords!
          </div>
        </div>
      `;

      // Update YouTube video embed & direct video watch link
      const ytIframe = document.getElementById('quiz-youtube-iframe');
      const ytLink = document.getElementById('quiz-youtube-direct-link');
      const ytSearchLink = document.getElementById('quiz-youtube-search-link');
      const ytTopicBadge = document.getElementById('quiz-yt-topic-badge');
      const ytHint = document.getElementById('quiz-yt-channel-hint');
      const ytTopic = q.topic || 'science lesson';

      const videoInfo = getEducationalVideoInfo(ytTopic);
      ytIframe.src = videoInfo.embedUrl;
      ytLink.href = videoInfo.watchUrl;
      if (ytSearchLink) ytSearchLink.href = `https://www.youtube.com/results?search_query=${encodeURIComponent(ytTopic + ' lecture Khan Academy CrashCourse')}`;
      if (ytTopicBadge) ytTopicBadge.textContent = `${escapeHTML(ytTopic)} Lesson`;
      if (ytHint) ytHint.textContent = `📺 Channel: ${videoInfo.channel} • "${videoInfo.title}"`;

      // Update Live Internet Wikipedia source
      fetchWikipediaSource(q.topic || 'Science');

      expBox.classList.remove('hidden');
      setTimeout(() => expBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' }), 100);
    }

    function getEducationalVideoInfo(topic = '') {
      const t = topic.toLowerCase();
      // Curated student-friendly educational YouTube videos
      if (t.includes('photo') || t.includes('chlorophyll') || t.includes('calvin') || t.includes('plant')) {
        return {
          id: 'uixA8ZXx0KU',
          embedUrl: 'https://www.youtube-nocookie.com/embed/uixA8ZXx0KU',
          watchUrl: 'https://www.youtube.com/watch?v=uixA8ZXx0KU',
          channel: 'Amoeba Sisters',
          title: 'Photosynthesis and the Teeny Tiny Pigment Pancakes'
        };
      }
      if (t.includes('newton') || t.includes('motion') || t.includes('gravity') || t.includes('force') || t.includes('mechanic')) {
        return {
          id: 'kKKM8Y-u7ds',
          embedUrl: 'https://www.youtube-nocookie.com/embed/kKKM8Y-u7ds',
          watchUrl: 'https://www.youtube.com/watch?v=kKKM8Y-u7ds',
          channel: 'Khan Academy',
          title: "Newton's Laws of Motion - Physics"
        };
      }
      if (t.includes('database') || t.includes('acid') || t.includes('normal') || t.includes('sql') || t.includes('relational')) {
        return {
          id: 'GFQaEYEc8_8',
          embedUrl: 'https://www.youtube-nocookie.com/embed/GFQaEYEc8_8',
          watchUrl: 'https://www.youtube.com/watch?v=GFQaEYEc8_8',
          channel: 'Decomplexify',
          title: 'Database Normalization: 1NF, 2NF, 3NF Explained'
        };
      }
      if (t.includes('cell') || t.includes('biology') || t.includes('dna') || t.includes('rna') || t.includes('transport')) {
        return {
          id: '8IlzKri08kk',
          embedUrl: 'https://www.youtube-nocookie.com/embed/8IlzKri08kk',
          watchUrl: 'https://www.youtube.com/watch?v=8IlzKri08kk',
          channel: 'Amoeba Sisters',
          title: 'Cell Transport & Plasma Membrane Structure'
        };
      }
      if (t.includes('enzyme') || t.includes('kinetic') || t.includes('cataly') || t.includes('rate')) {
        return {
          id: 'qgVFkRn8f10',
          embedUrl: 'https://www.youtube-nocookie.com/embed/qgVFkRn8f10',
          watchUrl: 'https://www.youtube.com/watch?v=qgVFkRn8f10',
          channel: 'Amoeba Sisters',
          title: 'Enzymes (Updated) - Active Sites, Substrates & Inhibition'
        };
      }
      if (t.includes('energy') || t.includes('thermodynamic') || t.includes('heat') || t.includes('gibbs') || t.includes('enthalpy') || t.includes('entropy')) {
        return {
          id: '8m6hHRlKwxY',
          embedUrl: 'https://www.youtube-nocookie.com/embed/8m6hHRlKwxY',
          watchUrl: 'https://www.youtube.com/watch?v=8m6hHRlKwxY',
          channel: 'CrashCourse',
          title: 'Thermodynamics: Crash Course Physics #23'
        };
      }
      if (t.includes('equil') || t.includes('le chatelier') || t.includes('equilibrium')) {
        return {
          id: 'dIDgPtfv3-k',
          embedUrl: 'https://www.youtube-nocookie.com/embed/dIDgPtfv3-k',
          watchUrl: 'https://www.youtube.com/watch?v=dIDgPtfv3-k',
          channel: 'Khan Academy',
          title: "Le Chatelier's Principle & Dynamic Equilibrium"
        };
      }
      if (t.includes('deriv') || t.includes('calculus') || t.includes('math') || t.includes('formula') || t.includes('dimension')) {
        return {
          id: 'WUvTyaaNkzM',
          embedUrl: 'https://www.youtube-nocookie.com/embed/WUvTyaaNkzM',
          watchUrl: 'https://www.youtube.com/watch?v=WUvTyaaNkzM',
          channel: '3Blue1Brown',
          title: 'Essence of Calculus: The Core Visual Intuition'
        };
      }
      // General Fallback
      return {
        id: 'sQK3Yr4Sc_k',
        embedUrl: 'https://www.youtube-nocookie.com/embed/sQK3Yr4Sc_k',
        watchUrl: 'https://www.youtube.com/watch?v=sQK3Yr4Sc_k',
        channel: 'Khan Academy',
        title: 'Core Science Fundamentals & Problem Solving'
      };
    }

    async function fetchWikipediaSource(topic = '') {
      const titleEl = document.getElementById('quiz-source-title');
      const linkEl = document.getElementById('quiz-source-link');
      const extractEl = document.getElementById('quiz-source-extract');
      const tagEl = document.getElementById('quiz-source-tag');

      // Clean topic keyword
      const cleanKeyword = topic.replace(/[^\w\s]/g, '').trim().split(' ').slice(0, 3).join(' ');
      titleEl.textContent = cleanKeyword || 'Educational Topic';
      linkEl.href = `https://en.wikipedia.org/wiki/${encodeURIComponent(cleanKeyword || 'Science')}`;
      extractEl.innerHTML = '<span class="inline-block w-3 h-3 border-2 border-neonGreen border-t-transparent rounded-full animate-spin mr-2"></span> Fetching verified internet reference...';

      try {
        const res = await fetch(`https://en.wikipedia.org/api/rest_v1/page/summary/${encodeURIComponent(cleanKeyword)}`);
        if (res.ok) {
          const data = await res.json();
          if (data && data.extract) {
            titleEl.textContent = data.title;
            linkEl.href = data.content_urls ? data.content_urls.desktop.page : `https://en.wikipedia.org/wiki/${encodeURIComponent(cleanKeyword)}`;
            extractEl.textContent = data.extract;
            tagEl.textContent = 'WIKIPEDIA VERIFIED SOURCE';
            tagEl.className = 'text-[10px] font-mono px-2 py-0.5 rounded bg-neonGreen/10 text-neonGreen border border-neonGreen/30';
            return;
          }
        }
      } catch (err) {
        console.warn('Wikipedia API fetch issue:', err);
      }

      // High-yield fallback citation
      extractEl.textContent = `Encyclopedic definition & academic consensus: ${cleanKeyword} represents a foundational concept in ${state.level || 'science and engineering'}. Consult the peer-reviewed reference article for comprehensive derivations and experimental proof.`;
      tagEl.textContent = 'ACADEMIC REFERENCE CITATION';
      tagEl.className = 'text-[10px] font-mono px-2 py-0.5 rounded bg-neonCyan/10 text-neonCyan border border-neonCyan/30';
    }

    // Dynamic Reinforcement Question Generator
    function spawnReinforcementQuestion(topic) {
      const qz = state.quiz;
      const reinforcementQ = {
        question: `[Adaptive Reinforcement Drill] Let's master "${topic}": How should you resolve problems involving this concept?`,
        options: [
          `Review the governing definitions of ${topic} and verify state invariants step by step.`,
          `Assume ${topic} has no effect on any reaction rate or equilibrium state.`,
          `Skip verifying physical units and invert the numerator and denominator.`,
          `Treat this concept as purely speculative with no empirical validation.`
        ],
        answer: 0,
        topic: topic,
        isReinforcement: true,
        explanation: `Reinforcement confirmed! Systematically isolating ${topic} ensures high-accuracy marks in ${state.level} evaluations.`
      };

      // Append reinforcement question to the active queue!
      qz.activeQuestions.push(reinforcementQ);
      document.getElementById('quiz-hud-progress').textContent = `Question ${qz.currentIndex + 1} of ${qz.activeQuestions.length}`;
    }

    function nextQuizQuestion() {
      sfx.click();
      const qz = state.quiz;
      qz.currentIndex++;
      document.getElementById('weakness-banner').classList.add('hidden');
      const ytIframe = document.getElementById('quiz-youtube-iframe');
      if (ytIframe) ytIframe.src = '';
      renderCurrentQuizQuestion();
    }

    function finishQuiz() {
      sfx.chime();
      const qz = state.quiz;
      document.getElementById('quiz-question-box').classList.add('hidden');
      const resultsBox = document.getElementById('quiz-results-box');
      resultsBox.classList.remove('hidden');

      const total = qz.activeQuestions.length;
      const percentage = Math.round((qz.score / total) * 100);

      document.getElementById('final-score-text').textContent = `${qz.score} / ${total}`;
      document.getElementById('final-percentage-badge').textContent = `${percentage}% Mastery Rate`;

      // Update global accuracy stat
      state.stats.quizzesTaken++;
      state.stats.totalAccuracy = percentage;
      localStorage.setItem('eduai_stat_quizzes', state.stats.quizzesTaken);
      localStorage.setItem('eduai_stat_acc', state.stats.totalAccuracy);
      document.getElementById('stat-accuracy').textContent = `${percentage}% Mastery`;

      // Mastered concepts
      const mList = document.getElementById('mastered-concepts-list');
      mList.innerHTML = qz.mastered.length ? 
        qz.mastered.map(m => `<li>• ${escapeHTML(m)}</li>`).join('') : 
        `<li class="text-gray-500">Take more quizzes to establish mastery.</li>`;

      // Flagged weak spots
      const wList = document.getElementById('flagged-weak-list');
      const remBtn = document.getElementById('remediate-weak-btn');
      if (qz.flaggedWeak.length) {
        wList.innerHTML = qz.flaggedWeak.map(w => `<li>• ${escapeHTML(w)}</li>`).join('');
        remBtn.classList.remove('hidden');
      } else {
        wList.innerHTML = `<li class="text-neonGreen">🏆 Clean sheet! Zero weak spots detected in this session.</li>`;
        remBtn.classList.add('hidden');
      }
    }

    function startTargetedRemediation() {
      sfx.click();
      const qz = state.quiz;
      const weakTopics = qz.flaggedWeak.slice();
      if (!weakTopics.length) return;

      const remediationQuestions = weakTopics.map((t, i) => ({
        question: `Targeted Remediation #${i + 1}: What is the primary analytical rule governing "${t}"?`,
        options: [
          `Strict adherence to boundary conditions and core formulas for ${t}.`,
          `Ignoring conservation constraints when convenient.`,
          `Inverting the sign of thermodynamic enthalpies at random.`,
          `Omitting references to substrate and equilibrium states.`
        ],
        answer: 0,
        topic: t,
        isReinforcement: true,
        explanation: `Remediation verified! Understanding ${t} eliminates common examiner traps.`
      }));

      qz.activeQuestions = remediationQuestions;
      qz.currentIndex = 0;
      qz.score = 0;
      qz.flaggedWeak = [];

      document.getElementById('quiz-results-box').classList.add('hidden');
      document.getElementById('quiz-question-box').classList.remove('hidden');
      renderCurrentQuizQuestion();
    }

    function exitQuizPrompt() {
      if (confirm('Exit this quiz session? Progress will be saved.')) {
        sfx.click();
        navigateModes();
      }
    }

    /* ===================================================
       10. FEATURE 3: SUPER NOTES (EXAM-ORIENTED CHEAT SHEET)
       =================================================== */
    function openSuperNotes() {
      sfx.click();
      if (!state.analyzedData) return;
      const data = state.analyzedData;

      document.getElementById('supernotes-doc-title').textContent = state.activeDocTitle + ' — Super Notes';
      document.getElementById('supernotes-grade-tag').textContent = `Target Exam Calibration: ${state.level || 'Undergraduate'}`;

      // 1. Mnemonics (Neon Purple)
      const mnemonicsGrid = document.getElementById('supernotes-mnemonics-grid');
      mnemonicsGrid.innerHTML = (data.mnemonics || []).map(m => `
        <div class="p-5 rounded-2xl bg-[#0B0E14] border border-neonPurple/40 shadow-glow-purple space-y-2">
          <div class="flex items-center justify-between">
            <span class="font-outfit font-black text-lg text-neonPurple tracking-wider">💡 ${escapeHTML(m.hook)}</span>
            <span class="text-[10px] font-mono text-gray-400 bg-white/5 px-2 py-0.5 rounded">MNEMONIC</span>
          </div>
          <div class="font-mono text-xs text-white bg-white/5 p-2 rounded">${escapeHTML(m.meaning)}</div>
          <div class="text-xs text-gray-300 font-inter">${escapeHTML(m.context)}</div>
        </div>
      `).join('');

      // 2. Exam Traps (Neon Pink)
      const trapsGrid = document.getElementById('supernotes-traps-grid');
      trapsGrid.innerHTML = (data.examTraps || []).map(t => `
        <div class="p-5 rounded-2xl bg-[#0B0E14] border border-neonPink/40 shadow-glow-pink space-y-2">
          <div class="flex items-center justify-between">
            <span class="font-outfit font-bold text-sm text-neonPink flex items-center gap-1.5">
              <span>⚠️</span> EXAM TRAP
            </span>
            <span class="text-[10px] font-mono text-neonPink bg-neonPink/10 px-2 py-0.5 rounded">WATCH OUT</span>
          </div>
          <div class="text-xs text-white font-medium">${escapeHTML(t.trap)}</div>
          <div class="text-xs text-neonGreen font-mono pt-1 border-t border-white/5 flex items-start gap-1">
            <span>✓</span> <span>Fix: ${escapeHTML(t.correction)}</span>
          </div>
        </div>
      `).join('');

      // 3. Quick Revision Cram Bullets (Neon Green)
      const bulletsBox = document.getElementById('supernotes-bullets-box');
      bulletsBox.innerHTML = (data.quickRevision || []).map(b => `
        <div class="flex items-start gap-3 text-xs sm:text-sm text-gray-200">
          <span class="text-neonGreen font-bold font-mono">⚡</span>
          <span>${escapeHTML(b)}</span>
        </div>
      `).join('');

      // 4. Formulas (Neon Cyan)
      const formulasGrid = document.getElementById('supernotes-formulas-grid');
      formulasGrid.innerHTML = (data.formulas || []).map(f => `
        <div class="p-4 rounded-2xl bg-[#0B0E14] border border-neonCyan/30 shadow-glow-cyan space-y-1.5">
          <div class="text-xs font-mono text-neonCyan font-bold">${escapeHTML(f.name)}</div>
          <div class="font-mono text-sm text-white bg-white/5 p-2 rounded">${escapeHTML(f.equation)}</div>
          <div class="text-[11px] text-gray-400 font-inter">${escapeHTML(f.variables)}</div>
        </div>
      `).join('');

      // 5. Mark-Graded Exam Q&As
      const qaList = document.getElementById('supernotes-qa-list');
      qaList.innerHTML = (data.examQA || []).map((qa, i) => `
        <div class="rounded-2xl glass-card border border-white/10 overflow-hidden">
          <div class="p-4 flex items-center justify-between cursor-pointer hover:bg-white/[0.02] transition-colors" onclick="toggleAccordion('qa-${i}')">
            <div class="flex items-center gap-3">
              <span class="px-2.5 py-1 rounded-full text-[11px] font-mono font-bold ${
                qa.marks === 1 ? 'bg-neonGreen/10 text-neonGreen border border-neonGreen/30' :
                qa.marks === 3 ? 'bg-neonCyan/10 text-neonCyan border border-neonCyan/30' :
                'bg-neonPurple/10 text-neonPurple border border-neonPurple/30'
              }">${qa.marks} MARK${qa.marks > 1 ? 'S' : ''}</span>
              <span class="font-outfit font-bold text-sm text-white">${escapeHTML(qa.q)}</span>
            </div>
            <span id="arrow-qa-${i}" class="text-xs text-gray-400 font-mono">▼</span>
          </div>
          <div id="body-qa-${i}" class="hidden p-4 bg-[#07080D]/90 border-t border-white/5 text-xs font-mono text-gray-300 whitespace-pre-line leading-relaxed">
            ${escapeHTML(qa.a)}
          </div>
        </div>
      `).join('');

      showScreen('screen-supernotes');
    }

    function toggleAccordion(id) {
      sfx.click();
      const body = document.getElementById('body-' + id);
      const arrow = document.getElementById('arrow-' + id);
      if (body) {
        body.classList.toggle('hidden');
        if (arrow) arrow.textContent = body.classList.contains('hidden') ? '▼' : '▲';
      }
    }

    /* ===================================================
       10B. FEATURE 4: INTERACTIVE CONCEPT MIND MAP ENGINE
       =================================================== */
    let currentMindmapLayout = 'dual-loop'; // 'dual-loop' | 'radial'
    let mindmapZoom = 1.0;
    let activeMindmapNodeTopic = '';

    const DEFAULT_BRANCH_COLORS = ['cyan', 'blue', 'purple', 'green', 'pink', 'yellow'];
    const DEFAULT_BRANCH_ICONS = ['💬', '🧩', '🎯', '🌿', '🎯', '⚖️'];

    function getDefaultMindMapData(title, grade) {
      const coreTitle = title || 'Visual Concept Topology';
      const levelText = grade || 'Undergraduate';
      return {
        central: {
          title: coreTitle,
          subtitle: `Calibrated for ${levelText} Syllabus`,
          takeaway: 'Core governing framework unifying theoretical foundations, physical pathways, and practical applications.'
        },
        branches: [
          {
            id: 'branch-1',
            side: 'left',
            position: 'top-left',
            color: 'cyan',
            icon: '💬',
            title: 'Core Foundations',
            subtitle: 'Essential baseline definitions, fundamental axioms, and preliminary system prerequisites.',
            takeaway: 'Frequently tested in Part A objective questions as foundational definitions.',
            connections: ['Dynamic Kinetics', 'Governing Derivations']
          },
          {
            id: 'branch-2',
            side: 'left',
            position: 'mid-left',
            color: 'blue',
            icon: '🧩',
            title: 'Dynamic Kinetics',
            subtitle: 'Reaction rates, threshold limits, catalysts, and state transition rates.',
            takeaway: 'High-yield examiner focus on rate-limiting steps and activation energies.',
            connections: ['Core Foundations', 'Reaction Pathways']
          },
          {
            id: 'branch-3',
            side: 'left',
            position: 'bottom-left',
            color: 'purple',
            icon: '🎯',
            title: 'Reaction Pathways',
            subtitle: 'Sequential intermediate transformations, carrier flows, and cyclic states.',
            takeaway: 'Step-marking rubrics award majority marks for naming intermediate molecules.',
            connections: ['Dynamic Kinetics', 'Thermodynamic Equilibrium']
          },
          {
            id: 'branch-4',
            side: 'right',
            position: 'top-right',
            color: 'green',
            icon: '🌿',
            title: 'Governing Derivations',
            subtitle: 'Mathematical formulations, dimensional consistency, and boundary constraints.',
            takeaway: 'Always state standard SI units and boundary initial conditions.',
            connections: ['Core Foundations', 'Thermodynamic Equilibrium']
          },
          {
            id: 'branch-5',
            side: 'right',
            position: 'mid-right',
            color: 'pink',
            icon: '🎯',
            title: 'Thermodynamic Equilibrium',
            subtitle: 'Dynamic reversibility, homeostatic compensation, and Le Chatelier shifts.',
            takeaway: 'When Delta G = 0, rates are balanced; stress induces predictable shifts.',
            connections: ['Reaction Pathways', 'Applied Systems']
          },
          {
            id: 'branch-6',
            side: 'right',
            position: 'bottom-right',
            color: 'yellow',
            icon: '⚖️',
            title: 'Applied Systems',
            subtitle: 'Practical experimental cases, industrial methodologies, and safety criteria.',
            takeaway: 'Top-scoring essay questions require real-world validation and safety trade-offs.',
            connections: ['Thermodynamic Equilibrium', 'Core Foundations']
          }
        ]
      };
    }

    function normalizeMindMapData(raw, title, grade) {
      if (!raw || typeof raw !== 'object') {
        return getDefaultMindMapData(title, grade);
      }

      const central = {
        title: String(raw.central?.title || title || 'Core Concept').trim(),
        subtitle: String(raw.central?.subtitle || `Calibrated for ${grade || 'Undergraduate'}`).trim(),
        takeaway: String(raw.central?.takeaway || 'Central governing system coordinating all functional branches.').trim()
      };

      let branches = Array.isArray(raw.branches) ? raw.branches : [];
      if (branches.length === 0) {
        return getDefaultMindMapData(title, grade);
      }

      // Ensure at least 6 branches by filling from defaults if needed
      const defaults = getDefaultMindMapData(title, grade).branches;
      const normalizedBranches = branches.map((b, i) => {
        const fallback = defaults[i % defaults.length];
        const color = b.color && DEFAULT_BRANCH_COLORS.includes(b.color.toLowerCase()) 
          ? b.color.toLowerCase() 
          : DEFAULT_BRANCH_COLORS[i % DEFAULT_BRANCH_COLORS.length];
        
        let connList = ['Core System'];
        if (Array.isArray(b.connections)) {
          connList = b.connections.map(c => String(c).trim()).filter(Boolean);
        } else if (typeof b.connections === 'string' && b.connections.trim()) {
          connList = b.connections.split(/[,;]+/).map(c => c.trim()).filter(Boolean);
        }
        if (connList.length === 0) connList = [fallback.connections[0] || 'Core System'];

        return {
          id: b.id || `branch-${i + 1}`,
          side: i < 3 ? 'left' : 'right',
          position: b.position || (i < 3 ? ['top-left', 'mid-left', 'bottom-left'][i] : ['top-right', 'mid-right', 'bottom-right'][i - 3]),
          color: color,
          icon: b.icon || DEFAULT_BRANCH_ICONS[i % DEFAULT_BRANCH_ICONS.length],
          title: String(b.title || fallback.title).trim(),
          subtitle: String(b.subtitle || fallback.subtitle).trim(),
          takeaway: String(b.takeaway || fallback.takeaway).trim(),
          connections: connList
        };
      });

      return { central, branches: normalizedBranches };
    }

    function openMindMap() {
      sfx.click();

      // Ensure active document or default state exists
      if (!state.analyzedData) {
        if (state.activeText && state.activeText.length > 20) {
          state.analyzedData = runLocalHeuristicEngine(state.activeText, state.level || 'Undergraduate');
        } else {
          // Provide rich instant sample so canvas is NEVER blank
          state.analyzedData = runLocalHeuristicEngine(PRESETS.bio, state.level || 'Undergraduate');
          state.activeDocTitle = 'Photosynthesis & Cellular Energetics';
          state.activeText = PRESETS.bio;
        }
      }

      // Ensure mindmap is normalized
      state.analyzedData.mindmap = normalizeMindMapData(
        state.analyzedData.mindmap,
        state.activeDocTitle || 'Lecture Material',
        state.level || 'Undergraduate'
      );

      const titleEl = document.getElementById('mindmap-doc-title');
      if (titleEl) {
        titleEl.textContent = (state.activeDocTitle || 'Lecture Material') + ' — Concept Topology';
      }
      const badgeEl = document.getElementById('mindmap-grade-badge');
      if (badgeEl) {
        badgeEl.textContent = `Calibrated for ${state.level || 'Undergraduate'}`;
      }

      // Reset zoom
      mindmapZoom = 1.0;

      showScreen('screen-mindmap');
      renderMindMap();
      renderMindMapLegendCards();
      setupMindMapInteractions();
    }

    function setMindmapLayout(layout) {
      sfx.click();
      currentMindmapLayout = layout;
      const btnDual = document.getElementById('mm-layout-dual');
      const btnRadial = document.getElementById('mm-layout-radial');
      if (layout === 'dual-loop') {
        if (btnDual) btnDual.className = 'px-3 py-1 rounded-lg bg-neonYellow/20 text-neonYellow font-bold transition-all';
        if (btnRadial) btnRadial.className = 'px-3 py-1 rounded-lg text-gray-400 hover:text-white transition-all';
      } else {
        if (btnDual) btnDual.className = 'px-3 py-1 rounded-lg text-gray-400 hover:text-white transition-all';
        if (btnRadial) btnRadial.className = 'px-3 py-1 rounded-lg bg-neonYellow/20 text-neonYellow font-bold transition-all';
      }
      renderMindMap();
    }

    function zoomMindMap(delta) {
      sfx.click();
      mindmapZoom = Math.min(Math.max(mindmapZoom * delta, 0.5), 2.5);
      applyMindMapTransform();
    }

    function resetMindMapZoom() {
      sfx.click();
      mindmapZoom = 1.0;
      applyMindMapTransform();
    }

    function applyMindMapTransform() {
      const g = document.getElementById('mindmap-svg-viewport');
      if (g) {
        // Zoom symmetrically centered at (500, 325) - perfectly stationary center without panning
        const cx = 500;
        const cy = 325;
        const tx = cx * (1 - mindmapZoom);
        const ty = cy * (1 - mindmapZoom);
        g.setAttribute('transform', `translate(${tx}, ${ty}) scale(${mindmapZoom})`);
      }
      const zoomText = `${Math.round(mindmapZoom * 100)}%`;
      const badge1 = document.getElementById('mm-zoom-level');
      if (badge1) badge1.textContent = zoomText;
      const badge2 = document.getElementById('mm-canvas-zoom-badge');
      if (badge2) badge2.textContent = zoomText;
    }

    function toggleMindMapFullscreen(forceState) {
      sfx.click();
      const container = document.getElementById('mindmap-canvas-container');
      const closeBtn = document.getElementById('mm-fs-close-btn');
      const fsLabel = document.getElementById('mm-fs-label');
      if (!container) return;

      const isCurrentlyFS = container.classList.contains('mindmap-fullscreen');
      const willBeFS = typeof forceState === 'boolean' ? forceState : !isCurrentlyFS;

      if (willBeFS) {
        container.classList.add('mindmap-fullscreen');
        if (closeBtn) closeBtn.classList.remove('hidden');
        if (fsLabel) fsLabel.textContent = 'Exit Full Screen';
        document.body.style.overflow = 'hidden';
      } else {
        container.classList.remove('mindmap-fullscreen');
        if (closeBtn) closeBtn.classList.add('hidden');
        if (fsLabel) fsLabel.textContent = 'Full Screen';
        document.body.style.overflow = '';
      }
      applyMindMapTransform();
    }

    function renderMindMap() {
      try {
        const viewport = document.getElementById('mindmap-svg-viewport');
        if (!viewport) return;

        // Ensure data exists and is properly structured
        if (!state.analyzedData || !state.analyzedData.mindmap) {
          state.analyzedData = state.analyzedData || {};
          state.analyzedData.mindmap = getDefaultMindMapData(state.activeDocTitle, state.level);
        }
        const data = state.analyzedData.mindmap;
        const branches = data.branches || [];

        const W = 1000;
        const H = 650;
        const cx = W / 2; // 500
        const cy = H / 2; // 325

        let svgHTML = '';

        if (currentMindmapLayout === 'dual-loop') {
          // ========================================================
          // DUAL-LOOP LAYOUT (Matching user reference template!)
          // Two connected loops: Left center 345, Right center 655, radius 140
          // ========================================================
          const leftLoopCx = 345;
          const rightLoopCx = 655;
          const loopR = 140;

          // 1. Dual Orbit Loops & Connecting Bridge
          svgHTML += `
            <!-- Dual Loop Orbit Rings -->
            <g opacity="0.6">
              <circle cx="${leftLoopCx}" cy="${cy}" r="${loopR}" fill="none" stroke="rgba(0, 229, 255, 0.35)" stroke-width="2.5" />
              <circle cx="${rightLoopCx}" cy="${cy}" r="${loopR}" fill="none" stroke="rgba(168, 85, 247, 0.35)" stroke-width="2.5" />
              <line x1="${leftLoopCx}" y1="${cy}" x2="${rightLoopCx}" y2="${cy}" stroke="rgba(255, 255, 255, 0.2)" stroke-width="1.5" stroke-dasharray="4,4" />
            </g>
          `;

          // 6 Fixed Branch Anchor Positions matching the template
          const fixedPositions = [
            // Left Loop: Top-Left, Mid-Left, Bottom-Left
            {
              orbX: 310, orbY: 185,
              pillX: 45, pillY: 140, pillW: 160, pillH: 34,
              stepPath: `M 310 185 L 310 157 L 205 157`,
              isLeft: true
            },
            {
              orbX: 205, orbY: 325,
              pillX: 35, pillY: 308, pillW: 160, pillH: 34,
              stepPath: `M 205 325 L 195 325`,
              isLeft: true
            },
            {
              orbX: 310, orbY: 465,
              pillX: 45, pillY: 476, pillW: 160, pillH: 34,
              stepPath: `M 310 465 L 310 493 L 205 493`,
              isLeft: true
            },
            // Right Loop: Top-Right, Mid-Right, Bottom-Right
            {
              orbX: 690, orbY: 185,
              pillX: 795, pillY: 140, pillW: 160, pillH: 34,
              stepPath: `M 690 185 L 690 157 L 795 157`,
              isLeft: false
            },
            {
              orbX: 795, orbY: 325,
              pillX: 805, pillY: 308, pillW: 160, pillH: 34,
              stepPath: `M 795 325 L 805 325`,
              isLeft: false
            },
            {
              orbX: 690, orbY: 465,
              pillX: 795, pillY: 476, pillW: 160, pillH: 34,
              stepPath: `M 690 465 L 690 493 L 795 493`,
              isLeft: false
            }
          ];

          // 2. Connector Lines
          branches.forEach((b, i) => {
            const pos = fixedPositions[i % fixedPositions.length];
            const hex = getBranchHexColor(b.color);
            svgHTML += `
              <path d="${pos.stepPath}" fill="none" stroke="${hex}" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" opacity="0.9" />
              <circle cx="${pos.orbX}" cy="${pos.orbY}" r="4" fill="${hex}" />
            `;
          });

          // 3. Central Hub (Silver Metallic core with ruby/crimson border matching template)
          const centralTitle = escapeHTML(truncate(data.central.title, 18));
          svgHTML += `
            <g class="cursor-pointer group" onclick="inspectMindMapNode(-1)">
              <!-- Outer Ruby Halo Ring -->
              <circle cx="${cx}" cy="${cy}" r="78" fill="rgba(225, 29, 72, 0.15)" stroke="url(#grad-ruby)" stroke-width="4" filter="url(#glow-pink)" />
              
              <!-- Metallic Silver Bevel Disc -->
              <circle cx="${cx}" cy="${cy}" r="68" fill="url(#grad-center)" stroke="#FFFFFF" stroke-width="2.5" filter="url(#orb-shadow)" />
              
              <!-- Dark Obsidian Core -->
              <circle cx="${cx}" cy="${cy}" r="55" fill="#0B0E14" stroke="rgba(255,255,255,0.3)" stroke-width="1.5" />
              
              <!-- Core Labels -->
              <text x="${cx}" y="${cy - 8}" text-anchor="middle" font-family="'Outfit', sans-serif" font-weight="900" font-size="14" fill="#FFFFFF">
                ${centralTitle}
              </text>
              <text x="${cx}" y="${cy + 11}" text-anchor="middle" font-family="'Space Mono', monospace" font-size="9" fill="#00E5FF" letter-spacing="1.5">
                CORE SYSTEM
              </text>
              <text x="${cx}" y="${cy + 25}" text-anchor="middle" font-family="'Space Mono', monospace" font-size="8" fill="#94A3B8">
                Click to Inspect
              </text>
            </g>
          `;

          // 4. Satellite Orbs & Pill Banners
          branches.forEach((b, i) => {
            const pos = fixedPositions[i % fixedPositions.length];
            const hex = getBranchHexColor(b.color);
            const gradId = getBranchGradientId(b.color);
            const filterId = getBranchFilterId(b.color);
            const isLeft = pos.isLeft;

            // 3D Spherical Satellite Orb
            svgHTML += `
              <g class="cursor-pointer group" onclick="inspectMindMapNode(${i})">
                <!-- Drop shadow & outer glow halo -->
                <circle cx="${pos.orbX}" cy="${pos.orbY}" r="38" fill="rgba(0,0,0,0.6)" stroke="${hex}" stroke-width="2.5" filter="${filterId}" />
                
                <!-- 3D Spherical Radial Gradient Body -->
                <circle cx="${pos.orbX}" cy="${pos.orbY}" r="32" fill="${gradId}" stroke="#FFFFFF" stroke-width="1.8" filter="url(#orb-shadow)" />
                
                <!-- Specular Highlight (Top-left shiny reflection) -->
                <ellipse cx="${pos.orbX - 8}" cy="${pos.orbY - 10}" rx="12" ry="7" fill="rgba(255,255,255,0.5)" transform="rotate(-30 ${pos.orbX - 8} ${pos.orbY - 10})" />
                
                <!-- Center Vector Icon -->
                <text x="${pos.orbX}" y="${pos.orbY + 8}" text-anchor="middle" font-size="20">
                  ${b.icon || '●'}
                </text>
              </g>
            `;

            // Horizontal Pill Banner & Subtitle Description
            const pillRadius = 17;
            const titleSafe = escapeHTML(truncate(b.title, 15));
            const subSafe = escapeHTML(truncate(b.subtitle, 32));
            const connSafe = escapeHTML(Array.isArray(b.connections) ? b.connections.slice(0, 2).join(' ➔ ') : 'Connected Node');

            // Left Pill: rounded on left side; Right Pill: rounded on right side
            svgHTML += `
              <g class="cursor-pointer group" onclick="inspectMindMapNode(${i})">
                <!-- Pill Shape -->
                <rect x="${pos.pillX}" y="${pos.pillY}" width="${pos.pillW}" height="${pos.pillH}" rx="${pillRadius}" fill="${hex}" filter="url(#orb-shadow)" />
                
                <!-- Pill Title Text -->
                <text x="${pos.pillX + (pos.pillW / 2)}" y="${pos.pillY + 21}" text-anchor="middle" font-family="'Outfit', sans-serif" font-weight="bold" font-size="12.5" fill="#000000">
                  ${titleSafe}
                </text>

                <!-- Subtitle Description below Pill -->
                <text x="${isLeft ? pos.pillX + pos.pillW : pos.pillX}" y="${pos.pillY + pos.pillH + 16}" text-anchor="${isLeft ? 'end' : 'start'}" font-family="'Inter', sans-serif" font-size="10.5" fill="#F1F5F9" font-weight="600">
                  ${subSafe}
                </text>
                
                <!-- Connection Pathway Monospace Subtext -->
                <text x="${isLeft ? pos.pillX + pos.pillW : pos.pillX}" y="${pos.pillY + pos.pillH + 30}" text-anchor="${isLeft ? 'end' : 'start'}" font-family="'Space Mono', monospace" font-size="8.5" fill="#94A3B8">
                  ${connSafe}
                </text>
              </g>
            `;
          });

        } else {
          // ========================================================
          // RADIAL STAR LAYOUT (Omnidirectional Topology)
          // ========================================================
          const radius = 220;
          const total = Math.max(branches.length, 1);
          const angleStep = (2 * Math.PI) / total;

          // Background Orbit Guide Rings
          svgHTML += `
            <circle cx="${cx}" cy="${cy}" r="${radius}" fill="none" stroke="rgba(255,230,0,0.2)" stroke-width="2" stroke-dasharray="6,6" />
            <circle cx="${cx}" cy="${cy}" r="${radius * 0.6}" fill="none" stroke="rgba(0,229,255,0.15)" stroke-width="1.5" />
          `;

          // Connecting Spokes
          branches.forEach((b, i) => {
            const angle = i * angleStep - Math.PI / 2;
            const nx = cx + radius * Math.cos(angle);
            const ny = cy + radius * Math.sin(angle);
            const hex = getBranchHexColor(b.color);

            svgHTML += `
              <line x1="${cx}" y1="${cy}" x2="${nx}" y2="${ny}" stroke="${hex}" stroke-width="2.5" stroke-dasharray="4,2" opacity="0.8" />
            `;
          });

          // Center Radial Core
          const centralTitle = escapeHTML(truncate(data.central.title, 16));
          svgHTML += `
            <g class="cursor-pointer" onclick="inspectMindMapNode(-1)">
              <circle cx="${cx}" cy="${cy}" r="72" fill="url(#grad-center)" stroke="#FFE600" stroke-width="3.5" filter="url(#glow-yellow)" />
              <circle cx="${cx}" cy="${cy}" r="56" fill="#0B0E14" />
              <text x="${cx}" y="${cy - 4}" text-anchor="middle" font-family="'Outfit', sans-serif" font-weight="900" font-size="13" fill="#FFFFFF">
                ${centralTitle}
              </text>
              <text x="${cx}" y="${cy + 15}" text-anchor="middle" font-family="'Space Mono', monospace" font-size="8.5" fill="#FFE600">
                RADIAL CORE
              </text>
            </g>
          `;

          // Radial Satellite Nodes
          branches.forEach((b, i) => {
            const angle = i * angleStep - Math.PI / 2;
            const nx = cx + radius * Math.cos(angle);
            const ny = cy + radius * Math.sin(angle);
            const hex = getBranchHexColor(b.color);
            const gradId = getBranchGradientId(b.color);
            const filterId = getBranchFilterId(b.color);
            const titleSafe = escapeHTML(truncate(b.title, 14));

            svgHTML += `
              <g class="cursor-pointer group" onclick="inspectMindMapNode(${i})">
                <circle cx="${nx}" cy="${ny}" r="38" fill="${gradId}" stroke="#FFFFFF" stroke-width="2" filter="${filterId}" />
                <text x="${nx}" y="${ny + 7}" text-anchor="middle" font-size="20">${b.icon || '●'}</text>
                
                <rect x="${nx - 65}" y="${ny + (ny > cy ? 44 : -68)}" width="130" height="28" rx="14" fill="#0B0E14" stroke="${hex}" stroke-width="1.8" />
                <text x="${nx}" y="${ny + (ny > cy ? 62 : -50)}" text-anchor="middle" font-family="'Outfit', sans-serif" font-weight="bold" font-size="11.5" fill="#FFFFFF">
                  ${titleSafe}
                </text>
              </g>
            `;
          });
        }

        viewport.innerHTML = svgHTML;
        applyMindMapTransform();

      } catch (err) {
        console.error('MindMap Render Error:', err);
        const viewport = document.getElementById('mindmap-svg-viewport');
        if (viewport) {
          viewport.innerHTML = `
            <text x="500" y="300" text-anchor="middle" fill="#FF2A6D" font-family="'Outfit', sans-serif" font-size="18" font-weight="bold">
              Topology Rendering Diagnostic
            </text>
            <text x="500" y="330" text-anchor="middle" fill="#E2E8F0" font-family="'Space Mono', monospace" font-size="12">
              ${escapeHTML(err.message || 'Error initializing graph')}
            </text>
            <rect x="420" y="360" width="160" height="36" rx="18" fill="#00E5FF" class="cursor-pointer" onclick="openMindMap()" />
            <text x="500" y="383" text-anchor="middle" fill="#000000" font-family="'Outfit', sans-serif" font-size="12" font-weight="bold" class="cursor-pointer" onclick="openMindMap()">
              Reload Graph
            </text>
          `;
        }
      }
    }

    function getBranchHexColor(color = '') {
      switch (String(color).toLowerCase()) {
        case 'cyan': return '#00E5FF';
        case 'blue': return '#0284C7';
        case 'green': return '#10B981';
        case 'purple': return '#A855F7';
        case 'pink': return '#FF2A6D';
        case 'yellow': return '#F59E0B';
        case 'amber': return '#F97316';
        default: return '#00E5FF';
      }
    }

    function getBranchGradientId(color = '') {
      switch (String(color).toLowerCase()) {
        case 'cyan': return 'url(#grad-cyan)';
        case 'blue': return 'url(#grad-blue)';
        case 'green': return 'url(#grad-green)';
        case 'purple': return 'url(#grad-purple)';
        case 'pink': return 'url(#grad-pink)';
        case 'yellow': return 'url(#grad-yellow)';
        case 'amber': return 'url(#grad-amber)';
        default: return 'url(#grad-cyan)';
      }
    }

    function getBranchFilterId(color = '') {
      switch (String(color).toLowerCase()) {
        case 'cyan': return 'url(#glow-cyan)';
        case 'blue': return 'url(#glow-blue)';
        case 'green': return 'url(#glow-green)';
        case 'purple': return 'url(#glow-purple)';
        case 'pink': return 'url(#glow-pink)';
        case 'yellow': return 'url(#glow-yellow)';
        default: return 'url(#glow-cyan)';
      }
    }

    function truncate(str = '', max = 20) {
      if (!str) return '';
      return str.length > max ? str.slice(0, max - 1) + '…' : str;
    }

    // Node Inspector Handling
    function inspectMindMapNode(idx) {
      sfx.click();
      const mm = state.analyzedData?.mindmap;
      if (!mm) return;

      const inspector = document.getElementById('mindmap-inspector');
      const iconEl = document.getElementById('inspector-icon');
      const badgeEl = document.getElementById('inspector-badge');
      const titleEl = document.getElementById('inspector-title');
      const descEl = document.getElementById('inspector-desc');
      const takeawayEl = document.getElementById('inspector-takeaway');
      const connEl = document.getElementById('inspector-connections');

      if (!inspector) return;

      if (idx === -1) {
        // Central Node
        activeMindmapNodeTopic = mm.central.title;
        if (iconEl) iconEl.textContent = '🧠';
        if (badgeEl) {
          badgeEl.textContent = 'CENTRAL SUBJECT HUB';
          badgeEl.className = 'px-2 py-0.5 rounded text-[10px] font-mono bg-neonYellow/20 text-neonYellow border border-neonYellow/30';
          badgeEl.style.borderColor = '';
          badgeEl.style.color = '';
        }
        if (titleEl) titleEl.textContent = mm.central.title;
        if (descEl) descEl.textContent = `${mm.central.subtitle}. This central node coordinates all functional sub-concepts, thermodynamic flows, and governing equations.`;
        if (takeawayEl) takeawayEl.textContent = mm.central.takeaway;
        if (connEl) {
          connEl.innerHTML = (mm.branches || []).map(b => `
            <li class="flex items-center gap-1.5"><span class="text-neonYellow">➔</span> ${escapeHTML(b.title)} (${escapeHTML(b.subtitle.slice(0, 30))}...)</li>
          `).join('');
        }
      } else {
        const b = (mm.branches || [])[idx];
        if (!b) return;
        activeMindmapNodeTopic = b.title;
        if (iconEl) iconEl.textContent = b.icon || '💡';
        const hex = getBranchHexColor(b.color);
        if (badgeEl) {
          badgeEl.textContent = `BRANCH #${idx + 1} • ${b.color.toUpperCase()}`;
          badgeEl.style.borderColor = hex;
          badgeEl.style.color = hex;
          badgeEl.className = 'px-2 py-0.5 rounded text-[10px] font-mono bg-white/5 border';
        }
        if (titleEl) titleEl.textContent = b.title;
        if (descEl) descEl.textContent = b.subtitle;
        if (takeawayEl) takeawayEl.textContent = b.takeaway;
        
        const connList = Array.isArray(b.connections) ? b.connections : [String(b.connections || 'Core System')];
        if (connEl) {
          connEl.innerHTML = connList.map(c => `
            <li class="flex items-center gap-1.5"><span class="text-neonCyan">⇄</span> ${escapeHTML(c)}</li>
          `).join('');
        }
      }

      inspector.classList.remove('hidden');
    }

    function closeMindMapInspector() {
      sfx.click();
      const inspector = document.getElementById('mindmap-inspector');
      if (inspector) inspector.classList.add('hidden');
    }

    function openQuizForConcept(conceptTitle) {
      sfx.click();
      closeMindMapInspector();
      if (!state.analyzedData) return;
      openAdaptiveQuiz();
    }

    function renderMindMapLegendCards() {
      const mm = state.analyzedData?.mindmap;
      if (!mm || !mm.branches) return;

      const grid = document.getElementById('mindmap-nodes-grid');
      if (!grid) return;

      grid.innerHTML = mm.branches.map((b, i) => {
        const hex = getBranchHexColor(b.color);
        return `
          <div class="p-4 rounded-2xl glass-card border border-white/10 hover:border-white/30 transition-all cursor-pointer group flex flex-col justify-between"
               onclick="inspectMindMapNode(${i})">
            <div>
              <div class="flex items-center justify-between mb-2">
                <span class="text-2xl">${b.icon || '●'}</span>
                <span class="text-[10px] font-mono px-2 py-0.5 rounded-full" style="color: ${hex}; border: 1px solid ${hex}; background: ${hex}15;">
                  BRANCH ${i + 1}
                </span>
              </div>
              <h5 class="font-outfit font-bold text-base text-white group-hover:text-neonYellow transition-colors">
                ${escapeHTML(b.title)}
              </h5>
              <p class="text-xs text-gray-400 mt-1 line-clamp-2 leading-relaxed">
                ${escapeHTML(b.subtitle)}
              </p>
            </div>
            <div class="mt-3 pt-2 border-t border-white/5 flex items-center justify-between text-[11px] font-mono text-gray-500 group-hover:text-neonYellow">
              <span>Inspect on Map</span>
              <span>➔</span>
            </div>
          </div>
        `;
      }).join('');
    }

    // Mind Map Interactions (Smooth mouse wheel zoom, NO dragging)
    function setupMindMapInteractions() {
      const container = document.getElementById('mindmap-canvas-container');
      if (!container || container.dataset.interactionsInitialized) return;
      container.dataset.interactionsInitialized = 'true';

      // Wheel Zoom (Centered, no dragging)
      container.addEventListener('wheel', (e) => {
        e.preventDefault();
        const delta = e.deltaY < 0 ? 1.08 : 0.92;
        zoomMindMap(delta);
      }, { passive: false });

      // Escape key to exit fullscreen presentation
      window.addEventListener('keydown', (e) => {
        if (e.key === 'Escape') {
          const container = document.getElementById('mindmap-canvas-container');
          if (container && container.classList.contains('mindmap-fullscreen')) {
            toggleMindMapFullscreen(false);
          }
        }
      });
    }

    function exportMindMapSVG() {
      sfx.click();
      const svg = document.getElementById('mindmap-svg');
      if (!svg) return;
      const serializer = new XMLSerializer();
      const source = serializer.serializeToString(svg);
      const blob = new Blob([source], { type: 'image/svg+xml;charset=utf-8' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `${(state.activeDocTitle || 'edu_ai')}_mind_map.svg`;
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      URL.revokeObjectURL(url);
    }

    /* ===================================================
       11. PROFILE, ANIME AVATARS & SETTINGS ENGINE
       =================================================== */
    const DEFAULT_AVATARS = [
      {
        id: 'naruto',
        name: 'Naruto Uzumaki',
        tag: '🍥 Hokage Mode',
        color: '#FF7700',
        bg: 'from-amber-500/20 to-orange-600/30',
        border: 'border-orange-500',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#120c04" stroke="#ff7700" stroke-width="3"/><circle cx="50" cy="50" r="32" fill="none" stroke="#ff9900" stroke-width="2" stroke-dasharray="4,3"/><rect x="25" y="28" width="50" height="14" rx="3" fill="#333" stroke="#bbb" stroke-width="1.5"/><circle cx="50" cy="35" r="4" fill="none" stroke="#fff" stroke-width="1.5"/><path d="M50 31 A 4 4 0 0 1 54 35 A 2 2 0 0 1 52 37" fill="none" stroke="#fff" stroke-width="1.2"/><circle cx="38" cy="55" r="3" fill="#00E5FF"/><circle cx="62" cy="55" r="3" fill="#00E5FF"/><path d="M42 68 Q50 75 58 68" stroke="#ff7700" stroke-width="2.5" fill="none" stroke-linecap="round"/><path d="M28 58 Q34 57 32 63 M26 62 Q32 61 30 67 M68 58 Q74 57 72 63 M70 62 Q76 61 74 67" stroke="#ff5500" stroke-width="1.5" stroke-linecap="round"/></svg>`
      },
      {
        id: 'kakashi',
        name: 'Kakashi Hatake',
        tag: '⚡ Copy Ninja',
        color: '#00E5FF',
        bg: 'from-cyan-500/20 to-blue-600/30',
        border: 'border-cyan-400',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#061019" stroke="#00E5FF" stroke-width="3"/><rect x="25" y="24" width="50" height="14" rx="3" fill="#333" stroke="#888" stroke-width="1.5"/><path d="M30 31 L70 31 M50 26 L50 36" stroke="#00E5FF" stroke-width="1.5"/><path d="M25 40 L45 75 L25 75 Z" fill="#222" opacity="0.6"/><circle cx="38" cy="48" r="4" fill="#ff2a6d"/><circle cx="38" cy="48" r="1.5" fill="#000"/><circle cx="62" cy="48" r="3" fill="#bbb"/><path d="M30 58 Q50 78 70 58 L70 82 Q50 88 30 82 Z" fill="#1b2533" stroke="#00e5ff" stroke-width="1.5"/><path d="M46 72 Q50 75 54 72" stroke="#555" stroke-width="1.5"/></svg>`
      },
      {
        id: 'sasuke',
        name: 'Sasuke Uchiha',
        tag: '🗡️ Rinnegan & Chidori',
        color: '#A855F7',
        bg: 'from-purple-500/20 to-indigo-600/30',
        border: 'border-purple-500',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#0d0718" stroke="#A855F7" stroke-width="3"/><path d="M25 35 Q50 18 75 35 Q70 65 50 68 Q30 65 25 35 Z" fill="#0a0515" stroke="#443366" stroke-width="1.5"/><circle cx="38" cy="50" r="4" fill="#ff0055"/><circle cx="38" cy="50" r="2" fill="#000"/><circle cx="62" cy="50" r="4" fill="#a855f7"/><circle cx="62" cy="50" r="2" fill="#fff"/><circle cx="62" cy="50" r="6" fill="none" stroke="#a855f7" stroke-width="1"/><path d="M44 65 Q50 68 56 65" stroke="#a855f7" stroke-width="2" fill="none" stroke-linecap="round"/><path d="M50 20 L50 32 M45 28 L55 28" stroke="#ff0055" stroke-width="2"/></svg>`
      },
      {
        id: 'luffy',
        name: 'Monkey D. Luffy',
        tag: '👒 Straw Hat Captain',
        color: '#FF2A6D',
        bg: 'from-red-500/20 to-amber-600/30',
        border: 'border-red-500',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#19060b" stroke="#FF2A6D" stroke-width="3"/><ellipse cx="50" cy="35" rx="36" ry="12" fill="#d97706" stroke="#b45309" stroke-width="1.5"/><ellipse cx="50" cy="35" rx="24" ry="7" fill="#dc2626"/><circle cx="50" cy="30" r="16" fill="#d97706"/><circle cx="38" cy="52" r="3" fill="#fff"/><circle cx="62" cy="52" r="3" fill="#fff"/><circle cx="38" cy="52" r="1.5" fill="#000"/><circle cx="62" cy="52" r="1.5" fill="#000"/><path d="M34 58 L42 62" stroke="#ff2a6d" stroke-width="1.5"/><path d="M36 68 Q50 82 64 68 Z" fill="#fff" stroke="#ff2a6d" stroke-width="2"/><path d="M44 74 L56 74" stroke="#ff2a6d" stroke-width="1"/></svg>`
      },
      {
        id: 'zoro',
        name: 'Roronoa Zoro',
        tag: '⚔️ King of Hell',
        color: '#00FF88',
        bg: 'from-emerald-500/20 to-teal-600/30',
        border: 'border-emerald-400',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#04140d" stroke="#00FF88" stroke-width="3"/><path d="M24 35 Q50 20 76 35 L72 45 Q50 38 28 45 Z" fill="#065f46" stroke="#00ff88" stroke-width="1.5"/><path d="M32 46 L38 56" stroke="#ff2a6d" stroke-width="2"/><circle cx="62" cy="50" r="3" fill="#00ff88"/><circle cx="62" cy="50" r="1.5" fill="#000"/><circle cx="36" cy="50" r="3" fill="#111"/><line x1="33" y1="47" x2="39" y2="53" stroke="#ff2a6d" stroke-width="1.5"/><path d="M40 68 Q50 64 60 68" stroke="#00ff88" stroke-width="2.5" fill="none" stroke-linecap="round"/><circle cx="28" cy="60" r="2" fill="#facc15"/><circle cx="28" cy="65" r="2" fill="#facc15"/><circle cx="28" cy="70" r="2" fill="#facc15"/></svg>`
      },
      {
        id: 'goku',
        name: 'Goku (Super Saiyan)',
        tag: '🐉 Saiyan Ki',
        color: '#FACC15',
        bg: 'from-amber-400/20 to-yellow-600/30',
        border: 'border-yellow-400',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#171203" stroke="#FACC15" stroke-width="3"/><path d="M50 14 L56 30 L72 20 L66 36 L84 34 L70 48 L80 62 L64 56 L62 76 L50 60 L38 76 L36 56 L20 62 L30 48 L16 34 L34 36 L28 20 L44 30 Z" fill="#facc15" opacity="0.85" stroke="#ea580c" stroke-width="1.5"/><circle cx="38" cy="50" r="3" fill="#00E5FF"/><circle cx="62" cy="50" r="3" fill="#00E5FF"/><path d="M34 46 L42 48 M66 46 L58 48" stroke="#000" stroke-width="2"/><path d="M42 66 Q50 72 58 66" stroke="#f97316" stroke-width="2.5" fill="none" stroke-linecap="round"/></svg>`
      },
      {
        id: 'gojo',
        name: 'Gojo Satoru',
        tag: '🐱 Six Eyes & Infinity',
        color: '#00E5FF',
        bg: 'from-sky-500/20 to-indigo-600/30',
        border: 'border-sky-400',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#050d1a" stroke="#00E5FF" stroke-width="3"/><path d="M22 42 Q50 28 78 42 L78 54 Q50 44 22 54 Z" fill="#1e1b4b" stroke="#00e5ff" stroke-width="2"/><circle cx="38" cy="48" r="4" fill="#38bdf8"/><circle cx="38" cy="48" r="2" fill="#fff"/><circle cx="62" cy="48" r="4" fill="#38bdf8"/><circle cx="62" cy="48" r="2" fill="#fff"/><path d="M20 28 Q50 15 80 28 Q75 40 50 38 Q25 40 20 28 Z" fill="#f8fafc" stroke="#94a3b8" stroke-width="1"/><path d="M44 68 Q50 73 56 68" stroke="#38bdf8" stroke-width="2.5" fill="none" stroke-linecap="round"/></svg>`
      },
      {
        id: 'killua',
        name: 'Killua Zoldyck',
        tag: '⚡ Godspeed Aura',
        color: '#A855F7',
        bg: 'from-violet-500/20 to-fuchsia-600/30',
        border: 'border-violet-400',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#0f0719" stroke="#A855F7" stroke-width="3"/><path d="M18 36 L30 18 L42 34 L54 16 L66 34 L78 18 L86 38 L76 52 L84 66 L68 62 L58 78 L50 64 L42 78 L32 62 L16 66 L24 52 Z" fill="#e2e8f0" stroke="#a855f7" stroke-width="1.5"/><circle cx="38" cy="50" r="4" fill="#3b82f6"/><circle cx="62" cy="50" r="4" fill="#3b82f6"/><path d="M42 66 Q50 70 58 66" stroke="#a855f7" stroke-width="2" fill="none" stroke-linecap="round"/><path d="M30 30 L36 38 L44 32 M68 30 L62 38 L54 32" stroke="#a855f7" stroke-width="1.5"/></svg>`
      },
      {
        id: 'kurama',
        name: 'Kurama Nine-Tails',
        tag: '🦊 Tailed Beast',
        color: '#FF5500',
        bg: 'from-orange-600/20 to-red-600/30',
        border: 'border-orange-600',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#140602" stroke="#FF5500" stroke-width="3"/><path d="M22 26 L38 42 L24 58 Z M78 26 L62 42 L76 58 Z" fill="#ea580c" stroke="#ff5500" stroke-width="1.5"/><circle cx="38" cy="52" r="4" fill="#dc2626"/><circle cx="62" cy="52" r="4" fill="#dc2626"/><line x1="38" y1="48" x2="38" y2="56" stroke="#000" stroke-width="2"/><line x1="62" y1="48" x2="62" y2="56" stroke="#000" stroke-width="2"/><path d="M36 68 Q50 80 64 68 Z" fill="#450a0a" stroke="#ff5500" stroke-width="1.5"/><polygon points="42,68 44,72 46,68 48,72 50,68 52,72 54,68 56,72 58,68" fill="#fff"/></svg>`
      },
      {
        id: 'cyberpunk',
        name: 'Cyber Samurai',
        tag: '🤖 Neon Android',
        color: '#00FF88',
        bg: 'from-teal-500/20 to-emerald-600/30',
        border: 'border-neonGreen',
        svg: `<svg viewBox="0 0 100 100" class="w-full h-full"><circle cx="50" cy="50" r="46" fill="#041209" stroke="#00FF88" stroke-width="3"/><rect x="30" y="30" width="40" height="42" rx="8" fill="#0f172a" stroke="#00ff88" stroke-width="2"/><rect x="34" y="44" width="32" height="8" rx="2" fill="#00ff88" opacity="0.9"/><line x1="30" y1="58" x2="70" y2="58" stroke="#00ff88" stroke-width="1.5"/><circle cx="38" cy="37" r="2" fill="#00E5FF"/><circle cx="62" cy="37" r="2" fill="#00E5FF"/><line x1="50" y1="20" x2="50" y2="30" stroke="#00ff88" stroke-width="2"/></svg>`
      }
    ];

    function getAvatarHTML(sizeClass = 'w-full h-full') {
      if (state.userCustomAvatar) {
        return `<img src="${state.userCustomAvatar}" class="${sizeClass} object-cover rounded-xl" alt="Custom Profile">`;
      }
      const found = DEFAULT_AVATARS.find(a => a.id === state.userAvatar) || DEFAULT_AVATARS[0];
      return `<div class="${sizeClass}">${found.svg}</div>`;
    }

    function renderNavAvatar() {
      const wrap = document.getElementById('nav-avatar-icon-wrap');
      if (wrap) wrap.innerHTML = getAvatarHTML();
      const nameEl = document.getElementById('nav-user-name');
      if (nameEl) nameEl.textContent = state.userName || 'Naruto Uzumaki';
    }

    function openProfileSettingsModal() {
      sfx.click();
      const modal = document.getElementById('profile-settings-modal');
      document.getElementById('profile-name-input').value = state.userName;
      document.getElementById('settings-gemini-key').value = state.geminiKey;
      document.getElementById('settings-gemini-model').value = state.geminiModel;
      document.getElementById('settings-sound-toggle').checked = state.soundEnabled;
      document.getElementById('tts-rate-slider').value = state.ttsRate || 1.0;
      document.getElementById('tts-rate-label').textContent = (state.ttsRate || 1.0) + 'x';
      
      const lvlText = document.getElementById('profile-current-level');
      if (lvlText) lvlText.textContent = state.levelBadge || '🎓 Undergraduate';

      // Update stat counters
      document.getElementById('pmodal-stat-docs').textContent = state.stats.docsAnalyzed;
      document.getElementById('pmodal-stat-quizzes').textContent = state.stats.quizzesTaken;
      document.getElementById('pmodal-stat-weak').textContent = state.stats.weakCleared;
      document.getElementById('pmodal-stat-acc').textContent = state.stats.quizzesTaken ? `${state.stats.totalAccuracy}%` : '0%';

      updateModalHeaderAvatar();
      renderAnimeAvatarsGrid();
      switchProfileModalTab('avatar');
      modal.classList.remove('hidden');
    }

    function closeProfileSettingsModal() {
      sfx.click();
      document.getElementById('profile-settings-modal').classList.add('hidden');
    }

    function switchProfileModalTab(tab) {
      sfx.click();
      const tabs = ['avatar', 'general', 'ai', 'stats'];
      tabs.forEach(t => {
        const btn = document.getElementById(`pmodal-tab-${t}`);
        const pane = document.getElementById(`pmodal-pane-${t}`);
        if (t === tab) {
          btn.className = 'px-4 py-2 rounded-xl bg-neonCyan/15 text-neonCyan border border-neonCyan/40 font-bold transition-all';
          pane.classList.remove('hidden');
        } else {
          btn.className = 'px-4 py-2 rounded-xl text-gray-400 hover:text-white hover:bg-white/5 border border-transparent transition-all';
          pane.classList.add('hidden');
        }
      });
    }

    function updateModalHeaderAvatar() {
      const headerAvatar = document.getElementById('modal-header-avatar');
      if (headerAvatar) headerAvatar.innerHTML = getAvatarHTML();
      const userTitle = document.getElementById('modal-user-title');
      if (userTitle) userTitle.textContent = `${state.userName} • Settings`;
    }

    function renderAnimeAvatarsGrid() {
      const grid = document.getElementById('anime-avatars-grid');
      if (!grid) return;
      grid.innerHTML = DEFAULT_AVATARS.map(a => {
        const isSelected = !state.userCustomAvatar && state.userAvatar === a.id;
        return `
          <button type="button" onclick="selectAvatar('${a.id}')"
            class="group p-2.5 rounded-2xl glass-card border ${isSelected ? 'border-neonCyan ring-2 ring-neonCyan/60 bg-neonCyan/10 shadow-glow-cyan' : 'border-white/10 hover:border-white/30'} flex flex-col items-center text-center transition-all duration-200 transform hover:scale-105 focus:outline-none">
            <div class="w-14 h-14 rounded-xl overflow-hidden p-1 bg-black/60 border border-white/10 group-hover:scale-110 transition-transform">
              ${a.svg}
            </div>
            <div class="mt-2 text-xs font-outfit font-bold text-white group-hover:text-neonCyan truncate w-full">
              ${escapeHTML(a.name)}
            </div>
            <div class="text-[10px] font-mono text-gray-400 truncate w-full">
              ${escapeHTML(a.tag)}
            </div>
          </button>
        `;
      }).join('');
    }

    function selectAvatar(id) {
      sfx.click();
      state.userAvatar = id;
      state.userCustomAvatar = '';
      localStorage.setItem('eduai_user_avatar', id);
      localStorage.removeItem('eduai_user_custom_avatar');
      updateModalHeaderAvatar();
      renderAnimeAvatarsGrid();
      renderNavAvatar();
    }

    function handleCustomAvatarUpload(input) {
      if (input.files && input.files[0]) {
        sfx.click();
        const reader = new FileReader();
        reader.onload = (e) => {
          state.userCustomAvatar = e.target.result;
          localStorage.setItem('eduai_user_custom_avatar', state.userCustomAvatar);
          updateModalHeaderAvatar();
          renderAnimeAvatarsGrid();
          renderNavAvatar();
          sfx.success();
        };
        reader.readAsDataURL(input.files[0]);
      }
    }

    function randomizeAnimeAvatar() {
      sfx.click();
      const current = state.userAvatar;
      const filtered = DEFAULT_AVATARS.filter(a => a.id !== current);
      const random = filtered[Math.floor(Math.random() * filtered.length)] || DEFAULT_AVATARS[0];
      selectAvatar(random.id);
    }

    function setThemeAccent(name, hex) {
      sfx.click();
      state.accentColor = name;
      localStorage.setItem('eduai_accent_color', name);
      sfx.chime();
    }

    function saveProfileSettings() {
      sfx.click();
      const nameInput = document.getElementById('profile-name-input').value.trim();
      if (nameInput) {
        state.userName = nameInput;
        localStorage.setItem('eduai_user_name', nameInput);
      }

      state.soundEnabled = document.getElementById('settings-sound-toggle').checked;
      localStorage.setItem('eduai_sound_enabled', state.soundEnabled);

      state.ttsRate = parseFloat(document.getElementById('tts-rate-slider').value) || 1.0;
      localStorage.setItem('eduai_tts_rate', state.ttsRate);

      state.geminiKey = document.getElementById('settings-gemini-key').value.trim();
      state.geminiModel = document.getElementById('settings-gemini-model').value;
      localStorage.setItem('eduai_gemini_key', state.geminiKey);
      localStorage.setItem('eduai_gemini_model', state.geminiModel);

      // Update AI badge
      const dot = document.getElementById('ai-status-dot');
      const lbl = document.getElementById('ai-status-label');
      if (state.geminiKey) {
        dot.className = 'w-2 h-2 rounded-full bg-neonCyan animate-ping';
        lbl.textContent = 'Gemini 2.5 Active';
      } else {
        dot.className = 'w-2 h-2 rounded-full bg-neonGreen animate-pulse';
        lbl.textContent = 'Mock AI Active';
      }

      renderNavAvatar();
      closeProfileSettingsModal();
      sfx.success();
    }

    function exportStudyDataJSON() {
      sfx.click();
      const payload = {
        user: state.userName,
        avatar: state.userAvatar,
        educationLevel: state.level,
        stats: state.stats,
        lastDocument: state.activeDocTitle,
        exportedAt: new Date().toISOString()
      };
      const blob = new Blob([JSON.stringify(payload, null, 2)], { type: 'application/json' });
      const a = document.createElement('a');
      a.href = URL.createObjectURL(blob);
      a.download = `eduai-data-${Date.now()}.json`;
      a.click();
    }

    function resetAllStudyData() {
      if (confirm('Are you sure you want to reset all cached progress, quiz scores, and weak points?')) {
        sfx.error();
        localStorage.clear();
        state.stats = { docsAnalyzed: 0, weakCleared: 0, quizzesTaken: 0, totalAccuracy: 0 };
        location.reload();
      }
    }

    // Helper script loader
    function loadDynamicScript(src) {
      return new Promise((resolve, reject) => {
        if (document.querySelector(`script[src="${src}"]`)) return resolve();
        const s = document.createElement('script');
        s.src = src;
        s.onload = resolve;
        s.onerror = reject;
        document.head.appendChild(s);
      });
    }

    // Bind settings button to profile modal
    const openSettingsBtn = document.getElementById('open-settings-btn');
    if (openSettingsBtn) {
      openSettingsBtn.onclick = openProfileSettingsModal;
    }

    // Initialize initial badges & avatars
    renderNavAvatar();
    if (state.level) {
      updateNavBadge();
    }
    if (state.geminiKey) {
      document.getElementById('ai-status-dot').className = 'w-2 h-2 rounded-full bg-neonCyan animate-ping';
      document.getElementById('ai-status-label').textContent = 'Gemini 2.5 Active';
    }
    document.getElementById('stat-docs').textContent = `${state.stats.docsAnalyzed} Docs`;
    document.getElementById('stat-weak').textContent = `${state.stats.weakCleared} Cleared`;
    document.getElementById('stat-accuracy').textContent = state.stats.quizzesTaken ? `${state.stats.totalAccuracy}% Mastery` : '--% Mastery';

    // Hash navigation helper
    if (window.location.hash === '#mindmap') {
      setTimeout(() => openMindMap(), 150);
    }
  </script>
</body>
</html>
