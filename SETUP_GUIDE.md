# 🚀 How to Publish PhishShield on GitHub

Follow these steps to get your project live with a shareable GitHub Pages link.

---

## Step 1 — Create a GitHub Account
If you don't have one: [github.com/signup](https://github.com/signup)

---

## Step 2 — Create a New Repository

1. Go to [github.com/new](https://github.com/new)
2. Fill in:
   - **Repository name:** `phishshield`
   - **Description:** `AI-powered phishing awareness training platform`
   - **Visibility:** Public ✅ (required for free GitHub Pages)
   - ❌ Do NOT check "Add a README file" (we already have one)
3. Click **Create repository**

---

## Step 3 — Upload the Files

### Option A — Via GitHub Web (easiest)

1. On your new empty repo page, click **"uploading an existing file"**
2. Drag and drop ALL these files:
   ```
   index.html
   README.md
   LICENSE
   CONTRIBUTING.md
   .gitignore
   docs/SECURITY.md
   .github/workflows/deploy.yml
   ```
3. Scroll down, add commit message: `Initial commit — PhishShield v2.0`
4. Click **Commit changes**

### Option B — Via Git CLI

```bash
# In the folder containing all the files:
git init
git add .
git commit -m "Initial commit — PhishShield v2.0"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/phishshield.git
git push -u origin main
```

---

## Step 4 — Enable GitHub Pages

1. Go to your repo → **Settings** tab
2. Left sidebar → **Pages**
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Wait ~60 seconds, then your site is live at:
   ```
   https://YOUR-USERNAME.github.io/phishshield
   ```

---

## Step 5 — Add the Live Link to README

1. Open `README.md` in GitHub
2. Click the pencil ✏️ icon to edit
3. Replace `https://your-username.github.io/phishshield` with your actual URL
4. Commit the change

---

## Step 6 — Add Topics & Description (optional but recommended)

On your repo's main page:
1. Click the ⚙️ gear icon next to "About"
2. Add description: `AI-powered phishing awareness training platform`
3. Add website: `https://your-username.github.io/phishshield`
4. Add topics: `cybersecurity` `phishing` `security-awareness` `ai` `education` `javascript`
5. Click **Save changes**

---

## ✅ You're Done!

Your project will now show:
- ⭐ A professional README with badges
- 🌐 A live demo link
- 📄 MIT License
- 🤝 Contributing guide
- 🔒 Security policy
- ⚡ Auto-deploy on every push (via GitHub Actions)

Share your link: `https://YOUR-USERNAME.github.io/phishshield`

---

## Troubleshooting

**Site not loading?**
- Make sure the repo is **Public**
- Wait 2–3 minutes after enabling Pages
- Check the Actions tab for any deploy errors

**GitHub Actions failing?**
- Go to **Actions** tab → click the failed workflow → read the error
- Usually it's a permissions issue — go to Settings → Actions → General → set "Workflow permissions" to "Read and write"
