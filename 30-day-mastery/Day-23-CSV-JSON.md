# Day 23 — CSV & JSON
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-22-Pathlib-OS]] · **Next:** [[Day-24-APIs-Requests]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day23_csv_json`

```bash
mkdir -p ~/python-practice/day23_csv_json && cd ~/python-practice/day23_csv_json
```

---

## Topics

- `csv` module read/write
- `json` load/dump
- Dict rows
- When CSV vs JSON

---

## Create sample data

```bash
vim people.csv
```

```csv
name,age,city
Nitish,25,Canada
Alex,30,Toronto
Sam,22,Moncton
```

---

## Learn by typing

```bash
vim day23_demo.py
```

```python
import csv
import json
from pathlib import Path

# Read CSV
with open("people.csv", newline="", encoding="utf-8") as f:
    reader = csv.DictReader(f)
    people = list(reader)

for p in people:
    print(p["name"], p["age"], p["city"])

# Write CSV
with open("people_out.csv", "w", newline="", encoding="utf-8") as f:
    writer = csv.DictWriter(f, fieldnames=["name", "age", "city"])
    writer.writeheader()
    writer.writerows(people)

# JSON dump/load
with open("people.json", "w", encoding="utf-8") as f:
    json.dump(people, f, indent=2)

with open("people.json", encoding="utf-8") as f:
    data = json.load(f)

print(json.dumps(data, indent=2))
```

```bash
python3 day23_demo.py
cat people.json
```

---

## Practice questions

1. Read CSV and print only people age ≥ 25 (remember age is string → `int()`).
2. Add a new person and rewrite CSV.
3. Convert CSV → JSON file.
4. Convert JSON → CSV file.
5. Compute average age from CSV.
6. What does `newline=""` do in csv open on some systems?
7. Pretty-print JSON with `indent=2`.
8. Handle missing file with try/except.
9. Store a nested dict in JSON (e.g., user with list of skills).
10. When is JSON better than CSV?

---

## Mini task — `audit_summary.py`

Create `audits.csv`:
```csv
audit,location,pass,fail
5S,101,8,2
Crane,102,10,0
HSE,301,12,3
```

Script prints:
- total pass, total fail
- fail rate %
- writes `summary.json`

---

## Checklist

- [ ] DictReader / DictWriter used
- [ ] json.load / dump used
- [ ] Mini audit summary done

**Next:** [[Day-24-APIs-Requests]]
