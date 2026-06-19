cp /mnt/user-data/outputs/register.html /home/claude/ai-learning-dashboard/register.html

cat > /home/claude/ai-learning-dashboard/README.md << 'EOF'
# 🤖 AI Learning Hub — 30-Day Program

A complete web app for learning AI Prompt Engineering and AI Content Creation.  
**Register page → Welcome onboarding → Interactive 30-day dashboard.**

## 📁 Files in this repo

| File | Purpose |
|------|---------|
| `register.html` | Landing page — Sign up / Log in + Welcome screen |
| `index.html` | The full 30-day interactive dashboard |
| `data/courses.json` | All 30 days of course data (reference) |
| `README.md` | This file |

---

## 🚀 Quick Deploy to GitHub Pages

### Step 1 — Create repo
1. Go to [github.com](https://github.com) → **"+"** → **New repository**
2. Name: `ai-learning-hub` · Visibility: **Public** · Click **Create**

### Step 2 — Upload all files
1. Click **"uploading an existing file"**
2. Upload: `register.html`, `index.html`, `README.md`, `data/courses.json`
3. Click **Commit changes**

### Step 3 — Enable GitHub Pages
1. **Settings** → **Pages** → Source: **Deploy from a branch**
2. Branch: **main** · Folder: **/ (root)** → **Save**
3. Live in ~2 min at: `https://YOUR-USERNAME.github.io/ai-learning-hub/register.html`

---

## 🔥 Connect Firebase (store user data in the cloud)

### Step 1 — Create Firebase project
1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Click **"Add project"** → name it `ai-learning-hub` → Create

### Step 2 — Enable Authentication
1. Left menu → **Authentication** → **Get started**
2. Enable **Email/Password** provider → Save
3. (Optional) Enable **Google** provider for one-click sign in

### Step 3 — Create Firestore database
1. Left menu → **Firestore Database** → **Create database**
2. Choose **Start in test mode** → Select your region → Done

### Step 4 — Get your config
1. Click the **gear icon** → **Project Settings**
2. Scroll to **"Your apps"** → click **"</> Web"** → Register app
3. Copy the `firebaseConfig` object

### Step 5 — Paste config into register.html
Open `register.html`, find this section and replace with your values:

```javascript
const firebaseConfig = {
  apiKey:            "YOUR_API_KEY",
  authDomain:        "YOUR_PROJECT_ID.firebaseapp.com",
  projectId:         "YOUR_PROJECT_ID",
  storageBucket:     "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId:             "YOUR_APP_ID"
};
```

---

## 🗄️ What gets stored in Firestore

Each user document is saved under `users/{uid}`:

```json
{
  "name":           "Alex Johnson",
  "email":          "alex@example.com",
  "createdAt":      "2026-06-19T...",
  "currentDay":     1,
  "completedDays":  [],
  "completedTasks": {}
}
```

---

## 🔗 Embed in Google Looker Studio

1. Deploy to GitHub Pages (above)
2. Copy your URL: `https://username.github.io/ai-learning-hub/register.html`
3. Looker Studio → **Insert → URL Embed** → paste URL → resize to canvas

---

## 💰 Firebase Free Tier

More than enough to get started:

- ✅ 10,000 authenticated users/month
- ✅ 1 GB Firestore storage
- ✅ 50,000 document reads/day
- ✅ 20,000 document writes/day
- ✅ Unlimited auth sign-ins

---

## 🗂️ The 30-Day Plan

| Week | Focus | Days |
|------|-------|------|
| Week 1 | **Foundations** | 1–7 |
| Week 2 | **Advanced Prompting** | 8–14 |
| Week 3 | **AI Content Creation** | 15–21 |
| Week 4 | **Mastery & Real Projects** | 22–30 |

---

*Built with Claude AI · Free to use and adapt*
EOF

cd /home/claude
zip -r ai-learning-hub-full.zip ai-learning-dashboard/
cp ai-learning-hub-full.zip /mnt/user-data/outputs/
echo "Done"
