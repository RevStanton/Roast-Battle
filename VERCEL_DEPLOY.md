# 🚀 Vercel Deployment Guide

## Deploy Your Roast Battle Arena to Vercel in 10 Minutes!

Vercel is perfect for this app because it handles both the frontend AND the backend API calls.

---

## Prerequisites

1. **GitHub Account** - [Sign up here](https://github.com) if you don't have one
2. **Vercel Account** - [Sign up here](https://vercel.com) (use your GitHub account to sign in)
3. **Anthropic API Key** - [Get one here](https://console.anthropic.com/)

---

## Step 1: Get Your Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com/)
2. Sign up or log in
3. Navigate to **API Keys** in the dashboard
4. Click **Create Key**
5. Copy your API key (you'll need this in Step 4)
6. Note: You'll need to add credits to your Anthropic account to use the API

---

## Step 2: Push to GitHub

### Option A: Using GitHub Web Interface (Easiest)

1. Go to [github.com/new](https://github.com/new)
2. Create a new repository called `roast-battle-arena`
3. Make it **Public** or **Private** (both work with Vercel)
4. Don't initialize with README
5. Click **Create repository**
6. Click "uploading an existing file"
7. Upload ALL files from this folder:
   - index.html
   - vercel.json
   - .env.example
   - README.md
   - LICENSE
   - CONTRIBUTING.md
   - VERCEL_DEPLOY.md
   - api/generate-roast.js
8. Commit the files

### Option B: Using Git Command Line

```bash
# Navigate to the project folder
cd /path/to/roast-battle-arena

# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add your GitHub repo as remote (replace YOUR-USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/roast-battle-arena.git

# Push to GitHub
git branch -M main
git push -u origin main
```

---

## Step 3: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New Project**
3. Import your `roast-battle-arena` repository
4. Click **Import**
5. Vercel will auto-detect the settings - just click **Deploy**

**Don't worry if it fails!** We still need to add the API key.

---

## Step 4: Add Your API Key to Vercel

This is the crucial step!

1. In your Vercel project dashboard, go to **Settings**
2. Click **Environment Variables** in the left sidebar
3. Add a new variable:
   - **Key**: `ANTHROPIC_API_KEY`
   - **Value**: Your API key from Step 1
   - **Environment**: Select all (Production, Preview, Development)
4. Click **Save**
5. Go back to **Deployments** tab
6. Click the **three dots** on your latest deployment
7. Click **Redeploy** → **Redeploy**

---

## Step 5: Test Your App! 🎉

1. Once deployment completes (takes ~1 minute), click **Visit**
2. Your app is now live at: `https://your-project-name.vercel.app`
3. Test it:
   - Select 2 personas
   - Enter a battle topic
   - Click "Let The Battle Begin!"
   - Watch the AI-generated roasts!

---

## Custom Domain (Optional)

Want a custom domain like `roastbattle.com`?

1. Buy a domain from any registrar (Namecheap, Google Domains, etc.)
2. In Vercel project → **Settings** → **Domains**
3. Add your domain
4. Follow Vercel's DNS instructions
5. Done! Your app is now on your custom domain

---

## Troubleshooting

### "API key not configured" error
- Make sure you added `ANTHROPIC_API_KEY` in Vercel environment variables
- Make sure you **redeployed** after adding the key
- Check the key is correct in Anthropic console

### Roasts not generating
- Check your Anthropic account has credits
- Open browser console (F12) to see detailed errors
- Check Vercel function logs: Project → **Logs** tab

### Deployment failed
- Check all files uploaded correctly to GitHub
- Make sure `api/generate-roast.js` is in the `api` folder
- Verify `vercel.json` exists in root

### Rate limiting issues
- Anthropic has rate limits on API usage
- Consider adding a rate limiter if you get lots of traffic
- Check your usage in Anthropic console

---

## Monitoring Usage & Costs

1. **Anthropic Console**: Monitor API usage and costs at [console.anthropic.com](https://console.anthropic.com/)
2. **Vercel Analytics**: Free basic analytics in your Vercel dashboard
3. Set up billing alerts in Anthropic to avoid surprises

---

## Updating Your App

Made changes? Easy to update:

1. Edit files locally
2. Push to GitHub:
   ```bash
   git add .
   git commit -m "Updated personas"
   git push
   ```
3. Vercel automatically redeploys! ✨

---

## Production Checklist

Before sharing with the world:

- [ ] API key is set in Vercel environment variables
- [ ] Tested all personas generate roasts
- [ ] Checked mobile responsiveness
- [ ] Set up billing alerts in Anthropic
- [ ] Consider adding rate limiting for production
- [ ] Add Google Analytics (optional)
- [ ] Share on social media! 🎉

---

## Going Viral Tips

1. **Share on Social Media**
   - Post funny roast examples
   - Use hashtags: #AIRoastBattle #AI #Funny
   - Tag tech/AI influencers

2. **Add Social Sharing**
   - Let users share their favorite roasts
   - Screenshot functionality for Instagram/Twitter

3. **Track Analytics**
   - See which personas are most popular
   - Track engagement
   - A/B test different features

4. **Iterate Based on Feedback**
   - Add user-requested personas
   - Improve roast quality
   - Add new features

---

## Need Help?

- **Vercel Docs**: [vercel.com/docs](https://vercel.com/docs)
- **Anthropic Docs**: [docs.anthropic.com](https://docs.anthropic.com)
- **Open an Issue**: On your GitHub repo

---

## Cost Estimates

**Vercel**: Free tier is generous
- Unlimited deployments
- 100GB bandwidth/month
- Serverless function executions included

**Anthropic API**:
- Claude Sonnet 4: ~$3 per million input tokens
- Each roast battle uses ~500-1000 tokens total
- Estimate: ~$0.003 per battle
- 1000 battles = ~$3

**Bottom line**: Very affordable to start! Set billing alerts to be safe.

---

Good luck making this go viral! 🔥🚀
