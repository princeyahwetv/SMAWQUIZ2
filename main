<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ISTEPS Welding Process Quiz</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&amp;family=Orbitron:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
        * { box-sizing: border-box; }
        
        .font-rajdhani { font-family: 'Rajdhani', sans-serif; }
        .font-orbitron { font-family: 'Orbitron', sans-serif; }
        
        @keyframes pulse-glow {
            0%, 100% { box-shadow: 0 0 20px rgba(251, 146, 60, 0.3); }
            50% { box-shadow: 0 0 40px rgba(251, 146, 60, 0.6); }
        }
        
        @keyframes spark {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-20px) scale(0); opacity: 0; }
        }
        
        @keyframes slide-up {
            from { transform: translateY(30px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        @keyframes progress-fill {
            from { width: 0; }
        }
        
        .animate-pulse-glow { animation: pulse-glow 2s ease-in-out infinite; }
        .animate-slide-up { animation: slide-up 0.5s ease-out forwards; }
        
        .spark {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #fb923c;
            border-radius: 50%;
            animation: spark 0.8s ease-out forwards;
        }
        
        .option-btn {
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .option-btn:hover:not(:disabled) {
            transform: translateX(8px);
            background: rgba(251, 146, 60, 0.15);
        }
        
        .option-btn::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 4px;
            background: #fb923c;
            transform: scaleY(0);
            transition: transform 0.3s ease;
        }
        
        .option-btn:hover::before { transform: scaleY(1); }
        
        .option-btn.selected {
            background: rgba(251, 146, 60, 0.2);
            border-color: #fb923c;
        }
        
        .option-btn.correct {
            background: rgba(34, 197, 94, 0.2);
            border-color: #22c55e;
        }
        
        .option-btn.incorrect {
            background: rgba(239, 68, 68, 0.2);
            border-color: #ef4444;
        }
        
        .welding-bg {
            background: 
                radial-gradient(ellipse at 20% 80%, rgba(251, 146, 60, 0.1) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 20%, rgba(59, 130, 246, 0.08) 0%, transparent 50%),
                linear-gradient(180deg, #0f172a 0%, #1e293b 50%, #0f172a 100%);
        }
        
        .card-glass {
            background: linear-gradient(135deg, rgba(30, 41, 59, 0.9) 0%, rgba(15, 23, 42, 0.95) 100%);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(251, 146, 60, 0.2);
        }
        
        .progress-bar {
            background: linear-gradient(90deg, #fb923c, #f97316, #ea580c);
            box-shadow: 0 0 10px rgba(251, 146, 60, 0.5);
        }
        
        .section-badge {
            background: linear-gradient(135deg, rgba(251, 146, 60, 0.2), rgba(234, 88, 12, 0.1));
            border: 1px solid rgba(251, 146, 60, 0.3);
        }
        
        .stats-card {
            background: linear-gradient(135deg, rgba(251, 146, 60, 0.1), transparent);
            border: 1px solid rgba(251, 146, 60, 0.2);
        }
        
        .torch-icon {
            filter: drop-shadow(0 0 8px rgba(251, 146, 60, 0.6));
        }
    </style>
  <style>body { box-sizing: border-box; }</style>
 </head>
 <body class="h-full font-rajdhani text-slate-100 welding-bg overflow-auto">
  <div id="app" class="min-h-full w-full">
   <!-- Welcome Screen -->
   <div id="welcome-screen" class="min-h-full flex flex-col items-center justify-center p-6">
    <div class="card-glass rounded-3xl p-8 md:p-12 max-w-2xl w-full text-center animate-slide-up">
     <!-- Welding Torch Icon -->
     <div class="mb-6 torch-icon">
      <svg class="w-24 h-24 mx-auto" viewbox="0 0 100 100" fill="none">
       <path d="M50 10 L55 30 L60 25 L58 40 L65 35 L55 55 L50 50 L45 55 L35 35 L42 40 L40 25 L45 30 Z" fill="url(#flame-gradient)" class="animate-pulse" /> <rect x="45" y="50" width="10" height="35" rx="2" fill="#64748b" /> <rect x="42" y="82" width="16" height="8" rx="2" fill="#475569" /> <defs>
        <lineargradient id="flame-gradient" x1="50" y1="10" x2="50" y2="55">
         <stop offset="0%" stop-color="#fbbf24" />
         <stop offset="50%" stop-color="#fb923c" />
         <stop offset="100%" stop-color="#ea580c" />
        </lineargradient>
       </defs>
      </svg>
     </div>
     <h1 id="site-title" class="font-orbitron text-3xl md:text-4xl font-bold mb-4 bg-gradient-to-r from-orange-400 via-amber-400 to-orange-500 bg-clip-text text-transparent">ISTEPS-TLE WELDING Lesson 2 Quiz</h1>
     <p id="welcome-msg" class="text-slate-300 text-lg mb-8">Master the fundamentals of welding processes through this comprehensive quiz</p><!-- Section Overview --> <!-- Student Name Input -->
     <div class="mb-8"><label for="student-name" class="block text-slate-300 font-medium mb-3">Student Name</label> <input id="student-name" type="text" placeholder="Enter your full name" class="w-full px-4 py-3 rounded-xl bg-slate-700/50 border-2 border-slate-600 hover:border-orange-400/50 focus:border-orange-400 focus:outline-none transition-colors text-slate-100 placeholder-slate-500">
     </div>
     <div class="grid grid-cols-2 md:grid-cols-3 gap-3 mb-8">
      <div class="section-badge rounded-lg p-3">
       <div class="font-orbitron text-orange-400 text-sm font-semibold">
        SMAW
       </div>
       <div class="text-xs text-slate-400">
        4 Questions
       </div>
      </div>
      <div class="section-badge rounded-lg p-3">
       <div class="font-orbitron text-orange-400 text-sm font-semibold">
        FCAW
       </div>
       <div class="text-xs text-slate-400">
        4 Questions
       </div>
      </div>
      <div class="section-badge rounded-lg p-3">
       <div class="font-orbitron text-orange-400 text-sm font-semibold">
        GMAW
       </div>
       <div class="text-xs text-slate-400">
        4 Questions
       </div>
      </div>
      <div class="section-badge rounded-lg p-3">
       <div class="font-orbitron text-orange-400 text-sm font-semibold">
        GTAW
       </div>
       <div class="text-xs text-slate-400">
        4 Questions
       </div>
      </div>
      <div class="section-badge rounded-lg p-3 col-span-2 md:col-span-1">
       <div class="font-orbitron text-orange-400 text-sm font-semibold">
        SAW &amp; PAW
       </div>
       <div class="text-xs text-slate-400">
        4 Questions
       </div>
      </div>
     </div>
     <div class="flex flex-col sm:flex-row gap-4 justify-center">
      <button id="start-btn" class="bg-gradient-to-r from-orange-500 to-amber-500 hover:from-orange-600 hover:to-amber-600 text-slate-900 font-bold py-4 px-8 rounded-xl text-lg transition-all duration-300 animate-pulse-glow"> 🔥 Start Quiz </button> <button id="history-btn" class="border-2 border-orange-500/50 hover:border-orange-400 hover:bg-orange-500/10 text-orange-400 font-bold py-4 px-8 rounded-xl text-lg transition-all duration-300"> 📊 View History </button>
     </div>
    </div>
   </div><!-- Quiz Screen -->
   <div id="quiz-screen" class="hidden min-h-full flex flex-col p-4 md:p-6">
    <!-- Header -->
    <div class="card-glass rounded-2xl p-4 mb-4">
     <div class="flex flex-wrap items-center justify-between gap-4">
      <div class="flex items-center gap-4">
       <span id="section-label" class="section-badge px-4 py-2 rounded-lg font-orbitron text-sm text-orange-400"> Section 1: SMAW </span> <span id="question-counter" class="text-slate-400 font-medium"> Question 1/20 </span>
      </div>
      <div class="flex items-center gap-4">
       <div class="flex items-center gap-2">
        <svg class="w-5 h-5 text-orange-400" fill="none" stroke="currentColor" viewbox="0 0 24 24">
         <circle cx="12" cy="12" r="10" stroke-width="2" /> <path d="M12 6v6l4 2" stroke-width="2" stroke-linecap="round" />
        </svg><span id="timer" class="font-orbitron text-orange-400">00:00</span>
       </div>
       <div class="flex items-center gap-2">
        <span class="text-slate-400">Score:</span> <span id="score-display" class="font-orbitron text-green-400">0</span>
       </div>
      </div>
     </div><!-- Progress Bar -->
     <div class="mt-4 h-2 bg-slate-700 rounded-full overflow-hidden">
      <div id="progress-bar" class="progress-bar h-full rounded-full transition-all duration-500" style="width: 5%"></div>
     </div>
    </div><!-- Question Card -->
    <div class="flex-1 flex flex-col">
     <div class="card-glass rounded-2xl p-6 md:p-8 flex-1 flex flex-col">
      <h2 id="question-text" class="text-xl md:text-2xl font-semibold mb-6 leading-relaxed">Question text goes here...</h2>
      <div id="options-container" class="space-y-3 flex-1">
       <!-- Options will be inserted here -->
      </div><!-- Feedback Area -->
      <div id="feedback-area" class="hidden mt-6 p-4 rounded-xl">
       <p id="feedback-text" class="font-medium"></p>
      </div><!-- Navigation -->
      <div class="mt-6 flex justify-between items-center">
       <button id="quit-btn" class="text-slate-400 hover:text-red-400 transition-colors"> ✕ Quit Quiz </button> <button id="next-btn" class="hidden bg-gradient-to-r from-orange-500 to-amber-500 hover:from-orange-600 hover:to-amber-600 text-slate-900 font-bold py-3 px-6 rounded-xl transition-all duration-300"> Next Question → </button>
      </div>
     </div>
    </div>
   </div><!-- Results Screen -->
   <div id="results-screen" class="hidden min-h-full flex flex-col items-center justify-center p-6">
    <div class="card-glass rounded-3xl p-8 md:p-12 max-w-2xl w-full text-center animate-slide-up">
     <div id="results-icon" class="text-6xl mb-4">
      🏆
     </div>
     <h2 class="font-orbitron text-3xl font-bold mb-2 text-orange-400">Quiz Complete!</h2>
     <p id="results-message" class="text-slate-300 mb-2">Great job on completing the welding processes quiz!</p>
     <p id="student-name-display" class="text-slate-400 text-sm mb-8">Student: <span class="text-orange-400 font-semibold">-</span></p><!-- Score Circle -->
     <div class="relative w-40 h-40 mx-auto mb-8">
      <svg class="w-full h-full transform -rotate-90">
       <circle cx="80" cy="80" r="70" fill="none" stroke="#334155" stroke-width="12" /> <circle id="score-circle" cx="80" cy="80" r="70" fill="none" stroke="url(#score-gradient)" stroke-width="12" stroke-linecap="round" stroke-dasharray="439.8" stroke-dashoffset="439.8" class="transition-all duration-1000" /> <defs>
        <lineargradient id="score-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
         <stop offset="0%" stop-color="#fb923c" />
         <stop offset="100%" stop-color="#fbbf24" />
        </lineargradient>
       </defs>
      </svg>
      <div class="absolute inset-0 flex flex-col items-center justify-center">
       <span id="final-score" class="font-orbitron text-4xl font-bold text-orange-400">0</span> <span class="text-slate-400 text-sm">/ 20</span>
      </div>
     </div><!-- Stats -->
     <div class="grid grid-cols-3 gap-4 mb-8">
      <div class="stats-card rounded-xl p-4">
       <div id="percentage-display" class="font-orbitron text-2xl font-bold text-green-400">
        0%
       </div>
       <div class="text-slate-400 text-sm">
        Accuracy
       </div>
      </div>
      <div class="stats-card rounded-xl p-4">
       <div id="time-display" class="font-orbitron text-2xl font-bold text-blue-400">
        0:00
       </div>
       <div class="text-slate-400 text-sm">
        Time
       </div>
      </div>
      <div class="stats-card rounded-xl p-4">
       <div id="grade-display" class="font-orbitron text-2xl font-bold text-orange-400">
        -
       </div>
       <div class="text-slate-400 text-sm">
        Grade
       </div>
      </div>
     </div>
     <div class="flex flex-col sm:flex-row gap-4 justify-center">
      <button id="submit-btn" class="bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white font-bold py-4 px-8 rounded-xl text-lg transition-all duration-300" target="_blank"> 📤 Submit to Teacher </button> <button id="retry-btn" class="bg-gradient-to-r from-orange-500 to-amber-500 hover:from-orange-600 hover:to-amber-600 text-slate-900 font-bold py-4 px-8 rounded-xl text-lg transition-all duration-300"> 🔄 Try Again </button> <button id="home-btn" class="border-2 border-orange-500/50 hover:border-orange-400 hover:bg-orange-500/10 text-orange-400 font-bold py-4 px-8 rounded-xl text-lg transition-all duration-300"> 🏠 Home </button>
     </div>
    </div>
   </div><!-- History Screen -->
   <div id="history-screen" class="hidden min-h-full flex flex-col p-6">
    <div class="card-glass rounded-2xl p-6 mb-4">
     <div class="flex items-center justify-between">
      <h2 class="font-orbitron text-2xl font-bold text-orange-400">📊 Quiz History</h2><button id="back-btn" class="text-slate-400 hover:text-orange-400 transition-colors"> ← Back to Home </button>
     </div>
    </div>
    <div id="history-list" class="flex-1 space-y-3 overflow-auto">
     <!-- History items will be inserted here -->
    </div>
    <div id="no-history" class="hidden flex-1 flex items-center justify-center">
     <div class="text-center">
      <div class="text-5xl mb-4">
       📝
      </div>
      <p class="text-slate-400">No quiz attempts yet. Start your first quiz!</p>
     </div>
    </div>
   </div>
  </div>
  <script>
        // Quiz Questions Data
        const questions = [
            // Section 1: SMAW
            {
                section: "Section 1: SMAW",
                question: "Which welding process is also commonly referred to by the name \"Stick\" welding?",
                options: ["GMAW", "SMAW", "GTAW", "FCAW"],
                correct: 1
            },
            {
                section: "Section 1: SMAW",
                question: "In SMAW, what is the primary purpose of the burning flux during the welding process?",
                options: ["To increase the speed of the weld", "To produce shielding gas and slag", "To act as the primary power source", "To eliminate the need for an electrode"],
                correct: 1
            },
            {
                section: "Section 1: SMAW",
                question: "Which welding method is specifically highlighted as being ideal for outdoor repairs and farm machinery?",
                options: ["GTAW", "PAW", "SMAW", "SAW"],
                correct: 2
            },
            {
                section: "Section 1: SMAW",
                question: "Why is SMAW equipment considered suitable for fieldwork?",
                options: ["It requires no external power.", "It uses a non-consumable electrode.", "It is portable and low-cost.", "It is the fastest welding process."],
                correct: 2
            },
            // Section 2: FCAW
            {
                section: "Section 2: FCAW",
                question: "What is the key difference between the electrode used in SMAW and the one used in FCAW?",
                options: ["SMAW uses a tubular wire, while FCAW uses a solid stick.", "SMAW uses a solid rod, while FCAW uses a manual filler rod.", "SMAW uses a flux-coated electrode, while FCAW uses a flux-filled tubular wire.", "There is no difference in the electrode types."],
                correct: 2
            },
            {
                section: "Section 2: FCAW",
                question: "According to the presentation, which process is most similar to a \"mechanical pencil\" due to its consistency and speed?",
                options: ["GMAW", "FCAW", "GTAW", "PAW"],
                correct: 1
            },
            {
                section: "Section 2: FCAW",
                question: "Which type of FCAW generates shielding gases directly from the flux without needing external gas?",
                options: ["Gas-shielded FCAW", "Self-shielded FCAW", "Dual-shielded FCAW", "Manual FCAW"],
                correct: 1
            },
            {
                section: "Section 2: FCAW",
                question: "FCAW is frequently used in which of the following heavy industries?",
                options: ["Medical device manufacturing", "Shipbuilding and structural steel", "Automotive body repair", "Kitchen equipment manufacturing"],
                correct: 1
            },
            // Section 3: GMAW
            {
                section: "Section 3: GMAW (MIG)",
                question: "What is the common name for Gas Metal Arc Welding (GMAW)?",
                options: ["Stick", "TIG", "MIG", "Plasma"],
                correct: 2
            },
            {
                section: "Section 3: GMAW (MIG)",
                question: "Which welding process is preferred for thin metals and automotive repairs because it produces minimal slag?",
                options: ["SMAW", "GMAW (MIG)", "SAW", "FCAW"],
                correct: 1
            },
            {
                section: "Section 3: GMAW (MIG)",
                question: "Which of these gases is mentioned as a common shielding gas for MIG welding?",
                options: ["Carbon dioxide", "Oxygen", "Hydrogen", "Nitrogen"],
                correct: 0
            },
            {
                section: "Section 3: GMAW (MIG)",
                question: "GMAW uses which type of electrode?",
                options: ["Non-consumable tungsten", "Flux-coated stick", "Continuous solid wire", "Granular flux rod"],
                correct: 2
            },
            // Section 4: GTAW
            {
                section: "Section 4: GTAW (TIG)",
                question: "What is unique about the tungsten electrode used in TIG (GTAW) welding?",
                options: ["It melts into the weld pool.", "It is non-consumable.", "It is coated in flux.", "It is fed through a continuous wire spool."],
                correct: 1
            },
            {
                section: "Section 4: GTAW (TIG)",
                question: "How is the filler metal added during TIG (GTAW) welding?",
                options: ["It is automatically fed through the torch.", "It comes from the flux coating on the electrode.", "It is manually fed with the welder's second hand.", "No filler metal is ever used in TIG welding."],
                correct: 2
            },
            {
                section: "Section 4: GTAW (TIG)",
                question: "Which welding process is described as producing clean welds with \"no sparks, smoke, or significant spatter\"?",
                options: ["FCAW", "GTAW (TIG)", "SMAW", "GMAW"],
                correct: 1
            },
            {
                section: "Section 4: GTAW (TIG)",
                question: "Which industry uses TIG welding for its accuracy and high-quality finish?",
                options: ["Shipbuilding", "Heavy construction", "Aerospace", "Farm machinery repair"],
                correct: 2
            },
            // Section 5: SAW & PAW
            {
                section: "Section 5: SAW & PAW",
                question: "In Submerged Arc Welding (SAW), what does the term \"submerged\" refer to?",
                options: ["The welding is performed underwater.", "The arc is buried under a layer of granular flux.", "The metal is dipped in a molten bath.", "The electrode is hidden inside the torch."],
                correct: 1
            },
            {
                section: "Section 5: SAW & PAW",
                question: "What is a major safety benefit of using SAW?",
                options: ["It uses lower voltage.", "It eliminates arc exposure and UV radiation.", "It does not require a power source.", "It can be used without gloves."],
                correct: 1
            },
            {
                section: "Section 5: SAW & PAW",
                question: "Which process uses a \"constricted\" arc for high energy concentration?",
                options: ["SMAW", "GMAW", "PAW (Plasma Arc Welding)", "FCAW"],
                correct: 2
            },
            {
                section: "Section 5: SAW & PAW",
                question: "Which welding process is rated as having the fastest speed for large structures?",
                options: ["GTAW", "SMAW", "SAW", "PAW"],
                correct: 2
            }
        ];

        // App State
        let currentQuestion = 0;
        let score = 0;
        let timerInterval = null;
        let startTime = null;
        let selectedAnswer = null;
        let quizHistory = [];
        let studentName = '';

        const defaultConfig = {
            site_title: "ISTEPS-TLE WELDING Lesson 2 Quiz",
            welcome_message: "Master the fundamentals of welding processes through this comprehensive quiz",
            background_color: "#0f172a",
            surface_color: "#1e293b",
            text_color: "#f1f5f9",
            primary_action_color: "#fb923c",
            secondary_action_color: "#64748b"
        };

        // DOM Elements
        const welcomeScreen = document.getElementById('welcome-screen');
        const quizScreen = document.getElementById('quiz-screen');
        const resultsScreen = document.getElementById('results-screen');
        const historyScreen = document.getElementById('history-screen');
        
        // Initialize Element SDK
        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange: async (config) => {
                    const siteTitle = config.site_title || defaultConfig.site_title;
                    const welcomeMsg = config.welcome_message || defaultConfig.welcome_message;
                    const bgColor = config.background_color || defaultConfig.background_color;
                    const surfaceColor = config.surface_color || defaultConfig.surface_color;
                    const textColor = config.text_color || defaultConfig.text_color;
                    const primaryColor = config.primary_action_color || defaultConfig.primary_action_color;
                    const secondaryColor = config.secondary_action_color || defaultConfig.secondary_action_color;
                    
                    document.getElementById('site-title').textContent = siteTitle;
                    document.getElementById('welcome-msg').textContent = welcomeMsg;
                    
                    document.body.style.setProperty('--bg-color', bgColor);
                    document.body.style.setProperty('--surface-color', surfaceColor);
                    document.body.style.setProperty('--text-color', textColor);
                    document.body.style.setProperty('--primary-color', primaryColor);
                    document.body.style.setProperty('--secondary-color', secondaryColor);
                },
                mapToCapabilities: (config) => ({
                    recolorables: [
                        {
                            get: () => config.background_color || defaultConfig.background_color,
                            set: (v) => { config.background_color = v; window.elementSdk.setConfig({ background_color: v }); }
                        },
                        {
                            get: () => config.surface_color || defaultConfig.surface_color,
                            set: (v) => { config.surface_color = v; window.elementSdk.setConfig({ surface_color: v }); }
                        },
                        {
                            get: () => config.text_color || defaultConfig.text_color,
                            set: (v) => { config.text_color = v; window.elementSdk.setConfig({ text_color: v }); }
                        },
                        {
                            get: () => config.primary_action_color || defaultConfig.primary_action_color,
                            set: (v) => { config.primary_action_color = v; window.elementSdk.setConfig({ primary_action_color: v }); }
                        },
                        {
                            get: () => config.secondary_action_color || defaultConfig.secondary_action_color,
                            set: (v) => { config.secondary_action_color = v; window.elementSdk.setConfig({ secondary_action_color: v }); }
                        }
                    ],
                    borderables: [],
                    fontEditable: undefined,
                    fontSizeable: undefined
                }),
                mapToEditPanelValues: (config) => new Map([
                    ["site_title", config.site_title || defaultConfig.site_title],
                    ["welcome_message", config.welcome_message || defaultConfig.welcome_message]
                ])
            });
        }

        // Initialize Data SDK
        const dataHandler = {
            onDataChanged(data) {
                quizHistory = data.sort((a, b) => new Date(b.quiz_date) - new Date(a.quiz_date));
                renderHistory();
            }
        };

        async function initDataSdk() {
            if (window.dataSdk) {
                const result = await window.dataSdk.init(dataHandler);
                if (!result.isOk) {
                    console.error("Failed to initialize data SDK");
                }
            }
        }
        initDataSdk();

        // Screen Navigation
        function showScreen(screen) {
            welcomeScreen.classList.add('hidden');
            quizScreen.classList.add('hidden');
            resultsScreen.classList.add('hidden');
            historyScreen.classList.add('hidden');
            screen.classList.remove('hidden');
        }

        // Timer Functions
        let timeRemaining = 60; // 1 minute = 60 seconds
        
        function startTimer() {
            timeRemaining = 60;
            updateTimerDisplay();
            timerInterval = setInterval(() => {
                timeRemaining--;
                updateTimerDisplay();
                
                if (timeRemaining <= 0) {
                    clearInterval(timerInterval);
                    endQuizTimeUp();
                }
            }, 1000);
        }

        function updateTimerDisplay() {
            const minutes = Math.floor(timeRemaining / 60).toString().padStart(2, '0');
            const seconds = (timeRemaining % 60).toString().padStart(2, '0');
            const timerElement = document.getElementById('timer');
            timerElement.textContent = `${minutes}:${seconds}`;
            
            // Change color when time is running out
            if (timeRemaining <= 10) {
                timerElement.classList.remove('text-orange-400');
                timerElement.classList.add('text-red-400', 'animate-pulse');
            }
        }

        function addBonusTime() {
            timeRemaining += 3;
            updateTimerDisplay();
        }

        function stopTimer() {
            clearInterval(timerInterval);
            return 60 - timeRemaining;
        }

        // Quiz Functions
        function startQuiz() {
            studentName = document.getElementById('student-name').value.trim();
            
            if (!studentName) {
                alert('Please enter your name to start the quiz.');
                return;
            }
            
            currentQuestion = 0;
            score = 0;
            selectedAnswer = null;
            document.getElementById('score-display').textContent = '0';
            showScreen(quizScreen);
            startTimer();
            loadQuestion();
        }

        function loadQuestion() {
            const q = questions[currentQuestion];
            selectedAnswer = null;
            
            document.getElementById('section-label').textContent = q.section;
            document.getElementById('question-counter').textContent = `Question ${currentQuestion + 1}/20`;
            document.getElementById('question-text').textContent = q.question;
            document.getElementById('progress-bar').style.width = `${((currentQuestion + 1) / 20) * 100}%`;
            
            const optionsContainer = document.getElementById('options-container');
            optionsContainer.innerHTML = '';
            
            const letters = ['A', 'B', 'C', 'D'];
            q.options.forEach((option, index) => {
                const btn = document.createElement('button');
                btn.className = 'option-btn w-full text-left p-4 rounded-xl border-2 border-slate-600 hover:border-orange-400 transition-all duration-300 flex items-center gap-4';
                btn.innerHTML = `
                    <span class="flex-shrink-0 w-10 h-10 rounded-lg bg-slate-700 flex items-center justify-center font-orbitron font-bold text-orange-400">${letters[index]}</span>
                    <span class="flex-1">${option}</span>
                `;
                btn.onclick = () => selectAnswer(index, btn);
                optionsContainer.appendChild(btn);
            });
            
            document.getElementById('feedback-area').classList.add('hidden');
            document.getElementById('next-btn').classList.add('hidden');
        }

        function selectAnswer(index, btn) {
            if (selectedAnswer !== null) return;
            
            selectedAnswer = index;
            const q = questions[currentQuestion];
            const buttons = document.querySelectorAll('.option-btn');
            
            buttons.forEach(b => b.disabled = true);
            
            if (index === q.correct) {
                btn.classList.add('correct');
                score++;
                document.getElementById('score-display').textContent = score;
                addBonusTime(); // Add 3 seconds bonus time for correct answer
                showFeedback(true, "Correct! Well done! 🔥 +3 seconds bonus!");
                createSparks(btn);
            } else {
                btn.classList.add('incorrect');
                buttons[q.correct].classList.add('correct');
                showFeedback(false, `Incorrect. The correct answer was: ${q.options[q.correct]}`);
            }
            
            document.getElementById('next-btn').classList.remove('hidden');
            document.getElementById('next-btn').textContent = currentQuestion < 19 ? 'Next Question →' : 'See Results →';
        }

        function showFeedback(isCorrect, message) {
            const feedbackArea = document.getElementById('feedback-area');
            const feedbackText = document.getElementById('feedback-text');
            
            feedbackArea.classList.remove('hidden');
            feedbackArea.className = `mt-6 p-4 rounded-xl ${isCorrect ? 'bg-green-500/20 border border-green-500/30' : 'bg-red-500/20 border border-red-500/30'}`;
            feedbackText.textContent = message;
            feedbackText.className = `font-medium ${isCorrect ? 'text-green-400' : 'text-red-400'}`;
        }

        function createSparks(element) {
            const rect = element.getBoundingClientRect();
            for (let i = 0; i < 8; i++) {
                const spark = document.createElement('div');
                spark.className = 'spark';
                spark.style.left = `${rect.left + Math.random() * rect.width}px`;
                spark.style.top = `${rect.top + Math.random() * rect.height}px`;
                document.body.appendChild(spark);
                setTimeout(() => spark.remove(), 800);
            }
        }

        function nextQuestion() {
            currentQuestion++;
            if (currentQuestion < 20) {
                loadQuestion();
            } else {
                showResults();
            }
        }

        function endQuizTimeUp() {
            currentQuestion = 20; // Force to end
            showResults();
        }

        async function showResults() {
            const timeTaken = stopTimer();
            const percentage = Math.round((score / 20) * 100);
            
            showScreen(resultsScreen);
            
            // Set results icon and message based on score
            let icon, message, grade;
            if (percentage >= 90) {
                icon = '🏆'; message = 'Outstanding! You\'re a welding expert!'; grade = 'A+';
            } else if (percentage >= 80) {
                icon = '🌟'; message = 'Excellent work! You really know your stuff!'; grade = 'A';
            } else if (percentage >= 70) {
                icon = '👍'; message = 'Good job! Keep practicing to master it!'; grade = 'B';
            } else if (percentage >= 60) {
                icon = '📚'; message = 'Not bad! Review the material and try again.'; grade = 'C';
            } else {
                icon = '💪'; message = 'Keep studying! You\'ll get there!'; grade = 'D';
            }
            
            document.getElementById('results-icon').textContent = icon;
            document.getElementById('results-message').textContent = message;
            document.getElementById('final-score').textContent = score;
            document.getElementById('percentage-display').textContent = `${percentage}%`;
            document.getElementById('grade-display').textContent = grade;
            
            const minutes = Math.floor(timeTaken / 60);
            const seconds = timeTaken % 60;
            document.getElementById('time-display').textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
            
            // Animate score circle
            setTimeout(() => {
                const circumference = 439.8;
                const offset = circumference - (percentage / 100) * circumference;
                document.getElementById('score-circle').style.strokeDashoffset = offset;
            }, 100);
            
            // Save to history
            if (window.dataSdk && quizHistory.length < 999) {
                const result = await window.dataSdk.create({
                    student_name: studentName,
                    quiz_date: new Date().toISOString(),
                    score: score,
                    total_questions: 20,
                    percentage: percentage,
                    time_taken: timeTaken
                });
                if (!result.isOk) {
                    console.error("Failed to save quiz result");
                }
            }
            
            // Display student name
            document.getElementById('student-name-display').innerHTML = `Student: <span class="text-orange-400 font-semibold">${studentName}</span>`;
        }

        function renderHistory() {
            const historyList = document.getElementById('history-list');
            const noHistory = document.getElementById('no-history');
            
            if (quizHistory.length === 0) {
                historyList.classList.add('hidden');
                noHistory.classList.remove('hidden');
                return;
            }
            
            historyList.classList.remove('hidden');
            noHistory.classList.add('hidden');
            
            historyList.innerHTML = quizHistory.map((item, index) => {
                const date = new Date(item.quiz_date);
                const minutes = Math.floor(item.time_taken / 60);
                const seconds = item.time_taken % 60;
                
                let gradeColor = 'text-orange-400';
                let grade = 'D';
                if (item.percentage >= 90) { grade = 'A+'; gradeColor = 'text-green-400'; }
                else if (item.percentage >= 80) { grade = 'A'; gradeColor = 'text-green-400'; }
                else if (item.percentage >= 70) { grade = 'B'; gradeColor = 'text-blue-400'; }
                else if (item.percentage >= 60) { grade = 'C'; gradeColor = 'text-yellow-400'; }
                
                return `
                    <div class="card-glass rounded-xl p-4 flex flex-col gap-2 animate-slide-up" style="animation-delay: ${index * 0.05}s">
                        <div class="flex items-center justify-between gap-4">
                            <div class="w-12 h-12 rounded-xl bg-orange-500/20 flex items-center justify-center font-orbitron font-bold ${gradeColor}">${grade}</div>
                            <div class="flex-1">
                                <div class="font-semibold">${item.student_name}</div>
                                <div class="text-slate-400 text-sm">${date.toLocaleDateString()} at ${date.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'})}</div>
                            </div>
                            <div class="text-right">
                                <div class="font-orbitron text-2xl font-bold text-orange-400">${item.score}/20</div>
                                <div class="text-slate-400 text-sm">${item.percentage}%</div>
                            </div>
                        </div>
                        <div class="text-slate-400 text-xs">Time: ${minutes}:${seconds.toString().padStart(2, '0')}</div>
                    </div>
                `;
            }).join('');
        }

        // Event Listeners
        document.getElementById('start-btn').addEventListener('click', startQuiz);
        document.getElementById('history-btn').addEventListener('click', () => showScreen(historyScreen));
        document.getElementById('next-btn').addEventListener('click', nextQuestion);
        document.getElementById('submit-btn').addEventListener('click', () => {
            const message = `Quiz Results - ${studentName}\nScore: ${score}/20 (${Math.round((score / 20) * 100)}%)\nReference: https://www.youtube.com/shorts/koG0CjWkmzg`;
            window.open(`https://www.youtube.com/shorts/koG0CjWkmzg`, '_blank', 'noopener,noreferrer');
        });
        document.getElementById('retry-btn').addEventListener('click', startQuiz);
        document.getElementById('home-btn').addEventListener('click', () => showScreen(welcomeScreen));
        document.getElementById('back-btn').addEventListener('click', () => showScreen(welcomeScreen));
        document.getElementById('quit-btn').addEventListener('click', () => {
            stopTimer();
            showScreen(welcomeScreen);
        });
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9d66eb89b7038d0f',t:'MTc3MjUyMjg2MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
