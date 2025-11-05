# GitHub Pages Deployment Guide

## 📚 Complete Setup Instructions

### Step 1: Prepare Your Repository

1. **Ensure you're on the main branch:**
   ```powershell
   git checkout main
   ```

2. **Merge your develop branch into main:**
   ```powershell
   git merge develop
   ```

3. **Add all files to git:**
   ```powershell
   git add .
   ```

4. **Commit your changes:**
   ```powershell
   git commit -m "Add GitHub Pages deployment workflow"
   ```

5. **Push to GitHub:**
   ```powershell
   git push origin main
   ```

### Step 2: Enable GitHub Pages

1. **Go to your GitHub repository:**
   - Open your browser and navigate to: `https://github.com/Bhaskararao-G/lgis-portfolio`

2. **Access Repository Settings:**
   - Click on the **Settings** tab (top menu)

3. **Configure GitHub Pages:**
   - In the left sidebar, scroll down to find **Pages** under "Code and automation"
   - Click on **Pages**

4. **Set the Source:**
   - Under **Build and deployment** section
   - For **Source**, select **GitHub Actions** from the dropdown
   - (Don't select "Deploy from a branch" - we want to use GitHub Actions)

5. **Save and Wait:**
   - The settings are saved automatically
   - GitHub will now use the workflow file we created

### Step 3: Verify Deployment

1. **Go to Actions Tab:**
   - Click on the **Actions** tab in your repository
   - You should see a workflow running called "Deploy to GitHub Pages"

2. **Monitor the Deployment:**
   - Click on the workflow run to see progress
   - Wait for all steps to complete (usually 1-2 minutes)
   - Look for a green checkmark indicating success

3. **Access Your Website:**
   - Once deployment is complete, go back to **Settings > Pages**
   - You'll see: "Your site is live at https://bhaskararao-g.github.io/lgis-portfolio/"
   - Click the link or visit the URL directly

### Step 4: Future Updates (Auto-Deployment)

From now on, every time you push to the `main` branch, your site will automatically redeploy!

**Workflow:**

1. **Make changes locally** (on develop branch):
   ```powershell
   git checkout develop
   # Make your changes to files
   git add .
   git commit -m "Your update message"
   git push origin develop
   ```

2. **Merge to main when ready to deploy:**
   ```powershell
   git checkout main
   git merge develop
   git push origin main
   ```

3. **Automatic deployment happens:**
   - GitHub Actions detects the push to main
   - Runs the deployment workflow
   - Updates your live website
   - No manual intervention needed!

## 🔧 Troubleshooting

### Issue: Workflow doesn't run
- **Solution:** Check that the workflow file is in `.github/workflows/deploy.yml`
- Make sure you pushed to the `main` branch

### Issue: Deployment fails
- **Solution:** Go to Actions tab and check the error logs
- Common issue: Permissions not set correctly
- Fix: Go to Settings > Actions > General > Workflow permissions
- Select "Read and write permissions"
- Click Save

### Issue: 404 Error when visiting site
- **Solution:** 
  - Ensure GitHub Pages is enabled in Settings
  - Verify the source is set to "GitHub Actions"
  - Check that index.html is in the root directory
  - Wait a few minutes after first deployment

### Issue: CSS not loading
- **Solution:**
  - Verify `styles.css` is in the same directory as `index.html`
  - Check the link tag in HTML: `<link rel="stylesheet" href="styles.css">`
  - Clear browser cache and reload

## 📝 Quick Reference Commands

```powershell
# Switch to main branch
git checkout main

# Pull latest changes
git pull origin main

# Merge develop into main
git merge develop

# Push to trigger deployment
git push origin main

# Check git status
git status

# View commit history
git log --oneline
```

## 🎯 Best Practices

1. **Always develop on the `develop` branch**
2. **Only merge to `main` when you want to deploy**
3. **Test your changes locally before merging to main**
4. **Write clear commit messages**
5. **Check the Actions tab after pushing to ensure deployment succeeds**

## 🌐 Your Live URL

After successful deployment, your website will be available at:

**https://bhaskararao-g.github.io/lgis-portfolio/**

---

**Note:** The first deployment may take a few minutes. Subsequent deployments are usually faster (1-2 minutes).
