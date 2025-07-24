# 🚀 HTML CI Pipeline using GitHub Actions

This project demonstrates a **basic Continuous Integration (CI) pipeline** for a simple HTML project using **GitHub Actions**. Every time code is pushed to the `main` or `production` branch, the pipeline validates the workflow by echoing messages and showing the current date—serving as a minimal, clear introduction to CI pipelines.

---

## 📁 Project Structure
html-ci-demo/
├── .github/
│ └── workflows/
│ └── html.yml
├── index.html
└── README.md

---

## ⚙️ GitHub Actions Workflow Overview

### 🔁 Trigger

This pipeline runs when code is pushed to:
- `main`
- `production`

```yaml
on:
  push:
    branches:
      - main
      - production

---
## 🛠 Jobs and Steps

jobs:
  run-basic-ci:
    name: Run Basic CI Check
    runs-on: ubuntu-latest

    steps:
      - name: 📥 Checkout Repository
        uses: actions/checkout@v3

      - name: 👋 Print Hello Message
        run: echo "✅ Hello from GitHub Actions - HTML CI Pipeline!"

      - name: 🕒 Print Current Date and Time
        run: date

      - name: 📄 List HTML Files
        run: ls -al *.html || echo "No HTML files found"


🎯 What I Learned

✅ Setting up a basic CI pipeline using GitHub Actions
✅ Understanding how workflows, jobs, and steps work
✅ Defining triggers based on Git events (push to branches)


🔮 Future Improvements

🔍 Add HTML validation using htmlhint
🚀 Deploy site to GitHub Pages or Netlify
🐳 Convert project into a Docker container and add Docker CI
🔔 Integrate Slack notifications for CI results
