# London Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the London Web landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-gray-800">London Web</div>
```
Simply replace "London Web" with your desired text.

### Hero Section
The main banner section contains your primary heading and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">Best Websites In London</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Custom Websites For Your Business</p>
```

Key Tailwind classes explained:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Dark gray text color

### Features Section
To modify feature cards:

1. Locate the feature card structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-laptop text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless user experience.</p>
</div>
```

2. To change icons:
   - Replace `fa-laptop` with any [Font Awesome icon](https://fontawesome.com/icons)
   - Keep the `fas` prefix for solid icons

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Change the `href` value to match your section ID
2. Update the link text between `<a>` tags
3. Maintain the classes for consistent styling

### Call-to-Action Links
Current CTA links point to "https://sigmaseo.io". To update:

```html
<!-- Find these lines and replace the href value -->
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and update the placeholder links:

```html
<!-- Original footer links -->
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes for new links to maintain consistency:
- `hover:text-white`
- `transition-colors`
- `duration-300`

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Icons Not Showing**
   - Verify Font Awesome CDN is loaded in `<head>`
   - Check icon class names on [Font Awesome](https://fontawesome.com)

3. **Responsive Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Test on multiple screen sizes using browser dev tools

4. **Style Changes Not Working**
   - Verify Tailwind CDN is loaded in `<head>`
   - Check for typos in class names
   - Maintain spacing between multiple classes

Remember to:
- Always test changes in multiple browsers
- Keep a backup of the original file
- Validate HTML at [W3C Validator](https://validator.w3.org)
- Test all links after making changes

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.