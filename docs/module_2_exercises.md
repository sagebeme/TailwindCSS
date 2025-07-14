# 🏋️ Module 2 Exercises: Core Concepts & Utility-First Workflow

These exercises will help you master Tailwind CSS's core utility classes and develop a solid understanding of the utility-first workflow. Each exercise builds upon the previous one, gradually introducing more complex concepts and real-world scenarios.

## Exercise 2.1: Typography and Text Styling Mastery

**Objective**: Master Tailwind's typography utilities by creating a comprehensive text showcase that demonstrates various text styling options.

**Time**: 45 minutes

**Prerequisites**:
- Completed Module 1 exercises
- Basic Tailwind CSS project setup

**Instructions**:

1. **Create a new HTML file**: Name it `typography-showcase.html` and set up the basic structure with Tailwind CSS linked.

2. **Create a typography showcase page**: Build a comprehensive page that demonstrates different text styling options. Start with this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typography Showcase</title>
    <link href="./output.css" rel="stylesheet">
</head>
<body class="bg-gray-50 min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <!-- Your content will go here -->
    </div>
</body>
</html>
```

3. **Add a main heading section**: Create a hero section with different heading sizes:

```html
<section class="text-center mb-16">
    <h1 class="text-6xl font-extrabold text-gray-900 mb-4">Typography Showcase</h1>
    <h2 class="text-4xl font-bold text-gray-700 mb-3">Demonstrating Tailwind's Text Utilities</h2>
    <h3 class="text-2xl font-semibold text-gray-600 mb-2">From Headlines to Body Text</h3>
    <h4 class="text-xl font-medium text-gray-500 mb-2">Every Style You Need</h4>
    <h5 class="text-lg font-normal text-gray-400 mb-1">For Modern Web Design</h5>
    <h6 class="text-base font-light text-gray-300">Complete Typography Control</h6>
</section>
```

4. **Create a font weight demonstration**: Add a section showing different font weights:

```html
<section class="mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-6 border-b-2 border-blue-500 pb-2">Font Weights</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-thin text-gray-700 mb-2">Thin (100)</p>
            <p class="text-sm text-gray-500">Perfect for elegant, minimal designs</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-extralight text-gray-700 mb-2">Extra Light (200)</p>
            <p class="text-sm text-gray-500">Subtle and sophisticated appearance</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-light text-gray-700 mb-2">Light (300)</p>
            <p class="text-sm text-gray-500">Clean and readable for body text</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-normal text-gray-700 mb-2">Normal (400)</p>
            <p class="text-sm text-gray-500">Standard weight for most content</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-medium text-gray-700 mb-2">Medium (500)</p>
            <p class="text-sm text-gray-500">Slightly emphasized text</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-semibold text-gray-700 mb-2">Semibold (600)</p>
            <p class="text-sm text-gray-500">Great for subheadings</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-bold text-gray-700 mb-2">Bold (700)</p>
            <p class="text-sm text-gray-500">Strong emphasis and headings</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-extrabold text-gray-700 mb-2">Extra Bold (800)</p>
            <p class="text-sm text-gray-500">Maximum impact headlines</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-xl font-black text-gray-700 mb-2">Black (900)</p>
            <p class="text-sm text-gray-500">Ultra-heavy display text</p>
        </div>
    </div>
</section>
```

5. **Add text color variations**: Create a color palette demonstration:

```html
<section class="mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-6 border-b-2 border-green-500 pb-2">Text Colors</h2>
    <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4">
        <div class="text-center">
            <p class="text-red-500 text-xl font-semibold mb-1">Red</p>
            <p class="text-red-300 text-sm">Light</p>
            <p class="text-red-700 text-sm">Dark</p>
        </div>
        <div class="text-center">
            <p class="text-blue-500 text-xl font-semibold mb-1">Blue</p>
            <p class="text-blue-300 text-sm">Light</p>
            <p class="text-blue-700 text-sm">Dark</p>
        </div>
        <div class="text-center">
            <p class="text-green-500 text-xl font-semibold mb-1">Green</p>
            <p class="text-green-300 text-sm">Light</p>
            <p class="text-green-700 text-sm">Dark</p>
        </div>
        <div class="text-center">
            <p class="text-yellow-500 text-xl font-semibold mb-1">Yellow</p>
            <p class="text-yellow-300 text-sm">Light</p>
            <p class="text-yellow-700 text-sm">Dark</p>
        </div>
        <div class="text-center">
            <p class="text-purple-500 text-xl font-semibold mb-1">Purple</p>
            <p class="text-purple-300 text-sm">Light</p>
            <p class="text-purple-700 text-sm">Dark</p>
        </div>
        <div class="text-center">
            <p class="text-pink-500 text-xl font-semibold mb-1">Pink</p>
            <p class="text-pink-300 text-sm">Light</p>
            <p class="text-pink-700 text-sm">Dark</p>
        </div>
    </div>
</section>
```

6. **Create text decoration and transformation examples**: Add a section for text styling effects:

```html
<section class="mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-6 border-b-2 border-purple-500 pb-2">Text Effects</h2>
    <div class="bg-white p-8 rounded-lg shadow-lg">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div>
                <h3 class="text-xl font-semibold mb-4 text-gray-700">Text Decorations</h3>
                <p class="underline mb-2">This text is underlined</p>
                <p class="line-through mb-2">This text has a line through it</p>
                <p class="no-underline mb-2">This text has no decoration</p>
                <p class="overline mb-2">This text is overlined</p>
            </div>
            <div>
                <h3 class="text-xl font-semibold mb-4 text-gray-700">Text Transformations</h3>
                <p class="uppercase mb-2">this text is uppercase</p>
                <p class="lowercase mb-2">THIS TEXT IS LOWERCASE</p>
                <p class="capitalize mb-2">this text is capitalized</p>
                <p class="normal-case mb-2">This Text Preserves Original Case</p>
            </div>
        </div>
    </div>
</section>
```

7. **Add text alignment and spacing examples**: Create a section demonstrating text alignment and line height:

```html
<section class="mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-6 border-b-2 border-indigo-500 pb-2">Text Alignment & Spacing</h2>
    <div class="space-y-6">
        <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-4 text-gray-700">Text Alignment</h3>
            <p class="text-left mb-2 bg-gray-100 p-2 rounded">Left aligned text (default)</p>
            <p class="text-center mb-2 bg-gray-100 p-2 rounded">Center aligned text</p>
            <p class="text-right mb-2 bg-gray-100 p-2 rounded">Right aligned text</p>
            <p class="text-justify bg-gray-100 p-2 rounded">Justified text spreads content evenly across the full width of the container, creating clean edges on both sides. This is particularly useful for formal documents and publications.</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-4 text-gray-700">Line Height Variations</h3>
            <p class="leading-tight mb-4 bg-gray-100 p-3 rounded">
                This paragraph has tight line height (leading-tight). Notice how the lines are closer together, creating a more compact appearance that's good for headings or when space is limited.
            </p>
            <p class="leading-normal mb-4 bg-gray-100 p-3 rounded">
                This paragraph has normal line height (leading-normal). This is the default spacing that provides good readability for most body text content.
            </p>
            <p class="leading-loose bg-gray-100 p-3 rounded">
                This paragraph has loose line height (leading-loose). The extra spacing between lines makes it easier to read and gives the text a more airy, relaxed feeling.
            </p>
        </div>
    </div>
</section>
```

8. **Test your typography showcase**: Open the file in your browser and verify that all text styles are applied correctly. Resize the browser window to test responsive behavior.

**Expected Outcome**:
- A comprehensive typography showcase displaying various text sizes, weights, colors, decorations, and alignments
- Responsive grid layouts that adapt to different screen sizes
- Clean, professional styling with proper spacing and visual hierarchy

**Extension Challenges**:
1. Add a section demonstrating letter spacing (`tracking-tight`, `tracking-normal`, `tracking-wide`)
2. Create a comparison showing the same text with different font families (if you have custom fonts configured)
3. Add hover effects to the font weight cards using `hover:` modifiers
4. Implement a dark mode toggle that changes text colors appropriately

## Exercise 2.2: Spacing and Layout Fundamentals

**Objective**: Master Tailwind's spacing utilities (margin, padding) and understand how they work together to create well-structured layouts.

**Time**: 50 minutes

**Prerequisites**:
- Completed Exercise 2.1
- Understanding of CSS box model

**Instructions**:

1. **Create a new HTML file**: Name it `spacing-layout.html` and set up the basic structure.

2. **Create a spacing demonstration page**: Start with this foundation:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spacing & Layout Fundamentals</title>
    <link href="./output.css" rel="stylesheet">
</head>
<body class="bg-gradient-to-br from-blue-50 to-indigo-100 min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <h1 class="text-5xl font-bold text-center text-gray-800 mb-12">Spacing & Layout Mastery</h1>
        <!-- Content sections will go here -->
    </div>
</body>
</html>
```

3. **Create a padding demonstration section**: Add visual examples of different padding values:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Padding Examples</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="bg-blue-500 text-white text-center font-semibold py-2">p-2</div>
            <div class="p-2 bg-blue-100">
                <div class="bg-blue-300 p-2 text-center text-sm">Content with small padding</div>
            </div>
        </div>
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="bg-green-500 text-white text-center font-semibold py-2">p-4</div>
            <div class="p-4 bg-green-100">
                <div class="bg-green-300 p-2 text-center text-sm">Content with medium padding</div>
            </div>
        </div>
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="bg-purple-500 text-white text-center font-semibold py-2">p-8</div>
            <div class="p-8 bg-purple-100">
                <div class="bg-purple-300 p-2 text-center text-sm">Content with large padding</div>
            </div>
        </div>
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="bg-red-500 text-white text-center font-semibold py-2">p-12</div>
            <div class="p-12 bg-red-100">
                <div class="bg-red-300 p-2 text-center text-sm">Content with extra large padding</div>
            </div>
        </div>
    </div>
</section>
```

4. **Add directional padding examples**: Show how to apply padding to specific sides:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Directional Padding</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="bg-white rounded-lg shadow-lg p-4">
            <h3 class="font-semibold text-gray-700 mb-3 text-center">Horizontal & Vertical</h3>
            <div class="space-y-3">
                <div class="px-6 py-2 bg-blue-100 border-2 border-dashed border-blue-300">
                    <div class="bg-blue-500 text-white text-center py-1 text-sm">px-6 py-2</div>
                </div>
                <div class="px-2 py-6 bg-green-100 border-2 border-dashed border-green-300">
                    <div class="bg-green-500 text-white text-center py-1 text-sm">px-2 py-6</div>
                </div>
            </div>
        </div>
        <div class="bg-white rounded-lg shadow-lg p-4">
            <h3 class="font-semibold text-gray-700 mb-3 text-center">Individual Sides</h3>
            <div class="space-y-3">
                <div class="pt-6 bg-yellow-100 border-2 border-dashed border-yellow-300">
                    <div class="bg-yellow-500 text-white text-center py-1 text-sm">pt-6 (top)</div>
                </div>
                <div class="pr-6 bg-pink-100 border-2 border-dashed border-pink-300">
                    <div class="bg-pink-500 text-white text-center py-1 text-sm">pr-6 (right)</div>
                </div>
                <div class="pb-6 bg-indigo-100 border-2 border-dashed border-indigo-300">
                    <div class="bg-indigo-500 text-white text-center py-1 text-sm">pb-6 (bottom)</div>
                </div>
            </div>
        </div>
        <div class="bg-white rounded-lg shadow-lg p-4">
            <h3 class="font-semibold text-gray-700 mb-3 text-center">Combined Padding</h3>
            <div class="pt-4 pr-8 pb-6 pl-2 bg-gradient-to-r from-purple-100 to-pink-100 border-2 border-dashed border-purple-300">
                <div class="bg-gradient-to-r from-purple-500 to-pink-500 text-white text-center py-2 text-sm rounded">
                    pt-4 pr-8 pb-6 pl-2
                </div>
            </div>
        </div>
    </div>
</section>
```

5. **Create margin demonstration**: Show how margins create space between elements:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Margin Examples</h2>
    <div class="bg-white rounded-lg shadow-lg p-8">
        <div class="space-y-6">
            <div class="bg-gray-100 p-4 rounded">
                <h3 class="font-semibold text-gray-700 mb-4">Vertical Margins</h3>
                <div class="bg-blue-200 p-3 mb-2 rounded">Element with mb-2</div>
                <div class="bg-blue-300 p-3 mb-4 rounded">Element with mb-4</div>
                <div class="bg-blue-400 p-3 mb-8 rounded">Element with mb-8</div>
                <div class="bg-blue-500 p-3 text-white rounded">Final element</div>
            </div>
            <div class="bg-gray-100 p-4 rounded">
                <h3 class="font-semibold text-gray-700 mb-4">Horizontal Margins</h3>
                <div class="flex flex-wrap items-center">
                    <div class="bg-green-300 p-2 mr-2 rounded text-sm">mr-2</div>
                    <div class="bg-green-400 p-2 mr-4 rounded text-sm">mr-4</div>
                    <div class="bg-green-500 p-2 mr-8 rounded text-sm text-white">mr-8</div>
                    <div class="bg-green-600 p-2 rounded text-sm text-white">Final</div>
                </div>
            </div>
            <div class="bg-gray-100 p-4 rounded">
                <h3 class="font-semibold text-gray-700 mb-4">Auto Margins (Centering)</h3>
                <div class="bg-purple-500 text-white p-4 mx-auto w-64 text-center rounded">
                    Centered with mx-auto
                </div>
            </div>
        </div>
    </div>
</section>
```

6. **Add negative margins demonstration**: Show how negative margins can be used creatively:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Negative Margins</h2>
    <div class="bg-white rounded-lg shadow-lg p-8 overflow-hidden">
        <div class="bg-gray-200 p-6 rounded-lg relative">
            <h3 class="font-semibold text-gray-700 mb-4">Overlapping Elements</h3>
            <div class="bg-blue-500 text-white p-4 rounded mb-4">Base element</div>
            <div class="bg-red-500 text-white p-4 rounded -mt-6 ml-8">
                Overlapping element with -mt-6 ml-8
            </div>
        </div>
        <div class="mt-8 bg-gray-200 p-6 rounded-lg">
            <h3 class="font-semibold text-gray-700 mb-4">Breaking Out of Container</h3>
            <div class="bg-gradient-to-r from-purple-500 to-pink-500 text-white p-6 -mx-4 rounded">
                This element extends beyond its container using -mx-4
            </div>
        </div>
    </div>
</section>
```

7. **Create a practical layout example**: Build a card layout that demonstrates proper spacing:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Practical Layout Example</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <article class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition-transform duration-300">
            <div class="h-48 bg-gradient-to-br from-blue-400 to-purple-500"></div>
            <div class="p-6">
                <h3 class="text-xl font-bold text-gray-800 mb-3">Perfect Spacing</h3>
                <p class="text-gray-600 mb-4 leading-relaxed">
                    This card demonstrates proper use of padding, margins, and spacing utilities to create a visually appealing and well-structured layout.
                </p>
                <div class="flex items-center justify-between pt-4 border-t border-gray-200">
                    <span class="text-sm text-gray-500">March 15, 2024</span>
                    <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-medium transition-colors duration-200">
                        Read More
                    </button>
                </div>
            </div>
        </article>
        
        <article class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition-transform duration-300">
            <div class="h-48 bg-gradient-to-br from-green-400 to-blue-500"></div>
            <div class="p-6">
                <h3 class="text-xl font-bold text-gray-800 mb-3">Consistent Design</h3>
                <p class="text-gray-600 mb-4 leading-relaxed">
                    Notice how all cards maintain the same spacing patterns, creating visual consistency across the entire layout.
                </p>
                <div class="flex items-center justify-between pt-4 border-t border-gray-200">
                    <span class="text-sm text-gray-500">March 12, 2024</span>
                    <button class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-lg text-sm font-medium transition-colors duration-200">
                        Read More
                    </button>
                </div>
            </div>
        </article>
        
        <article class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition-transform duration-300 md:col-span-2 lg:col-span-1">
            <div class="h-48 bg-gradient-to-br from-purple-400 to-pink-500"></div>
            <div class="p-6">
                <h3 class="text-xl font-bold text-gray-800 mb-3">Responsive Spacing</h3>
                <p class="text-gray-600 mb-4 leading-relaxed">
                    The spacing adapts beautifully across different screen sizes while maintaining proportional relationships.
                </p>
                <div class="flex items-center justify-between pt-4 border-t border-gray-200">
                    <span class="text-sm text-gray-500">March 10, 2024</span>
                    <button class="bg-purple-500 hover:bg-purple-600 text-white px-4 py-2 rounded-lg text-sm font-medium transition-colors duration-200">
                        Read More
                    </button>
                </div>
            </div>
        </article>
    </div>
</section>
```

8. **Test your spacing layout**: Open the file in your browser and examine how different spacing utilities affect the visual hierarchy and layout structure.

**Expected Outcome**:
- Clear visual demonstrations of padding and margin utilities
- Understanding of how spacing creates visual hierarchy
- Practical examples showing real-world application of spacing principles
- Responsive layout that maintains proper spacing across screen sizes

**Extension Challenges**:
1. Create a responsive spacing example where padding and margins change at different breakpoints (e.g., `p-4 md:p-8 lg:p-12`)
2. Build a complex layout using only spacing utilities (no flexbox or grid)
3. Experiment with the `space-y-*` and `space-x-*` utilities for consistent spacing between child elements
4. Create a "spacing calculator" section that shows the pixel values for each Tailwind spacing class

## Exercise 2.3: Color System and Backgrounds

**Objective**: Master Tailwind's comprehensive color system and background utilities to create visually appealing designs.

**Time**: 55 minutes

**Prerequisites**:
- Completed previous exercises in Module 2
- Basic understanding of color theory (helpful but not required)

**Instructions**:

1. **Create a new HTML file**: Name it `color-backgrounds.html` and set up the structure.

2. **Build a comprehensive color showcase**: Start with this foundation:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color System & Backgrounds</title>
    <link href="./output.css" rel="stylesheet">
</head>
<body class="bg-gray-900 min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <h1 class="text-5xl font-bold text-center text-white mb-12">Color System Mastery</h1>
        <!-- Content sections will go here -->
    </div>
</body>
</html>
```

3. **Create a color palette showcase**: Display Tailwind's color scales:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-white mb-8 text-center">Color Palettes</h2>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        <!-- Blue Palette -->
        <div class="bg-white rounded-xl p-6 shadow-2xl">
            <h3 class="text-2xl font-bold text-gray-800 mb-6 text-center">Blue Palette</h3>
            <div class="space-y-2">
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-50 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-50</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#eff6ff</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-100 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-100</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#dbeafe</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-200 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-200</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#bfdbfe</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-300 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-300</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#93c5fd</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-400 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-400</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#60a5fa</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-500 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-500</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#3b82f6</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-600 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-600</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#2563eb</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-700 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-700</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#1d4ed8</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-800 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-800</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#1e40af</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-blue-900 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">blue-900</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#1e3a8a</div>
                </div>
            </div>
        </div>
        
        <!-- Green Palette -->
        <div class="bg-white rounded-xl p-6 shadow-2xl">
            <h3 class="text-2xl font-bold text-gray-800 mb-6 text-center">Green Palette</h3>
            <div class="space-y-2">
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-50 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-50</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#f0fdf4</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-100 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-100</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#dcfce7</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-200 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-200</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#bbf7d0</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-300 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-300</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#86efac</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-400 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-400</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#4ade80</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-500 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-500</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#22c55e</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-600 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-600</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#16a34a</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-700 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-700</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#15803d</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-800 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-800</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#166534</div>
                </div>
                <div class="flex items-center">
                    <div class="w-16 h-8 bg-green-900 rounded-l border border-gray-300"></div>
                    <div class="flex-1 px-3 py-2 bg-gray-50 text-sm font-mono">green-900</div>
                    <div class="px-3 py-2 bg-gray-100 text-xs text-gray-600">#14532d</div>
                </div>
            </div>
        </div>
    </div>
</section>
```

4. **Add gradient backgrounds showcase**: Demonstrate Tailwind's gradient utilities:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-white mb-8 text-center">Gradient Backgrounds</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="h-32 bg-gradient-to-r from-purple-400 via-pink-500 to-red-500 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-purple-400 via-pink-500 to-red-500</span>
        </div>
        <div class="h-32 bg-gradient-to-br from-green-400 to-blue-600 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-green-400 to-blue-600</span>
        </div>
        <div class="h-32 bg-gradient-to-t from-yellow-400 via-red-500 to-pink-500 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-yellow-400 via-red-500 to-pink-500</span>
        </div>
        <div class="h-32 bg-gradient-to-bl from-indigo-500 via-purple-500 to-pink-500 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-indigo-500 via-purple-500 to-pink-500</span>
        </div>
        <div class="h-32 bg-gradient-to-tr from-blue-600 to-purple-600 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-blue-600 to-purple-600</span>
        </div>
        <div class="h-32 bg-gradient-to-l from-cyan-500 to-blue-500 rounded-xl shadow-lg flex items-center justify-center">
            <span class="text-white font-bold text-lg">from-cyan-500 to-blue-500</span>
        </div>
    </div>
</section>
```

5. **Create background pattern examples**: Show different background utilities:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-white mb-8 text-center">Background Patterns & Effects</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-white rounded-xl p-6 shadow-2xl">
            <h3 class="text-xl font-bold text-gray-800 mb-4">Solid Backgrounds</h3>
            <div class="space-y-4">
                <div class="h-16 bg-red-500 rounded-lg flex items-center justify-center text-white font-semibold">
                    bg-red-500
                </div>
                <div class="h-16 bg-blue-600 rounded-lg flex items-center justify-center text-white font-semibold">
                    bg-blue-600
                </div>
                <div class="h-16 bg-green-500 rounded-lg flex items-center justify-center text-white font-semibold">
                    bg-green-500
                </div>
                <div class="h-16 bg-purple-600 rounded-lg flex items-center justify-center text-white font-semibold">
                    bg-purple-600
                </div>
            </div>
        </div>
        
        <div class="bg-white rounded-xl p-6 shadow-2xl">
            <h3 class="text-xl font-bold text-gray-800 mb-4">Background Opacity</h3>
            <div class="relative">
                <div class="h-64 bg-gradient-to-br from-blue-400 to-purple-600 rounded-lg"></div>
                <div class="absolute inset-4 bg-white bg-opacity-90 rounded-lg flex items-center justify-center">
                    <span class="text-gray-800 font-semibold">bg-white bg-opacity-90</span>
                </div>
                <div class="absolute inset-8 bg-black bg-opacity-50 rounded-lg flex items-center justify-center">
                    <span class="text-white font-semibold">bg-black bg-opacity-50</span>
                </div>
                <div class="absolute inset-12 bg-red-500 bg-opacity-75 rounded-lg flex items-center justify-center">
                    <span class="text-white font-semibold">bg-red-500 bg-opacity-75</span>
                </div>
            </div>
        </div>
    </div>
</section>
```

6. **Add color contrast and accessibility examples**: Show proper color combinations:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-white mb-8 text-center">Color Contrast & Accessibility</h2>
    <div class="bg-white rounded-xl p-8 shadow-2xl">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div>
                <h3 class="text-xl font-bold text-gray-800 mb-4">Good Contrast Examples</h3>
                <div class="space-y-3">
                    <div class="bg-blue-600 text-white p-4 rounded-lg">
                        <p class="font-semibold">High Contrast</p>
                        <p class="text-sm">White text on blue background provides excellent readability</p>
                    </div>
                    <div class="bg-gray-800 text-white p-4 rounded-lg">
                        <p class="font-semibold">Dark Theme</p>
                        <p class="text-sm">White text on dark gray is easy to read</p>
                    </div>
                    <div class="bg-green-500 text-white p-4 rounded-lg">
                        <p class="font-semibold">Success Message</p>
                        <p class="text-sm">White text on green background for positive actions</p>
                    </div>
                </div>
            </div>
            
            <div>
                <h3 class="text-xl font-bold text-gray-800 mb-4">Poor Contrast Examples</h3>
                <div class="space-y-3">
                    <div class="bg-yellow-200 text-yellow-400 p-4 rounded-lg border-2 border-red-300">
                        <p class="font-semibold">Low Contrast ❌</p>
                        <p class="text-sm">This text is hard to read due to poor contrast</p>
                    </div>
                    <div class="bg-gray-300 text-gray-400 p-4 rounded-lg border-2 border-red-300">
                        <p class="font-semibold">Insufficient Contrast ❌</p>
                        <p class="text-sm">Gray on gray lacks proper contrast ratio</p>
                    </div>
                    <div class="bg-blue-200 text-blue-300 p-4 rounded-lg border-2 border-red-300">
                        <p class="font-semibold">Accessibility Issue ❌</p>
                        <p class="text-sm">This combination fails WCAG guidelines</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

7. **Create an interactive color picker section**: Build a practical color demonstration:

```html
<section class="mb-16">
    <h2 class="text-3xl font-bold text-white mb-8 text-center">Interactive Color Showcase</h2>
    <div class="bg-white rounded-xl p-8 shadow-2xl">
        <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4">
            <!-- Red Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-red-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-red-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-red-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-red-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-red-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Red</p>
            </div>
            
            <!-- Orange Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-orange-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-orange-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-orange-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-orange-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-orange-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Orange</p>
            </div>
            
            <!-- Yellow Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-yellow-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-yellow-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-yellow-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-yellow-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-yellow-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Yellow</p>
            </div>
            
            <!-- Green Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-green-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-green-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-green-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-green-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-green-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Green</p>
            </div>
            
            <!-- Blue Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-blue-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-blue-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-blue-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-blue-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-blue-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Blue</p>
            </div>
            
            <!-- Purple Colors -->
            <div class="text-center">
                <div class="w-full h-20 bg-purple-100 rounded-t-lg border border-gray-200"></div>
                <div class="w-full h-20 bg-purple-300 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-purple-500 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-purple-700 border-l border-r border-gray-200"></div>
                <div class="w-full h-20 bg-purple-900 rounded-b-lg border border-gray-200"></div>
                <p class="mt-2 text-sm font-semibold text-gray-700">Purple</p>
            </div>
        </div>
    </div>
</section>
```

8. **Test your color showcase**: Open the file in your browser and examine how different colors and backgrounds work together.

**Expected Outcome**:
- Comprehensive understanding of Tailwind's color system
- Visual demonstration of color palettes and gradients
- Understanding of color contrast and accessibility principles
- Practical examples of background utilities and effects

**Extension Challenges**:
1. Create a dark mode toggle that switches between light and dark color schemes
2. Build a color palette generator that shows complementary colors
3. Add hover effects that change background colors smoothly
4. Create a section demonstrating border colors and how they work with background colors

---

**Congratulations!** You've completed the core exercises for Module 2. You should now have a solid understanding of Tailwind's utility-first approach, typography system, spacing utilities, and color system. These fundamentals will serve as the foundation for more advanced Tailwind CSS techniques in the upcoming modules.

