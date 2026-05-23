# Personal academic website (Quarto + GitHub Pages)

A bilingual (English / 한국어) personal website scaffold for a Biblical Studies
scholar. Built with [Quarto](https://quarto.org) — free, open source, no server
or database. English lives at the root; Korean mirrors it under `ko/`.

## 1. One-time setup

1. **Install Quarto** (free): https://quarto.org/docs/get-started/
2. Put this folder in a GitHub repository.
   - For a user site, name the repo `yourusername.github.io`.
   - For a custom domain (e.g. `yourname.com`), any repo name works.

## 2. Preview locally

```bash
quarto preview
```

This opens the site in your browser and live-reloads as you edit.

## 3. Edit your content

Every page is a plain-text `.qmd` file you can edit (or ask Claude Code to edit):

| Page          | English          | Korean              |
|---------------|------------------|---------------------|
| Home          | `index.qmd`      | `ko/index.qmd`      |
| About         | `about.qmd`      | `ko/about.qmd`      |
| Publications  | `publications.qmd` | `ko/publications.qmd` |
| Presentations | `presentations.qmd` | `ko/presentations.qmd` |
| Blog          | `blog/index.qmd` | `ko/blog/index.qmd` |
| CV            | `cv.qmd`         | `ko/cv.qmd`         |
| Contact       | `contact.qmd`    | `ko/contact.qmd`    |

Replace every placeholder marked "Your Name", `yourusername`,
`you@example.com`, and so on. Site-wide settings (title, navbar, social links,
search) live in `_quarto.yml`. Fonts and colors live in `theme.scss`.

- **Profile photo:** replace `profile.jpg` with your own.
- **CV file:** drop your `cv.pdf` into the `files/` folder.

## 4. Add a blog post

Copy `blog/posts/2026-05-22-welcome/`, rename the folder (e.g.
`2026-06-01-my-topic`), and edit `index.qmd`. Do the same under
`ko/blog/posts/` for the Korean version.

## 5. Publish to GitHub Pages

Simplest, one command:

```bash
quarto publish gh-pages
```

Or automatic: the included `.github/workflows/publish.yml` rebuilds and deploys
every time you push to `main`. In the repo, go to **Settings → Pages** and set
the source to the `gh-pages` branch.

## Notes on the bilingual setup

- Content is fully mirrored: English at root, Korean under `ko/`.
- The navbar is shared site-wide, so it shows English labels with a "한국어"
  toggle. Each Korean page also has a small `English` link back at the top.
- **Upgrade path** for a fully localized navbar (Korean labels on Korean
  pages): use Quarto project profiles, or the `babelquarto` package
  (https://docs.ropensci.org/babelquarto/). This is optional and can wait.

## Optional polish

- Google Scholar / ORCID icons aren't in Quarto's default icon set. Add the
  `academicons` extension when you want them; GitHub, LinkedIn, and email work
  out of the box.
