# counter-app 

# HTML 
```markdown

<!DOCTYPE html>
```
- Specifies the document type and version of HTML being used.

## Document Structure
```html
<html lang="en">
```
- Defines the root element of the HTML document and specifies the language as English.

## Head Section
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
        integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="styles.css" />
    <title>Counter App</title>
</head>
```
- Contains meta information and external resources used by the document, such as character encoding, viewport settings, favicon, font-awesome CSS, custom CSS, and the document title.

## Body Section
```html
<body>
    <!-- Navigation -->
    <nav>
        <!-- Main navigation container -->
        <div class="nav-main">
            <!-- Navigation header -->
            <div class="nav-header">
                <!-- Header title -->
                <h1 class="nav-h1">Counter App</h1>
                <!-- Icon for navigation -->
                <i class="fa-solid fa-stopwatch-20"></i>
            </div>
            <!-- Menu links -->
            <ul class="menu">
                <li>
                    <a href="#">Home</a>
                </li>
                <li>
                    <a href="#">About</a>
                </li>
                <li>
                    <a href="#">Contact</a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- Main content container -->
    <div class="container">
        <!-- Counter section -->
        <div class="counter-div">
            <!-- Display count -->
            <span class="count">0</span>
            <!-- Horizontal line -->
            <hr style="width: 100%;" />
            <!-- Buttons for manipulating count -->
            <div class="buttons">
                <!-- Subtract button -->
                <button class="subtract" title="Decrease ">
                    <i class="fa-regular fa-hand-point-down downhand-styles subtract"></i>
                </button>
                <!-- Reset button -->
                <button class="reset" title="Reset ">
                    <i class="fa-solid fa-hand-sparkles reset"></i>
                </button>
                <!-- Add button -->
                <button class="add" title="Increase ">
                    <i class="fa-regular fa-hand-point-up uphand-styles add"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- JavaScript file -->
    <script src="script.js"></script>
</body>
```
- Defines the structure and content of the document body, including navigation, counter section, and script inclusion for JavaScript functionality.

These notes provide an overview of the structure and key elements of the HTML document.

# CSS 

1. **Font Imports**:
   - Two fonts are imported from Google Fonts: Roboto (weights 400 and 700) and Montserrat (weight 900).

2. **Global Styles**:
   - `*` selector applies `box-sizing: border-box` to all elements, ensuring consistent box models.
   - `body` styles set the default font family to 'Roboto', 'Montserrat', and sans-serif, along with resetting margin, padding, line-height, font-size, and background color.
   - `ul` removes default list-style-type.
   - `a` removes default text-decoration.
   - `nav` styling includes a background color (#3F72AF) and a box-shadow effect.

3. **Menu Styles**:
   - `.menu a` styles menu links with specific colors, font-weight, font-size, letter-spacing, padding, and a transition effect.
   - `:hover` effect changes the color and font-weight of menu links and increases the padding on the left.

4. **Header Styles**:
   - `.nav-header` sets up a flex container with specific alignment and padding.
   - `h1` and `.nav-h1` define styles for header titles with different font sizes and colors.

5. **Container Styles**:
   - `.container` sets the maximum width, margins, padding, and alignment for the main content container.

6. **Counter Styles**:
   - `.counter-div` styles a container for displaying a counter with specific width, border, padding, background color, text color, text alignment, border-radius, and box-shadow.
   - `.count` defines the font size for the counter number.

7. **Button Styles**:
   - `.buttons button` styles buttons with padding, margin, font size, color, font-weight, border, outline, border-radius, cursor, and box-shadow.
   - Specific classes like `button.subtract`, `button.reset`, and `button.add` set different background colors for buttons.

8. **Hand Styles**:
   - `.uphand-styles` and `.downhand-styles` define specific colors for hand icons.

9. **Media Queries**:
   - Adjustments for screens wider than 800px:
     - `.nav-main` adjusts its maximum width, margin, and display properties.
     - `.nav-header` removes padding.
     - `.menu` adjusts its height and display properties.
     - `.menu a` adjusts padding and margin.
     - `.menu a:hover` changes padding and background to transparent on hover.

# JavaScript

This JavaScript code is designed to interact with a webpage where there's a counter displayed and buttons to manipulate its value. Let's break down its functionality:

1. **Selecting Elements**:
   - `const count = document.querySelector(".count");`: Selects the element with the class "count", which likely represents the counter display.
   - `const buttons = document.querySelector(".buttons");`: Selects the element with the class "buttons", which likely represents the container for the buttons.

2. **Event Listener**:
   - `buttons.addEventListener("click", (e) => { ... });`: Listens for click events on the "buttons" container. When a click occurs, it executes the callback function.

3. **Event Handling**:
   - `console.log(e.target.classList);`: Logs the class list of the clicked element to the console.
   - Conditional statements check which button was clicked based on its class:
     - `if (e.target.classList.contains("add")) { ... }`: If the clicked element has the class "add", increment the counter value displayed.
     - `if (e.target.classList.contains("subtract")) { ... }`: If the clicked element has the class "subtract", decrement the counter value displayed.
     - `if (e.target.classList.contains("reset")) { ... }`: If the clicked element has the class "reset", reset the counter value displayed to zero.

4. **Color Change**:
   - `setColor()` function is called after each button click to update the color of the counter based on its value.
   - Inside `setColor()`, the color of the counter text is changed based on its value:
     - If the value is greater than 0, the color is set to "greenyellow".
     - If the value is less than 0, the color is set to "#fe9f7d".
     - If the value is 0, the color is set to "#fff" (white).

Overall, this script creates an interactive counter where clicking on specific buttons increments, decrements, or resets the counter value, and the color of the counter text changes accordingly.
