# crasr.github.io

Source for the CRASR data science site, <https://crasr.github.io>. It's built with [Quarto](https://quarto.org) and published by GitHub Actions on every push to `main`.

## One-time setup

1. Create a **public** repo in the CRASR org named exactly `crasr.github.io` and push this folder to `main`.
2. In the repo, go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.
3. Push (or run the *Publish site* workflow by hand). The site goes live at https://crasr.github.io after a minute or two.
4. Point people to it: org **Settings → Profile → URL**, and a link in the `.github/profile/README.md` org profile.

## Add a project

1. Copy `projects/_template.qmd` to `projects/<short-name>.qmd`.
2. Fill in the front matter:
   - `description` is what shows on the card.
   - `categories` become the filter tags.
   - `featured: true` puts the project on the home page.
3. Optional: add a card image at `projects/img/<short-name>.png`, ideally about 16:10. A real figure or screenshot from the project works best.
4. Commit and push.

The thumbnails in `projects/img/` are decorative placeholders. Replace them with real figures when you have them.

## Preview locally

```bash
quarto preview
```

## Things to fill in

Search the repo for `TODO`. They mark repo links, the About text, team members, and contact details.

## Notes

- Project pages can describe private tools. Just don't link a private repo; write "Private, contact us" instead.
- If you add R code chunks to any page, run `quarto render` locally and commit `_freeze/`. That way the Action can publish without installing R and your packages.
- Custom domain: set it under Settings → Pages. With Actions-based deploys you don't need a `CNAME` file.
