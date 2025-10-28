# GitHub Pages Deployment Guide

## 📋 Prerequisites

- GitHub account with `gigvault` organization
- Local `.github` repository ready to push

## 🚀 Step-by-Step Deployment

### Step 1: Create Repository on GitHub

1. Go to: https://github.com/organizations/gigvault/repositories/new
2. Repository name: **`.github`** (exactly this name)
3. Description: `GigVault Organization Profile & Website`
4. Visibility: **Public** (required for GitHub Pages)
5. ✅ **DO NOT** initialize with README (we already have one)
6. Click **"Create repository"**

### Step 2: Push Local Repository

```bash
# Navigate to .github directory
cd /Users/fatihturker/Desktop/Personal/Dev/gigvault/.github

# Verify git remote (should already exist)
git remote -v

# If remote doesn't exist, add it:
git remote add origin https://github.com/gigvault/.github.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to: https://github.com/gigvault/.github
2. Click **"Settings"** tab (top right)
3. Scroll down to **"Pages"** section (left sidebar)
4. Under **"Build and deployment"**:
   - **Source**: Deploy from a branch
   - **Branch**: `main`
   - **Folder**: `/docs` (NOT root!)
5. Click **"Save"**

### Step 4: Wait for Deployment

1. GitHub will automatically build and deploy (takes 1-2 minutes)
2. You'll see a message: "Your site is ready to be published at..."
3. After deployment completes, you'll see: 
   > ✅ Your site is live at https://gigvault.github.io/.github/

### Step 5: Access Your Website

🌐 **Website URL**: https://gigvault.github.io/.github/

Alternative URLs that also work:
- https://gigvault.github.io/.github/docs/
- https://gigvault.github.io/.github/docs/index.html

## 🔍 Troubleshooting

### Issue: "404 - Page Not Found"

**Solution 1**: Wait 2-3 minutes for initial deployment

**Solution 2**: Check deployment status
1. Go to: https://github.com/gigvault/.github/deployments
2. Look for "github-pages" deployment
3. If failed, check the error log

**Solution 3**: Verify Pages settings
- Settings → Pages
- Branch: `main`
- Folder: `/docs` ⚠️ (NOT root!)

### Issue: "Site not updating"

**Solution**: Clear GitHub Pages cache
1. Make a small change to `docs/index.html`
2. Commit and push
3. Wait 1-2 minutes

### Issue: "CSS/Styles not loading"

**Solution**: All styles are inline in `index.html`, should work automatically

## 📁 File Structure

```
.github/
├── README.md           # Organization profile (appears on org page)
├── docs/
│   └── index.html     # Website (GitHub Pages serves from here)
└── DEPLOY_GUIDE.md    # This file
```

## 🎨 Customization

### Custom Domain (Optional)

1. Buy a domain (e.g., gigvault.dev)
2. Settings → Pages → Custom domain
3. Add your domain
4. Add DNS records at your registrar:
   ```
   Type: CNAME
   Name: www
   Value: gigvault.github.io
   ```

### Analytics (Optional)

Add Google Analytics to `docs/index.html` before `</body>`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

## ✅ Success Checklist

- [ ] Repository created: `gigvault/.github`
- [ ] Files pushed to GitHub
- [ ] GitHub Pages enabled (Settings → Pages)
- [ ] Source: `main` branch, `/docs` folder
- [ ] Deployment successful (check Actions tab)
- [ ] Website accessible: https://gigvault.github.io/.github/

## 📞 Support

If issues persist:
1. Check GitHub Pages status: https://www.githubstatus.com/
2. Verify repository is public
3. Check deployment logs in Actions tab
4. Ensure `docs/index.html` exists and is valid HTML

---

**Note**: The `.github` repository name is special - it's used for organization profile AND GitHub Pages. This is why we use `/docs` folder for the website.

