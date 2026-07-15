# Day 8 — Functions
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-07-Week1-Project]] · **Next:** [[Day-09-Args-Scope-Lambda]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day08_functions`

```bash
mkdir -p ~/python-practice/day08_functions && cd ~/python-practice/day08_functions
```

---

## Topics

- `def`, parameters, `return`
- Why functions exist (reuse, clarity)
- Docstrings
- Multiple returns (tuple unpacking)

---

## Learn by typing

```bash
vim day08_demo.py
```

```python
def greet(name):
    """Return a greeting string."""
    return f"Hello, {name}!"

def add(a, b):
    return a + b

def stats(numbers):
    total = sum(numbers)
    avg = total / len(numbers)
    return total, avg

print(greet("Nitish"))
print(add(3, 4))

t, a = stats([10, 20, 30])
print("total", t, "avg", a)

# function with no return → returns None
def log(msg):
    print("[LOG]", msg)

result = log("started")
print(result)  # None
```

---

## Practice questions

1. Function `is_even(n)` → True/False.
2. Function `area_circle(r)` using `pi = 3.14159`.
3. Function `max_of_three(a,b,c)` without built-in `max`.
4. Function `count_vowels(text)`.
5. Function `celsius_to_fahrenheit(c)`.
6. Function that returns both min and max of a list.
7. Function `is_palindrome(s)` ignore spaces/case.
8. Function `factorial(n)` with loop.
9. Function `grade(score)` returns letter grade.
10. Write a function and call it 3 times with different inputs.

---

## Mini task — `calculator_fns.py`

Refactor a calculator using functions:
- `add`, `sub`, `mul`, `div`
- menu calls these functions
- division by zero returns a message string (no crash)

---

## Checklist

- [ ] Wrote functions with `return`
- [ ] Used a docstring
- [ ] Calculator uses functions

**Next:** [[Day-09-Args-Scope-Lambda]]
