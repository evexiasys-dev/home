# Evexia Wellness Center - Homepage

A stunning, professional, and interactive homepage for Evexia Wellness Center featuring modern design, smooth animations, and a pulsing event announcement strip.

## 🌟 Features

- **Pulsing Event Strip**: Eye-catching announcement banner at the top showcasing the "Puso ko, Mahal ko!" Heart Month event
- **Responsive Design**: Fully optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: CSS animations and transitions for enhanced user experience
- **Interactive Elements**: Hover effects, parallax scrolling, and smooth scroll navigation
- **Modern UI/UX**: Clean, professional design aligned with Evexia's wellness branding
- **Navigation Menu**: Fixed navbar with smooth scrolling to sections
- **Multiple Sections**:
  - Hero section with brand logo and call-to-action buttons
  - About section with statistics
  - Services showcase with 6 service cards
  - Events section featuring upcoming programs
  - Testimonials from satisfied clients
  - Contact section with form and location details
  - Google Maps integration
  - Footer with social media links

## 📁 File Structure

```
evexia-homepage/
├── index.html              # Main HTML file
├── css/
│   └── homepage.css        # Stylesheet with all styling and animations
├── js/
│   └── homepage.js         # JavaScript for interactivity
└── assets/
    └── images/
        ├── EWC-logo.png    # Main Evexia logo
        ├── favicon.png     # Browser favicon
        ├── header-bg.png   # Background image
        └── preview.png     # Social media preview
```

## 🚀 Setup Instructions

### Option 1: Local Development

1. **Extract all files** maintaining the folder structure
2. **Open with a local server** (required for proper functionality):

   **Using Python:**
   ```bash
   # Navigate to the evexia-homepage folder
   cd evexia-homepage
   
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```

   **Using Node.js:**
   ```bash
   npx http-server -p 8000
   ```

   **Using VS Code Live Server:**
   - Install the Live Server extension
   - Right-click on `index.html`
   - Select "Open with Live Server"

3. **Access the site** at `http://localhost:8000`

### Option 2: Deployment

#### GitHub Pages
1. Create a new repository on GitHub
2. Upload all files maintaining the folder structure
3. Go to Settings → Pages
4. Select your branch (usually `main`) and root folder
5. Click Save
6. Your site will be live at `https://[username].github.io/[repo-name]/`

#### Netlify
1. Create account at netlify.com
2. Drag and drop the `evexia-homepage` folder
3. Site will be live instantly with a random URL
4. Customize domain in settings

#### Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Navigate to the folder: `cd evexia-homepage`
3. Run: `vercel`
4. Follow the prompts

## 🎨 Customization Guide

### Updating the Event Strip

The pulsing event announcement is in the HTML at the top. To update:

```html
<!-- Find this section in index.html -->
<div class="event-strip" id="eventStrip">
  <div class="event-strip-content">
    <div class="event-pulse"></div>
    <span class="event-text">
      <i class="fas fa-heart"></i>
      <strong>Heart Month Special:</strong> Your event text here
    </span>
    <a href="your-link.html" class="event-btn">Know the Event</a>
  </div>
</div>
```

### Changing Colors

Edit the CSS variables in `css/homepage.css`:

```css
:root {
    --primary-green: #4CAF50;    /* Main brand color */
    --dark-green: #3D8B40;       /* Darker shade */
    --accent-coral: #FF6B6B;     /* Accent color */
    --accent-teal: #4ECDC4;      /* Secondary accent */
    /* ... more colors ... */
}
```

### Updating Content

- **Services**: Edit the `.service-card` sections in the HTML
- **Testimonials**: Edit the `.testimonial-card` sections
- **Events**: Edit the `.event-card` sections
- **Contact Info**: Update the `.contact-item` sections
- **About Text**: Modify the `.about-content` section

### Adding New Sections

1. Add the HTML section between existing sections
2. Add corresponding styles in `homepage.css`
3. Update navigation menu in both HTML and JavaScript

## 🔧 Key Features Explained

### Event Strip Behavior
- **Pulsing animation**: The yellow dot pulses continuously
- **Heartbeat icon**: Animated heart icon draws attention
- **Hide on scroll**: Strip hides when scrolling down, reappears when scrolling up
- **Responsive**: Stacks vertically on mobile devices

### Navigation
- **Fixed position**: Navbar stays at top while scrolling
- **Transparent initially**: Becomes opaque with blur effect when scrolled
- **Active state**: Highlights current section
- **Mobile menu**: Hamburger menu for mobile devices

### Animations
- **Scroll-triggered**: Elements fade in as you scroll
- **Parallax effect**: Hero content moves slower than page scroll
- **Hover effects**: Cards lift and tilt on hover
- **Counter animation**: Statistics count up when in view

## 📱 Responsive Breakpoints

- **Desktop**: 1024px and above
- **Tablet**: 768px to 1023px
- **Mobile**: Below 768px

## 🌐 Browser Compatibility

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ⚠️ IE11 (limited support)

## 📞 Integration Notes

### Linking to Event Page

The event strip button currently links to `puso-ko-mahal-ko.html`. Make sure this file exists in the same directory as `index.html`, or update the link:

```html
<a href="puso-ko-mahal-ko.html" class="event-btn">Know the Event</a>
```

### Contact Form

The contact form currently shows an alert on submission. To connect to a backend:

1. **Google Forms**: Use form action with Google Forms
2. **Email service**: Integrate with FormSpree, EmailJS, or similar
3. **Backend API**: Connect to your own server endpoint

Update the form handler in `js/homepage.js`:

```javascript
contactForm.addEventListener('submit', function (e) {
    e.preventDefault();
    // Add your form submission logic here
});
```

### Google Maps

The embedded map is already configured for Evexia Wellness Center. To update:

1. Go to [Google Maps](https://www.google.com/maps)
2. Search for your location
3. Click "Share" → "Embed a map"
4. Copy the iframe code
5. Replace the existing iframe in the HTML

## 🎯 Performance Tips

1. **Optimize images**: Compress all images before upload
2. **Minify CSS/JS**: Use build tools for production
3. **Enable caching**: Configure server caching headers
4. **Use CDN**: Consider using a CDN for Font Awesome and Google Fonts

## 🔒 Security Notes

- No sensitive data is collected client-side
- All external resources use HTTPS
- Form validation is implemented
- Consider adding CSRF protection for forms

## 📝 Credits

- **Design & Development**: Ransel Sumatra
- **Client**: Evexia Wellness Center
- **Fonts**: Google Fonts (Plus Jakarta Sans)
- **Icons**: Font Awesome 6
- **Maps**: Google Maps Platform

## 📄 License

This website is proprietary to Evexia Wellness Center. All rights reserved.

## 🆘 Support

For questions or support:
- Email: info@evexiawellnesscenter.com
- Developer: [@ranselberry](https://www.instagram.com/ranselberry/)

---

**Made with 💚 for Evexia Wellness Center**

*Wellness from Within*