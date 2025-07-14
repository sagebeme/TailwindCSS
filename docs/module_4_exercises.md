
# 🏋️ Module 4 Exercises: Components & Reusability

This module focuses on creating reusable components and extending Tailwind CSS to maintain a clean and scalable codebase.

## Exercise 4.1: Creating Reusable Button Components with `@apply`

**Objective**: Abstract common button styles into reusable component classes using the `@apply` directive.

**Time Estimate**: 45-60 minutes

**Prerequisites**: Basic understanding of Tailwind utilities, CLI setup for Tailwind CSS.

### Step-by-Step Instructions:

1.  **Setup**: Ensure you have a Tailwind CSS project set up with a CLI build process (e.g., using `npx tailwindcss -i ./input.css -o ./output.css --watch`). You will need an `input.css` file to add your custom component classes.

2.  **Create `input.css`**: If you don't have one, create an `input.css` file and add the following:
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

3.  **Define Button Component Classes**: In your `input.css` file, below the `@tailwind` directives, define several button component classes using `@apply`.
    ```css
    /* input.css */
    @layer components {
      .btn {
        @apply font-bold py-2 px-4 rounded transition-colors duration-300;
      }

      .btn-primary {
        @apply bg-blue-500 hover:bg-blue-700 text-white;
      }

      .btn-secondary {
        @apply bg-gray-300 hover:bg-gray-400 text-gray-800;
      }

      .btn-danger {
        @apply bg-red-500 hover:bg-red-700 text-white;
      }

      .btn-outline {
        @apply bg-transparent border border-blue-500 text-blue-500 hover:bg-blue-500 hover:text-white;
      }
    }
    ```
    *Note: We've created a base `.btn` class for common styles and specific classes for different button types.*

4.  **Create HTML File**: Create an `index.html` file and link your compiled `output.css` file.
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Button Components</title>
        <link href="./output.css" rel="stylesheet">
    </head>
    <body class="bg-gray-100 p-8">
        <div class="container mx-auto">
            <h1 class="text-3xl font-bold mb-8">Button Components Showcase</h1>
            <div class="space-x-4">
                <!-- Buttons will go here -->
            </div>
        </div>
    </body>
    </html>
    ```

5.  **Use the Button Components**: In your `index.html`, use the new component classes to create buttons. Notice how you can combine them.
    ```html
    <div class="space-x-4">
        <button class="btn btn-primary">Primary Button</button>
        <button class="btn btn-secondary">Secondary Button</button>
        <button class="btn btn-danger">Danger Button</button>
        <button class="btn btn-outline">Outline Button</button>
    </div>
    ```

6.  **Verify the Output**: Run your Tailwind build process (`npx tailwindcss ...`) and open `index.html` in your browser. You should see four styled buttons, each with the correct appearance and hover effects.

### Expected Outcome:

A set of reusable button components that can be applied with simple, semantic class names. This demonstrates how to abstract utility patterns into maintainable CSS classes, reducing repetition in your HTML.

### Extension Challenges:

-   Create a `.btn-lg` and `.btn-sm` class to control the size of the buttons.
-   Add a `disabled` state for the buttons (e.g., `.btn:disabled { @apply bg-gray-400 cursor-not-allowed; }`).
-   Implement a button with an icon using Flexbox and an SVG icon.

## Exercise 4.2: Building a Reusable Card Component

**Objective**: Create a versatile and reusable card component with different variations using `@apply` and custom classes.

**Time Estimate**: 60-75 minutes

**Prerequisites**: Understanding of `@apply`, basic Tailwind utilities.

### Step-by-Step Instructions:

1.  **Setup**: Continue with your existing Tailwind CLI project.

2.  **Define Card Component Classes**: In your `input.css` file, define a base `.card` class and some variations.
    ```css
    /* input.css */
    @layer components {
      .card {
        @apply bg-white rounded-lg shadow-md overflow-hidden;
      }

      .card-header {
        @apply p-4 border-b border-gray-200;
      }

      .card-body {
        @apply p-6;
      }

      .card-footer {
        @apply p-4 bg-gray-50 border-t border-gray-200;
      }

      .card-dark {
        @apply bg-gray-800 text-white shadow-xl;
        .card-header, .card-footer {
          @apply border-gray-700;
        }
        .card-footer {
          @apply bg-gray-900;
        }
      }
    }
    ```

3.  **Use the Card Components in HTML**: In your `index.html`, create several cards using the new component classes.
    ```html
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-12">
        <!-- Standard Card -->
        <div class="card">
            <div class="card-header">
                <h2 class="text-xl font-bold">Standard Card</h2>
            </div>
            <div class="card-body">
                <p>This is a standard card component with a header, body, and footer.</p>
            </div>
            <div class="card-footer">
                <button class="btn btn-primary">Action</button>
            </div>
        </div>

        <!-- Card with Image -->
        <div class="card">
            <img src="https://via.placeholder.com/400x200" alt="Card Image" class="w-full h-40 object-cover">
            <div class="card-body">
                <h2 class="text-xl font-bold mb-2">Card with Image</h2>
                <p>This card includes an image at the top.</p>
            </div>
        </div>

        <!-- Dark Card -->
        <div class="card card-dark">
            <div class="card-header">
                <h2 class="text-xl font-bold">Dark Card</h2>
            </div>
            <div class="card-body">
                <p>This is a dark variant of the card component.</p>
            </div>
            <div class="card-footer">
                <button class="btn btn-outline">Action</button>
            </div>
        </div>
    </div>
    ```

4.  **Verify the Output**: Open `index.html` in your browser. You should see three different card variations, each styled correctly based on the component classes you defined.

### Expected Outcome:

A flexible and reusable card component system. This exercise demonstrates how to create more complex components with multiple parts (header, body, footer) and variations (dark mode) using `@apply` and nested CSS rules.

### Extension Challenges:

-   Create a `.card-horizontal` variation where the image is on the left and the content is on the right.
-   Add a `.card-interactive` class that adds a hover effect (e.g., `hover:shadow-lg`, `hover:scale-105`).
-   Implement a card with a loading state (e.g., a skeleton loader) that can be toggled with a class.

## Exercise 4.3: Extending Tailwind with a Custom Plugin

**Objective**: Create a simple custom Tailwind CSS plugin to add new utility classes.

**Time Estimate**: 75-90 minutes

**Prerequisites**: Basic JavaScript knowledge, understanding of Tailwind configuration.

### Step-by-Step Instructions:

1.  **Setup**: Continue with your existing Tailwind CLI project.

2.  **Create Plugin File**: Create a new file named `my-tailwind-plugin.js` in your project's root directory.

3.  **Write the Plugin Code**: In `my-tailwind-plugin.js`, write the code for a simple plugin that adds a `no-scrollbar` utility and a `text-shadow` utility.
    ```javascript
    // my-tailwind-plugin.js
    const plugin = require("tailwindcss/plugin");

    module.exports = plugin(function ({ addUtilities, theme }) {
      const newUtilities = {
        '.no-scrollbar': {
          '-ms-overflow-style': 'none',  /* IE and Edge */
          'scrollbar-width': 'none',  /* Firefox */
          '&::-webkit-scrollbar': { 'display': 'none' } /* Safari and Chrome */
        },
        '.text-shadow': {
          'text-shadow': '2px 2px 4px rgba(0, 0, 0, 0.5)',
        },
        '.text-shadow-md': {
          'text-shadow': '4px 4px 8px rgba(0, 0, 0, 0.5)',
        },
        '.text-shadow-lg': {
          'text-shadow': '6px 6px 12px rgba(0, 0, 0, 0.5)',
        },
      };

      addUtilities(newUtilities, ['responsive', 'hover']);
    });
    ```

4.  **Configure `tailwind.config.js`**: Open your `tailwind.config.js` file and require your new plugin in the `plugins` array.
    ```javascript
    // tailwind.config.js
    module.exports = {
      content: ["./*.html"], // Make sure this is configured correctly
      theme: {
        extend: {},
      },
      plugins: [
        require('./my-tailwind-plugin.js'),
      ],
    }
    ```

5.  **Use the New Utilities in HTML**: In your `index.html`, use the new utility classes from your plugin.
    ```html
    <div class="mt-12">
        <h2 class="text-2xl font-bold mb-4 text-shadow-md">Plugin Utilities Showcase</h2>
        
        <div class="w-64 h-32 overflow-y-scroll border border-gray-300 no-scrollbar">
            <p class="p-4">This box has a scrollbar, but it's hidden by the 'no-scrollbar' utility from our custom plugin. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>

        <p class="text-3xl font-bold mt-8 text-shadow-lg hover:text-shadow">This text has a shadow effect.</p>
    </div>
    ```

6.  **Verify the Output**: Restart your Tailwind build process to ensure it picks up the new plugin. Open `index.html` in your browser. You should see that the scrollable box has no visible scrollbar, and the text has a shadow effect that changes on hover.

### Expected Outcome:

A working custom Tailwind CSS plugin that adds new, reusable utility classes to your project. This exercise demonstrates how to extend Tailwind's functionality to meet specific project needs, promoting a more modular and powerful styling workflow.

### Extension Challenges:

-   Create a plugin that adds custom component classes (e.g., `.alert-success`, `.alert-warning`) using the `addComponents` function.
-   Make the `text-shadow` utility configurable through the `theme` object in `tailwind.config.js`.
-   Add a custom variant to your plugin (e.g., a `print:` variant that only applies styles when printing).

