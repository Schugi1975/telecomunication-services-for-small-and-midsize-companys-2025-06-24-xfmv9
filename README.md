# Connectics Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Connectics telecommunication services landing page. Follow these step-by-step instructions to make common updates while preserving the page's responsive design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header/Navigation (fixed at top)
- Hero Section (main banner)
- Features Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Hero Section
Located near the top of the page, find this section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Telecommunication Services for Small and Midsize Companies
</h1>
```
To update the main heading:
1. Locate the `<h1>` tag
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Fast Delivery</h3>
    <p class="text-gray-600">Quick implementation of your telecommunication solutions...</p>
</div>
```
To update feature cards:
1. Locate the feature section (id="features")
2. Find the specific card you want to update
3. Modify the `<h3>` title and `<p>` description text
4. Keep all existing classes to maintain styling

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- `text-4xl`: Base size for mobile
- `md:text-5xl`: Size for medium screens
- `lg:text-6xl`: Size for large screens

#### Common Tailwind Modifications

To adjust colors:
```html
<!-- Original blue button -->
<a class="bg-blue-600 text-white">

<!-- Change to green -->
<a class="bg-green-600 text-white">
```

To modify spacing:
```html
<!-- Original padding -->
<div class="p-8">

<!-- Increase padding -->
<div class="p-12">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure it matches the corresponding section's `id`
3. For external links, use the full URL:
```html
<a href="https://connectics.ch">Visit Website</a>
```

### External Links
Current external links that need attention:
- Main website: `https://connectics.ch`
- Email: `mailto:info@connectics.ch`

To update:
1. Find all instances of these links
2. Replace with your actual website URL and email
3. Test all links after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that all Tailwind CSS classes remain intact
   - Verify closing tags match opening tags
   - Ensure proper div nesting

2. **Non-Working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure section IDs match their corresponding links

3. **Responsive Issues**
   - Keep the responsive class prefixes (md:, lg:)
   - Test on multiple screen sizes
   - Maintain the existing container classes

### Need Help?
If you encounter issues:
1. Check the HTML structure matches the original
2. Verify all classes are spelled correctly
3. Test links in multiple browsers
4. Ensure all external resources (Tailwind CSS, Alpine.js) are loading

Remember to always make a backup before making changes, and test thoroughly across different devices and browsers.