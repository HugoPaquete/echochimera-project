# Publishing this folder

This folder is ready to become a **public documentation-only GitHub
repository**. It contains no source code.

## 1. Create the repository

Create an empty public repository named:

```text
echochimera-project
```

Do not initialise it with source code.

## 2. Push only this folder

From this folder:

```bash
git init
git add .
git commit -m "ECHOCHIMERA public documentation v1.10.0"
git branch -M main
git remote add origin <repository-url>
git push -u origin main
```

## 3. Enable GitHub Pages

- Settings → Pages
- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`
- Enforce HTTPS

`_config.yml` uses the Minima theme. `index.md` is the landing page.

## 4. Repository settings

- description: “Public documentation for ECHOCHIMERA, an AI heautoscopy
  performance instrument”;
- topics:

```text
human-ai-performance
meta-listening
heautoscopy
generative-music
midi
constrained-agency
```

- social preview: `assets/gui/CONTACT_SHEET.png`;
- website: the Pages URL;
- enable two-factor authentication;
- protect `main` if collaborators are added.

## 5. Custom domain

If using a domain, create `CNAME` with the exact hostname:

```text
echochimera.example.org
```

Do not commit `CNAME` before the DNS record exists.

## 6. DOI

For the paper and documentation:

- deposit in Zenodo, OSF or the institutional repository;
- add the DOI to `CITATION.cff` and the paper page;
- keep the DOI version aligned with the public release.

The source and executable can remain private.

## 7. Never add

```text
*.py
_internal/
dist/
build/
backups/
runtime/
echochimera.json
*.zip executable
```

## 8. Verify before pushing

```bash
find . -name "*.py"
find . -type f -size +50M
```

Both should return nothing.

## 9. Link

Add the Pages URL to:

- ORCID;
- Ciência ID;
- personal website;
- institutional profile;
- CV;
- funding report.

## 10. FCT/CEEC

Before publishing, confirm with the funding office:

- open-access requirements for the paper;
- software/data deposit requirements;
- exact grant references;
- acknowledgement text.
