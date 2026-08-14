<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>POSE | Modern Fashion & Beauty</title>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;800&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- CSS VARIABLES & THEME (PURPLE PALETTE) --- */
        :root {
            --primary: #6B21A8;          /* Rich Deep Purple */
            --primary-light: #8B5CF6;    /* Vibrant Accent Purple */
            --primary-dark: #4C1D95;     /* Dark Purple for Hover */
            --secondary: #F3E8FF;        /* Soft Lavender Background */
            --accent-pink: #EC4899;      /* Hot Pink Highlight */
            --text-dark: #1F2937;        /* Main Text */
            --text-muted: #6B7280;       /* Subtitles */
            --white: #FFFFFF;
            --shadow: 0 4px 20px rgba(107, 33, 168, 0.08);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: #FAF5FF;
            color: var(--text-dark);
        }

        /* --- TOP BANNER --- */
        .top-bar {
            background: linear-gradient(90deg, var(--primary-dark), var(--primary-light));
            color: var(--white);
            text-align: center;
            padding: 8px 0;
            font-size: 13px;
            font-weight: 500;
            letter-spacing: 0.5px;
        }

        /* --- HEADER & NAVIGATION --- */
        header {
            background: var(--white);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 15px 20px;
        }

        .brand-logo {
            font-family: 'Playfair Display', serif;
            font-size: 32px;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            letter-spacing: 2px;
        }

        .brand-logo span {
            color: var(--accent-pink);
        }

        .search-bar {
            flex: 0 1 450px;
            position: relative;
        }

        .search-bar input {
            width: 100%;
            padding: 10px 40px 10px 15px;
            border-radius: 20px;
            border: 1px solid #E9D5FF;
            background-color: #FAF5FF;
            outline: none;
            transition: var(--transition);
        }

        .search-bar input:focus {
            border-color: var(--primary-light);
            box-shadow: 0 0 0 3px rgba(139, 92, 246, 0.2);
        }

        .search-bar i {
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--primary);
        }

        .header-icons {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .icon-btn {
            background: none;
            border: none;
            font-size: 18px;
            color: var(--text-dark);
            cursor: pointer;
            position: relative;
            transition: var(--transition);
        }

        .icon-btn:hover {
            color: var(--primary);
        }

        .badge {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--accent-pink);
            color: var(--white);
            font-size: 10px;
            font-weight: 700;
            padding: 2px 6px;
            border-radius: 10px;
        }

        /* --- CATEGORY NAVIGATION --- */
        nav {
            border-top: 1px solid #F3E8FF;
            background: var(--white);
        }

        .nav-links {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 30px;
            padding: 12px 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-size: 14px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: var(--transition);
        }

        .nav-links a:hover, .nav-links a.active {
            color: var(--primary);
        }

        /* --- HERO BANNER (SLIDER) --- */
        .hero-banner {
            background: linear-gradient(135deg, #F3E8FF 0%, #E9D5FF 100%);
            padding: 60px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-title {
            font-family: 'Playfair Display', serif;
            font-size: 48px;
            color: var(--primary-dark);
            margin-bottom: 15px;
        }

        .hero-subtitle {
            font-size: 18px;
            color: var(--text-muted);
            margin-bottom: 25px;
        }

        .btn-primary {
            background-color: var(--primary);
            color: var(--white);
            padding: 12px 30px;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(107, 33, 168, 0.3);
        }

        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        /* --- CATEGORY CIRCLES --- */
        .categories-section {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            color: var(--primary-dark);
            margin-bottom: 30px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: var(--accent-pink);
            margin: 8px auto 0;
            border-radius: 2px;
        }

        .circle-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
            gap: 20px;
            text-align: center;
        }

        .circle-item img {
            width: 110px;
            height: 110px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary-light);
            padding: 3px;
            transition: var(--transition);
            cursor: pointer;
        }

        .circle-item img:hover {
            transform: scale(1.05);
            border-color: var(--accent-pink);
        }

        .circle-item p {
            margin-top: 10px;
            font-weight: 600;
            font-size: 14px;
        }

        /* --- PRODUCT GRID (NYKAA STYLE CARDS) --- */
        .products-section {
            max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: var(--white);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-card:hover {
            transform: translateY(-50px 0 0);
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(107, 33, 168, 0.15);
        }

        .product-image {
            position: relative;
            width: 100%;
            height: 280px;
            overflow: hidden;
        }

        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .wishlist-btn {
            position: absolute;
            top: 12px;
            right: 12px;
            background: var(--white);
            border: none;
            width: 32px;
            height: 32px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-muted);
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .wishlist-btn:hover {
            color: var(--accent-pink);
        }

        .product-info {
            padding: 15px;
            text-align: left;
        }

        .brand-name {
            font-size: 12px;
            font-weight: 700;
            color: var(--primary);
            text-transform: uppercase;
        }

        .product-title {
            font-size: 14px;
            font-weight: 500;
            margin: 5px 0 10px;
            color: var(--text-dark);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .price-container {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 12px;
        }

        .current-price {
            font-size: 16px;
            font-weight: 700;
            color: var(--text-dark);
        }

        .original-price {
            font-size: 13px;
            color: var(--text-muted);
            text-decoration: line-through;
        }

        .discount {
            font-size: 12px;
            color: var(--accent-pink);
            font-weight: 600;
        }

        .add-to-cart-btn {
            width: 100%;
            background-color: var(--secondary);
            color: var(--primary-dark);
            border: 1px solid var(--primary-light);
            padding: 10px;
            font-weight: 600;
            cursor: pointer;
            border-radius: 0 0 12px 12px;
            transition: var(--transition);
        }

        .add-to-cart-btn:hover {
            background-color: var(--primary);
            color: var(--white);
        }

        /* --- PROMO BANNER --- */
        .promo-banner {
            max-width: 1200px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .promo-box {
            background: linear-gradient(90deg, var(--primary) 0%, var(--primary-light) 100%);
            border-radius: 16px;
            color: var(--white);
            padding: 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .promo-text h2 {
            font-family: 'Playfair Display', serif;
            font-size: 32px;
            margin-bottom: 10px;
        }

        .btn-light {
            background-color: var(--white);
            color: var(--primary);
            padding: 10px 25px;
            border-radius: 20px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }

        .btn-light:hover {
            background-color: var(--secondary);
        }

        /* --- FOOTER --- */
        footer {
            background-color: #2E1065;
            color: #E9D5FF;
            padding: 60px 0 20px;
            margin-top: 60px;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            padding: 0 20px 40px;
            border-bottom: 1px solid #4C1D95;
        }

        .footer-col h4 {
            color: var(--white);
            font-size: 16px;
            margin-bottom: 20px;
            position: relative;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a {
            color: #D8B4FE;
            text-decoration: none;
            font-size: 14px;
            transition: var(--transition);
        }

        .footer-col ul li a:hover {
            color: var(--white);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            font-size: 13px;
            color: #A855F7;
        }

        /* --- RESPONSIVE DESIGN --- */
        @media (max-width: 768px) {
            .header-container {
                flex-wrap: wrap;
                gap: 15px;
            }
            .search-bar {
                order: 3;
                flex: 1 1 100%;
            }
            .nav-links {
                overflow-x: auto;
                justify-content: flex-start;
                white-space: nowrap;
            }
            .hero-title {
                font-size: 32px;
            }
            .promo-box {
                flex-direction: column;
                text-align: center;
                gap: 20px;
            }
        }
    </style>
</head>
<body>

    <!-- TOP ANNOUNCEMENT BAR -->
    <div class="top-bar">
        ✨ GRAND LAUNCH SALE: Extra 20% OFF on First Orders | Code: <b>POSEFIRST</b>
    </div>

    <!-- HEADER -->
    <header>
        <div class="header-container">
            <a href="#" class="brand-logo">POSE<span>.</span></a>
            
            <div class="search-bar">
                <input type="text" placeholder="Search dresses, makeup, luxury brands...">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>

            <div class="header-icons">
                <button class="icon-btn" title="Account">
                    <i class="fa-regular fa-user"></i>
                </button>
                <button class="icon-btn" title="Wishlist">
                    <i class="fa-regular fa-heart"></i>
                    <span class="badge">3</span>
                </button>
                <button class="icon-btn" title="Bag">
                    <i class="fa-solid fa-bag-shopping"></i>
                    <span class="badge" id="cart-count">0</span>
                </button>
            </div>
        </div>

        <!-- CATEGORY NAVIGATION -->
        <nav>
            <ul class="nav-links">
                <li><a href="#" class="active">New Arrivals</a></li>
                <li><a href="#">Western Wear</a></li>
                <li><a href="#">Ethnic Elegance</a></li>
                <li><a href="#">Beauty & Makeup</a></li>
                <li><a href="#">Luxe Edit</a></li>
                <li><a href="#">Footwear</a></li>
                <li><a href="#">Offers</a></li>
            </ul>
        </nav>
    </header>

    <!-- HERO BANNER -->
    <section class="hero-banner">
        <div class="hero-content">
            <h1 class="hero-title">Unveil Your Signature Look</h1>
            <p class="hero-subtitle">Discover the finest curated collections in runway fashion and premium cosmetics.</p>
            <a href="#shop-now" class="btn-primary">Explore Collection</a>
        </div>
    </section>

    <!-- CATEGORIES SECTION -->
    <section class="categories-section">
        <h2 class="section-title">Shop By Category</h2>
        <div class="circle-grid">
            <div class="circle-item">
                <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=300&q=80" alt="Dresses">
                <p>Dresses</p>
            </div>
            <div class="circle-item">
                <img src="https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?auto=format&fit=crop&w=300&q=80" alt="Makeup">
                <p>Cosmetics</p>
            </div>
            <div class="circle-item">
                <img src="https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=300&q=80" alt="Handbags">
                <p>Handbags</p>
            </div>
            <div class="circle-item">
                <img src="https://images.unsplash.com/photo-1543163521-1bf539c55dd2?auto=format&fit=crop&w=300&q=80" alt="Footwear">
                <p>Heels</p>
            </div>
            <div class="circle-item">
                <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?auto=format&fit=crop&w=300&q=80" alt="Jewelry">
                <p>Jewelry</p>
            </div>
        </div>
    </section>

    <!-- FEATURED PRODUCTS SECTION -->
    <section class="products-section" id="shop-now">
        <h2 class="section-title">Trending Now</h2>
        <div class="product-grid">

            <!-- Card 1 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=500&q=80" alt="Product">
                    <button class="wishlist-btn"><i class="fa-regular fa-heart"></i></button>
                </div>
                <div class="product-info">
                    <span class="brand-name">POSE LUXE</span>
                    <h3 class="product-title">Velvet Evening Gown</h3>
                    <div class="price-container">
                        <span class="current-price">$89</span>
                        <span class="original-price">$120</span>
                        <span class="discount">(25% OFF)</span>
                    </div>
                </div>
                <button class="add-to-cart-btn" onclick="addToCart()">Add to Bag</button>
            </div>

            <!-- Card 2 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1586495777744-4413f21062fa?auto=format&fit=crop&w=500&q=80" alt="Product">
                    <button class="wishlist-btn"><i class="fa-regular fa-heart"></i></button>
                </div>
                <div class="product-info">
                    <span class="brand-name">GLAM GLOW</span>
                    <h3 class="product-title">Matte Velvet Lipstick - Plum</h3>
                    <div class="price-container">
                        <span class="current-price">$24</span>
                        <span class="original-price">$30</span>
                        <span class="discount">(20% OFF)</span>
                    </div>
                </div>
                <button class="add-to-cart-btn" onclick="addToCart()">Add to Bag</button>
            </div>

            <!-- Card 3 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1509631179647-0177331693ae?auto=format&fit=crop&w=500&q=80" alt="Product">
                    <button class="wishlist-btn"><i class="fa-regular fa-heart"></i></button>
                </div>
                <div class="product-info">
                    <span class="brand-name">URBAN POSE</span>
                    <h3 class="product-title">Classic Silk Blazer - Lilac</h3>
                    <div class="price-container">
                        <span class="current-price">$110</span>
                        <span class="original-price">$150</span>
                        <span class="discount">(26% OFF)</span>
                    </div>
                </div>
                <button class="add-to-cart-btn" onclick="addToCart()">Add to Bag</button>
            </div>

            <!-- Card 4 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796?auto=format&fit=crop&w=500&q=80" alt="Product">
                    <button class="wishlist-btn"><i class="fa-regular fa-heart"></i></button>
                </div>
                <div class="product-info">
                    <span class="brand-name">AURA BEAUTY</span>
                    <h3 class="product-title">Radiance Eyeshadow Palette</h3>
                    <div class="price-container">
                        <span class="current-price">$45</span>
                        <span class="original-price">$55</span>
                        <span class="discount">(18% OFF)</span>
                    </div>
                </div>
                <button class="add-to-cart-btn" onclick="addToCart()">Add to Bag</button>
            </div>

        </div>
    </section>

    <!-- PROMOTIONAL BANNER -->
    <section class="promo-banner">
        <div class="promo-box">
            <div class="promo-text">
                <h2>The Purple Carpet Sale</h2>
                <p>Up to 60% OFF on top designer brands and luxury skincare items.</p>
            </div>
            <a href="#" class="btn-light">Explore Offers</a>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <a href="#" class="brand-logo" style="color: var(--white);">POSE<span>.</span></a>
                <p style="margin-top: 15px; font-size: 13px;">Your ultimate destination for fashion, lifestyle, and beauty essentials.</p>
            </div>
            <div class="footer-col">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Store Locator</a></li>
                    <li><a href="#">POSE Journal</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Help & Support</h4>
                <ul>
                    <li><a href="#">Shipping & Returns</a></li>
                    <li><a href="#">Track Order</a></li>
                    <li><a href="#">FAQs</a></li>
                    <li><a href="#">Contact Us</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Connect With Us</h4>
                <div style="display: flex; gap: 15px; font-size: 18px; margin-top: 10px;">
                    <a href="#" style="color: white;"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#" style="color: white;"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#" style="color: white;"><i class="fa-brands fa-pinterest"></i></a>
                    <a href="#" style="color: white;"><i class="fa-brands fa-youtube"></i></a>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2026 POSE Fashion & Beauty Network. All Rights Reserved.
        </div>
    </footer>

    <!-- INTERACTIVITY JAVASCRIPT -->
    <script>
        let cartCount = 0;

        function addToCart() {
            cartCount++;
            document.getElementById('cart-count').innerText = cartCount;
            
            // Temporary feedback effect
            const cartBadge = document.getElementById('cart-count');
            cartBadge.style.transform = 'scale(1.4)';
            setTimeout(() => {
                cartBadge.style.transform = 'scale(1)';
            }, 200);
        }

        // Wishlist Toggle Logic
        document.querySelectorAll('.wishlist-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const icon = this.querySelector('i');
                if (icon.classList.contains('fa-regular')) {
                    icon.classList.remove('fa-regular');
                    icon.classList.add('fa-solid');
                    icon.style.color = '#EC4899';
                } else {
                    icon.classList.remove('fa-solid');
                    icon.classList.add('fa-regular');
                    icon.style.color = '';
                }
            });
        });
    </script>
</body>
</html>
