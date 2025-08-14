# DeWeerd Sweets - Setup Instructions

## Step 1: Initialize Git
Open Command Prompt or PowerShell and run:

```bash
cd "C:\Users\Greg\Documents\Claude Documents\deweerdsweets-com"
git init
```

## Step 2: Add files to Git
```bash
git add .
git commit -m "Initial commit for DeWeerd Sweets website"
```

## Step 3: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `deweerdsweets-com`
3. Make it PRIVATE
4. Don't initialize with README (we already have one)
5. Click "Create repository"

## Step 4: Connect to GitHub
After creating the repository, run these commands:

```bash
git branch -M main
git remote add origin https://github.com/acehandlin/deweerdsweets-com.git
git push -u origin main
```

## Step 5: Deploy on Netlify
1. Go to https://app.netlify.com
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub"
4. Select the `deweerdsweets-com` repository
5. Leave all settings as default
6. Click "Deploy site"

## Step 6: Configure Custom Domain
After deployment:
1. In Netlify, go to "Domain settings"
2. Click "Add custom domain"
3. Enter: `deweerdsweets.com`
4. Follow the prompts

## Step 7: Update DNS in Squarespace
1. Log into Squarespace Domains
2. Find `deweerdsweets.com`
3. Update nameservers to:
   - dns1.p01.nsone.net
   - dns2.p01.nsone.net
   - dns3.p01.nsone.net
   - dns4.p01.nsone.net

## Step 8: Wait for DNS Propagation
- Usually takes 15 minutes to a few hours
- SSL certificate will auto-provision once DNS is active

## Website Features Created:
✅ Sweet-themed design with pink/gold gradient
✅ 6 product categories (chocolates, cupcakes, cookies, cakes, seasonal, gift boxes)
✅ Contact form with inquiry types
✅ About section
✅ Responsive mobile-friendly design
✅ Smooth animations and hover effects

## Quick Commands for Updates:
After making changes to the website:
```bash
git add .
git commit -m "Update description here"
git push
```

Or use Claude Code:
```bash
claude-code "stage all changes and commit with a good message, then push to GitHub"
```