# Contributing (Mountain Bear WV)

Gateway site for the Mountain Bear companies.  
Static HTML on Cloudflare Pages — **push to `main` → live in ~1 minute**.

## Repo map

| File | What it is |
|------|------------|
| `index.html` | Home / gateway copy and company links |
| `styles.css` | Look and feel (colors, layout) |
| `assets/` | Logo, favicon, background image |

## Safe edits

- Headlines, lede text, button labels  
- Links to Farms / Wood Products / YouTube  
- Footer year is automatic — no need to change it  

## Avoid unless you know HTML

- Deleting or mismatching `</div>`, `</section>`, tags  
- Renaming files (breaks links and deploys)  
- Replacing `styles.css` wholesale without a preview  

## How to edit (simplest)

1. Open the file on GitHub → **Edit** (pencil).  
2. Change text carefully; keep existing tags.  
3. **Commit** to `main` (or open a branch + Pull Request if you prefer review).  
4. Wait ~1 minute → check https://mountainbearwv.com (hard-refresh).

## Related sites

- Farms: `dkraft/mountainbearfarms` → https://mountainbearfarms.com  
- Wood: `dkraft/mountainbearwoodproducts` → https://mountainbearwoodproducts.com  

You only need **GitHub** access for content. Cloudflare/DNS is separate.
