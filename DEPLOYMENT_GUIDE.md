# 🚀 Deployment Guide

This guide provides step-by-step instructions for deploying your 3D Interactive Portfolio to GitHub, Vercel, and Netlify.

## 📋 Pre-Deployment Checklist

- [x] All code is building successfully (`npm run build`)
- [x] Environment variables are set up
- [x] Responsive design tested (mobile, tablet, desktop)
- [x] SEO metadata configured
- [x] Performance optimizations applied
- [x] Security headers implemented

## 🔧 Environment Variables

Create a `.env.local` file with the following variables:

```env
# Analytics (Optional)
UMAMI_DOMAIN=your_umami_domain
UMAMI_SITE_ID=your_site_id

# Email Service (Optional - for contact form)
RESEND_API_KEY=your_resend_api_key
```

## 📦 GitHub Setup

### 1. Initialize Git Repository

```bash
# Initialize git if not already done
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit: Portfolio ready for deployment"
```

### 2. Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository (e.g., `3D-interactive-portfolio`)
3. **Do NOT** initialize with README, .gitignore, or license

### 3. Push to GitHub

```bash
# Add remote repository
git remote add origin https://github.com/YOUR_USERNAME/3D-interactive-portfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## ▲ Vercel Deployment

### Option 1: Deploy via Vercel Dashboard (Recommended)

1. Go to [Vercel](https://vercel.com)
2. Click "Add New Project"
3. Import your GitHub repository
4. Configure project:
   - **Framework Preset**: Next.js
   - **Build Command**: `npm run build`
   - **Output Directory**: `.next`
   - **Install Command**: `npm install`
5. Add environment variables (if any)
6. Click "Deploy"

### Option 2: Deploy via Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Deploy to production
vercel --prod
```

### Vercel Configuration

The project includes a `vercel.json` file with optimal settings:

```json
{
  "buildCommand": "npm run build",
  "devCommand": "npm run dev",
  "installCommand": "npm install",
  "framework": "nextjs",
  "outputDirectory": ".next"
}
```

## 🌐 Netlify Deployment

### Option 1: Deploy via Netlify Dashboard

1. Go to [Netlify](https://netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Choose GitHub and authorize Netlify
4. Select your repository
5. Configure build settings:
   - **Build command**: `npm run build`
   - **Publish directory**: `.next`
   - **Node version**: 18
6. Add environment variables (if any)
7. Click "Deploy site"

### Option 2: Deploy via Netlify CLI

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Initialize and deploy
netlify init
netlify deploy --prod
```

### Netlify Configuration

The project includes a `netlify.toml` file:

```toml
[build]
  command = "npm run build"
  publish = ".next"

[[plugins]]
  package = "@netlify/plugin-nextjs"

[build.environment]
  NODE_VERSION = "18"
```

### Install Netlify Next.js Plugin

For Netlify deployments, install the Next.js plugin:

```bash
npm install --save-dev @netlify/plugin-nextjs
```

Or add it in the Netlify dashboard under "Plugins".

## 🎨 Custom Domain Setup

### Vercel

1. Go to your project settings
2. Navigate to "Domains"
3. Add your custom domain
4. Update DNS records as instructed:
   - Add A record: `76.76.21.21`
   - Or CNAME record pointing to your Vercel project

### Netlify

1. Go to "Domain settings"
2. Click "Add custom domain"
3. Follow DNS configuration instructions
4. Enable HTTPS (automatic via Let's Encrypt)

## 📱 Responsive Design Verification

The portfolio is optimized for:

- **Mobile**: 320px - 767px
- **Tablet**: 768px - 1023px
- **Desktop**: 1024px and above

Test responsiveness:
- Use browser DevTools (F12) → Device toolbar
- Test on real devices
- Use [Responsive Design Checker](https://responsivedesignchecker.com/)

## ⚡ Performance Optimizations Applied

✅ **Image Optimization**
- Next.js Image component support
- AVIF and WebP formats
- Responsive image sizes

✅ **Code Optimization**
- SWC minification
- Tree shaking
- Code splitting
- Console removal in production

✅ **Security Headers**
- HSTS
- X-Frame-Options
- Content Security Policy
- XSS Protection

✅ **SEO**
- Meta tags
- Open Graph
- Twitter Cards
- Structured data
- Sitemap support

## 🔍 Post-Deployment Checks

### 1. Verify Deployment

- [ ] Site loads correctly
- [ ] All pages accessible
- [ ] 3D animations working
- [ ] Forms submitting (if applicable)
- [ ] Dark/Light theme toggle
- [ ] Responsive layout on all devices

### 2. Test Performance

Use these tools:
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [GTmetrix](https://gtmetrix.com/)

Target scores:
- Performance: 90+
- Accessibility: 90+
- Best Practices: 90+
- SEO: 90+

### 3. SEO Verification

- [ ] Meta tags present
- [ ] Open Graph tags working
- [ ] Robots.txt accessible
- [ ] Sitemap generated
- [ ] Google Search Console setup

## 🐛 Troubleshooting

### Build Fails

```bash
# Clear cache and rebuild
rm -rf .next node_modules
npm install
npm run build
```

### Environment Variables Not Working

- Ensure variables are prefixed with `NEXT_PUBLIC_` for client-side access
- Redeploy after adding/updating environment variables
- Check variable names match exactly (case-sensitive)

### 3D Models Not Loading

- Verify public folder structure
- Check file paths are correct
- Ensure files are committed to Git
- Check file sizes (large files may timeout)

### Responsive Issues

- Test with browser DevTools
- Check Tailwind breakpoints
- Verify viewport meta tag
- Test on actual devices

## 📊 Analytics Setup (Optional)

### Google Analytics

1. Create GA4 property
2. Add tracking code to `layout.tsx`
3. Redeploy

### Umami Analytics (Privacy-friendly)

1. Set up Umami instance or use cloud
2. Add environment variables:
   ```env
   UMAMI_DOMAIN=https://your-umami-instance.com/script.js
   UMAMI_SITE_ID=your-site-id
   ```
3. Redeploy

## 🔄 Continuous Deployment

Both Vercel and Netlify support automatic deployments:

- **Production**: Triggered on push to `main` branch
- **Preview**: Triggered on pull requests
- **Development**: Can be linked to `dev` branch

Configure branch deployments in:
- Vercel: Settings → Git
- Netlify: Site settings → Build & deploy

## 📝 Update Workflow

```bash
# Make changes to your code
git add .
git commit -m "Description of changes"
git push origin main

# Automatic deployment will trigger
```

## 🎉 Success!

Your portfolio is now live! Share it with:

- LinkedIn
- GitHub README
- Resume
- Professional networks

---

## 📚 Additional Resources

- [Next.js Deployment Documentation](https://nextjs.org/docs/deployment)
- [Vercel Documentation](https://vercel.com/docs)
- [Netlify Documentation](https://docs.netlify.com/)
- [Web Performance Best Practices](https://web.dev/performance/)

## 🤝 Support

For issues or questions:
- Check the [troubleshooting](#-troubleshooting) section
- Review platform-specific documentation
- Open an issue on GitHub

---

**Built with ❤️ using Next.js, Three.js, and Modern Web Technologies**
