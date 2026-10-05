# tyx8099.github.io

Personal portfolio site for **Tee Yu Xun** — Data Engineer / Analytics / Technical Product professional.

Built as a single-page static site (plain HTML/CSS/JS, no build step) so it deploys instantly via GitHub Pages.

## Structure

| File | Purpose |
|---|---|
| `index.html` | Page content — hero, about, experience, projects, skills/certifications, contact |
| `style.css` | Styling, including light/dark theme variables and responsive layout |
| `script.js` | Mobile nav toggle, dark-mode toggle (persisted via `localStorage`), footer year |

## Deploying to GitHub Pages

1. Create a GitHub repo named exactly `tyx8099.github.io` (if not already created).
2. Push this folder's contents to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/tyx8099/tyx8099.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → Deploy from a branch**, select `main` / `/ (root)`, save.
4. Site goes live at `https://tyx8099.github.io` within a minute or two.

## Customizing

- **Links**: Update the placeholder LinkedIn URL in `index.html` (search for `your-linkedin-handle`) and swap project GitHub links once those repos are public.
- **Content**: Experience, projects, skills, and certifications are pulled from `profile/master-profile.md` in the `hire-me-pls` repo — update both together if your profile changes.
- **Theme colors**: Adjust the CSS custom properties at the top of `style.css` (`:root` for light mode, `[data-theme="dark"]` for dark mode).
- **Custom domain**: Add a `CNAME` file containing your domain name to the repo root, then point your DNS at GitHub Pages.

## Local preview

Just open `index.html` directly in a browser, or serve it locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
