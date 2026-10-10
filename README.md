# Psygen Landing Page

Landing site for **Psygen**, a CTF team from the Department of Applied Mathematics and Computation Sciences, PSG College of Technology.

Currently a static "Coming Soon" page (`index.html`). No build step required.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

### Option A — Vercel
1. Import this repo at [vercel.com/new](https://vercel.com/new).
2. Framework preset: **Other** (static site, no build command, output directory `.`).
3. After deploy, go to the Vercel project → **Settings → Domains** → add `psygen.in` and `www.psygen.in`.
4. Vercel will show the DNS records to add at your domain registrar:
   - `A` record for `psygen.in` → Vercel's IP (shown in dashboard), or
   - `CNAME` record for `www.psygen.in` → `cname.vercel-dns.com`

### Option B — GitHub Pages
1. Push this repo to GitHub.
2. Repo **Settings → Pages** → Source: deploy from `main` branch, root folder.
3. The committed `CNAME` file already points to `psygen.in`; GitHub Pages reads it automatically.
4. At your domain registrar, add:
   - `A` records for `psygen.in` pointing to GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www.psygen.in` → `<your-github-username>.github.io`
5. In repo Settings → Pages, enable **Enforce HTTPS** once DNS propagates.

Pick one of the two (not both) to avoid conflicting DNS records.
