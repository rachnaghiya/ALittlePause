# A Little Pause — rachnaghiya.com

Static site. No build step, no dependencies.

## Files

```
index.html                 the whole site
support.js                 runtime the page loads (keep next to index.html)
uploads/                   images
uploads/Visuals/           the work-grid artwork
```

Keep the folder structure exactly as is — the paths are relative.

## Publish with GitHub Pages

1. On github.com click **New repository**. Name it `alittlepause` (or anything), set it **Public**, create it.
2. On the empty repo page click **uploading an existing file**.
3. Drag in `index.html`, `support.js` and the whole `uploads` folder. Commit.
4. Go to **Settings → Pages**. Under *Build and deployment*, Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)**. Save.
5. Wait ~1 minute. Your site is live at `https://<your-username>.github.io/<repo-name>/`.

### Using your own domain (rachnaghiya.com)

In **Settings → Pages → Custom domain**, enter the domain and save. Then at your domain registrar add:

- four `A` records for the apex domain pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- or a `CNAME` record for `www` pointing to `<your-username>.github.io`

Tick **Enforce HTTPS** once the certificate is issued (can take up to an hour).

## Notes

- The contact form posts to Formspree (`https://formspree.io/f/xzezzleo`). The first real submission needs to be confirmed from your Formspree inbox.
- The blog section pulls your three latest Substack posts at page load through a public CORS proxy. If that service is ever down, two fallback titles show instead.
