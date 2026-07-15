# Day 21 — Week 3 Project (OOP)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-20-Debug-Test]] · **Next:** [[Day-22-Pathlib-OS]]

**Time:** 90–120 min  
**Folder:** `~/python-practice/day21_project`

```bash
mkdir -p ~/python-practice/day21_project && cd ~/python-practice/day21_project
python3 -m venv .venv
source .venv/bin/activate
```

---

## Project options (pick ONE)

### Option A — Inventory System (recommended)

Classes:
- `Product(name, price, quantity)`
- `Inventory` with methods: `add_product`, `remove_product`, `total_value`, `list_products`

CLI menu in `main.py`. Save/load optional (JSON on Day 23 if you want later).

### Option B — Library Manager

- `Book`, `Member`, `Library`
- borrow / return books
- track who has what

### Option C — Simple RPG

- `Character(name, hp, attack)`
- `Hero`, `Monster` subclasses
- battle loop until one HP ≤ 0

---

## Requirements (all options)

- [ ] At least 2 classes
- [ ] `__init__` + methods
- [ ] One inheritance OR composition relationship
- [ ] `__str__` on main objects
- [ ] Basic input validation
- [ ] Runs fully from terminal
- [ ] Optional: 3+ assert tests in `test_*.py`

---

## Suggested structure

```text
day21_project/
├── .venv/
├── main.py
├── models.py
├── test_models.py
└── README.md
```

```bash
vim README.md
```

Write:
- what it does
- how to run: `python main.py`
- features list

---

## Reflection

```bash
vim week3_reflection.md
```

1. Did classes make the code clearer?
2. What was confusing about `self` / inheritance?
3. Confidence with OOP 1–10

---

## Checklist

- [ ] Project complete and runnable
- [ ] README written
- [ ] Ready for data/tools week

**Next:** [[Day-22-Pathlib-OS]]
