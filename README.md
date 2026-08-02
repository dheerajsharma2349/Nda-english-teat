<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UPSC NDA English Elite Mock Test | 50 Questions</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
        }
        .academy-font {
            font-family: 'Cinzel', serif;
        }
        .custom-scroll::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        .custom-scroll::-webkit-scrollbar-track {
            background: #0f172a;
        }
        .custom-scroll::-webkit-scrollbar-thumb {
            background: #334155;
            border-radius: 4px;
        }
        .custom-scroll::-webkit-scrollbar-thumb:hover {
            background: #475569;
        }
        .glassmorphism {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
        }
    </style>
</head>
<body class="bg-[#0b0f19] text-slate-100 min-h-screen flex flex-col antialiased custom-scroll">

    <!-- Top Premium Navbar -->
    <header class="bg-[#0e1424] border-b border-slate-800 sticky top-0 z-40 shadow-xl">
        <div class="max-w-7xl mx-auto px-4 py-3 flex flex-col md:flex-row justify-between items-center gap-4">
            
            <!-- Logo & Title -->
            <div class="flex items-center space-x-3.5">
                <div class="relative">
                    <div class="absolute -inset-1 bg-gradient-to-r from-amber-500 to-red-600 rounded-lg blur opacity-75"></div>
                    <div class="relative bg-slate-900 text-white px-3 py-1.5 rounded-lg font-bold text-sm tracking-widest academy-font border border-slate-700">NDA</div>
                </div>
                <div>
                    <h1 class="font-extrabold text-base md:text-lg tracking-wide bg-gradient-to-r from-amber-200 via-slate-100 to-amber-200 bg-clip-text text-transparent">ELITE TEST SERIES</h1>
                    <p class="text-[10px] text-amber-500/80 tracking-widest font-semibold uppercase">UPSC Pattern • English paper 2</p>
                </div>
            </div>

            <!-- Dashboard / Timer Controls -->
            <div class="flex items-center gap-3 w-full md:w-auto justify-end">
                
                <!-- Progress Circular/Text Bar -->
                <div class="bg-slate-900/90 border border-slate-800 px-3 py-1.5 rounded-xl flex items-center space-x-2">
                    <div class="text-right">
                        <span class="block text-[9px] text-slate-400 font-bold uppercase tracking-wider">Answered</span>
                        <span id="header-progress" class="text-sm font-extrabold text-emerald-400">0 / 50</span>
                    </div>
                </div>

                <!-- Marked Count -->
                <div class="bg-slate-900/90 border border-slate-800 px-3 py-1.5 rounded-xl flex items-center space-x-2">
                    <div class="text-right">
                        <span class="block text-[9px] text-slate-400 font-bold uppercase tracking-wider">Review Marks</span>
                        <span id="header-marked" class="text-sm font-extrabold text-amber-500">0</span>
                    </div>
                </div>

                <!-- Timer Area -->
                <div class="bg-slate-950 border border-red-900/50 px-4 py-1 rounded-xl flex items-center gap-3">
                    <div class="text-center">
                        <span class="block text-[8px] text-red-400 font-extrabold uppercase tracking-widest">Time Remaining</span>
                        <span id="timer-text" class="text-base md:text-lg font-mono font-black text-red-500">60:00</span>
                    </div>
                    <!-- Pause Button -->
                    <button id="pause-btn" onclick="togglePause()" class="p-1.5 bg-slate-800 hover:bg-slate-700 rounded-lg text-slate-300 transition">
                        <svg id="pause-icon" class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M10 9v6m4-6v6m7-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Sub-Navbar: Section Filter Tabs -->
    <div class="bg-[#0b0f19]/80 backdrop-blur sticky top-[69px] z-30 border-b border-slate-800/60 shadow-lg py-2">
        <div class="max-w-7xl mx-auto px-4 flex gap-2 overflow-x-auto custom-scroll pb-1">
            <button onclick="filterSection('ALL')" id="tab-ALL" class="tab-btn px-4 py-1.5 rounded-lg text-xs font-bold transition-all shrink-0 bg-amber-500 text-slate-950">ALL (50)</button>
            <button onclick="filterSection('SYNONYMS')" id="tab-SYNONYMS" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">SYNONYMS (10)</button>
            <button onclick="filterSection('ANTONYMS')" id="tab-ANTONYMS" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">ANTONYMS (10)</button>
            <button onclick="filterSection('SPOTTING ERRORS')" id="tab-SPOTTING_ERRORS" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">ERRORS (10)</button>
            <button onclick="filterSection('SENTENCE IMPROVEMENT')" id="tab-SENTENCE_IMPROVEMENT" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">IMPROV. (5)</button>
            <button onclick="filterSection('CLOZE TEST')" id="tab-CLOZE_TEST" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">CLOZE TEST (5)</button>
            <button onclick="filterSection('READING COMPREHENSION')" id="tab-READING_COMPREHENSION" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">COMPREHENSION (5)</button>
            <button onclick="filterSection('IDIOMS & PHRASES')" id="tab-IDIOMS_PHRASES" class="tab-btn px-3.5 py-1.5 rounded-lg text-xs font-semibold text-slate-400 hover:text-white hover:bg-slate-800/50 transition shrink-0">IDIOMS (5)</button>
        </div>
    </div>

    <!-- Main Workspace Container -->
    <main class="flex-grow max-w-7xl w-full mx-auto px-4 py-6 flex flex-col lg:flex-row gap-6 relative">
        
        <!-- Left Pane: Interactive Quiz Core -->
        <div class="flex-grow lg:w-3/4 flex flex-col gap-6">
            
            <!-- Instructions Panel -->
            <div id="instructions-box" class="bg-[#111827] border border-slate-800 rounded-2xl p-5 relative overflow-hidden">
                <div class="absolute right-0 top-0 h-32 w-32 bg-amber-500/5 rounded-full blur-3xl pointer-events-none"></div>
                <div class="flex items-start gap-4">
                    <div class="p-3 bg-amber-500/10 rounded-xl text-amber-500 shrink-0">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                    </div>
                    <div>
                        <h2 class="text-base font-bold text-slate-100 academy-font tracking-wide mb-1">GENERAL INSTRUCTIONS</h2>
                        <p class="text-xs text-slate-400 leading-relaxed mb-3">
                            This simulator mimics the exact toughness parameters of the UPSC NDA exam. Questions feature complex syntax patterns, rare lexical constructs, and rigorous conceptual grammar. 
                        </p>
                        <div class="flex flex-wrap gap-4 text-[11px] text-slate-300 font-medium">
                            <span class="flex items-center gap-1.5"><strong class="text-emerald-400">+4.00</strong> Correct Ans</span>
                            <span class="flex items-center gap-1.5"><strong class="text-red-400">-1.33</strong> Negative Marks</span>
                            <span class="flex items-center gap-1.5"><strong class="text-amber-500">Mark</strong> feature for flagged doubts</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Dynamic Question Sheet Container -->
            <div id="questions-viewport" class="space-y-6">
                <!-- Javascript will load actual items here -->
            </div>

            <!-- Action Controls Bar -->
            <div class="bg-[#0f172a] border border-slate-800 p-4 rounded-xl flex justify-between items-center gap-4">
                <button onclick="resetAnswers()" id="btn-reset" class="px-4 py-2 border border-slate-700 hover:border-slate-500 text-slate-300 rounded-lg text-xs font-bold transition">
                    Clear Sheet
                </button>
                <button onclick="triggerSubmitConfirmation()" id="btn-submit" class="px-6 py-2.5 bg-gradient-to-r from-red-600 to-amber-600 hover:from-red-500 hover:to-amber-500 text-white font-extrabold text-xs tracking-wider rounded-lg shadow-lg shadow-red-950/50 transition">
                    SUBMIT ANSWER SHEET
                </button>
            </div>
        </div>

        <!-- Right Pane: Live Map Sidebar -->
        <div class="lg:w-1/4 flex flex-col gap-6">
            
            <div class="bg-[#0f172a] border border-slate-800 p-5 rounded-2xl sticky top-40 space-y-5">
                <div class="flex items-center justify-between">
                    <h3 class="font-extrabold text-xs uppercase tracking-wider text-slate-300">Answer Grid</h3>
                    <span id="filter-label" class="text-[10px] bg-slate-800 px-2.5 py-0.5 rounded text-amber-500 font-bold">ALL</span>
                </div>

                <!-- Navigation grid map -->
                <div id="navigation-matrix" class="grid grid-cols-5 gap-2 max-h-56 overflow-y-auto custom-scroll pr-1">
                    <!-- Nav markers built dynamically by JS -->
                </div>

                <!-- Color Codes -->
                <div class="grid grid-cols-2 gap-3 text-[10px] text-slate-400 border-t border-slate-800 pt-4">
                    <div class="flex items-center gap-2">
                        <span class="w-2.5 h-2.5 rounded bg-slate-800 border border-slate-700"></span>
                        <span>Unanswered</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <span class="w-2.5 h-2.5 rounded bg-indigo-600"></span>
                        <span>Answered</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <span class="w-2.5 h-2.5 rounded bg-amber-500"></span>
                        <span>Marked</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <span class="w-2.5 h-2.5 rounded bg-amber-500 ring-2 ring-indigo-500"></span>
                        <span>Ans & Marked</span>
                    </div>
                </div>

                <!-- Analytics Dashboard Container (Appears on submit) -->
                <div id="analytics-panel" class="hidden border-t border-slate-800 pt-5 space-y-4">
                    <h4 class="font-extrabold text-slate-100 text-xs tracking-wider uppercase text-center">📊 REPORT CARD</h4>
                    
                    <div class="bg-slate-950 rounded-xl p-4 text-center border border-slate-800">
                        <span class="block text-[10px] text-slate-400 uppercase tracking-widest font-semibold">UPSC Score</span>
                        <span id="card-score" class="text-3xl font-black text-amber-400 tracking-tight">0.00 <span class="text-xs text-slate-400">/ 200</span></span>
                        <div class="mt-1 h-1.5 w-full bg-slate-800 rounded-full overflow-hidden">
                            <div id="score-bar" class="bg-gradient-to-r from-red-500 to-emerald-500 h-full w-0 transition-all duration-1000"></div>
                        </div>
                    </div>

                    <!-- Precise stats breakdown -->
                    <div class="grid grid-cols-3 gap-2 text-center text-[11px] font-bold">
                        <div class="bg-emerald-950/40 border border-emerald-900/30 p-2 rounded-lg text-emerald-400">
                            <span class="block text-[8px] text-slate-500 uppercase font-normal">Correct</span>
                            <span id="stat-c">0</span>
                        </div>
                        <div class="bg-red-950/40 border border-red-900/30 p-2 rounded-lg text-red-400">
                            <span class="block text-[8px] text-slate-500 uppercase font-normal">Incorrect</span>
                            <span id="stat-w">0</span>
                        </div>
                        <div class="bg-slate-900 border border-slate-800 p-2 rounded-lg text-slate-400">
                            <span class="block text-[8px] text-slate-500 uppercase font-normal">Left</span>
                            <span id="stat-s">50</span>
                        </div>
                    </div>

                    <!-- Performance Breakdown section-wise -->
                    <div class="space-y-2 border-t border-slate-800/50 pt-3">
                        <span class="block text-[9px] text-slate-400 font-bold uppercase tracking-widest text-center">Accuracy by Section</span>
                        <div id="section-breakdown-box" class="space-y-1.5 text-xs text-slate-300">
                            <!-- Dynamic list -->
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </main>

    <!-- Custom Modal: Cheating Guard / Pause State Overlay -->
    <div id="pause-overlay" class="fixed inset-0 bg-slate-950/98 z-[100] flex flex-col items-center justify-center p-4 hidden">
        <div class="text-center space-y-4">
            <div class="inline-flex p-4 bg-amber-500/10 rounded-full text-amber-500 animate-pulse border border-amber-500/20">
                <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"/></svg>
            </div>
            <h2 class="text-2xl font-black text-slate-100 tracking-wider academy-font">TEST DISCIPLINE ENFORCED</h2>
            <p class="text-sm text-slate-400 max-w-sm mx-auto leading-relaxed">
                Your test progress is saved securely. Timer is frozen. Click the button below to restore your exam sheet.
            </p>
            <button onclick="togglePause()" class="px-6 py-3 bg-gradient-to-r from-amber-500 to-red-600 hover:from-amber-400 hover:to-red-500 text-slate-950 font-black text-xs tracking-wider rounded-xl shadow-lg transition">
                RESUME SIMULATOR
            </button>
        </div>
    </div>

    <!-- Custom Confirmation Modal -->
    <div id="confirm-modal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-sm z-[110] flex items-center justify-center p-4 hidden">
        <div class="bg-[#0f172a] border border-slate-800 rounded-2xl max-w-md w-full p-6 shadow-2xl relative">
            <h3 class="text-base font-bold text-slate-100 academy-font mb-2 tracking-wide">CONFIRM SUBMISSION</h3>
            <p class="text-xs text-slate-400 leading-relaxed mb-6">
                Are you sure you want to finish the simulator? After submission, you will receive your analytical score and deep explanations of all questions immediately.
            </p>
            <div class="flex space-x-3 justify-end">
                <button onclick="closeConfirmation()" class="px-4 py-2 border border-slate-700 text-slate-300 rounded-lg text-xs font-semibold hover:bg-slate-800 transition">Cancel</button>
                <button onclick="finalSubmitTest()" class="px-5 py-2 bg-red-600 hover:bg-red-500 text-white rounded-lg text-xs font-extrabold transition">Submit Sheet</button>
            </div>
        </div>
    </div>

    <!-- Custom Notifications Toast -->
    <div id="toast-notif" class="fixed bottom-6 right-6 bg-slate-900 border border-indigo-500 text-slate-100 px-4 py-3 rounded-xl shadow-2xl flex items-center gap-3 transform translate-y-20 opacity-0 transition duration-300 z-50">
        <span id="toast-msg" class="text-xs font-bold">Action Recorded</span>
    </div>

    <!-- Script Block containing logical architecture and high-tier question bank -->
    <script>
        // Highly Advanced NDA-Grade English Question Database (50 items)
        const quizBank = [
            // SYNONYMS (1-10)
            {
                id: 1,
                section: "SYNONYMS",
                question: "The newly appointed General was known for his <strong class='underline decoration-amber-500 decoration-2'>fastidious</strong> attention to physical drills and tactical maneuvers.",
                options: {
                    a: "Meticulous",
                    b: "Sloppy",
                    c: "Indifferent",
                    d: "Erratic"
                },
                correct: "a",
                explanation: "<strong>Fastidious</strong> का अर्थ 'नखरेबाज' या 'अत्यंत सूक्ष्मता/बारीकी से काम करने वाला' (very attentive to accuracy and detail) होता है। अतः <strong>(a) Meticulous</strong> इसका सबसे निकटतम पर्यायवाची है।"
            },
            {
                id: 2,
                section: "SYNONYMS",
                question: "The defense operations were hampered by the <strong class='underline decoration-amber-500 decoration-2'>pernicious</strong> rumors spread by the enemy agents.",
                options: {
                    a: "Innocuous",
                    b: "Malevolent",
                    c: "Deleterious",
                    d: "Spurious"
                },
                correct: "c",
                explanation: "<strong>Pernicious</strong> का अर्थ 'हानिकारक या घातक' (having a harmful effect, especially in a gradual or subtle way) होता है। <strong>(c) Deleterious</strong> का अर्थ भी 'नुकसानदेह या हानिकारक' है।"
            },
            {
                id: 3,
                section: "SYNONYMS",
                question: "During the treaty discussions, the Ambassador’s <strong class='underline decoration-amber-500 decoration-2'>alacrity</strong> surprised everyone present in the hall.",
                options: {
                    a: "Apathy",
                    b: "Eagerness",
                    c: "Reluctance",
                    d: "Hesitation"
                },
                correct: "b",
                explanation: "<strong>Alacrity</strong> का अर्थ 'उत्साह, तत्परता या उत्सुकता' (brisk and cheerful readiness) होता है। अतः <strong>(b) Eagerness</strong> इसका सटीक पर्यायवाची है।"
            },
            {
                id: 4,
                section: "SYNONYMS",
                question: "The commander’s decision to attack the enemy post at night was indeed highly <strong class='underline decoration-amber-500 decoration-2'>sagacious</strong>.",
                options: {
                    a: "Foolish",
                    b: "Impulsive",
                    c: "Wise",
                    d: "Reckless"
                },
                correct: "c",
           
