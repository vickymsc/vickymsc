# Tailwind CSS Complete Guide (Basic → Advanced)

A full reference and learning guide for Tailwind CSS. This document is
designed to live in a repository as:

`TAILWINDCSS_GUIDE.md`

It covers:

-   Installation
-   Core utilities
-   Layout systems
-   Responsive design
-   Components
-   Configuration
-   Performance
-   Plugins
-   Production workflow
-   Interview questions

------------------------------------------------------------------------

# 1. What is Tailwind CSS

Tailwind CSS is a **utility‑first CSS framework** that lets you build
designs using small reusable classes directly in HTML.

Example:

``` html
<div class="bg-white p-6 rounded-lg shadow-lg">
```

Instead of writing CSS like:

``` css
.card {
  background:white;
  padding:24px;
  border-radius:10px;
}
```

Tailwind allows:

``` html
<div class="bg-white p-6 rounded-lg">
```

Benefits:

-   Faster UI development
-   Consistent design system
-   Responsive utilities built-in
-   Highly customizable
-   Smaller production CSS

------------------------------------------------------------------------

# 2. Installation (Recommended: Vite)

``` bash
npm create vite@latest my-project
cd my-project
npm install

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Edit `tailwind.config.js`

``` javascript
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Create `src/style.css`

``` css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Import:

``` javascript
import './style.css'
```

Run:

``` bash
npm run dev
```

------------------------------------------------------------------------

# 3. Spacing System

Spacing scale:

0 1 2 3 4 5 6 8 10 12 16 20 24 32 40 48 56 64

## Padding

  Class   Meaning
  ------- ----------------
  p-4     padding
  px-4    horizontal
  py-4    vertical
  pt-4    padding-top
  pb-4    padding-bottom

## Margin

  Class     Meaning
  --------- ---------------
  m-4       margin
  mx-auto   center
  mt-4      margin top
  mb-4      margin bottom

------------------------------------------------------------------------

# 4. Typography

## Font Size

text-xs\
text-sm\
text-base\
text-lg\
text-xl\
text-2xl\
text-3xl\
text-4xl

## Font Weight

font-light\
font-normal\
font-medium\
font-semibold\
font-bold

## Alignment

text-left\
text-center\
text-right

------------------------------------------------------------------------

# 5. Colors

Pattern:

color-shade

Example:

bg-blue-500\
text-gray-700\
border-red-300

Shades:

50 100 200 300 400 500 600 700 800 900

------------------------------------------------------------------------

# 6. Layout

  Class          Description
  -------------- ----------------------
  block          block element
  inline         inline
  inline-block   inline block
  hidden         display none
  container      responsive container

------------------------------------------------------------------------

# 7. Width & Height

w-full\
w-screen\
w-1/2\
w-1/3\
w-1/4

h-full\
h-screen

------------------------------------------------------------------------

# 8. Flexbox

Enable flex

flex\
inline-flex

Direction

flex-row\
flex-col

Alignment

items-start\
items-center\
items-end

Justify

justify-start\
justify-center\
justify-between\
justify-around

Gap

gap-2\
gap-4\
gap-6

Example

``` html
<div class="flex items-center justify-between">
```

------------------------------------------------------------------------

# 9. Grid

grid

Columns

grid-cols-2\
grid-cols-3\
grid-cols-4

Gap

gap-4\
gap-8

Example

``` html
<div class="grid grid-cols-3 gap-6">
```

------------------------------------------------------------------------

# 10. Borders

border\
border-2

Radius

rounded\
rounded-md\
rounded-lg\
rounded-xl\
rounded-full

------------------------------------------------------------------------

# 11. Shadows

shadow\
shadow-md\
shadow-lg\
shadow-xl\
shadow-2xl

------------------------------------------------------------------------

# 12. Background

bg-red-500\
bg-blue-500\
bg-gray-100

Background sizing

bg-cover\
bg-contain

Position

bg-center\
bg-top

------------------------------------------------------------------------

# 13. Position

static\
relative\
absolute\
fixed\
sticky

Position utilities

top-0\
left-0\
right-0\
bottom-0

------------------------------------------------------------------------

# 14. Z Index

z-0\
z-10\
z-20\
z-30\
z-40\
z-50

------------------------------------------------------------------------

# 15. Opacity

opacity-0\
opacity-25\
opacity-50\
opacity-75\
opacity-100

------------------------------------------------------------------------

# 16. Hover & States

hover:bg-blue-600\
hover:text-white\
hover:scale-105

focus:outline-none

active:scale-95

------------------------------------------------------------------------

# 17. Transitions

transition

duration-150\
duration-300\
duration-500

ease-in\
ease-out\
ease-in-out

Example

``` html
<button class="transition duration-300 hover:scale-110">
```

------------------------------------------------------------------------

# 18. Responsive Design

Breakpoints

  Prefix   Width
  -------- --------
  sm       640px
  md       768px
  lg       1024px
  xl       1280px
  2xl      1536px

Example

``` html
<div class="text-sm md:text-lg lg:text-xl">
```

------------------------------------------------------------------------

# 19. Dark Mode

``` html
<div class="bg-white dark:bg-gray-900">
```

Enable in config.

------------------------------------------------------------------------

# 20. Custom Theme Configuration

Edit `tailwind.config.js`

``` javascript
extend: {
  colors: {
    primary: '#ff6600',
    secondary: '#0ea5e9'
  }
}
```

Usage

``` html
<div class="bg-primary">
```

------------------------------------------------------------------------

# 21. Components Layer

Reusable classes

``` css
@layer components {
  .btn-primary {
    @apply bg-blue-500 text-white px-4 py-2 rounded;
  }
}
```

------------------------------------------------------------------------

# 22. Utility Layer

Custom utility

``` css
@layer utilities {
  .content-auto {
    content-visibility:auto;
  }
}
```

------------------------------------------------------------------------

# 23. Production Optimization

Tailwind automatically removes unused CSS in production.

Ensure `content` paths are correct.

Example:

``` javascript
content: [
 "./index.html",
 "./src/**/*.{js,ts,jsx,tsx}"
]
```

------------------------------------------------------------------------

# 24. Folder Structure (Recommended)

project

src components pages layouts styles

tailwind.config.js postcss.config.js

------------------------------------------------------------------------

# 25. Common UI Components

## Button

``` html
<button class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
Button
</button>
```

## Card

``` html
<div class="bg-white shadow-lg rounded-xl p-6">
<h2 class="text-xl font-bold">Card Title</h2>
<p class="text-gray-600 mt-2">Example card</p>
</div>
```

## Navbar

``` html
<nav class="flex justify-between items-center p-4 bg-gray-900 text-white">
<div>Logo</div>
<ul class="flex gap-4">
<li>Home</li>
<li>About</li>
<li>Contact</li>
</ul>
</nav>
```

------------------------------------------------------------------------

# 26. Performance Tips

-   Use production build
-   Keep config clean
-   Avoid unnecessary custom CSS
-   Reuse component classes

------------------------------------------------------------------------

# 27. Useful Plugins

Install plugins

``` bash
npm install @tailwindcss/forms
npm install @tailwindcss/typography
npm install @tailwindcss/aspect-ratio
```

Example

``` javascript
plugins: [
require('@tailwindcss/forms'),
require('@tailwindcss/typography')
]
```

------------------------------------------------------------------------

# 28. Real Project Workflow

Typical stack

Tailwind +

React\
Next.js\
Astro\
Laravel\
WordPress headless

------------------------------------------------------------------------

# 29. Top 50 Most Used Classes

flex grid items-center justify-center justify-between gap-4 p-4 px-6
py-2 m-4 mx-auto text-center text-white text-gray-700 text-xl font-bold
rounded rounded-lg shadow shadow-lg bg-white bg-gray-100 bg-blue-500
hover:bg-blue-600 transition duration-300 w-full h-screen container
border border-gray-200 opacity-75 z-50 relative absolute top-0 left-0

------------------------------------------------------------------------

# 30. Tailwind Interview Questions

### What is Tailwind CSS?

Utility-first CSS framework for building UI quickly.

### Difference between Tailwind and Bootstrap?

Bootstrap uses components.\
Tailwind uses utility classes.

### What is Purge in Tailwind?

Removes unused CSS for smaller bundles.

### What is @apply?

Allows combining utilities into reusable classes.

------------------------------------------------------------------------

# End of Guide
