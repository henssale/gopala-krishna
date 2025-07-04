<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Hens Farm - Your Source for Healthy Poultry</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- New Fonts: Merriweather for headings, Open Sans for body -->
    <link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@700;900&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Open Sans', sans-serif; /* Body font */
            background-color: #fcfceb; /* Very light creamy yellow */
            color: #3f3f46; /* Zinc 700 - a warm dark gray */
        }
        h1, h2, h3 {
            font-family: 'Merriweather', serif; /* Headings font */
        }
        .container {
            max-width: 1200px;
        }
        .card {
            background-color: #ffffff;
            border-radius: 1.5rem; /* Even more rounded corners */
            box-shadow: 0 20px 30px -10px rgba(0, 0, 0, 0.1), 0 10px 15px -8px rgba(0, 0, 0, 0.05); /* Deeper shadow */
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            border: 2px solid #fde68a; /* Warm yellow border */
        }
        .card:hover {
            transform: translateY(-12px); /* Stronger lift */
            box-shadow: 0 30px 50px -15px rgba(0, 0, 0, 0.2), 0 20px 20px -10px rgba(0, 0, 0, 0.1);
        }
        .btn-primary {
            background-color: #d97706; /* Amber 700 - a rich orange */
            color: white;
            padding: 1.1rem 2.8rem; /* Larger padding */
            border-radius: 0.75rem; /* Rounded-xl */
            transition: background-color 0.2s ease-in-out, transform 0.1s ease-in-out, box-shadow 0.2s ease-in-out;
            font-weight: 700; /* Bold */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            text-transform: uppercase; /* Uppercase text */
            letter-spacing: 0.05em; /* Slight letter spacing */
        }
        .btn-primary:hover {
            background-color: #b45309; /* Darker amber on hover */
            transform: translateY(-4px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
        }
        .btn-primary:active {
            transform: translateY(0);
            box-shadow: none;
        }
        .accent-color-1 {
            color: #d97706; /* Amber 700 */
        }
        .accent-color-2 {
            color: #16a34a; /* Green 600 */
        }
    </style>
</head>
<body class="flex flex-col min-h-screen">
    <!-- Header Section -->
    <header class="bg-amber-800 text-white p-8 shadow-xl rounded-b-3xl">
        <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-6xl font-extrabold mb-4 md:mb-0">Happy Hens Farm</h1>
            <nav>
                <ul class="flex space-x-10 text-2xl">
                    <li><a href="#about" class="hover:underline hover:text-amber-200 transition duration-200">About Us</a></li>
                    <li><a href="#hens" class="hover:underline hover:text-amber-200 transition duration-200">Our Hens</a></li>
                    <li><a href="#contact" class="hover:underline hover:text-amber-200 transition duration-200">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="bg-gradient-to-br from-amber-600 to-yellow-500 text-white py-32 text-center rounded-3xl mx-8 mt-12 shadow-2xl">
        <div class="container mx-auto px-10">
            <h2 class="text-8xl font-extrabold mb-10 leading-tight drop-shadow-lg">Healthy Hens for Your <span class="accent-color-2">Farm & Home!</span></h2>
            <p class="text-2xl mb-14 leading-relaxed max-w-5xl mx-auto">
                Discover a variety of happy, healthy hens ready to join your flock.
                Whether you're looking for prolific layers, hearty broilers, or just friendly companions, we have the perfect poultry for you.
            </p>
            <a href="#hens" class="btn-primary text-3xl font-bold inline-block hover:shadow-xl">Explore Our Hens</a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-28 px-6">
        <div class="container mx-auto text-center">
            <h2 class="text-6xl font-bold text-amber-800 mb-16">About Happy Hens Farm</h2>
            <p class="text-xl leading-relaxed max-w-5xl mx-auto text-gray-700">
                At Happy Hens Farm, we are deeply committed to raising healthy, happy chickens in a humane and natural environment.
                Our hens are fed high-quality, organic feed and enjoy ample space to roam freely, forage, and express their natural behaviors.
                We believe that well-cared-for hens produce the finest eggs and make the most joyful additions to any farm or backyard.
                Explore our selection and welcome new feathered friends into your life, raised with genuine care and passion!
            </p>
        </div>
    </section>

    <!-- Hens for Sale Section -->
    <section id="hens" class="py-28 bg-yellow-50 px-6">
        <div class="container mx-auto">
            <h2 class="text-6xl font-bold text-amber-800 text-center mb-20">Our Lovely Hens</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-16">
                <!-- Hen Card 1 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Lohmann+Brown" alt="Lohmann Brown Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Lohmann Brown</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        Renowned for being exceptional layers, consistently producing large, rich brown eggs. They are very docile and easy to manage, making them an ideal choice for first-time chicken keepers.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$25.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 2 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Rhode+Island+Red" alt="Rhode Island Red Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Rhode Island Red</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        A robust and versatile dual-purpose breed, highly valued for both their prolific egg production and quality meat. They are incredibly hardy and adapt well to various climates.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$30.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 3 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Plymouth+Rock" alt="Plymouth Rock Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Plymouth Rock</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        A beloved heritage breed, known for their friendly disposition and calm temperament. They are consistent layers of large, beautiful brown eggs, perfect for any flock.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$28.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 4 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Leghorn" alt="Leghorn Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Leghorn</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        Highly efficient and prolific white egg layers. These energetic and active birds thrive in free-ranging environments, making them a great choice for open spaces.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$22.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 5 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Orpington" alt="Orpington Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Orpington</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        Large, fluffy, and incredibly friendly, Orpingtons are known for their gentle nature. They are excellent for families and provide a calming presence in any backyard flock.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$35.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>

                <!-- Hen Card 6 -->
                <div class="card p-12 flex flex-col items-center text-center">
                    <img src="https://placehold.co/450x350/d97706/FFFFFF?text=Silkie" alt="Silkie Hen" class="w-full h-72 object-cover mb-12 rounded-2xl shadow-lg">
                    <h3 class="text-4xl font-semibold text-gray-900 mb-6">Silkie</h3>
                    <p class="text-gray-700 mb-10 leading-relaxed">
                        Distinctive for their unique fluffy feathers and exceptionally gentle temperament. Silkies are often used as excellent broody hens, making them perfect for hatching eggs.
                    </p>
                    <span class="accent-color-1 text-4xl font-bold mb-10">$40.00</span>
                    <button class="btn-primary">Inquire Now</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-28 px-6 bg-white">
        <div class="container mx-auto text-center">
            <h2 class="text-6xl font-bold text-amber-800 mb-16">Get in Touch!</h2>
            <p class="text-xl leading-relaxed max-w-4xl mx-auto mb-14 text-gray-700">
                Have questions about our hens, their care, or ready to make a purchase? We'd love to hear from you!
                Fill out the form below or contact us directly.
            </p>
            <div class="max-w-2xl mx-auto bg-yellow-50 p-14 rounded-3xl shadow-2xl border border-yellow-100">
                <form class="space-y-12">
                    <div>
                        <label for="name" class="block text-left text-gray-800 text-xl font-medium mb-5">Your Name</label>
                        <input type="text" id="name" name="name" class="w-full p-6 border-2 border-yellow-300 rounded-lg focus:outline-none focus:ring-4 focus:ring-amber-500 transition duration-200 text-xl" placeholder="John Doe">
                    </div>
                    <div>
                        <label for="email" class="block text-left text-gray-800 text-xl font-medium mb-5">Your Email</label>
                        <input type="email" id="email" name="email" class="w-full p-6 border-2 border-yellow-300 rounded-lg focus:outline-none focus:ring-4 focus:ring-amber-500 transition duration-200 text-xl" placeholder="john.doe@example.com">
                    </div>
                    <div>
                        <label for="message" class="block text-left text-gray-800 text-xl font-medium mb-5">Your Message</label>
                        <textarea id="message" name="message" rows="8" class="w-full p-6 border-2 border-yellow-300 rounded-lg focus:outline-none focus:ring-4 focus:ring-amber-500 transition duration-200 text-xl" placeholder="I'm interested in purchasing..."></textarea>
                    </div>
                    <button type="submit" class="btn-primary w-full text-3xl font-bold">Send Message</button>
                </form>
                <div class="mt-16 text-gray-800">
                    <p class="text-2xl mb-6">Or contact us directly:</p>
                    <p class="font-bold accent-color-1 text-3xl">Email: info@happyhensfarm.com</p>
                    <p class="font-bold accent-color-1 text-3xl">Phone: +1 (123) 456-7890</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-amber-900 text-white py-14 mt-auto rounded-t-3xl">
        <div class="container mx-auto text-center px-6">
            <p class="text-xl">&copy; 2025 Happy Hens Farm. All rights reserved.</p>
            <p class="mt-5 text-lg">Proudly providing healthy poultry to happy homes since 2020.</p>
            <div class="flex justify-center space-x-10 mt-10">
                <a href="#" class="text-white hover:text-amber-200 transition duration-200 text-lg">Privacy Policy</a>
                <a href="#" class="text-white hover:text-amber-200 transition duration-200 text-lg">Terms of Service</a>
            </div>
        </div>
    </footer>
</body>
</html>
