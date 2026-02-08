# Proxiant AI Website

**The professionals behind your AI transition.**

## Deploy to GitHub Pages

### Step 1: Create a GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Name it `proxiant.ai` (or any name you prefer)
3. Set it to **Public** (required for free GitHub Pages)
4. Do NOT initialize with README (we already have one)

### Step 2: Push This Folder
```bash
cd proxiant-github-pages
git init
git add .
git commit -m "Initial Proxiant AI website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/proxiant.ai.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Click **Save**

### Step 4: Connect Custom Domain
1. In the same Pages settings, enter `proxiant.ai` under **Custom domain**
2. Click **Save**
3. Go to your domain registrar and add these DNS records:

**A Records (apex domain):**
| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**CNAME Record (www subdomain):**
| Type | Name | Value |
|------|------|-------|
| CNAME | www | YOUR_USERNAME.github.io |

4. Wait 15-60 minutes for DNS propagation
5. Back in GitHub Pages settings, check **Enforce HTTPS**

### Step 5: Verify Domain (Recommended)
1. Go to GitHub → **Settings** → **Pages** → **Add a domain**
2. Enter `proxiant.ai`
3. Add the TXT record GitHub provides to your DNS

## Site Structure
```
proxiant-github-pages/
├── index.html          # Main homepage
├── academy.html        # Proxiant Academy
├── solutions.html      # Proxiant Solutions
├── labs.html           # Proxiant Labs
├── CNAME               # Custom domain config
├── assets/
│   ├── logo.svg        # Full logo (light background)
│   ├── logo-dark.svg   # Full logo (dark background)
│   ├── logo-icon.svg   # Icon only
│   └── favicon.png     # 500x500 favicon/avatar
└── README.md           # This file
```
