<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AlexKingHD|Multi-Dimensional Developer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        @keyframes glitch {
            0% { text-shadow: 2px 0 red; }
            25% { text-shadow: -2px 0 cyan; }
            50% { text-shadow: 2px 0 lime; }
            75% { text-shadow: -2px 0 yellow; }
            100% { text-shadow: 2px 0 red; }
        }
        .floating { animation: float 6s ease-in-out infinite; }
        .glitch-effect { animation: glitch 1s linear infinite; }
        .pixel-corners { clip-path: polygon(0 10px, 10px 10px, 10px 0, calc(100% - 10px) 0, calc(100% - 10px) 10px, 100% 10px, 100% calc(100% - 10px), calc(100% - 10px) calc(100% - 10px), calc(100% - 10px) 100%, 10px 100%, 10px calc(100% - 10px), 0 calc(100% - 10px)); }
        .typing-cursor { animation: blink 1s step-end infinite; }
        @keyframes blink { from, to { opacity: 0; } 50% { opacity: 1; } }
        .matrix-bg { background: repeating-linear-gradient(0deg, rgba(0,255,0,0.1), rgba(0,255,0,0.1) 1px, transparent 1px, transparent 2px); }
        .hidden-egg { opacity: 0; transition: all 0.3s; }
        .hidden-egg:hover { opacity: 1; }
        .game-card:hover .game-preview { display: block; }
        .console-text { font-family: 'Courier New', monospace; }


        @keyframes shake {
        0%   { transform: translate(0px, 0px) rotate(0deg); }
        10%  { transform: translate(-0.5px, 1px) rotate(-0.5deg); }
        20%  { transform: translate(1px, -0.5px) rotate(0.5deg); }
        30%  { transform: translate(-1px, 0.5px) rotate(0deg); }
        40%  { transform: translate(0.5px, -1px) rotate(0.5deg); }
        50%  { transform: translate(-0.5px, 1px) rotate(-0.5deg); }
        60%  { transform: translate(1px, -0.5px) rotate(0deg); }
        70%  { transform: translate(-1px, 0.5px) rotate(0.5deg); }
        80%  { transform: translate(0.5px, -1px) rotate(-0.5deg); }
        90%  { transform: translate(-0.5px, 1px) rotate(0deg); }
        100% { transform: translate(0px, 0px) rotate(0deg); }
        }

        .shake {
        animation: shake 1s ease-in-out infinite;
        }

        .pulse-animation {
        animation: pulse 2s infinite;
        }
        @keyframes pulse {
        0% { transform: scale(1); opacity: 1; }
        50% { transform: scale(1.05); opacity: 0.8; }
        100% { transform: scale(1); opacity: 1; }
        }

    </style>
</head>
<body class="bg-gray-900 text-green-400 matrix-bg min-h-screen overflow-x-hidden">
    <!-- Easter Egg Console -->
    <div id="console" class="fixed bottom-0 left-0 w-full bg-black bg-opacity-90 text-green-400 p-4 hidden z-50 h-64 overflow-y-auto">
        <div class="flex justify-between items-center mb-2">
            <span class="console-text">> DEV_CONSOLE v1.0</span>
            <button onclick="closeConsole()" class="text-red-500 hover:text-red-400">X</button>
        </div>
        <div id="console-output" class="console-text mb-2"></div>
        <div class="flex">
            <span class="console-text mr-2">></span>
            <input id="console-input" type="text" class="console-text bg-transparent border-b border-green-400 flex-grow outline-none text-green-400" autocomplete="off">
        </div>
    </div>


    <!-- Hidden Konami Code Listener -->
    <div id="konami-activated" class="fixed inset-0 bg-black z-50 flex items-center justify-center hidden">
        <div class="text-center p-8 bg-gray-900 border-4 border-blue-500 max-w-2xl shadow-2xl">
            <h2 class="text-4xl font-bold mb-4 glitch-effect text-white">UBISOFT DREAM UNLOCKED</h2>
            <p class="mb-4 text-gray-300">
                In another life, I was just a kid holding a controller, escaping into worlds like Assassin's Creed and Far Cry.
                Today, I build those worlds — one line of code at a time.
            </p>
            <p class="mb-6 text-gray-400">
                Ubisoft sparked this fire. This site, these projects, this journey — they all lead there.
                You just unlocked the core of my passion.
            </p>
            <button onclick="closeKonami()" class="px-6 py-2 bg-blue-600 hover:bg-blue-500 text-white font-semibold rounded">
                Back to Reality — For Now
            </button>
        </div>
    </div>

    <div class="hidden-egg absolute top-10 left-10 w-10 h-10 cursor-pointer" onclick="activateConsole()"></div>
    <div class="hidden-egg absolute top-10 right-10 w-10 h-10 cursor-pointer" onclick="showUbisoftDream()"></div>

    <!-- Main Content -->
    <div class="container mx-auto px-4 py-12 relative">
        <!-- Secret Click Areas -->
        
        <!-- Hero Section -->
        <section class="flex flex-col md:flex-row items-center justify-between mb-20 relative">
            <div class="md:w-1/2 mb-10 md:mb-0">
                <h1 class="text-5xl md:text-7xl font-bold mb-4">
                    <span class="text-green-400">Alex</span><span class="text-white">KingH.D.</span>
                </h1>
                <div class="text-2xl md:text-3xl mb-6">
                    <span id="typing-text" class="relative">Multi-Dimensional Developer<span class="typing-cursor">|</span></span>
                </div>
                <p class="text-gray-300 mb-8 text-lg">
                    Bridging worlds between game development, web technologies, AI, and content creation. 
                    My main mission is to finish high school and continue with my second main mission to join the Ubisoft team as a C++ Programmer or Lead Snowdrop Engine Programmer.
                </p>
                <div class="flex space-x-4">
                    <a href="#contact" class="px-6 py-3 bg-green-600 hover:bg-green-500 rounded-lg font-medium transition-all transform hover:scale-105">Hire Me</a>
                    <a href="#projects" class="px-6 py-3 border border-green-400 hover:bg-gray-800 rounded-lg font-medium transition-all transform hover:scale-105">See Projects</a>
                </div>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <div class="relative floating">
                    <div class="w-64 h-64 md:w-80 md:h-80 bg-gray-800 rounded-full overflow-hidden border-4 border-green-400 shadow-lg shadow-green-400/30">
                        <!-- Replace with your image -->
                        <div class="w-full h-full bg-gray-700 flex items-center justify-center">
                        <img src="./src/images/logocanal.png" alt="AlexKingHD" class="w-64 h-64">
                        </div>
                    </div>
                    <div class="absolute -bottom-5 -right-5 bg-gray-800 border-2 border-green-400 p-2 rounded-lg shadow-lg">
                        <span class="text-sm">Currently coding</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Matrix -->
        <section id="skills" class="mb-20">
            <h2 class="text-3xl font-bold mb-10 text-center relative">
                <span class="bg-gray-900 px-4 relative z-10">Dev Toolkit</span>
                <div class="absolute h-1 bg-green-400 top-1/2 left-0 right-0 -z-0"></div>
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Game Dev Card -->
                <div class="bg-gray-800 p-6 rounded-lg border-l-4 border-green-400 hover:shadow-lg hover:shadow-green-400/20 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-gray-700 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-gamepad text-2xl text-green-400"></i>
                        </div>
                        <h3 class="text-xl font-bold">Game Development</h3>
                    </div>
                    <div class="space-y-3">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Unity (C#)</span>
                                <span>70%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 70%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Unreal (C++)</span>
                                <span>15%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 15%"></div>
                            </div>
                        </div>
                    </div>
                    <div class="mt-4 text-sm text-gray-300">
                        Started: Unity (13/04/2025), Unreal (20/06/2025)
                    </div>
                </div>
                
                <!-- Web Front Card -->
                <div class="bg-gray-800 p-6 rounded-lg border-l-4 border-green-400 hover:shadow-lg hover:shadow-green-400/20 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-gray-700 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-code text-2xl text-green-400"></i>
                        </div>
                        <h3 class="text-xl font-bold">Frontend Web</h3>
                    </div>
                    <div class="space-y-3">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>HTML</span>
                                <span>100%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 100%"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Tailwind</span>
                                <span>78%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 78%"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between mb-1">
                                <span>CSS</span>
                                <span>50%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 50%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                
                <!-- Web End Card -->
                <div class="bg-gray-800 p-6 rounded-lg border-l-4 border-green-400 hover:shadow-lg hover:shadow-green-400/20 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-gray-700 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-server text-2xl text-green-400"></i>
                        </div>
                        <h3 class="text-xl font-bold">Backend Web</h3>
                    </div>
                    <div class="space-y-3">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>PHP</span>
                                <span>100%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 100%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>MySQL</span>
                                <span>95%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>React (Vite/TS)</span>
                                <span>85%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2.5">
                                <div class="bg-green-400 h-2.5 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- AI Dev Card -->
                <div class="bg-gray-800 p-6 rounded-lg border-l-4 border-green-400 hover:shadow-lg hover:shadow-green-400/20 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-gray-700 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-robot text-2xl text-green-400"></i>
                        </div>
                        <h3 class="text-xl font-bold">AI Development</h3>
                    </div>
                    <p class="text-xl text-white text-center">Private projects</p>
                    <p class="text-gray-300 mb-4 text-center">Coming in 2026</p>
                    <div class="flex justify-center">
                        <div class="relative w-24 h-24">
                            <div class="absolute inset-0 rounded-full border-4 border-green-400 border-t-transparent animate-spin"></div>
                            <div class="absolute inset-2 rounded-full border-4 border-green-400 border-b-transparent animate-spin animation-delay-100"></div>
                            <div class="absolute inset-4 rounded-full border-4 border-green-400 border-r-transparent animate-spin animation-delay-200"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Showcase -->
        <section id="projects" class="mb-20">
            <h2 class="text-3xl font-bold mb-10 text-center relative">
                <span class="bg-gray-900 px-4 relative z-10">Game Dev Projects</span>
                <div class="absolute h-1 bg-green-400 top-1/2 left-0 right-0 -z-0"></div>
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="game-card bg-gray-800 rounded-lg overflow-hidden border border-gray-700 hover:border-green-400 transition-all relative h-96">
                    <div class="h-48 bg-gray-700 flex items-center justify-center">
                        <i class="fas fa-dice-d20 text-6xl text-green-400"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">MOBA GAME</h3>
                        <p class="text-gray-300 mb-4">A MOBA (Multiplayer Online Battle Arena) game is a competitive video game, in which two players teams are facing in a virtual arena.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">C#</span>
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">Unity</span>
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">3D</span>
                        </div>
                    </div>
                    <div class="game-preview absolute inset-0 bg-black bg-opacity-90 hidden flex items-center justify-center p-6">
                        <div class="text-center">
                            <h4 class="text-xl font-bold mb-4">Coming Soon</h4>
                            <p class="mb-4">This project is currently in development</p>
                            <!-- <button class="px-4 py-2 bg-green-600 rounded hover:bg-green-500">View Details</button> -->
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="game-card bg-gray-800 rounded-lg overflow-hidden border border-gray-700 hover:border-green-400 transition-all relative h-96">
                    <div class="h-48 bg-gray-700 flex items-center justify-center">
                        <i class="fas fa-ghost text-6xl text-green-400"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">FPS GAME</h3>
                        <p class="text-gray-300 mb-4">with realistic experience due to the Unreal Engine</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">C++</span>
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">Unreal</span>
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">Blueprint</span>
                        </div>
                    </div>
                    <div class="game-preview absolute inset-0 bg-black bg-opacity-90 hidden flex items-center justify-center p-6">
                        <div class="text-center">
                            <h4 class="text-xl font-bold mb-4">Coming Soon</h4>
                            <p class="mb-4">This project is currently in development</p>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 (Easter Egg Project) -->
                <div class="game-card bg-gray-800 rounded-lg overflow-hidden border border-gray-700 hover:border-green-400 transition-all relative h-96" onclick="showUbisoftEgg()">
                    <div class="h-48 bg-gray-700 flex items-center justify-center">
                        <i class="fas fa-question text-6xl text-green-400"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Secret Project</h3>
                        <p class="text-gray-300 mb-4">Click to discover something special</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">???</span>
                            <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">Secret</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Content Creation -->
        <section class="mb-20">
            <h2 class="text-3xl font-bold mb-10 text-center relative">
                <span class="bg-gray-900 px-4 relative z-10">Content Creation</span>
                <div class="absolute h-1 bg-green-400 top-1/2 left-0 right-0 -z-0"></div>
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- YouTube -->
                <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 hover:border-green-400 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-red-600 rounded-full flex items-center justify-center mr-4">
                            <i class="fab fa-youtube text-2xl text-white"></i>
                        </div>
                        <h3 class="text-xl font-bold">YouTube</h3>
                    </div>
                    <p class="text-gray-300 mb-4">Game dev tutorials, project showcases, and tech reviews</p>
                    <a href="https://www.youtube.com/@AlexKingHDV1" target="_blank" class="inline-block px-4 py-2 bg-red-600 hover:bg-red-500 rounded text-white">
                        Visit Channel
                    </a>
                </div>
                
                <!-- Kick -->
                <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 hover:border-green-400 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center mr-4">
                            <img src="https://i.pinimg.com/736x/f6/4f/56/f64f5611aabc03a17fa0a1ddfc7d0490.jpg">
                        </div>
                        <h3 class="text-xl font-bold">Kick</h3>
                    </div>
                    <p class="text-gray-300 mb-4">Live coding sessions, game development streams</p>
                    <a href="https://kick.com/alexkinghd" target="_blank" class="inline-block px-4 py-2 bg-purple-600 hover:bg-purple-500 rounded text-white">
                        Follow Me
                    </a>
                </div>
                
                <!-- Twitch -->
                <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 hover:border-green-400 transition-all">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-purple-500 rounded-full flex items-center justify-center mr-4">
                            <i class="fab fa-twitch text-2xl text-white"></i>
                        </div>
                        <h3 class="text-xl font-bold">Twitch</h3>
                    </div>
                    <p class="text-gray-300 mb-4">Game development and occasional gaming streams</p>
                    <a href="https://www.twitch.tv/alexkinghdv2/about" target="_blank" class="inline-block px-4 py-2 bg-purple-500 hover:bg-purple-400 rounded text-white">
                        Follow Me
                    </a>
                </div>
            </div>
        </section>

        <!-- Ubisoft Dream -->
        <section class="mb-20 bg-gray-800 rounded-lg p-8 border border-green-400 relative overflow-hidden">
            <div class="absolute -right-20 -top-20 w-64 h-64 bg-green-400 rounded-full opacity-10"></div>
            <div class="absolute -left-20 -bottom-20 w-64 h-64 bg-green-400 rounded-full opacity-10"></div>
            <div class="relative z-10">
                <h2 class="text-3xl font-bold mb-6 text-center">Ubisoft Dream</h2>
                <div class="flex flex-col md:flex-row items-center">
                    <div class="md:w-1/2 mb-6 md:mb-0 flex justify-center">
                        <div class="w-48 h-48 bg-gray-700 rounded-lg border-2 border-green-400 flex items-center justify-center">
                            <i class="fas fa-crown text-6xl text-yellow-400"></i>
                        </div>
                    </div>
                    <div class="md:w-1/2">
                        <p class="text-gray-300 mb-4">
                            My ultimate goal is to join Ubisoft’s creative forces, helping shape worlds that inspire millions — just like their games inspired me.
                            It all started when I first played *Assassin’s Creed* and got lost in the immersive storytelling and breathtaking world-building.
                        </p>
                        <p class="text-gray-300 mb-4">
                            That moment sparked more than just curiosity — it planted a seed. I didn’t just want to *play* games. I wanted to *make* them.
                            Ubisoft represents everything I admire in the industry: innovation, narrative depth, and communities that truly connect.
                        </p>
                        <p class="text-gray-300 mb-6">
                            Today, I write code with the same excitement I had holding a controller as a kid — every day pushing myself to become the kind of developer I'd want on *their* team.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact -->
        <section id="contact" class="mb-20">
            <h2 class="text-3xl font-bold mb-10 text-center relative">
                <span class="bg-gray-900 px-4 relative z-10">Get In Touch</span>
                <div class="absolute h-1 bg-green-400 top-1/2 left-0 right-0 -z-0"></div>
            </h2>
            
            <div class="bg-gray-800 rounded-lg p-8 max-w-3xl mx-auto">
                <form id="contact-form" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <label for="name" class="block mb-2 text-sm font-medium">Your Name</label>
                            <input type="text" id="name" class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-green-400 focus:border-green-400" required>
                        </div>
                        <div>
                            <label for="email" class="block mb-2 text-sm font-medium">Your Email</label>
                            <input type="email" id="email" class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-green-400 focus:border-green-400" required>
                        </div>
                    </div>
                    <div>
                        <label for="subject" class="block mb-2 text-sm font-medium">Subject</label>
                        <input type="text" id="subject" class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-green-400 focus:border-green-400" required>
                    </div>
                    <div>
                        <label for="message" class="block mb-2 text-sm font-medium">Message</label>
                        <textarea id="message" rows="5" class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-green-400 focus:border-green-400" required></textarea>
                    </div>
                    <button type="submit" class="px-6 py-3 bg-green-600 hover:bg-green-500 rounded-lg font-medium w-full transition-all transform hover:scale-105">
                        Send Message
                    </button>
                </form>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 py-8 border-t border-gray-700">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h2 class="text-2xl font-bold">
                        <span class="text-green-400">Alex</span><span class="text-white">KingH.D.</span>
                    </h2>
                    <p class="text-gray-400">Multi-Dimensional Developer</p>
                </div>
                <div class="flex space-x-6">
                    <a href="https://www.youtube.com/@AlexKingHDV1" target="_blank" class="text-gray-400 hover:text-red-500 text-2xl">
                        <i class="fab fa-youtube"></i>
                    </a>
                    <a href="https://kick.com/alexkinghd" target="_blank" class="text-gray-400 hover:text-purple-400 text-2xl">
                        <span class="font-bold">K</span>
                    </a>
                    <a href="https://www.twitch.tv/alexkinghdv2/about" target="_blank" class="text-gray-400 hover:text-purple-400 text-2xl">
                        <i class="fab fa-twitch"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-blue-400 text-2xl">
                        <i class="fab fa-linkedin"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-gray-300 text-2xl">
                        <i class="fab fa-github"></i>
                    </a>
                </div>
            </div>
            <div class="mt-8 text-center text-gray-500 text-sm">
                <p>© 2025 AlexKingHD. All rights reserved. Designed with passion and code.</p>
                <p class="mt-2">Looking for the console? Try the Konami code ↑↑↓↓←→←→</p>
            </div>
        </div>

    <!-- Fake Call Overlay -->
    <div id="fake-call" class="fixed bg-black bg-opacity-90 inset-0 z-50 hidden flex items-center justify-center">
        <div id="call-window" class="bg-gray-800 border-4 border-green-400 p-8 rounded-xl text-center max-w-sm w-full shadow-lg">
            <!-- Conținutul -->
        </div>
    </div>



    </footer>


    <script>

        let currentAudioId = null;
        let callTimerInterval = null;


        // Typing animation
        const typingText = document.getElementById('typing-text');
        const phrases = ["Multi-Dimensional Developer", "Beginner Game Developer", "Web Wizard", "AI Explorer", "Content Creator"];
        let phraseIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        let isEnd = false;

        function type() {
            const currentPhrase = phrases[phraseIndex];
            
            if (isDeleting) {
                typingText.textContent = currentPhrase.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingText.textContent = currentPhrase.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentPhrase.length) {
                isEnd = true;
                setTimeout(() => {
                    isDeleting = true;
                }, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                phraseIndex = (phraseIndex + 1) % phrases.length;
            }

            const speed = isDeleting ? 100 : isEnd ? 200 : 150;
            setTimeout(type, speed);
            isEnd = false;
        }

        // Start typing animation
        setTimeout(type, 1000);

        // Easter Egg Console
        function activateConsole() {
            const consoleElement = document.getElementById('console');
            consoleElement.classList.remove('hidden');
            document.getElementById('console-input').focus();
            
            // Add welcome message
            const output = document.getElementById('console-output');
            output.innerHTML = `
                <div>> Welcome to AlexKingHD's Developer Console</div>
                <div>> Type 'help' for available commands</div>
            `;

            showFakeCall("id-2");
        }

        function closeConsole() {
            document.getElementById('console').classList.add('hidden');
        }

        // Console commands
        document.getElementById('console-input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                const input = this.value.trim();
                const output = document.getElementById('console-output');
                
                // Add input to output
                output.innerHTML += `<div>> ${input}</div>`;
                
                // Process commands
                switch(input.toLowerCase()) {
                    case 'help':
                        output.innerHTML += `
                            <div>> Available commands:</div>
                            <div>> - about: Learn about AlexKingHD</div>
                            <div>> - skills: View skill details</div>
                            <div>> - ubisoft: Secret Ubisoft dream</div>
                            <div>> - clear: Clear console</div>
                            <div>> - easteregg: Find hidden eggs</div>
                        `;
                        break;
                    case 'about':
                        output.innerHTML += `
                            <div>> AlexKingHD is a multi-disciplinary developer specializing in:</div>
                            <div>> - Game Development (Unity/Unreal)</div>
                            <div>> - Web Development (Frontend/Backend)</div>
                            <div>> - AI Development (Coming 2026)</div>
                            <div>> - Content Creation (YouTube/Twitch/Kick)</div>
                        `;
                        break;
                    case 'skills':
                        output.innerHTML += `
                            <div>> Current skill levels:</div>
                            <div>> Unity: 70% (Started: 13/04/2025)</div>
                            <div>> Unreal: 15% (Started: 20/06/2025)</div>
                            <div>> Tailwind: 78%</div>
                            <div>> CSS: 50%</div>
                            <div>> PHP: 100% (First backend language)</div>
                            <div>> MySQL: 95%</div>
                            <div>> React (Vite/TS): 35%</div>
                        `;
                        break;
                    case 'ubisoft':
                        output.innerHTML += `<div>> Ubisoft isn't just a company to me — it's the reason I started coding.</div>
                                            <div>> My dream is to join them, not just as a fan — but as a creator.</div>`;
                        showUbisoftDream();
                        break;
                    case 'clear':
                        output.innerHTML = '';
                        break;
                    case 'easteregg':
                        output.innerHTML += `
                            <div>> You've found the console Easter egg!</div>
                            <div>> Try clicking around the website for more secrets.</div>
                            <div>> Hint: Check the top corners of the page.</div>
                        `;
                        break;
                    default:
                        output.innerHTML += `<div>> Unknown command. Type 'help' for available commands.</div>`;
                }
                
                // Clear input
                this.value = '';
                
                // Scroll to bottom
                output.scrollTop = output.scrollHeight;
            }
        });

        // Konami Code
        const konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight'];
        let konamiIndex = 0;

        document.addEventListener('keydown', function(e) {
            if (e.key === konamiCode[konamiIndex]) {
                konamiIndex++;
                if (konamiIndex === konamiCode.length) {
                    activateKonami();
                    konamiIndex = 0;
                }
            } else {
                konamiIndex = 0;
            }
        });

        function activateKonami() {
            document.getElementById('konami-activated').classList.remove('hidden');
            document.body.style.overflow = 'hidden';

        showFakeCall("id-1");
        }


        function closeKonami() {
            document.getElementById('konami-activated').classList.add('hidden');
            document.body.style.overflow = 'auto';
        }

        // Ubisoft Easter Egg
        function showUbisoftDream() {
            const output = document.getElementById('console-output');
            if (output) {
                output.innerHTML += `
                    <div>> AlexKingHD's Ubisoft Dream:</div>
                    <div>> From playing games to developing own game,</div>
                    <div>> the journey to Ubisoft is a path of passion and dedication.</div>
                    <div>> Every line of code brings this dream closer to reality.</div>
                `;
                output.scrollTop = output.scrollHeight;
            }
            
            // Visual effect
            document.body.classList.add('glitch-effect');
            setTimeout(() => {
                document.body.classList.remove('glitch-effect');
            }, 1000);
        }

        function showUbisoftEgg() {
            alert("You found a secret path! The Konami code (↑↑↓↓←→←→) will reveal more about my Ubisoft dream.");
        }

        // Contact form
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });


            function showFakeCall(audioId) {
                const callWindow = document.getElementById("fake-call");
                const callBox = document.getElementById("call-window");

                callWindow.classList.remove("hidden");

                callBox.classList.remove("bottom-4", "left-4", "fixed", "max-w-xs", "text-left", "p-4");

                callBox.classList.add("shake");

                callBox.innerHTML = `
                <h2 class="text-2xl font-bold mb-2 text-center">Incoming Call</h2>
                <h1 class="text-xl text-white font-bold mb-4 text-center">Rafi</h1>
                <img src="./src/images/avatar.webp" alt="Rafi Avatar" class="w-24 h-24 rounded-full mx-auto mb-6 pulse-animation">\

                <div id="call-buttons" class="w-full flex justify-center space-x-8">
                    <!-- Decline Button -->
                    <button onclick="declineCall()"  class="flex flex-col items-center">
                    <div class="w-16 h-16 rounded-full bg-red-500 flex items-center justify-center shadow-lg hover:bg-red-600 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 8l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2M5 3a2 2 0 00-2 2v1c0 8.284 6.716 15 15 15h1a2 2 0 002-2v-3.28a1 1 0 00-.684-.948l-4.493-1.498a1 1 0 00-1.21.502l-1.13 2.257a11.042 11.042 0 01-5.516-5.517l2.257-1.128a1 1 0 00.502-1.21L9.228 3.683A1 1 0 008.279 3H5z" />
                        </svg>
                    </div>
                    <span class="text-sm mt-2">Decline</span>
                    </button>
                    
                    <!-- Answer Button -->
                    <button onclick="answerCall()" class="flex flex-col items-center">
                    <div class="w-16 h-16 rounded-full bg-green-500 flex items-center justify-center shadow-lg hover:bg-green-600 transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                        </svg>
                    </div>
                    <span class="text-sm mt-2">Answer</span>
                    </button>
                </div>


                <div id="end-call-container" class="hidden mt-4 flex justify-center">
                    <button onclick="endCall()" class="bg-red-700 hover:bg-red-600 px-6 py-2 rounded-full text-white">
                        End Call
                    </button>
                </div>
              `;

                currentAudioId = audioId;

                const ringTone = new Audio('./src/sounds/ringtone.mp3');
                ringTone.loop = true;
                ringTone.play();

                window.fakeRingtone = ringTone;
            }


            function answerCall() {
                const callWindow = document.getElementById("fake-call");
                const callBox = document.getElementById("call-window");
                const callButtons = document.getElementById("call-buttons");
                const endCallContainer = document.getElementById("end-call-container");

                callButtons.classList.add("hidden");
                endCallContainer.classList.remove("hidden");

                callBox.classList.remove("shake"); 

                if (window.fakeRingtone) {
                    window.fakeRingtone.pause();
                    window.fakeRingtone.currentTime = 0;
                }

                callBox.classList.add("fixed", "top-4", "right-4", "max-w-xs", "text-left", "p-4");
                callBox.innerHTML = `
                    <div class="flex items-center gap-3 mb-2">
                        <img src="./src/images/avatar.webp" alt="Rafi Avatar" class="w-12 h-12 rounded-full">
                        <div>
                            <p class="text-white font-bold">Rafi</p>
                            <p id="call-timer" class="text-sm text-green-300">00:00</p>
                        </div>
                    </div>
                    <div id="end-call-container" class="mt-2">
                        <button onclick="endCall()" class="bg-red-700 hover:bg-red-600 px-4 py-1 rounded-full text-white">
                            End Call
                        </button>
                    </div>
                `;

                if (currentAudioId) {
                    const audio = document.getElementById(currentAudioId);
                    if (audio) {
                        audio.currentTime = 0;
                        audio.play();

                        let seconds = 0;
                        const timerElement = document.getElementById("call-timer");

                        callTimerInterval = setInterval(() => {
                            seconds++;
                            const mins = String(Math.floor(seconds / 60)).padStart(2, '0');
                            const secs = String(seconds % 60).padStart(2, '0');
                            timerElement.textContent = `${mins}:${secs}`;
                        }, 1000);

                        audio.onended = () => {
                            endCall();
                        };
                    }
                }
            }

            function endCall() {
                const callWindow = document.getElementById("fake-call");

                if (currentAudioId) {
                    const audio = document.getElementById(currentAudioId);
                    if (audio) {
                        audio.pause();
                        audio.currentTime = 0;
                        audio.onended = null;
                    }
                }

                if (callTimerInterval) {
                    clearInterval(callTimerInterval);
                    callTimerInterval = null;
                }

                callWindow.classList.add("hidden");
                currentAudioId = null;
            }


            function declineCall() {
                const callWindow = document.getElementById("fake-call");

                if (window.fakeRingtone) {
                    window.fakeRingtone.pause();
                    window.fakeRingtone.currentTime = 0;
                }

                document.getElementById("call-window").classList.remove("shake");

                callWindow.classList.add("hidden");
                currentAudioId = null;
}




    </script>
    <audio id="id-1" src="./src/sounds/id1.mp3"></audio>
    <audio id="id-2" src="./src/sounds/id2.mp3"></audio>
</body>
</html>
