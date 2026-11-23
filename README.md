# The Forge website

Single-page site for **The Forge**, the tabletop RPG zone run by the York Board Games Convention.

Live at **https://forge.ybgc.co.uk**

## How publishing works

The site is plain HTML and CSS, hosted on GitHub Pages from the **`live`** branch.
Anything committed and pushed to `live` goes live automatically, usually within a minute or two.

```
git add .
git commit -m "Describe your change"
git push origin live
```

## Files

| File | What it is |
| --- | --- |
| `index.html` | All the page content |
| `styles.css` | Colours, fonts and layout |
| `favicon.svg` | Browser tab icon |
| `CNAME` | Tells GitHub Pages to serve the site on forge.ybgc.co.uk. Don't delete it. |

## Brand palette

| Name | Hex |
| --- | --- |
| Charcoal | `#202326` |
| Ivory | `#F2F0E9` |
| Brass | `#B58A52` |
| Forge green | `#536B55` |

Headings use Oswald; body text uses EB Garamond (both from Google Fonts).

## Previewing locally

Open `index.html` in a browser, or run `npx http-server` in this folder and visit http://localhost:8080.
