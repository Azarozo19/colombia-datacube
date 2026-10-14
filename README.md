# datacube-colombia website

Static Spanish-language website for the Colombia FORCE datacube.

## Edit locally

The deployable website is in `dist/`:

- `dist/index.html` contains the page, styles, and browser interactions.
- `dist/assets/` contains the images.

Because the site has no build step, changes can be previewed with:

```bash
python -m http.server 8000 --directory dist
```

Then open `http://localhost:8000`.

## Publish for free with GitHub Pages

1. Create a public GitHub repository and push this repository's `main` branch.
2. Open the GitHub repository's **Settings → Pages**.
3. Under **Build and deployment**, select **GitHub Actions** as the source.
4. Open the **Actions** tab and run **Deploy website to GitHub Pages**, or push
   another commit to `main`.

The workflow in `.github/workflows/pages.yml` publishes `dist/` automatically.
The default URL is:

```text
https://GITHUB-USERNAME.github.io/REPOSITORY-NAME/
```

Invite collaborators from **Settings → Collaborators** so each maintainer can
edit through their own GitHub account. A purchased custom domain can be attached
later without changing the website source.

GitHub Pages is the sole hosting target for this repository. Pushes to `main`
publish the contents of `dist/` through the Pages workflow.
