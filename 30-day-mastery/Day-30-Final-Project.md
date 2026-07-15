# Day 30 — Final Project + Next Steps
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-29-Portfolio-Polish]]

**Time:** 2–3 hours (or split across a weekend)  
**Folder:** `~/python-practice/projects/final_project`

```bash
mkdir -p ~/python-practice/projects/final_project && cd ~/python-practice/projects/final_project
python3 -m venv .venv
source .venv/bin/activate
```

---

## Goal

Build your **capstone**: bigger than Day 28, combining multiple week skills.

You should use **at least 5** of these:
- functions
- files or CSV/JSON
- exceptions
- classes (optional but strong)
- venv + requirements
- pandas and/or matplotlib
- regex or API
- README + git

---

## Capstone ideas

### 1) IPC Audit Compliance Mini Dashboard (CLI)
- Load audit CSVs
- Clean columns
- Compute pass rates by audit/location/week
- Export Excel/CSV summary (pandas `to_csv`)
- Save charts
- Perfect story for your work experience

### 2) Personal Finance Analyzer
- Import bank CSV
- Categorize with keywords/regex
- Monthly spend charts
- Top merchants

### 3) Job Application Tracker
- Add jobs (company, role, status, date)
- Store JSON/CSV
- Stats: applied/interview/offer counts
- Chart of weekly applications

### 4) Study Habit Analytics
- Log daily minutes per topic
- Streak calculation
- Charts + weekly report text file

### 5) API Data Pipeline
- Fetch → transform → save CSV → summary stats → chart

---

## Delivery checklist

- [ ] `README.md` with setup/run/sample
- [ ] `requirements.txt`
- [ ] `.gitignore`
- [ ] Sample data
- [ ] `main.py` entrypoint
- [ ] No crash on common bad inputs
- [ ] At least one chart OR structured summary output
- [ ] You can demo in under 3 minutes

---

## Final self-exam (no notes)

Explain out loud / write answers:

1. How do you create and run a Python file in terminal with vim?
2. List vs dict — when each?
3. What does `return` do in a function?
4. Why use `with open(...)`?
5. What is a virtual environment?
6. What is a DataFrame?
7. What is an API in plain English?
8. What is OOP inheritance?
9. How do you read a traceback?
10. What project did you build and what problem does it solve?

---

## 30-day graduation

```bash
vim GRADUATION.md
```

Write:
- Before vs after skills
- Best project link/path
- Top 3 bugs you conquered
- Next 30-day goal (DSA? SQL+Python? automation at work?)

---

## After Day 30 — recommended paths

| Path | Focus next |
|------|------------|
| **Data Analyst** | More pandas, SQL, Power BI + Python |
| **Automation** | pathlib, schedules, Excel (`openpyxl`), email |
| **Backend** | Flask/FastAPI, databases |
| **Interviews** | DSA practice + [[python-50-question-easy]] harder sets |
| **Work impact** | Automate one IPC/report task end-to-end |

Related vault notes:
- [[Python_Roadmap]]
- [[PythonProjects]]
- [[Python_Foundations_Checklist]]
- [[python-50-question-easy]]
- [[Data_Analysis]]

---

## Congrats

If you coded almost every day in the terminal, you did not just “watch Python” — you **built the habit**.

Keep the loop forever:

```bash
vim something.py
python3 something.py
```

**Back to plan:** [[Python_30_Day_Mastery]]
