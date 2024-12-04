# Restaurant Website Project

## Project Overview
Create a responsive restaurant website that allows customers to view the menu, make reservations, and learn about the restaurant. The site must function on both mobile and desktop devices.

## User Stories

### 1. Homepage Experience
**As a first-time website visitor**  
I want to understand what makes this restaurant special  
So that I can decide if I want to dine there

**Acceptance Criteria:**
- Responsive navigation menu
- Hero image optimized for both mobile and desktop
- Restaurant name and tagline
- Clear path to menu and reservations
- Operating hours
- Brief "About Us" section
- Address/Location

### 2. Menu Browsing
**As a potential customer**  
I want to browse the restaurant's complete menu  
So that I can see what dishes are available

**Acceptance Criteria:**
- 6 dishes displayed:
  - 2 appetizers
  - 2 main courses
  - 2 desserts
- Each dish shows:
  - Name
  - Price
  - Description
  - Appetizing image (400px wide)
- Menu items have hover effect
- Responsive grid layout
- Clear categorization of dishes

### 3. Reservation Process
**As a customer**  
I want to make a table reservation  
So that I can secure a dining spot

**Acceptance Criteria:**
- Form collects:
  - Name
  - Email
  - Date
  - Time
  - Number of guests
  - Special requests (optional)
- Form validation for required fields
- Submit button clearly visible
- Submits to thank-you page

### 4. Reservation Confirmation
**As a customer who submitted a reservation**  
I want to see a confirmation  
So that I know my reservation was received

**Acceptance Criteria:**
- Displays confirmation message
- Provides way to return to homepage
- Matches site's design

### Bonus Feature: Detailed Dish Pages
**As an interested diner**  
I want to learn more about specific dishes  
So that I can make informed choices

**Acceptance Criteria:**
- Individual page for each dish including:
  - Larger image
  - Detailed description
  - Complete ingredient list
  - Dietary information
  - Allergen warnings
  - Price
  - Back to menu link

## Technical Requirements

### Required Technologies
- HTML5
- CSS3
- Flexbox
- Google Fonts (minimum 2 fonts, maximum 3)
- GitHub Pages

### Color Requirements
- Use between 3-5 colors total
- Must use CSS variables for colors
- Suggested color roles:
  - Primary color
  - Accent color
  - Text color
  - Background color
  - Light/neutral color

### HTML Page Linking Example
```html
<!-- Example of linking between pages in the same directory -->
<a href="menu.html">View Our Menu</a>
<a href="contact.html">Contact Us</a>
<a href="index.html">Return Home</a>
```

### Flexbox Example
```css
/* Basic Flexbox Container */
.container {
    display: flex;
    justify-content: space-between;
}

/* Flexbox Items */
.item {
    flex: 1;
}
```

### CSS Hover Effects Example
```css
/* Basic hover effect */
.button {
    background-color: blue;
    transition: background-color 0.3s ease;
}

.button:hover {
    background-color: darkblue;
}
```

### CSS Variables Example
```css
/* Declaring variables */
body {
    --primary-color: #333;
    --accent-color: #ff0000;
    --text-color: #222;
    --bg-color: #ffffff;
}
```

### Google Fonts Example
```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Source+Sans+Pro:wght@400;600&display=swap" rel="stylesheet">
```

### File Structure
```
restaurant-website/ (root)
├── index.html
├── menu.html
├── contact.html
├── thank-you.html
├── assets/
│   ├── css/
│   │   ├── reset.css
│   │   └── style.css
│   └── img/
│       ├── hero-desktop.png
│       ├── hero-mobile.png
│       └── menu/
│           ├── appetizer1.png
│           ├── appetizer2.png
│           ├── main1.png
│           ├── main2.png
│           ├── dessert1.png
│           └── dessert2.png
├── README.md
└── dishes/           # For bonus feature
    ├── appetizer1.html
    ├── appetizer2.html
    ├── main1.html
    ├── main2.html
    ├── dessert1.html
    └── dessert2.html
```

### Starter Code

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Name</title>
    <!-- Google Fonts must be loaded before stylesheets -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Source+Sans+Pro:wght@400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="assets/css/reset.css">
    <link rel="stylesheet" href="assets/css/style.css">
</head>
<body class="page-home">
    <header class="header">
        <div class="header-logo">Restaurant Name</div>
        <nav class="header-nav">
            <a href="index.html" class="nav-link active">Home</a>
            <a href="menu.html" class="nav-link">Menu</a>
            <a href="contact.html" class="nav-link">Contact</a>
        </nav>
    </header>

    <main>
        <section class="hero">
            <picture>
                <source 
                    media="(min-width: 768px)"
                    srcset="assets/img/hero-desktop.png">
                <source 
                    media="(max-width: 767px)"
                    srcset="assets/img/hero-mobile.png">
                <img 
                    src="assets/img/hero-mobile.png" 
                    alt="Welcome to Restaurant Name"
                    class="hero-image">
            </picture>
            <div class="hero-content">
                <h1>Welcome to Restaurant Name</h1>
                <p>Tagline goes here</p>
            </div>
        </section>
    </main>
</body>
</html>
```

```css
/*reset.css*/
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

```css
/* style.css */
body {
    --primary-color: #2C3E50;    /* Dark Blue */
    --accent-color: #E74C3C;     /* Red */
    --text-color: #333333;       /* Dark Gray */
    --light-color: #ECF0F1;      /* Light Gray */
    margin: 0;
    padding: 0;
    font-family: 'Source Sans Pro', sans-serif;
    color: var(--text-color);
}

* {
    box-sizing: border-box;
}

h1, h2, h3 {
    font-family: 'Playfair Display', serif;
}

/* Header & Navigation */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color: var(--light-color);
}

.header-nav {
    display: flex;
    gap: 2rem;
}

.nav-link {
    color: var(--text-color);
    text-decoration: none;
}

.nav-link.active {
    font-weight: bold;
    color: var(--accent-color);
}

/* Hero Section */
.hero {
    position: relative;
}

.hero-image {
    width: 100%;
    height: 60vh;
    object-fit: cover;
}

.hero-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
}

/* Responsive Design */
@media (max-width: 767px) {
    .hero-image {
        height: 40vh;
    }
}
```

## Image Resources and Requirements

### Free Stock Photo Sources
- Unsplash (https://unsplash.com)
  - Search terms: "restaurant interior", "plated food", "gourmet dishes"
- Pexels (https://pexels.com)
  - Food photography and restaurant atmosphere
- Foodiesfeed (https://foodiesfeed.com)
  - Professional food photography

### Image Requirements
- Required Format: PNG
- Alt tags required for all images
- Image credits must be included in README
- Hero Images:
  - Desktop: 1920px wide
  - Mobile: 800px wide
- Menu Items:
  - All dishes: 400px wide

### Image Attribution Example
```html
<!-- In HTML -->
<img 
    src="assets/img/hero.png" 
    alt="Cozy restaurant interior with warm lighting and wooden tables" 
    class="hero__image">

<!-- In README -->
## Image Credits
- Hero Image: Photo by [Jane Smith](https://unsplash.com/@janesmith) on [Unsplash](https://unsplash.com)
- Pasta Dish: Photo by [John Doe](https://pexels.com/@johndoe) on [Pexels](https://pexels.com)
```

**Bonus:** Use WebP format with PNG fallback for better performance

### Image Editing Tool
Photopea (https://www.photopea.com)

Steps for resizing and saving:
1. File > Open
2. Image > Image Size
3. Set width (height adjusts automatically)
4. File > Export as > PNG

## README Requirements
```markdown
# Restaurant Name Website

## Description
[Theme, target audience, special features]

## Technologies Used
- HTML5
- CSS3
- Flexbox
- Google Fonts
- GitHub Pages

## Features
[List implemented features]

## Screenshot
![Website Screenshot](screenshot-link)

## Image Credits
[List all image sources]

## Live Demo
[GitHub Pages link]

## Installation
[Local viewing instructions]

## Color Palette
[Document colors used]

## Google Fonts
[Document fonts used]

## Future Improvements
[List 3-5 potential improvements]
```

## Timeline (2 weeks)

### Week 1
- Day 1: Repository setup, navigation implementation
- Day 2-3: Image sourcing and editing
- Day 4-5: Menu page creation

### Week 2
- Day 1-2: Contact form implementation
- Day 3: Hover effects and styling
- Day 4: Testing and responsive design
- Day 5: Documentation and deployment

## Evaluation Criteria
- Functionality & Requirements (40%)
- Code Quality & Organization (25%)
- Design & User Experience (20%)
- Documentation & README (15%)

## Submission Requirements
- Professional README.md
- Correct file structure
- Working GitHub Pages deployment
- All images credited
- Screenshot in README
- No HTML validation errors
- All links functional
- Responsive design working
- Current page indicator working
- All hover effects implemented