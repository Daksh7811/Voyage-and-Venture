<html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voyage & Venture | Vibrant Cultural Travels</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'papaya': '#FF9A76',
                        'peach': '#FFB26B',
                        'sunshine': '#FFD56F',
                        'leaf': '#939B62',
                        'ocean': '#156064',
                        'coral': '#FF7F50',
                        'plum': '#9A5B6A',
                        'sky': '#87CEEB'
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #F6F4F0 100%);
        }
        
        .hero-bg {
            background: linear-gradient(45deg, 
                rgba(255, 154, 118, 0.8) 0%, 
                rgba(255, 178, 107, 0.7) 30%, 
                rgba(255, 213, 111, 0.6) 70%, 
                rgba(147, 155, 98, 0.5) 100%),
                url('https://placehold.co/1920x1080?text=World+Culture+Journeys&font=poppins') center/cover;
        }
        
        .feature-card {
            transition: all 0.3s ease;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px -10px rgba(0,0,0,0.1);
        }
        
        .feature-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px -10px rgba(0,0,0,0.2);
        }
        
        .gradient-text {
            background: linear-gradient(90deg, #FF9A76, #156064);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .culture-tab {
            transition: all 0.3s;
        }
        
        .culture-tab.active {
            transform: scale(1.05);
            box-shadow: 0 10px 20px -5px rgba(0,0,0,0.1);
        }
        
        .activity-item {
            background: white;
            border-radius: 15px;
            transition: all 0.3s;
        }
        
        .activity-item:hover {
            transform: translateX(5px);
        }
        
        .animate-bounce-slow {
            animation: bounce 3s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        .floating {
            animation: floating 6s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
    </style>
</head>
<body class="overflow-x-hidden">
    <!-- Floating decorative elements -->
    <div class="fixed -left-20 top-1/4 w-40 h-40 rounded-full bg-papaya opacity-30 blur-xl -z-10"></div>
    <div class="fixed -right-20 bottom-1/4 w-60 h-60 rounded-full bg-leaf opacity-20 blur-xl -z-10"></div>
    
    <!-- Navigation -->
    <nav class="bg-white/90 backdrop-blur-md border-b border-white/30 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex justify-between items-center py-4">
                <div class="flex items-center space-x-2">
                    <img class="h-10 w-10" src="https://placehold.co/100x100?text=VV&font=poppins" alt="Voyage & Ventures Logo - Colorful compass icon">
                    <span class="text-2xl font-bold gradient-text hidden sm:inline">Voyage & Venture</span>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#" class="font-medium text-gray-700 hover:text-ocean transition">Home</a>
                    <a href="#features" class="font-medium text-gray-700 hover:text-ocean transition">Features</a>
                    <a href="#tours" class="font-medium text-gray-700 hover:text-ocean transition">Tours</a>
                    <a href="#plan" class="font-medium text-gray-700 hover:text-ocean transition">Plan Trip</a>
                    <a href="#community" class="font-medium text-gray-700 hover:text-ocean transition">Community</a>
                </div>
                <div class="flex items-center space-x-4">
                    <button class="bg-gradient-to-r from-papaya to-peach text-white px-5 py-2 rounded-full font-medium hover:opacity-90 transition shadow-lg">
                        Sign In
                    </button>
                    <button class="md:hidden text-gray-700">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-bg min-h-[90vh] flex items-center relative overflow-hidden">
        <div class="absolute inset-0 z-10 bg-black/20"></div>
        <div class="max-w-7xl mx-auto px-6 z-20 py-20">
            <div class="text-center md:text-left md:w-2/3">
                <h1 class="text-5xl md:text-7xl font-bold text-white mb-6 leading-tight">
                    Travel With <span class="text-amber-200">Color,</span> 
                    <span class="text-emerald-100">Culture,</span> and 
                    <span class="text-coral">Connection</span>
                </h1>
                <p class="text-xl text-white/90 mb-10 max-w-2xl">
                    Our vibrant journeys connect you to the roots of local cultures while charting new routes of discovery through immersive experiences.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                    <button class="bg-gradient-to-r from-ocean to-leaf text-white px-8 py-4 rounded-full font-bold text-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1 flex items-center">
                        <i class="fas fa-play-circle mr-2"></i> Explore Tours
                    </button>
                    <button onclick="openModal('quizModal')" class="bg-white/20 backdrop-blur-md border-2 border-white text-white px-8 py-4 rounded-full font-bold text-lg hover:bg-white/30 transition flex items-center">
                        <i class="fas fa-question-circle mr-2"></i> Take Our Quiz
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Floating decorative shapes -->
        <div class="absolute bottom-20 right-20 w-24 h-24 bg-sunshine rounded-full opacity-80 animate-bounce-slow hidden lg:block"></div>
        <div class="absolute bottom-1/3 left-1/4 w-16 h-16 bg-white rounded-full opacity-70 floating hidden lg:block" style="animation-delay: 0.5s;"></div>
        <div class="absolute top-1/4 right-1/3 w-20 h-20 bg-coral rounded-lg rotate-45 opacity-70 floating hidden lg:block" style="animation-delay: 1s;"></div>
    </section>

    <!-- Features Grid -->
    <section id="features" class="py-20 px-6 max-w-7xl mx-auto">
        <div class="text-center mb-16">
            <h2 class="text-4xl font-bold mb-4 gradient-text">Our Colorful Features</h2>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                Experience travel planning reimagined with our vibrant suite of tools designed for cultural explorers
            </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Feature 1 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-sky to-ocean flex items-center justify-center">
                    <i class="fas fa-clipboard-list text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-ocean">Culture Match Quiz</h3>
                    <p class="text-gray-600 mb-4">
                        Take our vibrant personality quiz to match with tours tailored to your interests in history, food, art, or nature.
                    </p>
                    <button class="text-papaya font-medium flex items-center">
                        Try it now <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
            
            <!-- Feature 2 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-peach to-coral flex items-center justify-center">
                    <i class="fas fa-home text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-coral">Local Homestays</h3>
                    <p class="text-gray-600 mb-4">
                        Stay with verified local families in colorful homes that immerse you in authentic daily life and traditions.
                    </p>
                    <button class="text-peach font-medium flex items-center">
                        Browse stays <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
            
            <!-- Feature 3 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-sunshine to-leaf flex items-center justify-center">
                    <i class="fas fa-hands-helping text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-leaf">Artisan Workshops</h3>
                    <p class="text-gray-600 mb-4">
                        Learn pottery, dance, weaving and more directly from master craftspeople in their vibrant studios.
                    </p>
                    <button class="text-leaf font-medium flex items-center">
                        Discover classes <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
            
            <!-- Feature 4 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-plum to-papaya flex items-center justify-center">
                    <i class="fas fa-film text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-plum">Cultural Documentaries</h3>
                    <p class="text-gray-600 mb-4">
                        Watch vibrant short films showcasing destinations before you visit, with local stories and traditions.
                    </p>
                    <button class="text-plum font-medium flex items-center">
                        Watch previews <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
            
            <!-- Feature 5 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-ocean to-sky flex items-center justify-center">
                    <i class="fas fa-language text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-sky">Language Guides</h3>
                    <p class="text-gray-600 mb-4">
                        Learn essential phrases and cultural customs through our colorful interactive mini-guides.
                    </p>
                    <button class="text-ocean font-medium flex items-center">
                        Start learning <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
            
            <!-- Feature 6 -->
            <div class="feature-card">
                <div class="h-48 bg-gradient-to-r from-leaf to-sunshine flex items-center justify-center">
                    <i class="fas fa-map-marked-alt text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-xl font-bold mb-3 text-sunshine">Roots Mapper</h3>
                    <p class="text-gray-600 mb-4">
                        Trace your ancestry and plan visits to ancestral villages with our colorful mapping tools.
                    </p>
                    <button class="text-leaf font-medium flex items-center">
                        Explore heritage <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Quiz Modal -->
    <div id="quizModal" class="fixed inset-0 bg-black/50 backdrop-blur-md flex items-center justify-center z-50 hidden" onclick="closeModal('quizModal')">
        <div class="bg-white rounded-3xl p-8 max-w-2xl w-full max-h-[90vh] overflow-y-auto mx-4 relative" onclick="event.stopPropagation()">
            <button onclick="closeModal('quizModal')" class="absolute top-4 right-4 text-gray-500 hover:text-gray-700">
                <i class="fas fa-times text-xl"></i>
            </button>
            
            <div class="text-center mb-8">
                <h2 class="text-3xl font-bold mb-4 gradient-text">Find Your Perfect Cultural Match</h2>
                <p class="text-gray-600">Answer just 5 questions to discover tours tailored to your interests</p>
                <div class="w-full bg-gray-200 rounded-full h-2.5 mt-4">
                    <div class="bg-gradient-to-r from-papaya to-leaf h-2.5 rounded-full" style="width: 20%"></div>
                </div>
            </div>
            
            <!-- Question 1 -->
            <div id="quizQ1" class="quiz-question">
                <h3 class="text-xl font-semibold mb-6">1. What sparks your travel excitement?</h3>
                <div class="grid grid-cols-2 gap-4">
                    <button class="quiz-option h-32 flex flex-col items-center justify-center rounded-xl bg-gradient-to-br from-amber-50 to-amber-100 border-2 border-amber-200 hover:border-amber-400 transition" data-category="history">
                        <i class="fas fa-landmark text-4xl text-amber-600 mb-3"></i>
                        <span class="font-medium text-amber-800">Ancient Wonders</span>
                    </button>
                    <button class="quiz-option h-32 flex flex-col items-center justify-center rounded-xl bg-gradient-to-br from-red-50 to-red-100 border-2 border-red-200 hover:border-red-400 transition" data-category="food">
                        <i class="fas fa-utensils text-4xl text-red-600 mb-3"></i>
                        <span class="font-medium text-red-800">Local Flavors</span>
                    </button>
                    <button class="quiz-option h-32 flex flex-col items-center justify-center rounded-xl bg-gradient-to-br from-blue-50 to-blue-100 border-2 border-blue-200 hover:border-blue-400 transition" data-category="art">
                        <i class="fas fa-paint-brush text-4xl text-blue-600 mb-3"></i>
                        <span class="font-medium text-blue-800">Creative Expressions</span>
                    </button>
                    <button class="quiz-option h-32 flex flex-col items-center justify-center rounded-xl bg-gradient-to-br from-green-50 to-green-100 border-2 border-green-200 hover:border-green-400 transition" data-category="nature">
                        <i class="fas fa-tree text-4xl text-green-600 mb-3"></i>
                        <span class="font-medium text-green-800">Natural Beauty</span>
                    </button>
                </div>
            </div>
            
            <!-- Question 2 (hidden initially) -->
            <div id="quizQ2" class="quiz-question hidden">
                <h3 class="text-xl font-semibold mb-6">2. Choose your ideal day abroad:</h3>
                <div class="space-y-4">
                    <button class="quiz-option w-full p-4 text-left rounded-xl bg-gradient-to-r from-purple-50 to-purple-100 border-2 border-purple-200 hover:border-purple-400 transition">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-university text-purple-600 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-purple-800">Exploring museums and historic sites</h4>
                                <p class="text-sm text-purple-600">Absorbing centuries of stories</p>
                            </div>
                        </div>
                    </button>
                    <button class="quiz-option w-full p-4 text-left rounded-xl bg-gradient-to-r from-orange-50 to-orange-100 border-2 border-orange-200 hover:border-orange-400 transition">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-orange-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-store-alt text-orange-600 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-orange-800">Market hopping and cooking classes</h4>
                                <p class="text-sm text-orange-600">Tasting authentic regional flavors</p>
                            </div>
                        </div>
                    </button>
                    <button class="quiz-option w-full p-4 text-left rounded-xl bg-gradient-to-r from-cyan-50 to-cyan-100 border-2 border-cyan-200 hover:border-cyan-400 transition">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-cyan-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-theater-masks text-cyan-600 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-cyan-800">Gallery tours and craft workshops</h4>
                                <p class="text-sm text-cyan-600">Engaging with local artists</p>
                            </div>
                        </div>
                    </button>
                    <button class="quiz-option w-full p-4 text-left rounded-xl bg-gradient-to-r from-lime-50 to-lime-100 border-2 border-lime-200 hover:border-lime-400 transition">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-lime-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-hiking text-lime-600 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lime-800">Hiking to scenic viewpoints</h4>
                                <p class="text-sm text-lime-600">Connecting with nature's beauty</p>
                            </div>
                        </div>
                    </button>
                </div>
            </div>
            
            <!-- Navigation buttons -->
            <div class="flex justify-between mt-8">
                <button class="text-gray-500 hover:text-gray-700 font-medium" disabled>
                    <i class="fas fa-arrow-left mr-2"></i> Back
                </button>
                <button class="bg-gradient-to-r from-papaya to-peach text-white px-6 py-2 rounded-full font-medium hover:shadow-lg transition disabled:opacity-50" disabled>
                    Next <i class="fas fa-arrow-right ml-2"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Cultural Explorer Section -->
    <section id="tours" class="py-20 bg-gradient-to-b from-white to-amber-50">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Curated Cultural Experiences</h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Journey through our rainbow of immersive tours designed to connect you with local traditions
                </p>
            </div>
            
            <!-- Culture Tabs -->
            <div class="flex flex-wrap justify-center gap-2 mb-12">
                <button class="culture-tab active px-6 py-2 rounded-full font-medium bg-gradient-to-r from-papaya to-peach text-white" data-category="all">
                    Show All
                </button>
                <button class="culture-tab px-6 py-2 rounded-full font-medium bg-amber-100 text-amber-800 border border-amber-200" data-category="history">
                    <i class="fas fa-landmark mr-2"></i> History
                </button>
                <button class="culture-tab px-6 py-2 rounded-full font-medium bg-red-100 text-red-800 border border-red-200" data-category="food">
                    <i class="fas fa-utensils mr-2"></i> Food
                </button>
                <button class="culture-tab px-6 py-2 rounded-full font-medium bg-blue-100 text-blue-800 border border-blue-200" data-category="art">
                    <i class="fas fa-palette mr-2"></i> Art
                </button>
                <button class="culture-tab px-6 py-2 rounded-full font-medium bg-green-100 text-green-800 border border-green-200" data-category="nature">
                    <i class="fas fa-leaf mr-2"></i> Nature
                </button>
            </div>
            
            <!-- Tours Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Tour 1 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="history">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Rajasthan+Heritage" alt="Colorful palaces and forts of Rajasthan with intricate carvings" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-amber-600 text-white text-sm font-medium rounded-full">History</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Royal Rajasthan Trail</h3>
                        <p class="text-gray-600 mb-4">Explore the vibrant forts and palaces while learning Maharaja history from local experts</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹12,299</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Tour 2 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="food">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Bengal+Food+Tour" alt="Vibrant Bengal street food market with colorful dishes and ingredients" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-red-600 text-white text-sm font-medium rounded-full">Food</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Bengal Culinary Adventure</h3>
                        <p class="text-gray-600 mb-4">Cook with local chefs and taste your way through floating markets and night bazaars</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹16,899</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Tour 3 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="art">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Ahemdabad+Art+Tour" alt="Renaissance art galleries and sculptures in Florence with golden light" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-blue-600 text-white text-sm font-medium rounded-full">Art</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800"> Ahemdabad Journey</h3>
                        <p class="text-gray-600 mb-4">Private viewings and workshops with modern masters</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹17,599</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Tour 4 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="nature">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Karnataka+Eco+Tour" alt="Lush green rainforest with colorful toucans and tropical plants" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-green-600 text-white text-sm font-medium rounded-full">Nature</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Madhya Pradesh Wildlife Immersion</h3>
                        <p class="text-gray-600 mb-4">Meet rare wildlife with conservationists in the vibrant rainforests and beaches</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹14,199</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Tour 5 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="history">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Hampi+Archaeology" alt="Ancient Hampi's temple under golden sunlight" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-amber-600 text-white text-sm font-medium rounded-full">History</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Hampi Archaeology Expedition</h3>
                        <p class="text-gray-600 mb-4">Special access to excavation sites and expert-led tours of ancient wonders</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹13,299</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Tour 6 -->
                <div class="tour-card culture-card bg-white rounded-2xl overflow-hidden shadow-xl" data-category="food">
                    <div class="relative h-48">
                        <img src="https://placehold.co/600x400?text=Asam's+Tea+Culture" alt="Traditional Asam's tea ceremony in garden setting" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                            <span class="inline-block px-3 py-1 bg-red-600 text-white text-sm font-medium rounded-full">Food</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Assam's Tea & Gastronomy</h3>
                        <p class="text-gray-600 mb-4">Tea ceremonies with masters in Assam's hidden gems</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-xl text-ocean">₹16,899</span>
                                <span class="text-gray-500 text-sm">/ person</span>
                            </div>
                            <button class="px-4 py-2 bg-gradient-to-r from-papaya to-peach text-white rounded-full text-sm font-medium hover:shadow-md transition">
                                Details
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <button class="px-8 py-3 border-2 border-papaya text-papaya font-bold rounded-full hover:bg-papaya hover:text-white transition duration-300">
                    View All Cultural Tours
                </button>
            </div>
        </div>
    </section>

    <!-- Trip Planner Section -->
    <section id="plan" class="py-20 bg-gradient-to-b from-sky-50 to-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Craft Your Colorful Journey</h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Drag, drop, and design your perfect cultural itinerary with our vibrant planning tools
                </p>
            </div>
            
            <div class="flex flex-col lg:flex-row gap-8">
                <!-- Activities Panel -->
                <div class="lg:w-1/3 bg-white p-6 rounded-2xl shadow-lg">
                    <div class="flex justify-between items-center mb-6">
                        <h3 class="text-xl font-bold text-plum">Available Activities</h3>
                        <div class="flex space-x-2">
                            <button class="p-2 rounded-lg bg-plum/10 text-plum hover:bg-plum/20">
                                <i class="fas fa-filter"></i>
                            </button>
                            <button class="p-2 rounded-lg bg-plum/10 text-plum hover:bg-plum/20">
                                <i class="fas fa-search"></i>
                            </button>
                        </div>
                    </div>
                    
                    <div class="space-y-3">
                        <div class="activity-item flex items-center p-4 shadow-sm cursor-grab" draggable="true">
                            <div class="w-12 h-12 bg-amber-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-landmark text-amber-600 text-xl"></i>
                            </div>
                            <div class="flex-1">
                                <h4 class="font-medium text-gray-800">Heritage Walking Tour</h4>
                                <p class="text-sm text-gray-500">3 hours · Historic District</p>
                            </div>
                            <button class="text-papaya hover:text-peach">
                                <i class="fas fa-plus-circle text-xl"></i>
                            </button>
                        </div>
                        
                        <div class="activity-item flex items-center p-4 shadow-sm cursor-grab" draggable="true">
                            <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-mortar-pestle text-red-600 text-xl"></i>
                            </div>
                            <div class="flex-1">
                                <h4 class="font-medium text-gray-800">Spice Market Cooking</h4>
                                <p class="text-sm text-gray-500">4 hours · Local Market</p>
                            </div>
                            <button class="text-papaya hover:text-peach">
                                <i class="fas fa-plus-circle text-xl"></i>
                            </button>
                        </div>
                        
                        <div class="activity-item flex items-center p-4 shadow-sm cursor-grab" draggable="true">
                            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-paint-brush text-blue-600 text-xl"></i>
                            </div>
                            <div class="flex-1">
                                <h4 class="font-medium text-gray-800">Textile Art Workshop</h4>
                                <p class="text-sm text-gray-500">2.5 hours · Artist Studio</p>
                            </div>
                            <button class="text-papaya hover:text-peach">
                                <i class="fas fa-plus-circle text-xl"></i>
                            </button>
                        </div>
                        
                        <div class="activity-item flex items-center p-4 shadow-sm cursor-grab" draggable="true">
                            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mr-4">
                                <i class="fas fa-leaf text-green-600 text-xl"></i>
                            </div>
                            <div class="flex-1">
                                <h4 class="font-medium text-gray-800">Sunset Nature Walk</h4>
                                <p class="text-sm text-gray-500">1.5 hours · National Park</p>
                            </div>
                            <button cl
