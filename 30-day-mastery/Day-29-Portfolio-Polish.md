# Day 29 — Portfolio Polish (README + Git)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-28-Mini-Project]] · **Next:** [[Day-30-Final-Project]]

**Time:** 60–90 min  
**Folder:** your Day 28 project

---

## Topics

- Good README structure
- `.gitignore` for Python
- Git basics: init, add, commit
- (Optional) GitHub repo
- Cleaning code for strangers

---

## 1) README template

```bash
cd ~/python-practice/projects/mini_tool
vim README.md
```

```markdown
# Project Title

## What it does
Short 2–3 lines.

## Why I built it
Learning goal / real use case.

## Features
- Feature 1
- Feature 2
- Feature 3

## Setup
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Run
```bash
python main.py
```

## Sample output
Paste a few lines of terminal output.

## What I learned
- ...
```

---

## 2) .gitignore

```bash
vim .gitignore
```

```text
.venv/
__pycache__/
*.pyc
.DS_Store
output/
*.png
.env
```

---

## 3) Git basics

```bash
git init
git status
git add .
git commit -m "Initial commit: working mini tool with README"
git log --oneline
```

### Optional GitHub

```bash
# if gh is installed and you want remote:
# gh repo create python-mini-tool --public --source=. --push
```

Only push if you want it public and there are **no secrets**.

---

## 4) Code polish checklist

- [ ] Clear file/function names
- [ ] No dead code
- [ ] Comments only where useful
- [ ] Consistent indentation
- [ ] One command to run
- [ ] Sample data included
- [ ] Errors handled

---

## Practice questions

1. What belongs in README vs comments in code?
2. Why ignore `.venv`?
3. Write a good 1-line commit message for a bugfix.
4. What is the difference between `git add` and `git commit`?
5. List 3 things recruiters look for in a project README.
6. Should screenshots/charts be in repo? When?
7. How do you reinstall packages from `requirements.txt`?
8. Clean one ugly function in your project today.
9. Add a "Future improvements" section.
10. Record a 60-second demo script (text) of your tool.

---

## Mini task

Polish Day 28 project to “showable” quality. If no GitHub, still have local git commits.

---

## Checklist

- [ ] Strong README
- [ ] .gitignore present
- [ ] At least 1 clean commit
- [ ] Project demo-ready

**Next:** [[Day-30-Final-Project]]
