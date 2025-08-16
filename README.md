# Edward-sales-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Build Your AI Marketing Agency in 48 Hours</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: #0a0a0a;
            color: #ffffff;
            line-height: 1.6;
        }

        /* Container */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(ellipse at center, rgba(255,215,0,0.1) 0%, transparent 70%);
            pointer-events: none;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            width: 100%;
        }

        .preheader {
            font-size: 0.9rem;
            color: #ffd700;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .hero-headline {
            font-size: clamp(2.5rem, 6vw, 4.5rem);
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, #ffffff 0%, #ffd700 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subheader {
            font-size: clamp(1.1rem, 2.5vw, 1.4rem);
            color: #cccccc;
            max-width: 70rem;
            margin: 0 auto 3rem;
            line-height: 1.5;
        }

        .vsl-container {
            margin: 3rem 0;
        }

        .vsl-icon {
            position: relative;
            display: inline-block;
            cursor: pointer;
            transition: transform 0.3s ease;
            text-decoration: none;
        }

        .vsl-icon:hover {
            transform: scale(1.05);
        }

        .vsl-thumbnail {
            width: 16rem;
            height: 9rem;
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
            border: 2px solid #ffd700;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .play-button {
            width: 4rem;
            height: 4rem;
            background: linear-gradient(135deg, #ffd700 0%, #ffed4a 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 20px rgba(255,215,0,0.3);
        }

        .play-button::after {
            content: '';
            width: 0;
            height: 0;
            border-left: 16px solid #0a0a0a;
            border-top: 10px solid transparent;
            border-bottom: 10px solid transparent;
            margin-left: 4px;
        }

        .vsl-text {
            color: #ffd700;
            font-size: 1rem;
            font-weight: 600;
            margin-top: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-primary {
            display: inline-block;
            background: linear-gradient(135deg, #ffd700 0%, #ffed4a 100%);
            color: #0a0a0a;
            padding: 1.2rem 3rem;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            border-radius: 8px;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 20px rgba(255,215,0,0.3);
            margin-top: 2rem;
        }

        .cta-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(255,215,0,0.5);
        }

        /* Section Styling */
        .section {
            padding: 6rem 0;
            border-top: 1px solid #2a2a2a;
        }

        .section-headline {
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 800;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, #ffffff 0%, #ffd700 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .content-block {
            max-width: 50rem;
            margin: 0 auto;
            font-size: 1.1rem;
            line-height: 1.8;
            color: #e0e0e0;
        }

        .content-block p {
            margin-bottom: 1.5rem;
        }

        .content-block strong {
            color: #ffd700;
            font-weight: 700;
        }

        .bullets-list {
            list-style: none;
            margin: 2rem 0;
        }

        .bullets-list li {
            padding: 1rem 0;
            border-bottom: 1px solid #2a2a2a;
            font-size: 1.1rem;
            line-height: 1.6;
        }

        .bullets-list li:last-child {
            border-bottom: none;
        }

        .feature {
            color: #ffd700;
            font-weight: 700;
        }

        .offer-box {
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
            border: 2px solid #ffd700;
            border-radius: 16px;
            padding: 3rem;
            text-align: center;
            margin: 3rem auto;
            max-width: 40rem;
            box-shadow: 0 8px 40px rgba(0,0,0,0.3);
        }

        .price {
            font-size: 3rem;
            font-weight: 900;
            color: #ffd700;
            margin: 1rem 0;
        }

        .guarantee {
            background: #2a2a2a;
            padding: 1.5rem;
            border-radius: 12px;
            margin: 2rem 0;
            border-left: 4px solid #ffd700;
        }

        .faq-item {
            background: #1a1a1a;
            border-radius: 12px;
            padding: 2rem;
            margin: 1.5rem 0;
            border-left: 4px solid #ffd700;
        }

        .faq-question {
            font-size: 1.2rem;
            font-weight: 700;
            color: #ffd700;
            margin-bottom: 1rem;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .container {
                padding: 0 1.5rem;
            }
            
            .hero {
                padding: 2rem 0;
            }
            
            .section {
                padding: 4rem 0;
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 0 1rem;
            }
            
            .hero-headline {
                font-size: 2.5rem;
            }
            
            .vsl-thumbnail {
                width: 12rem;
                height: 7rem;
            }
            
            .play-button {
                width: 3rem;
                height: 3rem;
            }
            
            .cta-primary {
                padding: 1rem 2rem;
                font-size: 1rem;
            }
            
            .offer-box {
                padding: 2rem 1.5rem;
            }
            
            .section {
                padding: 3rem 0;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in-up {
            animation: fadeInUp 0.8s ease-out;
        }
    </style>
</head>
<body>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="container">
            <div class="hero-content fade-in-up">
                <div class="preheader">For Ambitious Entrepreneurs Ready To Scale</div>
                
                <h1 class="hero-headline">
                    Get A Complete AI Marketing Agency Built For You In Just 48 Hours
                </h1>
                
                <p class="hero-subheader">
                    Skip months of setup frustration and technical headaches. Our team builds your entire AI-powered marketing agency infrastructure over one weekend — complete with client acquisition systems, automated fulfillment, and everything you need to start closing $1,500-$2,500/month retainer clients immediately.
                </p>
                
                <div class="vsl-container">
                    <a href="https://docs.google.com/document/d/1ZUyquyL0fr5O2K4-K4Xk5p3Ik82VB5vjVBbAg-Lx4cA/edit?usp=sharing" class="vsl-icon" target="_blank">
                        <div class="vsl-thumbnail">
                            <div class="play-button"></div>
                        </div>
                        <div class="vsl-text">Click Here To See The: VSL I WROTE FOR YOU</div>
                    </a>
                </div>
                
                <a href="#offer" class="cta-primary">CLAIM YOUR AGENCY SETUP NOW</a>
            </div>
        </div>
    </section>

    <!-- PROBLEM IDENTIFICATION -->
    <section class="section">
        <div class="container">
            <h2 class="section-headline">
                You're One Weekend Away From Financial Freedom... But Here's What's Really Holding You Back
            </h2>
            
            <div class="content-block">
                <p>You've seen the success stories. Six-figure agency owners. Seven-figure entrepreneurs. All building massive businesses with AI and automation.</p>
                
                <p>But every time you try to start your own agency, you hit the same brick walls...</p>
                
                <p><strong>The endless technical setup.</strong> Choosing tools, integrating systems, building funnels, creating processes. Weeks turn into months and you're still not ready to take on a single client.</p>
                
                <p><strong>The client acquisition nightmare.</strong> How do you even find businesses that need AI marketing? What do you charge? How do you prove you can deliver results when you're just starting?</p>
                
                <p><strong>The fulfillment overwhelm.</strong> Even if you land a client, how do you actually deliver the work without working 80-hour weeks?</p>
                
                <p>Meanwhile, every day you delay is another day your competitors get ahead. Another day you stay stuck in the same income bracket. Another day you watch others build the business you know you could run better.</p>
                
                <p>The truth is, <strong>most people never launch their agency because they get lost in the setup</strong>. They spend months trying to figure out systems that should take hours to implement.</p>
                
                <p>But what if there was a way to skip all of that?</p>
            </div>
        </div>
    </section>

    <!-- ORIGIN STORY -->
    <section class="section">
        <div class="container">
            <h2 class="section-headline">
                How A $700K Month Revealed The Agency Setup Secret Nobody's Talking About
            </h2>
            
            <div class="content-block">
                <p>Three years ago, I was exactly where you are right now.</p>
                
                <p>I knew AI was the future. I could see the opportunity. But every time I tried to build my own marketing agency, I'd get stuck in the same cycle...</p>
                
                <p>Spend weeks researching tools. Try to build funnels. Attempt to create systems. Get overwhelmed. Give up. Repeat.</p>
                
                <p>Then I met Edward Air.</p>
                
                <p>Edward had just closed a <strong>$700,000 month</strong> with his AI marketing agency. But here's the thing that shocked me...</p>
                
                <p><strong>He wasn't a technical genius.</strong> He wasn't some coding wizard or marketing mastermind.</p>
                
                <p>What he had was something different. A complete system. Built once, duplicated endlessly.</p>
                
                <p>While everyone else was trying to build their agency from scratch, Edward had cracked the code on <strong>instant infrastructure</strong>. His team could take someone with zero experience and have them ready to close clients in under 48 hours.</p>
                
                <p>The secret? <strong>Stop building. Start duplicating.</strong></p>
                
                <p>Why spend months creating systems when you can copy ones that are already generating millions?</p>
            </div>
        </div>
    </section>

    <!-- SOLUTION REVELATION -->
    <section class="section">
        <div class="container">
            <h2 class="section-headline">
                The "Weekend Agency Method" That's Generated Over $15 Million In Client Results
            </h2>
            
            <div class="content-block">
                <p>Here's how it works...</p>
                
                <p><strong>Friday evening:</strong> You purchase the AIMA Accelerator. Edward's team receives your information and begins building your agency infrastructure.</p>
                
                <p><strong>Saturday:</strong> While you sleep, our team installs your client acquisition systems, sets up your automated fulfillment processes, and configures your entire sales pipeline.</p>
                
                <p><strong>Sunday:</strong> You receive your complete agency setup. Ready to prospect. Ready to close. Ready to deliver.</p>
                
                <p><strong>Monday morning:</strong> You're taking sales calls.</p>
                
                <p>This isn't some generic template. This is the <strong>exact same infrastructure</strong> that's generated over $15 million in client results.</p>
                
                <p>The same AI-powered acquisition systems. The same automated fulfillment processes. The same retention frameworks that keep clients paying month after month.</p>
                
                <p>But here's the best part...</p>
                
                <ul class="bullets-list">
                    <li><span class="feature">Client Acquisition on Autopilot:</span> AI-powered prospecting systems that identify and reach out to your ideal clients while you sleep, so you wake up to booked discovery calls instead of empty calendars.</li>
                    
                    <li><span class="feature">90%+ Client Retention Framework:</span> Automated systems that deliver consistent results and keep clients happy for years, so you build predictable recurring revenue instead of constantly chasing new business.</li>
                    
                    <li><span class="feature">Done-For-You Fulfillment Systems:</span> Complete automation that handles 80% of client work without you lifting a finger, so you can serve dozens of clients without working 80-hour weeks.</li>
                    
                    <li><span class="feature">Proven Sales Scripts & Processes:</span> Word-for-word conversations that close $2,500/month retainers consistently, so you never have to guess what to say on sales calls again.</li>
                    
                    <li><span class="feature">Premium Positioning Framework:</span> Position yourself as the AI expert in your market immediately, so clients see you as the obvious choice instead of just another service provider.</li>
                </ul>
                
                <p>This is everything you need to start, scale, and automate a six-figure AI marketing agency.</p>
                
                <p>Built in 48 hours. Ready to profit immediately.</p>
            </div>
        </div>
    </section>

    <!-- PRODUCT INTRODUCTION -->
    <section class="section">
        <div class="container">
            <h2 class="section-headline">
                Introducing The AIMA Accelerator: Your Complete Agency In A Box
            </h2>
            
            <div class="content-block">
                <p>This is not a course. This is not coaching. This is not another "figure it out yourself" program.</p>
                
                <p><strong>This is your agency. Built for you. Ready to profit.</strong></p>
                
                <p>Think about what you're getting here...</p>
                
                <p>If you hired a team to build this for you, you'd pay at least $25,000. If you tried to build it yourself, it would take 6-12 months (if you ever finished at all).</p>
                
                <p>But because Edward's team has built this system hundreds of times, they can deliver it to you in 48 hours.</p>
                
                <p>Same results. Same infrastructure. Same profit potential.</p>
                
                <p>The only difference? <strong>You're not starting from scratch.</strong></p>
                
                <p>While your competitors spend the next year trying to figure out client acquisition, you'll already be closing $2,500/month retainers.</p>
                
                <p>While they struggle with fulfillment, your automated systems will be delivering results on autopilot.</p>
                
                <p>While they burn out trying to do everything manually, you'll be scaling with AI and automation.</p>
            </div>
        </div>
    </section>

    <!-- OFFER STRUCTURE -->
    <section class="section" id="offer">
        <div class="container">
            <h2 class="section-headline">
                Get Your Complete AI Agency Built This Weekend
            </h2>
            
            <div class="offer-box">
                <h3 style="font-size: 2rem; margin-bottom: 1rem; color: #ffd700;">The AIMA Accelerator</h3>
                <p style="font-size: 1.2rem; margin-bottom: 2rem; color: #cccccc;">Your Complete AI Marketing Agency Setup</p>
                
                <div class="price">$37</div>
                
                <ul class="bullets-list" style="text-align: left; max-width: 30rem; margin: 2rem auto;">
                    <li>Complete AI agency infrastructure built in 48 hours</li>
                    <li>Automated client acquisition systems installed</li>
                    <li>90%+ retention fulfillment processes configured</li>
                    <li>Proven sales scripts and closing frameworks</li>
                    <li>Premium positioning and branding setup</li>
                    <li>Ready-to-use proposals and pricing structure</li>
                </ul>
                
                <div class="guarantee">
                    <strong style="color: #ffd700;">2-Year Money-Back Guarantee</strong><br>
                    If your agency setup doesn't help you book qualified sales calls within 30 days, or if you're not completely satisfied for any reason within 2 full years, we'll refund every penny. No questions asked.
                </div>
                
                <a href="#" class="cta-primary" style="margin-top: 2rem; display: inline-block;">GET THE AIMA ACCELERATOR NOW - $37</a>
                
                <p style="color: #ffd700; margin-top: 1rem; font-size: 0.9rem;">⚡ Limited Time: Only 50 setups available this month</p>
            </div>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <section class="section">
        <div class="container">
            <h2 class="section-headline">
                Everything You Need To Know Before You Start Your Weekend Agency Build
            </h2>
            
            <div class="faq-item">
                <div class="faq-question">This sounds too good to be true. How can you build a complete agency for just $37?</div>
                <p>Here's the honest truth: Edward's team has built this system hundreds of times. What takes most people 6-12 months to figure out, they can duplicate in 48 hours. The $37 covers the setup and gives you access to systems that have generated millions. Think of it like buying a franchise for the price of a dinner.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">Will this actually work for someone with no experience?</div>
                <p>That's exactly who this works best for. Experienced marketers often have bad habits and outdated strategies. You get to start with a proven system that's already generating results. Plus, most clients don't care about your experience — they care about results. And this system delivers results.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">What if I can't close clients right away?</div>
                <p>The system includes proven sales scripts, objection handling frameworks, and positioning strategies. If you follow the process, you will book qualified calls. But if for any reason you're not booking calls within 30 days, you get your money back. No questions asked.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">How is this different from other agency programs?</div>
                <p>Other programs teach you how to build an agency. This IS your agency. Built, configured, and ready to profit. Instead of spending months learning, you spend weekend implementing. Instead of guessing what works, you get systems that are already proven.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">What kind of results can I realistically expect?</div>
                <p>Conservative estimate: 2-5 clients at $1,500-$2,500/month within 90 days. That's $3,000-$12,500 monthly recurring revenue. Many of our agency owners hit $10K+ months within 60 days. The system is designed for scale, so your income grows as you add more clients.</p>
            </div>
            
            <div style="text-align: center; margin-top: 4rem;">
                <a href="#" class="cta-primary">CLAIM YOUR AGENCY SETUP - $37</a>
                <p style="color: #cccccc; margin-top: 1rem;">Join 500+ entrepreneurs who've built profitable AI agencies this month</p>
            </div>
        </div>
    </section>

    <script>
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
                }
            });
        });

        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all sections for animation
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'all 0.8s ease-out';
            observer.observe(section);
        });
    </script>

</body>
</html>
