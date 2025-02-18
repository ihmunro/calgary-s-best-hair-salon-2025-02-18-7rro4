# Nice Look Landing Page - Maintenance Guide

This guide will help you maintain and customize the Nice Look salon landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the salon name and navigation menu. To update:

1. **Salon Name**:
```html
<a href="#" class="text-xl font-bold tracking-tight">Nice Look</a>
```
Replace "Nice Look" with your desired name while keeping the surrounding tags intact.

2. **Navigation Menu Items**:
```html
<nav class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-200">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-200">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-200">Contact</a>
</nav>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
Update the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-white mb-6">
    Calgary's Best Hair Salon
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-2xl">
    Experience the perfect blend of style and expertise at Nice Look. Where beauty meets excellence.
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Large text size (mobile)
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `font-bold`: Bold text weight
- `mb-6`: Margin bottom spacing
- `text-white`: White text color
- `text-gray-300`: Light gray text color

To modify styling, adjust these classes. For example:
- Make text larger: Change `text-4xl` to `text-5xl`
- Add spacing: Increase `mb-6` to `mb-8`
- Change color: Replace `text-white` with `text-gray-100`

## Managing Links

### External Links
Look for and update these important external links:

1. **Booking Button** (appears multiple times):
```html
<a href="https://calgaryshairsalon.com" class="inline-flex items-center...">
```
Replace `https://calgaryshairsalon.com` with your actual booking URL.

2. **Email Contact**:
```html
<a href="mailto:iainhmunro@gmail.com" class="text-gray-400 hover:text-white...">
```
Update with your salon's email address.

### Internal Links
Navigation menu links use anchor tags to scroll to sections:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

Ensure these IDs match their corresponding sections:
```html
<section id="features" class="py-24 bg-gray-800">
<section id="benefits" class="py-24 bg-gray-900">
```

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Replace the placeholder links in the footer:

```html
<!-- Original footer links -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>

<!-- Updated footer links -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. **Styling Problems**
   - Check for missing class names
   - Verify Tailwind CSS is properly loaded
   - Confirm class spelling matches Tailwind conventions

3. **Responsive Issues**
   - Test on multiple screen sizes
   - Verify media query classes (md:, lg:) are correct
   - Check for proper spacing classes

### Need Help?
If you encounter issues:
1. Verify changes against the original code
2. Test in multiple browsers
3. Use browser developer tools (F12) to inspect elements
4. Ensure all HTML tags are properly closed

Remember to always backup your files before making changes, and test your updates across different devices and browsers.