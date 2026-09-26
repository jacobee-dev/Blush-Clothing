# Blush-Clothing

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blush Mini Clothing Store</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: #ffeef5;
            color: #4a343b;
            line-height: 1.6;
        }

        /* Navigation */
        header {
            background: #ffffff;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 25px;
            font-weight: bold;
            color: #c75b7a;
        }

        .logo i {
            margin-right: 7px;
        }

        nav a {
            text-decoration: none;
            color: #4a343b;
            margin-left: 20px;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
        }

        nav a:hover {
            color: #d85f83;
        }

        /* Pages */
        .page {
            display: none;
            min-height: 90vh;
            padding: 60px 8%;
        }

        .page.active {
            display: block;
        }

        /* Home */
        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 40px;
            max-width: 1100px;
            margin: auto;
        }

        .hero-text {
            flex: 1;
        }

        .hero-text h1 {
            font-family: 'Playfair Display', serif;
            font-size: 52px;
            color: #b94d6d;
            margin-bottom: 15px;
        }

        .hero-text h2 {
            font-size: 20px;
            margin-bottom: 15px;
            color: #704752;
        }

        .hero-text p {
            max-width: 550px;
            margin-bottom: 25px;
            color: #685158;
        }

        .btn {
            display: inline-block;
            background: #d65f82;
            color: white;
            padding: 12px 25px;
            border-radius: 25px;
            text-decoration: none;
            border: none;
            cursor: pointer;
            font-family: 'Poppins', sans-serif;
            transition: 0.3s;
        }

        .btn:hover {
            background: #b94d6d;
            transform: translateY(-2px);
        }

        /* Clothing Image */
        .hero-image {
            flex: 1;
            text-align: center;
        }

        .hero-image img {
            width: 100%;
            max-width: 430px;
            height: 430px;
            object-fit: cover;
            border-radius: 30px;
            box-shadow: 0 10px 30px rgba(150, 70, 95, 0.2);
        }

        /* Features */
        .features {
            max-width: 1100px;
            margin: 60px auto 0;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .feature-card {
            background: white;
            padding: 25px;
            text-align: center;
            border-radius: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.06);
        }

        .feature-card i {
            font-size: 30px;
            color: #d65f82;
            margin-bottom: 12px;
        }

        .feature-card h3 {
            font-family: 'Playfair Display', serif;
            margin-bottom: 8px;
            color: #a94766;
        }

        /* General Section */
        .content-box {
            background: white;
            max-width: 850px;
            margin: auto;
            padding: 45px;
            border-radius: 25px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.07);
        }

        .content-box h1 {
            font-family: 'Playfair Display', serif;
            text-align: center;
            color: #b94d6d;
            font-size: 40px;
            margin-bottom: 20px;
        }

        .content-box h2 {
            color: #c05272;
            margin-top: 25px;
            margin-bottom: 8px;
        }

        .content-box i {
            color: #d65f82;
            margin-right: 8px;
        }

        /* Contact Form */
        .contact-container {
            max-width: 650px;
            margin: auto;
        }

        form {
            margin-top: 25px;
        }

        label {
            display: block;
            margin-bottom: 7px;
            font-weight: 500;
        }

        input,
        textarea {
            width: 100%;
            padding: 13px 15px;
            border: 1px solid #e4b7c5;
            border-radius: 12px;
            margin-bottom: 18px;
            font-family: 'Poppins', sans-serif;
            outline: none;
            background: #fffafd;
        }

        input:focus,
        textarea:focus {
            border-color: #d65f82;
            box-shadow: 0 0 5px rgba(214,95,130,0.2);
        }

        textarea {
            height: 140px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #c75b7a;
            color: white;
            text-align: center;
            padding: 18px;
            font-size: 13px;
        }

        footer i {
            margin: 0 7px;
        }

        /* Mobile */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 10px;
            }

            nav a {
                margin: 0 7px;
                font-size: 13px;
            }

            .hero {
                flex-direction: column;
                text-align: center;
            }

            .hero-text h1 {
                font-size: 40px;
            }

            .hero-text p {
                margin-left: auto;
                margin-right: auto;
            }

            .hero-image img {
                height: 320px;
            }

            .features {
                grid-template-columns: 1fr;
            }

            .content-box {
                padding: 25px;
            }

            .content-box h1 {
                font-size: 32px;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->
    <header>
        <div class="logo">
            <i class="fa-solid fa-shirt"></i>
            Blush Mini
        </div>

        <nav>
            <a onclick="showPage('home')">
                <i class="fa-solid fa-house"></i> Home
            </a>

            <a onclick="showPage('privacy')">
                <i class="fa-solid fa-lock"></i> Privacy
            </a>

            <a onclick="showPage('contact')">
                <i class="fa-solid fa-envelope"></i> Contact
            </a>
        </nav>
    </header>


    <!-- PAGE 1: HOME -->
    <section id="home" class="page active">

        <div class="hero">

            <div class="hero-text">
                <h1>Blush Mini</h1>

                <h2>
                    <i class="fa-solid fa-heart"></i>
                    Simple Clothes, Pretty Style
                </h2>

                <p>
                    Welcome to Blush Mini, a small clothing store made for
                    people who love simple, cute, and comfortable fashion.
                    We offer stylish clothing pieces that are easy to wear
                    and perfect for everyday outfits.
                </p>

                <p>
                    Our goal is to provide affordable and fashionable clothes
                    while giving our customers a simple and enjoyable shopping
                    experience.
                </p>

                <button class="btn" onclick="showPage('contact')">
                    <i class="fa-solid fa-paper-plane"></i>
                    Contact Us
                </button>
            </div>

            <div class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=800&q=80"
                    alt="Fashionable clothing"
                >
            </div>

        </div>


        <!-- Store Features -->
        <div class="features">

            <div class="feature-card">
                <i class="fa-solid fa-shirt"></i>
                <h3>Trendy Clothes</h3>
                <p>
                    Simple and fashionable pieces for everyday style.
                </p>
            </div>

            <div class="feature-card">
                <i class="fa-solid fa-heart"></i>
                <h3>Made With Love</h3>
                <p>
                    We choose clothing that our customers can enjoy wearing.
                </p>
            </div>

            <div class="feature-card">
                <i class="fa-solid fa-tags"></i>
                <h3>Affordable</h3>
                <p>
                    Cute and stylish clothing at friendly prices.
                </p>
            </div>

        </div>

    </section>


    <!-- PAGE 2: PRIVACY -->
    <section id="privacy" class="page">

        <div class="content-box">

            <h1>
                <i class="fa-solid fa-shield-halved"></i>
                Privacy Statement
            </h1>

            <p>
                At Blush Mini, we respect your privacy. This website is
                designed as a simple clothing store website and does not
                use cookies or user tracking.
            </p>

            <h2>
                <i class="fa-solid fa-database"></i>
                Information We Collect
            </h2>

            <p>
                The contact form may ask for your name, email address,
                and message. This information is only provided when you
                choose to enter it in the form.
            </p>

            <h2>
                <i class="fa-solid fa-cookie-bite"></i>
                Cookies and Tracking
            </h2>

            <p>
                This website does not use tracking cookies, advertising
                trackers, or analytics tools to monitor your activity.
            </p>

            <h2>
                <i class="fa-solid fa-lock"></i>
                Your Privacy
            </h2>

            <p>
                We aim to keep the information you provide private and
                only use it for communication related to your message.
                Please avoid submitting sensitive personal information
                through the contact form.
            </p>

        </div>

    </section>


    <!-- PAGE 3: CONTACT -->
    <section id="contact" class="page">

        <div class="content-box contact-container">

            <h1>
                <i class="fa-solid fa-comments"></i>
                Contact Us
            </h1>

            <p style="text-align:center;">
                Have a question about our clothing store?
                Send us a message!
            </p>

            <form onsubmit="sendMessage(event)">

                <label for="name">
                    <i class="fa-solid fa-user"></i>
                    Name
                </label>

                <input
                    type="text"
                    id="name"
                    placeholder="Enter your name"
                    required
                >


                <label for="email">
                    <i class="fa-solid fa-envelope"></i>
                    Email
                </label>

                <input
                    type="email"
                    id="email"
                    placeholder="Enter your email"
                    required
                >


                <label for="message">
                    <i class="fa-solid fa-message"></i>
                    Message
                </label>

                <textarea
                    id="message"
                    placeholder="Write your message here..."
                    required
                ></textarea>


                <button type="submit" class="btn">
                    <i class="fa-solid fa-paper-plane"></i>
                    Send Message
                </button>

            </form>

        </div>

    </section>


    <!-- Footer -->
    <footer>
        <p>
            <i class="fa-solid fa-shirt"></i>
            © 2026 Blush Mini Clothing Store
            <i class="fa-solid fa-heart"></i>
        </p>
    </footer>


    <!-- JavaScript -->
    <script>

        function showPage(pageId) {

            // Hide all pages
            const pages = document.querySelectorAll('.page');

            pages.forEach(function(page) {
                page.classList.remove('active');
            });

            // Show selected page
            document.getElementById(pageId).classList.add('active');

            // Scroll to top
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }


        function sendMessage(event) {

            event.preventDefault();

            const name = document.getElementById('name').value;

            alert(
                "Thank you, " + name +
                "! Your message has been received."
            );

            // Clear the form
            event.target.reset();
        }

    </script>

</body>
</html>