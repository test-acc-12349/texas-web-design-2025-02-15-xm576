# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text**
```html
<!-- Find this section -->
<a href="/" class="text-2xl font-bold text-gray-800">
    TWD
</a>

<!-- Replace "TWD" with your desired text -->
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <!-- Each menu item follows this pattern -->
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6">
    Texas Web Design  <!-- Replace this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-200 mb-12">
    Best Websites In Texas  <!-- Replace this text -->
</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `text-[color]`: Controls text color (e.g., `text-gray-800`, `text-white`)
- `mb-[size]`: Controls bottom margin (e.g., `mb-6`, `mb-12`)

## Managing Links

### Navigation Menu Links
Current navigation links to update:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. For internal links (same page), use `#section-id`
4. For external links, use full URL (e.g., `https://example.com`)

### Call-to-Action (CTA) Links
Update the "Get Started" buttons:

```html
<!-- Header CTA -->
<a href="https://twd.com" class="hidden md:inline-block px-6 py-2">
    Get Started
</a>

<!-- Hero Section CTA -->
<a href="https://twd.com" class="inline-block px-8 py-4">
    Start Your Project
</a>
```

Replace `https://twd.com` with your actual website URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the footer links section:

```html
<div>
    <h4 class="text-lg font-semibold mb-6 text-white">Links</h4>
    <ul class="space-y-4">
        <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Blog</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms</a></li>
        <!-- Add new links here -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - IDs must be unique
   - Check for typos in href values

2. **Responsive Design Issues**
   - Keep the `md:` prefix for desktop-specific styles
   - Don't remove `container` and `mx-auto` classes
   - Maintain the existing responsive class structure

3. **Missing Icons**
   - Verify Font Awesome CDN link is present in `<head>`
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all CDN links are accessible
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code

Remember to always backup your files before making changes, and test your updates across different devices and browsers.