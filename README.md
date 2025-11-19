# Threshold Insights Website

Coming soon landing page for Threshold Insights - a biopharma and drug development consultancy.

## Repository Contents

- `index.html` - Main landing page
- `Threshold_insights_final_logo.png` - Company logo
- `README.md` - This file
- `CNAME` - Custom domain configuration for thresholdpharma.com

## Deployment Instructions

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Repository settings:
   - **Repository name**: `threshold-insights-website` (or any name you prefer)
   - **Description**: "Threshold Insights coming soon page"
   - **Visibility**: Public (required for free GitHub Pages)
   - **Do NOT** initialise with README, .gitignore, or license
5. Click "Create repository"

### Step 2: Upload Files to GitHub

**Option A: Using GitHub Web Interface (Easiest)**

1. On your new repository page, click "uploading an existing file"
2. Drag and drop all files from this folder:
   - index.html
   - Threshold_insights_final_logo.png
   - CNAME (if using custom domain)
3. Add commit message: "Initial commit - coming soon page"
4. Click "Commit changes"

**Option B: Using Git Command Line**

```bash
# Navigate to this folder in your terminal
cd /path/to/threshold-insights-website

# Initialise git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit - coming soon page"

# Add your GitHub repository as remote (replace with your repository URL)
git remote add origin https://github.com/YOUR-USERNAME/threshold-insights-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (top navigation)
3. Click "Pages" in the left sidebar
4. Under "Source":
   - Select "Deploy from a branch"
   - Branch: Select "main"
   - Folder: Select "/ (root)"
5. Click "Save"
6. GitHub will provide a URL (e.g., `https://YOUR-USERNAME.github.io/threshold-insights-website/`)
7. Your site will be live within 1-2 minutes

### Step 4: Configure Custom Domain (thresholdpharma.com)

#### On GitHub:

1. In Settings > Pages, find "Custom domain"
2. Enter: `thresholdpharma.com`
3. Click "Save"
4. Check "Enforce HTTPS" (wait a few minutes for certificate generation)

#### On Your Domain Registrar:

You need to configure DNS records. Add these records to your domain's DNS settings:

**Option A: Using A Records (Recommended)**

Add these four A records pointing to GitHub's servers:

```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**AND** add a CNAME record for www subdomain:

```
Type: CNAME
Name: www
Value: YOUR-USERNAME.github.io
```

**Option B: Using CNAME Record (Alternative)**

```
Type: CNAME
Name: @
Value: YOUR-USERNAME.github.io
```

**DNS Propagation**: Changes can take 24-48 hours to fully propagate, though often much faster.

### Step 5: Verify Deployment

1. Visit your GitHub Pages URL to confirm the site is live
2. Once DNS propagates, visit `https://thresholdpharma.com`
3. Verify the page displays correctly and the email link works

## Making Updates

To update the website:

1. Edit files locally
2. Commit and push changes to GitHub:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push
   ```
3. Changes will appear on the live site within 1-2 minutes

## Technical Details

- **Framework**: Pure HTML/CSS (no dependencies)
- **Responsive**: Mobile-optimised
- **Performance**: Lightweight, fast loading
- **Accessibility**: WCAG AA compliant contrast ratios
- **Browser Support**: All modern browsers

## Support

For questions about the website, contact lavinia@thresholdinsights.com

---

**Built with GitHub Pages** | **Last updated**: November 2025