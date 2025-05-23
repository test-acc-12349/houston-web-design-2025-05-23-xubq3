# Houston Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Houston Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line and update "HWD":
```html
<a href="/" class="text-2xl font-bold text-blue-600">HWD</a>
```

2. **Navigation Menu Items**: Located in the header `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```

### Hero Section
The main headline and subtitle are in the first `<section>` after `<main>`:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Houston Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Houston</p>
```

#### Tailwind CSS Class Guide
- Text sizes: `text-4xl`, `text-5xl`, `text-6xl` (larger numbers = bigger text)
- Colors: `text-gray-900`, `text-blue-600` (higher numbers = darker shades)
- Spacing: `mb-6`, `py-24` (m=margin, p=padding, numbers are in multiples of 4px)

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
   - Features (`#features`)
   - Benefits (`#benefits`)
   - FAQ (`#faq`)
   - Contact (`#contact`)

2. Call-to-Action Links:
```html
<a href="https://hwd.com" class="inline-block px-8 py-4 bg-blue-600 text-white">Start Your Project</a>
```

### Updating Links
To update any link:

1. Find the `<a>` tag
2. Modify the `href` attribute
3. Example:
```html
<!-- Before -->
<a href="https://hwd.com">Start Your Project</a>

<!-- After -->
<a href="https://yournewdomain.com">Start Your Project</a>
```

### Internal vs External Links
- Internal links (same page): Use `#section-id` format
- External links: Use full URL including `https://`
- Local pages: Use relative paths like `./privacy.html`

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file paths are correct
   - Ensure external URLs include `https://`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance on different screen sizes
   - Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Styling Problems**
   - Check for missing classes
   - Verify Tailwind CSS is properly loaded
   - Ensure the font family link is present in `<head>`

### Best Practices

1. Always test changes on multiple screen sizes
2. Keep backup copies of working files
3. Validate links before publishing
4. Maintain consistent styling across all pages

Remember to update the copyright year in the footer annually:
```html
<p class="text-gray-400">&copy; 2024 Houston Web Design. All rights reserved.</p>
```

For additional help or advanced customization, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.