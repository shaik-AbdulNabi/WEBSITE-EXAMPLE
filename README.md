
<html><head><base href="/">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FlipBuy - Shop Everything!</title>
    
    <style>
    :root {
      --primary: #2874f0;
      --secondary: #fb641b;
      --text-light: #878787;
      --text-dark: #212121;
      --white: #ffffff;
      --off-white: #f1f3f6;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Roboto', sans-serif;
    }
    
    /* Header Styles */
    header {
      background: var(--primary);
      padding: 0.8rem 2rem;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    
    .header-container {
      max-width: 1400px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      gap: 2rem;
    }
    
    .logo {
      color: var(--white);
      font-size: 1.5rem;
      font-weight: bold;
      text-decoration: none;
    }
    
    .search-container {
      flex: 1;
      max-width: 600px;
      position: relative;
    }
    
    .search-input {
      width: 100%;
      padding: 0.8rem 1rem;
      border: none;
      border-radius: 4px;
      font-size: 1rem;
    }
    
    .header-actions {
      display: flex;
      align-items: center;
      gap: 2rem;
    }
    
    .header-btn {
      color: var(--white);
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 500;
    }
    
    /* Hero Section */
    .hero {
      background: var(--off-white);
      padding: 2rem;
    }
    
    .hero-slider {
      max-width: 1400px;
      margin: 0 auto;
      position: relative;
      height: 280px;
      overflow: hidden;
    }
    
    .slide {
      position: absolute;
      width: 100%;
      height: 100%;
      opacity: 0;
      transition: opacity 0.5s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--white);
      border-radius: 8px;
    }
    
    .slide.active {
      opacity: 1;
    }
    
    /* Categories Section */
    .categories {
      max-width: 1400px;
      margin: 2rem auto;
      padding: 0 2rem;
    }
    
    .category-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
    }
    
    .category-card {
      text-align: center;
      padding: 1rem;
      background: var(--white);
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    
    .category-card:hover {
      transform: translateY(-5px);
    }
    
    /* Responsive */
    @media (max-width: 768px) {
      .header-container {
        flex-wrap: wrap;
        gap: 1rem;
      }
      
      .search-container {
        order: 3;
        width: 100%;
        max-width: none;
      }
      
      .hero-slider {
        height: 200px;
      }
    }
    
    /* Product Grid */
    .products {
      max-width: 1400px;
      margin: 2rem auto;
      padding: 0 2rem;
    }
    
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 2rem;
    }
    
    .product-card {
      background: var(--white);
      border-radius: 8px;
      padding: 1rem;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }
    
    .product-card:hover {
      transform: translateY(-5px);
    }
    
    .product-image {
      width: 100%;
      height: 200px;
      object-fit: contain;
      margin-bottom: 1rem;
    }
    
    .product-title {
      font-size: 1rem;
      color: var(--text-dark);
      margin-bottom: 0.5rem;
    }
    
    .product-price {
      font-size: 1.2rem;
      font-weight: bold;
      color: var(--text-dark);
      margin-bottom: 0.5rem;
    }
    
    .product-rating {
      color: var(--text-light);
      margin-bottom: 1rem;
    }
    
    .btn {
      background: var(--secondary);
      color: var(--white);
      border: none;
      padding: 0.8rem 1.5rem;
      border-radius: 4px;
      cursor: pointer;
      font-weight: 500;
      width: 100%;
    }
    
    </style>
    
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    </head>
    <body>
    
    <header>
      <div class="header-container">
        <a href="/" class="logo">FlipBuy</a>
        
        <div class="search-container">
          <input type="text" class="search-input" placeholder="Search for products, brands and more...">
        </div>
        
        <div class="header-actions">
          <a href="/login" class="header-btn">
            <i class="fas fa-user"></i>
            Login
          </a>
          <a href="/cart" class="header-btn">
            <i class="fas fa-shopping-cart"></i>
            Cart
          </a>
        </div>
      </div>
    </header>
    
    <section class="hero">
      <div class="hero-slider">
        <div class="slide active" style="background-color: #f1f3f6;">
          <img src="https://picsum.photos/1200/280" alt="Special Offer">
        </div>
        <div class="slide" style="background-color: #ffffff;">
          <img src="https://picsum.photos/1200/281" alt="New Arrivals">
        </div>
      </div>
    </section>
    
    <section class="categories">
      <h2>Shop By Category</h2>
      <div class="category-grid">
        <div class="category-card">
          <i class="fas fa-mobile-alt fa-3x"></i>
          <h3>Electronics</h3>
        </div>
        <div class="category-card">
          <i class="fas fa-tshirt fa-3x"></i>
          <h3>Fashion</h3>
        </div>
        <div class="category-card">
          <i class="fas fa-shopping-basket fa-3x"></i>
          <h3>Groceries</h3>
        </div>
        <div class="category-card">
          <i class="fas fa-home fa-3x"></i>
          <h3>Home</h3>
        </div>
      </div>
    </section>
    
    <section class="products">
      <h2>Trending Products</h2>
      <div class="product-grid">
        <div class="product-card">
          <img src="https://picsum.photos/200" alt="Product" class="product-image">
          <h3 class="product-title">Smartphone XYZ</h3>
          <div class="product-price">₹14,999</div>
          <div class="product-rating">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="far fa-star"></i>
            (234)
          </div>
          <button class="btn">Add to Cart</button>
        </div>
        
        <div class="product-card">
          <img src="https://picsum.photos/201" alt="Product" class="product-image">
          <h3 class="product-title">Wireless Earbuds</h3>
          <div class="product-price">₹1,999</div>
          <div class="product-rating">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star-half-alt"></i>
            (412)
          </div>
          <button class="btn">Add to Cart</button>
        </div>
        
        <div class="product-card">
          <img src="https://picsum.photos/202" alt="Product" class="product-image">
          <h3 class="product-title">Smart Watch</h3>
          <div class="product-price">₹2,499</div>
          <div class="product-rating">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            (789)
          </div>
          <button class="btn">Add to Cart</button>
        </div>
        
        <div class="product-card">
          <img src="https://picsum.photos/203" alt="Product" class="product-image">
          <h3 class="product-title">Laptop Backpack</h3>
          <div class="product-price">₹999</div>
          <div class="product-rating">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star-half-alt"></i>
            <i class="far fa-star"></i>
            (167)
          </div>
          <button class="btn">Add to Cart</button>
        </div>
      </div>
    </section>
    
    <script>
    // Hero Slider
    let currentSlide = 0;
    const slides = document.querySelectorAll('.slide');
    
    function showSlide(n) {
      slides[currentSlide].classList.remove('active');
      currentSlide = (n + slides.length) % slides.length;
      slides[currentSlide].classList.add('active');
    }
    
    setInterval(() => {
      showSlide(currentSlide + 1);
    }, 5000);
    
    // Add to Cart functionality
    const addToCartButtons = document.querySelectorAll('.btn');
    addToCartButtons.forEach(button => {
      button.addEventListener('click', () => {
        const product = button.closest('.product-card');
        const productName = product.querySelector('.product-title').textContent;
        alert(`Added ${productName} to cart!`);
      });
    });
    
    // Search functionality
    const searchInput = document.querySelector('.search-input');
    searchInput.addEventListener('input', (e) => {
      const searchTerm = e.target.value.toLowerCase();
      // Implement search logic here
    });
    
    </script>
    
    </body></html>
