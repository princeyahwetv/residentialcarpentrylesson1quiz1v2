<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Residential Carpentry - OHS Principles</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
    body {
      box-sizing: border-box;
    }
    
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800&display=swap');
    
    * {
      font-family: 'Poppins', sans-serif;
    }
    
    .quiz-option {
      transition: all 0.2s ease;
      cursor: pointer;
    }
    
    .quiz-option:hover {
      transform: translateX(4px);
    }
    
    .quiz-option.selected {
      border-width: 2px;
    }
    
    .quiz-option.correct {
      animation: correctPulse 0.5s ease;
    }
    
    .quiz-option.incorrect {
      animation: shake 0.5s ease;
    }
    
    @keyframes correctPulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.02); }
    }
    
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-10px); }
      75% { transform: translateX(10px); }
    }
    
    .fade-in {
      animation: fadeIn 0.3s ease;
    }
    
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .input-field {
      transition: all 0.2s ease;
    }

    .input-field:focus {
      outline: none;
      transform: translateY(-2px);
    }

    .timer-warning {
      animation: pulse 1s ease-in-out infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.7; }
    }

    .timer-critical {
      animation: flashRed 0.5s ease-in-out infinite;
    }

    @keyframes flashRed {
      0%, 100% { background-color: #ef4444; }
      50% { background-color: #dc2626; }
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full">
  <div id="app-wrapper" class="h-full w-full overflow-auto"><!-- Main Content -->
   <div id="main-content" class="min-h-full w-full"><!-- Header -->
    <header class="w-full py-8 px-6 shadow-sm">
     <div class="max-w-6xl mx-auto">
      <h1 id="site-title" class="text-4xl font-bold mb-2">ISTEPS-ICT SELF TUTORING EDUCATIONAL PLATFORM</h1>
      <p class="text-lg mb-1">Research Study by JOEL P. RODRIGUEZ, LPT, MAVEd</p>
      <p id="lesson-title" class="text-xl font-semibold">Residential Carpentry - Quarter 3</p>
     </div>
    </header><!-- Content Section -->
    <main class="w-full py-8 px-6">
     <div class="max-w-6xl mx-auto"><!-- Introduction -->
      <section class="mb-8 p-6 rounded-lg shadow-md">
       <h2 class="text-2xl font-bold mb-4">What is OHS (Occupational Health and Safety)?</h2>
       <p class="text-lg mb-4 leading-relaxed">Occupational Health and Safety (OHS) refers to the policies, procedures, and practices that ensure the safety, health, and welfare of all people engaged in work or employment. In carpentry, OHS principles are essential to prevent accidents, injuries, and health hazards in the workplace.</p>
      </section><!-- Key OHS Principles -->
      <section class="mb-8 p-6 rounded-lg shadow-md">
       <h2 class="text-2xl font-bold mb-4">Key OHS Principles in Carpentry</h2>
       <ul class="list-disc list-inside space-y-2 text-lg">
        <li>Use of Personal Protective Equipment (PPE)</li>
        <li>Proper Tool Handling and Maintenance</li>
        <li>Safe Work Practices and Procedures</li>
        <li>Hazard Identification and Risk Assessment</li>
        <li>Emergency Preparedness and Response</li>
        <li>Workplace Cleanliness and Organization (5S)</li>
       </ul>
      </section><!-- PPE Section -->
      <section class="mb-8 p-6 rounded-lg shadow-md">
       <h2 class="text-2xl font-bold mb-4">Personal Protective Equipment (PPE)</h2>
       <p class="text-lg leading-relaxed mb-4">PPE is specialized clothing or equipment worn by workers for protection against health and safety hazards. Proper use of PPE is mandatory in carpentry work.</p>
       <div class="space-y-4">
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">Essential PPE for Carpentry:</h3>
         <ul class="list-disc list-inside space-y-1 text-lg ml-4">
          <li>Safety Helmet/Hard Hat - Protects head from falling objects</li>
          <li>Safety Goggles - Protects eyes from wood chips and dust</li>
          <li>Ear Protection - Reduces noise from power tools</li>
          <li>Dust Mask/Respirator - Prevents inhalation of sawdust</li>
          <li>Work Gloves - Protects hands from cuts and splinters</li>
          <li>Steel-Toed Boots - Protects feet from heavy objects</li>
          <li>High-Visibility Vest - Ensures visibility on work sites</li>
         </ul>
        </div>
       </div>
      </section><!-- Safety Practices -->
      <section class="mb-8 p-6 rounded-lg shadow-md">
       <h2 class="text-2xl font-bold mb-4">Safe Work Practices in Carpentry</h2>
       <div class="space-y-4">
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">1. Tool Safety</h3>
         <p class="text-lg">Always inspect tools before use. Keep cutting tools sharp and properly maintained. Store tools safely when not in use.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">2. Electrical Safety</h3>
         <p class="text-lg">Check power tools for damaged cords. Use Ground Fault Circuit Interrupters (GFCI). Keep electrical equipment away from water.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">3. Ladder and Scaffold Safety</h3>
         <p class="text-lg">Inspect ladders before use. Maintain three points of contact. Ensure scaffolding is properly erected and stable.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">4. Material Handling</h3>
         <p class="text-lg">Use proper lifting techniques. Get assistance for heavy materials. Store materials securely to prevent falling.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">5. Housekeeping</h3>
         <p class="text-lg">Keep work area clean and organized. Remove tripping hazards immediately. Properly dispose of waste materials and debris.</p>
        </div>
       </div>
      </section><!-- Hazards Section -->
      <section class="mb-8 p-6 rounded-lg shadow-md">
       <h2 class="text-2xl font-bold mb-4">Common Hazards in Carpentry</h2>
       <div class="space-y-4">
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">Physical Hazards</h3>
         <p class="text-lg">Cuts from sharp tools, struck by falling objects, caught in machinery, slips trips and falls.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">Chemical Hazards</h3>
         <p class="text-lg">Exposure to wood preservatives, adhesives, solvents, and paints. Always use in well-ventilated areas.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">Ergonomic Hazards</h3>
         <p class="text-lg">Repetitive motions, awkward postures, manual handling of heavy materials leading to musculoskeletal injuries.</p>
        </div>
        <div class="p-4 rounded-lg">
         <h3 class="text-xl font-semibold mb-2">Environmental Hazards</h3>
         <p class="text-lg">Excessive noise from power tools, wood dust exposure, extreme temperatures, poor lighting.</p>
        </div>
       </div>
      </section><!-- Quiz Button -->
      <div class="text-center mb-12"><button id="quiz-button" class="px-8 py-4 rounded-lg font-bold text-xl shadow-lg hover:shadow-xl transition-all duration-200 transform hover:scale-105"> 📝 Take the Quiz </button>
      </div>
     </div>
    </main><!-- Footer -->
    <footer class="w-full py-6 px-6 text-center">
     <p id="footer-text" class="text-base font-semibold mb-1">Research Study by JOEL P. RODRIGUEZ LPT MAVED. @2024 LESSON: Residential Carpentry TLE Quarter 3</p>
    </footer>
   </div><!-- Quiz Modal -->
   <div id="quiz-modal" class="fixed inset-0 flex items-center justify-center p-4 hidden" style="z-index: 1000;">
    <div class="absolute inset-0 opacity-90"></div>
    <div class="relative w-full max-w-3xl max-h-[90%] overflow-y-auto rounded-xl shadow-2xl p-8"><button id="close-quiz" class="absolute top-4 right-4 text-3xl font-bold hover:opacity-70 transition-opacity">×</button>
     <h2 id="quiz-title" class="text-3xl font-bold mb-6 text-center">OHS Principles in Carpentry Quiz</h2><!-- Student Information Form -->
     <div id="student-info-form" class="mb-8">
      <div class="space-y-4">
       <div><label for="student-name" class="block text-lg font-semibold mb-2">Name:</label> <input type="text" id="student-name" class="input-field w-full px-4 py-3 rounded-lg border-2" placeholder="Enter your full name" required>
       </div>
       <div><label for="student-grade" class="block text-lg font-semibold mb-2">Grade:</label> <input type="text" id="student-grade" class="input-field w-full px-4 py-3 rounded-lg border-2" placeholder="Enter your grade level" required>
       </div>
       <div><label for="student-section" class="block text-lg font-semibold mb-2">Section:</label> <input type="text" id="student-section" class="input-field w-full px-4 py-3 rounded-lg border-2" placeholder="Enter your section" required>
       </div>
       <div id="info-error" class="text-red-600 font-semibold hidden">
        Please fill in all fields before starting the quiz.
       </div><button id="start-quiz-button" class="w-full py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all"> Start Quiz → </button>
      </div>
     </div><!-- Student Info Display (shown during quiz) -->
     <div id="student-info-display" class="mb-6 p-4 rounded-lg hidden">
      <div class="flex justify-between items-center flex-wrap gap-2">
       <div>
        <span class="font-semibold">Name:</span> <span id="display-name"></span>
       </div>
       <div>
        <span class="font-semibold">Grade:</span> <span id="display-grade"></span>
       </div>
       <div>
        <span class="font-semibold">Section:</span> <span id="display-section"></span>
       </div>
      </div>
     </div><!-- Timer Display -->
     <div id="timer-display" class="mb-6 p-4 rounded-lg text-center font-bold text-2xl hidden">
      ⏱️ Time Remaining: <span id="timer-value">3:00</span>
     </div>
     <div id="quiz-container"></div>
     <div id="quiz-navigation" class="mt-8 flex justify-between items-center hidden"><button id="prev-button" class="px-6 py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all disabled:opacity-50 disabled:cursor-not-allowed"> ← Previous </button>
      <div id="question-counter" class="text-lg font-semibold"></div><button id="next-button" class="px-6 py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all"> Next → </button> <button id="submit-button" class="px-6 py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all hidden"> Submit Quiz </button>
     </div>
     <div id="quiz-results" class="mt-8 p-6 rounded-lg hidden">
      <div class="mb-4 p-4 rounded-lg">
       <div class="text-center mb-2">
        <p class="font-semibold">Student Information</p>
       </div>
       <div class="space-y-1 text-center">
        <p><span class="font-semibold">Name:</span> <span id="result-name"></span></p>
        <p><span class="font-semibold">Grade:</span> <span id="result-grade"></span></p>
        <p><span class="font-semibold">Section:</span> <span id="result-section"></span></p>
       </div>
      </div>
      <h3 class="text-2xl font-bold mb-4 text-center">Quiz Results</h3>
      <div class="text-center mb-6">
       <p class="text-5xl font-bold mb-2" id="score-display"></p>
       <p class="text-xl" id="score-message"></p>
      </div>
      <div class="space-y-3"><button id="send-results-button" class="w-full py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all"> 📧 Send Results to Teacher </button> <button id="retry-button" class="w-full py-3 rounded-lg font-semibold shadow-md hover:shadow-lg transition-all"> 🔄 Retry Quiz </button>
      </div>
     </div>
    </div>
   </div>
  </div>
  <script>
    const defaultConfig = {
      background_color: '#e0f2fe',
      surface_color: '#ffffff',
      text_color: '#0c4a6e',
      primary_action_color: '#0ea5e9',
      secondary_action_color: '#38bdf8',
      font_family: 'Poppins',
      font_size: 16,
      site_title: 'ISTEPS-ICT SELF TUTORING EDUCATIONAL PLATFORM',
      lesson_title: 'Residential Carpentry - Quarter 3',
      quiz_button_text: '📝 Take the Quiz',
      quiz_title: 'OHS Principles in Carpentry Quiz',
      footer_text: 'Research Study by JOEL P. RODRIGUEZ LPT MAVED. @2024 LESSON: Residential Carpentry TLE Quarter 3'
    };

    const quizQuestions = [
      {
        question: "What does OHS stand for in carpentry work?",
        options: [
          "Occupational Hazard System",
          "Occupational Health and Safety",
          "Office Health Standards",
          "Organized Handling System"
        ],
        correct: 1
      },
      {
        question: "Which PPE protects your head from falling objects?",
        options: [
          "Safety Goggles",
          "Dust Mask",
          "Safety Helmet/Hard Hat",
          "Ear Protection"
        ],
        correct: 2
      },
      {
        question: "What is the main purpose of safety goggles in carpentry?",
        options: [
          "To look professional",
          "To protect eyes from wood chips and dust",
          "To improve vision",
          "To protect from sun glare"
        ],
        correct: 1
      },
      {
        question: "Why should you wear steel-toed boots in a carpentry workshop?",
        options: [
          "They are more comfortable",
          "They are required by fashion",
          "To protect feet from heavy falling objects",
          "To prevent slipping only"
        ],
        correct: 2
      },
      {
        question: "What should you do before using any power tool?",
        options: [
          "Use it immediately",
          "Inspect it for damage and defects",
          "Oil all parts",
          "Share it with others first"
        ],
        correct: 1
      },
      {
        question: "What does GFCI stand for in electrical safety?",
        options: [
          "General Fault Circuit Interrupter",
          "Ground Fault Circuit Interrupter",
          "Ground Fixed Circuit Insulator",
          "General Fixed Circuit Insulator"
        ],
        correct: 1
      },
      {
        question: "When using a ladder, you should maintain:",
        options: [
          "One point of contact",
          "Two points of contact",
          "Three points of contact",
          "Four points of contact"
        ],
        correct: 2
      },
      {
        question: "What is the proper way to lift heavy materials?",
        options: [
          "Bend at the waist and use your back",
          "Use proper lifting techniques and get assistance if needed",
          "Lift as fast as possible",
          "Always lift alone to prove strength"
        ],
        correct: 1
      },
      {
        question: "Good housekeeping in a carpentry workshop means:",
        options: [
          "Cleaning only at the end of the week",
          "Leaving tools scattered for easy access",
          "Keeping work area clean, organized, and free of tripping hazards",
          "Storing materials anywhere"
        ],
        correct: 2
      },
      {
        question: "Which of the following is a physical hazard in carpentry?",
        options: [
          "Proper ventilation",
          "Cuts from sharp tools",
          "Good lighting",
          "Clean workspace"
        ],
        correct: 1
      },
      {
        question: "Chemical hazards in carpentry include exposure to:",
        options: [
          "Fresh air",
          "Water",
          "Wood preservatives, adhesives, and solvents",
          "Sunlight"
        ],
        correct: 2
      },
      {
        question: "Ergonomic hazards in carpentry are related to:",
        options: [
          "Chemical exposure",
          "Electrical shocks",
          "Repetitive motions and awkward postures",
          "Noise levels"
        ],
        correct: 2
      },
      {
        question: "What type of protection should you use when operating loud power tools?",
        options: [
          "Safety goggles",
          "Ear protection/earplugs",
          "Dust mask",
          "Gloves"
        ],
        correct: 1
      },
      {
        question: "Why is it important to keep cutting tools sharp?",
        options: [
          "They look better",
          "Sharp tools are safer and require less force, reducing accidents",
          "They are easier to store",
          "They cost less"
        ],
        correct: 1
      },
      {
        question: "What should you do if you find a damaged power cord on a tool?",
        options: [
          "Use it carefully",
          "Tape it and continue working",
          "Do not use it and report it immediately for repair",
          "Ignore it"
        ],
        correct: 2
      }
    ];

    let currentQuestion = 0;
    let userAnswers = new Array(quizQuestions.length).fill(null);
    let quizSubmitted = false;
    let studentInfo = {
      name: '',
      grade: '',
      section: ''
    };
    let timeRemaining = 180;
    let timerInterval = null;
    let timeUsed = 0;

    async function onConfigChange(config) {
      const baseFontSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const fontStack = `${customFont}, Arial, sans-serif`;

      const backgroundColor = config.background_color || defaultConfig.background_color;
      const surfaceColor = config.surface_color || defaultConfig.surface_color;
      const textColor = config.text_color || defaultConfig.text_color;
      const primaryColor = config.primary_action_color || defaultConfig.primary_action_color;
      const secondaryColor = config.secondary_action_color || defaultConfig.secondary_action_color;

      document.getElementById('app-wrapper').style.backgroundColor = backgroundColor;
      document.getElementById('app-wrapper').style.color = textColor;
      
      document.querySelector('header').style.backgroundColor = surfaceColor;
      document.querySelector('header').style.color = textColor;
      document.querySelector('footer').style.backgroundColor = surfaceColor;
      document.querySelector('footer').style.color = textColor;

      const sections = document.querySelectorAll('section');
      sections.forEach(section => {
        section.style.backgroundColor = surfaceColor;
        section.style.color = textColor;
      });

      const contentDivs = document.querySelectorAll('section > div > div');
      contentDivs.forEach(div => {
        div.style.backgroundColor = backgroundColor;
      });

      document.getElementById('quiz-button').style.backgroundColor = primaryColor;
      document.getElementById('quiz-button').style.color = surfaceColor;

      const modal = document.querySelector('#quiz-modal > div:last-child');
      if (modal) {
        modal.style.backgroundColor = surfaceColor;
        modal.style.color = textColor;
      }

      const modalBackdrop = document.querySelector('#quiz-modal > div:first-child');
      if (modalBackdrop) {
        modalBackdrop.style.backgroundColor = textColor;
      }

      document.getElementById('close-quiz').style.color = textColor;

      document.getElementById('prev-button').style.backgroundColor = secondaryColor;
      document.getElementById('prev-button').style.color = surfaceColor;
      document.getElementById('next-button').style.backgroundColor = primaryColor;
      document.getElementById('next-button').style.color = surfaceColor;
      document.getElementById('submit-button').style.backgroundColor = primaryColor;
      document.getElementById('submit-button').style.color = surfaceColor;
      document.getElementById('start-quiz-button').style.backgroundColor = primaryColor;
      document.getElementById('start-quiz-button').style.color = surfaceColor;
      document.getElementById('retry-button').style.backgroundColor = primaryColor;
      document.getElementById('retry-button').style.color = surfaceColor;
      document.getElementById('send-results-button').style.backgroundColor = '#10b981';
      document.getElementById('send-results-button').style.color = surfaceColor;

      document.getElementById('quiz-results').style.backgroundColor = backgroundColor;
      document.getElementById('student-info-display').style.backgroundColor = backgroundColor;

      const inputFields = document.querySelectorAll('.input-field');
      inputFields.forEach(input => {
        input.style.backgroundColor = surfaceColor;
        input.style.borderColor = secondaryColor;
        input.style.color = textColor;
      });

      const labels = document.querySelectorAll('#student-info-form label');
      labels.forEach(label => {
        label.style.color = textColor;
        label.style.fontFamily = fontStack;
        label.style.fontSize = `${baseFontSize * 1.125}px`;
      });

      document.getElementById('site-title').textContent = config.site_title || defaultConfig.site_title;
      document.getElementById('lesson-title').textContent = config.lesson_title || defaultConfig.lesson_title;
      document.getElementById('quiz-button').textContent = config.quiz_button_text || defaultConfig.quiz_button_text;
      document.getElementById('quiz-title').textContent = config.quiz_title || defaultConfig.quiz_title;
      document.getElementById('footer-text').textContent = config.footer_text || defaultConfig.footer_text;

      document.getElementById('site-title').style.fontFamily = fontStack;
      document.getElementById('site-title').style.fontSize = `${baseFontSize * 2}px`;

      document.getElementById('lesson-title').style.fontFamily = fontStack;
      document.getElementById('lesson-title').style.fontSize = `${baseFontSize * 1.25}px`;

      const headerSubtitle = document.querySelector('header p:not(#lesson-title)');
      if (headerSubtitle) {
        headerSubtitle.style.fontFamily = fontStack;
        headerSubtitle.style.fontSize = `${baseFontSize * 1.125}px`;
        headerSubtitle.style.color = textColor;
      }

      document.getElementById('footer-text').style.fontFamily = fontStack;
      document.getElementById('footer-text').style.fontSize = `${baseFontSize}px`;

      const allHeadings = document.querySelectorAll('h2, h3');
      allHeadings.forEach(heading => {
        heading.style.fontFamily = fontStack;
        if (heading.tagName === 'H2') {
          heading.style.fontSize = `${baseFontSize * 1.5}px`;
        } else if (heading.tagName === 'H3') {
          heading.style.fontSize = `${baseFontSize * 1.25}px`;
        }
      });

      const allParagraphs = document.querySelectorAll('p, li');
      allParagraphs.forEach(p => {
        p.style.fontFamily = fontStack;
        p.style.fontSize = `${baseFontSize}px`;
      });

      document.getElementById('quiz-button').style.fontFamily = fontStack;
      document.getElementById('quiz-button').style.fontSize = `${baseFontSize * 1.25}px`;

      document.getElementById('quiz-title').style.fontFamily = fontStack;
      document.getElementById('quiz-title').style.fontSize = `${baseFontSize * 1.875}px`;

      document.getElementById('start-quiz-button').style.fontFamily = fontStack;
      document.getElementById('start-quiz-button').style.fontSize = `${baseFontSize}px`;

      updateQuizColors();
    }

    function updateTimer() {
      const minutes = Math.floor(timeRemaining / 60);
      const seconds = timeRemaining % 60;
      const timerValue = document.getElementById('timer-value');
      const timerDisplay = document.getElementById('timer-display');
      
      if (!timerValue || !timerDisplay) return;
      
      const config = window.elementSdk ? window.elementSdk.config : defaultConfig;
      const surfaceColor = config.surface_color || defaultConfig.surface_color;
      
      timerValue.textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
      
      if (timeRemaining <= 30) {
        timerDisplay.style.backgroundColor = '#ef4444';
        timerDisplay.style.color = surfaceColor;
        timerDisplay.classList.add('timer-critical');
        timerDisplay.classList.remove('timer-warning');
      } else if (timeRemaining <= 60) {
        timerDisplay.style.backgroundColor = '#f59e0b';
        timerDisplay.style.color = surfaceColor;
        timerDisplay.classList.add('timer-warning');
        timerDisplay.classList.remove('timer-critical');
      } else {
        timerDisplay.style.backgroundColor = '#10b981';
        timerDisplay.style.color = surfaceColor;
        timerDisplay.classList.remove('timer-warning', 'timer-critical');
      }
    }

    function startTimer() {
      if (timerInterval) {
        clearInterval(timerInterval);
      }
      
      timerInterval = setInterval(() => {
        timeRemaining--;
        timeUsed++;
        updateTimer();
        
        if (timeRemaining <= 0) {
          clearInterval(timerInterval);
          autoSubmitQuiz();
        }
      }, 1000);
    }

    function stopTimer() {
      if (timerInterval) {
        clearInterval(timerInterval);
        timerInterval = null;
      }
    }

    function addBonusTime() {
      timeRemaining += 60;
      updateTimer();
    }

    function autoSubmitQuiz() {
      if (!quizSubmitted) {
        const timerDisplay = document.getElementById('timer-display');
        if (timerDisplay) {
          timerDisplay.innerHTML = '⏰ <strong>Time\'s Up!</strong> Quiz auto-submitted.';
        }
        
        setTimeout(() => {
          submitQuiz();
        }, 1500);
      }
    }

    function updateQuizColors() {
      const config = window.elementSdk ? window.elementSdk.config : defaultConfig;
      const backgroundColor = config.background_color || defaultConfig.background_color;
      const surfaceColor = config.surface_color || defaultConfig.surface_color;
      const textColor = config.text_color || defaultConfig.text_color;
      const primaryColor = config.primary_action_color || defaultConfig.primary_action_color;
      const secondaryColor = config.secondary_action_color || defaultConfig.secondary_action_color;

      const options = document.querySelectorAll('.quiz-option');
      options.forEach(option => {
        if (option.classList.contains('selected') && !quizSubmitted) {
          option.style.backgroundColor = primaryColor;
          option.style.borderColor = primaryColor;
          option.style.color = surfaceColor;
        } else if (option.classList.contains('correct')) {
          option.style.backgroundColor = '#10b981';
          option.style.borderColor = '#10b981';
          option.style.color = surfaceColor;
        } else if (option.classList.contains('incorrect')) {
          option.style.backgroundColor = '#ef4444';
          option.style.borderColor = '#ef4444';
          option.style.color = surfaceColor;
        } else {
          option.style.backgroundColor = surfaceColor;
          option.style.borderColor = secondaryColor;
          option.style.color = textColor;
        }
      });
    }

    function showQuestion(index) {
      const container = document.getElementById('quiz-container');
      if (!container) return;
      
      const question = quizQuestions[index];
      const config = window.elementSdk ? window.elementSdk.config : defaultConfig;
      const baseFontSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const fontStack = `${customFont}, Arial, sans-serif`;
      const backgroundColor = config.background_color || defaultConfig.background_color;
      const surfaceColor = config.surface_color || defaultConfig.surface_color;
      const textColor = config.text_color || defaultConfig.text_color;
      const primaryColor = config.primary_action_color || defaultConfig.primary_action_color;
      const secondaryColor = config.secondary_action_color || defaultConfig.secondary_action_color;

      container.innerHTML = `
        <div class="fade-in">
          <h3 class="text-xl font-semibold mb-6" style="font-family: ${fontStack}; font-size: ${baseFontSize * 1.25}px; color: ${textColor};">
            Question ${index + 1}: ${question.question}
          </h3>
          <div class="space-y-3">
            ${question.options.map((option, i) => {
              let optionClass = 'quiz-option border-2 p-4 rounded-lg';
              let optionStyle = `font-family: ${fontStack}; font-size: ${baseFontSize}px; background-color: ${surfaceColor}; border-color: ${secondaryColor}; color: ${textColor};`;
              
              if (quizSubmitted) {
                if (i === question.correct) {
                  optionClass += ' correct';
                  optionStyle = `font-family: ${fontStack}; font-size: ${baseFontSize}px; background-color: #10b981; border-color: #10b981; color: ${surfaceColor};`;
                } else if (userAnswers[index] === i) {
                  optionClass += ' incorrect';
                  optionStyle = `font-family: ${fontStack}; font-size: ${baseFontSize}px; background-color: #ef4444; border-color: #ef4444; color: ${surfaceColor};`;
                }
              } else if (userAnswers[index] === i) {
                optionClass += ' selected';
                optionStyle = `font-family: ${fontStack}; font-size: ${baseFontSize}px; background-color: ${primaryColor}; border-color: ${primaryColor}; color: ${surfaceColor};`;
              }
              
              return `<div class="${optionClass}" data-option="${i}" style="${optionStyle}">${String.fromCharCode(65 + i)}. ${option}</div>`;
            }).join('')}
          </div>
        </div>
      `;

      if (!quizSubmitted) {
        container.querySelectorAll('.quiz-option').forEach(opt => {
          opt.addEventListener('click', function() {
            const optionIndex = parseInt(this.dataset.option);
            const wasAnswered = userAnswers[currentQuestion] !== null;
            
            userAnswers[currentQuestion] = optionIndex;
            
            if (!wasAnswered && optionIndex === question.correct) {
              addBonusTime();
              
              const timerDisplay = document.getElementById('timer-display');
              if (timerDisplay) {
                const originalContent = timerDisplay.innerHTML;
                timerDisplay.innerHTML = '🎉 <strong>+1 Minute Bonus!</strong> Correct answer!';
                timerDisplay.style.backgroundColor = '#10b981';
                
                setTimeout(() => {
                  timerDisplay.innerHTML = originalContent;
                  updateTimer();
                }, 2000);
              }
            }
            
            showQuestion(currentQuestion);
          });
        });
      }

      updateNavigation();
    }

    function updateNavigation() {
      const prevButton = document.getElementById('prev-button');
      const nextButton = document.getElementById('next-button');
      const submitButton = document.getElementById('submit-button');
      const counter = document.getElementById('question-counter');
      
      if (!prevButton || !nextButton || !submitButton || !counter) return;
      
      const config = window.elementSdk ? window.elementSdk.config : defaultConfig;
      const baseFontSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const fontStack = `${customFont}, Arial, sans-serif`;
      const textColor = config.text_color || defaultConfig.text_color;

      counter.textContent = `${currentQuestion + 1} / ${quizQuestions.length}`;
      counter.style.fontFamily = fontStack;
      counter.style.fontSize = `${baseFontSize * 1.125}px`;
      counter.style.color = textColor;

      prevButton.disabled = currentQuestion === 0;

      if (currentQuestion === quizQuestions.length - 1) {
        nextButton.classList.add('hidden');
        if (!quizSubmitted) {
          submitButton.classList.remove('hidden');
        } else {
          submitButton.classList.add('hidden');
        }
      } else {
        nextButton.classList.remove('hidden');
        submitButton.classList.add('hidden');
      }

      prevButton.style.fontFamily = fontStack;
      prevButton.style.fontSize = `${baseFontSize}px`;
      nextButton.style.fontFamily = fontStack;
      nextButton.style.fontSize = `${baseFontSize}px`;
      submitButton.style.fontFamily = fontStack;
      submitButton.style.fontSize = `${baseFontSize}px`;
    }

    function startQuiz() {
      const name = document.getElementById('student-name').value.trim();
      const grade = document.getElementById('student-grade').value.trim();
      const section = document.getElementById('student-section').value.trim();
      const errorDiv = document.getElementById('info-error');

      if (!name || !grade || !section) {
        if (errorDiv) errorDiv.classList.remove('hidden');
        return;
      }

      if (errorDiv) errorDiv.classList.add('hidden');

      studentInfo = { name, grade, section };

      const displayName = document.getElementById('display-name');
      const displayGrade = document.getElementById('display-grade');
      const displaySection = document.getElementById('display-section');
      
      if (displayName) displayName.textContent = name;
      if (displayGrade) displayGrade.textContent = grade;
      if (displaySection) displaySection.textContent = section;

      const infoForm = document.getElementById('student-info-form');
      const infoDisplay = document.getElementById('student-info-display');
      const timerDisplay = document.getElementById('timer-display');
      const navigation = document.getElementById('quiz-navigation');
      
      if (infoForm) infoForm.classList.add('hidden');
      if (infoDisplay) infoDisplay.classList.remove('hidden');
      if (timerDisplay) timerDisplay.classList.remove('hidden');
      if (navigation) navigation.classList.remove('hidden');

      timeRemaining = 180;
      timeUsed = 0;
      updateTimer();
      startTimer();

      showQuestion(currentQuestion);
    }

    function submitQuiz() {
      stopTimer();
      quizSubmitted = true;
      let score = 0;

      quizQuestions.forEach((question, index) => {
        if (userAnswers[index] === question.correct) {
          score++;
        }
      });

      const percentage = Math.round((score / quizQuestions.length) * 100);
      const config = window.elementSdk ? window.elementSdk.config : defaultConfig;
      const baseFontSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const fontStack = `${customFont}, Arial, sans-serif`;
      const textColor = config.text_color || defaultConfig.text_color;

      const resultName = document.getElementById('result-name');
      const resultGrade = document.getElementById('result-grade');
      const resultSection = document.getElementById('result-section');
      
      if (resultName) resultName.textContent = studentInfo.name;
      if (resultGrade) resultGrade.textContent = studentInfo.grade;
      if (resultSection) resultSection.textContent = studentInfo.section;

      const scoreDisplay = document.getElementById('score-display');
      const scoreMessage = document.getElementById('score-message');
      
      const timeMinutes = Math.floor(timeUsed / 60);
      const timeSeconds = timeUsed % 60;
      const timeString = `${timeMinutes}:${timeSeconds.toString().padStart(2, '0')}`;
      
      if (scoreDisplay) {
        scoreDisplay.textContent = `${score}/${quizQuestions.length} (${percentage}%)`;
        scoreDisplay.style.fontFamily = fontStack;
        scoreDisplay.style.fontSize = `${baseFontSize * 3}px`;
        scoreDisplay.style.color = textColor;
      }

      let message = '';
      if (percentage >= 90) {
        message = `Excellent! You have mastered this topic! 🎉 Time: ${timeString}`;
      } else if (percentage >= 75) {
        message = `Great job! You have a good understanding! 👏 Time: ${timeString}`;
      } else if (percentage >= 60) {
        message = `Good effort! Review the material for better results. 📚 Time: ${timeString}`;
      } else {
        message = `Keep studying! You can do better! 💪 Time: ${timeString}`;
      }

      if (scoreMessage) {
        scoreMessage.textContent = message;
        scoreMessage.style.fontFamily = fontStack;
        scoreMessage.style.fontSize = `${baseFontSize * 1.25}px`;
        scoreMessage.style.color = textColor;
      }

      const results = document.getElementById('quiz-results');
      const navigation = document.getElementById('quiz-navigation');
      const infoDisplay = document.getElementById('student-info-display');
      const timerDisplay = document.getElementById('timer-display');
      
      if (results) results.classList.remove('hidden');
      if (navigation) navigation.classList.add('hidden');
      if (infoDisplay) infoDisplay.classList.add('hidden');
      if (timerDisplay) timerDisplay.classList.add('hidden');

      currentQuestion = 0;
      showQuestion(currentQuestion);
    }

    function resetQuiz() {
      stopTimer();
      currentQuestion = 0;
      userAnswers = new Array(quizQuestions.length).fill(null);
      quizSubmitted = false;
      timeRemaining = 180;
      timeUsed = 0;

      const nameInput = document.getElementById('student-name');
      const gradeInput = document.getElementById('student-grade');
      const sectionInput = document.getElementById('student-section');
      
      if (nameInput) nameInput.value = '';
      if (gradeInput) gradeInput.value = '';
      if (sectionInput) sectionInput.value = '';

      const results = document.getElementById('quiz-results');
      const infoDisplay = document.getElementById('student-info-display');
      const navigation = document.getElementById('quiz-navigation');
      const timerDisplay = document.getElementById('timer-display');
      const infoForm = document.getElementById('student-info-form');
      const errorDiv = document.getElementById('info-error');
      
      if (results) results.classList.add('hidden');
      if (infoDisplay) infoDisplay.classList.add('hidden');
      if (navigation) navigation.classList.add('hidden');
      if (timerDisplay) timerDisplay.classList.add('hidden');
      if (infoForm) infoForm.classList.remove('hidden');
      if (errorDiv) errorDiv.classList.add('hidden');
    }

    // Event Listeners
    document.getElementById('quiz-button').addEventListener('click', function() {
      const modal = document.getElementById('quiz-modal');
      if (modal) modal.classList.remove('hidden');
      resetQuiz();
    });

    document.getElementById('close-quiz').addEventListener('click', function() {
      const modal = document.getElementById('quiz-modal');
      if (modal) modal.classList.add('hidden');
      stopTimer();
    });

    document.getElementById('start-quiz-button').addEventListener('click', function() {
      startQuiz();
    });

    document.getElementById('prev-button').addEventListener('click', function() {
      if (currentQuestion > 0) {
        currentQuestion--;
        showQuestion(currentQuestion);
      }
    });

    document.getElementById('next-button').addEventListener('click', function() {
      if (currentQuestion < quizQuestions.length - 1) {
        currentQuestion++;
        showQuestion(currentQuestion);
      }
    });

    document.getElementById('submit-button').addEventListener('click', function() {
      submitQuiz();
    });

    document.getElementById('retry-button').addEventListener('click', function() {
      resetQuiz();
    });

    document.getElementById('send-results-button').addEventListener('click', function() {
      let score = 0;
      quizQuestions.forEach((question, index) => {
        if (userAnswers[index] === question.correct) {
          score++;
        }
      });
      
      const percentage = Math.round((score / quizQuestions.length) * 100);
      const timeMinutes = Math.floor(timeUsed / 60);
      const timeSeconds = timeUsed % 60;
      const timeString = `${timeMinutes}:${timeSeconds.toString().padStart(2, '0')}`;
      
      const subject = encodeURIComponent('OHS Principles Quiz Results - ' + studentInfo.name);
      const body = encodeURIComponent(
        'RESIDENTIAL CARPENTRY - LESSON 1: OHS PRINCIPLES\n' +
        'Quiz Results\n\n' +
        '===========================================\n' +
        'STUDENT INFORMATION\n' +
        '===========================================\n' +
        'Name: ' + studentInfo.name + '\n' +
        'Grade: ' + studentInfo.grade + '\n' +
        'Section: ' + studentInfo.section + '\n\n' +
        '===========================================\n' +
        'QUIZ PERFORMANCE\n' +
        '===========================================\n' +
        'Score: ' + score + '/' + quizQuestions.length + '\n' +
        'Percentage: ' + percentage + '%\n' +
        'Time Taken: ' + timeString + '\n\n' +
        '===========================================\n' +
        'DETAILED ANSWERS\n' +
        '===========================================\n' +
        quizQuestions.map((q, i) => {
          const studentAnswer = userAnswers[i] !== null ? q.options[userAnswers[i]] : 'No answer';
          const correctAnswer = q.options[q.correct];
          const isCorrect = userAnswers[i] === q.correct ? '✓ CORRECT' : '✗ INCORRECT';
          return `\nQuestion ${i + 1}: ${q.question}\n` +
                 `Student Answer: ${studentAnswer}\n` +
                 `Correct Answer: ${correctAnswer}\n` +
                 `Status: ${isCorrect}\n`;
        }).join('\n') +
        '\n===========================================\n' +
        'Submitted via Residential Carpentry Educational Platform\n' +
        'Research Study by JOEL P. RODRIGUEZ, LPT, MAVEd'
      );
      
      window.open('mailto:joel.rodriguez@deped.gov.ph?subject=' + subject + '&body=' + body, '_blank', 'noopener,noreferrer');
    });

    document.getElementById('quiz-modal').addEventListener('click', function(e) {
      if (e.target === this) {
        this.classList.add('hidden');
        stopTimer();
      }
    });

    document.getElementById('student-name').addEventListener('keypress', function(e) {
      if (e.key === 'Enter') {
        e.preventDefault();
        const gradeInput = document.getElementById('student-grade');
        if (gradeInput) gradeInput.focus();
      }
    });

    document.getElementById('student-grade').addEventListener('keypress', function(e) {
      if (e.key === 'Enter') {
        e.preventDefault();
        const sectionInput = document.getElementById('student-section');
        if (sectionInput) sectionInput.focus();
      }
    });

    document.getElementById('student-section').addEventListener('keypress', function(e) {
      if (e.key === 'Enter') {
        e.preventDefault();
        startQuiz();
      }
    });

    // Initialize SDK
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities: (config) => ({
          recolorables: [
            {
              get: () => config.background_color || defaultConfig.background_color,
              set: (value) => {
                config.background_color = value;
                window.elementSdk.setConfig({ background_color: value });
              }
            },
            {
              get: () => config.surface_color || defaultConfig.surface_color,
              set: (value) => {
                config.surface_color = value;
                window.elementSdk.setConfig({ surface_color: value });
              }
            },
            {
              get: () => config.text_color || defaultConfig.text_color,
              set: (value) => {
                config.text_color = value;
                window.elementSdk.setConfig({ text_color: value });
              }
            },
            {
              get: () => config.primary_action_color || defaultConfig.primary_action_color,
              set: (value) => {
                config.primary_action_color = value;
                window.elementSdk.setConfig({ primary_action_color: value });
              }
            },
            {
              get: () => config.secondary_action_color || defaultConfig.secondary_action_color,
              set: (value) => {
                config.secondary_action_color = value;
                window.elementSdk.setConfig({ secondary_action_color: value });
              }
            }
          ],
          borderables: [],
          fontEditable: {
            get: () => config.font_family || defaultConfig.font_family,
            set: (value) => {
              config.font_family = value;
              window.elementSdk.setConfig({ font_family: value });
            }
          },
          fontSizeable: {
            get: () => config.font_size || defaultConfig.font_size,
            set: (value) => {
              config.font_size = value;
              window.elementSdk.setConfig({ font_size: value });
            }
          }
        }),
        mapToEditPanelValues: (config) => new Map([
          ['site_title', config.site_title || defaultConfig.site_title],
          ['lesson_title', config.lesson_title || defaultConfig.lesson_title],
          ['quiz_button_text', config.quiz_button_text || defaultConfig.quiz_button_text],
          ['quiz_title', config.quiz_title || defaultConfig.quiz_title],
          ['footer_text', config.footer_text || defaultConfig.footer_text]
        ])
      });
    }

    // Apply initial styles
    onConfigChange(defaultConfig);
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9b9f626695ba043d',t:'MTc2Nzc0NjIyMy4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
