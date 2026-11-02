# TDU email analysis – Suyash's oversight folder

## Roles & process
- Suyash (user) = observer/reviewer giving Oliver direction; Oliver = analyst; Abhishek = manager/approver; Haodong = export/data owner
- Planning phase until Abhishek approves the final plan – no analysis or deliverable changes before then
- Flow: plan with Oliver → ask Abhishek/Haodong only when input needed (via Suyash) → final draft to Abhishek → then execute

## Current state (9 Oct 2026)
- Step 1 = Excel contact list + written summary; dashboard + live refresh = Step 2
- Priorities: Q1, Q2, E1 → Q3, E3, E5 → E4; samples 30 emails/extraction, 20 reply pairs, 50 contacts
- Oliver works Mon/Wed/Thu (~8h/day; earlier "20h/week" unresolved); estimate 19h for Step 1
- Draft plan v0.2 due Mon 12 Oct 12:00, final draft end of day; Abhishek/Haodong answers requested by Mon 10:00

## Files
- `insights.md` – plan table "Where we are" (Date · Who · What · Status) + Parking lot; the record of deadlines (used by the stay-on-track skill). Keep it current.
- `decisions.md` – decisions log (E-rows); add new rows, never delete old ones.
- `tracker/`, `emails/`, `reports/` – drafts from the team-lead skill (tracker tasks/comments, emails and questions, milestone updates to Abhishek).
- Project skills in `.claude/skills/`: `plan-then-approve` (plan + approval before any change), `team-lead` (tasks, emails, reviews, updates), `stay-on-track` (deadlines, side jobs, status line).
- `Email Data-*/Email Data/CSV|JSON/` – 7,856 emails (1 Jul 2025–6 Oct 2026); CSV and JSON are the same emails, count once
- `Data_Analysis_Project_Plan_Completed.docx`, `project_kickoff_questions_Completed.txt` – Oliver's original plan v0.1
- `Re__Report_and_Questions/` – Oliver's Excel, findings summary, scope check; my Outlook email drafts (*.html)
- `Step1_Analysis_Scope_Check_Revised.docx` – Oliver's latest scope answers

## Data gotchas
- Lowercase sender domains before counting (SOTC.IN vs sotc.in gave 101 vs 159)
- Timestamp timezone unknown – no hour-of-day conclusions
- TDU staff domains: turtledownunder.com.au AND turtledownunder.co.nz; gmail.com is not an agency
- My quick text-search counts are rough; Oliver's extraction counts are the reference

## Environment (Windows)
- No Node.js – build .docx with python-docx, not docx-js
- Render .docx: Word COM `ExportAsFixedFormat(path, 17)` via PowerShell, then PyMuPDF (`fitz`) to PNG
- `PYTHONIOENCODING=utf-8 python ...` in Bash when printing document text (cp1252 errors otherwise)
- Read Word comments: parse `word/comments.xml`; map to anchored text via `commentRangeStart/End` in `document.xml`

## Working with Suyash
- Plain language, one issue at a time when asked, real examples from the data
- Email drafts as Outlook-pasteable HTML (inline styles, tables) or plain text; never send anything
- Use AskUserQuestion for decisions that are Suyash's; offer a recommended default
