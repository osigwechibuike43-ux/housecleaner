# 🧹 SparkleHome — House Cleaning Service Website

A premium, fully responsive house cleaning service website built with pure HTML, CSS, and JavaScript. No frameworks or build tools required.

---

## 📁 Folder Structure

```
house-cleaning-website/
│
├── index.html          ← Main homepage (all sections in one file)
│
├── css/
│   └── style.css       ← All styles (commented by section)
│
├── js/
│   └── script.js       ← All JavaScript (commented by feature)
│
├── images/             ← Add your own photos here
│   ├── cleaner1.jpg    (Hero poster / fallback image)
│   ├── kitchen.jpg     (Kitchen video poster)
│   ├── bathroom.jpg    (Bathroom video poster)
│   └── logo.png        (Your logo — also used as favicon)
│
├── videos/             ← Add your MP4 video files here
│   ├── cleaning-home.mp4       (Hero background video)
│   ├── kitchen-cleaning.mp4    (Showcase: kitchen)
│   ├── floor-mop.mp4           (Showcase: floor mopping)
│   ├── vacuuming.mp4           (Showcase: vacuuming)
│   └── bathroom-cleaning.mp4  (Showcase: bathroom)
│
└── assets/
    └── icons/          ← Optional custom SVG icons
```

---

## 🚀 How to Run

1. **Download / unzip** this folder onto your computer.
2. **Double-click `index.html`** — it opens directly in your browser. No server needed!
3. Or right-click `index.html` → Open With → Chrome / Firefox / Edge.

---

## 🎥 Adding Your Videos

Videos are the most important visual element. Here's how to add them:

1. Record or download MP4 cleaning videos (Pexels.com has free ones).
2. Name them exactly as listed in the folder structure above.
3. Drop them into the `videos/` folder.
4. That's it! The `<video>` tags in `index.html` already point to the right paths.

**If a video is missing**, the browser automatically shows the `poster` image defined on the `<video>` tag. The site still looks great without videos.

### ✂️ Compressing Videos (important for website speed)
Large video files slow down your site. Use a free tool like **HandBrake** or **FFmpeg** to compress:
- Target: under 5MB per video
- Format: MP4 (H.264 codec)
- Resolution: 720p is fine for backgrounds

---

## 🖼️ Adding Your Images

Replace the Unsplash placeholder URLs in `index.html` with your own images:

```html
<!-- Find lines like this in index.html: -->
<img src="https://images.unsplash.com/..." alt="Home Cleaning" />

<!-- Replace with your local file: -->
<img src="images/home-cleaning.jpg" alt="Home Cleaning" />
```

---

## ✏️ Customising the Content

### Change Company Name
Search for `SparkleHome` in `index.html` and replace with your company name.

### Change Colors
Open `css/style.css` and edit the CSS variables at the top (Section 1):
```css
:root {
  --clr-accent:  #c9a84c;   /* ← Change this gold color to your brand color */
  --clr-dark:    #0a0f1e;   /* ← Change this dark background color */
}
```

### Change Prices
Find the service cards in `index.html` (Section 3: Services) and update the `card-price` spans.

### Connect the Contact Form
In `js/script.js`, find the comment:
```
/* TO DO: Replace the block below with a real API call. */
```
Replace the `setTimeout` mock with a real `fetch()` call to your backend or a form service like:
- **Formspree.io** (free, easy)
- **EmailJS** (client-side email)
- **Netlify Forms** (if hosting on Netlify)

---

## 🌐 Hosting Your Website

### Free Options:
| Service | Steps |
|---|---|
| **Netlify** | Drag & drop folder at netlify.com/drop |
| **GitHub Pages** | Push to GitHub → Settings → Pages |
| **Vercel** | Connect GitHub repo or drag & drop |

### Paid (custom domain):
- Upload all files via FTP to any web host (Hostinger, Bluehost, etc.)
- Point your domain to the hosting server

---

## 🔧 Features Summary

| Feature | How It Works |
|---|---|
| Sticky Navbar | CSS `position: fixed` + JS adds `.scrolled` class on scroll |
| Active Nav Links | JS `IntersectionObserver` watches sections, highlights matching link |
| Mobile Menu | JS toggles `.open` class on hamburger + nav |
| Hero Video BG | HTML `<video autoplay muted loop>` with CSS `object-fit: cover` |
| Scroll Animations | JS `IntersectionObserver` adds `.visible` class → CSS transitions |
| Stats Counter | JS `setInterval` counts from 0 to `data-target` value |
| Card Tilt Effect | JS reads mouse position → applies CSS `perspective + rotateX/Y` |
| Form Validation | JS checks required fields, shows inline error/success messages |
| Back-to-Top Button | Shows after 400px scroll; click triggers `window.scrollTo` |
| Video Fallback | If MP4 missing, browser shows `poster=""` image automatically |

---

## 📱 Browser Support

Works on all modern browsers:
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+
- ✅ Mobile Safari / Chrome on iOS & Android

---

*Built with ❤️ — SparkleHome 2024*
