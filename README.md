# Resend Quickstart Docs

A 3-page documentation site built with [Mintlify](https://mintlify.com) for the Documentation Assessment Course, Day 10.

## Pages

| Page | File | Description |
|---|---|---|
| Overview | `index.mdx` | Home page, site structure, quick reference table |
| Tutorial | `tutorial-resend.mdx` | Step-by-step guide to sending email with Resend in Node.js |
| API Reference | `api-reference.mdx` | Full reference for the Send Email endpoint |

## Local preview

Install the Mintlify CLI and run the local dev server:

```bash
npm install -g mintlify
mintlify dev
```

The site runs at `http://localhost:3000`.

## Deploy to Mintlify

1. Push this repository to GitHub.
2. Go to [dashboard.mintlify.com](https://dashboard.mintlify.com) and sign in.
3. Click **Add new project**.
4. Connect your GitHub account and select this repository.
5. Mintlify detects `mint.json` and deploys automatically.
6. Your live URL will be `https://your-project.mintlify.app`.

## Linting with Vale

This project uses [Vale](https://vale.sh) to lint documentation for hedging language and passive voice.

Install Vale and run it locally:

```bash
# Install Vale (macOS)
brew install vale

# Install Vale (Linux)
snap install vale

# Run the linter
vale *.mdx
```

Vale also runs automatically on every push and pull request via GitHub Actions (`.github/workflows/lint.yml`).

## Project structure

```
.
+-- mint.json               # Mintlify configuration
+-- index.mdx               # Home / overview page
+-- tutorial-resend.mdx     # Tutorial page
+-- api-reference.mdx       # API reference page
+-- .vale.ini               # Vale linter configuration
+-- .vale/
|   +-- styles/
|       +-- write-good/
|           +-- Hedging.yml       # Flags weak/hedging words
|           +-- PassiveVoice.yml  # Flags passive voice
+-- .github/
    +-- workflows/
        +-- lint.yml        # GitHub Actions Vale workflow
```
