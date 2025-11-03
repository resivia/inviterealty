# Deployment Guide - Invite Realty Website

This guide provides step-by-step instructions for deploying your rental management website to various hosting platforms.

## Quick Links

- **GitHub Repository**: https://github.com/resivia/inviterealty
- **Live Demo**: [Your deployment URL here]

## Prerequisites

Before deploying, ensure you have:
- [ ] A GitHub account with repository access
- [ ] Website files committed and pushed to GitHub
- [ ] Domain name (optional, but recommended)

## Deployment Options

### Option 1: GitHub Pages (Free & Easy)

GitHub Pages is the simplest way to host your static website for free.

**Steps:**

1. Go to your repository: https://github.com/resivia/inviterealty

2. Click **Settings** → **Pages** (in the left sidebar)

3. Under "Source":
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click **Save**

4. Wait 2-3 minutes for deployment

5. Your site will be available at: `https://resivia.github.io/inviterealty/`

**Custom Domain Setup (Optional):**
- Add a `CNAME` file with your domain name
- Configure DNS settings with your domain provider
- Add custom domain in GitHub Pages settings

### Option 2: Netlify (Recommended for Production)

Netlify offers automatic deployments, forms, and HTTPS out of the box.

**Steps:**

1. Visit https://www.netlify.com and sign up/login

2. Click **Add new site** → **Import an existing project**

3. Choose **GitHub** and authorize Netlify

4. Select repository: `resivia/inviterealty`

5. Configure build settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or use `/`)
   - Click **Deploy site**

6. Your site will be live at: `https://random-name-12345.netlify.app`

**Benefits:**
- Automatic deployments on git push
- Free SSL certificate
- Custom domain support
- Form handling (upgrade contact form)
- Edge network (fast worldwide)

**Form Integration:**
To enable Netlify form handling, add `netlify` attribute to your form:
```html
<form name="contact" method="POST" data-netlify="true">
```

### Option 3: Vercel (Modern & Fast)

Vercel provides instant deployments with excellent performance.

**Steps:**

1. Visit https://vercel.com and sign up/login

2. Click **Add New** → **Project**

3. Import from GitHub: `resivia/inviterealty`

4. Configure:
   - Framework Preset: Other
   - Build Command: (leave empty)
   - Output Directory: (leave empty)
   - Click **Deploy**

5. Your site will be live at: `https://inviterealty.vercel.app`

**Benefits:**
- Zero configuration
- Automatic HTTPS
- Global CDN
- Real-time deployment preview
- Custom domain support

### Option 4: Traditional Web Hosting

For traditional shared hosting (GoDaddy, Bluehost, etc.):

**Steps:**

1. Download your repository files or clone locally:
   ```bash
   git clone https://github.com/resivia/inviterealty.git
   ```

2. Connect to your hosting via FTP/SFTP or cPanel File Manager

3. Upload these files to your public_html or www directory:
   - index.html
   - styles.css
   - script.js
   - (any images you add)

4. Your site will be accessible at your domain

## Post-Deployment Configuration

### 1. Update Contact Information

Edit `index.html` and update:
```html
<!-- Location -->
<p>Your City, State</p>

<!-- Phone -->
<p>(555) 123-4567</p>

<!-- Email -->
<p>info@inviterealty.com</p>
```

### 2. Configure Contact Form

Choose one of these options:

**Option A: Formspree (Easy)**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
- Sign up at https://formspree.io
- Create a new form
- Replace YOUR_FORM_ID in the form action

**Option B: EmailJS (JavaScript)**
- Sign up at https://www.emailjs.com
- Create email service
- Add EmailJS SDK and configure in script.js

**Option C: Netlify Forms**
- Deploy to Netlify
- Add `data-netlify="true"` to form element
- Form submissions appear in Netlify dashboard

### 3. Add Google Analytics (Optional)

Add before closing `</head>` tag in index.html:
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

### 4. Setup Custom Domain

**DNS Configuration:**
For most hosting platforms, add these DNS records:

For root domain (inviterealty.com):
```
Type: A
Name: @
Value: [Hosting provider IP or CNAME]
```

For www subdomain:
```
Type: CNAME
Name: www
Value: [Your deployment URL]
```

**Provider-Specific:**
- **GitHub Pages**: Add CNAME file with domain
- **Netlify**: Add domain in Site Settings → Domain Management
- **Vercel**: Add domain in Project Settings → Domains

### 5. SSL Certificate

Most modern hosting platforms provide free SSL:
- **GitHub Pages**: Automatic with custom domains
- **Netlify**: Automatic (Let's Encrypt)
- **Vercel**: Automatic (Let's Encrypt)
- **Traditional Hosting**: May need to enable in cPanel or purchase

## Testing Checklist

After deployment, verify:

- [ ] Website loads correctly
- [ ] All pages/sections are accessible
- [ ] Navigation works (including mobile menu)
- [ ] Contact form submits successfully
- [ ] All links work
- [ ] Images load (if added)
- [ ] Responsive design works on mobile
- [ ] HTTPS is working (SSL certificate)
- [ ] Custom domain resolves (if configured)

## Performance Optimization

### 1. Image Optimization
When adding property images:
- Use WebP format for better compression
- Resize images to actual display size
- Use lazy loading: `<img loading="lazy" src="...">`

### 2. Caching
Add to your hosting configuration:
```
# .htaccess (Apache)
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType text/css "access plus 1 year"
  ExpiresByType application/javascript "access plus 1 year"
  ExpiresByType image/jpeg "access plus 1 year"
</IfModule>
```

### 3. CDN (Content Delivery Network)
Consider using Cloudflare for:
- Faster global delivery
- DDoS protection
- Free SSL
- Caching optimization

## Monitoring & Maintenance

### Regular Tasks
- **Weekly**: Check contact form submissions
- **Monthly**: Review analytics data
- **Quarterly**: Update service descriptions
- **Yearly**: Refresh testimonials and images

### Tools to Use
- Google Analytics (traffic monitoring)
- Google Search Console (SEO)
- Uptime Robot (uptime monitoring)
- Lighthouse (performance audits)

## Troubleshooting

### Common Issues

**1. Website not loading**
- Check DNS propagation (can take up to 48 hours)
- Verify hosting platform deployment status
- Check browser console for errors

**2. CSS/JavaScript not working**
- Verify file paths are correct
- Check for HTTPS mixed content issues
- Clear browser cache

**3. Contact form not working**
- Verify form action URL
- Check form service configuration
- Test with different email addresses

**4. Mobile menu not working**
- Check JavaScript console for errors
- Verify script.js is loading
- Test on different mobile browsers

## Support & Updates

For website updates:
1. Make changes locally or in GitHub
2. Commit and push to GitHub
3. Automatic deployment will trigger (Netlify/Vercel)
4. Or manually upload files (traditional hosting)

For issues or questions:
- Check documentation: README.md
- Review deployment logs on hosting platform
- Contact hosting support if needed

## Security Considerations

- [ ] Enable HTTPS/SSL
- [ ] Use environment variables for sensitive data
- [ ] Implement rate limiting on contact form
- [ ] Regular security updates
- [ ] Monitor for suspicious activity

---

## Quick Reference

**GitHub Repository**: https://github.com/resivia/inviterealty

**Recommended Hosting**: Netlify (free tier sufficient)

**Domain Registrar Options**: 
- Namecheap
- Google Domains
- GoDaddy

**Email Services**: 
- Google Workspace
- Microsoft 365
- Zoho Mail

---

**Need Help?** Contact your developer or refer to hosting provider documentation.

Last Updated: 2024-11-03
