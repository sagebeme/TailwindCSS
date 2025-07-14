# 🏋️ Module 3 Exercises: Layout & Responsiveness

This module focuses on mastering Tailwind CSS utilities for creating flexible and adaptive layouts using Flexbox and Grid, along with responsive design principles.

## Exercise 3.1: Responsive Card Grid

**Objective**: Build a responsive grid of product cards that adapts to different screen sizes using Tailwind CSS Grid utilities.

**Time Estimate**: 60-75 minutes

**Prerequisites**: Basic HTML structure, understanding of Tailwind spacing and typography.

### Step-by-Step Instructions:

1.  **Setup**: Create a new HTML file (e.g., `responsive-card-grid.html`) and link the Tailwind CDN (or use your CLI setup).
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Responsive Card Grid</title>
        <script src="https://cdn.tailwindcss.com"></script>
    </head>
    <body class="bg-gray-100 p-8">
        <div class="container mx-auto">
            <h1 class="text-4xl font-bold text-center mb-8">Our Products</h1>
            <div id="product-grid">
                <!-- Product Cards will go here -->
            </div>
        </div>
    </body>
    </html>
    ```

2.  **Create a Single Product Card**: Inside the `#product-grid` div, add the HTML for one product card. Style it with basic Tailwind utilities.
    ```html
    <div class="bg-white rounded-lg shadow-md overflow-hidden">
        <img src="https://via.placeholder.com/400x300" alt="Product Image" class="w-full h-48 object-cover">
        <div class="p-6">
            <h2 class="text-xl font-semibold mb-2">Product Title</h2>
            <p class="text-gray-600 mb-4">Short description of the product. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            <div class="flex justify-between items-center">
                <span class="text-lg font-bold text-blue-600">$29.99</span>
                <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md">
                    Add to Cart
                </button>
            </div>
        </div>
    </div>
    ```

3.  **Duplicate Cards**: Duplicate the product card HTML 5-7 more times to have a total of 6-8 cards.

4.  **Apply Grid Layout**: To the `#product-grid` div, add the `grid` class. Then, apply responsive `grid-cols-*` classes:
    -   On mobile (default): `grid-cols-1`
    -   On small screens (`sm:`): `sm:grid-cols-2`
    -   On medium screens (`md:`): `md:grid-cols-3`
    -   On large screens (`lg:`): `lg:grid-cols-4`
    -   Add a `gap-6` to create space between cards.

    ```html
    <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <!-- Product Cards -->
    </div>
    ```

5.  **Test Responsiveness**: Open the `responsive-card-grid.html` file in your browser. Resize the browser window to see how the grid adapts. Observe how the number of columns changes at each breakpoint.

### Expected Outcome:

A visually appealing grid of product cards that automatically adjusts its column count based on the screen width. On small screens, cards should stack vertically. As the screen size increases, cards should arrange themselves into 2, 3, and then 4 columns.

### Extension Challenges:

-   Add a responsive image aspect ratio using `aspect-w-*` and `aspect-h-*` utilities (requires `@tailwindcss/aspect-ratio` plugin).
-   Implement a simple hover effect on the cards (e.g., `hover:shadow-xl`, `hover:scale-105`).
-   Add a filter/sort bar above the grid that uses Flexbox for alignment.

## Exercise 3.2: Responsive Header & Footer

**Objective**: Build a responsive header with a navigation menu and a responsive footer that adapts to mobile and desktop views.

**Time Estimate**: 45-60 minutes

**Prerequisites**: Basic HTML, understanding of Flexbox.

### Step-by-Step Instructions:

1.  **Setup**: Create a new HTML file (e.g., `responsive-header-footer.html`).
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Responsive Header & Footer</title>
        <script src="https://cdn.tailwindcss.com"></script>
    </head>
    <body class="flex flex-col min-h-screen">
        <header>
            <!-- Header content -->
        </header>

        <main class="flex-grow container mx-auto p-8">
            <h1 class="text-3xl font-bold text-center">Main Content Area</h1>
            <p class="text-center mt-4">Resize your browser to see the header and footer adapt!</p>
        </main>

        <footer>
            <!-- Footer content -->
        </footer>
    </body>
    </html>
    ```

2.  **Build the Header**: Inside the `<header>` tags, create a responsive navigation bar.
    -   Use `bg-blue-600` and `text-white` for background and text color.
    -   Use `container mx-auto px-4 py-4` for consistent padding and centering.
    -   Use `flex justify-between items-center` for logo and navigation alignment.
    -   For the navigation links (`<nav>` or `<div>` with `<a>` tags):
        -   On mobile, hide the links (`hidden`).
        -   On medium screens (`md:`), make them visible and use `md:flex md:space-x-6` to arrange them horizontally with spacing.
    -   Add a simple logo (e.g., `<span>` with `text-2xl font-bold`).

    ```html
    <header class="bg-blue-600 text-white shadow-lg">
        <div class="container mx-auto px-4 py-4">
            <div class="flex justify-between items-center">
                <span class="text-2xl font-bold">MyBrand</span>
                <nav class="hidden md:flex md:space-x-6">
                    <a href="#" class="hover:text-blue-200 transition-colors">Home</a>
                    <a href="#" class="hover:text-blue-200 transition-colors">Products</a>
                    <a href="#" class="hover:text-blue-200 transition-colors">About Us</a>
                    <a href="#" class="hover:text-blue-200 transition-colors">Contact</a>
                </nav>
                <!-- You can add a mobile menu toggle button here later -->
            </div>
        </div>
    </header>
    ```

3.  **Build the Footer**: Inside the `<footer>` tags, create a responsive footer.
    -   Use `bg-gray-800` and `text-white` for background and text color.
    -   Use `container mx-auto px-4 py-8` for consistent padding and centering.
    -   For the content (e.g., copyright, social links, quick links):
        -   On mobile, stack items vertically (`flex flex-col items-center space-y-4`).
        -   On medium screens (`md:`), arrange them horizontally (`md:flex md:justify-between md:items-center`).

    ```html
    <footer class="bg-gray-800 text-white mt-12">
        <div class="container mx-auto px-4 py-8">
            <div class="flex flex-col items-center space-y-4 md:flex-row md:justify-between md:items-center md:space-y-0">
                <p>&copy; 2024 MyBrand. All rights reserved.</p>
                <div class="flex space-x-4">
                    <a href="#" class="hover:text-gray-400 transition-colors">Privacy Policy</a>
                    <a href="#" class="hover:text-gray-400 transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
    ```

4.  **Test Responsiveness**: Open `responsive-header-footer.html` in your browser. Resize the window to observe how the header navigation and footer content change their layout at different breakpoints.

### Expected Outcome:

A web page with a header and footer that gracefully adapt to various screen sizes. The header navigation should hide on mobile and appear on desktop. The footer content should stack on mobile and spread out horizontally on desktop.

### Extension Challenges:

-   Implement a mobile menu toggle (hamburger icon) for the header using JavaScript to show/hide the navigation links on small screens.
-   Add social media icons to the footer using an icon library (e.g., Font Awesome) and style them with Tailwind.
-   Create a multi-column layout within the footer for quick links and contact information, using Grid.

## Exercise 3.3: Complex Form Layout

**Objective**: Design a multi-column, responsive contact form using a combination of Flexbox and Grid for optimal layout on all devices.

**Time Estimate**: 75-90 minutes

**Prerequisites**: Understanding of form elements, Flexbox, and Grid.

### Step-by-Step Instructions:

1.  **Setup**: Create a new HTML file (e.g., `responsive-form.html`).
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Responsive Contact Form</title>
        <script src="https://cdn.tailwindcss.com"></script>
    </head>
    <body class="bg-gray-100 flex items-center justify-center min-h-screen p-8">
        <div class="bg-white rounded-lg shadow-xl p-8 max-w-3xl w-full">
            <h1 class="text-3xl font-bold text-center mb-8">Contact Us</h1>
            <form>
                <!-- Form fields will go here -->
            </form>
        </div>
    </body>
    </html>
    ```

2.  **Basic Form Field Styling**: Create a reusable div for a form group (label + input). Style the label and input elements.
    ```html
    <div class="mb-4">
        <label for="name" class="block text-gray-700 text-sm font-bold mb-2">Name:</label>
        <input type="text" id="name" name="name" 
               class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
               placeholder="Your Name">
    </div>
    ```

3.  **Create Two-Column Layout (Name & Email)**: Place the 


Name and Email fields inside a grid container. Make it a single column on mobile and two columns on medium screens and up.
    ```html
    <div class="grid grid-cols-1 md:grid-cols-2 md:gap-6">
        <div class="mb-4">
            <label for="first-name" class="block text-gray-700 text-sm font-bold mb-2">First Name:</label>
            <input type="text" id="first-name" name="first-name" 
                   class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
                   placeholder="John">
        </div>
        <div class="mb-4">
            <label for="last-name" class="block text-gray-700 text-sm font-bold mb-2">Last Name:</label>
            <input type="text" id="last-name" name="last-name" 
                   class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
                   placeholder="Doe">
        </div>
    </div>
    <div class="mb-4">
        <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email:</label>
        <input type="email" id="email" name="email" 
               class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
               placeholder="your.email@example.com">
    </div>
    ```

4.  **Add Subject and Message Fields**: Add a subject line (full width) and a textarea for the message (full width).
    ```html
    <div class="mb-4">
        <label for="subject" class="block text-gray-700 text-sm font-bold mb-2">Subject:</label>
        <input type="text" id="subject" name="subject" 
               class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
               placeholder="Subject of your message">
    </div>
    <div class="mb-6">
        <label for="message" class="block text-gray-700 text-sm font-bold mb-2">Message:</label>
        <textarea id="message" name="message" rows="5"
                  class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:ring-2 focus:ring-blue-500"
                  placeholder="Your message here..."></textarea>
    </div>
    ```

5.  **Add Checkbox and Submit Button**: Use Flexbox to align a checkbox and a submit button.
    ```html
    <div class="flex items-center justify-between">
        <div class="flex items-center">
            <input type="checkbox" id="terms" name="terms" class="h-4 w-4 text-blue-600 focus:ring-blue-500 border-gray-300 rounded">
            <label for="terms" class="ml-2 block text-sm text-gray-900">I agree to the terms</label>
        </div>
        <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">
            Send Message
        </button>
    </div>
    ```

6.  **Test Responsiveness**: Open `responsive-form.html` in your browser. Resize the window to see how the form fields adapt. The first name and last name fields should be stacked on mobile and side-by-side on larger screens.

### Expected Outcome:

A clean, professional, and responsive contact form. The layout should be easy to use on mobile devices, with fields stacking vertically. On larger screens, the layout should utilize the available space by placing some fields side-by-side, creating a more compact and visually appealing form.

### Extension Challenges:

-   Add validation styling for form fields (e.g., red borders for errors, green for success) using JavaScript and Tailwind classes.
-   Implement a custom-styled select dropdown for a "department" field.
-   Create a more complex grid layout for the form, perhaps with a sidebar for contact information next to the form fields on larger screens.
-   Add a file upload field with custom styling.

