# Instructions For Codex Agents

This is Khang Nguyen's personal GitHub Pages website.

## Repository Shape

- Framework: plain static HTML/CSS/JS
- Package manager: none
- Build command: none
- Test command: none
- Deploy output directory: repository root
- Hosting: GitHub Pages through GitHub Actions

## Working Rules

1. Inspect the repository before editing.
2. Keep changes small and easy to review.
3. Use branches named `codex/<short-description>` for future work.
4. Run any available formatter, linter, test, or build before opening a PR.
5. If no automated checks exist, preview the static site and verify links/assets manually.
6. Commit with a clear message and open a pull request summarizing changes, validation, and deployment impact.
7. Do not merge unless Khang explicitly asks.

## Deployment Rules

Keep deployment on GitHub Pages unless Khang explicitly chooses another host.

The preferred workflow is `.github/workflows/deploy.yml` using:

- `actions/configure-pages`
- `actions/upload-pages-artifact`
- `actions/deploy-pages`

Use least-privilege workflow permissions:

- `contents: read`
- `pages: write`
- `id-token: write`

## Secret Safety

Never ask for passwords in chat.

Never commit:

- UCLA Logon credentials
- SSH passwords
- personal passwords
- GitHub tokens
- API keys
- `.env` files

If a future deployment path needs a secret, stop and explain why. Tell Khang the exact GitHub Settings page and exact secret name to create manually.
