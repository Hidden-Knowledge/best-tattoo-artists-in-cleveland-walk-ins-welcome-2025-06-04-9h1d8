# CLE Tatted Landing Page - Maintenance Guide

This guide will help you maintain and customize the CLE Tatted tattoo shop landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold">CLE Tatted</a>
```
Simply replace "CLE Tatted" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="hover:text-gray-600 transition-colors duration-300">Artists</a>
    <a href="#" class="hover:text-gray-600 transition-colors duration-300">Gallery</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
To update the main headline and subtext:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Best Tattoo Artists in Cleveland<br>Walk-Ins Welcome
</h1>
<p class="text-xl md:text-2xl mb-8">Where Cleveland Gets Tattooed — Walk Right In.</p>
```

#### Tailwind CSS Class Guide:
- `text-4xl`: Large text on mobile
- `md:text-6xl`: Larger text on desktop
- `mb-6`: Margin bottom spacing
- `leading-tight`: Line height control

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-black rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-paint-brush text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Custom Designs</h3>
    <p class="text-gray-600">Unique artwork tailored to your vision and style.</p>
</div>
```

To modify:
1. Change the icon by updating the `fa-paint-brush` class
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current placeholder links to update:

```html
<!-- Replace # with actual page URLs -->
<a href="#" class="hover:text-gray-600">Artists</a>
<a href="#" class="hover:text-gray-600">Gallery</a>
<a href="#" class="hover:text-gray-600">Pricing</a>
<a href="#" class="hover:text-gray-600">Contact</a>
```

To update:
1. Replace `#` with your page URL
2. Example: `<a href="artists.html">Artists</a>`
3. For external links, use full URLs: `<a href="https://example.com">Link</a>`

### Booking Links
The site uses Stripe for booking. Update these links:

```html
<!-- Find all instances of -->
<a href="https://stripe.com" class="bg-black text-white px-6 py-2">Book Now</a>

<!-- Replace with your actual booking URL -->
<a href="https://your-booking-system.com" class="bg-black text-white px-6 py-2">Book Now</a>
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Images**
   - Check that image URLs are correct
   - Ensure images exist in the specified location
   - Verify image paths are relative to your HTML file

2. **Responsive Design Issues**
   - Mobile menu not showing:
     ```html
     <!-- Check these classes are present -->
     <div class="hidden md:flex items-center space-x-8">
     ```
   - Content overflow:
     - Verify container classes: `container mx-auto px-4`
     - Check for proper spacing classes (`p-`, `m-` prefixes)

3. **Social Media Icons Not Showing**
   - Ensure Font Awesome is properly loaded:
     ```html
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
     ```

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links start with either `http://`, `https://`, or are relative paths
- Test the page on multiple devices and browsers

Remember to always make a backup of your files before making changes!