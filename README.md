# Joe's Mows - Lawn Care Website

A professional, responsive website for Joe's Mows lawn care services, inspired by modern lawn care company websites.

## Features

- **Fully Responsive Design** - Works perfectly on desktop, tablet, and mobile devices
- **Modern UI/UX** - Clean, professional design with smooth animations
- **Service Showcase** - Detailed sections for all lawn care services
- **Contact Form** - Easy-to-use form for quote requests
- **Service Areas** - Display of coverage areas
- **SEO Optimized** - Proper meta tags and semantic HTML
- **Fast Loading** - Optimized CSS and JavaScript

## Structure

```
joes-mows-website/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # Interactive functionality
└── README.md          # This file
```

## Getting Started

### Option 1: Open Directly
Simply open `index.html` in your web browser.

### Option 2: Use a Local Server
For a better development experience:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js (with npx)
npx serve

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Customization Guide

### 1. Business Information

**Contact Details** (in `index.html`):
- Phone: Search for `770-555-MOWS` and replace with actual number
- Email: Search for `info@joesmows.com` and replace with actual email
- Hours: Update in the contact section

**Service Areas** (in `index.html`):
- Update the area cards in the Service Areas section with your actual coverage areas

### 2. Colors and Branding

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #2d7a3e;      /* Main brand color */
    --primary-dark: #1f5a2d;       /* Darker shade */
    --secondary-color: #5fb878;     /* Accent color */
    --accent-color: #ffa500;        /* Highlight color */
}
```

### 3. Services

Edit the services in the Services section of `index.html`:
- Add/remove service cards
- Update service descriptions
- Change service icons (using emojis or add Font Awesome)

### 4. Images

Replace placeholder images:
- Hero section: Update the background in the `.hero` CSS class
- About section: Replace the `.image-placeholder` div with an actual `<img>` tag

### 5. Add Google Fonts

The site uses Google Fonts (Montserrat and Open Sans). To change fonts:
1. Visit [Google Fonts](https://fonts.google.com)
2. Select your fonts
3. Replace the font link in the `<head>` section
4. Update font-family references in `styles.css`

## Adding Functionality

### Form Submission

Currently, the form prevents default submission and shows a success message. To connect to a backend:

**Option 1: Email Service (Formspree, EmailJS)**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**Option 2: Custom Backend**
Update the form handler in `script.js` to send data to your API endpoint.

### Google Analytics

Add between `<head>` tags:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Live Chat

Add popular chat widgets like:
- **Tawk.to** (Free)
- **Intercom**
- **LiveChat**

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Minimal external dependencies
- Optimized CSS with modern features
- Vanilla JavaScript (no frameworks needed)
- Lazy loading animations

## SEO Optimization

The site includes:
- Semantic HTML5 elements
- Meta descriptions
- Proper heading hierarchy
- Alt text for images (when added)
- Mobile-friendly design
- Fast load times

### Next Steps for SEO:
1. Add real images with proper alt text
2. Create a sitemap.xml
3. Add robots.txt
4. Submit to Google Search Console
5. Set up Google Business Profile
6. Get listed in local directories

## Hosting Options

### Free Options:
- **Netlify** - `netlify deploy`
- **Vercel** - `vercel`
- **GitHub Pages** - Push to GitHub and enable Pages
- **Cloudflare Pages**

### Paid Options:
- Traditional web hosting (GoDaddy, Bluehost, etc.)
- VPS (DigitalOcean, Linode)
- WordPress hosting (if converting to WordPress)

## Converting to WordPress

If you want to use this design with WordPress:
1. Create a custom theme
2. Convert HTML sections to PHP template files
3. Integrate with WordPress loops and functions
4. Add custom post types for services

## License

This website template is free to use and modify for your business.

## Support

For customization help or questions:
- Review the code comments
- Check browser console for any errors
- Ensure all files are in the same directory

## Future Enhancements

Consider adding:
- [ ] Blog section for lawn care tips
- [ ] Customer testimonials/reviews
- [ ] Photo gallery of completed work
- [ ] Online booking system
- [ ] Payment integration
- [ ] Before/After image sliders
- [ ] Service pricing calculator
- [ ] Live availability calendar
- [ ] Customer portal/login area
- [ ] Seasonal promotions banner

---

Built with ❤️ for Joe's Mows
