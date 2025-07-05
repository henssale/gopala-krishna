<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-lang-key="pageTitle">Chicks Sold - Roosters & Hens for Sale</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f8f8;
        }
        /* Custom scrollbar for a cleaner look */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb {
            background: #888;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #555;
        }

        /* Modal styles */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        .modal-overlay.open {
            opacity: 1;
            visibility: visible;
        }
        .modal-content {
            background-color: white;
            padding: 2rem;
            border-radius: 1rem;
            max-width: 90%;
            max-height: 90%;
            overflow-y: auto;
            position: relative;
            transform: translateY(-20px);
            transition: transform 0.3s ease;
        }
        .modal-overlay.open .modal-content {
            transform: translateY(0);
        }
        .modal-close-button {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #333;
        }

        /* Hidden class for dynamic content */
        .hidden-section {
            display: none;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header -->
    <header class="bg-gradient-to-r from-yellow-600 to-orange-500 shadow-lg py-4 px-6 md:px-10 rounded-b-xl">
        <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
            <a href="#" class="text-white text-3xl font-bold tracking-tight mb-4 md:mb-0" data-lang-key="headerTitle">
                Chicks Sold
            </a>
            <nav>
                <ul class="flex flex-wrap justify-center space-x-4 md:space-x-8 text-lg font-medium">
                    <li><a href="#" id="homeNavBtn" class="text-white hover:text-yellow-200 transition duration-300 ease-in-out" data-lang-key="navHome">Home</a></li>
                    <li><a href="#" id="roostersNavBtn" class="text-white hover:text-yellow-200 transition duration-300 ease-in-out" data-lang-key="navRoosters">Roosters</a></li>
                    <li><a href="#" id="hensNavBtn" class="text-white hover:text-yellow-200 transition duration-300 ease-in-out" data-lang-key="navHens">Hens</a></li>
                    <li><a href="#" id="contactNavBtn" class="text-white hover:text-yellow-200 transition duration-300 ease-in-out" data-lang-key="navContact">Contact</a></li>
                    <li><a href="#" id="translatorNavBtn" class="text-white hover:text-yellow-200 transition duration-300 ease-in-out">Translator</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="relative bg-cover bg-center h-screen flex items-center justify-center text-center p-6" style="background-image: url('https://placehold.co/1920x1080/F59E0B/FFFFFF?text=Farm+Background');">
        <div class="absolute inset-0 bg-black opacity-50 rounded-xl"></div>
        <div class="relative z-10 text-white max-w-4xl mx-auto">
            <h1 class="text-5xl md:text-7xl font-extrabold leading-tight mb-6 drop-shadow-lg" data-lang-key="heroHeading">
                Quality Roosters & Hens
            </h1>
            <button id="viewBirdsBtn" class="bg-white text-orange-600 hover:bg-orange-100 transition duration-300 ease-in-out
                                      px-8 py-4 rounded-full text-xl font-semibold shadow-xl transform hover:scale-105" data-lang-key="heroButton">
                View Our Birds
            </button>
        </div>
    </section>

    <!-- Roosters Section (Original - will be hidden when new page is active) -->
    <section id="roosters" class="py-16 bg-gray-50 px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="roostersHeading">Our Majestic Roosters</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Rooster Card 1 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/DC2626/FFFFFF?text=Rooster+1" alt="Dominant Red Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-red-700" data-lang-key="rooster1Title">Red Ranger</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster1Desc">A proud and vigilant leader, excellent for flock protection.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹75</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="rooster1" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Rooster Card 2 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/6B7280/FFFFFF?text=Rooster+2" alt="Grey Speckled Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-gray-700" data-lang-key="rooster2Title">Silver Sentinel</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster2Desc">Calm demeanor, striking plumage, and good fertility.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹60</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="rooster2" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Rooster Card 3 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/10B981/FFFFFF?text=Rooster+3" alt="Green-feathered Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-green-700" data-lang-key="rooster3Title">Emerald King</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster3Desc">Rare and beautiful, with a gentle temperament.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹90</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="rooster3" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Hens Section (Original - will be hidden when new page is active) -->
    <section id="hens" class="py-16 bg-white px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="hensHeading">Our Productive Hens</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Hen Card 1 -->
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/FBBF24/FFFFFF?text=Hen+1" alt="Golden Layer Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-yellow-700" data-lang-key="hen1Title">Golden Layer</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen1Desc">Reliable egg producer, friendly and active.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹40</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="hen1" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Hen Card 2 -->
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/A78BFA/FFFFFF?text=Hen+2" alt="Purple Plumed Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-purple-700" data-lang-key="hen2Title">Violet Queen</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen2Desc">Unique coloration, good mothering instincts.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹55</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="hen2" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Hen Card 3 -->
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/3B82F6/FFFFFF?text=Hen+3" alt="Blue Egg Layer Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-blue-700" data-lang-key="hen3Title">Sky Blue Layer</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen3Desc">Known for laying beautiful blue eggs.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹50</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="hen3" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Chicks Section (New on Home Page) -->
    <section id="chicks" class="py-16 bg-gray-50 px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="chicksHeading">Our Adorable Chicks</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Chick Card 1 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/FFC0CB/FFFFFF?text=Chick+A" alt="Cute Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-pink-700" data-lang-key="chick1Title">Cute Chick</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="chick1Desc">Healthy and active chick, perfect for your flock.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹15</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="chick1" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Chick Card 2 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/ADD8E6/FFFFFF?text=Chick+B" alt="Fluffy Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-blue-700" data-lang-key="chick2Title">Fluffy Chick</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="chick2Desc">Soft and fluffy, growing fast.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹12</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="chick2" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Chick Card 3 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition duration-300 ease-in-out">
                    <img src="https://placehold.co/400x300/90EE90/FFFFFF?text=Chick+C" alt="Energetic Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-green-700" data-lang-key="chick3Title">Energetic Chick</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="chick3Desc">Vibrant and playful, ready for a new home.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-3xl font-bold text-orange-600">₹18</span>
                            <button class="show-more-btn bg-orange-500 text-white px-6 py-2 rounded-full hover:bg-orange-600 transition duration-300 ease-in-out shadow-md" data-bird-id="chick3" data-lang-key="showMoreButton">
                                Show More
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>


    <!-- New Roosters Page Section -->
    <section id="roostersPage" class="py-16 bg-gray-50 px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8 hidden-section">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="roostersPageHeading">All Roosters</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
                <!-- Replicate Rooster Cards or add more here -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/DC2626/FFFFFF?text=Rooster+1" alt="Dominant Red Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-red-700" data-lang-key="rooster1Title">Red Ranger</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster1Desc">A proud and vigilant leader, excellent for flock protection.</p>
                    </div>
                </div>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/6B7280/FFFFFF?text=Rooster+2" alt="Grey Speckled Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-gray-700" data-lang-key="rooster2Title">Silver Sentinel</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster2Desc">Calm demeanor, striking plumage, and good fertility.</p>
                    </div>
                </div>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/10B981/FFFFFF?text=Rooster+3" alt="Green-feathered Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-green-700" data-lang-key="rooster3Title">Emerald King</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster3Desc">Rare and beautiful, with a gentle temperament.</p>
                    </div>
                </div>
            </div>
            <h3 class="text-3xl font-bold mb-8 text-orange-600" data-lang-key="newRoosterPhotosHeading">New Rooster Photos</h3>
            <div id="newRoosterPhotosContainer" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- New rooster photos will be loaded here -->
                <img src="https://placehold.co/500x350/FF0000/FFFFFF?text=New+Rooster+A" alt="New Rooster Photo A" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/CC0000/FFFFFF?text=New+Rooster+B" alt="New Rooster Photo B" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/990000/FFFFFF?text=New+Rooster+C" alt="New Rooster Photo C" class="w-full h-auto rounded-lg shadow-md object-cover">
            </div>
        </div>
    </section>

    <!-- New Hens Page Section -->
    <section id="hensPage" class="py-16 bg-white px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8 hidden-section">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="hensPageHeading">All Hens</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
                <!-- Replicate Hen Cards or add more here -->
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/FBBF24/FFFFFF?text=Hen+1" alt="Golden Layer Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-yellow-700" data-lang-key="hen1Title">Golden Layer</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen1Desc">Reliable egg producer, friendly and active.</p>
                    </div>
                </div>
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/A78BFA/FFFFFF?text=Hen+2" alt="Purple Plumed Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-purple-700" data-lang-key="hen2Title">Violet Queen</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen2Desc">Unique coloration, good mothering instincts.</p>
                    </div>
                </div>
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/3B82F6/FFFFFF?text=Hen+3" alt="Blue Egg Layer Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-blue-700" data-lang-key="hen3Title">Sky Blue Layer</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen3Desc">Known for laying beautiful blue eggs.</p>
                    </div>
                </div>
            </div>
            <h3 class="text-3xl font-bold mb-8 text-orange-600" data-lang-key="newHenPhotosHeading">New Hen Photos</h3>
            <div id="newHenPhotosContainer" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- New hen photos will be loaded here -->
                <img src="https://placehold.co/500x350/FFD700/FFFFFF?text=New+Hen+A" alt="New Hen Photo A" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/DAA520/FFFFFF?text=New+Hen+B" alt="New Hen Photo B" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/B8860B/FFFFFF?text=New+Hen+C" alt="New Hen Photo C" class="w-full h-auto rounded-lg shadow-md object-cover">
            </div>
        </div>
    </section>

    <!-- New All Birds Page Section -->
    <section id="allBirdsPage" class="py-16 bg-gray-100 px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8 hidden-section">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold mb-12 text-orange-600" data-lang-key="allBirdsPageHeading">All Our Birds</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
                <!-- Replicate a mix of rooster and hen cards here -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/DC2626/FFFFFF?text=Rooster+1" alt="Dominant Red Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-red-700" data-lang-key="rooster1Title">Red Ranger</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster1Desc">A proud and vigilant leader, excellent for flock protection.</p>
                    </div>
                </div>
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/FBBF24/FFFFFF?text=Hen+1" alt="Golden Layer Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-yellow-700" data-lang-key="hen1Title">Golden Layer</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen1Desc">Reliable egg producer, friendly and active.</p>
                    </div>
                </div>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/6B7280/FFFFFF?text=Rooster+2" alt="Grey Speckled Rooster" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-gray-700" data-lang-key="rooster2Title">Silver Sentinel</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="rooster2Desc">Calm demeanor, striking plumage, and good fertility.</p>
                    </div>
                </div>
                <div class="bg-gray-50 rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/A78BFA/FFFFFF?text=Hen+2" alt="Purple Plumed Hen" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-purple-700" data-lang-key="hen2Title">Violet Queen</h3>
                        <p class="text-gray-600 mb-4" data-lang-key="hen2Desc">Unique coloration, good mothering instincts.</p>
                    </div>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-8 text-orange-600" data-lang-key="chicksPhotosHeading">Chicks Photos</h3>
            <div id="chicksPhotosContainer" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 mb-12">
                <!-- Placeholder for new chicks photos with prices -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/FFC0CB/FFFFFF?text=Chick+A" alt="Cute Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-pink-700">Cute Chick</h3>
                        <p class="text-gray-600 mb-4">Healthy and active chick, perfect for your flock.</p>
                        <span class="text-3xl font-bold text-orange-600">₹15</span>
                    </div>
                </div>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/ADD8E6/FFFFFF?text=Chick+B" alt="Fluffy Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-blue-700">Fluffy Chick</h3>
                        <p class="text-gray-600 mb-4">Soft and fluffy, growing fast.</p>
                        <span class="text-3xl font-bold text-orange-600">₹12</span>
                    </div>
                </div>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden">
                    <img src="https://placehold.co/400x300/90EE90/FFFFFF?text=Chick+C" alt="Energetic Chick" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-green-700">Energetic Chick</h3>
                        <p class="text-gray-600 mb-4">Vibrant and playful, ready for a new home.</p>
                        <span class="text-3xl font-bold text-orange-600">₹18</span>
                    </div>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-8 text-orange-600" data-lang-key="newBirdPhotosHeading">New Bird Photos</h3>
            <div id="newAllBirdPhotosContainer" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Placeholder for new bird photos -->
                <img src="https://placehold.co/500x350/FF6347/FFFFFF?text=New+Bird+1" alt="New Bird Photo 1" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/4682B4/FFFFFF?text=New+Bird+2" alt="New Bird Photo 2" class="w-full h-auto rounded-lg shadow-md object-cover">
                <img src="https://placehold.co/500x350/32CD32/FFFFFF?text=New+Bird+3" alt="New Bird Photo 3" class="w-full h-auto rounded-lg shadow-md object-cover">
            </div>
        </div>
    </section>


    <!-- Contact Us Section (now just a placeholder for the content that will be in the modal) -->
    <section id="contact" class="py-16 bg-gray-100 px-6 md:px-10 rounded-xl shadow-md m-4 md:m-8 hidden-section">
        <!-- This section is now hidden as its content will be displayed in a modal -->
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8 px-6 md:px-10 rounded-t-xl mt-4">
        <div class="container mx-auto text-center text-sm">
            <!-- Removed copyright and design credit -->
        </div>
    </footer>

    <!-- Photo Modal Structure -->
    <div id="photoModal" class="modal-overlay">
        <div class="modal-content">
            <button class="modal-close-button" onclick="closeModal('photoModal')">&times;</button>
            <h3 id="modalBirdName" class="text-3xl font-bold mb-6 text-orange-600 text-center"></h3>
            <div id="modalPhotoContainer" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Photos will be dynamically loaded here -->
            </div>
        </div>
    </div>

    <!-- Contact Details Modal Structure -->
    <div id="contactModal" class="modal-overlay">
        <div class="modal-content">
            <button class="modal-close-button" onclick="closeModal('contactModal')">&times;</button>
            <h3 class="text-3xl font-bold mb-6 text-orange-600 text-center" data-lang-key="contactModalHeading">Contact Details</h3>
            <div class="text-lg text-gray-700 space-y-4 text-center">
                <p data-lang-key="contactEmail">Email: <a href="mailto:info@poultrysale.com" class="text-orange-600 hover:underline">info@poultrysale.com</a></p>
                <p data-lang-key="contactPhone">Phone: <a href="tel:+919866653372" class="text-orange-600 hover:underline">9866653372</a></p>
                <p data-lang-key="contactAddress">Address: 4-160 P P MARRU, GUTLAPADU,BHIMAVARAM MANDAL WEST GODAVARI DISTRICT ANDHRA PRADESH 534239</p>
            </div>
        </div>
    </div>

    <!-- Translator Modal Structure (still exists but not directly opened by nav button) -->
    <div id="translatorModal" class="modal-overlay">
        <div class="modal-content">
            <button class="modal-close-button" onclick="closeModal('translatorModal')">&times;</button>
            <h3 class="text-3xl font-bold mb-6 text-orange-600 text-center" data-lang-key="translatorModalHeading">English to Telugu Translator</h3>
            <div class="space-y-4">
                <div class="flex justify-center gap-4 mb-6">
                    <!-- These buttons are now redundant if the nav button directly toggles -->
                    <button id="translateToTeluguBtn" class="bg-green-600 text-white px-6 py-3 rounded-full text-lg font-semibold hover:bg-green-700 transition duration-300 ease-in-out shadow-md">
                        Translate to Telugu
                    </button>
                    <button id="translateToEnglishBtn" class="bg-blue-600 text-white px-6 py-3 rounded-full text-lg font-semibold hover:bg-blue-700 transition duration-300 ease-in-out shadow-md">
                        Translate to English
                    </button>
                </div>
                <div>
                    <label for="englishInput" class="block text-left text-gray-700 text-sm font-medium mb-2" data-lang-key="englishInputLabel">English Text:</label>
                    <textarea id="englishInput" rows="4" placeholder="Enter English text here..."
                              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500"></textarea>
                </div>
                <button id="translateBtn" class="w-full bg-orange-600 text-white px-6 py-3 rounded-full text-lg font-semibold
                                             hover:bg-orange-700 transition duration-300 ease-in-out shadow-md" data-lang-key="translateButton">
                    Translate to Telugu
                </button>
                <div>
                    <label for="teluguOutput" class="block text-left text-gray-700 text-sm font-medium mb-2" data-lang-key="teluguOutputLabel">Telugu Translation:</label>
                    <textarea id="teluguOutput" rows="4" readonly
                              class="w-full px-4 py-3 border border-gray-300 rounded-lg bg-gray-50 text-gray-800 focus:outline-none"></textarea>
                </div>
            </div>
        </div>
    </div>


    <script>
        // Data for additional photos (using placeholder images)
        const birdPhotos = {
            rooster1: [
                'https://placehold.co/500x350/DC2626/FFFFFF?text=Rooster+1A',
                'https://placehold.co/500x350/DC2626/FFFFFF?text=Rooster+1B',
                'https://placehold.co/500x350/DC2626/FFFFFF?text=Rooster+1C'
            ],
            rooster2: [
                'https://placehold.co/500x350/6B7280/FFFFFF?text=Rooster+2A',
                'https://placehold.co/500x350/6B7280/FFFFFF?text=Rooster+2B',
                'https://placehold.co/500x350/6B7280/FFFFFF?text=Rooster+2C'
            ],
            rooster3: [
                'https://placehold.co/500x350/10B981/FFFFFF?text=Rooster+3A',
                'https://placehold.co/500x350/10B981/FFFFFF?text=Rooster+3B',
                'https://placehold.co/500x350/10B981/FFFFFF?text=Rooster+3C'
            ],
            hen1: [
                'https://placehold.co/500x350/FBBF24/FFFFFF?text=Hen+1A',
                'https://placehold.co/500x350/FBBF24/FFFFFF?text=Hen+1B',
                'https://placehold.co/500x350/FBBF24/FFFFFF?text=Hen+1C'
            ],
            hen2: [
                'https://placehold.co/500x350/A78BFA/FFFFFF?text=Hen+2A',
                'https://placehold.co/500x350/A78BFA/FFFFFF?text=Hen+2B',
                'https://placehold.co/500x350/A78BFA/FFFFFF?text=Hen+2C'
            ],
            hen3: [
                'https://placehold.co/500x350/3B82F6/FFFFFF?text=Hen+3A',
                'https://placehold.co/500x350/3B82F6/FFFFFF?text=Hen+3B',
                'https://placehold.co/500x350/3B82F6/FFFFFF?text=Hen+3C'
            ],
            chick1: [
                'https://placehold.co/500x350/FFC0CB/FFFFFF?text=Chick+1A',
                'https://placehold.co/500x350/FFC0CB/FFFFFF?text=Chick+1B',
                'https://placehold.co/500x350/FFC0CB/FFFFFF?text=Chick+1C'
            ],
            chick2: [
                'https://placehold.co/500x350/ADD8E6/FFFFFF?text=Chick+2A',
                'https://placehold.co/500x350/ADD8E6/FFFFFF?text=Chick+2B',
                'https://placehold.co/500x350/ADD8E6/FFFFFF?text=Chick+2C'
            ],
            chick3: [
                'https://placehold.co/500x350/90EE90/FFFFFF?text=Chick+3A',
                'https://placehold.co/500x350/90EE90/FFFFFF?text=Chick+3B',
                'https://placehold.co/500x350/90EE90/FFFFFF?text=Chick+3C'
            ]
        };

        // Full website translation dictionary
        const translations = {
            en: {
                pageTitle: "Chicks Sold - Roosters & Hens for Sale",
                headerTitle: "Chicks Sold",
                navHome: "Home",
                navRoosters: "Roosters",
                navHens: "Hens",
                navContact: "Contact",
                // navTranslator will be handled dynamically
                heroHeading: "Quality Roosters & Hens",
                heroButton: "View Our Birds",
                roostersHeading: "Our Majestic Roosters",
                rooster1Title: "Red Ranger",
                rooster1Desc: "A proud and vigilant leader, excellent for flock protection.",
                rooster2Title: "Silver Sentinel",
                rooster2Desc: "Calm demeanor, striking plumage, and good fertility.",
                rooster3Title: "Emerald King",
                rooster3Desc: "Rare and beautiful, with a gentle temperament.",
                hensHeading: "Our Productive Hens",
                hen1Title: "Golden Layer",
                hen1Desc: "Reliable egg producer, friendly and active.",
                hen2Title: "Violet Queen",
                hen2Desc: "Unique coloration, good mothering instincts.",
                hen3Title: "Sky Blue Layer",
                hen3Desc: "Known for laying beautiful blue eggs.",
                chicksHeading: "Our Adorable Chicks", // New translation key for home page chicks
                chick1Title: "Cute Chick", // New translation key
                chick1Desc: "Healthy and active chick, perfect for your flock.", // New translation key
                chick2Title: "Fluffy Chick", // New translation key
                chick2Desc: "Soft and fluffy, growing fast.", // New translation key
                chick3Title: "Energetic Chick", // New translation key
                chick3Desc: "Vibrant and playful, ready for a new home.", // New translation key
                showMoreButton: "Show More",
                contactModalHeading: "Contact Details",
                contactEmail: "Email: info@poultrysale.com",
                contactPhone: "Phone: 9866653372",
                contactAddress: "Address: 4-160 P P MARRU, GUTLAPADU,BHIMAVARAM MANDAL WEST GODAVARI DISTRICT ANDHRA PRADESH 534239",
                translatorModalHeading: "English to Telugu Translator",
                englishInputLabel: "English Text:",
                teluguOutputLabel: "Telugu Translation:",
                translateButton: "Translate to Telugu",
                roostersPageHeading: "All Roosters",
                hensPageHeading: "All Hens",
                newRoosterPhotosHeading: "New Rooster Photos",
                newHenPhotosHeading: "New Hen Photos",
                allBirdsPageHeading: "All Our Birds",
                newBirdPhotosHeading: "New Bird Photos",
                chicksPhotosHeading: "Chicks Photos" // Existing translation key for all birds page
            },
            te: {
                pageTitle: "కోడిపిల్లలు అమ్మబడును - కోడిపుంజులు & కోడిపిల్లలు అమ్మకం", // Kōḍipillalu am'mabaḍunu - Kōḍipunjulu & kōḍipillalu am'makaṁ
                headerTitle: "కోడిపిల్లలు అమ్మబడును", // Kōḍipillalu am'mabaḍunu
                navHome: "హోమ్", // Hōm
                navRoosters: "కోడిపుంజులు", // Kōḍipunjulu
                navHens: "కోడిపిల్లలు", // Kōḍipillalu
                navContact: "సంప్రదించండి", // Sampradin̄caṇḍi
                // navTranslator will be handled dynamically
                heroHeading: "నాణ్యమైన కోడిపుంజులు & కోడిపిల్లలు", // Nāṇyamaina kōḍipunjulu & kōḍipillalu
                heroButton: "మా పక్షులను చూడండి", // Mā pakṣulanu cūḍaṇḍi
                roostersHeading: "మా గంభీరమైన కోడిపుంజులు", // Mā gambhīramaina kōḍipunjulu
                rooster1Title: "రెడ్ రేంజర్", // Reḍ rēnjar
                rooster1Desc: "గర్వించదగిన మరియు అప్రమత్తమైన నాయకుడు, మంద రక్షణకు అద్భుతమైనది.", // Garvin̄cadagina mariyu apramattamaina nāyakuḍu, manda rakṣaṇaku adbhutamainadi.
                rooster2Title: "సిల్వర్ సెంటినెల్", // Silvar senṭinel
                rooster2Desc: "శాంత స్వభావం, ఆకర్షణీయమైన ఈకలు మరియు మంచి సంతానోత్పత్తి.", // Śānta svabhāvaṁ, ākarṣaṇīyamaina īkalu mariyu man̄ci santānōtpatti.
                rooster3Title: "ఎమరాల్డ్ కింగ్", // Emarālḍ kiṅg
                rooster3Desc: "అరుదైన మరియు అందమైన, సున్నితమైన స్వభావంతో.", // Arudaina mariyu andamaina, sunnitamaina svabhāvatō.
                hensHeading: "కోడి పెట్టలు", // Updated translation
                hen1Title: "గోల్డెన్ లేయర్", // Gōlḍen lēyar
                hen1Desc: "నమ్మకమైన గుడ్డు ఉత్పత్తిదారు, స్నేహపూర్వక మరియు చురుకైన.", // Nammakaina guḍḍu utpattidāru, snēhapūrvaka mariyu curukaina.
                hen2Title: "వైలెట్ క్వీన్", // Vailēṭ kvīn
                hen2Desc: "ప్రత్యేకమైన రంగు, మంచి తల్లిదండ్రుల లక్షణాలు.", // Prat'yēkamaina raṅgu, man̄ci tallidaṇḍrula lakṣaṇālu.
                hen3Title: "స్కై బ్లూ లేయర్", // Skai blū lēyar
                hen3Desc: "అందమైన నీలి గుడ్లు పెట్టడానికి ప్రసిద్ధి చెందినది.", // Andamaina nīli guḍlu peṭṭaḍāniki prasid'dhi cēndinadi.
                chicksHeading: "మా ముద్దుల కోడిపిల్లలు", // New translation key for home page chicks
                chick1Title: "ముద్దుల కోడిపిల్ల", // New translation key
                chick1Desc: "ఆరోగ్యకరమైన మరియు చురుకైన కోడిపిల్ల, మీ మందకు సరైనది.", // New translation key
                chick2Title: "మెత్తటి కోడిపిల్ల", // New translation key
                chick2Desc: "మెత్తగా మరియు మెత్తగా, వేగంగా పెరుగుతోంది.", // New translation key
                chick3Title: "శక్తివంతమైన కోడిపిల్ల", // New translation key
                chick3Desc: "సజీవంగా మరియు ఉల్లాసంగా, కొత్త ఇంటికి సిద్ధంగా ఉంది.", // New translation key
                showMoreButton: "మరిన్ని చూడండి", // Marinni cūḍaṇḍi
                contactModalHeading: "సంప్రదింపు వివరాలు", // Sampradimpu vivarālu
                contactEmail: "ఇమెయిల్: info@poultrysale.com", // Imeyil: info@poultrysale.com
                contactPhone: "ఫోన్: 9866653372", // Phōn: 9866653372
                contactAddress: "చిరునామా: 4-160 పి పి మార్రు, గుట్లపాడు, భీమవరం మండలం పశ్చిమ గోదావరి జిల్లా ఆంధ్రప్రదేశ్ 534239", // Cirunāmā: 4-160 Pi Pi Mārru, Guṭlapāḍu, Bhīmavaraṁ Maṇḍalaṁ Paścima Gōdāvari Jillā Āndhrapradēś 534239
                translatorModalHeading: "ఇంగ్లీష్ నుండి తెలుగు అనువాదకుడు", // Iṅglīṣ nuṇḍi telugu anuvādakuḍu
                englishInputLabel: "ఇంగ్లీష్ వచనం:", // Iṅglīṣ vacanaṁ:
                teluguOutputLabel: "తెలుగు అనువాదం:", // Telugu anuvādaṁ:
                translateButton: "తెలుగులోకి అనువదించు", // Telugulōki anuvadin̄cu
                roostersPageHeading: "అన్ని కోడిపుంజులు", // Anni kōḍipunjulu
                hensPageHeading: "అన్ని కోడిపిల్లలు", // Anni kōḍipillalu
                newRoosterPhotosHeading: "కొత్త కోడిపుంజుల ఫోటోలు", // Kotta kōḍipunjula phoṭōlu
                newHenPhotosHeading: "కొత్త కోడిపిల్లల ఫోటోలు", // Kotta kōḍipillala phoṭōlu
                allBirdsPageHeading: "మా అన్ని పక్షులు", // Mā anni pakṣulu
                newBirdPhotosHeading: "కొత్త పక్షుల ఫోటోలు", // Kotta pakṣula phoṭōlu
                chicksPhotosHeading: "కోడిపిల్లల ఫోటోలు" // Existing translation key for all birds page
            }
        };

        let currentLanguage = 'en'; // Default language

        // Function to set the language of the entire page
        function setLanguage(lang) {
            currentLanguage = lang;
            document.querySelectorAll('[data-lang-key]').forEach(element => {
                const key = element.getAttribute('data-lang-key');
                if (translations[lang] && translations[lang][key]) {
                    // Special handling for the page title
                    if (key === 'pageTitle') {
                        document.title = translations[lang][key];
                    } else if (key === 'contactEmail' || key === 'contactPhone' || key === 'contactAddress') {
                        // For contact details, only update the text content, not the href
                        const anchorTag = element.querySelector('a');
                        if (anchorTag) {
                            const originalText = anchorTag.textContent;
                            const translatedPrefix = translations[lang][key].split(':')[0];
                            const value = originalText.split(':').length > 1 ? originalText.split(':')[1].trim() : originalText.trim(); // Get the actual value after the prefix
                            // Reconstruct the innerHTML to keep the anchor tag intact
                            element.innerHTML = `${translatedPrefix}: <a href="${anchorTag.href}" class="text-orange-600 hover:underline">${value}</a>`;
                        } else {
                            // If no anchor tag, just set the text content
                            element.textContent = translations[lang][key];
                        }
                    }
                    else {
                        element.textContent = translations[lang][key];
                    }
                }
            });

            // Handle the Translator button text dynamically
            if (translatorNavBtn) {
                if (lang === 'en') {
                    translatorNavBtn.textContent = "తెలుగు"; // Telugu text for "Telugu"
                } else {
                    translatorNavBtn.textContent = "English"; // English text for "English"
                }
            }

            // Update placeholder for English input if needed
            if (lang === 'en') {
                englishInput.placeholder = "Enter English text here...";
            } else {
                englishInput.placeholder = "ఇక్కడ ఇంగ్లీష్ వచనాన్ని నమోదు చేయండి...";
            }
        }

        // Get elements
        const homeNavBtn = document.getElementById('homeNavBtn');
        const roostersNavBtn = document.getElementById('roostersNavBtn');
        const hensNavBtn = document.getElementById('hensNavBtn');
        const contactNavBtn = document.getElementById('contactNavBtn');
        const translatorNavBtn = document.getElementById('translatorNavBtn');
        const viewBirdsBtn = document.getElementById('viewBirdsBtn'); // Get the new button reference

        const heroSection = document.getElementById('home');
        const roostersSection = document.getElementById('roosters');
        const hensSection = document.getElementById('hens');
        const chicksSection = document.getElementById('chicks'); // New chicks section on home page
        const contactSection = document.getElementById('contact'); // This is the hidden section, not the modal

        const roostersPage = document.getElementById('roostersPage');
        const hensPage = document.getElementById('hensPage');
        const allBirdsPage = document.getElementById('allBirdsPage'); // Get the new all birds page reference

        const photoModal = document.getElementById('photoModal');
        const modalPhotoContainer = document.getElementById('modalPhotoContainer');
        const modalBirdName = document.getElementById('modalBirdName');
        const showMoreButtons = document.querySelectorAll('.show-more-btn');

        const contactModal = document.getElementById('contactModal');

        const translatorModal = document.getElementById('translatorModal'); // Still need this to access its internal elements
        const englishInput = document.getElementById('englishInput');
        const teluguOutput = document.getElementById('teluguOutput');
        const translateBtn = document.getElementById('translateBtn');


        // Simple translation dictionary for individual word translation (for demonstration purposes)
        const wordTranslationDictionary = {
            "hello": "నమస్కారం",
            "hi": "నమస్కారం",
            "rooster": "పుంజు",
            "hen": "కోడి",
            "chicks": "కోడిపిల్లలు",
            "sold": "అమ్మబడును",
            "contact": "సంప్రదించండి",
            "quality": "నాణ్యత",
            "birds": "పక్షులు",
            "farm": "వ్యవసాయ క్షేత్రం",
            "chicken": "కోడి",
            "good morning": "శుభోదయం",
            "how are you": "మీరు ఎలా ఉన్నారు?",
            "thank you": "ధన్యవాదాలు",
            "buy": "కొనుగోలు చేయండి",
            "sale": "అమ్మకం",
            "welcome": "సుస్వాగతం",
            "home": "ఇల్లు",
            "price": "ధర" // New translation for price
        };

        // Function to show a specific page/section and hide others
        function showPage(pageId) {
            // Hide all main content sections
            heroSection.classList.add('hidden-section');
            roostersSection.classList.add('hidden-section');
            hensSection.classList.add('hidden-section');
            chicksSection.classList.add('hidden-section'); // Hide new chicks section
            roostersPage.classList.add('hidden-section');
            hensPage.classList.add('hidden-section');
            allBirdsPage.classList.add('hidden-section'); // Hide the new all birds page too
            contactSection.classList.add('hidden-section'); // Ensure this is also hidden if it was ever visible

            // Show the requested section(s)
            if (pageId === 'home') {
                heroSection.classList.remove('hidden-section');
                roostersSection.classList.remove('hidden-section');
                hensSection.classList.remove('hidden-section');
                chicksSection.classList.remove('hidden-section'); // Show chicks section on home
            } else if (pageId === 'roostersPage') {
                roostersPage.classList.remove('hidden-section');
            } else if (pageId === 'hensPage') {
                hensPage.classList.remove('hidden-section');
            } else if (pageId === 'allBirdsPage') { // New case for all birds page
                allBirdsPage.classList.remove('hidden-section');
            }
            // Modals are handled separately by openModal/closeModal
        }


        // Function to open a specific modal
        function openModal(modalId, birdId = null, birdName = null) {
            const modal = document.getElementById(modalId);
            if (modalId === 'photoModal' && birdId && birdName) {
                // For photo modal, birdName might be in Telugu, need to adjust
                const displayBirdName = currentLanguage === 'te' ? ` ${birdName}` : ` of ${birdName}`;
                modalBirdName.textContent = `More Photos${displayBirdName}`; // Keep "More Photos" in English for simplicity or add to dictionary
                modalPhotoContainer.innerHTML = ''; // Clear previous photos

                const photos = birdPhotos[birdId];
                if (photos) {
                    photos.forEach(src => {
                        const img = document.createElement('img');
                        img.src = src;
                        img.alt = birdName;
                        img.classList.add('w-full', 'h-auto', 'rounded-lg', 'shadow-md', 'object-cover');
                        modalPhotoContainer.appendChild(img);
                    });
                } else {
                    modalPhotoContainer.innerHTML = '<p class="text-center text-gray-600 col-span-full">No additional photos available.</p>';
                }
            }
            modal.classList.add('open');
        }

        // Function to close a specific modal
        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.classList.remove('open');
        }

        // Add event listeners to all "Show More" buttons
        showMoreButtons.forEach(button => {
            button.addEventListener('click', (event) => {
                const birdId = event.target.dataset.birdId;
                // Get the bird's name from the h3 element within the same card
                const birdName = event.target.closest('.bg-white, .bg-gray-50').querySelector('h3').textContent;
                openModal('photoModal', birdId, birdName);
            });
        });

        // Add event listener for the "Home" navigation button
        homeNavBtn.addEventListener('click', (event) => {
            event.preventDefault();
            showPage('home');
        });

        // Add event listener for the "Roosters" navigation button
        roostersNavBtn.addEventListener('click', (event) => {
            event.preventDefault();
            showPage('roostersPage');
        });

        // Add event listener for the "Hens" navigation button
        hensNavBtn.addEventListener('click', (event) => {
            event.preventDefault();
            showPage('hensPage');
        });

        // Add event listener for the "Contact" navigation button
        contactNavBtn.addEventListener('click', (event) => {
            event.preventDefault(); // Prevent default anchor behavior (scrolling)
            openModal('contactModal');
        });

        // Modified event listener for the "Translator" navigation button
        translatorNavBtn.addEventListener('click', (event) => {
            event.preventDefault(); // Prevent default anchor behavior (scrolling)
            if (currentLanguage === 'en') {
                setLanguage('te');
            } else {
                setLanguage('en');
            }
        });

        // New event listener for "View Our Birds" button
        if (viewBirdsBtn) {
            viewBirdsBtn.addEventListener('click', (event) => {
                event.preventDefault();
                showPage('allBirdsPage'); // Show the new All Birds page
            });
        }


        // Translator functionality (for individual word translation, still accessible if modal is opened by other means)
        translateBtn.addEventListener('click', () => {
            const englishText = englishInput.value.toLowerCase().trim();
            let translatedText = "";

            // Simple word-by-word translation
            const words = englishText.split(/\s+/); // Split by one or more spaces
            if (words.length > 0) {
                translatedText = words.map(word => {
                    // Remove punctuation for better matching
                    const cleanWord = word.replace(/[.,!?;:]/g, '');
                    return wordTranslationDictionary[cleanWord] || cleanWord; // Translate if found, otherwise keep original
                }).join(' ');
            }

            teluguOutput.value = translatedText || "Translation not available for this text.";
        });

        // Close modals when clicking outside their content
        photoModal.addEventListener('click', (event) => {
            if (event.target === photoModal) {
                closeModal('photoModal');
            }
        });

        contactModal.addEventListener('click', (event) => {
            if (event.target === contactModal) {
                closeModal('contactModal');
            }
        });

        // The translator modal itself is no longer directly opened by the nav button,
        // but if it were opened by other means, these would still close it.
        translatorModal.addEventListener('click', (event) => {
            if (event.target === translatorModal) {
                closeModal('translatorModal');
            }
        });

        // Initialize language and show home page on page load
        document.addEventListener('DOMContentLoaded', () => {
            setLanguage('en'); // Set default language to English on load
            showPage('home'); // Show the home page content by default
        });
    </script>

</body>
</html>
