# Landing Page Maintenance Guide

This guide will help you maintain and customize the WillabySolutions landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">WillabySolutions</a>
```
Simply replace "WillabySolutions" with your company name.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">End Customer Service Nightmares in 60 Seconds</h1>
```

The text sizes are responsive:
- `text-4xl`: Mobile devices
- `md:text-5xl`: Medium screens
- `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:bg-gray-750 transition-all duration-300 transform hover:scale-105 hover:shadow-xl hover:shadow-purple-500/10">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full mb-6">
        <!-- Icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description</p>
</div>
```

To modify:
1. Update the title in the `<h3>` tag
2. Change the description in the `<p>` tag
3. Keep the existing classes for consistent styling

### Tailwind CSS Tips for Beginners
- `text-{size}`: Controls font size (xs, sm, base, lg, xl, 2xl, etc.)
- `font-{weight}`: Controls font boldness (light, normal, medium, semibold, bold)
- `mb-{size}`: Adds margin bottom (1-16, where 4 = 1rem)
- `p-{size}`: Adds padding all around
- `rounded-{size}`: Controls border radius

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://willabysolutions.com">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #) point to section IDs on the page
2. External links need full URLs
3. Example update:
```html
<a href="https://your-domain.com/features">Features</a>
```

### Call-to-Action Buttons
Located in hero and final sections:
```html
<a href="https://willabysolutions.com" class="inline-block px-8 py-4 text-lg font-semibold bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">Transform Your Support Now</a>
```

Replace `https://willabysolutions.com` with your desired URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't work if section ID is `features`

2. **Styling Issues**
   - Check for missing classes
   - Maintain the full chain of responsive classes (e.g., `text-4xl md:text-5xl lg:text-6xl`)

3. **Layout Problems**
   - Keep the container structure:
```html
<div class="container mx-auto px-6">
    <!-- Content here -->
</div>
```

4. **Social Media Links**
   - Replace # in footer social links with actual social media URLs
   - Keep the SVG icons intact for proper display

Remember to:
- Test all links after updating
- Verify responsive design on different screen sizes
- Maintain consistent spacing and padding
- Keep the gradient styling for visual consistency

Need help? Contact technical support or refer to the Tailwind CSS documentation for detailed class references.