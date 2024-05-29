# counter-app

# HTML 
```markdown
```html
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
                <h1 class="nav-h1">Counter App</h1>
                <!-- Header title -->
                <i class="fa-solid fa-stopwatch-20"></i>
                <!-- Icon for navigation -->
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
