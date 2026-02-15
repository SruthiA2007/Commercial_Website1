# Ex02 Commercial Website
## Date:15.02.2026

## AIM:
To create a commercial website using CSS Flexbox.

## ALGORITHM:
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM:
## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SwiftCart | Modern Flexbox Store</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="navbar">
        <div class="logo">SwiftCart</div>
        <nav>
            <ul class="nav-links">
                <li><a href="#fashion">Fashion</a></li>
                <li><a href="#electronics">Electronics</a></li>
                <li><a href="#groceries">Groceries</a></li>
                <li><a href="#about">About</a></li>
            </ul>
        </nav>
        <button class="login-btn">Login</button>
    </header>

    <section id="fashion" class="section-container">
        <h2 class="category-title">Fashion Section</h2>
        <div class="product-flex-container">
            <div class="product-card">
                <img src="./images/photo.png" alt="Dress">
                <h3>Floral printed maxi</h3>
                <span class="price">₹4,999</span>
            </div>
            <div class="product-card">
                <img src="https://images.pexels.com/photos/1126993/pexels-photo-1126993.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Dress">
                <h3>Designer Dress</h3>
                <span class="price">₹2,899</span>
            </div>
            <div class="product-card">
                <img src="saree.png" alt="Dress">
                <h3>Saree</h3>
                <span class="price">₹25,000</span>
            </div>
        </div>
    </section>

    <section id="electronics" class="section-container" style="background-color: #f0f2f5;">
        <h2 class="category-title">Electronics Section</h2>
        <div class="product-flex-container">
            <div class="product-card">
                <img src="https://images.pexels.com/photos/18105/pexels-photo.jpg?auto=compress&cs=tinysrgb&w=400" alt="Laptop">
                <h3>Gaming Laptop</h3>
                <span class="price">₹75,000</span>
            </div>
            <div class="product-card">
                <img src="./images/Screenshot 2026-02-07 144003.png" alt="Phone">
                <h3>Iphone Pro</h3>
                <span class="price">₹55,000</span>
            </div>
            <div class="product-card">
                <img src="camera.png" alt="camera">
                <h3>Camera</h3>
                <span class="price">₹25,000</span>
            </div>
        </div>
    </section>

    <section id="groceries" class="section-container">
        <h2 class="category-title">Groceries Section</h2>
        <div class="product-flex-container">
            <div class="product-card">
                <img src="snacks.png" alt="snacks">
                <h3>Healthy Snacks</h3>
                <span class="price">₹150/kg</span>
            </div>
            <div class="product-card">
                <img src="veg.png" alt="veg">
                <h3>Vegitables</h3>
                <span class="price">₹200</span>
            </div>
            <div class="product-card">
                <img src="fruits.png" alt="fruits">
                <h3>Freash Fruits</h3>
                <span class="price">₹300</span>
            </div>
        </div>
    </section>

    <section id="about" class="info-section">
        <div class="info-card">
            <h2>About SwiftCart</h2>
            <p>This is a modern commercial website experiment created using <b>CSS Flexbox</b>. All sections are perfectly centered and responsive.</p>
        </div>
    </section>

    <footer class="footer-info">
        <p>© 2026 SwiftCart Experiment | All Rights Reserved</p>
    </footer>

</body>
</html>
```
## style.css
```

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background-color: #f4f7f6;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2874f0;
    padding: 15px 10%;
    color: white;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo { font-size: 24px; font-weight: bold; }
.nav-links { display: flex; list-style: none; gap: 30px; }
.nav-links a { color: white; text-decoration: none; font-weight: 500; }
.login-btn { background: white; color: #2874f0; border: none; padding: 8px 20px; font-weight: bold; cursor: pointer; }


.section-container {
    padding: 60px 10%;
    text-align: center;
}

.category-title {
    margin-bottom: 40px;
    font-size: 2rem;
    color: #333;
}


.product-flex-container {
    display: flex;
    justify-content: center; 
    align-items: center;
    flex-wrap: wrap; 
    gap: 80px; 
}

.product-card {
    background: white;
    padding: 20px;
    width: 350px; 
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    transition: 0.3s;
}

.product-card:hover {
    transform: translateY(-10px);
}

.product-card img {
    width: 100%;
    height: 300px; 
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 15px;
}

.price {
    display: block;
    font-size: 1.4rem;
    font-weight: bold;
    color: #388e3c;
    margin-top: 10px;
}

/* ABOUT & FOOTER */
.info-section {
    padding: 60px 10%;
    background: #fff;
    display: flex;
    justify-content: center;
}

.info-card { text-align: center; max-width: 700px; }

.footer-info {
    background: #172337;
    color: white;
    text-align: center;
    padding: 30px;
}
```

## OUTPUT:
<img width="1916" height="1024" alt="Screenshot 2026-02-15 183537" src="https://github.com/user-attachments/assets/fa8038b4-fc34-43df-b154-2523f30ee1db" />
<img width="1916" height="1014" alt="Screenshot 2026-02-15 183755" src="https://github.com/user-attachments/assets/9c78fad5-b7a9-4b80-87cb-33938d414523" />
<img width="1916" height="1016" alt="Screenshot 2026-02-15 183741" src="https://github.com/user-attachments/assets/706cdf57-3267-42cf-9032-3b67f69b7ad1" />
<img width="1919" height="1033" alt="Screenshot 2026-02-15 183824" src="https://github.com/user-attachments/assets/b90d1fd2-7c68-4efe-ad08-55598409c790" />

## RESULT:
The program for creating commercial website using CSS Flexbox is executed successfully.
