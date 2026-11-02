# Development Branch Guide

## Purpose

The `development` branch is the shared integration branch for the Turtle Down Under sales email analysis project. It brings together reviewed work from the data analysis team before that work is released to `main`.

This guide defines the proposed team workflow. Branch protection, reviewers and automated checks must be configured separately in GitHub.

## Branch responsibilities

| Branch | Purpose |
| --- | --- |
| `main` | Stable, approved project releases. |
| `development` | Reviewed team contributions being integrated and validated. |

Normal flow: task issue → feature branch in a fork → PR to `development` → team review → merge → release PR to `main`.

## Project scope

The team imports email data, cleans and standardises records, matches related emails into conversations, validates grouping accuracy, and analyses sales and communication patterns. Reusable processing code belongs in `src/`; exploratory work belongs in `notebooks/`.

## Recommended folders

| Location | Contents |
| --- | --- |
| `.github/` | Task issue templates, PR template and automated workflows. |
| `config/` | Example configuration without credentials. |
| `data/sample/` | Small synthetic or anonymised examples. |
| `notebooks/exploratory/` | Exploratory analysis notebooks. |
| `notebooks/validation/` | Analysis used to check matching and other results. |
| `src/sales_email_analysis/ingestion/` | Email JSON/CSV loading and parsing. |
| `src/sales_email_analysis/cleaning/` | Cleaning dates, subjects, senders and bodies. |
| `src/sales_email_analysis/matching/` | Email matching and conversation grouping. |
| `src/sales_email_analysis/analysis/` | Metrics and reusable analytical functions. |
| `sql/` | Database schemas and analysis queries. |
| `tests/` | Checks for processing behaviour and known edge cases. |
| `reports/figures/` | Approved, non-sensitive charts and report figures. |
| `docs/` | Methodology, data dictionary and task documentation. |

Root files should include `README.md`, `CONTRIBUTING.md`, `.gitignore` and a dependency definition such as `requirements.txt`.

Use folders according to the work's purpose rather than creating one folder per person. Git does not track empty folders; add a useful README, starter file or `.gitkeep` where needed.

## Before starting a task

1. Create or select an issue with an assigned owner.
2. Describe the problem, scope, expected output and acceptance criteria.
3. Agree on affected files and interfaces with teammates when work overlaps.
4. Fork the team repository once, if organisation permissions allow forking. Reuse that fork for later tasks.
5. Create a separate branch for each task from the latest upstream `development`.

## First-time contributor setup

Run these commands in the VS Code terminal. Replace `YOUR-USERNAME` with your GitHub username.

```powershell
git clone https://github.com/turtledownunder/sales-email-analysis
cd sales-email-analysis
git remote add upstream https://github.com/turtledownunder/sales-email-analysis.git
git remote -v
```

`origin` should point to your fork. `upstream` should point to the shared team repository. Private repository access and forking depend on organisation permissions.

## Start an assigned task

Make sure existing changes are committed or stashed before switching branches.

```powershell
git fetch upstream
git switch -c feature/12-email-cleaning upstream/development
```

Replace `12` with the issue number and `email-cleaning` with a short task description. This creates a new local task branch from the team's latest development work.

## Save and push changes

Place changes in the relevant project folders. Add comments explaining important assumptions or non-obvious decisions, update documentation, and validate the task against its acceptance criteria.

Review changes before staging:

```powershell
git status
git diff
```

Stage only the files belonging to the task. For example:

```powershell
git add src/sales_email_analysis/cleaning/ tests/
git diff --cached
git commit -m "Add email cleaning and validation"
git push -u origin feature/12-email-cleaning
```

Use actual changed paths in the staging command. Do not include unrelated edits or private data.

## Open a pull request

| PR setting | Value |
| --- | --- |
| Base repository | `turtledownunder/sales-email-analysis` |
| Base branch | `development` |
| Head repository | Your fork |
| Compare branch | Your task branch, such as `feature/12-email-cleaning` |

The PR description should include:

- Related issue number.
- Problem addressed and changes made.
- Validation performed and relevant results.
- Anonymised examples or screenshots when useful.
- Any limitations, assumptions or follow-up work.

Use a draft PR when work is still in progress. Keep each PR focused on one task.

## Team review and merge

A reviewer should check correctness, readability, folder placement, data handling and evidence that the acceptance criteria are met. For email matching, include examples of correct matches and unrelated conversations that remain separate.

Discuss questions in the PR, address requested changes, and push updates to the same task branch. A maintainer merges the PR after approval and successful required checks. Team members should not approve their own PRs.

Recommended branch protection for both `development` and `main`:

- Require a pull request before merging.
- Require at least one teammate's approval.
- Require review conversations to be resolved.
- Require configured automated checks to pass.
- Block force pushes and branch deletion.

These are intended repository settings, not settings applied by this document.

```

## Release to main

When a set of contributions has been integrated and validated, a maintainer opens a PR from the team repository's `development` branch to `main`. Include a summary of changes, validation and known limitations. Merge after the required release review.

```
### Auther Qasim Nasir