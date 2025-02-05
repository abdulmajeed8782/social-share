# Social Media Follow Buttons for WordPress

This repository provides a simple and optimized HTML, CSS, and JavaScript snippet to add social media follow buttons with icons to a WordPress website.

## Features
- **Optimized for WordPress:** Works seamlessly with any theme.
- **Font Awesome Icons:** Uses the latest Font Awesome icons.
- **Fully Responsive:** Works on all screen sizes.
- **Easy to Integrate:** Simple copy-paste method or function-based WordPress integration.

## How to Add This Code to Your WordPress Site

### 1️⃣ **Method 1: Using a WordPress Widget (Easiest)**
1. Login to your WordPress Admin Dashboard.
2. Navigate to `Appearance` > `Widgets`.
3. Drag a `Custom HTML` widget to your desired widget area (Footer, Sidebar, etc.).
4. Copy and paste the HTML code below:

```html
<div class="social-buttons">
    <a href="https://www.pinterest.com//" class="social-button pinterest" target="_blank" aria-label="Follow on Pinterest">
        <i class="fa-brands fa-pinterest"></i>
    </a>
    <a href="https://www.facebook.com/" class="social-button facebook" target="_blank" aria-label="Follow on Facebook">
        <i class="fa-brands fa-facebook-f"></i>
    </a>
    <a href="https://www.reddit.com//" class="social-button reddit" target="_blank" aria-label="Follow on Reddit">
        <i class="fa-brands fa-reddit"></i>
    </a>
    <a href="https://www.instagram.com//" class="social-button instagram" target="_blank" aria-label="Follow on Instagram">
        <i class="fa-brands fa-instagram"></i>
    </a>
</div>
```

5. Click `Save` and check your site!

---

### 2️⃣ **Method 2: Adding to WordPress Theme Files**
1. Go to `Appearance` > `Theme File Editor`.
2. Select `header.php`, `footer.php`, or any template file where you want to insert the buttons.
3. Paste the HTML code above inside the `<body>` tag where you want the buttons to appear.
4. Click `Update File`.

---

### 3️⃣ **Method 3: Adding Font Awesome in WordPress (Fix Icon Issue)**
Sometimes, WordPress blocks external scripts, preventing Font Awesome icons from displaying. To fix this:

#### **Option 1: Add Font Awesome via CDN in Header**
1. Go to `Appearance` > `Theme File Editor`.
2. Open `header.php`.
3. Add this before `</head>`:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
```

#### **Option 2: Enqueue Font Awesome in WordPress (Recommended)**
If you want a proper WordPress method, add this to `functions.php`:

```php
function load_font_awesome() {
    wp_enqueue_style('font-awesome', 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css');
}
add_action('wp_enqueue_scripts', 'load_font_awesome');
```

---

### 🎨 **CSS Styling (If Needed)**
To ensure proper styling, add this to your `style.css` file:

```css
.social-buttons {
    display: flex;
    justify-content: center;
    gap: 10px;
    padding: 10px;
}
.social-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 45px;
    height: 45px;
    border-radius: 50%;
    text-decoration: none;
    color: white;
    font-size: 20px;
    transition: 0.3s;
}
.social-button:hover {
    opacity: 0.8;
}
.pinterest { background: #E60023; }
.facebook { background: #1877F2; }
.reddit { background: #FF4500; }
.instagram { background: linear-gradient(45deg, #F09433, #E6683C, #DC2743, #CC2366, #BC1888); }
```

---

## 📌 **Troubleshooting**
- **Icons not appearing?** Add Font Awesome using **Method 3** above.
- **WordPress blocks external scripts?** Use the `functions.php` method to enqueue Font Awesome.
- **Want buttons in the footer?** Use `Appearance > Widgets > Custom HTML`.

---

## 📝 **License**
This project is licensed under the MIT License.

---

## ❤️ **Contribute**
If you have improvements, feel free to submit a **pull request**!

---

---
