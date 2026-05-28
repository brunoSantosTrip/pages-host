@'
# pages-host

Internal hosting for HTML / JS / CSS microsites, published to GitHub Pages.

## How submissions work

1. Someone drops a file in Slack `#publish-internal`
2. Jarvis (Publisher bot) reviews the code, opens a PR against this repo
3. A human reviewer merges the PR
4. GitHub Actions deploys the new content to Pages
5. The file is live at `https://brunosantostrip.github.io/pages-host/apps/<submitter-slug>/<filename>`

## Layout

- `index.html` — landing page (you''re looking at the host)
- `apps/<submitter-slug>/<file>` — each submitter gets their own folder
- `.github/workflows/pages.yml` — the deploy workflow

Submissions are governed by the rules in the Jarvis Publisher persona — see `slackbot/personas/publisher/brain/persona.md` for what gets approved/rejected.
'@ | Out-File -FilePath README.md -Encoding utf8