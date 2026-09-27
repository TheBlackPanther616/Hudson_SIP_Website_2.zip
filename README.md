# Joseph Hudson Jr. — SIP / Boards Website (SIP311)

Static site: no build step, no framework. Six pages + one stylesheet.

## Publish on GitHub Pages (≈5 minutes)
1. Create a new **public** repo named `YOUR-GITHUB.github.io` (site at the root URL) — or any name, e.g. `sip-site` (site at `https://YOUR-GITHUB.github.io/sip-site/`).
2. Upload everything in this folder (drag-and-drop on github.com works, or `git add . && git commit -m "SIP site" && git push`).
3. Repo → **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. Wait ~1 minute; the URL appears at the top of the Pages settings. Paste it in the discussion post.

## Before you post — find-and-replace these placeholders
| Placeholder | Where | Replace with |
|---|---|---|
| `YOUR-GITHUB` | all pages (footer, SIP, Projects, Contact) | your GitHub username |
| `YOUR-LINKEDIN` | footer, Contact | your LinkedIn slug |
| `YOUR-CHANNEL` | footer, SIP | your YouTube handle |
| `YOUR-UAT-EMAIL@uat.edu` | Contact | your UAT email |
| `YOUR-FORM-ID` | contact.html | free Formspree endpoint (formspree.io → New form → copy the /f/xxxx id). Until then the form has no backend. |

Run once from this folder: `sed -i 's/YOUR-GITHUB/yourname/g; s/YOUR-LINKEDIN/yourslug/g' *.html`

## Images and documents to drop in
- `img/headshot.jpg` — then in index.html replace the headshot placeholder div with `<img class="headshot" src="img/headshot.jpg" alt="Joseph Hudson Jr.">`
- `img/` — logos, UML, mockup, n8n screenshot (names listed on each placeholder). Replace each `<div class="placeholder ...">` with `<img src="img/name.png" alt="...">`.
- `docs/Hudson_Module13_FinalProject_SRS.pdf`, `docs/Hudson_SIP311_Pitch.pdf`, `docs/Hudson_SIP_Brief.pdf` (the SIP Brief subpage embeds this automatically).

## Pages
index · sip (with #claim #description #architecture #prototype #visuals #code #brief #roadmap) · sip-brief · boards · projects · contact
