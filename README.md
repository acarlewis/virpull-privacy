# VirPull Companion Privacy Policy

A static privacy policy website for the **VirPull Companion** browser extension.

- Plain HTML and CSS only. No JavaScript, frameworks, analytics or tracking.
- No build step: the files are served exactly as they are.
- Works on GitHub Pages and can also be opened locally by double-clicking `index.html`.

```
virpull-privacy/
├── index.html   # The privacy policy page
├── style.css    # Styles (responsive, supports light and dark mode)
└── README.md    # This file
```

---

## Before you publish

1. **Contact email:** open `index.html`, find `your-email@example.com` in the *Contact* section, and replace **both** occurrences (the `mailto:` link and the visible text) with your real email address.
2. **Last updated date:** if you change the policy, update the date near the top of `index.html`. Change both the `datetime="YYYY-MM-DD"` attribute and the visible text.

---

## Deploying with GitHub Pages

### 1. Create a GitHub repository

1. Sign in at [github.com](https://github.com).
2. Click the **+** icon in the top-right corner and choose **New repository**.
3. Enter a **Repository name**, for example `virpull-privacy`.
4. Set visibility to **Public**. GitHub Pages is free for public repositories. Private repositories need a paid GitHub plan to use Pages.
5. Leave **Add a README file** unchecked, because this project already has one.
6. Click **Create repository**.

### 2. Upload the files

**Option A: in the browser (no tools needed)**

1. On the new repository's page, click the **uploading an existing file** link. You can also use **Add file → Upload files**.
2. Drag `index.html`, `style.css` and `README.md` into the upload area.
   Upload the files themselves, not the folder that contains them. `index.html` must be at the top level of the repository.
3. Under **Commit changes**, keep **Commit directly to the `main` branch** selected.
4. Click **Commit changes**.

**Option B: with Git on the command line**

From inside the project folder, run the following. Replace `YOUR-USERNAME` with your GitHub username.

```bash
git init
git add index.html style.css README.md
git commit -m "Add VirPull Companion privacy policy"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/virpull-privacy.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. In the repository, click **Settings** (the tab at the top of the repository page).
2. In the left sidebar, under **Code and automation**, click **Pages**.
3. Under **Build and deployment → Source**, select **Deploy from a branch**.

### 4. Select the main branch and root folder

1. Under **Branch**, choose **`main`** from the first dropdown.
2. Choose **`/ (root)`** from the folder dropdown.
3. Click **Save**.

GitHub will now publish the site. The first deployment usually takes one to two minutes. To follow its progress, open the repository's **Actions** tab, where a workflow named *pages build and deployment* runs.

### 5. Find the public URL

1. Go back to **Settings → Pages**.
2. When deployment finishes, a message at the top says **"Your site is live at …"**, followed by the URL. There is also a **Visit site** button.
3. The URL follows this pattern:

   ```
   https://YOUR-USERNAME.github.io/virpull-privacy/
   ```

   For example, if your username is `octocat` and the repository is named `virpull-privacy`, the URL is
   `https://octocat.github.io/virpull-privacy/`.

Use this URL as the **privacy policy URL** in your browser extension store listing, such as the Chrome Web Store developer dashboard.

---

## Updating the policy later

Edit `index.html`, either directly on GitHub with the pencil icon or locally followed by a push, and commit the change to `main`. GitHub Pages redeploys automatically within a minute or two. Remember to update the **Last updated** date.

## Troubleshooting

- **404 page:** check that `index.html` is at the top level of the repository and not inside a subfolder, and that Pages is set to the `main` branch and the `/ (root)` folder. Wait a couple of minutes after saving, then refresh.
- **Page shows no styling:** check that `style.css` was uploaded to the same top-level folder as `index.html`. The filename is case-sensitive and must be all lowercase.
- **Old version still showing:** wait for the *pages build and deployment* run in the **Actions** tab to finish, then hard-refresh the page (Ctrl+F5, or Cmd+Shift+R on macOS).
