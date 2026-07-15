# Day 7 — Week 1 Project + Review
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-06-Dicts-Tuples-Sets]] · **Next:** [[Day-08-Functions]]

**Time:** 90 min  
**Folder:** `~/python-practice/day07_project`

```bash
mkdir -p ~/python-practice/day07_project && cd ~/python-practice/day07_project
```

---

## Goal

Combine Days 1–6 into one real mini-app. No new big theory.

---

## Project options (pick ONE)

### Option A — Personal Expense Logger (recommended)

```bash
vim expense_logger.py
```

Features:
1. Menu loop
2. Add expense: description, amount, category
3. Store each expense as a dict inside a list
4. View all expenses
5. Show total spent
6. Show total by category
7. Quit

Example structure:
```python
expenses = [
    {"desc": "Coffee", "amount": 4.5, "category": "Food"},
    {"desc": "Bus", "amount": 3.0, "category": "Transport"},
]
```

### Option B — Quiz Game

- Store questions in a list of dicts
- Ask user each question
- Keep score
- Print final percentage

### Option C — Number Stats Tool

- Ask user for numbers until they type `done`
- Print count, sum, average, min, max
- Print even/odd counts

---

## Review checklist (self-test)

Without notes, can you explain:
- [ ] Variable vs type
- [ ] f-string
- [ ] if/elif/else
- [ ] for vs while
- [ ] list vs dict
- [ ] How to create/edit/run with vim + python3

---

## Stretch (optional)

- Save a “session summary” printout formatted nicely
- Add input validation (amount must be a number)
- Use `try/except` only if you already know it (else wait for Day 12)

---

## Reflection (write in vim)

```bash
vim week1_reflection.md
```

Answer:
1. What felt easy?
2. What was hardest?
3. One bug you fixed and how
4. Confidence score 1–10

---

## Checklist

- [ ] Project runs end-to-end from terminal
- [ ] At least 4 menu features work
- [ ] Reflection written
- [ ] Ready for functions week

**Next:** [[Day-08-Functions]]
