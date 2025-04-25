# Thrapston Accountants Landing Page - Maintenance Guide

This guide will help you maintain and customize the Thrapston Accountants landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing and Managing Links](#fixing-and-managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Thrapston</a>
```
- Replace "Thrapston" with your company name
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Expert Accountants for UK Small Businesses
</h1>
```
- Replace the headline text while keeping the HTML tags
- Size classes explanation:
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-pound-sign text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">No Monthly Fees</h3>
    <p class="text-gray-600">Transparent pricing structure...</p>
</div>
```
To modify:
1. Change the icon by updating the `fas fa-pound-sign` class
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Fixing and Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure the referenced section has matching ID
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://www.yoursite.com/services"`

### Call-to-Action Links
Update all instances of the website URL:
```html
<a href="https://www.thrapstonaccounting.com" class="inline-block bg-blue-600...">
```
Replace with your actual website URL.

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-3">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - Example: `href="#features"` needs `id="features"` on target section

2. **Responsive Design Issues**
   - Check responsive classes are properly set:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)

### Need More Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Ensure all files are in the correct directory
- Verify all HTML tags are properly closed

Remember to test all changes across different devices and screen sizes before deploying to production.