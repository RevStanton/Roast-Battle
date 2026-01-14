# 🚀 Quick Setup Guide

## Get Your Roast Battle Arena Live in 5 Minutes!

### Step 1: Create a GitHub Account
If you don't have one already, go to [github.com](https://github.com) and sign up.

### Step 2: Create a New Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it: `roast-battle-arena` (or whatever you like!)
3. Keep it **Public** (required for free GitHub Pages)
4. **Don't** initialize with README (we already have one)
5. Click "Create repository"

### Step 3: Upload Your Files

You have two options:

#### Option A: Using the Web Interface (Easiest)
1. On your new repository page, click "uploading an existing file"
2. Drag and drop ALL files from the `roast-battle-arena` folder:
   - index.html
   - README.md
   - LICENSE
   - CONTRIBUTING.md
   - .gitignore
3. Click "Commit changes"

#### Option B: Using Git (If you're comfortable with terminal)
```bash
cd /path/to/roast-battle-arena
git remote add origin https://github.com/YOUR-USERNAME/roast-battle-arena.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. In your repository, click **Settings**
2. Scroll down to **Pages** (in the left sidebar)
3. Under "Source", select **main branch**
4. Click **Save**
5. Wait 1-2 minutes for deployment

### Step 5: Visit Your Live Site! 🎉

Your app will be live at:
```
https://YOUR-USERNAME.github.io/roast-battle-arena
```

## Customization After Setup

### Update Personas
Edit `index.html` and change the `personas` array

### Change Colors
Modify the CSS variables in the `:root` section

### Add Features
Check out CONTRIBUTING.md for ideas and guidelines

## Troubleshooting

**Site not loading?**
- Wait 2-3 minutes after enabling Pages
- Check that you selected the right branch in Settings → Pages
- Make sure the repository is Public

**Roasts not generating?**
- This app uses the Claude API which works in the Claude.ai environment
- For external hosting, you'll need to implement a backend proxy for API calls
- Consider using environment variables for API keys

**Want to add your own domain?**
- GitHub Pages supports custom domains!
- Go to Settings → Pages → Custom domain
- Follow GitHub's instructions

## Next Steps

- Share your app with friends
- Get feedback and iterate
- Add new personas
- Consider adding analytics to track usage
- Join the community and contribute back!

## Need Help?

- Check the main README.md for more details
- Open an issue on GitHub
- Read GitHub's [Pages documentation](https://docs.github.com/en/pages)

Happy battling! 🔥
