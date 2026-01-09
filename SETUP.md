# Setup Guide

Quick guide to deploy GMU Shuttle Tracker on GitHub.

## Method 1: GitHub Web Interface

1. Go to https://github.com/new
2. Repository name: `gmu-shuttle-tracker`
3. Description: `Real-time GMU shuttle tracking system`
4. Choose Public or Private
5. Click "Create repository"
6. Click "uploading an existing file"
7. Drag and drop all files from this folder
8. Commit changes

### Enable GitHub Pages

1. Go to repository Settings
2. Navigate to Pages section
3. Source: Deploy from a branch
4. Branch: `main` → `/ (root)`
5. Save

Your site will be live at: `https://YOUR_USERNAME.github.io/gmu-shuttle-tracker`

## Method 2: Git Command Line

```bash
cd /path/to/project/folder

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gmu-shuttle-tracker.git
git push -u origin main
```

Then enable GitHub Pages as described in Method 1.

## Method 3: GitHub Desktop

1. Download GitHub Desktop from https://desktop.github.com
2. File → New Repository
3. Name: `gmu-shuttle-tracker`
4. Choose location
5. Create Repository
6. Copy all files into the repository folder
7. Commit changes
8. Publish repository

Then enable GitHub Pages as described in Method 1.

## Update Repository Later

```bash
git add .
git commit -m "Update description"
git push
```

## Verify Deployment

Repository: `https://github.com/YOUR_USERNAME/gmu-shuttle-tracker`
Live Site: `https://YOUR_USERNAME.github.io/gmu-shuttle-tracker`

## Troubleshooting

**Permission denied**: Use Personal Access Token instead of password
1. GitHub → Settings → Developer settings → Personal access tokens
2. Generate new token with `repo` scope
3. Use token as password when pushing

**Pages not working**: Check Settings → Pages → ensure source is set correctly

**404 Error**: Wait a few minutes after enabling Pages for first deployment
