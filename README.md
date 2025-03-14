Restaurant Website
A modern two-page restaurant website built with HTML, CSS (Grid + Flexbox), and SASS/SCSS. The website includes a homepage and a menu page, with a responsive layout and consistent design.

Project Overview
This project is a modern and responsive restaurant website consisting of two main pages:

index.html → Home Page
menu.html → Menu Page
The website is built using:
HTML5, CSS Grid & Flexbox, SASS/SCSS, Modular file structure, Fully responsive design

File Structure

AS7/
├── src/
│   ├── styles/
│   │   ├── layout/
│   │   ├── components/
│   │   ├── utilities/
│   │   └── main.scss
│   ├── assets/
│   │   └── images/
│   │       ├── r1.jpg
│   │       ├── r2.jpg
│   │       └── r3.jpg
│   │       ├── Pizza.jpg
│   │       ├── Pasta.jpg
│   │       └── Burger.jpg
│   ├── index.html
│   ├── menu.html
├── dist/
│   └── css/
│       └── main.css
├── package.json
└── README.md

SASS/SCSS Features Implemented
1. Variables
Defined and used variables for colors, fonts, spacing, etc.:
$primary-color: #ff5722;
$secondary-color: #333;
$text-color: #ffffff;
$spacing: 20px;

2. Custom Properties
Defined CSS custom properties to allow for easier theme adjustments:

:root {
  --main-color: #ff5722;
}

3. Nesting
Used nesting to organize styles hierarchically and increase readability:

.navbar {
  .nav-item {
    &:hover {
      color: $primary-color;
    }
  }
}

4. Interpolation
Used interpolation to dynamically create selectors and values:
$size: 200px;
.grid-container {
  width: #{$size};
}

5. Placeholder Selectors
Defined reusable styles using placeholders:
%centered {
  display: flex;
  justify-content: center;
  align-items: center;
}

6. Mixins
Created mixins for reusable style blocks:
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

7. Functions
Used SASS functions for dynamic calculations:
@function calculate-spacing($factor) {
  @return $factor * $spacing;
}

8. Additional SASS/SCSS Features
 @extend → Used to avoid code repetition
 @if → Used for conditional styling
 @for → Used to generate dynamic styles
 object-fit → Ensured consistent image scaling

 CSS Layout Techniques
 CSS Grid Layout
    Used CSS Grid for creating consistent and responsive grid layouts on both pages:

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  padding: 20px;
}

 Flexbox Layout
    Used Flexbox for aligning the navigation bar and footer:

.navbar {
  display: flex;
  justify-content: center;
  align-items: center;
}

 