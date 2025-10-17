# Mouse Follower & Color Changer Game

This project is a simple, single-file web application that tracks and displays the user's mouse coordinates in real-time, and includes a "game" element where the background color can be randomly changed by clicking a button. It's built using only HTML and vanilla JavaScript for a lightweight, self-contained experience.

## How to Use

1.  **Save the file:** Copy the entire `index.html` content and save it as `index.html` on your computer.
2.  **Open in browser:** Double-click the `index.html` file, or open it with any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  **Track Mouse:** Move your mouse cursor anywhere within the browser window. The X and Y coordinates of your cursor will be displayed and updated dynamically in the top-left corner of the page.
4.  **Change Color:** Click the "Change Background Color" button located in the center of the page. Each click will instantly change the background of the web page to a new, random color.

## Code Explanation

This application demonstrates fundamental web development concepts within a single HTML file:

*   **HTML Structure:**
    *   A `div` with the `id="coords-display"` serves as the container for showing the real-time mouse coordinates.
    *   A `button` with `id="color-changer-button"` acts as the interactive element for changing the background color.
    *   Standard `h1` and `p` tags provide introductory text and instructions to the user.

*   **CSS Styling (`<style>` tag):**
    *   The `body` is styled using Flexbox to center the main content vertically and horizontally, ensuring it takes up the full viewport height (`min-height: 100vh`). A `transition` property is applied to `background-color` for a smooth visual effect when the color changes.
    *   `#coords-display` uses `position: fixed` to keep the coordinate display visible in the top-left corner regardless of scrolling, with a semi-transparent background for readability.
    *   `#color-changer-button` is styled to be visually appealing and interactive, with `hover` and `active` states providing visual feedback to the user.

*   **JavaScript Logic (`<script>` tag):**
    *   **Mouse Tracking:** An `addEventListener` is attached to the `document` object to listen for `mousemove` events. Whenever the mouse moves, the event's `clientX` and `clientY` properties (representing the cursor's X and Y coordinates relative to the viewport) are used to update the `textContent` of the `coords-display` element.
    *   **Color Changer:** Another `addEventListener` is attached to the `color-changer-button` for `click` events. When the button is clicked, three random numbers between 0 and 255 are generated using `Math.random()` and `Math.floor()`. These numbers are then formatted into an `rgb()` string, which is applied to `document.body.style.backgroundColor`, thereby changing the page's background to a new random color.

## License

This project is licensed under the MIT License.