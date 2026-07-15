# Day 4 — Loops (for & while)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-03-Conditionals]] · **Next:** [[Day-05-Lists]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day04_loops`

```bash
mkdir -p ~/python-practice/day04_loops && cd ~/python-practice/day04_loops
```

---

## Topics

- `for` with `range()`
- Looping over strings/lists
- `while` loops
- `break`, `continue`
- Nested loops
- Accumulators (running total)

---

## Learn by typing

```bash
vim day04_demo.py
```

```python
# for + range
for i in range(5):          # 0..4
    print(i)

for i in range(1, 6):       # 1..5
    print(i)

for i in range(0, 10, 2):   # step 2
    print(i)

# loop over string
for ch in "Python":
    print(ch)

# while
n = 3
while n > 0:
    print("countdown", n)
    n -= 1

# break / continue
for i in range(10):
    if i == 3:
        continue   # skip 3
    if i == 7:
        break      # stop at 7
    print(i)

# accumulator
total = 0
for i in range(1, 6):
    total += i
print("sum 1..5 =", total)
```

---

## Practice questions

1. Print numbers 1 to 20.
2. Print multiplication table for a user number (1–10).
3. Sum of all even numbers from 1 to 100.
4. Factorial of N using a loop.
5. Reverse a string using a loop (no slicing).
6. Count vowels in a sentence.
7. Guessing game: secret number 7; keep asking until correct (`while`).
8. Print this pattern:
   ```
   *
   **
   ***
   ****
   ```
9. Find all divisors of a number.
10. Print Fibonacci sequence first N terms.

---

## Mini task — `menu_loop.py`

Show a menu forever until user chooses Quit:

```
1) Say hello
2) Add two numbers
3) Quit
```

Use `while True` + `break`.

---

## Checklist

- [ ] `for` and `while` both used
- [ ] Used `break` and `continue`
- [ ] Built accumulator sum
- [ ] Menu loop works

**Next:** [[Day-05-Lists]]
