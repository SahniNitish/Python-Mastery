# Day 28 — Mini Project Day (Build a Tool)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-27-Regex]] · **Next:** [[Day-29-Portfolio-Polish]]

**Time:** 90–150 min  
**Folder:** `~/python-practice/projects/mini_tool`

```bash
mkdir -p ~/python-practice/projects/mini_tool && cd ~/python-practice/projects/mini_tool
python3 -m venv .venv
source .venv/bin/activate
# install only what you need, e.g.:
# python -m pip install requests pandas matplotlib
```

---

## Goal

Ship **one useful tool** you can show on GitHub/LinkedIn. Prefer something related to your work/study.

---

## Project menu (pick ONE)

### A) Audit CSV Analyzer (IPC-flavored) ✅ recommended
- Input: CSV of audits (`audit,location,date,pass,fail`)
- Outputs:
  - summary stats in terminal
  - `summary.json`
  - bar chart of fails by audit type
- Skills: pandas + matplotlib + pathlib + argparse optional

### B) Expense Tracker CLI
- Add/list/summary
- Save to CSV/JSON
- Monthly totals

### C) API → CSV downloader
- Fetch public API data
- Normalize fields
- Save CSV + print top rows

### D) File Renamer Batch Tool
- Rename files in a folder with a pattern
- Dry-run mode first, then apply

---

## Definition of done

- [ ] Runs from terminal with clear instructions
- [ ] Handles bad input / missing file without crashing
- [ ] Has `README.md` with run steps
- [ ] Has sample data file
- [ ] You can explain every function in 30 seconds

---

## Suggested layout

```text
mini_tool/
├── .venv/
├── main.py
├── README.md
├── sample_data.csv
├── requirements.txt
└── output/
```

```bash
python -m pip freeze > requirements.txt
vim README.md
vim main.py
```

---

## Stretch

- Add `--help` with `argparse`
- Write 3 tests
- Add a second chart

---

## Checklist

- [ ] Tool finished
- [ ] Sample run works on fresh terminal session
- [ ] Ready to polish tomorrow

**Next:** [[Day-29-Portfolio-Polish]]
