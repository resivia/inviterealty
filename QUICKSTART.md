# Quick Start Guide - Invite Realty Website

Get your rental management website live in under 10 minutes!

## 🚀 Fastest Path to Deployment (Netlify)

### Step 1: Open Netlify (2 minutes)
1. Go to: https://www.netlify.com
2. Click **"Sign up"** or **"Log in"**
3. Choose **"Sign up with GitHub"**
4. Authorize Netlify to access your repositories

### Step 2: Deploy Your Site (1 minute)
1. Click **"Add new site"** → **"Import an existing project"**
2. Select **"Deploy with GitHub"**
3. Search for and select: **`inviterealty`**
4. Leave all settings as default
5. Click **"Deploy inviterealty"**

### Step 3: Wait for Deployment (2 minutes)
- Watch the deployment progress
- Your site will be live at: `https://random-name-12345.netlify.app`
- You can customize this URL or add your own domain

### ✅ Done! Your website is live!

---

## 📱 View Your Live Site

**Temporary Preview**: https://8000-isvtwufq0sb7omuj2649k-583b4d74.sandbox.novita.ai

**After Netlify Deployment**: Check your Netlify dashboard for the live URL

---

## 🎯 Essential Customizations (5 minutes)

### 1. Update Contact Information
Open `index.html` and find these lines to update:

**Location** (around line 204):
```html
<p>Your City, State</p>
```
Change to:
```html
<p>Los Angeles, California</p>
```

**Phone** (around line 216):
```html
<p>(555) 123-4567</p>
```
Change to your real phone number

**Email** (around line 228):
```html
<p>info@inviterealty.com</p>
```
Change to your real email

### 2. Connect Contact Form (Netlify)
In `index.html`, find the `<form>` tag (around line 161) and add:
```html
<form class="contact-form" id="contactForm" name="contact" method="POST" data-netlify="true">
```

Just add: `name="contact" method="POST" data-netlify="true"`

### 3. Commit and Push Changes
```bash
git add .
git commit -m "Update contact information"
git push origin main
```

Netlify will automatically redeploy with your changes!

---

## 🎨 Optional: Customize Colors (2 minutes)

Open `styles.css` and find the `:root` section (around line 11):

```css
:root {
    --primary-color: #2563eb;      /* Main blue color */
    --secondary-color: #10b981;    /* Green accent */
}
```

Change to your brand colors! Try:
- Real Estate Blue: `#1e40af`
- Professional Green: `#059669`
- Elegant Purple: `#7c3aed`

---

## 📊 Check Your GitHub Repository

**Repository URL**: https://github.com/resivia/inviterealty

What's in your repo:
- ✅ Complete website code
- ✅ Full documentation
- ✅ Deployment guides
- ✅ Ready for customization

---

## 🔗 Important Links

| What | Where |
|------|-------|
| 🌐 Live Preview | https://8000-isvtwufq0sb7omuj2649k-583b4d74.sandbox.novita.ai |
| 📦 GitHub Repo | https://github.com/resivia/inviterealty |
| 📝 Pull Request | https://github.com/resivia/inviterealty/pull/1 |
| 📚 Full Documentation | See README.md |
| 🚀 Deployment Guide | See DEPLOYMENT.md |
| 📋 Project Summary | See PROJECT_SUMMARY.md |

---

## ❓ FAQ

### How do I add my own domain?
1. In Netlify dashboard, go to **Domain settings**
2. Click **"Add custom domain"**
3. Follow the DNS configuration steps
4. SSL certificate is automatic!

### How do I receive form submissions?
With Netlify Forms (already configured):
- Go to your Netlify site dashboard
- Click **"Forms"** in the menu
- All submissions appear there
- Set up email notifications in settings

### How do I add images?
1. Create an `images` folder in your project
2. Add your photos
3. Update `index.html` image sources:
   ```html
   <img src="images/property1.jpg" alt="Property">
   ```
4. Commit and push to GitHub

### How do I update content?
1. Edit `index.html` directly
2. Save your changes
3. Commit: `git commit -am "Update content"`
4. Push: `git push origin main`
5. Netlify auto-deploys in 1-2 minutes!

---

## 🆘 Need Help?

1. **Check the docs**: Read DEPLOYMENT.md for detailed guides
2. **Review code**: All code is commented for clarity
3. **Test locally**: Run `python3 -m http.server 8000`
4. **GitHub Issues**: Report problems in your repository

---

## 🎉 Congratulations!

Your professional rental management website is ready to help you grow your business!

**Next Steps**:
1. ✅ Deploy to Netlify (10 minutes)
2. ✅ Update contact information (5 minutes)
3. ✅ Add your branding and photos
4. ✅ Share your website URL with clients!

---

**Made with ❤️ for Invite Realty**

Ready to manage properties like a pro! 🏠
