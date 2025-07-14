# 🏋️ Module 1 Exercises: Introduction to Tailwind CSS & Setup

These exercises are designed to help you solidify your understanding of Tailwind CSS fundamentals, including its philosophy, setup methods, configuration, and responsive design principles. Follow the step-by-step instructions carefully, and don't hesitate to experiment!

## Exercise 1.1: Tailwind CSS CDN Quick Start

**Objective**: Get a basic understanding of Tailwind CSS by using its CDN and applying some core utility classes.

**Time**: 30 minutes

**Prerequisites**:
- A text editor (like VS Code).
- A web browser.

**Instructions**:

1.  **Create a new HTML file**: Save it as `index.html` in a new folder (e.g., `tailwind-cdn-project`).

2.  **Add basic HTML structure**: Include the necessary `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags.

3.  **Include the Tailwind CSS CDN**: Place the following `<script>` tag inside your `<head>` section:
    ```html
    <script src="https://cdn.tailwindcss.com"></script>
    ```

4.  **Add a simple heading**: Inside your `<body>`, add an `<h1>` tag with some text, e.g., "Hello, Tailwind CSS!".

5.  **Apply basic Tailwind utility classes to the heading**: Add the following classes to your `<h1>` tag:
    -   `text-4xl`: Makes the text large.
    -   `font-bold`: Makes the text bold.
    -   `text-blue-600`: Sets the text color to a shade of blue.
    -   `p-8`: Adds padding around the heading.
    -   `text-center`: Centers the text.

    Your `<h1>` tag should look something like this:
    ```html
    <h1 class="text-4xl font-bold text-blue-600 p-8 text-center">
        Hello, Tailwind CSS!
    </h1>
    ```

6.  **Create a simple card**: Below your heading, add a `<div>` element that will serve as a card. Give it some content, like a paragraph and a button.

7.  **Style the card using Tailwind utilities**: Apply the following classes to your card `<div>`:
    -   `bg-white`: White background.
    -   `p-6`: Padding inside the card.
    -   `rounded-lg`: Rounded corners.
    -   `shadow-xl`: A large shadow.
    -   `max-w-sm`: Maximum width of small size.
    -   `mx-auto`: Center the block horizontally.
    -   `mt-10`: Margin top.

    For the paragraph inside the card:
    -   `text-gray-700`: Dark gray text color.
    -   `mb-4`: Margin bottom.

    For the button inside the card:
    -   `bg-green-500`: Green background.
    -   `hover:bg-green-700`: Darker green on hover.
    -   `text-white`: White text.
    -   `font-bold`: Bold font.
    -   `py-2`: Vertical padding.
    -   `px-4`: Horizontal padding.
    -   `rounded`: Rounded corners.
    -   `mt-4`: Margin top.

    Your card structure should resemble this:
    ```html
    <div class="bg-white p-6 rounded-lg shadow-xl max-w-sm mx-auto mt-10">
        <p class="text-gray-700 mb-4">
            This is a simple card demonstrating Tailwind CSS utility classes via CDN.
        </p>
        <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded mt-4">
            Click Me
        </button>
    </div>
    ```

8.  **Open `index.html` in your browser**: Observe how the styles are applied. Try changing some class values (e.g., `text-red-500`, `p-10`) and refresh the browser to see the immediate changes.

**Expected Outcome**:
-   A web page with a large, blue, centered heading.
-   A white card with rounded corners, a shadow, centered on the page, containing a paragraph and a green button.
-   The button changes color when you hover over it.

**Extension Challenges**:
1.  Change the background color of the `<body>` using a Tailwind class (e.g., `bg-gray-100`).
2.  Add a border to the card using `border` and `border-gray-300` classes.
3.  Experiment with different font sizes (`text-sm`, `text-lg`, `text-xl`) and font weights (`font-light`, `font-medium`) on the paragraph text.

## Exercise 1.2: Setting Up a Tailwind Project with CLI

**Objective**: Set up a Tailwind CSS project using Node.js, npm, and the Tailwind CSS CLI, which is the recommended approach for production.

**Time**: 45 minutes

**Prerequisites**:
-   Node.js and npm installed on your system. You can download them from [nodejs.org](https://nodejs.org/).
-   A terminal or command prompt.

**Instructions**:

1.  **Create a new project directory**: Open your terminal and create a new folder for this exercise. Navigate into it.
    ```bash
    mkdir tailwind-cli-project
    cd tailwind-cli-project
    ```

2.  **Initialize a new npm project**: This creates a `package.json` file.
    ```bash
    npm init -y
    ```

3.  **Install Tailwind CSS, PostCSS, and Autoprefixer**: Install these as development dependencies.
    ```bash
    npm install -D tailwindcss postcss autoprefixer
    ```

4.  **Generate Tailwind and PostCSS config files**: This creates `tailwind.config.js` and `postcss.config.js`.
    ```bash
    npx tailwindcss init -p
    ```

5.  **Configure `tailwind.config.js`**: Open `tailwind.config.js` and update the `content` array to include your HTML files. For this exercise, we'll assume your HTML file is in the root directory.
    ```javascript
    // tailwind.config.js
    module.exports = {
      content: [
        "./*.html", // Look for Tailwind classes in all HTML files in the root directory
      ],
      theme: {
        extend: {},
      },
      plugins: [],
    }
    ```

6.  **Create your input CSS file**: Create a file named `input.css` (or `src/input.css`) in your project root and add the Tailwind directives:
    ```css
    /* input.css */
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

7.  **Add a build script to `package.json`**: Open `package.json` and add the `build:css` script under the `scripts` section. This script will compile your Tailwind CSS.
    ```json
    // package.json
    "scripts": {
      "build:css": "tailwindcss -i ./input.css -o ./output.css --watch",
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    ```

8.  **Create your `index.html` file**: Create `index.html` in your project root and link to the `output.css` file that will be generated.
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Tailwind CLI Project</title>
        <link href="./output.css" rel="stylesheet">
    </head>
    <body>
        <div class="min-h-screen flex items-center justify-center bg-gradient-to-r from-purple-400 via-pink-500 to-red-500">
            <div class="bg-white p-10 rounded-xl shadow-2xl text-center transform transition-all duration-500 hover:scale-105">
                <h1 class="text-5xl font-extrabold text-gray-800 mb-4">Hello from CLI!</h1>
                <p class="text-lg text-gray-600 mb-6">This project is set up with Tailwind CSS CLI.</p>
                <button class="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-8 rounded-full shadow-lg transform hover:translate-y-1 transition-all duration-300">
                    Discover More
                </button>
            </div>
        </div>
    </body>
    </html>
    ```

9.  **Run the build process**: Open your terminal and run the build script. Keep this terminal window open as it will watch for changes.
    ```bash
    npm run build:css
    ```
    You should see `output.css` generated in your project directory.

10. **Open `index.html` in your browser**: Verify that the styles are applied correctly. Try changing some classes in `index.html` (e.g., `bg-blue-600` to `bg-green-600`) and save. The `output.css` should recompile, and upon refreshing your browser, you should see the changes.

**Expected Outcome**:
-   A fully functional Tailwind CSS project set up using the CLI.
-   `output.css` file is generated and contains the necessary Tailwind styles.
-   Changes to HTML classes are reflected in the browser after recompilation.

**Extension Challenges**:
1.  Install a local development server (e.g., `npm install -g live-server` then `live-server` in your project folder) to automatically refresh the browser on file changes.
2.  Add a new HTML file (e.g., `about.html`) and link `output.css` to it. Add some Tailwind classes and verify they work.
3.  Try adding a custom CSS rule directly in `input.css` (e.g., `.my-custom-class { @apply text-red-500; }`) and use it in your HTML.

## Exercise 1.3: Customizing Tailwind's Theme

**Objective**: Learn how to customize Tailwind CSS by extending and overwriting its default theme in `tailwind.config.js`.

**Time**: 40 minutes

**Prerequisites**:
-   Completed Exercise 1.2 (Tailwind CLI project setup).

**Instructions**:

1.  **Open `tailwind.config.js`**: This is where you'll make all your customizations.

2.  **Extend the color palette**: Add a new brand color and extend an existing color. Inside `theme.extend.colors`, add:
    ```javascript
    // tailwind.config.js
    module.exports = {
      // ...
      theme: {
        extend: {
          colors: {
            'primary-brand': '#FF6347', // Tomato red
            'secondary-brand': '#4682B4', // Steel blue
            // Extend an existing color (e.g., gray) with a new shade
            gray: {
              '950': '#0d0d0d',
            },
          },
        },
      },
      // ...
    }
    ```

3.  **Use the new colors in `index.html`**: Apply your new custom colors to elements in your `index.html`.
    ```html
    <h1 class="text-primary-brand">My Custom Brand Heading</h1>
    <p class="text-secondary-brand">This text uses the secondary brand color.</p>
    <div class="bg-gray-950 p-4 text-white">Dark background with custom gray.</div>
    ```

4.  **Extend the font family**: Add a custom font stack. Inside `theme.extend.fontFamily`, add:
    ```javascript
    // tailwind.config.js
    module.exports = {
      // ...
      theme: {
        extend: {
          fontFamily: {
            'sans': ['Inter', 'ui-sans-serif', 'system-ui', '-apple-system', 'BlinkMacSystemFont', '"Segoe UI"', 'Roboto', '"Helvetica Neue"', 'Arial', '"Noto Sans"', 'sans-serif', '"Apple Color Emoji"', '"Segoe UI Emoji"', '"Segoe UI Symbol"', '"Noto Color Emoji"'],
            'heading': ['Montserrat', 'sans-serif'], // Add a new custom font family
          },
        },
      },
      // ...
    }
    ```
    *Note: For `Inter` and `Montserrat` to work, you'd typically link them from Google Fonts in your HTML. For this exercise, assume they are available or use system fonts.* For simplicity, you can just add a unique name like `'my-custom-font': ['"Comic Sans MS"', 'cursive']` to see the effect.

5.  **Apply the custom font in `index.html`**: Use the `font-heading` class.
    ```html
    <h2 class="font-heading text-3xl mt-8">A Heading with a Custom Font</h2>
    ```

6.  **Extend spacing values**: Add larger spacing options. Inside `theme.extend.spacing`, add:
    ```javascript
    // tailwind.config.js
    module.exports = {
      // ...
      theme: {
        extend: {
          spacing: {
            '128': '32rem',
            '144': '36rem',
          },
        },
      },
      // ...
    }
    ```

7.  **Use the new spacing in `index.html`**: Apply the new spacing classes.
    ```html
    <div class="h-128 bg-blue-100 w-full mt-10"></div>
    <div class="h-144 bg-green-100 w-full mt-10"></div>
    ```

8.  **Observe changes**: Ensure your `npm run build:css` script is running. Refresh your browser to see the applied custom styles.

**Expected Outcome**:
-   Your HTML elements use the new `primary-brand`, `secondary-brand`, and `gray-950` colors.
-   The `font-heading` class applies your chosen custom font.
-   The `h-128` and `h-144` classes correctly set the height of elements.

**Extension Challenges**:
1.  **Overwrite a default color**: Try overwriting the default `blue` color palette (by placing `colors` directly under `theme` instead of `theme.extend`). Observe what happens to `text-blue-600` if you don't redefine it.
2.  **Add custom breakpoints**: Define a new breakpoint (e.g., `'tablet': '768px'`) in `theme.extend.screens` and use it in your HTML.
3.  **Add custom box shadows**: Extend `boxShadow` with a unique shadow style.

## Exercise 1.4: Responsive Design with Breakpoints

**Objective**: Practice building responsive layouts using Tailwind CSS's mobile-first breakpoint system.

**Time**: 35 minutes

**Prerequisites**:
-   Completed Exercise 1.2 (Tailwind CLI project setup).

**Instructions**:

1.  **Create a responsive text element**: Add a `<div>` with text that changes alignment based on screen size.
    ```html
    <div class="text-center sm:text-left md:text-right lg:text-center p-4 bg-yellow-100 mt-10">
        This text changes alignment based on screen size.
    </div>
    ```

2.  **Create a responsive grid layout**: Build a simple grid of items that changes column count on different breakpoints.
    ```html
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-4 mt-10">
        <div class="bg-blue-200 p-4 rounded text-center">Item 1</div>
        <div class="bg-blue-200 p-4 rounded text-center">Item 2</div>
        <div class="bg-blue-200 p-4 rounded text-center">Item 3</div>
        <div class="bg-blue-200 p-4 rounded text-center">Item 4</div>
        <div class="bg-blue-200 p-4 rounded text-center">Item 5</div>
        <div class="bg-blue-200 p-4 rounded text-center">Item 6</div>
    </div>
    ```

3.  **Implement a responsive image visibility**: Show/hide an image based on screen size.
    ```html
    <img src="https://via.placeholder.com/300" alt="Placeholder Image" class="hidden md:block mx-auto mt-10">
    <p class="block md:hidden text-center mt-4">Image hidden on small screens.</p>
    ```
    *Note: You can replace `https://via.placeholder.com/300` with any image URL.*

4.  **Test responsiveness**: Open `index.html` in your browser. Resize your browser window or use your browser's developer tools (F12, then toggle device toolbar) to simulate different screen sizes. Observe how the layout and element visibility change at each breakpoint.

**Expected Outcome**:
-   The text alignment changes as you resize the browser window.
-   The grid layout adapts, showing 1, 2, 3, or 4 columns based on the screen width.
-   The image appears only on medium screens and larger, and the text message appears only on small screens.

**Extension Challenges**:
1.  Create a responsive navigation bar that stacks vertically on small screens and becomes horizontal on larger screens using Flexbox utilities and responsive prefixes.
2.  Design a responsive pricing table with 3 columns that collapse into a single column on mobile.
3.  Experiment with `min-w-`, `max-w-`, `min-h-`, `max-h-` utilities combined with responsive prefixes.

---

**Congratulations!** You've completed the first module's exercises. You should now have a solid grasp of Tailwind CSS's core philosophy, how to set up a project, customize its theme, and build responsive designs using its powerful breakpoint system. Keep practicing and experimenting with these concepts!

