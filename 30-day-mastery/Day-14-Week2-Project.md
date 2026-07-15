# Day 14 — Week 2 Project
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-13-Comprehensions]] · **Next:** [[Day-15-Classes-Objects]]

**Time:** 90 min  
**Folder:** `~/python-practice/day14_project`

```bash
mkdir -p ~/python-practice/day14_project && cd ~/python-practice/day14_project
```

---

## Goal

Build a multi-file CLI app using functions, files, and exceptions.

---

## Project: Student Marks Manager (recommended)

**Files:**
- `main.py` — menu only
- `storage.py` — load/save
- `grades.py` — calculations

### Features
1. Add student (name, marks)
2. List all students
3. Average of all marks
4. Top student
5. Save to `students.txt` (or CSV-like lines: `name,marks`)
6. Load from file on start
7. Quit

### Suggested line format
```text
Nitish,88
Alex,92
```

### Skeleton ideas

```python
# storage.py
def load_students(path="students.txt"):
    ...

def save_students(students, path="students.txt"):
    ...

# grades.py
def average(students):
    ...

def top_student(students):
    ...
```

Handle:
- missing file on first run
- invalid marks input
- empty list cases

---

## Alternative projects

| Project | Skills used |
|---------|-------------|
| Password vault (local file) | functions, files, dicts |
| Habit tracker | append logs, stats |
| Flashcard quiz with save score | modules, files |

---

## Review self-test

- [ ] I can write a function with parameters and return
- [ ] I can import my own module
- [ ] I can read/write a text file
- [ ] I can catch ValueError / FileNotFoundError
- [ ] I can use a list comprehension

---

## Reflection

```bash
vim week2_reflection.md
```

What architecture choice was hardest (splitting files)? What will you reuse in Week 3?

---

## Checklist

- [ ] App runs via `python3 main.py`
- [ ] Data persists after quit/reopen
- [ ] Errors don't crash the program
- [ ] Reflection done

**Next:** [[Day-15-Classes-Objects]]
