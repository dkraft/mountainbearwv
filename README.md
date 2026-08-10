# mountainbearwv.com

Static gateway site for **Mountain Bear WV** — landing page pointing to:

- [mountainbearfarms.com](https://mountainbearfarms.com)
- [mountainbearwoodproducts.com](https://mountainbearwoodproducts.com)
- YouTube: [@MountainBearFarmsWV](https://www.youtube.com/@MountainBearFarmsWV)

## Stack

- Static HTML/CSS (no CMS, no server)
- Host: **Cloudflare Pages** (free)
- DNS: **Hover** (keep nameservers at Hover)

## Local preview

```bash
cd mountainbearwv
python3 -m http.server 8080
# open http://127.0.0.1:8080
```

## Deploy (Cloudflare Pages)

1. Create a free GitHub repo (e.g. `mountainbearwv`) and push this folder.
2. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** → connect the repo.
3. Build settings: **Framework preset** = None, **Build command** empty, **Output directory** = `/` (or leave root).
4. After deploy, note the `*.pages.dev` URL.
5. **Custom domains** → add `mountainbearwv.com` and `www.mountainbearwv.com`.
6. Cloudflare will show required DNS records — apply them at Hover (see below).

## Hover DNS (you apply; do not share password)

Keep Hover nameservers. In Hover → domain → **DNS**:

| Type  | Hostname | Value (from Cloudflare after you add the domain) |
|-------|----------|--------------------------------------------------|
| CNAME | `www`    | `<your-project>.pages.dev`                       |
| A / AAAA or CNAME | `@` (apex) | values Cloudflare lists for the root domain |

Also keep or set:

| Type | Hostname | Value |
|------|----------|--------|
| MX   | `@`      | keep Hover email if you use it |

After DNS propagates (often minutes, up to a few hours), HTTPS is automatic via Cloudflare.

## Hover access for collaborators

**Hover does not support inviting Grok (or a second person) as a DNS collaborator** on a normal personal account the way GitHub or Cloudflare does.

Safe options:

1. **Recommended:** You paste DNS records we provide (2 minutes). Never share your Hover password.
2. **Optional later:** Move DNS only to Cloudflare (change nameservers at Hover to Cloudflare’s). Then invite a team member on Cloudflare for DNS. Domain registration stays at Hover.
3. **Do not:** email/chat your Hover password or 2FA codes.

## Brand source

Logo and color direction from the public YouTube channel avatar:
https://www.youtube.com/@MountainBearFarmsWV
