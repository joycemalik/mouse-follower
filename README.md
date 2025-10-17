# Mouse Follower & Color Game

A simple, single-page web application that tracks and displays your mouse coordinates in real-time. It also includes a fun "game" feature: a button that changes the background color of the page to a random color when clicked.

## How to Use

1.  Save the provided HTML content into a file named `index.html`.
2.  Open `index.html` using any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  Move your mouse cursor anywhere on the page, and the displayed coordinates will update dynamically.
4.  Click the "Change Background Color" button to instantly change the page's background to a new, random color.

## Code Explanation

This project is a single `index.html` file, containing all the HTML structure, CSS styling, and JavaScript logic.

*   **HTML Structure:**
    *   A `div` with the ID `coordinates` is used to display the current X and Y position of the mouse.
    *   A `button` with the ID `colorButton` is provided for the background color changing game.

*   **CSS Styling:**
    *   Basic styling is applied to the `body` to center content and provide a default background.
    *   The `#coordinates` div is styled for prominence and readability.
    *   The `#colorButton` is styled to be visually appealing and provide hover/active feedback.
    *   A `transition` property on the `body` ensures smooth color changes.

*   **JavaScript Logic:**
    *   **Mouse Tracking:** An `mousemove` event listener is attached to the `document`. This listener continuously updates the `textContent` of the `coordinatesDiv` with the `clientX` and `clientY` properties of the event object, which represent the mouse's horizontal and vertical coordinates relative to the viewport.
    *   **Random Background Color:** A `click` event listener is attached to the `colorButton`. When clicked, it calls `getRandomRgbColor()` to generate a new `rgb()` color string. This random color is then applied to `document.body.style.backgroundColor`, changing the page's background.

## License

This project is licensed under the MIT License.