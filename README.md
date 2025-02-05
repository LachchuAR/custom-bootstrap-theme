# Bootstrap 5.3.3 Custom Theme

## Overview

This project customizes **Bootstrap 5.3.3** by overriding default theme colors and adding new custom colors using SCSS. A sample HTML file is included to demonstrate Bootstrap components with the modified theme.

## Features

- Customized **Bootstrap 5.3.3** theme
- Overridden default Bootstrap color variables
- Additional custom colors (`custom-primary`, `custom-secondary`)
- Styled Bootstrap buttons, accordions, and UI elements
- Uses **Live Sass Compiler** for SCSS compilation

## Installation & Setup

Follow these steps to set up the project locally:

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone (https://github.com/LachchuAR/custom-bootstrap-theme.git)
cd bootstrap-custom-theme
```

### 2. Install Dependencies

Run the following command to install Bootstrap and other required dependencies:

```bash
npm install
```

### 3. Install Live Sass Compiler Extension (VS Code)

Since this project uses **Live Sass Compiler**, install it in VS Code:

1. Open **VS Code**
2. Go to **Extensions** (`Ctrl + Shift + X`)
3. Search for **Live Sass Compiler**
4. Click **Install**

### 4. Compile SCSS to CSS

1. Open the project in VS Code
2. Right-click on `src/main.scss`
3. Select **"Watch Sass"** from the context menu
4. The compiler will generate `src/main.css`
5. Include the compiled CSS in your HTML file:
   ```html
   <link rel="stylesheet" href="src/main.css">
   ```

## Project Structure

```
/bootstrap-custom-theme
  ├── node_modules/        # Bootstrap package (installed via npm)
  ├── src/                
  │   ├── main.css         # Compiled CSS file (Generated by Live Sass Compiler)
  │   ├── main.scss        # Main SCSS file importing Bootstrap
  │   ├── index.html       # Demo page with Bootstrap components
  ├── package.json         # NPM package file
  ├── .gitignore           # Ignore unnecessary files from Git
  ├── README.md            # Documentation file
```

## SCSS Customization (`src/main.scss`)

### Overridden Bootstrap Colors:

```scss
$primary: #ff0062;
$secondary: #6db629;
$success: #28a745;
$info: #17a2b8;
$warning: #ffc107;
$danger: #dc3545;
$light: #f8f9fa;
$dark: #343a40;
```

### Added Custom Colors:

```scss
$custom-primary: #007bff;
$custom-secondary: #6c757d;
```

### Updated Theme Colors Map:

```scss
$theme-colors: (
  "primary":    $primary,
  "secondary":  $secondary,
  "success":    $success,
  "info":       $info,
  "warning":    $warning,
  "danger":     $danger,
  "light":      $light,
  "dark":       $dark,
  "custom-primary": $custom-primary,
  "custom-secondary": $custom-secondary,
);
```

### Import Bootstrap in SCSS (`src/main.scss`)

```scss
@import "../node_modules/bootstrap/scss/bootstrap";
```

## Usage in HTML (`src/index.html`)

- **Include Bootstrap JS**:
  ```html
  <script src="../node_modules/bootstrap/dist/js/bootstrap.bundle.min.js"></script>
  ```

- **Example: Custom Buttons**
  ```html
  <button class="btn btn-custom-primary">Custom Primary</button>
  <button class="btn btn-custom-secondary">Custom Secondary</button>
  ```

**Note: Without cloning the repository, follow these steps:**

### 1. Initialize NPM Project

First, create a new project folder and initialize it with `npm`:

```bash
mkdir bootstrap-custom-theme
cd bootstrap-custom-theme
npm init -y

npm install bootstrap@5.3.3

### Note: To get the latest version of Bootstrap, visit the official Bootstrap website and check for the most up-to-date version. Replace 5.3.3 with the desired version. (https://getbootstrap.com) 

### Created by LachchuAR

For more information, feel free to reach out or check out my work at [GitHub - LachchuAR](https://github.com/LachchuAR).
