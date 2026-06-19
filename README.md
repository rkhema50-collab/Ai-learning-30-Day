# 🤖 30-Day AI Learning Dashboard

An interactive 30-day learning plan for **AI Prompt Engineering** and **AI Content Creation** — built as a standalone HTML dashboard that works in any browser, Power BI, or Google Looker Studio.

## 🚀 Live Demo

> After enabling GitHub Pages, your dashboard will be live at:
> `https://YOUR-USERNAME.github.io/ai-learning-dashboard`

---

## ✨ Features

- 📅 **30 structured days** of AI learning across 4 weeks
- 📚 **Curated course** for every single day (mostly free)
- ✅ **Interactive task checkboxes** — check off tasks as you complete them
- 🏆 **Progress tracking** — marks days complete, saves to browser
- 🔗 **Direct course links** — one click to open each resource
- 🌙 **Dark mode UI** — easy on the eyes for long study sessions
- 📱 **Responsive** — works on desktop, tablet, and mobile

---

## 📁 File Structure

```
ai-learning-dashboard/
├── index.html        ← Main dashboard (single file, no dependencies)
├── README.md         ← This file
└── data/
    └── courses.json  ← All 30 days of course data (reference)
```

---

## 🛠️ How to Deploy on GitHub Pages

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **"+"** icon → **"New repository"**
3. Name it: `ai-learning-dashboard`
4. Set to **Public**
5. Click **"Create repository"**

### Step 2 — Upload the files

1. On your new repo page, click **"uploading an existing file"**
2. Drag and drop ALL files from this folder:
   - `index.html`
   - `README.md`
   - `data/courses.json`
3. Scroll down → click **"Commit changes"**

### Step 3 — Enable GitHub Pages

1. Go to your repo → click **"Settings"** (top menu)
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"** → select **"Deploy from a branch"**
4. Branch: **"main"** → Folder: **"/ (root)"**
5. Click **"Save"**
6. Wait 1–2 minutes → your site is live at:
   `https://YOUR-USERNAME.github.io/ai-learning-dashboard`

---

## 🔗 Embed in Google Looker Studio

1. Copy your GitHub Pages URL
2. Open [Looker Studio](https://lookerstudio.google.com)
3. Create a new report → **Insert → URL Embed**
4. Paste your URL → resize to fill the canvas
5. Done! Full interactivity preserved inside Looker Studio

---

## 📊 Embed in Power BI

1. Install **"HTML Content"** visual from AppSource (free)
2. Add the visual to your report
3. Create a measure pointing to your GitHub Pages URL
4. Or use the **Web Content** tile and paste the URL directly

---

## 🗂️ The 30-Day Plan at a Glance

| Week | Focus | Days |
|------|-------|------|
| Week 1 | **Foundations** — How AI works, first prompts, formats | 1–7 |
| Week 2 | **Advanced Prompting** — CoT, personas, templates | 8–14 |
| Week 3 | **AI Content Creation** — Blogs, social, video, images | 15–21 |
| Week 4 | **Mastery** — Workflows, tools ecosystem, real projects | 22–30 |

---

## 🔧 Customization

The dashboard is a single `index.html` file with no external dependencies (except Google Fonts). To customize:

- **Change courses**: Edit the `DAYS` array in the `<script>` section
- **Change colors**: Edit the CSS variables in `:root`
- **Add days**: Extend the `DAYS` array (update week index `w:` accordingly)
- **Change fonts**: Replace the Google Fonts import link

---

## 📄 License

Free to use for personal learning. Share it, fork it, adapt it.

---

*Built with ❤️ using Claude AI*
