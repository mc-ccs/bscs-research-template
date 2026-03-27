# 📘 Research Documentation Template

This repository is a modular research-writing template built with:

- **Markdown** for writing and versioning content
- **MkDocs + Material** for local preview and web publishing
- **GitHub** for collaboration and progress tracking
- **GitHub Actions** for validation and deployment

The research manuscript is organized by chapter and section so teams can write, review, and revise content without working in one large document.

This repository is distributed to students through a GitHub Classroom assignment, so each student or group starts from an assigned repository before cloning it locally.

---

# 📁 Project Structure

All research manuscript content lives in the `docs/` directory.

```text
docs/
├── index.md
├── 01-front-matter/
│   ├── a-title-page.md
│   ├── b-abstract.md
│   ├── c-table-of-contents.md
│   ├── d-list-of-figures.md
│   └── e-list-of-tables.md
├── 02-chapter-1-introduction/
│   ├── a-project-context.md
│   ├── b-purpose-and-description.md
│   ├── c-objectives-rq-alignment.md
│   └── d-scope-and-mvp.md
├── 03-chapter-2-related-literature/
│   ├── a-domain-literature.md
│   ├── b-synthesis-matrix.md
│   └── c-technical-gap.md
├── 04-chapter-3-methods/
│   ├── a-institutional-framework.md
│   ├── b-product-backlog.md
│   ├── c-sprint-structure.md
│   ├── d-definition-of-done.md
│   ├── e-system-architecture.md
│   ├── f-logic-flow.md
│   └── g-validation-plan.md
├── 05-chapter-4-results/
│   ├── a-scrum-execution.md
│   ├── b-features-and-outputs.md
│   └── c-report-validation.md
├── 06-chapter-5-discussion/
│   ├── a-summary-of-key-findings.md
│   ├── b-rq3-validation-analysis.md
│   ├── c-limitations.md
│   └── d-recommendations.md
├── 07-appendices/
│   ├── a-cv/
│   │   ├── member1.md
│   │   └── member2.md
│   ├── b-topic-mine/
│   │   ├── member1.md
│   │   └── member2.md
│   ├── c-title-proposal-and-problem-statement-form.md
│   ├── d-comparative-summary.md
│   ├── e-gate-1-title-defense.md
│   ├── f-tech-stack.md
│   ├── g-sprint-0-retrospective.md
│   ├── h-sprint-0-review-and-sprint-1-planning.md
│   ├── i-gate-2-proposal-defense.md
│   ├── j-sprint-1-retrospective.md
│   ├── k-sprint-1-review-and-sprint-2-planning.md
│   ├── l-sprint-2-retrospective.md
│   ├── m-sprint-2-review-and-sprint-3-planning.md
│   ├── n-sprint-3-retrospective.md
│   ├── o-sprint-3-review-and-final-sprint-planning.md
│   ├── p-gate-3-pre-defense.md
│   ├── q-raw-seq-and-sus-data.md
│   ├── r-final-sprint-retrospective.md
│   ├── s-final-sprint-review.md
│   └── t-gate-4-final-defense.md
├── img/
└── src/
```

This structure keeps the research manuscript:

- Modular
- Easier to review
- Easier to maintain
- Ready for web publication

---

# 🚀 Getting Started

## 1. Accept and Clone Your Classroom Repository

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Before cloning, accept the GitHub Classroom assignment link provided by your instructor.

## 2. Install Requirements

```bash
pip install mkdocs mkdocs-material
```

## 3. Start Writing

Edit the Markdown files inside `docs/`.

Use these folders consistently:

- `docs/` for research chapters and appendices
- `docs/img/` for screenshots, diagrams, and figures
- `docs/src/` for source code, scripts, datasets, or supporting files

## 4. Preview Locally

```bash
mkdocs serve
```

Open `http://127.0.0.1:8000/` in your browser.

---

# ✍️ Suggested Writing Flow

1. Update the relevant section in `docs/`
2. Preview changes locally with `mkdocs serve`
3. Commit only related edits
4. Push your branch and open a pull request

Example commit flow:

```bash
git add .
git commit -m "docs: update chapter 1 objectives"
git push
```

---

# 🤝 Collaboration Workflow

## 1. Create a Working Branch

```bash
git checkout -b doc/<your-topic>
```

Examples:

- `doc/add-abstract`
- `doc/update-methods`
- `rev/fix-chapter-3-typos`

Branch roles:

- `doc/*` for regular writing and content updates
- `rev/*` for revisions and corrections
- `develop` for the latest integrated version deployed to UAT
- `release/<name>` for staging-ready versions
- `main` for approved production content

## 2. Write Clear Commit Messages

```text
feat: add system architecture diagrams
fix: correct grammar in introduction
docs: update abstract and validation plan
```

## 3. Keep Pull Requests Focused

Do not combine unrelated changes in one pull request.

## 4. Open a Pull Request

For regular work, open the pull request against `develop`.

Promotion flow:

1. Merge `doc/*` or `rev/*` into `develop`
2. Create or update `release/<name>` from `develop`
3. Merge to `main` after final approval

## 5. Sync Before Starting New Work

If your repository tracks an upstream classroom or template repository:

```bash
git pull upstream develop
```

If not, sync from your default remote instead:

```bash
git pull origin develop
```

---

# 🌐 Deployment Overview

GitHub Actions automatically validates pull requests and deploys the MkDocs site when supported branches are updated.

Deployment targets:

- `main` deploys the production site from the root of `gh-pages`
- `develop` deploys the UAT site to `gh-pages/uat`
- `release/<name>` deploys a staging site to `gh-pages/<name>`

Examples:

- `release/sprint-0` deploys to `gh-pages/sprint-0`
- `release/final-demo` deploys to `gh-pages/final-demo`

Pull requests to `main` and `develop` are validated before merge. Pushes to `main`, `develop`, and `release/*` trigger deployment.

## One-Time GitHub Pages Setup

After the first deployment:

1. Go to **Settings**
2. Open **Pages**
3. Under **Build and deployment**:
   - Set **Source** to `Deploy from a branch`
   - Set **Branch** to `gh-pages`
   - Set **Folder** to `/ (root)`
4. Save the settings

Published URLs follow this pattern:

```text
Production: https://<username>.github.io/<repository-name>/
UAT:        https://<username>.github.io/<repository-name>/uat/
Staging:    https://<username>.github.io/<repository-name>/<release-name>/
```

---

# 🔄 Student Workflow Diagram

```mermaid
flowchart TD
    A[Accept GitHub Classroom Assignment] --> B[Clone Repository]
    B --> C[Create Working Branch]
    C --> D[Edit Research Files in docs/]
    D --> E[Preview with MkDocs]
    E --> F[Commit and Push Changes]
    F --> G[Open Pull Request to Develop]
    G --> H{Review and Validation}
    H -->|Approved| I[Merge to Develop]
    I --> J[Deploy UAT]
    J --> K[Create or Update Release Branch]
    K --> L[Deploy Staging]
    L --> M{Approved for Production?}
    M -->|Yes| N[Merge to Main]
    N --> O[Deploy Production]
```

---

# ✅ Summary

This template gives you:

- A chapter-based research structure
- A clean Markdown authoring workflow
- Local preview with MkDocs
- Team collaboration through Git and pull requests
- Automated validation and GitHub Pages deployment
