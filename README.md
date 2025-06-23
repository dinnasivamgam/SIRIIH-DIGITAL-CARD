# SIRIIH-DIGITAL-CARD
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Haritha Dinna Sivamugam - Animated Digital Business Card</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif; /* Default font for body */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #1a1a1a; /* Dark background for overall page */
            margin: 0;
            padding: 1rem;
            box-sizing: border-box;
            overflow: hidden; /* Prevent scrollbars from animation overflow */
        }
        .digital-card-container {
            width: 100%;
            max-width: 400px; /* Max width for a digital card, slightly wider for readability */
            height: auto;
            background: 
                linear-gradient(145deg, rgba(255, 255, 255, 0.08) 0%, rgba(255, 255, 255, 0) 70%), /* Subtle highlight */
                linear-gradient(20deg, #101010 0%, #3a3a3a 100%); /* Deep dark gradient */
            border-radius: 1.5rem;
            box-shadow: 
                0 25px 50px -12px rgba(0, 0, 0, 0.5), /* Stronger main shadow */
                0 10px 20px -5px rgba(0, 0, 0, 0.4),  /* Mid-level shadow */
                inset 0 0 15px rgba(255, 255, 255, 0.05); /* Subtle inner glow for gloss */
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2.5rem 1.5rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            color: #e0e0e0; /* Light text for dark background */
            border: 1px solid rgba(255, 255, 255, 0.1); /* Subtle light border */
            
            /* Initial state for card animation */
            opacity: 0;
            transform: translateY(20px) scale(0.98);
            animation: cardFadeIn 1s ease-out forwards; /* Apply card animation */
        }

        /* Adding a pseudo-element for subtle texture overlay */
        .digital-card-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: url("data:image/svg+xml,%3Csvg width='6' height='6' viewBox='0 0 6 6' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%239C92AC' fill-opacity='0.05' fill-rule='evenodd'%3E%3Cpath d='M96 23C78.916 23 64 37.916 64 55v36c0 17.084 14.916 32 32 32s32-14.916 32-32V55c0-17.084-14.916-32-32-32zm0 40c-4.418 0-8-3.582-8-8s3.582-8 8-8 8 3.582 8 8-3.582 8-8 8z' /%3E%3C/g%3E%3C/svg%3E");
            opacity: 0.2; /* Adjust for desired intensity */
            pointer-events: none; /* Allows clicks to pass through */
            /* Animation for texture */
            animation: texturePan 30s linear infinite alternate;
        }

        /* Hover effect for the card */
        .digital-card-container:hover {
            transform: translateY(0) scale(1.02); /* Scale up slightly on hover */
            box-shadow: 0 30px 60px -15px rgba(0, 0, 0, 0.6), 0 15px 30px -10px rgba(0, 0, 0, 0.5), inset 0 0 20px rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        }

        /* Keyframe for card fade-in */
        @keyframes cardFadeIn {
            0% { opacity: 0; transform: translateY(20px) scale(0.98); }
            100% { opacity: 1; transform: translateY(0) scale(1); }
        }

        /* Keyframe for element fade-in and subtle glow for gold elements */
        @keyframes elementFadeInUp {
            0% { opacity: 0; transform: translateY(10px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes elementSlideInLeft {
            0% { opacity: 0; transform: translateX(-20px); }
            100% { opacity: 1; transform: translateX(0); }
        }
        
        @keyframes elementSlideInRight {
            0% { opacity: 0; transform: translateX(20px); }
            100% { opacity: 1; transform: translateX(0); }
        }

        @keyframes goldPulse {
            0%, 100% { text-shadow: 0 0 8px rgba(255, 215, 0, 0.7); } 
            50% { text-shadow: 0 0 15px rgba(255, 215, 0, 1), 0 0 20px rgba(255, 215, 0, 0.5); }
        }

        @keyframes dividerGlow {
            0%, 100% { background-color: #4a4a4a; opacity: 0.6; }
            50% { background-color: #FFD700; opacity: 0.8; }
        }

        @keyframes texturePan {
            0% { background-position: 0% 0%; }
            100% { background-position: 100% 100%; }
        }


        /* Apply animations with delay */
        .animated-item {
            opacity: 0; /* Hidden by default */
            animation: elementFadeInUp 0.6s ease-out forwards;
        }

        .animated-delay-1 { animation-delay: 0.5s; }
        .animated-delay-2 { animation-delay: 0.7s; }
        .animated-delay-3 { animation-delay: 0.9s; }
        .animated-delay-4 { animation-delay: 1.1s; }
        .animated-delay-5 { animation-delay: 1.3s; }
        .animated-delay-6 { animation-delay: 1.5s; }
        .animated-delay-7 { animation-delay: 1.7s; }
        .animated-delay-8 { animation-delay: 1.9s; }
        .animated-delay-9 { animation-delay: 2.1s; }
        .animated-delay-10 { animation-delay: 2.3s; }
        .animated-delay-11 { animation-delay: 2.5s; }
        .animated-delay-12 { animation-delay: 2.7s; }


        .section-divider {
            width: 80%;
            height: 2px;
            background-color: #4a4a4a; /* Dark grey divider */
            margin: 1.5rem auto;
            border-radius: 1px;
            opacity: 0.6; /* Slightly transparent for texture */
            animation: dividerGlow 4s infinite alternate; /* Divider glow */
        }
        .text-gold {
            color: #FFD700; /* Standard shiny gold color */
            text-shadow: 0 0 8px rgba(255, 215, 0, 0.7); /* Subtle glow for gold text */
            animation: goldPulse 3s infinite alternate; /* Apply subtle pulse animation */
        }
        /* New font styles for names */
        .font-playfair {
            font-family: 'Playfair Display', serif;
        }
        .text-logo {
            font-family: 'Playfair Display', serif; /* Consistent with other names */
            font-size: 2.5rem; /* Larger font size for logo effect */
            font-weight: 700; /* Bold for prominence */
            color: #FFD700; /* Standard shiny gold color */
            text-shadow: 0 0 12px rgba(255, 215, 0, 0.9); /* More prominent glow for logo */
            margin-bottom: 2.5rem; /* Space below the logo */
            letter-spacing: 0.05em; /* Slightly increased letter spacing */
            animation: elementFadeInUp 0.6s ease-out forwards; /* Initial fade-in */
        }
        /* Style for clickable links */
        .contact-link {
            transition: color 0.2s ease-in-out, transform 0.2s ease-in-out;
            display: flex; /* Ensure icon and text are inline */
            align-items: center;
            justify-content: center; /* Center content in link */
        }
        .contact-link:hover {
            color: #FFFFC0; /* Lighter shiny gold on hover */
            transform: translateY(-2px);
        }

        /* Responsive adjustments */
        @media (max-width: 450px) {
            .digital-card-container {
                padding: 1.5rem 0.75rem;
                border-radius: 1rem;
            }
            .text-logo {
                font-size: 2.2rem; /* Adjust font size for smaller screens */
            }
            .h-5, .w-5 {
                height: 1.25rem;
                width: 1.25rem;
            }
            .text-xl {
                font-size: 1.15rem;
            }
            .text-md {
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <div class="digital-card-container">
        <!-- Text-based Logo (Directly using H1 for logo) -->
        <h1 class="text-logo animated-item">SIRIIH GROUPS</h1>
        
        <div class="section-divider animated-item animated-delay-1"></div>

        <!-- Personal Details -->
        <h3 class="text-xl font-semibold text-gray-100 mb-1 font-playfair animated-item animated-delay-2">HARITHA DINNA SIVAMUGAM</h3>
        <p class="text-md text-gray-300 font-medium mb-4 animated-item animated-delay-3">FOUNDER & CEO</p>

        <div class="section-divider animated-item animated-delay-4"></div>

        <!-- Contact Information -->
        <div class="mt-6 text-gray-200 text-sm">
            <div class="flex items-center justify-center mb-2 animated-item animated-delay-5">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gold mr-2" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M7 2a2 2 0 00-2 2v12a2 2 0 002 2h6a2 2 0 002-2V4a2 2 0 00-2-2H7zm3 14a1 1 0 100-2 1 1 0 000 2z" clip-rule="evenodd" />
                </svg>
                <a href="tel:+918754150169" class="contact-link">+91 87541 50169</a>
            </div>
            <div class="flex items-start justify-center text-center leading-relaxed mb-4 animated-item animated-delay-6">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gold mr-2 flex-shrink-0 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
                </svg>
                <address class="not-italic">
                    <a href="https://www.google.com/maps/search/?api=1&query=No:2,SSS+Avenue,Kulathupalayam+Road,Kovaipudur,Coimbatore+-641042" target="_blank" rel="noopener noreferrer" class="contact-link">
                        No:2, SSS Avenue,<br>
                        Kulathupalayam Road,<br>
                        Kovaipudur, Coimbatore - 641042
                    </a>
                </address>
            </div>

            <!-- Social Media Section -->
            <div class="section-divider animated-item animated-delay-7"></div>
            <p class="text-sm text-gray-300 font-medium mb-3 animated-item animated-delay-8">Follow us on</p>
            <div class="grid grid-cols-1 gap-3 w-full">
                <a href="https://www.instagram.com/siriihgroups" target="_blank" rel="noopener noreferrer" class="contact-link text-gray-200 animated-item animated-delay-9">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gold mr-2" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                        <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                        <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                    </svg>
                    <span>@siriihgroups (Instagram)</span>
                </a>
                <a href="https://www.facebook.com/siriihgroups" target="_blank" rel="noopener noreferrer" class="contact-link text-gray-200 animated-item animated-delay-10">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gold mr-2" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"></path>
                    </svg>
                    <span>@siriihgroups (Facebook)</span>
                </a>
                <a href="https://twitter.com/siriihgroups" target="_blank" rel="noopener noreferrer" class="contact-link text-gray-200 animated-item animated-delay-11">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gold mr-2" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M22.254 5.923c-.792.351-1.64.587-2.525.69a4.484 4.484 0 0 0 1.956-2.433c-.876.521-1.85.897-2.88 1.1A4.485 4.485 0 0 0 14.004 2c-2.483 0-4.5 2.017-4.5 4.5 0 .351.04.693.118 1.02a12.722 12.722 0 0 1-9.22-4.664c-.38.65-.596 1.408-.596 2.21 0 1.554.79 2.924 1.987 3.73A4.47 4.47 0 0 1 .927 9.855v.056c0 2.17 1.547 3.978 3.596 4.39a4.524 4.524 0 0 1-2.022.077c.571 1.782 2.222 3.084 4.183 3.118a8.96 8.96 0 0 1-5.556 1.916c-.36 0-.71-.022-1.05-.064a12.72 12.72 0 0 0 6.945 2.036c8.337 0 12.87-6.914 12.87-12.87 0-.196-.004-.39-.013-.585A9.13 9.13 0 0 0 22.254 5.923z"></path>
                    </svg>
                    <span>@siriihgroups (X / Twitter)</span>
                </a>
            </div>
        </div>
    </div>
</body>
</html>


