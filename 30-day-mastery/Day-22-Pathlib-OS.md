# Day 22 — pathlib & OS Automation
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-21-Week3-Project]] · **Next:** [[Day-23-CSV-JSON]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day22_pathlib`

```bash
mkdir -p ~/python-practice/day22_pathlib && cd ~/python-practice/day22_pathlib
```

---

## Topics

- `pathlib.Path` (modern file paths)
- List files, create folders, check exists
- Rename / move basics
- Light `os` module
- Automating boring folder tasks

---

## Learn by typing

```bash
vim day22_demo.py
```

```python
from pathlib import Path
import os

cwd = Path.cwd()
print("cwd:", cwd)
print("home:", Path.home())

practice = Path.home() / "python-practice" / "day22_pathlib"
print(practice.exists())

# create folders
data_dir = practice / "data" / "raw"
data_dir.mkdir(parents=True, exist_ok=True)

# write a file with pathlib
sample = data_dir / "sample.txt"
sample.write_text("hello pathlib\n", encoding="utf-8")
print(sample.read_text(encoding="utf-8"))

# list files
for p in practice.rglob("*.txt"):
    print("found", p, "size", p.stat().st_size)

print("pid", os.getpid())
print("user", os.getenv("USER"))
```

```bash
python3 day22_demo.py
```

---

## Practice questions

1. Print your home directory with Path.
2. Create folder `reports/2026`.
3. Write `hello.txt` using `write_text`.
4. Read it back with `read_text`.
5. List all `.py` files under `~/python-practice` with `rglob`.
6. Check if a path `exists()` and `is_file()`.
7. Append a line to a file (read + write or open in append).
8. Count how many files are in a folder.
9. Build a path with `/` operator (not string `+`).
10. Name one automation idea useful at work (e.g., rename exports).

---

## Mini task — `organize_downloads_lite.py`

In a practice folder (NOT real Downloads yet):
1. Create `inbox/` with a few fake files: `a.txt`, `b.csv`, `c.txt`
2. Script moves `.txt` → `txt/`, `.csv` → `csv/`
3. Use `Path.rename` or `shutil.move`

```bash
mkdir -p inbox
touch inbox/a.txt inbox/b.csv inbox/c.txt
vim organize.py
python3 organize.py
ls txt csv
```

---

## Checklist

- [ ] Used Path for create/read/list
- [ ] Organizer script works on sample files

**Next:** [[Day-23-CSV-JSON]]
