# Tailwind CSS Quick Reference

## Common Utility Classes

### Layout
```css
/* Display */
block, inline-block, inline, flex, inline-flex, grid, inline-grid, hidden

/* Position */
static, fixed, absolute, relative, sticky

/* Flexbox */
flex-row, flex-col, flex-wrap, flex-nowrap
justify-start, justify-center, justify-end, justify-between, justify-around, justify-evenly
items-start, items-center, items-end, items-stretch, items-baseline

/* Grid */
grid-cols-1 to grid-cols-12
col-span-1 to col-span-12
gap-0, gap-1, gap-2, gap-4, gap-6, gap-8
```

### Spacing
```css
/* Padding */
p-0, p-1, p-2, p-3, p-4, p-5, p-6, p-8, p-10, p-12, p-16, p-20, p-24
px-*, py-*, pt-*, pr-*, pb-*, pl-*

/* Margin */
m-0, m-1, m-2, m-3, m-4, m-5, m-6, m-8, m-10, m-12, m-16, m-20, m-24
mx-*, my-*, mt-*, mr-*, mb-*, ml-*
```

### Typography
```css
/* Font Size */
text-xs, text-sm, text-base, text-lg, text-xl, text-2xl, text-3xl, text-4xl, text-5xl, text-6xl

/* Font Weight */
font-thin, font-light, font-normal, font-medium, font-semibold, font-bold, font-extrabold, font-black

/* Text Alignment */
text-left, text-center, text-right, text-justify

/* Text Color */
text-gray-900, text-red-500, text-blue-600, text-green-500, text-yellow-400, text-purple-600
```

### Colors
```css
/* Background Colors */
bg-white, bg-gray-100, bg-red-500, bg-blue-600, bg-green-500, bg-yellow-400, bg-purple-600

/* Border Colors */
border-gray-300, border-red-500, border-blue-600, border-green-500

/* Text Colors */
text-gray-900, text-white, text-red-500, text-blue-600, text-green-500
```

### Borders & Rounded Corners
```css
/* Border Width */
border, border-0, border-2, border-4, border-8

/* Border Radius */
rounded-none, rounded-sm, rounded, rounded-md, rounded-lg, rounded-xl, rounded-2xl, rounded-full

/* Border Style */
border-solid, border-dashed, border-dotted, border-double, border-none
```

### Responsive Breakpoints
```css
/* Default (mobile first) */
sm:  /* 640px and up */
md:  /* 768px and up */
lg:  /* 1024px and up */
xl:  /* 1280px and up */
2xl: /* 1536px and up */
```

### Hover & Focus States
```css
hover:bg-blue-600
hover:text-white
focus:outline-none
focus:ring-2
focus:ring-blue-500
```

## Common Patterns

### Card Component
```html
<div class="bg-white rounded-lg shadow-md p-6 max-w-sm mx-auto">
  <h2 class="text-xl font-bold text-gray-800 mb-2">Card Title</h2>
  <p class="text-gray-600 mb-4">Card description text goes here.</p>
  <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">
    Action Button
  </button>
</div>
```

### Navigation Bar
```html
<nav class="bg-white shadow-lg">
  <div class="max-w-7xl mx-auto px-4">
    <div class="flex justify-between items-center py-4">
      <div class="text-xl font-bold text-gray-800">Logo</div>
      <div class="hidden md:flex space-x-8">
        <a href="#" class="text-gray-600 hover:text-gray-900">Home</a>
        <a href="#" class="text-gray-600 hover:text-gray-900">About</a>
        <a href="#" class="text-gray-600 hover:text-gray-900">Contact</a>
      </div>
    </div>
  </div>
</nav>
```

### Button Styles
```html
<!-- Primary Button -->
<button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">
  Primary
</button>

<!-- Secondary Button -->
<button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded">
  Secondary
</button>

<!-- Outline Button -->
<button class="border border-blue-500 text-blue-500 hover:bg-blue-500 hover:text-white font-bold py-2 px-4 rounded">
  Outline
</button>
```

### Form Elements
```html
<!-- Input Field -->
<input type="text" class="border border-gray-300 rounded-md px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="Enter text">

<!-- Select Dropdown -->
<select class="border border-gray-300 rounded-md px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
  <option>Option 1</option>
  <option>Option 2</option>
</select>

<!-- Textarea -->
<textarea class="border border-gray-300 rounded-md px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" rows="4" placeholder="Enter message"></textarea>
```

### Grid Layouts
```html
<!-- 3-Column Grid -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
  <div class="bg-white p-6 rounded-lg shadow">Column 1</div>
  <div class="bg-white p-6 rounded-lg shadow">Column 2</div>
  <div class="bg-white p-6 rounded-lg shadow">Column 3</div>
</div>

<!-- Responsive Grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
  <!-- Grid items -->
</div>
```

### Flexbox Layouts
```html
<!-- Centered Content -->
<div class="flex items-center justify-center min-h-screen">
  <div class="text-center">
    <h1 class="text-4xl font-bold">Centered Content</h1>
  </div>
</div>

<!-- Space Between -->
<div class="flex justify-between items-center">
  <div>Left Content</div>
  <div>Right Content</div>
</div>
```

## Customization Examples

### Custom Colors in Config
```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        'brand-blue': '#1e40af',
        'brand-green': '#059669',
        'custom': {
          50: '#f0f9ff',
          500: '#3b82f6',
          900: '#1e3a8a',
        }
      }
    }
  }
}
```

### Custom Spacing
```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      spacing: {
        '72': '18rem',
        '84': '21rem',
        '96': '24rem',
      }
    }
  }
}
```

### Custom Fonts
```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        'custom': ['Inter', 'sans-serif'],
        'heading': ['Poppins', 'sans-serif'],
      }
    }
  }
}
```

## Performance Tips

### Purging Unused CSS
```javascript
// tailwind.config.js
module.exports = {
  content: [
    './src/**/*.{html,js,jsx,ts,tsx}',
    './public/index.html',
  ],
  // ... rest of config
}
```

### Using @apply for Components
```css
/* styles.css */
.btn-primary {
  @apply bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded;
}

.card {
  @apply bg-white rounded-lg shadow-md p-6;
}
```

## Debugging Tips

1. **Use browser dev tools** to inspect applied classes
2. **Check class spelling** - Tailwind classes must be exact
3. **Verify responsive breakpoints** with browser resize
4. **Use Tailwind CSS IntelliSense** for VS Code
5. **Check purge configuration** if styles are missing in production

## Useful Resources

- [Tailwind CSS Cheat Sheet](https://tailwindcomponents.com/cheatsheet/)
- [Tailwind CSS Playground](https://play.tailwindcss.com/)
- [Color Palette Generator](https://tailwindcss.com/docs/customizing-colors)
- [Component Examples](https://tailwindui.com/components)


