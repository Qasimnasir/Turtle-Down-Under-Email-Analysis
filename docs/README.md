# Project Documentation

This folder contains documentation for the Turtle Down Under sales email analysis project, including task guides, methodology, data definitions and instructions for using contributed work.

## Required documentation for every contribution

Anyone submitting scripts, notebooks, SQL queries, configuration, reports or other project work must include or update the relevant documentation in the same pull request.

**Every task document must state the exact repository-relative folder and file paths where the work can be accessed, with clickable relative links.** Include the main entry point and any supporting files needed to use the contribution. Update these links whenever files are moved or renamed.

For example, a document saved directly in `docs/` should link to a cleaning script like this:

```markdown
## Where to find this work

All paths below are relative to the repository root.

- Main script: [`src/sales_email_analysis/cleaning/clean_emails.py`](../src/sales_email_analysis/cleaning/clean_emails.py)
- Supporting tests: [`tests/test_clean_emails.py`](../tests/test_clean_emails.py)
```

These are illustrative paths. Replace them with files that exist in your contribution. Link destinations are relative to the document's location: use `../` from `docs/` to reach the repository root, or `../../` from a document one folder deeper.

## What to include

| Item | Required information |
| --- | --- |
| Task | Clear title, purpose and related issue number. |
| Work location | Exact repository-relative paths and clickable links to contributed files. |
| Setup | Dependencies, configuration and prerequisites. |
| Usage | Commands to run from the repository root, or steps to open and use the work. |
| Inputs | Expected formats, required fields and how authorised users obtain the data. |
| Outputs | Results produced and their destination paths. |
| Validation | Checks performed, relevant results and known limitations. |

If work is documentation-only, identify the document path and explain its purpose; mark execution-related fields as not applicable.

## Task documentation template

Create a descriptive file such as `docs/email_cleaning.md` and use the following template. Replace all placeholders before submitting.

````markdown
# <Task title>

## Purpose

<Explain the problem and what this contribution does.>

Related issue: #<issue-number>

## Where to find this work

Paths are relative to the repository root.

- Main file: [`<repository-relative-file-path>`](<relative-link-from-this-document>)
- Supporting files: <paths and links, or none>
- Validation files: <paths and links, or not applicable>

## Setup

<List dependencies and configuration. Do not include credentials.>

## How to use

Run from the repository root:

```powershell
<actual command>
```

<For notebooks or non-executable work, provide the appropriate opening or usage steps.>

## Inputs and outputs

- Inputs: <format, required fields and approved source>
- Outputs: <results and exact output folder/file paths>

## Validation and limitations

<Describe checks performed, results and known limitations.>
````

## Documentation index

When adding a task document, add a row below so teammates can discover it. Use links relative to this README and include the location of the related work.

| Document | Purpose | Related work location |
| --- | --- | --- |

## Before opening a pull request

- Include documentation alongside the related work in the same PR.
- Confirm every file path is accurate and every relative link resolves on the PR branch.
- Provide reproducible usage steps and document output locations.
- Add the task document to the index above.
- Exclude real customer emails, credentials and sensitive notebook outputs.
- Target the shared repository's `development` branch for normal task contributions.

Documentation should let another team member find, understand and use the work without asking the author where it is stored.
