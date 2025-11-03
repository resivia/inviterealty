# Invite Realty - Rental Management Website

A modern, professional website for Invite Realty's rental management services. This website showcases comprehensive property management solutions for landlords and property owners.

## Features

- **Responsive Design**: Fully responsive layout that works seamlessly on desktop, tablet, and mobile devices
- **Modern UI/UX**: Clean, professional design with smooth animations and transitions
- **Service Showcase**: Detailed presentation of all rental management services
- **Contact Form**: Interactive form for consultation scheduling
- **Smooth Navigation**: Sticky navigation bar with smooth scrolling to sections
- **SEO Optimized**: Semantic HTML structure for better search engine visibility

## Services Highlighted

1. **Tenant Screening**: Rigorous background checks and verification processes
2. **Maintenance Services**: 24/7 property support and maintenance coordination
3. **Financial Transparency**: Detailed reporting and online account access
4. **Local Expertise**: Market knowledge and area-specific insights

## Technology Stack

- **HTML5**: Semantic markup for better accessibility
- **CSS3**: Modern styling with custom properties and flexbox/grid layouts
- **Vanilla JavaScript**: Interactive features without dependencies
- **Google Fonts**: Inter font family for professional typography

## File Structure

```
inviterealty/
├── index.html          # Main HTML file
├── styles.css          # CSS styling
├── script.js           # JavaScript functionality
└── README.md          # Documentation
```

## Getting Started

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/resivia/inviterealty.git
cd inviterealty
```

2. Open `index.html` in your web browser or use a local development server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server -p 8000
```

3. Visit `http://localhost:8000` in your browser

### Deployment

This is a static website and can be deployed to various hosting platforms:

#### GitHub Pages
1. Go to repository Settings > Pages
2. Select main branch as source
3. Save and wait for deployment
4. Access at: `https://resivia.github.io/inviterealty/`

#### Netlify
1. Connect your GitHub repository
2. Configure build settings (none needed for static site)
3. Deploy automatically on push

#### Vercel
1. Import GitHub repository
2. Deploy with zero configuration
3. Get instant HTTPS deployment

## Customization

### Update Company Information

Edit `index.html` to update:
- Company name and branding
- Contact information (phone, email, address)
- Service descriptions
- Call-to-action buttons

### Modify Colors

Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --primary-dark: #1e40af;       /* Darker shade */
    --secondary-color: #10b981;    /* Secondary/accent color */
}
```

### Add Images

Replace the placeholder image section in `index.html` with actual property images:
```html
<div class="benefits-image">
    <img src="your-image.jpg" alt="Description">
</div>
```

### Form Integration

To connect the contact form to a backend:

1. Update the form submission handler in `script.js`
2. Use a service like:
   - Formspree
   - EmailJS
   - Custom backend API
   - Netlify Forms

Example with Formspree:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Minimal dependencies (no frameworks)
- Optimized CSS and JavaScript
- Fast loading times
- Mobile-first responsive design

## Accessibility

- Semantic HTML structure
- ARIA labels where appropriate
- Keyboard navigation support
- Responsive text sizing

## Future Enhancements

Potential features to add:
- [ ] Property listing/portfolio section
- [ ] Testimonials slider
- [ ] Blog for property management tips
- [ ] Owner/tenant portal integration
- [ ] Multi-language support
- [ ] Property calculator tool
- [ ] Newsletter signup
- [ ] Live chat integration

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

## License

This project is proprietary and owned by Invite Realty.

## Contact

For questions or support, contact:
- Email: info@inviterealty.com
- Phone: (555) 123-4567
- Website: [Your Website URL]

## Acknowledgments

- Design inspired by modern real estate and property management websites
- Icons from Feather Icons (via inline SVG)
- Fonts from Google Fonts (Inter)

---

Built with ❤️ for Invite Realty
