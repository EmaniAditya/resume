# Meme Resume

This branch shows a 3-second meme + 2-second gag, then redirects to the resume.

## Setup
1. Replace `images/the_img.jpeg` with your meme image.
2. Update the resume URL in `index.html`.
3. Enable GitHub Pages (branch root).
4. Share `https://<user>.github.io/resume`.

Edit `index.html` to tweak timing or image.

---

## 🛠️ How It Works
1. **GitHub Pages** serves everything in this repository as a static website.
2. `index.html` runs a tiny JavaScript snippet that shows a meme, a message, and then immediately redirects the visitor to your resume URL.

---

## 📝 Detailed Setup
1. **Create a new repository** named whatever you like (`resume`, `cv`, or even the root repo `your-username.github.io`).
2. **Add an `index.html`** file that immediately redirects to your resume URL. You can use the one in this repo as a template.
3. **Push your code** to GitHub.
4. **Enable GitHub Pages**:  Repository ➜ Settings ➜ Pages ➜ "Deploy from a branch" (pick `main`, folder `/root`).
5. **Wait ~1 minute** for Pages to build, then visit `https://<your-username>.github.io/<repo>`.

---

## 🔄 Updating Your Resume
If you are hosting the resume on a different platform, you just need to update the URL in `index.html`.

---

## 💡 Tips & Tricks
* **Custom Domain:** Add a `CNAME` file or configure Pages DNS for a vanity URL (e.g., `resume.yourdomain.com`).
* **Analytics:** Drop in a simple script (e.g., Plausible) inside `index.html` before redirecting.

---

## 🙋‍♂️ Troubleshooting
| Symptom | Fix |
|---------|-----|
| 404 on PDF | Make sure the PDF URL in `index.html` is correct. |
| GitHub Pages not showing latest PDF | Wait ~1-2 min or clear browser cache; Pages uses a CDN. |
| Redirect loop | Ensure `index.html` doesn’t redirect to itself. |

---

## 📜 License
This guide is released under the MIT License. Feel free to copy, adapt, and share.

---

## ⭐️ Who Made This?
Maintained by **Aditya**.  
If this helped you, consider giving the repo a star! ⭐️