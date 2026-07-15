# Day 3 — Conditionals (if / elif / else)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-02-Strings-Operators]] · **Next:** [[Day-04-Loops]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day03_conditionals`

```bash
mkdir -p ~/python-practice/day03_conditionals && cd ~/python-practice/day03_conditionals
```

---

## Topics

- `if`, `elif`, `else`
- Indentation (4 spaces)
- Nested conditions
- Truthiness (`""`, `0`, `None` are falsy)
- Ternary: `a if condition else b`

---

## Learn by typing

```bash
vim day03_demo.py
```

```python
score = int(input("Score (0-100): "))

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Grade: {grade}")

# Nested
age = int(input("Age: "))
if age >= 18:
    if age >= 65:
        print("Senior ticket")
    else:
        print("Adult ticket")
else:
    print("Child ticket")

# Ternary
n = 7
label = "even" if n % 2 == 0 else "odd"
print(n, "is", label)
```

---

## Practice questions

1. Even or odd checker.
2. Largest of three numbers (no `max()` — use if/elif).
3. Password check: if input equals `"python30"`, print Access Granted, else Denied.
4. Temperature: < 0 Freezing, 0–15 Cold, 16–25 Nice, > 25 Hot.
5. Leap year rule: divisible by 4, but not by 100 unless also by 400.
6. Simple calculator: ask two numbers and operator `+ - * /`.
7. Login: username `"admin"` AND password `"1234"`.
8. Fizz only: if number divisible by 3 print Fizz else the number.
9. Validate age is between 1 and 120 inclusive.
10. Rock-paper-scissors vs fixed computer choice `"rock"` (user inputs).

---

## Mini task — `grade_report.py`

Ask for 3 subject scores. Print average and overall Pass/Fail (pass if average ≥ 50). Print letter grade for average.

---

## Checklist

- [ ] Comfortable with indentation
- [ ] Used if/elif/else chains
- [ ] Nested if at least once
- [ ] Mini task done

**Next:** [[Day-04-Loops]]
