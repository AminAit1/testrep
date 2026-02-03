# Static Website Deployment Guide 🚀

A complete guide to deploying your static website to Netlify using GitHub.

## What You've Got

A professional static website with:
- Responsive design (mobile-friendly)
- Modern gradient hero section
- Service cards with hover effects
- Contact form
- Smooth scrolling navigation
- Clean, professional styling

## Prerequisites

Before starting, make sure you have:
- A GitHub account (sign up at github.com)
- A Netlify account (sign up at netlify.com - can use GitHub to sign in)
- Git installed on your computer

## Step-by-Step Deployment

### 1. Install Git (if you haven't already)

**Windows:** Download from https://git-scm.com/download/win
**Mac:** Open Terminal and run: `xcode-select --install`
**Linux:** Run: `sudo apt-get install git`

### 2. Set Up Your Local Repository

Open your terminal/command prompt and navigate to where you want to save your project:

```bash
cd Desktop  # or wherever you want the folder
mkdir my-static-site
cd my-static-site
```

Copy the three files (index.html, style.css, script.js) into this folder, then:

```bash
git init
git add .
git commit -m "Initial commit - first static website"
```

### 3. Create a GitHub Repository

1. Go to https://github.com and click the "+" icon → "New repository"
2. Name it something like "my-static-site" or "portfolio-website"
3. Keep it **public** (required for free Netlify)
4. **Don't** initialize with README (we already have files)
5. Click "Create repository"

### 4. Push Your Code to GitHub

GitHub will show you commands. Use these (replace YOUR-USERNAME and YOUR-REPO):

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git branch -M main
git push -u origin main
```

If prompted, enter your GitHub credentials.

### 5. Deploy to Netlify

1. Go to https://netlify.com and log in
2. Click "Add new site" → "Import an existing project"
3. Choose "Deploy with GitHub"
4. Authorize Netlify to access your GitHub
5. Select your repository from the list
6. Leave the settings as default:
   - Build command: (empty)
   - Publish directory: (empty or "/")
7. Click "Deploy site"

🎉 **Done!** Netlify will give you a URL like `random-name-123.netlify.app`

### 6. Customize Your Domain (Optional)

In Netlify:
1. Go to "Site settings" → "Domain management"
2. Click "Options" → "Edit site name"
3. Change to something like "yourname-portfolio.netlify.app"

Or buy a custom domain and connect it in the same section!

## Making Updates

Whenever you want to update your site:

```bash
# Make your changes to the files
git add .
git commit -m "Updated hero text"
git push
```

Netlify automatically redeploys when you push to GitHub! 🔄

## Customization Tips

### Change Colors
In `style.css`, update these lines:
- Line 46: `background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);` - Hero gradient
- Line 52: `.logo { color: #4f46e5; }` - Brand color

### Add Your Content
- Update "YourBrand" in `index.html` line 12
- Change hero text in lines 18-20
- Modify service cards starting at line 37

### Add More Pages
Create new HTML files (like `about.html`) and link them in the nav!

## Troubleshooting

**Problem:** Git push asks for username/password repeatedly
**Solution:** Set up SSH keys or use a personal access token

**Problem:** Site not updating on Netlify
**Solution:** Check the "Deploys" tab for errors, make sure you pushed to GitHub

**Problem:** CSS not loading
**Solution:** Make sure all three files are in the same folder

## Next Steps

- Add Google Analytics
- Connect a contact form backend (Netlify Forms is free!)
- Add more pages
- Customize the design
- Get a custom domain

## Resources

- [Netlify Docs](https://docs.netlify.com/)
- [GitHub Guides](https://guides.github.com/)
- [HTML/CSS Reference](https://developer.mozilla.org/en-US/)

Good luck with your side hustle! 💪
