<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Hens Farm - Your Source for Healthy Poultry</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- New Fonts: Lato for headings, Open Sans for body -->
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@700;900&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Open Sans', sans-serif; /* Body font */
            background-color: #fdfaf6; /* Off-white, warm background */
            color: #333d29; /* Dark forest green text */
        }
        h1, h2, h3 {
            font-family: 'Lato', sans-serif; /* Headings font */
        }
        .container {
            max-width: 1200px;
        }
        .card {
            background-color: #ffffff;
            border-radius: 1rem; /* Softly rounded corners */
            box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.05), 0 5px 10px -3px rgba(0, 0, 0, 0.02); /* Subtle shadow */
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            border: 1px solid #e6e6e6; /* Very light gray border */
        }
        .card:hover {
            transform: translateY(-8px); /* Gentle lift effect */
            box-shadow: 0 15px 30px -8px rgba(0, 0, 0, 0.08), 0 8px 15px -5px rgba(0, 0, 0, 0.04);
        }
        .btn-primary {
            background-color: #6b8e23; /* Olive Drab - earthy green */
            color: white;
            padding: 0.9rem 2.2rem;
            border-radius: 0.5rem; /* Slightly less rounded */
            transition: background-color 0.2s ease-in-out, transform 0.1s ease-in-out;
            font-weight: 700;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
            text-transform: uppercase;
            letter-spacing: 0.08em;
        }
        .btn-primary:hover {
            background-color: #5a761e; /* Darker olive on hover */
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }
        .btn-primary:active {
            transform: translateY(0);
            box-shadow: none;
        }
        .accent-color-1 {
            color: #6b8e23; /* Olive Drab */
        }
        .accent-color-2 {
            color: #daa520; /* Goldenrod - warm yellow accent */
        }
    </style>
</head>
<body class="flex flex-col min-h-screen">
    <!-- Header Section -->
    <header class="bg-white text-gray-800 p-6 shadow-md">
        <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-4xl font-extrabold mb-4 md:mb-0 accent-color-1">Happy Hens Farm</h1>
            <nav>
                <ul class="flex space-x-6 text-lg">
                    <li><a href="#about" class="hover:text-accent-color-1 transition duration-200">About Us</a></li>
                    <li><a href="#hens" class="hover:text-accent-color-1 transition duration-200">Our Hens</a></li>
                    <li><a href="#contact" class="hover:text-accent-color-1 transition duration-200">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-cover bg-center h-96 flex items-center justify-center text-white" style="background-image: url('https://placehold.co/1920x600/6b8e23/FFFFFF?text=Happy+Hens+Background');">
        <div class="absolute inset-0 bg-black opacity-40"></div> <!-- Overlay for text readability -->
        <div class="container mx-auto px-8 text-center relative z-10">
            <h2 class="text-6xl font-extrabold mb-4 leading-tight drop-shadow-lg">Healthy Hens for Your <span class="accent-color-2">Farm & Home!</span></h2>
            <p class="text-xl mb-8 leading-relaxed max-w-3xl mx-auto">
                Discover a variety of happy, healthy hens ready to join your flock.
                Quality poultry, raised with care, delivered to your door.
            </p>
            <a href="#hens" class="btn-primary text-xl font-bold inline-block">Explore Our Hens</a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-20 px-6 bg-fdfaf6">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold accent-color-1 mb-10">About Happy Hens Farm</h2>
            <p class="text-lg leading-relaxed max-w-4xl mx-auto text-gray-700">
                At Happy Hens Farm, we are deeply committed to raising healthy, happy chickens in a humane and natural environment.
                Our hens are fed high-quality, organic feed and enjoy ample space to roam freely, forage, and express their natural behaviors.
                We believe that well-cared-for hens produce the finest eggs and make the most joyful additions to any farm or backyard.
                Explore our selection and welcome new feathered friends into your life, raised with genuine care and passion!
            </p>
        </div>
    </section>

    <!-- Hens for Sale Section -->
    <section id="hens" class="py-20 bg-gray-50 px-6">
        <div class="container mx-auto">
            <h2 class="text-4xl font-bold accent-color-1 text-center mb-12">Our Lovely Hens</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <!-- Hen Card 1 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Lohmann+Brown" alt="Lohmann Brown Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Lohmann Brown</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Exceptional layers, consistent production of large brown eggs. Docile and easy to manage, ideal for beginners.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$25.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 2 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Rhode+Island+Red" alt="Rhode Island Red Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Rhode Island Red</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Robust dual-purpose breed for eggs and meat. Hardy and adaptable to various climates.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$30.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 3 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Plymouth+Rock" alt="Plymouth Rock Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Plymouth Rock</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Beloved heritage breed, friendly and calm. Consistent layers of large brown eggs.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$28.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 4 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Leghorn" alt="Leghorn Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Leghorn</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Highly efficient white egg layers. Energetic and active, thriving in free-ranging environments.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$22.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 5 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Orpington" alt="Orpington Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Orpington</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Large, fluffy, and incredibly friendly. Gentle nature makes them great for families.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$35.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 6 -->
                <div class="card p-8 flex flex-col items-center text-center">
                    <img src="https://placehold.co/400x250/6b8e23/FFFFFF?text=Silkie" alt="Silkie Hen" class="w-full h-48 object-cover mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-3">Silkie</h3>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Unique fluffy feathers, gentle temperament. Excellent broody hens for hatching eggs.
                    </p>
                    <span class="accent-color-1 text-xl font-bold mb-4">$40.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-6 bg-white">
        <div class="container mx-auto text-center">
            <h2 class="text-4xl font-bold accent-color-1 mb-10">Get in Touch!</h2>
            <p class="text-lg leading-relaxed max-w-3xl mx-auto mb-8 text-gray-700">
                Have questions about our hens, their care, or ready to make a purchase? We'd love to hear from you!
                Fill out the form below or contact us directly.
            </p>
            <div class="max-w-xl mx-auto bg-gray-50 p-10 rounded-xl shadow-md border border-gray-100">
                <form class="space-y-8">
                    <div>
                        <label for="name" class="block text-left text-gray-800 text-base font-medium mb-3">Your Name</label>
                        <input type="text" id="name" name="name" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-accent-color-1 transition duration-200" placeholder="John Doe">
                    </div>
                    <div>
                        <label for="email" class="block text-left text-gray-800 text-base font-medium mb-3">Your Email</label>
                        <input type="email" id="email" name="email" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-accent-color-1 transition duration-200" placeholder="john.doe@example.com">
                    </div>
                    <div>
                        <label for="message" class="block text-left text-gray-800 text-base font-medium mb-3">Your Message</label>
                        <textarea id="message" name="message" rows="6" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-accent-color-1 transition duration-200" placeholder="I'm interested in purchasing..."></textarea>
                    </div>
                    <button type="submit" class="btn-primary w-full text-lg font-semibold">Send Message</button>
                </form>
                <div class="mt-10 text-gray-800">
                    <p class="text-lg mb-2">Or contact us directly:</p>
                    <p class="font-bold accent-color-1 text-xl">Email: info@happyhensfarm.com</p>
                    <p class="font-bold accent-color-1 text-xl">Phone: +1 (123) 456-7890</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-gray-800 text-white py-10 mt-auto">
        <div class="container mx-auto text-center px-4">
            <p class="text-lg">&copy; 2025 Happy Hens Farm. All rights reserved.</p>
            <p class="mt-3 text-md">Proudly providing healthy poultry to happy homes since 2020.</p>
            <div class="flex justify-center space-x-8 mt-6">
                <a href="#" class="text-white hover:text-gray-300 transition duration-200 text-md">Privacy Policy</a>
                <a href="#" class="text-white hover:text-gray-300 transition duration-200 text-md">Terms of Service</a>
            </div>
        </div>
    </footer>
</body>
</html>
