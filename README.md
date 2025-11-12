# AI Automation Sydney Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, customizing, and managing your AI Automation Sydney landing page. This document provides step-by-step instructions for developers of all skill levels.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Customizing Colors and Branding](#customizing-colors-and-branding)
8. [Mobile Responsiveness Tips](#mobile-responsiveness-tips)
9. [Troubleshooting Common Issues](#troubleshooting-common-issues)
10. [Performance Optimization](#performance-optimization)

---

## Getting Started

### What You Need

- A text editor (we recommend **Visual Studio Code** - it's free!)
- Basic familiarity with HTML and CSS
- An understanding of how your web hosting works
- A way to upload files to your server (FTP client or hosting control panel)

### File Organization

Your landing page consists of:

```
your-website/
├── index.html (main landing page - the file provided)
├── privacy.html (privacy policy - you'll create this)
├── terms.html (terms of service - you'll create this)
├── blog.html (blog page - optional)
└── assets/ (optional folder for images, CSS, JS)
```

### Before Making Changes

**Always create a backup** of your `index.html` file before making changes. You can:
1. Right-click the file in your file manager
2. Select "Copy"
3. Rename the copy to `index-backup.html`

---

## Understanding the Page Structure

Your landing page is organized into distinct sections. Here's what each section contains:

### 1. **Header Navigation** (Lines 72-107)
```html
<header class="w-full">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
        <!-- Logo and Desktop Menu -->
        <!-- Mobile Menu -->
    </nav>
</header>
```
**Contains:** Logo, navigation links, mobile menu button

### 2. **Hero Section** (Lines 109-175)
```html
<section class="relative py-20 md:py-32 lg:py-40 bg-gradient-to-br...">
```
**Contains:** Main headline, subheading, call-to-action buttons, statistics

### 3. **Features Section** (Lines 177-291)
```html
<section id="features" class="py-16 md:py-24 bg-white">
```
**Contains:** Six feature cards with icons and descriptions

### 4. **Benefits Section** (Lines 293-436)
```html
<section id="benefits" class="py-16 md:py-24 bg-gradient-to-br...">
```
**Contains:** Three main benefit cards, additional benefits grid

### 5. **About Us Section** (Lines 438-507)
```html
<section class="py-16 md:py-24 bg-white">
```
**Contains:** Company history, track record, why choose us

### 6. **Testimonials Section** (Lines 509-588)
```html
<section id="testimonials" class="py-16 md:py-24...">
```
**Contains:** Four client testimonials with star ratings

### 7. **Call-to-Action Section** (Lines 590-615)
```html
<section class="relative py-16 md:py-24 overflow-hidden">
```
**Contains:** Main CTA with background image, buttons

### 8. **FAQ Section** (Lines 617-797)
```html
<section id="faq" class="py-16 md:py-24 bg-white">
```
**Contains:** Five collapsible FAQ items with answers

### 9. **Contact Form Section** (Lines 799-900)
```html
<section id="contact" class="py-20 bg-gray-50">
```
**Contains:** Contact information and Web3Forms contact form

### 10. **Footer** (Lines 902-1005)
```html
<footer class="bg-[#1A1A1A] text-gray-300 py-12 md:py-16">
```
**Contains:** Links, company info, social media, copyright

---

## Updating Text Content

Text content is the easiest element to change. Follow these step-by-step instructions for each section.

### How to Edit Text - Basic Steps

1. **Open** `index.html` in your text editor (right-click → Open With)
2. **Use Find & Replace** (press `Ctrl+H` on Windows or `Cmd+H` on Mac)
3. **Type** the text you want to find in the first box
4. **Type** the replacement text in the second box
5. **Click** "Replace All" or replace individually
6. **Save** the file (Ctrl+S or Cmd+S)
7. **Upload** the updated file to your server

### Header Navigation Text

**Location:** Lines 85-90

**Current Code:**
```html
<a href="#features" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">FAQ</a>
```

**To Change Menu Items:**
1. Find the word "Features" and replace with your desired text
2. Find the word "Benefits" and replace with your desired text
3. The `href="#features"` part should match the section's `id` (keep these the same)

**Example:** If you want to rename "Benefits" to "Why Us"
- Find: `>Benefits</a>`
- Replace with: `>Why Us</a>`

### Hero Section Headline

**Location:** Lines 127-131

**Current Code:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-semibold leading-tight text-[#1A1A1A]">
    AI Automation <span class="gradient-text">Sydney</span>
</h1>
<p class="text-2xl md:text-3xl font-semibold text-[#FF5A5F] leading-snug">
    Best n8n Automation Agency
</p>
```

**To Update:**
- Change `AI Automation` to your company name
- Change `Sydney` to your location (this text has special gradient styling)
- Change `Best n8n Automation Agency` to your tagline

**Important:** Keep the `<span class="gradient-text">` tags around the word you want to have gradient color effect.

### Hero Section Description

**Location:** Lines 133-138

**Current Code:**
```html
<p class="text-lg md:text-xl text-gray-600 leading-relaxed font-light max-w-lg">
    Transform your business with expert n8n automation services. Streamline workflows, eliminate manual tasks, and unlock unprecedented productivity with our Sydney-based automation specialists.
</p>
```

**To Update:**
Simply replace the text between the `<p>` and `</p>` tags with your description. Keep the HTML tags exactly as they are.

### Hero Section Statistics

**Location:** Lines 154-169

**Current Code:**
```html
<div class="space-y-2">
    <p class="text-3xl font-bold text-[#FF5A5F]">500+</p>
    <p class="text-sm text-gray-600 font-light">Workflows Automated</p>
</div>
```

**To Update Each Statistic:**
1. Change `500+` to your number
2. Change `Workflows Automated` to your statistic label

**Example:**
```html
<div class="space-y-2">
    <p class="text-3xl font-bold text-[#FF5A5F]">1000+</p>
    <p class="text-sm text-gray-600 font-light">Projects Completed</p>
</div>
```

### Features Section

**Location:** Lines 207-291

Each feature card follows this structure:

**Current Code (Feature 1):**
```html
<div class="card p-8 shadow-md">
    <div class="flex items-start space-x-4 mb-6">
        <div class="flex-shrink-0">
            <span class="material-symbols-rounded text-4xl text-[#FF5A5F]">build</span>
        </div>
        <div>
            <h3 class="text-xl font-semibold text-[#1A1A1A] mb-2">Expert n8n Automation</h3>
            <p class="text-gray-600 font-light leading-relaxed">
                Our certified n8n specialists design and implement sophisticated workflow automation solutions...
            </p>
        </div>
    </div>
    <ul class="space-y-2 text-sm text-gray-600 font-light">
        <li class="flex items-center space-x-2">
            <span class="material-symbols-rounded text-lg text-[#FF5A5F]">check_circle</span>
            <span>Custom workflow design and development</span>
        </li>
        <!-- More list items -->
    </ul>
</div>
```

**To Update a Feature:**

1. **Change the title:** Replace `Expert n8n Automation` with your feature name
2. **Change the description:** Replace the paragraph text with your description
3. **Change the bullet points:** Replace each `<span>` text with your benefits
4. **Change the icon:** Replace `build` with another icon name (see [Icon Reference](#icon-reference) below)

**Icon Reference:**
Common icons you can use:
- `build` - For building/construction
- `location_on` - For location/Sydney
- `smart_toy` - For AI/intelligence
- `trending_up` - For growth/scaling
- `shield` - For security
- `support_agent` - For support
- `schedule` - For time/speed
- `person_check` - For people/team
- `public` - For global/local
- `savings` - For cost savings
- `speed` - For speed/performance

Find more icons at: https://fonts.google.com/icons

### Benefits Section

**Location:** Lines 327-380

**Current Code (Example):**
```html
<h3 class="text-2xl font-semibold text-[#1A1A1A] mb-4">Save Valuable Time</h3>
<p class="text-gray-600 font-light leading-relaxed mb-6">
    Eliminate repetitive manual tasks that consume hours every week...
</p>
```

**To Update:**
1. Change the heading text
2. Change the main description
3. Update each bullet point in the list below

### About Us Section

**Location:** Lines 469-495

**Current Code:**
```html
<p class="text-lg text-gray-600 font-light leading-relaxed">
    Founded in 2020, AI Automation Sydney emerged from a simple yet powerful vision...
</p>
```

**To Update:**
Replace the entire paragraph with your company story. You can use multiple `<p>` tags for multiple paragraphs.

### Testimonials Section

**Location:** Lines 540-588

**Current Code (Example):**
```html
<div class="testimonial-card">
    <div class="flex items-center justify-between mb-4">
        <div>
            <h4 class="text-lg font-semibold text-[#1A1A1A]">Sarah Mitchell</h4>
            <p class="text-sm text-gray-600 font-light">Operations Director, Tech Innovations Ltd</p>
        </div>
    </div>
    <div class="flex mb-4">
        <span class="material-symbols-rounded text-lg star-rating">star</span>
        <!-- More stars -->
    </div>
    <p class="text-gray-700 font-light leading-relaxed">
        "The team at AI Automation Sydney completely transformed..."
    </p>
</div>
```

**To Update a Testimonial:**
1. Change `Sarah Mitchell` to the client's name
2. Change `Operations Director, Tech Innovations Ltd` to their title and company
3. Change the testimonial text (keep the quotation marks)
4. To change star rating: Add or remove `<span class="material-symbols-rounded text-lg star-rating">star</span>` lines

**To Add a New Testimonial:**
Copy the entire testimonial card block and paste it below the last testimonial, then update the information.

### FAQ Section

**Location:** Lines 665-797

**Current Code (Example):**
```html
<div class="faq-item border border-gray-200 rounded-lg overflow-hidden">
    <div class="faq-question bg-gray-50 hover:bg-gray-100 px-6 py-4 cursor-pointer transition-colors duration-300">
        <div class="flex items-center justify-between">
            <h3 class="text-lg font-semibold text-[#1A1A1A]">What is n8n and why should we use it?</h3>
            <span class="faq-icon material-symbols-rounded text-[#FF5A5F] transition-transform duration-300">expand_more</span>
        </div>
    </div>
    <div class="faq-answer hidden px-6 py-4 bg-white border-t border-gray-200">
        <p class="text-gray-700 font-light leading-relaxed mb-4">
            n8n is a powerful, open-source workflow automation platform...
        </p>
    </div>
</div>
```

**To Update an FAQ:**
1. Change the question text: `What is n8n and why should we use it?`
2. Change the answer text inside the `faq-answer` div
3. You can have multiple `<p>` tags for longer answers
4. Keep the HTML structure exactly as shown

**To Add a New FAQ:**
Copy the entire `faq-item` block and paste it before the closing `</div>` of the FAQ section, then update the question and answer.

### Footer Links and Text

**Location:** Lines 902-1005

**Current Code (Example):**
```html
<li><a href="#features" class="hover:text-[#FF5A5F] transition-colors duration-300">n8n Automation</a></li>
```

**To Update Footer Links:**
1. Change the text between `<a>` and `</a>` tags
2. Update the `href=""` attribute to point to the correct page or section

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first framework that uses predefined classes to style elements. This landing page uses Tailwind exclusively (no separate CSS file needed).

### Understanding Tailwind Classes

Each class controls specific styling:

```html
<div class="text-4xl md:text-5xl font-semibold text-[#1A1A1A]">
```

Breaking this down:
- `text-4xl` - Font size on mobile (extra large)
- `md:text-5xl` - Font size on medium screens and up (larger)
- `font-semibold` - Font weight (semi-bold)
- `text-[#1A1A1A]` - Text color (dark gray/black)

### Common Tailwind Classes Used on This Page

#### Text Sizing
- `text-sm` - Small text (14px)
- `text-base` - Normal text (16px)
- `text-lg` - Large text (18px)
- `text-xl` - Extra large (20px)
- `text-2xl` - 2x large (24px)
- `text-3xl` - 3x large (30px)
- `text-4xl` - 4x large (36px)
- `text-5xl` - 5x large (48px)
- `text-6xl` - 6x large (60px)
- `text-7xl` - 7x large (84px)

#### Font Weight
- `font-light` - Thin/light text
- `font-normal` - Regular text
- `font-semibold` - Semi-bold text
- `font-bold` - Bold text

#### Colors
- `text-gray-600` - Medium gray text
- `text-gray-700` - Darker gray text
- `text-white` - White text
- `text-[#FF5A5F]` - Brand red color
- `text-[#FFD166]` - Brand yellow color

#### Spacing
- `px-4` - Horizontal padding (left and right)
- `py-4` - Vertical padding (top and bottom)
- `mb-4` - Margin bottom
- `mt-4` - Margin top
- `space-y-4` - Vertical space between child elements

#### Layout
- `flex` - Flexbox container
- `grid` - CSS Grid container
- `grid-cols-1` - 1 column on mobile
- `md:grid-cols-2` - 2 columns on medium screens
- `lg:grid-cols-3` - 3 columns on large screens

#### Responsive Prefixes
- `md:` - Applies on medium screens and up (768px+)
- `lg:` - Applies on large screens and up (1024px+)
- `sm:` - Applies on small screens and up (640px+)

### Example: Changing a Heading Size

**Current Code:**
```html
<h2 class="text-4xl md:text-5xl font-semibold text-[#1A1A1A]">
    Powerful Features for Modern Automation
</h2>
```

**To Make It Larger:**
Replace `text-4xl md:text-5xl` with `text-5xl md:text-6xl`

**Result:**
```html
<h2 class="text-5xl md:text-6xl font-semibold text-[#1A1A1A]">
    Powerful Features for Modern Automation
</h2>
```

### Example: Changing Text Color

**Current Code:**
```html
<h3 class="text-xl font-semibold text-[#1A1A1A] mb-2">Expert n8n Automation</h3>
```

**To Change to Brand Red:**
Replace `text-[#1A1A1A]` with `text-[#FF5A5F]`

**Result:**
```html
<h3 class="text-xl font-semibold text-[#FF5A5F] mb-2">Expert n8n Automation</h3>
```

### Example: Changing Spacing

**Current Code:**
```html
<p class="text-lg md:text-xl text-gray-600 leading-relaxed font-light max-w-lg">
```

**To Add More Margin Below:**
Add `mb-8` at the end

**Result:**
```html
<p class="text-lg md:text-xl text-gray-600 leading-relaxed font-light max-w-lg mb-8">
```

### Example: Making Elements Full Width on Mobile

**Current Code:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

This already uses `grid-cols-1` (full width on mobile) and `md:grid-cols-2` (2 columns on medium screens).

**To Change to 3 Columns on Medium Screens:**
Replace `md:grid-cols-2` with `md:grid-cols-3`

### Common Customizations

#### Make All Text Larger
Find and replace (Ctrl+H):
- Find: `text-lg`
- Replace with: `text-xl`

#### Change All Button Colors
Find and replace:
- Find: `bg-[#FF5A5F]`
- Replace with: `bg-[#YOUR-COLOR]` (use hex color codes)

#### Increase Spacing Between Sections
Find and replace:
- Find: `py-16 md:py-24`
- Replace with: `py-20 md:py-32`

---

## Fixing and Managing Links

Links are critical for navigation. This section shows you exactly where to find and update every link on the page.

### Understanding Links

A link in HTML looks like this:
```html
<a href="destination-url" class="styling-classes">Link Text</a>
```

- `href` - Where the link goes
- Link Text - What users see and click

### All Links on This Page - Complete List

#### 1. Navigation Menu Links (Header)

**Location:** Lines 86-91 (Desktop) and Lines 100-106 (Mobile)

**Current Links:**
```html
<!-- Desktop Menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="https://test.com" class="btn-primary">Get Started</a>

<!-- Mobile Menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="https://test.com" class="btn-primary">Get Started</a>
```

**What Each Link Does:**
- `#features` - Jumps to Features section on same page
- `#benefits` - Jumps to Benefits section on same page
- `#testimonials` - Jumps to Testimonials section on same page
- `#faq` - Jumps to FAQ section on same page
- `https://test.com` - External link (currently placeholder)

**To Update the "Get Started" Button:**
1. Find: `<a href="https://test.com"`
2. Replace with: `<a href="your-actual-url"`

**Example:** If your booking page is at `https://yourdomain.com/book`
```html
<a href="https://yourdomain.com/book" class="btn-primary">Get Started</a>
```

#### 2. Hero Section Buttons

**Location:** Lines 142-153

**Current Code:**
```html
<a href="https://test.com" class="btn-primary text-center sm:text-left">
    <span class="flex items-center justify-center sm:justify-start space-x-2">
        <span>Start Your Automation Journey</span>
        <span class="material-symbols-rounded text-lg">arrow_forward</span>
    </span>
</a>
<a href="#benefits" class="btn-secondary text-center sm:text-left">
    <span class="flex items-center justify-center sm:justify-start space-x-2">
        <span>Learn More</span>
        <span class="material-symbols-rounded text-lg">expand_more</span>
    </span>
</a>
```

**To Update:**
- First button: Change `https://test.com` to your booking/contact URL
- Second button: The `#benefits` link is correct (jumps to Benefits section)

#### 3. CTA Section Buttons

**Location:** Lines 603-614

**Current Code:**
```html
<a href="https://test.com" class="btn-primary text-center">
    <span class="flex items-center justify-center space-x-2">
        <span>Schedule Your Free Consultation</span>
        <span class="material-symbols-rounded text-lg">arrow_forward</span>
    </span>
</a>
<a href="mailto:admin@test.com" class="btn-secondary text-center">
    <span class="flex items-center justify-center space-x-2">
        <span>Contact Us</span>
        <span class="material-symbols-rounded text-lg">mail</span>
    </span>
</a>
```

**To Update:**
- First button: Change `https://test.com` to your booking URL
- Second button: Change `admin@test.com` to your email address

**Email Link Explanation:**
- `mailto:` tells the browser to open the user's email client
- The email address goes after the colon

#### 4. Footer Links

**Location:** Lines 952-975

**Current Code:**
```html
<!-- Services Links -->
<li><a href="#features">n8n Automation</a></li>
<li><a href="#features">Workflow Design</a></li>
<li><a href="#features">API Integration</a></li>
<li><a href="#features">Support & Maintenance</a></li>

<!-- Resources Links -->
<li><a href="blog.html">Blog</a></li>
<li><a href="#faq">FAQ</a></li>
<li><a href="#testimonials">Case Studies</a></li>
<li><a href="https://test.com">Contact</a></li>

<!-- Legal Links -->
<li><a href="privacy.html">Privacy Policy</a></li>
<li><a href="terms.html">Terms of Service</a></li>
<li><a href="blog.html">Blog</a></li>
```

**To Update:**
- Service links: Update to point to your service pages
- Blog link: Change `blog.html` to your actual blog URL
- Contact link: Change `https://test.com` to your contact page
- Privacy link: Keep as `privacy.html` (you'll create this file)
- Terms link: Keep as `terms.html` (you'll create this file)

#### 5. Footer Contact Information

**Location:** Lines 978-1000

**Current Code:**
```html
<a href="mailto:admin@test.com" class="text-sm font-light hover:text-[#FF5A5F]">admin@test.com</a>
```

**To Update:**
Change `admin@test.com` to your actual email address

#### 6. Footer Social Media Links

**Location:** Lines 1009-1027

**Current Code:**
```html
<a href="#" class="w-10 h-10 rounded-lg bg-gray-800 hover:bg-[#FF5A5F]" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**To Update:**
Replace `#` with your actual social media URLs:
- Facebook: `https://facebook.com/yourpage`
- Twitter: `https://twitter.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Instagram: `https://instagram.com/yourhandle`

**Complete Example:**
```html
<a href="https://facebook.com/aiautomationsydney" class="w-10 h-10 rounded-lg bg-gray-800 hover:bg-[#FF5A5F]" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>
<a href="https://twitter.com/aiautosydney" class="w-10 h-10 rounded-lg bg-gray-800 hover:bg-[#FF5A5F]" aria-label="Twitter">
    <i class="fab fa-twitter text-white"></i>
</a>
```

### How to Find and Update All Links - Quick Method

1. **Open Find & Replace** (Ctrl+H on Windows, Cmd+H on Mac)
2. **Find:** `href="https://test.com"`
3. **Replace with:** `href="your-actual-url"`
4. **Click Replace All**
5. **Repeat for:** `admin@test.com` → your email

### Testing Links

After updating links:

1. **Save the file** (Ctrl+S)
2. **Upload to your server**
3. **Test each link:**
   - Click navigation menu items
   - Click buttons
   - Click footer links
   - Verify they go to the correct destination
4. **Check on mobile** - Use a phone to test mobile menu links

---

## Adding Privacy and Terms Pages

Your footer currently links to `privacy.html` and `terms.html`, but these files don't exist yet. Here's how to create them.

### Step 1: Create the Privacy Policy File

1. **Open your text editor** (Visual Studio Code, Notepad++, etc.)
2. **Create a new file** (File → New)
3. **Copy and paste** the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - AI Automation Sydney">
    <title>Privacy Policy - AI Automation Sydney</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700,800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Poppins', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="w-full sticky top-0 z-50 bg-white box-shadow">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 rounded-lg bg-gradient-to-br from-[#FF5A5F] to-[#FFD166] flex items-center justify-center">
                    <i class="fas fa-rocket text-white text-lg"></i>
                </div>
                <h1 class="text-xl font-semibold text-[#1A1A1A]">AI Automation Sydney</h1>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-semibold text-[#1A1A1A] mb-8">Privacy Policy</h1>
        
        <div class="space-y-8 text-gray-700 font-light leading-relaxed">
            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">1. Introduction</h2>
                <p>
                    AI Automation Sydney ("Company," "we," "us," "our," or "our Company") operates the website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">2. Information Collection and Use</h2>
                <p>We collect several different types of information for various purposes to provide and improve our Service to you:</p>
                <ul class="list-disc list-inside space-y-2 mt-4">
                    <li>Personal Data: While using our Service, we may ask you to provide us with certain personally identifiable information that can be used to contact or identify you ("Personal Data"). This may include, but is not limited to:
                        <ul class="list-circle list-inside space-y-1 mt-2 ml-4">
                            <li>Email address</li>
                            <li>First name and last name</li>
                            <li>Phone number</li>
                            <li>Address, State, Province, ZIP/Postal code, City</li>
                            <li>Cookies and Usage Data</li>
                        </ul>
                    </li>
                    <li>Usage Data: We may also collect information on how the Service is accessed and used ("Usage Data"). This may include information such as your computer's Internet Protocol address, browser type, browser version, the pages you visit, the time and date of your visit, and other diagnostic data.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">3. Use of Data</h2>
                <p>AI Automation Sydney uses the collected data for various purposes:</p>
                <ul class="list-disc list-inside space-y-2 mt-4">
                    <li>To provide and maintain our Service</li>
                    <li>To notify you about changes to our Service</li>
                    <li>To allow you to participate in interactive features of our Service when you choose to do so</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so that we can improve our Service</li>
                    <li>To monitor the usage of our Service</li>
                    <li>To detect, prevent and address technical and security issues</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">4. Security of Data</h2>
                <p>
                    The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">5. Changes to This Privacy Policy</h2>
                <p>
                    We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "effective date" at the top of this Privacy Policy.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">6. Contact Us</h2>
                <p>
                    If you have any questions about this Privacy Policy, please contact us:
                </p>
                <ul class="list-disc list-inside space-y-2 mt-4">
                    <li>By email: admin@test.com</li>
                    <li>By visiting this page on our website: <a href="index.html" class="text-[#FF5A5F] hover:underline">AI Automation Sydney</a></li>
                </ul>
            </section>

            <p class="text-sm text-gray-500 mt-12">Last updated: January 2025</p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-[#1A1A1A] text-gray-300 py-8 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="font-light">&copy; 2025 AI Automation Sydney. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

4. **Save the file:**
   - Click File → Save As
   - Name it: `privacy.html`
   - Make sure you save it in the **same folder** as your `index.html`
   - Save as type: "All Files" (not .txt)

### Step 2: Create the Terms of Service File

1. **Create another new file** in your text editor
2. **Copy and paste** the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - AI Automation Sydney">
    <title>Terms of Service - AI Automation Sydney</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700,800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Poppins', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="w-full sticky top-0 z-50 bg-white box-shadow">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 rounded-lg bg-gradient-to-br from-[#FF5A5F] to-[#FFD166] flex items-center justify-center">
                    <i class="fas fa-rocket text-white text-lg"></i>
                </div>
                <h1 class="text-xl font-semibold text-[#1A1A1A]">AI Automation Sydney</h1>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-[#FF5A5F] transition-colors duration-300 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-semibold text-[#1A1A1A] mb-8">Terms of Service</h1>
        
        <div class="space-y-8 text-gray-700 font-light leading-relaxed">
            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on AI Automation Sydney's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside space-y-2 mt-4">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">3. Disclaimer</h2>
                <p>
                    The materials on AI Automation Sydney's website are provided on an 'as is' basis. AI Automation Sydney makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">4. Limitations</h2>
                <p>
                    In no event shall AI Automation Sydney or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the website, even if AI Automation Sydney or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on the website could include technical, typographical, or photographic errors. AI Automation Sydney does not warrant that any of the materials on the website are accurate, complete, or current. AI Automation Sydney may make changes to the materials contained on the website at any time without notice.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">6. Links</h2>
                <p>
                    AI Automation Sydney has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by AI Automation Sydney of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">7. Modifications</h2>
                <p>
                    AI Automation Sydney may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of Australia, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-semibold text-[#1A1A1A] mb-4">9. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <ul class="list-disc list-inside space-y-2 mt-4">
                    <li>Email: admin@test.com</li>
                    <li>Website: <a href="index.html" class="text-[#FF5A5F] hover:underline">AI Automation Sydney</a></li>
                </ul>
            </section>

            <p class="text-sm text-gray-500 mt-12">Last updated: January 2025</p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-[#1A1A1A] text-gray-300 py-8 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="font-light">&copy; 2025 AI Automation Sydney. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file:**
   - Click File → Save As
   - Name it: `terms.html`
   - Save it in the **same folder** as your `index.html`
   - Save as type: "All Files"

### Step 3: Verify the Links Work

1. **Make sure all three files are in the same folder:**
   - `index.html`
   - `privacy.html`
   - `terms.html`

2. **Upload all three files to your server**

3. **Test the links:**
   - Go to your website homepage
   - Scroll to the footer
   - Click on "Privacy Policy" - should take you to privacy.html
   - Click on "Terms of Service" - should take you to terms.html
   - Click "Back to Home" on those pages - should return to index.html

### Step 4: Customize Your Policy Content

The template files above contain generic text. You should customize them with your actual business information:

**In privacy.html, change:**
- `admin@test.com` → your actual email
- Add your specific data collection practices
- Add your specific data usage practices

**In terms.html, change:**
- `admin@test.com` → your actual email
- Add your specific terms and conditions
- Update the governing law if needed (currently set to Australia)

### How to Edit Policy Content

1. **Open** `privacy.html` in your text editor
2. **Find the section** you want to change (e.g., "Use of Data")
3. **Replace the text** with your information
4. **Keep the HTML structure** exactly the same
5. **Save and upload** the updated file

**Example:**
```html
<!-- Original -->
<p>
    The security of your data is important to us, but remember that no method of transmission over the Internet...
</p>

<!-- Updated with your information -->
<p>
    We take data security very seriously. All client information is encrypted using industry-standard SSL encryption, and we maintain regular security audits to ensure compliance with GDPR and Australian Privacy Act requirements.
</p>
```

---

## Customizing Colors and Branding

The landing page uses a consistent color scheme. Here's how to change the brand colors throughout the entire page.

### Current Brand Colors

The page uses these main colors:

- **Primary Red:** `#FF5A5F` (used for buttons, links, icons)
- **Secondary Yellow:** `#FFD166` (used for accents, gradients)
- **Dark Gray/Black:** `#1A1A1A` (used for text, backgrounds)
- **Light Gray:** `#F3F4F6` and variations (used for backgrounds)

### How to Change Brand Colors

The easiest way is to use Find & Replace to change colors throughout the entire page:

1. **Open Find & Replace** (Ctrl+H or Cmd+H)
2. **Find:** `#FF5A5F` (the red color)
3. **Replace with:** `#YOUR-NEW-COLOR` (your hex color code)
4. **Click Replace All**
5. **Repeat for the yellow color:** `#FFD166` → `#YOUR-ACCENT-COLOR`

### Finding Hex Color Codes

If you don't know your brand color's hex code:

1. Go to https://www.google.com/search?q=color+picker
2. Enter your color name or RGB values
3. Copy the hex code (starts with #)
4. Use it in the Find & Replace

### Example: Changing from Red/Yellow to Blue/Green

**Step 1: Change Red to Blue**
- Find: `#FF5A5F`
- Replace with: `#0066CC` (blue)

**Step 2: Change Yellow to Green**
- Find: `#FFD166`
- Replace with: `#00CC66` (green)

### Locations Where Brand Colors Are Used

**Primary Color (#FF5A5F) appears in:**
- Button backgrounds (`.btn-primary`)
- Hover states
- Icon colors
- Text highlights
- Gradient backgrounds
- Accent elements

**Secondary Color (#FFD166) appears in:**
- Gradient combinations
- Accent backgrounds
- Hover effects
- Secondary buttons (`.btn-secondary`)

**To Change Only Buttons:**

Find: `.btn-primary { background-color: #FF5A5F;`
Replace with: `.btn-primary { background-color: #YOUR-COLOR;`

**To Change Only Text Links:**

Find: `hover:text-[#FF5A5F]`
Replace with: `hover:text-[#YOUR-COLOR]`

---

## Mobile Responsiveness Tips

This landing page is designed to work on all devices. Here's how the responsive design works and how to maintain it when making changes.

### Understanding Responsive Classes

The page uses Tailwind's responsive prefixes:

- **No prefix** - Applies on all screen sizes
- **`sm:`** - Small screens (640px and up)
- **`md:`** - Medium screens (768px and up)
- **`lg:`** - Large screens (1024px and up)

### Example: Responsive Text Sizes

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl">
    Heading Text
</h1>
```

This means:
- Mobile: 48px font size (`text-5xl`)
- Tablet (768px+): 60px font size (`md:text-6xl`)
- Desktop (1024px+): 84px font size (`lg:text-7xl`)

### Example: Responsive Grid Layout

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Cards here -->
</div>
```

This means:
- Mobile: 1 column (full width)
- Tablet: 2 columns
- Desktop: 3 columns

### When Adding New Content

**Always include responsive classes:**

❌ **Wrong - Not responsive:**
```html
<h2 class="text-4xl font-semibold">My Heading</h2>
```

✅ **Correct - Responsive:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold">My Heading</h2>
```

### Testing on Mobile

1. **On your computer:**
   - Right-click the page
   - Select "Inspect" or "Developer Tools"
   - Click the mobile device icon (top left of developer tools)
   - Choose different device sizes to test

2. **On your phone:**
   - Visit your website
   - Rotate between portrait and landscape
   - Check that text is readable
   - Check that buttons are clickable
   - Check that images scale properly

### Common Mobile Issues and Fixes

**Issue: Text is too small on mobile**
- Add `md:text-lg` or `md:text-xl` to increase size on larger screens

**Issue: Images are too wide on mobile**
- Add `max-w-full` class to ensure images don't overflow

**Issue: Buttons are too small to click on mobile**
- Add `py-3 px-4` for more padding

**Issue: Columns don't stack on mobile**
- Make sure grid includes `grid-cols-1` before any responsive prefixes

---

## Troubleshooting Common Issues

### Issue 1: Links Don't Work

**Problem:** Clicking a link doesn't go anywhere

**Solution:**
1. Check the `href` attribute is correct
2. Make sure external links start with `https://`
3. Make sure anchor links start with `#` and match section IDs
4. Check for typos in the URL

**Example of Correct Links:**
```html
<!-- Anchor link (same page) -->
<a href="#features">Features</a>

<!-- External link -->
<a href="https://example.com">Example</a>

<!-- Email link -->
<a href="mailto:email@example.com">Email Us</a>

<!-- File link -->
<a href="privacy.html">Privacy Policy</a>
```

### Issue 2: Text Looks Wrong

**Problem:** Text is too large, too small, or wrong color

**Solution:**
1. Check the text size classes (`text-lg`, `text-xl`, etc.)
2. Check the color class (`text-gray-600`, `text-[#FF5A5F]`, etc.)
3. Make sure you didn't accidentally delete any classes
4. Verify responsive prefixes are correct (`md:text-lg`, etc.)

### Issue 3: Buttons Look Wrong

**Problem:** Buttons are broken, ugly, or don't match the design

**Solution:**
1. Check the button class is either `btn-primary` or `btn-secondary`
2. Make sure the button styling hasn't been changed
3. Verify the button text is between `<a>` and `</a>` tags
4. Check the `href` attribute is present

### Issue 4: Layout is Broken on Mobile

**Problem:** Page doesn't look good on phones

**Solution:**
1. Test in browser developer tools (F12)
2. Check that responsive classes are present (`md:`, `lg:`)
3. Verify grid columns include `grid-cols-1` for mobile
4. Make sure you didn't remove responsive prefixes

### Issue 5: Form Doesn't Work

**Problem:** Contact form doesn't submit

**Solution:**
1. Check that Web3Forms API key is correct (line 866)
2. Verify form fields have correct `name` attributes
3. Check that button is type="submit"
4. Verify the form `action` attribute points to Web3Forms

### Issue 6: Colors Look Different

**Problem:** Brand colors aren't showing correctly

**Solution:**
1. Check that hex color codes are correct (start with #)
2. Verify you didn't accidentally change hex codes
3. Clear browser cache (Ctrl+Shift+Delete)
4. Try a different browser to test

### Issue 7: Icons Don't Show

**Problem:** Material icons are missing or showing as boxes

**Solution:**
1. Check that the Google Fonts icon link is present (line 21)
2. Verify icon names are correct (check at https://fonts.google.com/icons)
3. Make sure icon class is `material-symbols-rounded`
4. Check that icon is inside a `<span>` tag

### Issue 8: Page Loads Slowly

**Problem:** Website is slow to load

**Solution:**
1. Optimize images - compress them before uploading
2. Check that external CDN links are working (Tailwind, Font Awesome, etc.)
3. Minimize the number of custom fonts
4. Remove unused CSS classes
5. Enable browser caching on your server

---

## Performance Optimization

### Best Practices

#### 1. Image Optimization

The page uses external images in the CTA section. To optimize:

```html
<!-- Current -->
<div class="absolute inset-0 bg-cover bg-center" 
     style="background-image: url('https://images.unsplash.com/photo-1552664730-d307ca884978?w=1200&h=600&fit=crop'); opacity: 0.2;">
</div>
```

**To optimize:**
1. Download the image
2. Compress it using https://tinypng.com
3. Upload to your server
4. Update the URL to your local image

#### 2. Lazy Loading

For future images you add, use lazy loading:

```html
<img src="image.jpg" loading="lazy" alt="Description">
```

#### 3. Minify CSS

Before going to production, minify your CSS to reduce file size:
1. Copy all CSS from `<style>` section
2. Go to https://cssnano.co/playground/
3. Paste and minify
4. Replace original CSS

#### 4. Enable Caching

Ask your hosting provider to enable:
- Browser caching
- Gzip compression
- CDN caching

### Monitoring Performance

Use these free tools to check your page speed:

1. **Google PageSpeed Insights** - https://pagespeed.web.dev
2. **GTmetrix** - https://gtmetrix.com
3. **WebPageTest** - https://www.webpagetest.org

### Quick Wins

1. **Remove unused JavaScript** - The page only needs the script at the bottom
2. **Combine CSS** - All CSS is in the `<style>` tag (good!)
3. **Use modern image formats** - WebP instead of PNG/JPG
4. **Minimize redirects** - Make sure all links go directly to pages

---

## Advanced Customizations

### Adding New Sections

To add a new section, follow this template:

```html
<!-- New Section Template -->
<section id="section-name" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16 space-y-4">
            <h2 class="text-4xl md:text-5xl font-semibold text-[#1A1A1A]">
                Section Title
            </h2>
            <p class="text-lg text-gray-600 font-light max-w-2xl mx-auto">
                Section description goes here
            </p>
        </div>

        <!-- Your content here -->
    </div>
</section>
```

Then add a link in the navigation:
```html
<a href="#section-name" class="text-gray-700 hover:text-[#FF5A5F]">Section Name</a>
```

### Changing Fonts

The page uses "Poppins" font. To change it:

1. **Find:** `<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700,800&display=swap"`

2. **Go to:** https://fonts.google.com

3. **Select a new font** and copy the link

4. **Replace the old link** with the new one

5. **Update the CSS:**
```css
* {
    font-family: 'YourNewFont', sans-serif;
}
```

### Adding Animations

Add hover animations to elements:

```html
<!-- Add to any element -->
<div class="transition-all duration-300 hover:scale-105 hover:shadow-lg">
    Content here
</div>
```

---

## Deployment Checklist

Before going live, verify:

- [ ] All placeholder links updated (`https://test.com`)
- [ ] All email addresses updated (`admin@test.com`)
- [ ] Privacy policy created and linked
- [ ] Terms of service created and linked
- [ ] All internal links working (Features, Benefits, FAQ, etc.)
- [ ] Footer links updated
- [ ] Social media links updated
- [ ] Contact form API key correct
- [ ] Mobile responsiveness tested
- [ ] All text proofread for typos
- [ ] Brand colors finalized
- [ ] Images optimized
- [ ] Page speed tested
- [ ] All sections reviewed

---

## Getting Help

### Resources

- **HTML/CSS Learning:** https://www.w3schools.com
- **Tailwind CSS Docs:** https://tailwindcss.com/docs
- **Google Fonts Icons:** https://fonts.google.com/icons
- **Color Picker:** https://www.google.com/search?q=color+picker
- **Web3Forms Documentation:** https://web3forms.com

### Common Questions

**Q: Can I use this on multiple websites?**
A: Yes, you can reuse this template for different projects. Just update all the content and branding.

**Q: How do I add more features or sections?**
A: Copy an existing section block and modify the content. Keep the HTML structure the same.

**Q: Can I remove sections I don't need?**
A: Yes, you can delete entire sections. Just make sure to remove their navigation links too.

**Q: How do I change the layout?**
A: Modify the Tailwind classes. Start with grid columns and spacing classes.

---

## Final Notes

### Best Practices

1. **Always backup** before making major changes
2. **Test changes locally** before uploading
3. **Keep the HTML structure** intact when editing
4. **Use Find & Replace** for bulk changes
5. **Validate your HTML** at https://validator.w3.org
6. **Test on multiple devices** before going live
7. **Monitor your analytics** to see what works

### Support

If you encounter issues:

1. Check the [Troubleshooting](#troubleshooting-common-issues) section
2. Review the relevant section in this guide
3. Check browser console for errors (F12 → Console tab)
4. Validate your HTML and CSS
5. Test in a different browser

---

**Last Updated:** January 2025

**Version:** 1.0

**Questions?** Refer to the appropriate section in this guide or consult the resources listed above.