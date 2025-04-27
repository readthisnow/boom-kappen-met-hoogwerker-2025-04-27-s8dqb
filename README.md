# Landing Page Maintenance Guide

This guide will help you maintain and customize the BoomKappen landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-emerald-600">BoomKappen</a>
```
- Replace `BoomKappen` with your company name
- Adjust size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)
- Change color by modifying `text-emerald-600` (options: `text-blue-600`, `text-red-600`, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Boom Kappen Met Hoogwerker
</h1>
<p class="text-xl md:text-2xl text-emerald-600 font-semibold mb-8">
    Tijdelijk 10% Korting op Alle Diensten
</p>
```
- Update headline text between the `<h1>` tags
- Modify promotion text in the `<p>` tag
- Responsive sizes are preset (`text-4xl` for mobile, `text-5xl` for tablet, `text-6xl` for desktop)

### Tailwind CSS Class Guide
Common classes used in this page:
- `container mx-auto`: Centers content with automatic margins
- `px-4 sm:px-6 lg:px-8`: Responsive padding (increases with screen size)
- `py-24`: Vertical padding (24 units)
- `text-emerald-600`: Text color (emerald theme)
- `bg-white`: Background color
- `rounded-full`: Fully rounded corners
- `hover:scale-105`: Grows element to 105% on hover

## Managing Links

### Navigation Menu Links
```html
<div class="hidden lg:flex space-x-8">
    <a href="#diensten" class="text-gray-600 hover:text-emerald-600 transition-colors">Diensten</a>
    <a href="#voordelen" class="text-gray-600 hover:text-emerald-600 transition-colors">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-emerald-600 transition-colors">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-emerald-600 transition-colors">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute
2. For internal links (same page sections), use `#section-name`
3. For external links, use full URL: `https://example.com`

### Call-to-Action Buttons
```html
<a href="https://hansschuiling.nl" class="inline-block px-8 py-4 text-lg font-semibold text-white bg-emerald-600 rounded-full">
    Direct Offerte Aanvragen
</a>
```
- Replace `https://hansschuiling.nl` with your desired URL
- Update button text between the tags

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
```html
<!-- Find this section in the footer -->
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-emerald-400 transition-colors">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-emerald-400 transition-colors">Terms & Conditions</a></li>
</ul>
```
- Replace `#` with proper file paths
- Maintain consistent styling using the same classes

### Step 3: Ensure Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-emerald-400 transition-colors"
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check for correct `href` values
   - Ensure file names match exactly (including case)
   - Verify file locations in your directory

2. **Styling Issues**
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names
   - Ensure responsive classes use correct breakpoints (`sm:`, `md:`, `lg:`)

3. **Layout Problems**
   - Verify `container` class is present on main sections
   - Check for proper closing tags
   - Ensure responsive classes are correctly ordered

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check HTML validity using [W3C Validator](https://validator.w3.org/)
- Inspect elements using browser developer tools (F12)

Remember to always test changes across different screen sizes and browsers before publishing updates.