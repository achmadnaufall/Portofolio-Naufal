<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Achmad Naufal - 3D Animator</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css" rel="stylesheet">
    <!-- Add Swiper's CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Swiper/8.4.5/swiper-bundle.min.css">
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
        }
        
        .reveal-text {
            animation: reveal 1s ease-in-out;
        }
        
        @keyframes reveal {
            0% { transform: translateY(20px); opacity: 0; }
            100% { transform: translateY(0); opacity: 1; }
        }

        .hero-image {
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }

        .gradient-text {
            background: linear-gradient(90deg, #0ea5e9, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .social-icon {
            transition: all 0.3s ease;
        }

        .social-icon:hover {
            transform: translateY(-3px);
        }

        /* Carousel Styles */
        .swiper-container {
            width: 100%;
            padding-top: 50px;
            padding-bottom: 50px;
        }

        .swiper-slide {
            background-position: center;
            background-size: cover;
            width: 300px;
            height: 300px;
        }

        .swiper-slide iframe {
            width: 100%;
            height: 100%;
            border-radius: 15px;
            box-shadow: 0 15px 25px rgba(0,0,0,0.3);
        }

        /* Mobile menu styles */
        .mobile-menu {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: rgba(17, 24, 39, 0.95);
            z-index: 40;
        }

        .mobile-menu.active {
            display: flex;
        }

        @media (max-width: 768px) {
            .hero-content {
                padding: 2rem 1rem;
            }
            
            .hero-image-container {
                margin-top: 2rem;
                padding: 0 1rem;
            }

            .swiper-slide {
                width: 250px;
                height: 250px;
            }
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Fixed Navigation -->
    <nav class="fixed w-full z-50 bg-gray-900/90 backdrop-blur-sm">
        <div class="container mx-auto px-4 sm:px-6 py-4">
            <div class="flex justify-between items-center">
                <a href="#" class="text-2xl font-bold gradient-text">AN.</a>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-4">
                    <a href="#work" class="px-4 py-2 rounded-lg hover:bg-sky-500/10 transition-colors duration-300">Work</a>
                    <a href="#about" class="px-4 py-2 rounded-lg hover:bg-sky-500/10 transition-colors duration-300">About</a>
                    <a href="#contact" class="px-4 py-2 rounded-lg hover:bg-sky-500/10 transition-colors duration-300">Contact</a>
                    <div class="flex space-x-4 ml-4">
                        <a href="https://www.linkedin.com/in/achmad-naufal-9b044a199/" target="_blank" class="social-icon p-2 rounded-lg hover:bg-sky-500/10">
                            <img src="https://i.ibb.co.com/bBz1qdV/linkedin.png" alt="LinkedIn" class="w-6 h-6">
                        </a>
                        <a href="mailto:achmadnaufal3@gmail.com" class="social-icon p-2 rounded-lg hover:bg-sky-500/10">
                            <img src="https://i.ibb.co.com/rb7jJB8/gmail.webp" alt="Email" class="w-6 h-6">
                        </a>
                        <a href="https://wa.me/081808582445" class="social-icon p-2 rounded-lg hover:bg-sky-500/10">
                            <img src="https://i.ibb.co.com/r6fX13g/WA.png" alt="WhatsApp" class="w-6 h-6">
                        </a>
                    </div>
                </div>

                <!-- Mobile Menu Button -->
                <button class="md:hidden text-2xl" id="mobile-menu-button">☰</button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div class="mobile-menu hidden md:hidden" id="mobile-menu">
            <div class="container mx-auto px-4 py-8 flex flex-col items-center space-y-6">
                <a href="#work" class="text-xl py-2">Work</a>
                <a href="#about" class="text-xl py-2">About</a>
                <a href="#contact" class="text-xl py-2">Contact</a>
                <div class="flex space-x-6 mt-6">
                    <a href="https://www.linkedin.com/in/achmad-naufal-9b044a199/" target="_blank" class="social-icon">
                        <img src="https://i.ibb.co.com/bBz1qdV/linkedin.png" alt="LinkedIn" class="w-8 h-8">
                    </a>
                    <a href="mailto:achmadnaufal3@gmail.com" class="social-icon">
                        <img src="https://i.ibb.co.com/rb7jJB8/gmail.webp" alt="Email" class="w-8 h-8">
                    </a>
                    <a href="https://wa.me/081808582445" class="social-icon">
                        <img src="https://i.ibb.co.com/r6fX13g/WA.png" alt="WhatsApp" class="w-8 h-8">
                    </a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="min-h-screen flex items-center gradient-bg">
        <div class="container mx-auto px-4 sm:px-6 py-24">
            <div class="grid md:grid-cols-2 gap-8 lg:gap-12 items-center">
                <div data-aos="fade-right" class="hero-content">
                    <h2 class="text-sky-400 text-xl font-semibold mb-4">3D Animator</h2>
                    <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold mb-6 gradient-text">Achmad Naufal</h1>
                    <p class="text-gray-300 text-base sm:text-lg mb-8">I am a passionate 3D Animator dedicated to bringing stories to life through high-quality and engaging animations. Animation is not just my profession but my true calling, and I strive to deliver work that inspires and exceeds expectations.</p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <a href="#work" class="bg-sky-500 hover:bg-sky-600 text-white px-8 py-3 rounded-full transition-colors duration-300 text-center">View Work</a>
                        <a href="#contact" class="border border-sky-500 hover:bg-sky-500/10 px-8 py-3 rounded-full transition-colors duration-300 text-center">Contact Me</a>
                    </div>
                </div>
                <div class="hidden md:block hero-image-container" data-aos="fade-left">
                    <div class="relative">
                        <div class="hero-image relative z-10">
                            <img src="https://i.ibb.co.com/7j3rw3p/Foto-Profil-Achmad-Naufal.jpg" alt="Achmad Naufal" class="rounded-2xl shadow-2xl w-full">
                        </div>
                        <div class="absolute inset-0 bg-sky-500/20 rounded-2xl filter blur-3xl"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
  <!-- Work Section -->
<section id="work" class="py-20 bg-gray-900">
    <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2 class="text-4xl font-bold mb-4 gradient-text">Featured Works</h2>
            <p class="text-gray-400 max-w-2xl mx-auto">Explore my collection of 3D animations, series works, and commercial projects.</p>
        </div>

        <!-- Filter Buttons -->
        <div class="flex flex-wrap justify-center gap-4 mb-12" data-aos="fade-up">
            <button class="px-6 py-2 rounded-full bg-sky-500 text-white">All</button>
            <button class="px-6 py-2 rounded-full hover:bg-sky-500/10 border border-sky-500">3D Bumper</button>
            <button class="px-6 py-2 rounded-full hover:bg-sky-500/10 border border-sky-500">Series</button>
            <button class="px-6 py-2 rounded-full hover:bg-sky-500/10 border border-sky-500">Commercials</button>
            <button class="px-6 py-2 rounded-full hover:bg-sky-500/10 border border-sky-500">VFX</button>
        </div>

        <!-- 3D Bumper Section with Carousel -->
        <div class="mb-16" data-aos="fade-up">
            <h3 class="text-2xl font-bold text-sky-400 mb-8 text-center">3D Bumper Projects</h3>
            <div class="swiper-container" id="bumperSwiper">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">
                        <iframe src="https://www.youtube.com/embed/bnE9b4bX-HM?si=2tYIuOchgDlwUWOB" 
                                title="YouTube video player" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen></iframe>
                    </div>
                    <div class="swiper-slide">
                        <iframe src="https://www.youtube.com/embed/ClLzL6glFn4?si=y4XhpPI8-xYAMq-K" 
                                title="YouTube video player" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen></iframe>
                    </div>
                    <div class="swiper-slide">
                        <iframe src="https://www.youtube.com/embed/XeFFIanDb3A?si=ge6kzS8kI9DGHhho" 
                                title="YouTube video player" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen></iframe>
                    </div>
                    <div class="swiper-slide">
                        <iframe src="https://www.youtube.com/embed/UpvxG8tGIys?si=oIfW0k0dnytJIFZo" 
                                title="YouTube video player" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen></iframe>
                    </div>
                    <div class="swiper-slide">
                        <iframe src="https://www.youtube.com/embed/ddCpib3W5z8?si=dwWthQBfK88uhwd1" 
                                title="YouTube video player" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen></iframe>
                    </div>
                </div>
                <!-- Add Navigation -->
                <div class="swiper-button-next text-sky-500"></div>
                <div class="swiper-button-prev text-sky-500"></div>
                <!-- Add Pagination -->
                <div class="swiper-pagination"></div>
            </div>
        </div>

        <!-- Project Grid -->
        <div class="grid grid-cols-1 gap-12">
            <!-- Project 1: Pawpawland -->
            <div class="bg-gray-800 rounded-xl overflow-hidden" data-aos="fade-up">
                <div class="aspect-w-16 aspect-h-9 relative" style="padding-top: 56.25%;">
                    <iframe 
                        src="https://www.youtube.com/embed/s8DQqebfqnc" 
                        frameborder="0" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen
                        class="absolute inset-0 w-full h-full">
                    </iframe>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2 text-sky-400">Pawpawland</h3>
                    <p class="text-gray-300">I work as a 3D animator for series, mini-series, animated ads, and short projects.</p>
                </div>
            </div>

            <!-- Project 2: Animated Advertisements -->
            <div class="bg-gray-800 rounded-xl overflow-hidden" data-aos="fade-up">
                <div class="aspect-w-9 aspect-h-16 relative mx-auto max-w-[200px]" style="padding-top: 177.78%;">
                    <iframe 
                        src="https://www.instagram.com/reel/DDG-aVvyw1H/embed" 
                        frameborder="0" 
                        allowfullscreen
                        class="absolute inset-0 w-full h-full">
                    </iframe>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2 text-sky-400">Animated Advertisements</h3>
                    <p class="text-gray-300">My portfolio involves working on animated advertisements with real live video or VFX. I specialize as a 3D animator and 3D tracking camera expert.</p>
                </div>
            </div>

            <!-- Project 3: Animation Series -->
            <div class="bg-gray-800 rounded-xl overflow-hidden" data-aos="fade-up">
                <div class="aspect-w-16 aspect-h-9 relative" style="padding-top: 56.25%;">
                    <iframe 
                        src="https://www.youtube.com/embed/E3uQFNuo7vg" 
                        frameborder="0" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen
                        class="absolute inset-0 w-full h-full">
                    </iframe>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2 text-sky-400">Animation Series Portfolio</h3>
                    <p class="text-gray-300">I also worked on animation for the 3D animation series <strong>Cocomelon</strong>, <strong>Superfamily</strong>, and <strong>Kangaroo Beach</strong>.</p>
                </div>
            </div>
        </div>
    </div>
</section>
  <!-- About Section -->
<section id="about" class="py-20 bg-gray-800">
    <div class="container mx-auto px-4 sm:px-6">
        <div class="max-w-4xl mx-auto" data-aos="fade-up">
            <h2 class="text-4xl font-bold mb-8 gradient-text text-center">About Me</h2>
            <div class="bg-gray-700/50 p-6 sm:p-8 rounded-2xl backdrop-blur-sm">
                <p class="text-gray-300 text-lg mb-6">
                    With over 2.5 years of experience in 3D animation, I have had the opportunity to work on a diverse range of projects, including animated series and commercial advertisements. My expertise is centered around creating smooth character animations and scene compositions that enhance storytelling.
                </p>
                <p class="text-gray-300 text-lg mb-6">
                    I've contributed to notable projects including Cocomelon, Superfamily, and Kangaroo Beach, where I specialized in character animation and scene composition. My work in commercial projects has helped brands bring their visions to life through captivating animated content.
                </p>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mt-12">
                    <div class="bg-gray-800/50 p-6 rounded-xl transform hover:-translate-y-2 transition-all duration-300">
                        <h3 class="text-xl font-bold text-sky-400 mb-2">Experience</h3>
                        <p class="text-gray-400">2+ Years</p>
                    </div>
                    <div class="bg-gray-800/50 p-6 rounded-xl transform hover:-translate-y-2 transition-all duration-300">
                        <h3 class="text-xl font-bold text-sky-400 mb-2">Projects</h3>
                        <p class="text-gray-400">10+ Completed</p>
                    </div>
                    <div class="bg-gray-800/50 p-6 rounded-xl transform hover:-translate-y-2 transition-all duration-300">
                        <h3 class="text-xl font-bold text-sky-400 mb-2">Specialization</h3>
                        <p class="text-gray-400">Character Animation</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section id="contact" class="py-20 bg-gray-900">
    <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2 class="text-4xl font-bold mb-4 gradient-text">Get in Touch</h2>
            <p class="text-gray-400 max-w-2xl mx-auto">Feel free to reach out for collaborations or just a friendly hello</p>
        </div>
        
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
            <!-- LinkedIn Card -->
            <div class="bg-gray-800/50 p-6 rounded-xl backdrop-blur-sm transform hover:-translate-y-2 transition-all duration-300">
                <div class="text-center">
                    <img src="https://i.ibb.co.com/bBz1qdV/linkedin.png" alt="LinkedIn" class="w-16 h-16 mx-auto mb-4">
                    <h3 class="text-xl font-bold mb-2">LinkedIn</h3>
                    <p class="text-gray-400 mb-4">Let's connect professionally</p>
                    <a href="https://www.linkedin.com/in/achmad-naufal-9b044a199/" target="_blank" 
                       class="inline-block bg-[#0077B5] text-white px-6 py-2 rounded-full hover:bg-[#0077B5]/80 transition-colors duration-300">
                        Visit Profile
                    </a>
                </div>
            </div>

            <!-- Email Card -->
            <div class="bg-gray-800/50 p-6 rounded-xl backdrop-blur-sm transform hover:-translate-y-2 transition-all duration-300">
                <div class="text-center">
                    <img src="https://i.ibb.co.com/rb7jJB8/gmail.webp" alt="Email" class="w-16 h-16 mx-auto mb-4">
                    <h3 class="text-xl font-bold mb-2">Email</h3>
                    <p class="text-gray-400 mb-4">achmadnaufal3@gmail.com</p>
                    <button onclick="copyEmail()" 
                            class="bg-[#EA4335] text-white px-6 py-2 rounded-full hover:bg-[#EA4335]/80 transition-colors duration-300">
                        Copy Email
                    </button>
                </div>
            </div>

            <!-- WhatsApp Card -->
            <div class="bg-gray-800/50 p-6 rounded-xl backdrop-blur-sm transform hover:-translate-y-2 transition-all duration-300">
                <div class="text-center">
                    <img src="https://i.ibb.co.com/r6fX13g/WA.png" alt="WhatsApp" class="w-16 h-16 mx-auto mb-4">
                    <h3 class="text-xl font-bold mb-2">WhatsApp</h3>
                    <p class="text-gray-400 mb-4">+62 81808582445</p>
                    <button onclick="copyWhatsApp()" 
                            class="bg-[#25D366] text-white px-6 py-2 rounded-full hover:bg-[#25D366]/80 transition-colors duration-300">
                        Copy Number
                    </button>
                </div>
            </div>
        </div>
    </div>
</section>
  <!-- Footer -->
<footer class="bg-gray-800 py-8">
    <div class="container mx-auto px-6 text-center text-gray-400">
        <p>&copy; 2025 Achmad Naufal. All rights reserved.</p>
    </div>
</footer>

<!-- Scripts -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Swiper/8.4.5/swiper-bundle.min.js"></script>
<script>
    // Initialize AOS
    AOS.init({
        duration: 800,
        once: true,
        offset: 100
    });

    // Initialize Swiper
    const bumperSwiper = new Swiper("#bumperSwiper", {
        effect: "cards",
        grabCursor: true,
        centeredSlides: true,
        slidesPerView: "auto",
        spaceBetween: 30,
        loop: true,
        autoplay: {
            delay: 3000,
            disableOnInteraction: false,
        },
        pagination: {
            el: ".swiper-pagination",
            clickable: true,
        },
        navigation: {
            nextEl: ".swiper-button-next",
            prevEl: ".swiper-button-prev",
        },
        breakpoints: {
            320: {
                slidesPerView: 1,
                spaceBetween: 20
            },
            640: {
                slidesPerView: "auto",
                spaceBetween: 30
            }
        }
    });

    // Mobile Menu Toggle
    const mobileMenuButton = document.getElementById('mobile-menu-button');
    const mobileMenu = document.getElementById('mobile-menu');

    mobileMenuButton.addEventListener('click', () => {
        mobileMenu.classList.toggle('hidden');
        mobileMenu.classList.toggle('active');
    });

    // Close mobile menu when clicking outside
    document.addEventListener('click', (e) => {
        if (!mobileMenu.contains(e.target) && !mobileMenuButton.contains(e.target)) {
            mobileMenu.classList.add('hidden');
            mobileMenu.classList.remove('active');
        }
    });

    // Copy functions
    function copyEmail() {
        navigator.clipboard.writeText('achmadnaufal3@gmail.com')
            .then(() => {
                showCopyAlert('Email copied to clipboard!');
            })
            .catch(() => {
                showCopyAlert('Failed to copy email. Please try again.');
            });
    }

    function copyWhatsApp() {
        navigator.clipboard.writeText('081808582445')
            .then(() => {
                showCopyAlert('WhatsApp number copied to clipboard!');
            })
            .catch(() => {
                showCopyAlert('Failed to copy number. Please try again.');
            });
    }

    // Custom alert function
    function showCopyAlert(message) {
        const alert = document.createElement('div');
        alert.className = 'fixed bottom-4 right-4 bg-sky-500 text-white px-6 py-3 rounded-lg shadow-lg transform transition-all duration-300 opacity-0';
        alert.textContent = message;
        document.body.appendChild(alert);

        // Fade in
        setTimeout(() => {
            alert.style.opacity = '1';
        }, 10);

        // Fade out and remove
        setTimeout(() => {
            alert.style.opacity = '0';
            setTimeout(() => {
                document.body.removeChild(alert);
            }, 300);
        }, 2000);
    }

    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
                // Close mobile menu if open
                mobileMenu.classList.add('hidden');
                mobileMenu.classList.remove('active');
            }
        });
    });
</script>
</body>
</html>
