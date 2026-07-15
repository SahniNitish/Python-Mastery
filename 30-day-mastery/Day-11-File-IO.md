# Day 11 — File Read / Write
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-10-Modules-Stdlib]] · **Next:** [[Day-12-Exceptions]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day11_files`

```bash
mkdir -p ~/python-practice/day11_files && cd ~/python-practice/day11_files
```

---

## Topics

- `open()`, modes `r`, `w`, `a`
- `with` context manager (always prefer)
- `read`, `readline`, `readlines`, `write`
- Path basics (relative paths)
- Difference: write overwrites, append adds

---

## Learn by typing

```bash
vim day11_demo.py
```

```python
# write (creates or overwrites)
with open("notes.txt", "w") as f:
    f.write("Line 1: Hello\n")
    f.write("Line 2: Python files\n")

# append
with open("notes.txt", "a") as f:
    f.write("Line 3: Appended\n")

# read all
with open("notes.txt", "r") as f:
    content = f.read()
print(content)

# read line by line
with open("notes.txt", "r") as f:
    for line in f:
        print(">", line.strip())
```

```bash
python3 day11_demo.py
cat notes.txt
```

---

## Practice questions

1. Write your name and 3 goals into `goals.txt`.
2. Read and print `goals.txt`.
3. Append today's date as a new line.
4. Count lines in a file.
5. Count words in a file.
6. Copy `notes.txt` to `notes_backup.txt` using Python.
7. Ask user for a todo item; append to `todos.txt`.
8. Read a file and print only lines containing the word `"Python"`.
9. Create `numbers.txt` with numbers 1–10 one per line; read and sum them.
10. Explain why `with open(...)` is safer than bare `open/close`.

---

## Mini task — `journal.py`

CLI daily journal:
1. Add entry (appends timestamp + text to `journal.txt`)
2. View all entries
3. Quit

```python
from datetime import datetime
# f"[{datetime.now()}] {text}\n"
```

---

## Checklist

- [ ] Wrote, appended, read files
- [ ] Always used `with open`
- [ ] Journal app works

**Next:** [[Day-12-Exceptions]]
