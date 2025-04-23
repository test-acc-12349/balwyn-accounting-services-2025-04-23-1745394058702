# Balwyn Landing Page Maintenance Guide

This guide will help you maintain and customize the Balwyn Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Balwyn</a>
```
- Replace "Balwyn" with your company name
- Keep the classes intact to maintain the gradient effect

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Balwyn accounting services</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">Strategic financial guidance beyond the spreadsheet</p>
```
- Update text between the `<h1>` tags for the main headline
- Modify the `<p>` content for the subtitle
- The classes ensure responsive text sizing:
  - `text-4xl`: Base size
  - `md:text-5xl`: Medium screens
  - `lg:text-7xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 p-8 rounded-2xl hover:shadow-xl hover:shadow-purple-500/10 transition-all duration-300">
    <h3 class="text-xl font-bold mb-4">Business Experts</h3>
    <p class="text-gray-400">Industry-leading professionals dedicated to your financial success</p>
</div>
```
- Update the `<h3>` text for feature titles
- Modify `<p>` content for feature descriptions
- Keep the class structure to maintain hover effects and spacing

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The "Get Started" button links need updating:
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
```
- Replace `https://theaccountants.com` with your actual URL
- Test the link after updating

## Linking Privacy and Terms Pages

### Footer Links Section
Locate the Legal section in the footer:
```html
<div>
    <h4 class="font-bold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
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

### Common Issues and Solutions

1. **Broken Gradient Text**
If the gradient text disappears:
```html
<!-- Ensure these classes are present -->
bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent
```

2. **Responsive Menu Issues**
The mobile menu is hidden by default:
```html
<!-- Check these classes -->
<div class="hidden md:flex space-x-8">
```
- `hidden`: Hides on mobile
- `md:flex`: Shows on medium screens

3. **Animation Not Working**
Check the AOS initialization:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true
    });
</script>
```
- Ensure the AOS script is loaded
- Verify `data-aos` attributes on elements

Remember to:
- Always backup before making changes
- Test on multiple screen sizes
- Validate links after updating
- Keep the responsive design intact by maintaining Tailwind classes

Need more help? Refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [AOS Documentation](https://michalsnik.github.io/aos/)