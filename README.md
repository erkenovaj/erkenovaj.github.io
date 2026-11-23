# Jamilya Erkenova — personal site

A minimal, dependency-free personal site that doubles as a CV.
Plain HTML + CSS: no frameworks, no webfonts, no build step.
`Ctrl+P` / the "Download CV (PDF)" button produces a clean printable CV from the same file.

## Files

- `index.html` — all content, grouped by section with comments in mind: About → Research → Projects → Teaching → Experience → Training → Organizing → Writing.
- `style.css` — design system + a `@media print` block that turns the page into a CV.

## Deploy to GitHub Pages (user site)

1. Create a new public repo named **`erkenovaj.github.io`** (this exact name — it makes the site available at that address).
2. Copy `index.html` and `style.css` into the repo root and push:
   ```
   git init
   git add .
   git commit -m "personal site"
   git branch -M main
   git remote add origin https://github.com/erkenovaj/erkenovaj.github.io.git
   git push -u origin main
   ```
3. GitHub Pages is enabled automatically for `username.github.io` repos. Wait ~1 minute, then check https://erkenovaj.github.io

## Custom domain (optional, ~$11/year)

`jamilyaerkenova.com` was checked and appears unregistered (as of Nov 2026).

1. Buy the domain at Porkbun or Cloudflare Registrar (at-cost pricing).
2. In the repo, add a file named `CNAME` containing one line: `jamilyaerkenova.com`
3. At your registrar, set DNS records:
   - `A` records for the apex → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `erkenovaj.github.io`
4. Repo → Settings → Pages → check "Enforce HTTPS".

## Editing content

Everything is in `index.html`. Frequent edit points:

- **Header**: tagline, "Seeking" line, contacts.
- **Research → Evals & benchmarks**: the first item (`Yet Another Connections Benchmark`) has no link yet — add `<a href="…">` around the title when the preprint is public.
- **Teaching**: verify the org name for the "Compute Verification" course lead entry.
- **Footer**: change the `last updated` stamp whenever you push.

## Deliberate omissions

- No phone number, no documents, no personal identifiers beyond email.
- NSD internship (2022, 5 months) is intentionally left off the site — it stays in the PDF CV if needed.
- GFlowNets project removed per author's decision.
- Any under-review work (e.g. workshop submissions) should stay off the site until decisions, for review anonymity.
