<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HealthBridge Connect</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/@tailwindcss/browser@4"></script>
    <style>
        /* Custom CSS for the slider and other elements, if needed */
        .carousel {
            position: relative;
            width: 100%;
            overflow: hidden;
        }

        .carousel-content {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .carousel-item {
            flex: 0 0 100%;
            min-width: 100%;
        }

        .carousel-prev, .carousel-next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(255, 255, 255, 0.5);
            color: #000;
            border: none;
            padding: 10px;
            cursor: pointer;
            font-size: 20px;
            border-radius: 50%;
            transition: background-color 0.3s ease;
        }

        .carousel-prev:hover, .carousel-next:hover {
            background-color: rgba(255, 255, 255, 0.8);
        }

        .carousel-prev {
            left: 10px;
        }

        .carousel-next {
            right: 10px;
        }

        .fade {
          animation-name: fade;
          animation-duration: 1.5s;
          animation-timing-function: ease-in-out;
        }

        @keyframes fade {
          from {opacity: .4}
          to {opacity: 1}
        }

    </style>
</head>
<body class="bg-gray-950 font-inter">
    <div id="root">
        <header class="bg-gray-900 py-4 border-b border-gray-800">
            <div class="container mx-auto px-4 flex justify-between items-center">
                <a href="#" class="text-2xl font-bold text-white">
                    <i class="fas fa-heart text-red-500 mr-2"></i>
                    HealthBridge Connect
                </a>
                <nav class="hidden md:block">
                    <ul class="flex space-x-6">
                        <li><a href="#" data-page="home" class="text-gray-300 hover:text-white transition-colors">Home</a></li>
                        <li><a href="#1st" data-page="about" class="text-gray-300 hover:text-white transition-colors">About Us</a></li>
                        <li><a href="#solutions-page" data-page="solutions" class="text-gray-300 hover:text-white transition-colors">Solutions</a></li>
                        <li><a href="#get-involved-page" data-page="get-involved" class="text-gray-300 hover:text-white transition-colors">Get Involved</a></li>
                        <li><a href="#resources-page" data-page="resources" class="text-gray-300 hover:text-white transition-colors">Resources</a></li>
                        <li><a href="#contactus" data-page="contact" class="text-gray-300 hover:text-white transition-colors">Contact</a></li>
                    </ul>
                </nav>
                <div class="md:hidden">
                    <button id="mobile-menu-button" class="text-gray-300 hover:text-white">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                        </svg>
                    </button>
                    <div id="mobile-menu" class="hidden absolute top-16 right-0 bg-gray-900 border border-gray-800 shadow-lg rounded-md py-2 px-4 space-y-2">
                        <a href="#" data-page="home" class="block text-gray-300 hover:text-white transition-colors">Home</a>
                        <a href="#" data-page="about" class="block text-gray-300 hover:text-white transition-colors">About Us</a>
                        <a href="#" data-page="solutions" class="block text-gray-300 hover:text-white transition-colors">Solutions</a>
                        <a href="#" data-page="get-involved" class="block text-gray-300 hover:text-white transition-colors">Get Involved</a>
                        <a href="#" data-page="resources" class="block text-gray-300 hover:text-white transition-colors">Resources</a>
                        <a href="#" data-page="contact" class="block text-gray-300 hover:text-white transition-colors">Contact</a>
                    </div>
                </div>
            </div>
        </header>

        <main id="content">
            <section id="home-page" class="page active">
                <section class="text-center py-20 bg-gradient-to-br from-gray-900 via-purple-900 to-black">
                    <div class="container mx-auto px-4">
                        <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-purple-400 mb-4 animate-fade">
                            Bridging the Healthcare Gap
                        </h1>
                        <p class="text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto mb-8 animate-fade" style="animation-delay: 0.3s;">
                            Connecting underserved communities to quality healthcare through innovative solutions.
                        </p>
                        <a href="#contactus" data-page="about" class="bg-gradient-to-r from-blue-500 to-purple-500 text-white px-8 py-3 rounded-full hover:from-blue-600 hover:to-purple-600 transition-all duration-300 animate-fade" style="animation-delay: 0.6s;">
                            Learn More About Us
                        </a>
                    </div>
                </section>

                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                            <div class="shadow-md border-0 bg-white/5 backdrop-blur-md">
                                <div class="flex flex-row items-center justify-between space-y-0 pb-2">
                                    <div class="text-sm font-medium text-gray-300">People Served</div>
                                    <i class="fas fa-users text-blue-500 w-6 h-6"></i>
                                </div>
                                <div class="text-2xl font-bold text-white">50,000+</div>
                            </div>
                            <div class="shadow-md border-0 bg-white/5 backdrop-blur-md">
                                <div class="flex flex-row items-center justify-between space-y-0 pb-2">
                                    <div class="text-sm font-medium text-gray-300">Mobile Clinics</div>
                                    <i class="fas fa-map-pin text-green-500 w-6 h-6"></i>
                                </div>
                                <div class="text-2xl font-bold text-white">25+</div>
                            </div>
                            <div class="shadow-md border-0 bg-white/5 backdrop-blur-md">
                                <div class="flex flex-row items-center justify-between space-y-0 pb-2">
                                    <div class="text-sm font-medium text-gray-300">Telemedicine Consults</div>
                                    <i class="fas fa-smartphone text-purple-500 w-6 h-6"></i>
                                </div>
                                <div class="text-2xl font-bold text-white">100,000+</div>
                            </div>
                            <div class="shadow-md border-0 bg-white/5 backdrop-blur-md">
                                <div class="flex flex-row items-center justify-between space-y-0 pb-2">
                                    <div class="text-sm font-medium text-gray-300">Community Health Workers</div>
                                    <i class="fas fa-heart text-red-500 w-6 h-6"></i>
                                </div>
                                <div class="text-2xl font-bold text-white">500+</div>
                            </div>
                        </div>
                    </div>
                </section>

                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white text-center mb-12">Our Solutions</h2>
                        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-smartphone text-blue-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Telemedicine & mHealth</h3>
                                    <p class="text-gray-300">Connects patients in remote areas with healthcare professionals through video consultations and mobile health technologies.</p>
                                    <a href="#telemedicine-page" data-page="telemedicine" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-users text-green-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Community Health Workers</h3>
                                    <p class="text-gray-300">Trains and supports local health workers to provide essential services and health education within their communities.</p>
                                    <a href="#chw-page" data-page="chw" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                 <div class="p-6">
                                    <i class="fas fa-map-pin text-purple-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Mobile Health Clinics</h3>
                                    <p class="text-gray-300">Delivers healthcare services directly to underserved populations through mobile medical units.</p>
                                    <a href="#mobileclinics-page" data-page="mobileclinics" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-book-open text-yellow-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Digital Health Literacy</h3>
                                    <p class="text-gray-300">Empowers individuals with the knowledge and skills to manage their health using digital tools and resources.</p>
                                    <a href="#digitalhealth-page" data-page="digitalhealth" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-search text-orange-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">AI Diagnostics</h3>
                                    <p class="text-gray-300">Improves the speed and accuracy of diagnosis in remote areas using artificial intelligence.</p>
                                    <a href="#ai-diagnostics-page" data-page="ai-diagnostics" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white text-center mb-12">What People Say</h2>
                        <div id="testimonial-carousel" class="carousel">
                            <div class="carousel-content">
                                <div class="carousel-item fade">
                                    <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md p-6">
                                        <div class="flex items-center space-x-4 mb-4">
                                            <img src="https://via.placeholder.com/100x100?text=MR" alt="Maria Rodriguez" class="w-12 h-12 rounded-full" />
                                            <div>
                                                <div class="font-semibold text-white">Maria Rodriguez</div>
                                                <div class="text-sm text-gray-400">Rural Village, Mexico</div>
                                            </div>
                                        </div>
                                        <p class="text-gray-300 italic">"Thanks to HealthBridge Connect, I can now consult with a doctor without traveling for days. This has changed my life!"</p>
                                    </div>
                                </div>
                                <div class="carousel-item fade">
                                    <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md p-6">
                                        <div class="flex items-center space-x-4 mb-4">
                                            <img src="https://via.placeholder.com/100x100?text=DO" alt="David Ochieng" class="w-12 h-12 rounded-full" />
                                            <div>
                                                <div class="font-semibold text-white">David Ochieng</div>
                                                <div class="text-sm text-gray-400">Nairobi, Kenya</div>
                                            </div>
                                        </div>
                                        <p class="text-gray-300 italic">"The mobile clinic brought healthcare right to our community. The services were excellent and the staff were very caring."</p>
                                    </div>
                                </div>
                                 <div class="carousel-item fade">
                                    <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md p-6">
                                        <div class="flex items-center space-x-4 mb-4">
                                            <img src="https://via.placeholder.com/100x100?text=SC" alt="Sarah Chen" class="w-12 h-12 rounded-full" />
                                            <div>
                                                <div class="font-semibold text-white">Sarah Chen</div>
                                                <div class="text-sm text-gray-400">Remote Island, Philippines</div>
                                            </div>
                                        </div>
                                        <p class="text-gray-300 italic">"The digital health literacy program helped me understand my health conditions and how to manage them better."</p>
                                    </div>
                                </div>
                            </div>
                            <button class="carousel-prev"><i class="fas fa-chevron-left"></i></button>
                            <button class="carousel-next"><i class="fas fa-chevron-right"></i></button>
                        </div>
                    </div>
                </section>

                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white text-center mb-12">Our Partners</h2>
                        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-8">
                            <div class="flex items-center justify-center p-4">
                                <img src="https://via.placeholder.com/150x50?text=GHF" alt="Global Health Foundation" class="h-12 opacity-70 hover:opacity-100 transition-opacity" />
                            </div>
                            <div class="flex items-center justify-center p-4">
                                <img src="https://via.placeholder.com/150x50?text=RAI" alt="Rural Aid Initiative" class="h-12 opacity-70 hover:opacity-100 transition-opacity" />
                            </div>
                             <div class="flex items-center justify-center p-4">
                                <img src="https://via.placeholder.com/150x50?text=TFG" alt="Tech For Good" class="h-12 opacity-70 hover:opacity-100 transition-opacity" />
                            </div>
                             <div class="flex items-center justify-center p-4">
                                <img src="https://via.placeholder.com/150x50?text=HAN" alt="Health Access Now" class="h-12 opacity-70 hover:opacity-100 transition-opacity" />
                            </div>
                             <div class="flex items-center justify-center p-4">
                                <img src="https://via.placeholder.com/150x50?text=CHS" alt="Community Health Systems" class="h-12 opacity-70 hover:opacity-100 transition-opacity" />
                            </div>
                        </div>
                    </div>
                </section>

                <section class="py-12" id="1st">
                    <div class="container mx-auto px-4 text-center">
                        <h2 class="text-3xl font-bold text-white mb-6">Stay Updated</h2>
                        <p class="text-gray-300 mb-8">Subscribe to our newsletter for the latest news and updates.</p>
                        <form id="newsletter-form" class="flex flex-col sm:flex-row justify-center items-center gap-4 w-full max-w-md mx-auto">
                            <input type="email" id="email" placeholder="Enter your email address" class="bg-white/10 text-white border-gray-700 placeholder:text-gray-400 rounded-md px-4 py-3 w-full sm:w-auto" required />
                            <button type="submit" class="bg-gradient-to-r from-purple-500 to-blue-500 text-white px-8 py-3 rounded-full hover:from-purple-600 hover:to-blue-600 transition-all duration-300 disabled:opacity-70 disabled:cursor-not-allowed">
                                Subscribe
                            </button>
                        </form>
                        <p id="subscription-message" class="mt-4 text-green-400 hidden">
                            <i class="fas fa-check-circle mr-2"></i>
                            Thank you for subscribing!
                        </p>
                        <p id="subscription-error" class="mt-4 text-red-400 hidden">
                            <i class="fas fa-exclamation-triangle mr-2"></i>
                            Please enter a valid email address.
                        </p>
                    </div>
                </section>
            </section>

            <section id="about-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">About Us</h2>
                        <p class="text-gray-300 leading-relaxed">
                            HealthBridge Connect is a non-profit organization dedicated to improving healthcare access in underserved communities around the world. We believe that everyone, regardless of their location or socioeconomic status, deserves access to quality healthcare.
                        </p>
                        <p class="text-gray-300 leading-relaxed">
                            Our mission is to bridge the healthcare gap by developing and implementing innovative, scalable, and sustainable solutions. We work in partnership with local communities, governments, NGOs, and the private sector to achieve our goals.
                        </p>
                    </div>
                </section>

                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Our Team</h2>
                        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Jinitha M</h3>
                                <p class="text-gray-400">Student</p>
                                <p class="text-gray-300 mt-2">Jinitha approaches public health expert with over 20 years of experience...</p>
                            </div>
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Srujan M</h3>
                                <p class="text-gray-400">Student<br>srujanm1426@gmail.com</p>
                                <p class="text-gray-300 mt-2">Srujan leads our technology initiatives, developing innovative solutions...</p>
                            </div>
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Moulya Shree V</h3>
                                <p class="text-gray-400">Student</p>
                                <p class="text-gray-300 mt-2">Moulya works closely with communities to ensure our programs meet their needs...</p>
                            </div>
                        </div>
                    </div>
                </section>

                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Our Values</h2>
                         <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Equity</h3>
                                <p class="text-gray-300 mt-2">We believe in equal access to healthcare for everyone.</p>
                            </div>
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Innovation</h3>
                                <p class="text-gray-300 mt-2">We strive to develop creative and effective solutions.</p>
                            </div>
                            <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md">
                                <h3 class="text-xl font-semibold text-white">Collaboration</h3>
                                <p class="text-gray-300 mt-2">We work in partnership with others to maximize our impact.</p>
                            </div>
                        </div>
                    </div>
                </section>
            </section>

            <section id="solutions-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Our Solutions</h2><p class="text-gray-300 leading-relaxed">
                            We develop and implement a range of solutions to address the challenges of healthcare access in underserved communities. Our programs are designed to be innovative, scalable, and sustainable.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                           <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-smartphone text-blue-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Telemedicine & mHealth</h3>
                                    <p class="text-gray-300">Connects patients in remote areas with healthcare professionals through video consultations and mobile health technologies.</p>
                                    <a href="#telemedicine-page" data-page="telemedicine" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-users text-green-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Community Health Workers</h3>
                                    <p class="text-gray-300">Trains and supports local health workers to provide essential services and health education within their communities.</p>
                                    <a href="#chw-page" data-page="chw" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                 <div class="p-6">
                                    <i class="fas fa-map-pin text-purple-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Mobile Health Clinics</h3>
                                    <p class="text-gray-300">Delivers healthcare services directly to underserved populations through mobile medical units.</p>
                                    <a href="#mobileclinics-page" data-page="mobileclinics" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                    <i class="fas fa-book-open text-yellow-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">Digital Health Literacy</h3>
                                    <p class="text-gray-300">Empowers individuals with the knowledge and skills to manage their health using digital tools and resources.</p>
                                    <a href="#digitalhealth-page" data-page="digitalhealth" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                            <div class="shadow-lg border-0 bg-white/5 backdrop-blur-md transition-transform transform hover:scale-105">
                                <div class="p-6">
                                     <i class="fas fa-search text-orange-500 w-8 h-8 mb-4"></i>
                                    <h3 class="text-xl font-semibold text-white">AI Diagnostics</h3>
                                    <p class="text-gray-300">Improves the speed and accuracy of diagnosis in remote areas using artificial intelligence.</p>
                                    <a href="#ai-diagnostics-page" data-page="ai-diagnostics" class="mt-4 inline-block w-full bg-blue-500/20 text-blue-400 hover:bg-blue-500/30 hover:text-blue-300 py-2 rounded-md text-center">Learn More</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
            </section>

            <section id="telemedicine-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Telemedicine & mHealth</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Telemedicine and mobile health (mHealth) solutions are transforming healthcare delivery, especially in underserved communities. By leveraging technology, we can connect patients with healthcare providers remotely, overcoming geographical barriers and improving access to care.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Key Features</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Video consultations with doctors and specialists</li>
                            <li>Remote monitoring of vital signs</li>
                            <li>Mobile apps for health education and reminders</li>
                            <li>Electronic health records</li>
                            <li>Integration with local health systems</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Benefits</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Increased access to healthcare, especially in remote areas</li>
                            <li>Reduced travel time and costs for patients</li>
                            <li>Improved quality of care and patient outcomes</li>
                            <li>Greater convenience and flexibility</li>
                            <li>Enhanced communication between patients and providers</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Our Impact</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Our telemedicine programs have enabled thousands of patients in underserved communities to receive timely and quality care. We have partnered with local healthcare providers to establish telemedicine clinics, train healthcare workers, and provide technical support.
                        </p>
                    </div>
                </section>
            </section>

             <section id="chw-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Community Health Workers</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Community Health Workers (CHWs) are essential to extending healthcare services to underserved populations. They are trusted members of their communities who provide basic healthcare, health education, and connect people to the formal health system.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Our Approach</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Recruiting and training CHWs from local communities</li>
                            <li>Providing ongoing training and support</li>
                            <li>Equipping CHWs with essential medical supplies and technology</li>
                            <li>Integrating CHWs into the local health system</li>
                            <li>Monitoring and evaluating the impact of CHW programs</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Key Activities</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Conducting health education sessions</li>
                            <li>Providing basic first aid and treatment</li>
                            <li>Conducting home visits to vulnerable populations</li>
                            <li>Identifying and referring patients to health facilities</li>
                            <li>Collecting health data and reporting to health authorities</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Impact</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Our CHW programs have significantly improved health outcomes in underserved communities. CHWs have increased access to healthcare, promoted preventive care, and reduced the burden on health facilities.
                        </p>
                    </div>
                </section>
            </section>

            <section id="mobileclinics-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Mobile Health Clinics</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Mobile health clinics are a flexible and effective way to deliver healthcare services to underserved populations. These mobile units can travel to remote and hard-to-reach areas, providing essential medical care directly to those who need it most.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Services Offered</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>General check-ups and consultations</li>
                            <li>Vaccinations and immunizations</li>
                            <li>Maternal and child health services</li>
                            <li>Basic laboratory tests</li>
                            <li>Treatment of common illnesses</li>
                            <li>Health education and promotion</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Our Fleet</h2>
                        <p class="text-gray-300 leading-relaxed">
                            We operate a fleet of well-equipped mobile health clinics that are staffed by qualified healthcare professionals. Our clinics are designed to provide a comfortable and safe environment for patients.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Schedule & Locations</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Our mobile clinics operate on a regular schedule, visiting different communities throughout the week. Check our schedule to find a clinic near you.
                        </p>
                        </div>
                </section>
            </section>

            <section id="digitalhealth-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Digital Health Literacy</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Digital health literacy is the ability to seek, find, understand, and appraise health information from electronic sources and apply the knowledge gained to addressing or solving a health problem. In today's digital age, it is crucial for individuals to have the skills to navigate and use health information effectively.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Our Programs</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Online courses and workshops</li>
                            <li>Mobile apps for health education</li>
                            <li>Interactive tools and resources</li>
                            <li>Community training sessions</li>
                            <li>Partnerships with schools and libraries</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Key Topics</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Finding reliable health information online</li>
                            <li>Evaluating the credibility of health websites</li>
                            <li>Using mobile apps for health management</li>
                            <li>Protecting your privacy and security online</li>
                            <li>Communicating with healthcare providers online</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Impact</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Our digital health literacy programs have empowered individuals to take control of their health, make informed decisions, and access healthcare services more effectively.
                        </p>
                    </div>
                </section>
            </section>

            <section id="ai-diagnostics-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">AI Diagnostics</h2>
                        <p class="text-gray-300 leading-relaxed">
                            Artificial intelligence (AI) is revolutionizing healthcare, particularly in diagnostics. AI-powered tools can analyze medical images, lab results, and other data to detect diseases earlier and more accurately. This technology has the potential to transform healthcare delivery in underserved communities, where access to specialists and advanced diagnostic equipment may be limited.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Our Solutions</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>AI-powered image analysis for detecting diseases like tuberculosis and malaria</li>
                            <li>Machine learning algorithms for predicting disease risk</li>
                            <li>Mobile apps with AI for rapid point-of-care diagnostics</li>
                            <li>Integration of AI tools into telemedicine platforms</li>
                            <li>Training programs for healthcare workers on using AI diagnostics</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Benefits</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Faster and more accurate diagnoses</li>
                            <li>Earlier detection of diseases, leading to better outcomes</li>
                            <li>Reduced need for specialist consultations</li>
                            <li>Lower healthcare costs</li>
                            <li>Improved access to diagnostics in remote areas</li>
                        </ul>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Ethical Considerations</h2>
                        <p class="text-gray-300 leading-relaxed">
                            We are committed to developing and deploying AI diagnostics in an ethical and responsible manner. We prioritize data privacy, security, and fairness, and we work closely with communities to ensure that our solutions are culturally appropriate and meet their needs.
                        </p>
                    </div>
                </section>
            </section>

            <section id="get-involved-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Get Involved</h2>
                        <p class="text-gray-300 leading-relaxed">
                            There are many ways to support our mission and help us improve healthcare access in underserved communities. Whether you want to donate, volunteer your time, or partner with us, your contribution can make a significant difference.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <div class="w-full">
                            <div class="tabs">
                                <div class="tabs-list grid w-full grid-cols-3 bg-white/5 backdrop-blur-md border border-gray-700">
                                    <button data-tab="donate" class="tab text-white data-[state=active]:bg-blue-500/20 data-[state=active]:text-blue-400 px-4 py-2 rounded-t-md">
                                        <i class="fas fa-donate mr-2"></i> Donate
                                    </button>
                                    <button data-tab="volunteer" class="tab text-white data-[state=active]:bg-green-500/20 data-[state=active]:text-green-400 px-4 py-2 rounded-t-md">
                                        <i class="fas fa-hand-paper mr-2"></i> Volunteer
                                    </button>
                                    <button data-tab="partners" class="tab text-white data-[state=active]:bg-purple-500/20 data-[state=active]:text-purple-400 px-4 py-2 rounded-t-md">
                                        <i class="fas fa-hands-helping mr-2"></i> Partnerships
                                    </button>
                                </div>
                                <div class="tabs-content">
                                    <div data-tab-content="donate" class="tab-content active space-y-4 p-6 bg-white/5 backdrop-blur-md">
                                        <h3 class="text-2xl font-semibold text-white">Make a Donation</h3>
                                        <p class="text-gray-300">
                                            Your donation will help us provide essential healthcare services, train community health workers, and expand our programs to reach more people in need.
                                        </p>
                                        <button class="bg-gradient-to-r from-blue-500 to-purple-500 text-white px-8 py-3 rounded-full hover:from-blue-600 hover:to-purple-600 transition-all duration-300">
                                            Donate Now
                                        </button>
                                        <p class="text-gray-400">
                                            We accept all major credit cards and online payment methods.
                                        </p>
                                    </div>
                                    <div data-tab-content="volunteer" class="tab-content space-y-4 p-6 bg-white/5 backdrop-blur-md">
                                        <h3 class="text-2xl font-semibold text-white">Volunteer With Us</h3>
                                        <p class="text-gray-300">
                                            We rely on the support of dedicated volunteers to help us deliver our programs and services. Whether you are a healthcare professional, a student, or simply passionate about our cause, we have a volunteer opportunity for you.
                                        </p>
                                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                                            <li>Medical professionals (doctors, nurses, etc.)</li>
                                            <li>Administrative support</li>
                                            <li>Community outreach</li>
                                            <li>Translation services</li>
                                            <li>Fundraising and event planning</li>
                                        </ul>
                                         <button class="bg-gradient-to-r from-green-500 to-teal-500 text-white px-8 py-3 rounded-full hover:from-green-600 hover:to-teal-600 transition-all duration-300">
                                            Volunteer Opportunities
                                        </button>
                                    </div>
                                    <div data-tab-content="partners" class="tab-content space-y-4 p-6 bg-white/5 backdrop-blur-md">
                                        <h3 class="text-2xl font-semibold text-white">Partner With Us</h3>
                                        <p class="text-gray-300">
                                            We partner with NGOs, corporations, government agencies, and other organizations to leverage resources, expertise, and networks. Together, we can achieve greater impact and create lasting change.
                                        </p>
                                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                                            <li>Financial partnerships</li>
                                            <li>In-kind donations</li>
                                            <li>Technical assistance</li>
                                            <li>Program collaboration</li>
                                            <li>Joint advocacy</li>
                                        </ul>
                                        <button class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-8 py-3 rounded-full hover:from-purple-600 hover:to-pink-600 transition-all duration-300">
                                            Become a Partner
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
            </section>

            <section id="resources-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-3xl font-bold text-white mb-6">Resources</h2>
                        <p class="text-gray-300 leading-relaxed">
                            We provide a variety of resources to support healthcare professionals, community health workers, and individuals seeking health information.
                        </p>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Blog & News</h2>
                        <div class="bg-white/5 backdrop-blur-md rounded-lg p-6 shadow-md mb-4">
                            <h3 class="text-xl font-semibold text-white">Latest Update</h3>
                            <p class="text-gray-400">Posted on March 15, 2024</p>
                            <p class="text-gray-300 mt-2">We launched a new mobile clinic in rural Kenya...</p>
                        </div>
                    </div>
                </section>
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">Downloads</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li><a href="https://chwcentral.org/wp-content/uploads/2013/07/Community-Health-Worker-Training-Manual.pdf" class="text-blue-400 hover:text-blue-300">Community Health Worker Training Manual (PDF)</a></li>
                            <li><a href="https://iris.who.int/bitstream/handle/10665/364221/9789240059184-eng.pdf?sequence=1&isAllowed=y" class="text-blue-400 hover:text-blue-300">Telemedicine Implementation Guide (PDF)</a></li>
                            <li><a href="https://iris.who.int/bitstream/handle/10665/205244/B5148.pdf?sequence=1" class="text-blue-400 hover:text-blue-300">Digital Health Literacy Toolkit (ZIP)</a></li>
                        </ul>
                    </div>
                </section>
                <section class="py-12 bg-gray-900">
                    <div class="container mx-auto px-4">
                        <h2 class="text-2xl font-bold text-white mb-4">External Resources</h2>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li><a href="https://www.who.int/" target="_blank" rel="noopener noreferrer" class="text-blue-400 hover:text-blue-300">World Health Organization (WHO)</a></li>
                            <li><a href="https://www.un.org/sustainabledevelopment/health/" target="_blank" rel="noopener noreferrer" class="text-blue-400 hover:text-blue-300">UN Sustainable Development Goals - Goal 3</a></li>
                            <li><a href="https://www.cdc.gov/" target="_blank" rel="noopener noreferrer" class="text-blue-400 hover:text-blue-300">Centers for Disease Control and Prevention (CDC)</a></li>
                        </ul>
                    </div>
                </section>
            </section>

            <!-- <section id="contact-page" class="page">
                <section class="py-12">
                    <div class="container mx-auto px-4">
                        <h2 clas -->



                        <footer id="contactus" style="background-color: #262525; padding: 20px; text-align: center; border-top: 1px solid #ddd;">
                            <div style="max-width: 800px; margin: 0 auto; color: white;">
                              <div style="display: flex; justify-content: space-around; flex-wrap: wrap;">
                                <div style="margin-bottom: 10px; ">
                                  <strong>Contact Us</strong><br>
                                  Email: <a href="mailto:info@example.com">srujanm1426@gmail.com</a><br>
                                  Phone: +91 8971338636<br>
                                  Address: Mysore, Karnataka, India
                                </div>
                          
                              
                                <div style="margin-bottom: 10px;">
                                  <strong>Follow Us</strong><br>
                               
                                  <a href="https://www.linkedin.com/in/srujan-m-932947298/">LinkedIn</a>
                                </div>
                              </div>
                              <hr style="margin-top: 20px; border: none; border-top: 1px solid #ddd;">
                              <p>&copy; 2024 Example Company. All rights reserved.</p>
                            </div>
                          </footer>
