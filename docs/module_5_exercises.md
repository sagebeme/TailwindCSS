
# 🏋️ Module 5 Exercises: Advanced Tailwind & Production

This module focuses on advanced styling techniques, accessibility, dark mode, and best practices for production-ready applications.

## Exercise 5.1: Creating Interactive Elements with Transitions and Transforms

**Objective**: Build an interactive card component that uses Tailwind CSS transitions and transforms for engaging hover effects.

**Time Estimate**: 60-75 minutes

**Prerequisites**: Understanding of basic Tailwind utilities, hover variants.

### Step-by-Step Instructions:

1.  **Setup**: Create a new HTML file (e.g., `interactive-card.html`) and link the Tailwind CDN.
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Interactive Card</title>
        <script src="https://cdn.tailwindcss.com"></script>
    </head>
    <body class="bg-gray-200 flex items-center justify-center min-h-screen">
        <div class="container mx-auto p-8">
            <!-- Interactive Card will go here -->
        </div>
    </body>
    </html>
    ```

2.  **Create the Card Structure**: Build a card with an image, title, description, and a button.
    ```html
    <div class="group bg-white rounded-lg shadow-lg overflow-hidden max-w-sm mx-auto">
        <div class="overflow-hidden">
            <img src="https://via.placeholder.com/400x250" alt="Card Image" class="w-full h-auto object-cover">
        </div>
        <div class="p-6">
            <h2 class="text-2xl font-bold text-gray-800 mb-2">Interactive Card</h2>
            <p class="text-gray-600 mb-6">Hover over this card to see some cool effects!</p>
            <button class="bg-blue-500 text-white px-6 py-2 rounded-full font-semibold">
                Learn More
            </button>
        </div>
    </div>
    ```
    *Note: We added a `group` class to the main card container. This will allow us to apply hover effects to child elements when the parent is hovered.*

3.  **Add Transition and Transform Utilities**: Now, let's add the interactive effects.
    -   To the main card container (`.group`), add `transition-all duration-500` and `hover:shadow-2xl`.
    -   To the `<img>` tag, add `transition-transform duration-500` and `group-hover:scale-110`.
    -   To the `<button>`, add `transition-all duration-300`, `group-hover:bg-blue-600`, and `group-hover:translate-y-1`.

    ```html
    <div class="group bg-white rounded-lg shadow-lg overflow-hidden max-w-sm mx-auto transition-all duration-500 hover:shadow-2xl">
        <div class="overflow-hidden">
            <img src="https://via.placeholder.com/400x250" alt="Card Image" 
                 class="w-full h-auto object-cover transition-transform duration-500 group-hover:scale-110">
        </div>
        <div class="p-6">
            <h2 class="text-2xl font-bold text-gray-800 mb-2">Interactive Card</h2>
            <p class="text-gray-600 mb-6">Hover over this card to see some cool effects!</p>
            <button class="bg-blue-500 text-white px-6 py-2 rounded-full font-semibold transition-all duration-300 group-hover:bg-blue-600 group-hover:translate-y-1">
                Learn More
            </button>
        </div>
    </div>
    ```

4.  **Verify the Effects**: Open `interactive-card.html` in your browser. Hover over the card. You should see:
    -   The card's shadow becomes more pronounced.
    -   The image smoothly scales up.
    -   The button changes color and moves down slightly.

### Expected Outcome:

A visually engaging card component that provides clear feedback to the user on hover. This exercise demonstrates how to combine transitions, transforms, and group-hover variants to create sophisticated interactive effects with only utility classes.

### Extension Challenges:

-   Add a text overlay to the image that fades in on hover (`opacity-0 group-hover:opacity-100`).
-   Implement a custom animation (e.g., a subtle pulse) on the button using `@keyframes` and your `tailwind.config.js`.
-   Create a gallery of these interactive cards using a responsive grid.

## Exercise 5.2: Implementing a Dark Mode Toggle

**Objective**: Add a dark mode theme to a simple webpage and create a toggle button to switch between light and dark modes.

**Time Estimate**: 75-90 minutes

**Prerequisites**: Basic JavaScript, understanding of Tailwind configuration, CLI setup.

### Step-by-Step Instructions:

1.  **Setup**: Ensure you have a Tailwind CLI project. In your `tailwind.config.js`, set `darkMode` to `class`.
    ```javascript
    // tailwind.config.js
    module.exports = {
      darkMode: 'class',
      content: ["./*.html"],
      theme: {
        extend: {},
      },
      plugins: [],
    }
    ```

2.  **Create HTML Structure**: Create an `index.html` file with some basic content and a toggle button.
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Dark Mode Toggle</title>
        <link href="./output.css" rel="stylesheet">
        <script>
            // JavaScript for toggling dark mode will go here
        </script>
    </head>
    <body class="bg-white text-gray-900">
        <div class="container mx-auto p-8">
            <header class="flex justify-between items-center mb-8">
                <h1 class="text-3xl font-bold">Dark Mode Example</h1>
                <button id="darkModeToggle" class="px-4 py-2 rounded-md font-semibold">
                    Toggle Dark Mode
                </button>
            </header>
            <div class="p-6 rounded-lg shadow-md">
                <h2 class="text-2xl font-semibold mb-4">Article Title</h2>
                <p>This is some sample content that will change color in dark mode.</p>
            </div>
        </div>
    </body>
    </html>
    ```

3.  **Apply Dark Mode Styles**: Use the `dark:` variant to apply styles for dark mode.
    -   `<body>`: `dark:bg-gray-900 dark:text-white`
    -   `<h1>`: `dark:text-gray-100`
    -   Toggle button: `bg-gray-200 text-gray-800 dark:bg-gray-700 dark:text-gray-200`
    -   Article container: `bg-gray-50 dark:bg-gray-800`
    -   Article title: `dark:text-gray-200`
    -   Article paragraph: `dark:text-gray-400`

    *Update your HTML with these classes.*

4.  **Add JavaScript for Toggling**: Inside the `<script>` tag in your `<head>`, add the JavaScript to handle the dark mode toggle and persistence.
    ```javascript
    // Check for saved theme in localStorage and apply it on page load
    if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
        document.documentElement.classList.add('dark')
    } else {
        document.documentElement.classList.remove('dark')
    }

    function toggleDarkMode() {
        if (document.documentElement.classList.contains('dark')) {
            document.documentElement.classList.remove('dark');
            localStorage.theme = 'light';
        } else {
            document.documentElement.classList.add('dark');
            localStorage.theme = 'dark';
        }
    }

    // Attach event listener after the DOM is loaded
    document.addEventListener('DOMContentLoaded', function() {
        const toggleButton = document.getElementById('darkModeToggle');
        if (toggleButton) {
            toggleButton.addEventListener('click', toggleDarkMode);
        }
    });
    ```

5.  **Verify Functionality**: Run your Tailwind build process and open `index.html`. Click the "Toggle Dark Mode" button. The page should switch between light and dark themes. Refresh the page; it should remember your last selected theme.

### Expected Outcome:

A fully functional dark mode implementation. The webpage should respect the user's OS preference on the first visit and allow them to manually toggle the theme. The selected theme should persist across page reloads.

### Extension Challenges:

-   Create a more visually appealing toggle switch (e.g., a sun/moon icon that changes).
-   Add smooth transitions to the color changes using `transition-colors`.
-   Ensure all components on your page (buttons, forms, cards) have appropriate dark mode styles.

## Exercise 5.3: Accessibility Audit and Fixes

**Objective**: Identify and fix common accessibility issues in a pre-built component using Tailwind CSS and best practices.

**Time Estimate**: 60-75 minutes

**Prerequisites**: Understanding of semantic HTML, focus states, and color contrast.

### Step-by-Step Instructions:

1.  **Setup**: Use the following HTML snippet in a new file (e.g., `accessibility-fix.html`). This code has several accessibility issues.
    ```html
    <!-- BAD EXAMPLE - DO NOT COPY AS-IS -->
    <div class="bg-gray-200 p-8">
        <div class="text-2xl">Sign Up</div>
        <div class="mt-4">
            <div class="text-gray-600">Email</div>
            <input type="text" class="border w-full p-2">
        </div>
        <div class="mt-4">
            <div class="text-gray-600">Password</div>
            <input type="password" class="border w-full p-2">
        </div>
        <div class="mt-6">
            <div class="bg-blue-500 text-white p-2 text-center">Submit</div>
        </div>
    </div>
    ```

2.  **Identify Accessibility Issues**: Audit the code and identify the problems. Some issues include:
    -   Non-semantic HTML (`<div>` used for headings, labels, and buttons).
    -   Missing `for` attributes on labels and `id` attributes on inputs.
    -   Poor color contrast (potentially `text-gray-600` on `bg-gray-200`).
    -   No focus states for interactive elements.
    -   A `<div>` is used as a button, making it inaccessible to keyboard and screen reader users.

3.  **Fix the Issues**: Rewrite the HTML to be accessible, using Tailwind CSS to style it correctly.
    -   Use `<h1>` for the heading.
    -   Use `<label>` for labels and link them to inputs with `for` and `id`.
    -   Use a `<button>` element for the submit action.
    -   Add clear focus states (`focus:ring-2`, `focus:outline-none`).
    -   Improve color contrast.

    **Corrected Code:**
    ```html
    <div class="bg-white p-8 rounded-lg shadow-md max-w-md mx-auto">
        <h1 class="text-3xl font-bold text-gray-900 mb-6">Sign Up</h1>
        <form>
            <div class="mb-4">
                <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email Address</label>
                <input type="email" id="email" name="email"
                       class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-6">
                <label for="password" class="block text-gray-700 text-sm font-bold mb-2">Password</label>
                <input type="password" id="password" name="password"
                       class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mt-6">
                <button type="submit" 
                        class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-md focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500">
                    Submit
                </button>
            </div>
        </form>
    </div>
    ```

4.  **Verify Accessibility**: Open the corrected file in your browser.
    -   Use the Tab key to navigate through the form. You should see clear focus rings on the inputs and the button.
    -   Click on the labels; the corresponding input fields should become focused.
    -   Use a color contrast checker tool to verify that the text and background colors meet WCAG AA standards.

### Expected Outcome:

A form that is not only visually styled but also semantically correct and accessible. Users should be able to navigate and use the form with a keyboard, and screen readers should be able to interpret the form structure correctly. This exercise highlights that accessibility is a combination of correct HTML structure and thoughtful styling.

### Extension Challenges:

-   Add ARIA attributes for validation feedback (e.g., `aria-invalid="true"`).
-   Implement a custom-styled, accessible checkbox for "I agree to the terms."
-   Use a tool like Axe DevTools or Lighthouse to run an automated accessibility audit on your component.

