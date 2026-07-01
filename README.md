# LeadRescue

AI-powered missed call recovery system for home service contractors.

## 🚀 Deploy to Vercel via GitHub

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) → click **New repository**
2. Name it `leadrescue` (or anything you like)
3. Set to **Public** or **Private** (both work with Vercel)
4. **Do NOT** tick "Add README" — leave it empty
5. Click **Create repository**

### Step 2 — Upload Files to GitHub

In your new empty repo click **"uploading an existing file"** (or use Git):

**Option A — Upload via browser (easiest):**
1. Click **"uploading an existing file"** link on the repo page
2. Drag & drop these three files:
   - `index.html`
   - `vercel.json`
   - `.gitignore`
3. Scroll down → click **Commit changes**

**Option B — Upload via Git CLI:**
```bash
git init
git add index.html vercel.json .gitignore README.md
git commit -m "Initial commit — LeadRescue website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/leadrescue.git
git push -u origin main
```

### Step 3 — Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) → click **Add New → Project**
2. Click **"Import Git Repository"**
3. Connect your GitHub account if not already connected
4. Select your `leadrescue` repo → click **Import**
5. On the configure page:
   - **Framework Preset:** `Other`
   - **Root Directory:** `./` (leave as default)
   - **Build & Output Settings:** leave all blank (static site, no build needed)
6. Click **Deploy**

✅ Vercel will give you a live URL like `leadrescue.vercel.app` in about 30 seconds.

### Step 4 — Connect a Custom Domain (Optional)

1. In Vercel dashboard → your project → **Settings → Domains**
2. Add your domain e.g. `leadrescue.com`
3. Vercel shows you the DNS records to add at your domain registrar
4. Add them → SSL is automatic (usually live within 5 minutes)

---

## 📁 File Structure

```
leadrescue/
├── index.html      ← The entire website (single file)
├── vercel.json     ← Vercel deployment + security headers config
├── .gitignore      ← Keeps junk files out of the repo
└── README.md       ← This file
```

## 🔒 Security Headers Applied via vercel.json

| Header | Purpose |
|--------|---------|
| `X-Frame-Options: DENY` | Blocks clickjacking |
| `X-Content-Type-Options: nosniff` | Blocks MIME-sniffing attacks |
| `Strict-Transport-Security` | Forces HTTPS always |
| `Content-Security-Policy` | Restricts what scripts/resources can load |
| `Referrer-Policy` | Controls referrer data sent to other sites |
| `Permissions-Policy` | Disables unused browser APIs (mic, camera, etc.) |

## 📬 Form Submissions

All demo booking and newsletter forms submit to Formspree (`xwvdqzvk`).
Log in at [formspree.io](https://formspree.io) to see all submissions.

---

Built with LeadRescue · AI-powered lead recovery for contractors
