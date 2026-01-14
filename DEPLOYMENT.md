# 🚀 DEPLOYMENT GUIDE

This guide will help you deploy your 3D Interactive Portfolio to Vercel.

## ✅ What We've Done

1. ✓ Updated README.md with your information
2. ✓ Created `.env.example` for documentation
3. ✓ Created `.env.local` with your Resend API key
4. ✓ Added `vercel.json` configuration
5. ✓ Committed and pushed changes to GitHub

## 📋 Prerequisites

- GitHub account with your repository
- Vercel account (free tier works perfectly)

## 🌐 Deploy to Vercel

### Step 1: Sign Up/Login to Vercel

1. Go to [vercel.com](https://vercel.com)
2. Click **"Sign Up"** or **"Login"**
3. Choose **"Continue with GitHub"**
4. Authorize Vercel to access your GitHub account

### Step 2: Import Your Project

1. On Vercel dashboard, click **"Add New..."** → **"Project"**
2. Find your repository: `3D-interactive-portfolio`
3. Click **"Import"**

### Step 3: Configure Project Settings

Vercel will auto-detect Next.js settings:
- **Framework Preset**: Next.js ✓
- **Root Directory**: ./ ✓
- **Build Command**: `npm run build` ✓
- **Output Directory**: `.next` ✓

### Step 4: Add Environment Variables

⚠️ **IMPORTANT**: Add your environment variables

1. In the **"Environment Variables"** section, click **"Add"**
2. Add the following:
   - **Name**: `RESEND_API_KEY`
   - **Value**: `re_a772b7i6_7MpHnXLu4ey7q7Az1ZRJrpN6`
   - **Environment**: Select all (Production, Preview, Development)

### Step 5: Deploy

1. Click **"Deploy"**
2. Wait 2-3 minutes for the build to complete
3. You'll see a success screen with your live URL! 🎉

### Step 6: Configure Custom Domain (Optional)

1. Go to your project **Settings** → **Domains**
2. Add your domain: `vasusharma.com`
3. Follow the DNS configuration instructions
4. Add both:
   - `vasusharma.com`
   - `www.vasusharma.com`

## 🔄 Automatic Deployments

Every time you push to GitHub:
- **Main branch** → Automatic production deployment
- **Other branches** → Preview deployments with unique URLs

## ⚙️ Post-Deployment Checklist

- [ ] Verify the site loads correctly
- [ ] Test the contact form (uses Resend API)
- [ ] Check 3D animations work smoothly
- [ ] Test on mobile devices
- [ ] Verify all navigation links
- [ ] Check SEO meta tags
- [ ] Test in different browsers

## 🔧 Environment Variables Reference

| Variable | Purpose | Where to Get |
|----------|---------|--------------|
| `RESEND_API_KEY` | Contact form emails | [resend.com](https://resend.com) |

## 📊 Vercel Dashboard Features

- **Deployments**: View all deployment history
- **Analytics**: Track visitor metrics (upgrade required)
- **Logs**: Debug runtime errors
- **Environment Variables**: Manage secrets safely
- **Domains**: Configure custom domains

## 🐛 Troubleshooting

### Build Fails
- Check the build logs in Vercel dashboard
- Ensure all dependencies are in `package.json`
- Verify environment variables are set correctly

### Contact Form Not Working
- Verify `RESEND_API_KEY` is set in Vercel
- Check Resend dashboard for API usage
- Ensure email domain is verified in Resend

### 3D Models Not Loading
- Check browser console for errors
- Verify public assets are committed to Git
- Ensure file paths are correct (case-sensitive)

### Slow Performance
- Enable Vercel Analytics
- Check bundle size with `npm run build`
- Consider lazy loading heavy components

## 🎯 Next Steps

1. **Add Projects**: Edit `src/data/projects.tsx` to showcase your work
2. **Custom Domain**: Configure your domain DNS
3. **Analytics**: Set up Vercel Analytics or Google Analytics
4. **SEO**: Submit sitemap to Google Search Console
5. **Social Sharing**: Test Open Graph preview on social media

## 📝 Making Updates

To update your live site:

```bash
# Make your changes
git add .
git commit -m "Your update message"
git push origin main
```

Vercel will automatically deploy within 1-2 minutes!

## 🔗 Useful Links

- **GitHub Repo**: https://github.com/vasudevsharmalive-code/3D-interactive-portfolio
- **Vercel Dashboard**: https://vercel.com/dashboard
- **Resend Dashboard**: https://resend.com/emails
- **Next.js Docs**: https://nextjs.org/docs

## 🆘 Need Help?

- Vercel Support: support@vercel.com
- Vercel Discord: https://vercel.com/discord
- Next.js Discord: https://nextjs.org/discord

---

**Deployed with ❤️ on Vercel**
