# Deploying Joe's Mows to Railway

## Quick Deployment Steps

### Option 1: Deploy from GitHub (Recommended)

1. **Create a GitHub Repository**
   ```bash
   cd ~/Documents/joes-mows-website
   git init
   git add .
   git commit -m "Initial commit - Joe's Mows website"
   ```

2. **Push to GitHub**
   - Create a new repository on GitHub (e.g., `joes-mows-website`)
   - Run:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/joes-mows-website.git
   git branch -M main
   git push -u origin main
   ```

3. **Deploy on Railway**
   - Go to [railway.app](https://railway.app)
   - Sign in with GitHub
   - Click "New Project" → "Deploy from GitHub repo"
   - Select your `joes-mows-website` repository
   - Railway will auto-detect and deploy!

### Option 2: Deploy with Railway CLI

1. **Install Railway CLI**
   ```bash
   npm i -g @railway/cli
   # or
   brew install railway
   ```

2. **Login and Deploy**
   ```bash
   cd ~/Documents/joes-mows-website
   railway login
   railway init
   railway up
   ```

## Configuration Files Included

- **`railway.toml`** - Railway-specific configuration
- **`nixpacks.toml`** - Build configuration for static hosting
- **`.gitignore`** - Files to exclude from deployment

## Custom Domain Setup

Once deployed, you can add a custom domain:

1. In Railway dashboard, go to your project
2. Click on "Settings" → "Domains"
3. Click "Generate Domain" for a free railway.app subdomain
4. Or add your custom domain (e.g., joesmows.com)

### Custom Domain DNS Settings

If using your own domain, add these DNS records:

**Option A: Using A Record**
- Type: `A`
- Name: `@` (or `www`)
- Value: Railway will provide the IP address

**Option B: Using CNAME (preferred)**
- Type: `CNAME`
- Name: `www`
- Value: Your Railway deployment URL

## Environment Variables

This is a static site with no environment variables needed. If you add backend functionality later, you can set them in Railway's dashboard under Settings → Variables.

## Automatic Deployments

Railway automatically redeploys when you push to your GitHub repository:

```bash
git add .
git commit -m "Update content"
git push
```

Changes will be live in ~2 minutes!

## Troubleshooting

### Site not loading
- Check Railway logs: `railway logs`
- Ensure port 8080 is used (configured in railway.toml)

### CSS/Images not loading
- Verify all file paths are relative (no absolute paths)
- Check that all files are committed to git

### Need to update content
1. Edit files locally
2. Test locally: `python -m http.server 8080`
3. Commit and push changes

## Local Testing

Before deploying, test locally:

```bash
python -m http.server 8080
# Visit http://localhost:8080
```

## Cost

Railway offers:
- **Hobby Plan**: $5/month for personal projects
- 500 hours of usage included
- Additional usage billed per hour

For a static website like this, the Hobby plan is more than sufficient.

## Support

If you need help:
- Railway Docs: https://docs.railway.app
- Railway Discord: https://discord.gg/railway
- Check Railway status: https://status.railway.app

---

**Your site will be live at:** `https://YOUR-PROJECT.railway.app`

After adding a custom domain: `https://joesmows.com`
