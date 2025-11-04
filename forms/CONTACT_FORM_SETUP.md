# Contact Form Setup Guide

The contact form in `index.html` currently points to `forms/contact.php`, but this requires backend setup.

## Option 1: Use Formspree (Recommended - Free & Easy)

1. Go to [formspree.io](https://formspree.io/)
2. Sign up for free account
3. Create a new form and get your form endpoint
4. In `index.html` line 575, change:
   ```html
   <form action="forms/contact.php" method="post" ...>
   ```
   To:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="post" ...>
   ```

## Option 2: Use Web3Forms (Free)

1. Go to [web3forms.com](https://web3forms.com/)
2. Get your access key
3. Add hidden field to form in `index.html`:
   ```html
   <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
   ```
4. Change form action to:
   ```html
   <form action="https://api.web3forms.com/submit" method="POST" ...>
   ```

## Option 3: Use EmailJS (JavaScript-based)

1. Go to [emailjs.com](https://www.emailjs.com/)
2. Set up email service
3. Add EmailJS script and modify form submission with JavaScript

## Option 4: Keep PHP (Requires Hosting)

If you have PHP hosting:
1. Restore `contact.php` from template
2. Install PHP Email Form library (pro version)
3. Configure SMTP settings in contact.php

## Current Status

❌ Contact form is NOT functional
✅ Form UI works and looks good
⚠️ Choose one option above to make it functional

## Recommendation

For GitHub Pages / static hosting → Use **Formspree** or **Web3Forms**
For PHP hosting → Set up PHP backend

---

After setup, test your contact form thoroughly!

