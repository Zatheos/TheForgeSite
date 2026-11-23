# The Forge website

Single-page site for **The Forge**, the tabletop RPG zone run by the York Board Games Convention.

Live at **https://forge.ybgc.co.uk**

## How publishing works

The site is plain HTML and CSS on our Krystal hosting. A GitHub Action
([.github/workflows/deploy.yml](.github/workflows/deploy.yml)) copies the **`live`** branch to the
site's folder on the server over SFTP every time someone pushes to `live`. It usually takes under a minute.

```
git add .
git commit -m "Describe your change"
git push origin live
```

The deploy makes the server folder match the repo exactly, so files on the server that aren't in the
repo get deleted. It never deploys `.md` files, `.github/` or `.claude/`, and never touches `.htaccess`,
`.well-known/` or `cgi-bin/` on the server.

To check what a deploy would do without changing anything: **Actions → Deploy to forge.ybgc.co.uk →
Run workflow**, with "Dry run" ticked.

### Repository secrets

Under **Settings → Secrets and variables → Actions**:

| Secret | Value |
| --- | --- |
| `DEPLOY_PROTOCOL` | `sftp` |
| `DEPLOY_HOST` | Krystal server address |
| `DEPLOY_PORT` | `722` |
| `DEPLOY_USER` | cPanel username |
| `DEPLOY_PATH` | Full path to the forge.ybgc.co.uk folder |
| `DEPLOY_PASSWORD` | cPanel / SFTP password |

## Files

| File | What it is |
| --- | --- |
| `index.html` | All the page content |
| `styles.css` | Colours, fonts and layout |
| `favicon.svg` | Browser tab icon |

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
