# IT-Breeze Landing Page Maintenance Guide

This guide will help you maintain and customize the IT-Breeze landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
```html
<a href="/" class="text-2xl font-bold text-blue-600">IT-Breeze</a>
```
- To change the company name, replace "IT-Breeze" with your desired text
- Adjust text size using classes like `text-xl`, `text-2xl`, or `text-3xl`
- Modify color using `text-[color]-[shade]` (e.g., `text-blue-600`)

### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Website Development in Malta
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Create stunning website for an affordable price
</p>
```
- Update headings by replacing text between `<h1>` tags
- Modify subheading by changing text between `<p>` tags
- Responsive text sizes are controlled by:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Feature Cards
Each feature card follows this structure:
```html
<div class="p-8 rounded-xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-mobile-alt text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Responsive Design</h3>
    <p class="text-gray-600">Websites that look perfect on any device...</p>
</div>
```
To modify:
1. Change icon: Replace `fa-mobile-alt` with any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading: Replace text between `<h3>` tags
3. Update description: Modify text between `<p>` tags

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
1. Identify the section ID you want to link to
2. Update the `href` attribute to match the section ID
3. Example: `<a href="#new-section">New Section</a>`

### External Links
To update the "Get Started" button:
```html
<a href="https://it-breeze.info" class="inline-block bg-blue-600...">
    Get Started Today
</a>
```
Replace `https://it-breeze.info` with your desired URL

### Email Links
```html
<a href="mailto:info@it-breeze.info">Get in Touch</a>
```
Replace `info@it-breeze.info` with your contact email

## Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check that you haven't removed any essential Tailwind classes
- Verify all `div` tags are properly closed
- Ensure responsive classes (md:, lg:) remain intact

2. **Missing Icons**
- Verify Font Awesome is properly loaded
- Check icon class names against Font Awesome documentation
- Ensure the icon prefix (fas, far, fab) matches the icon type

3. **Non-working Links**
- Verify file paths are correct
- Check that section IDs match their corresponding href attributes
- Ensure external URLs include the proper protocol (https://)

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all changes against this original HTML
3. Test responsiveness at different screen sizes
4. Ensure all required CDN links remain in the head section

Remember to always backup your files before making changes!