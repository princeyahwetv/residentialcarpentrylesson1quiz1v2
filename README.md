<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Residential Carpentry Quest</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      box-sizing: border-box;
    }
    
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');
    
    * {
      font-family: 'Poppins', -apple-system, BlinkMacSystemFont, sans-serif;
    }
    
    .scenario-card {
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    .scenario-card:hover {
      transform: translateY(-4px);
    }
    
    .choice-btn {
      transition: all 0.2s ease;
    }
    
    .choice-btn:hover:not(:disabled) {
      transform: scale(1.02);
    }
    
    .choice-btn:active:not(:disabled) {
      transform: scale(0.98);
    }
    
    .correct-flash {
      animation: correctPulse 0.6s ease;
    }
    
    .incorrect-flash {
      animation: incorrectShake 0.5s ease;
    }
    
    @keyframes correctPulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }
    
    @keyframes incorrectShake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-10px); }
      75% { transform: translateX(10px); }
    }
    
    .progress-bar {
      transition: width 0.5s ease;
    }
    
    .fade-in {
      animation: fadeIn 0.5s ease;
    }
    
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .star {
      display: inline-block;
      animation: starPop 0.5s ease;
    }
    
    @keyframes starPop {
      0% { transform: scale(0) rotate(0deg); }
      50% { transform: scale(1.2) rotate(180deg); }
      100% { transform: scale(1) rotate(360deg); }
    }
    
    .shooting-star {
      animation: shootingStar 3s ease-in-out infinite;
      filter: drop-shadow(0 0 10px #fbbf24) drop-shadow(0 0 20px #fbbf24);
    }
    
    @keyframes shootingStar {
      0% {
        transform: translate(-100px, 100px) rotate(-45deg);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      50% {
        transform: translate(50px, -50px) rotate(-45deg);
        opacity: 1;
      }
      60% {
        opacity: 0;
      }
      100% {
        transform: translate(100px, -100px) rotate(-45deg);
        opacity: 0;
      }
    }
    
    .star-trail {
      position: absolute;
      width: 80px;
      height: 2px;
      background: linear-gradient(to right, transparent, #fbbf24, transparent);
      animation: trailFade 3s ease-in-out infinite;
    }
    
    @keyframes trailFade {
      0%, 60%, 100% {
        opacity: 0;
      }
      10%, 50% {
        opacity: 1;
      }
    }
    
    .glitter-container {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
    
    .glitter {
      position: absolute;
      width: 4px;
      height: 4px;
      background: #fbbf24;
      border-radius: 50%;
      animation: glitterSparkle 1.5s ease-in-out infinite;
      box-shadow: 0 0 6px #fbbf24, 0 0 12px #fbbf24;
    }
    
    @keyframes glitterSparkle {
      0%, 100% {
        opacity: 0;
        transform: scale(0);
      }
      50% {
        opacity: 1;
        transform: scale(1);
      }
    }
    
    .glitter:nth-child(1) { top: 20%; left: 30%; animation-delay: 0s; }
    .glitter:nth-child(2) { top: 40%; left: 70%; animation-delay: 0.3s; }
    .glitter:nth-child(3) { top: 60%; left: 20%; animation-delay: 0.6s; }
    .glitter:nth-child(4) { top: 80%; left: 60%; animation-delay: 0.9s; }
    .glitter:nth-child(5) { top: 30%; left: 50%; animation-delay: 1.2s; }
    .glitter:nth-child(6) { top: 70%; left: 80%; animation-delay: 0.4s; }
    .glitter:nth-child(7) { top: 50%; left: 40%; animation-delay: 0.7s; }
    .glitter:nth-child(8) { top: 35%; left: 85%; animation-delay: 1s; }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full">
  <div id="app-wrapper" class="h-full w-full overflow-auto"></div>
  <script>
    const defaultConfig = {
      background_color: "#0f172a",
      card_color: "#1e293b",
      text_color: "#f1f5f9",
      correct_color: "#10b981",
      incorrect_color: "#ef4444",
      font_family: "Poppins",
      font_size: 16,
      game_title: "Residential Carpentry Quest",
      intro_text: "Master agricultural tasks and farming practices at home!",
      complete_message: "Congratulations! You've mastered agricultural practices!"
    };

    const scenarios = [
      {
        id: 1,
        task: "Prepare soil for planting",
        taskDescription: "Show how to properly prepare soil by loosening, removing weeds, and adding compost. Take a photo of your prepared garden bed.",
        emoji: "🌱",
        instruction: "Your task: Find a garden area at home. Loosen the soil with a tool, remove any weeds, and mix in compost or organic matter. Take a photo showing your prepared soil ready for planting."
      },
      {
        id: 2,
        task: "Plant seeds or seedlings properly",
        taskDescription: "Demonstrate proper planting technique with correct depth and spacing. Photograph your planting work.",
        emoji: "🌾",
        instruction: "Your task: Plant seeds or seedlings following proper depth and spacing guidelines. Take a photo showing your planting rows or containers with proper technique."
      },
      {
        id: 3,
        task: "Set up a watering system",
        taskDescription: "Show your watering method and schedule for plants. Take a photo of your watering practice.",
        emoji: "💧",
        instruction: "Your task: Demonstrate proper watering technique. Show your watering can, hose, or irrigation system in action. Take a photo showing how you water your plants effectively without overwatering."
      },
      {
        id: 4,
        task: "Perform weeding and maintenance",
        taskDescription: "Show proper weeding technique and plant maintenance. Photograph your maintenance work.",
        emoji: "🌿",
        instruction: "Your task: Remove weeds carefully without damaging crops. Perform basic plant maintenance like removing dead leaves or stems. Take a photo of your weeding and maintenance work."
      },
      {
        id: 5,
        task: "Apply organic fertilizer or compost",
        taskDescription: "Show how to properly apply fertilizer or compost to plants. Photo your fertilization technique.",
        emoji: "🍂",
        instruction: "Your task: Apply organic fertilizer or compost around your plants. Show proper application technique without burning plants. Take a photo demonstrating safe and effective fertilization."
      },
      {
        id: 6,
        task: "Harvest crops properly",
        taskDescription: "Demonstrate proper harvesting technique for vegetables or fruits. Show your harvest.",
        emoji: "🥬",
        instruction: "Your task: Harvest ripe vegetables, fruits, or herbs using proper technique. Show careful handling to avoid plant damage. Take a photo of your harvest and proper harvesting method."
      },
      {
        id: 7,
        task: "Document your garden and submit",
        taskDescription: "Take an overview photo of your complete garden project and submit all evidence to Google Classroom.",
        emoji: "🎓",
        instruction: "Your final task: Take a final photo showing your complete garden or agricultural project. Then gather all 7 evidence photos and upload them to your Agricultural Quest assignment in Google Classroom."
      }
    ];

    let capturedImages = [];
    let studentName = "";
    let hasStarted = false;

    let currentScenario = 0;
    let score = 0;
    let answered = false;

    async function onConfigChange(config) {
      const customFont = config.font_family || defaultConfig.font_family;
      const baseSize = config.font_size || defaultConfig.font_size;
      const bgColor = config.background_color || defaultConfig.background_color;
      const cardColor = config.card_color || defaultConfig.card_color;
      const textColor = config.text_color || defaultConfig.text_color;
      const correctColor = config.correct_color || defaultConfig.correct_color;
      const incorrectColor = config.incorrect_color || defaultConfig.incorrect_color;
      const gameTitle = config.game_title || defaultConfig.game_title;
      const introText = config.intro_text || defaultConfig.intro_text;
      const completeMessage = config.complete_message || defaultConfig.complete_message;

      const app = document.getElementById('app-wrapper');
      app.style.fontFamily = `${customFont}, -apple-system, BlinkMacSystemFont, sans-serif`;
      app.style.backgroundColor = bgColor;
      app.style.color = textColor;

      document.documentElement.style.setProperty('--bg-color', bgColor);
      document.documentElement.style.setProperty('--card-color', cardColor);
      document.documentElement.style.setProperty('--text-color', textColor);
      document.documentElement.style.setProperty('--correct-color', correctColor);
      document.documentElement.style.setProperty('--incorrect-color', incorrectColor);

      const titleElement = document.getElementById('game-title');
      if (titleElement) {
        titleElement.textContent = gameTitle;
        titleElement.style.fontSize = `${baseSize * 2}px`;
      }

      const introElement = document.getElementById('intro-text');
      if (introElement) {
        introElement.textContent = introText;
        introElement.style.fontSize = `${baseSize * 1.125}px`;
      }

      const completeTextElement = document.getElementById('complete-text');
      if (completeTextElement) {
        completeTextElement.textContent = completeMessage;
        completeTextElement.style.fontSize = `${baseSize * 1.125}px`;
      }

      const allText = document.querySelectorAll('.text-base');
      allText.forEach(el => el.style.fontSize = `${baseSize}px`);

      const allLargeText = document.querySelectorAll('.text-xl');
      allLargeText.forEach(el => el.style.fontSize = `${baseSize * 1.25}px`);

      const allSmallText = document.querySelectorAll('.text-sm');
      allSmallText.forEach(el => el.style.fontSize = `${baseSize * 0.875}px`);
    }

    function render() {
      const app = document.getElementById('app-wrapper');
      const bgColor = window.elementSdk?.config?.background_color || defaultConfig.background_color;
      const cardColor = window.elementSdk?.config?.card_color || defaultConfig.card_color;
      const textColor = window.elementSdk?.config?.text_color || defaultConfig.text_color;
      const gameTitle = window.elementSdk?.config?.game_title || defaultConfig.game_title;
      const introText = window.elementSdk?.config?.intro_text || defaultConfig.intro_text;
      const completeMessage = window.elementSdk?.config?.complete_message || defaultConfig.complete_message;

      if (currentScenario === 0 && score === 0 && !answered && !hasStarted) {
        app.innerHTML = `
          <div class="min-h-full flex items-center justify-center p-8" style="background-color: ${bgColor}; color: ${textColor};">
            <div class="max-w-3xl w-full text-center fade-in">
              <div class="mb-6 p-6 rounded-2xl relative overflow-hidden" style="background-color: ${cardColor};">
                <div class="relative inline-block mb-4" style="width: 120px; height: 60px;">
                  <div class="shooting-star text-4xl">⭐</div>
                  <div class="star-trail"></div>
                  <div class="glitter-container">
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                    <div class="glitter"></div>
                  </div>
                </div>
                <h2 class="text-xl font-bold mb-2">ISTEPS-ICT</h2>
                <p class="text-sm opacity-90">Self Tutoring Educational Platform for Students</p>
                <p class="text-xs mt-2 opacity-75">A research study by JOEL P. RODRIGUEZ LPT, MAVED</p>
              </div>
              <div class="text-6xl mb-6">🌾</div>
              <h1 id="game-title" class="text-5xl font-bold mb-4">${gameTitle}</h1>
              <p id="intro-text" class="text-xl mb-8 opacity-90">${introText}</p>
              
              <div class="mb-6">
                <label for="student-name" class="block text-lg font-semibold mb-3">Enter Your Name</label>
                <input 
                  type="text" 
                  id="student-name" 
                  placeholder="Your full name" 
                  class="w-full max-w-md mx-auto px-6 py-4 rounded-xl text-lg text-center font-semibold"
                  style="background-color: ${cardColor}; color: ${textColor}; border: 2px solid rgba(255, 255, 255, 0.2);"
                  value="${studentName}"
                >
                <p id="name-error" class="text-sm mt-2 hidden" style="color: ${window.elementSdk?.config?.incorrect_color || defaultConfig.incorrect_color};">
                  Please enter your name to continue
                </p>
              </div>
              
              <button id="start-btn" class="px-8 py-4 rounded-xl font-semibold text-lg shadow-lg hover:shadow-xl transition-all" style="background-color: ${cardColor}; color: ${textColor};">
                Start Game 🚀
              </button>
            </div>
          </div>
        `;
        
        const nameInput = document.getElementById('student-name');
        const startBtn = document.getElementById('start-btn');
        const nameError = document.getElementById('name-error');
        
        startBtn.addEventListener('click', () => {
          const name = nameInput.value.trim();
          if (name.length > 0) {
            studentName = name;
            hasStarted = true;
            startGame();
          } else {
            nameError.classList.remove('hidden');
            nameInput.style.borderColor = window.elementSdk?.config?.incorrect_color || defaultConfig.incorrect_color;
          }
        });
        
        nameInput.addEventListener('input', () => {
          nameError.classList.add('hidden');
          nameInput.style.borderColor = 'rgba(255, 255, 255, 0.2)';
        });
        
        nameInput.addEventListener('keypress', (e) => {
          if (e.key === 'Enter') {
            startBtn.click();
          }
        });
      } else if (currentScenario < scenarios.length) {
        renderScenario();
      } else {
        renderComplete();
      }
    }

    function startGame() {
      currentScenario = 0;
      score = 0;
      answered = false;
      renderScenario();
    }

    function renderScenario() {
      const app = document.getElementById('app-wrapper');
      const scenario = scenarios[currentScenario];
      const progress = ((currentScenario) / scenarios.length) * 100;
      const bgColor = window.elementSdk?.config?.background_color || defaultConfig.background_color;
      const cardColor = window.elementSdk?.config?.card_color || defaultConfig.card_color;
      const textColor = window.elementSdk?.config?.text_color || defaultConfig.text_color;
      const correctColor = window.elementSdk?.config?.correct_color || defaultConfig.correct_color;
      const incorrectColor = window.elementSdk?.config?.incorrect_color || defaultConfig.incorrect_color;

      const hasImage = capturedImages[currentScenario];

      app.innerHTML = `
        <div class="min-h-full p-6" style="background-color: ${bgColor}; color: ${textColor};">
          <div class="max-w-4xl mx-auto">
            <div class="mb-6">
              <div class="flex justify-between items-center mb-2">
                <span class="text-sm font-semibold">Progress</span>
                <span class="text-sm font-semibold">Completed: ${score}/${scenarios.length}</span>
              </div>
              <div class="w-full h-3 rounded-full overflow-hidden" style="background-color: rgba(255, 255, 255, 0.1);">
                <div class="progress-bar h-full rounded-full" style="width: ${progress}%; background-color: ${correctColor};"></div>
              </div>
            </div>

            <div class="scenario-card rounded-2xl p-8 shadow-2xl fade-in" style="background-color: ${cardColor};">
              <div class="text-center mb-6">
                <div class="text-6xl mb-4">${scenario.emoji}</div>
                <h2 class="text-2xl font-bold mb-2">Task ${currentScenario + 1}: ${scenario.task}</h2>
                <p class="text-lg opacity-90 mb-4">${scenario.taskDescription}</p>
              </div>

              <div class="mb-6 p-6 rounded-xl" style="background-color: rgba(255, 255, 255, 0.05); border: 2px dashed rgba(255, 255, 255, 0.2);">
                <h3 class="font-bold text-lg mb-3">📋 Instructions</h3>
                <p class="text-base">${scenario.instruction}</p>
              </div>

              <div class="mb-6">
                <h3 class="font-bold text-lg mb-3">📸 Upload Evidence</h3>
                <p class="text-sm opacity-75 mb-4">Take a photo or screenshot of your completed task as proof.</p>
                
                <div id="image-preview" class="mb-4 ${hasImage ? '' : 'hidden'}">
                  <img id="preview-img" src="${hasImage || ''}" alt="Evidence preview" class="w-full max-w-md mx-auto rounded-xl shadow-lg" style="max-height: 300px; object-fit: contain;">
                  <button id="remove-img" class="mt-3 px-4 py-2 rounded-lg font-semibold" style="background-color: ${incorrectColor}; color: ${textColor};">
                    Remove Photo
                  </button>
                </div>

                <label for="file-input-${currentScenario}" class="block">
                  <div class="cursor-pointer p-8 rounded-xl text-center transition-all hover:opacity-80" style="background-color: rgba(255, 255, 255, 0.1); border: 2px dashed rgba(255, 255, 255, 0.3);">
                    <div class="text-4xl mb-2">📷</div>
                    <p class="font-semibold">Click to ${hasImage ? 'Change' : 'Upload'} Photo</p>
                    <p class="text-sm opacity-75 mt-1">or take a picture</p>
                  </div>
                </label>
                <input type="file" id="file-input-${currentScenario}" accept="image/*" capture="environment" class="hidden">
              </div>
              
              <button id="complete-btn" class="w-full py-4 rounded-xl font-semibold text-lg transition-all ${hasImage ? '' : 'opacity-50'}" ${hasImage ? '' : 'disabled'} style="background-color: ${correctColor}; color: ${textColor};">
                ${hasImage ? 'Complete Task ✓' : 'Upload Evidence First'}
              </button>
            </div>
          </div>
        </div>
      `;

      const fileInput = document.getElementById(`file-input-${currentScenario}`);
      const previewContainer = document.getElementById('image-preview');
      const previewImg = document.getElementById('preview-img');
      const completeBtn = document.getElementById('complete-btn');
      const removeBtn = document.getElementById('remove-img');

      fileInput.addEventListener('change', (e) => {
        const file = e.target.files[0];
        if (file) {
          const reader = new FileReader();
          reader.onload = (event) => {
            capturedImages[currentScenario] = event.target.result;
            previewImg.src = event.target.result;
            previewContainer.classList.remove('hidden');
            completeBtn.disabled = false;
            completeBtn.classList.remove('opacity-50');
            completeBtn.innerHTML = 'Complete Task ✓';
          };
          reader.readAsDataURL(file);
        }
      });

      if (removeBtn) {
        removeBtn.addEventListener('click', () => {
          capturedImages[currentScenario] = null;
          previewContainer.classList.add('hidden');
          completeBtn.disabled = true;
          completeBtn.classList.add('opacity-50');
          completeBtn.innerHTML = 'Upload Evidence First';
          fileInput.value = '';
        });
      }

      completeBtn.addEventListener('click', () => {
        if (capturedImages[currentScenario]) {
          completeTask();
        }
      });
    }

    function completeTask() {
      score++;
      answered = false;
      currentScenario++;
      render();
    }

    function renderComplete() {
      const app = document.getElementById('app-wrapper');
      const percentage = Math.round((score / scenarios.length) * 100);
      const bgColor = window.elementSdk?.config?.background_color || defaultConfig.background_color;
      const cardColor = window.elementSdk?.config?.card_color || defaultConfig.card_color;
      const textColor = window.elementSdk?.config?.text_color || defaultConfig.text_color;
      const correctColor = window.elementSdk?.config?.correct_color || defaultConfig.correct_color;
      const completeMessage = window.elementSdk?.config?.complete_message || defaultConfig.complete_message;

      let stars = '';
      const starCount = score >= scenarios.length ? 3 : score >= scenarios.length * 0.7 ? 2 : 1;
      for (let i = 0; i < starCount; i++) {
        stars += `<span class="star text-5xl" style="animation-delay: ${i * 0.2}s;">⭐</span>`;
      }

      let evidenceGallery = '';
      capturedImages.forEach((img, index) => {
        if (img) {
          evidenceGallery += `
            <div class="text-center">
              <div class="text-2xl mb-2">${scenarios[index].emoji}</div>
              <img src="${img}" alt="Task ${index + 1} evidence" class="w-full rounded-lg shadow-md mb-2" style="max-height: 150px; object-fit: cover;">
              <p class="text-xs opacity-75">Task ${index + 1}</p>
            </div>
          `;
        }
      });

      app.innerHTML = `
        <div class="min-h-full p-8" style="background-color: ${bgColor}; color: ${textColor};">
          <div class="max-w-4xl mx-auto text-center fade-in">
            <div class="rounded-2xl p-12 shadow-2xl mb-6" style="background-color: ${cardColor};">
              <div class="text-6xl mb-6">🎉</div>
              <h1 class="text-4xl font-bold mb-4">Congratulations, ${studentName}! 🎉</h1>
              <p id="complete-text" class="text-xl mb-6 opacity-90">${completeMessage}</p>
              
              <div class="mb-6">${stars}</div>
              
              <div class="text-6xl font-bold mb-2" style="color: ${correctColor};">${score}/${scenarios.length}</div>
              <p class="text-2xl font-semibold mb-8">Tasks Completed</p>
              
              <div class="mt-8 p-6 rounded-xl text-left" style="background-color: rgba(255, 255, 255, 0.05);">
                <p class="text-base mb-4 leading-relaxed">
                  This task may feel challenging, but remember that even small efforts help promote sustainable agriculture and food production.
                </p>
                <p class="text-base mb-4 leading-relaxed">
                  <strong>Be a responsible 21st-century farmer</strong>—sustainable, knowledgeable, and respectful of the land.
                </p>
                <p class="text-base leading-relaxed">
                  Keep practicing good agricultural techniques and always care for your plants and soil. 🌱🌾
                </p>
              </div>
            </div>

            ${evidenceGallery ? `
              <div class="rounded-2xl p-8 shadow-2xl mb-6" style="background-color: ${cardColor};">
                <h2 class="text-2xl font-bold mb-6">📸 Your Evidence Portfolio</h2>
                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
                  ${evidenceGallery}
                </div>
              </div>
            ` : ''}

            <div class="space-y-4">
              <a href="https://www.youtube.com/watch?v=9IK9a01vyy4" target="_blank" rel="noopener noreferrer" class="block">
                <button class="w-full px-8 py-4 rounded-xl font-semibold text-lg shadow-lg hover:shadow-xl transition-all" style="background-color: ${correctColor}; color: ${textColor};">
                  📤 Send to Your Teacher
                </button>
              </a>
              
              <button id="restart-btn" class="w-full px-8 py-4 rounded-xl font-semibold text-lg shadow-lg hover:shadow-xl transition-all" style="background-color: rgba(255, 255, 255, 0.1); color: ${textColor};">
                Start New Quest 🔄
              </button>
            </div>
          </div>
        </div>
      `;

      document.getElementById('restart-btn').addEventListener('click', () => {
        currentScenario = 0;
        score = 0;
        answered = false;
        hasStarted = false;
        studentName = "";
        capturedImages = [];
        render();
      });
    }

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
              get: () => config.card_color || defaultConfig.card_color,
              set: (value) => {
                config.card_color = value;
                window.elementSdk.setConfig({ card_color: value });
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
              get: () => config.correct_color || defaultConfig.correct_color,
              set: (value) => {
                config.correct_color = value;
                window.elementSdk.setConfig({ correct_color: value });
              }
            },
            {
              get: () => config.incorrect_color || defaultConfig.incorrect_color,
              set: (value) => {
                config.incorrect_color = value;
                window.elementSdk.setConfig({ incorrect_color: value });
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
          ["game_title", config.game_title || defaultConfig.game_title],
          ["intro_text", config.intro_text || defaultConfig.intro_text],
          ["complete_message", config.complete_message || defaultConfig.complete_message]
        ])
      });
    }

    render();
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9bac9d6420d9403a',t:'MTc2Nzg4NDk1NC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
