# 🚀 HTML CI Pipeline using GitHub Actions

This project demonstrates a **basic Continuous Integration (CI) pipeline** for a simple HTML project using **GitHub Actions**. Every time code is pushed to the `main` or `production` branch, the pipeline validates the workflow by echoing messages and showing the current date—serving as a minimal, clear introduction to CI pipelines.

---

## 📁 Project Structure
html-ci-demo/
├── .github/
│ └── workflows/
│ └── hello-world.yml
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

## 🛠 Jobs and Steps

jobs:
  hello_word:
    runs-on: ubuntu-latest
    steps:
      - name: Print hello world
        run: echo "Hello world"

      - name: Print current date
        run: date

