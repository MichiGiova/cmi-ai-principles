# Vercel 404 Error Troubleshooting Guide

## Current Issue
Getting 404 NOT_FOUND error on Vercel deployment.

## Files in Repository
- ✅ `index.html` (main file)
- ✅ `CMI_25logo.svg` (logo)
- ✅ `package.json` (project config)
- ✅ `vercel.json` (deployment config)
- ✅ `README.md` (documentation)

## Possible Causes & Solutions

### 1. GitHub Repository Structure
**Problem**: Files might not be in the root directory of the GitHub repository.

**Check**: 
- Go to your GitHub repository
- Verify that `index.html` is directly in the root (not in a subfolder)
- The URL should be: `https://github.com/username/repo-name/index.html`

**Fix**: If files are in a subfolder, move them to the root directory.

### 2. Vercel Project Settings
**Problem**: Vercel might be looking in the wrong directory.

**Check**:
1. Go to Vercel Dashboard → Your Project → Settings
2. Check "Build & Development Settings"
3. Verify:
   - **Framework Preset**: "Other" or "Static Site"
   - **Root Directory**: `./` (root)
   - **Output Directory**: Leave empty or set to `./`
   - **Build Command**: Leave empty
   - **Install Command**: Leave empty

### 3. Vercel Build Configuration
**Problem**: Vercel might not be detecting the static site properly.

**Current vercel.json**:
```json
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}
```

**Alternative vercel.json** (try this if above doesn't work):
```json
{
  "version": 2,
  "builds": [
    {
      "src": "index.html",
      "use": "@vercel/static"
    }
  ]
}
```

### 4. Test with Simple File
**Problem**: Complex HTML might have issues.

**Test**: Try accessing `/test.html` on your Vercel URL to see if the simple test file works.

### 5. Force Redeploy
**Problem**: Vercel might be serving cached 404.

**Solution**:
1. Go to Vercel Dashboard
2. Click on your project
3. Go to "Deployments" tab
4. Click "Redeploy" on the latest deployment
5. Or trigger a new deployment by pushing a small change to GitHub

### 6. Check Vercel Logs
**Steps**:
1. Go to Vercel Dashboard → Your Project
2. Click on the latest deployment
3. Check "Function Logs" and "Build Logs" for errors

### 7. Manual Upload Test
**Test**: Try uploading the files directly through Vercel's dashboard instead of GitHub integration.

## Quick Fixes to Try

### Fix 1: Simplify vercel.json
Replace current vercel.json with:
```json
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}
```

### Fix 2: Remove vercel.json entirely
Delete vercel.json and let Vercel auto-detect the static site.

### Fix 3: Check GitHub repository
Ensure all files are in the root directory of your GitHub repository.

## Next Steps
1. Try accessing `/test.html` on your Vercel URL
2. Check Vercel project settings
3. Force redeploy
4. Check Vercel logs for specific errors

