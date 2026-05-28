# Khang Nguyen Personal Website

This repository hosts the personal website for Khang Nguyen at <https://khangnguyen275.github.io/>.

The site is intentionally simple for the starter version: plain HTML, CSS, and a small SVG asset. It deploys through GitHub Pages with GitHub Actions and does not require UCLA hosting credentials.

## Local Development

Open `index.html` directly in a browser, or serve the folder with any small static server.

Example:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000/>.

## Build And Test

There is no build step yet.

- Build command: none
- Test command: none
- Deploy output directory: repository root

Before publishing changes, open the site locally and check that navigation, links, and assets work.

## Deployment

Deployment uses the official GitHub Pages Actions flow:

- `.github/workflows/deploy.yml`
- `actions/configure-pages`
- `actions/upload-pages-artifact`
- `actions/deploy-pages`

The workflow runs on pushes to `main` and can also be started manually from the Actions tab.

## Manual GitHub Settings

In GitHub, open this repository and go to:

`Settings` -> `Pages`

Set:

- Source: `GitHub Actions`

If Actions are disabled for the repository, go to:

`Settings` -> `Actions` -> `General`

Confirm that Actions are allowed for this repository.

## Future Changes With Codex

Ask Codex for natural-language website edits, such as:

- "Update the About section with this bio."
- "Add a CV link."
- "Create a projects section for these three projects."
- "Make the homepage more academic and less minimal."

For future edits, Codex should:

1. Inspect the repository before editing.
2. Create a branch named `codex/<short-description>`.
3. Make the requested change.
4. Run the available checks or local preview.
5. Commit with a clear message.
6. Open a pull request.
7. Avoid merging unless explicitly asked.

## Credentials

Do not store passwords, tokens, UCLA Logon credentials, SSH passwords, or personal credentials in this repository.

This site should deploy using GitHub's built-in Pages workflow and `GITHUB_TOKEN`.
