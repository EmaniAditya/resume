# Host Your Resume on GitHub Pages

Easily share a **single, always-up-to-date link** (e.g. `https://<your-username>.github.io/resume`) that points to the latest version of your resume PDF.  
This repository shows one lightweight way to achieve that.

---

## 🤡 Meme Splash Version
This `real-resume` branch adds a playful intro: a full-screen meme shows for **3 seconds**, followed by a gag message for **2 seconds** before redirecting to `ESAadityaReddyResume.pdf`.

Swap `images/the_img.jpeg` or edit the timing/target in `index.html` to customize.

---

## 📄 What You Get
* A single link with a **3-second meme splash screen** (perfect ice-breaker).
* After the meme + 2-second message, visitors are automatically redirected.
* Zero infrastructure or ongoing costs – just GitHub Pages.
* Simple updates: replace the meme image or PDF and push.

---

## 🚀 Quick Start (Copy-Paste Version)
```bash
# 1. Fork or clone this repo (or create a new repo named "resume")
# 2. Replace the existing PDF(s) with your own, keeping the same filename(s)
# 3. (Optional) Adjust index.html logic if you want multiple resume versions
# 4. Commit & push
# 5. In the repo settings ➜ Pages, turn on GitHub Pages (branch: main /root)
# 6. Share the link https://<your-username>.github.io/resume
```
That’s it – your resume is live! 💼

---

## 🛠️ How It Works
1. **GitHub Pages** serves this repo as a static site.
2. `index.html` first displays a full-screen meme image (`images/the_img.jpeg`) for **3 s**.
3. It then shows a short message (“Oh that was the real resume… here’s my wrong resume…”) for **2 s**.
4. Finally it redirects to the designated PDF (`ESAadityaReddyResume.pdf`).
5. Swap the image or change `pdfFile` in `index.html` to customize.

> _Legacy note_: The earlier multi-resume conditional logic was simplified in this branch.

---

## 📝 Detailed Setup
1. **Create a new repository** named whatever you like (`resume`, `cv`, or even the root repo `your-username.github.io`).
2. **Add your resume PDF** to the repo-root. Give it a short, stable filename (e.g., `Resume.pdf`).
3. **Add an `index.html`** file that immediately redirects to that PDF:
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <meta http-equiv="refresh" content="0; url=Resume.pdf" />
     </head>
   </html>
   ```
   This repo contains a more flexible version allowing multiple PDFs—use whichever suits your needs.
4. **Push your code** to GitHub.
5. **Enable GitHub Pages**:  Repository ➜ Settings ➜ Pages ➜ "Deploy from a branch" (pick `main`, folder `/root`).
6. **Wait ~1 minute** for Pages to build, then visit `https://<your-username>.github.io/<repo>`.

---

## 🔄 Updating Your Resume
1. Replace the old PDF with a new version (keep the filename).
2. `git add` → `git commit -m "chore: update resume"` → `git push`.
3. GitHub Pages will redeploy automatically – your link now serves the new PDF.

---

## 💡 Tips & Tricks
* **Custom Domain:** Add a `CNAME` file or configure Pages DNS for a vanity URL (e.g., `resume.yourdomain.com`).
* **Analytics:** Drop in a simple script (e.g., Plausible) inside `index.html` before redirecting.
* **Version Control:** Use branches or filenames (`Resume_2025.pdf`) if you need to keep historical copies.

---

## 🙋‍♂️ Troubleshooting
| Symptom | Fix |
|---------|-----|
| 404 on PDF | Make sure the PDF filename in `index.html` matches exactly (case-sensitive). |
| GitHub Pages not showing latest PDF | Wait ~1-2 min or clear browser cache; Pages uses a CDN. |
| Redirect loop | Ensure `index.html` doesn’t redirect to itself – path must point to the PDF. |

---

## 📜 License
This guide is released under the MIT License. Feel free to copy, adapt, and share.

---

## ⭐️ Who Made This?
Maintained by **Aditya**.  
If this helped you, consider giving the repo a star! ⭐️
