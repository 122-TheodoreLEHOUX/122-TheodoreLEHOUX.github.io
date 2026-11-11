# Theodore Lehoux — Portfolio

This is the source for my personal portfolio website. It is written in Markdown and built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/), then published to GitHub Pages.

The existing `pyproject.toml` and `uv.lock` are separate Python project configuration; the Pages workflow installs the website dependencies from `requirements.txt`.

## Project structure

```text
.
├── .github/workflows/pages.yml
├── docs/
│   └── index.md
├── environment.yml
├── mkdocs.yml
└── requirements.txt
```

## Preview locally

Install the requirements and start the MkDocs development server:

```powershell
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Open <http://127.0.0.1:8000> to preview the site. Alternatively, create the Conda environment from `environment.yml`:

```powershell
conda env create -f environment.yml
conda activate portfolio
python -m mkdocs serve
```

## Publish with GitHub Pages

The workflow in `.github/workflows/pages.yml` builds the site and deploys it whenever changes are pushed to `master`.

In the GitHub repository, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**.

For a personal site, the repository must be named `<your-github-username>.github.io`. This repository is configured for `122-TheodoreLEHOUX.github.io`, so its URL is <https://122-theodorelehoux.github.io/>.

## Customize

Edit `docs/index.md` to update the page. Site title, theme, navigation, and repository links are configured in `mkdocs.yml`.
