# Day 12 — Exceptions (try / except)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-11-File-IO]] · **Next:** [[Day-13-Comprehensions]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day12_exceptions`

```bash
mkdir -p ~/python-practice/day12_exceptions && cd ~/python-practice/day12_exceptions
```

---

## Topics

- `try`, `except`, `else`, `finally`
- Common errors: `ValueError`, `ZeroDivisionError`, `FileNotFoundError`, `TypeError`
- Raising errors with `raise`
- Don't bare-except everything silently

---

## Learn by typing

```bash
vim day12_demo.py
```

```python
# ValueError from bad int conversion
try:
    n = int(input("Enter a number: "))
    print(100 / n)
except ValueError:
    print("That was not a number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
else:
    print("All good, no errors.")
finally:
    print("This always runs.")

# File missing
try:
    with open("missing.txt") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found — create it first.")

# raise your own
def set_age(age):
    if age < 0:
        raise ValueError("age cannot be negative")
    return age

try:
    set_age(-3)
except ValueError as e:
    print("Error:", e)
```

---

## Practice questions

1. Safe divider: never crash on zero.
2. Keep asking for integer until valid.
3. Open user-provided filename; handle missing file.
4. Catch `TypeError` from `"2" + 2` (demo).
5. Function `sqrt_safe(n)` raises ValueError if n < 0.
6. Convert list of strings to ints; skip bad values with try/except.
7. Difference between `else` and `finally` in try block?
8. Write a tiny bank withdraw that raises error if amount > balance.
9. Log errors to `errors.log` when exception happens.
10. Why is `except:` (bare) usually a bad idea?

---

## Mini task — `safe_calc.py`

Calculator that never crashes:
- invalid numbers handled
- divide by zero handled
- loop until quit

---

## Checklist

- [ ] Handled ValueError and ZeroDivisionError
- [ ] Handled FileNotFoundError
- [ ] Used `raise` once
- [ ] Safe calculator done

**Next:** [[Day-13-Comprehensions]]
