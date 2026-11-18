# kithminrw.github.io

Source for my personal website, **[www.kithminrw.com](https://www.kithminrw.com/)**: about, education, experience, publications, research projects, skills, press, awards and news.

[![Deploy site to GitHub Pages](https://github.com/kithminrw/kithminrw.github.io/actions/workflows/pages.yml/badge.svg)](https://github.com/kithminrw/kithminrw.github.io/actions/workflows/pages.yml)

## Repository layout

| Path | What it is |
|---|---|
| `docs/` | **The live site.** Everything in this folder is published as-is. |
| `docs/index.html` | The single page that holds every section of the site. |
| `docs/img/`, `docs/images/`, `docs/skills/`, `docs/svg/` | Logos, photos and icons used on the page. |
| `docs/css/`, `docs/js/`, `docs/assets/`, `docs/fonts/` | Styles, scripts and vendor libraries. |
| `docs/CNAME` | Custom domain record (`www.kithminrw.com`). |
| `.github/workflows/pages.yml` | GitHub Actions workflow that deploys `docs/` to GitHub Pages. |
| `src/`, `scripts/`, `dist/`, `package.json`, `.travis.yml` | Left over from the original theme. Not used to build or deploy the site. |

## Editing the site

1. Edit `docs/index.html` (add images under `docs/img/` or `docs/images/`).
2. Preview locally:

   ```bash
   python3 -m http.server 8000 --directory docs
   ```

   then open <http://localhost:8000>.
3. Commit and push to `master`. The site updates within a minute or two.

## Deployment

The site is deployed by GitHub Actions, not from a branch:

- Every push to `master` runs the [Deploy site to GitHub Pages](.github/workflows/pages.yml) workflow, which uploads `docs/` unchanged (no build step, no Jekyll) and publishes it.
- The workflow can also be run manually from the **Actions** tab (`workflow_dispatch`).
- Repository **Settings → Pages → Source** must be set to **GitHub Actions**.
- The custom domain `www.kithminrw.com` and **Enforce HTTPS** are configured in **Settings → Pages**.

## Related sites

- [Open Photonics](https://www.kithminrw.com/silicon-photonics-lasers-tutorial/): a silicon photonics and lasers tutorial.
- [BRICD](https://www.thebricd.org/): Biomedical Research in IC Design, an open community designing biomedical ICs.
- [GitHub profile](https://github.com/kithminrw)

## Credits

The site started from the [Start Bootstrap Resume](https://startbootstrap.com/theme/resume) theme, which is MIT-licensed (see [LICENSE](LICENSE)).
