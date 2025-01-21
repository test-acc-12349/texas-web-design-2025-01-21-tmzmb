# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Texas Web Design  <!-- Change this text to update company name -->
</a>
```

#### Navigation Menu Items
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Websites In Texas  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Creating high-converting... <!-- Subheading text -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold, medium)
- `bg-{color}`: Sets background color
- `p-{size}`: Sets padding (4, 6, 8, etc.)
- `mb-{size}`: Sets margin bottom
- `md:`: Applies styles only on medium screens and up

## Fixing Broken Links

### Current Link Structure
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="...">
    Get Started
</a>
```

### How to Update Links
1. For internal section links (starting with #):
   - Ensure the href matches the section ID
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Replace `https://twd.com` with your actual website URL
   - Example: `<a href="https://yourwebsite.com">`

3. Email links in contact section:
```html
<!-- Update email address here -->
<p class="text-xl mb-10">Contact us at admin@twd.com</p>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:

```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create two new files:
   - privacy.html
   - terms.html
2. Copy the header and footer from index.html to maintain consistent styling

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#Features"` won't link to `id="features"`

2. Responsive Design Issues
   - Check mobile view using browser dev tools
   - Ensure `md:` classes are used for responsive layouts
   - Don't remove `hidden md:flex` from navigation menu

3. Gradient Text Not Showing
   - Verify all three classes are present:
     ```html
     bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent
     ```

### Need Help?
- Check the Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness at different screen sizes

Remember to always backup your files before making changes, and test thoroughly after each modification.