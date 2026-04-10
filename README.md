# DAGA

**Make Nuclear Physics Great Again.**

Front page: `index.html`
Direct-reaction campaign page: `direct.html`

Landing page at [vibein.science](https://vibein.science).

## Deploy (GitHub Pages)

1. Create repo on GitHub, push this directory.
2. Repo → **Settings** → **Pages** → Source: `Deploy from a branch`, Branch: `main`, Folder: `/ (root)`.
3. (Custom domain) Add `vibein.science` in the Pages settings; this will auto-create a `CNAME` file. In your registrar DNS, add:
   - `A` records for apex `vibein.science` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - or `CNAME` `www` → `<username>.github.io`
4. Enable **Enforce HTTPS**.
