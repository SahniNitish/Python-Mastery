# Day 10 — Modules & Standard Library
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-09-Args-Scope-Lambda]] · **Next:** [[Day-11-File-IO]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day10_modules`

```bash
mkdir -p ~/python-practice/day10_modules && cd ~/python-practice/day10_modules
```

---

## Topics

- `import`, `from x import y`
- Your own module (`.py` file imported by another)
- Useful stdlib: `math`, `random`, `datetime`, `statistics`
- `if __name__ == "__main__"`

---

## Learn by typing

**File 1 — helper module**

```bash
vim utils.py
```

```python
def shout(text):
    return text.upper() + "!"

def average(nums):
    return sum(nums) / len(nums)

if __name__ == "__main__":
    print("utils.py run directly")
    print(shout("hello"))
```

**File 2 — main**

```bash
vim main.py
```

```python
import math
import random
from datetime import datetime, timedelta
from statistics import mean, median
import utils

print(math.sqrt(16))
print(math.pi)
print(random.randint(1, 10))
print(random.choice(["A", "B", "C"]))

now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M"))
print(now + timedelta(days=7))

data = [10, 20, 30, 40]
print(mean(data), median(data))
print(utils.shout("day 10"))
print(utils.average(data))
```

```bash
python3 main.py
python3 utils.py   # runs the __main__ block
```

---

## Practice questions

1. Import `math` and compute hypotenuse: `sqrt(a**2 + b**2)` (or `math.hypot`).
2. Simulate a dice roll 10 times.
3. Print today's date in `DD-MM-YYYY`.
4. Generate a random password of length 8 from letters+digits (`random.choice` + string).
5. Create `geometry.py` with `area_rect`, import it in another file.
6. What does `if __name__ == "__main__"` protect against?
7. Use `statistics.mean` on user-entered numbers.
8. Shuffle a list of names and print order.
9. Calculate days until next New Year using `datetime`.
10. List 5 stdlib modules you might use at work.

---

## Mini task — `lucky_date.py`

Print:
- current date/time
- a random motivational quote from a list
- square root of a user number (math)

Split quote helper into `quotes.py`.

---

## Checklist

- [ ] Imported stdlib modules
- [ ] Created and imported your own module
- [ ] Used `__name__ == "__main__"`

**Next:** [[Day-11-File-IO]]
