# irawolfson.com

Personal academic website for Ira Wolfson.

## Files Included

```
irawolfson-site/
├── index.html          # About page (home)
├── research.html       # Research projects
├── publications.html   # Academic publications
├── teaching.html       # Courses and teaching
├── sunburst.html       # SunBURST tool page
├── services.html       # Science! At Your Service (coming soon)
├── dossier.html        # Prediction Dossiers (coming soon)
├── contact.html        # Contact information
├── assets/
│   ├── style.css       # Shared stylesheet
│   └── images/
│       ├── sunburst-logo.png
│       └── science-service-logo.png
└── README.md           # This file
```

## Deployment Instructions

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create an account)
2. Click the **+** button → **New repository**
3. Name it exactly: `irawolfson.github.io`
4. Make it **Public**
5. Click **Create repository**

### Step 2: Upload Site Files

**Option A: Using GitHub's web interface (easier)**

1. In your new repository, click **"uploading an existing file"**
2. Drag all the files from this folder into the upload area
3. Make sure to preserve the folder structure (assets/ folder with its contents)
4. Click **Commit changes**

**Option B: Using Git command line**

```bash
cd irawolfson-site
git init
git add .
git commit -m "Initial site"
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/irawolfson.github.io.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository → **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Select **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait 2-3 minutes, then visit: `https://YOUR_GITHUB_USERNAME.github.io`

### Step 4: Point Your Domain (GoDaddy)

In GoDaddy DNS Management for irawolfson.com:

1. Delete any existing A records or CNAME for @ or www

2. Add these **A records** for @ (root domain):
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

3. Add a **CNAME record** for www:
   - Host: www
   - Points to: YOUR_GITHUB_USERNAME.github.io

4. Back in GitHub repo Settings → Pages:
   - Under "Custom domain", enter: irawolfson.com
   - Click Save
   - Check "Enforce HTTPS" after DNS propagates (~1-48 hours)

## Updating Content

**To edit pages:**
1. Go to your repository on GitHub
2. Click on the file you want to edit (e.g., `publications.html`)
3. Click the pencil icon (Edit)
4. Make your changes
5. Click "Commit changes"

**To add your CV:**
1. Rename your CV file to `cv.pdf`
2. Upload it to the `assets/` folder in your repository

**To add teaching materials:**
1. Create folders like `teaching/em-fields/` or `teaching/matlab/`
2. Upload materials there
3. Uncomment the links in `teaching.html`

## What You'll Need to Add

1. **Your CV** as `assets/cv.pdf`
2. **Teaching materials** in `teaching/` subfolders (optional)
3. **Update publications** as papers are accepted/published
4. **Fill in Services page** when ready to launch Science! At Your Service
5. **Fill in Dossier page** when ready to launch prediction dossiers
