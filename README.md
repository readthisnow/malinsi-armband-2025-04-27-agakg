# Malinsi Landing Page - Maintenance Guide

This guide will help you maintain and customize the Malinsi landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Malinsi" to your brand name:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Malinsi</a>
```

2. **Navigation Items**: Locate these lines to modify menu items:
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Voordelen</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
```

### Hero Section
The main banner section contains:

1. **Main Heading**: Update this text:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Koop Malinsi Armband Met Korting</h1>
```

2. **Subheading**: Modify this line:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12">Exclusief design, beperkte voorraad beschikbaar</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-300`, `bg-gray-900`
- Spacing: `px-6`, `py-4`, `mb-8`
- Responsive prefixes: `md:`, `lg:`

Example of changing text size:
```html
<!-- Original -->
<p class="text-xl">Your text</p>

<!-- Larger text -->
<p class="text-2xl">Your text</p>
```

## Managing Links

### Navigation Links
1. Internal section links are prefixed with #:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```

2. Call-to-action buttons use external links:
```html
<a href="https://amzn.to/4iy8qd2" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">Koop Nu</a>
```

### Updating External Links
1. Find all Amazon links (currently `https://amzn.to/4iy8qd2`)
2. Replace with your product URL
3. Test each link after updating

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">Instagram</a>
    <a href="#" class="text-gray-400 hover:text-white">Facebook</a>
</div>
```

Replace `#` with your social media profiles.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace these placeholder links:
```html
<!-- Original -->
<li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>

<!-- Updated -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Step 3: Style Consistency
Ensure your new pages use the same styling:
```html
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <!-- Copy the same head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 font-sans antialiased">
    <!-- Your privacy/terms content here -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing classes
   - Verify responsive class prefixes (`md:`, `lg:`)

3. **Layout Issues**
   - Check container classes: `container mx-auto px-6`
   - Verify grid classes: `grid grid-cols-1 md:grid-cols-2`
   - Ensure proper nesting of flex containers

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check HTML validity using [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes and test on multiple devices after updates.