# Day 9 — Args, Scope & Lambda
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-08-Functions]] · **Next:** [[Day-10-Modules-Stdlib]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day09_args`

```bash
mkdir -p ~/python-practice/day09_args && cd ~/python-practice/day09_args
```

---

## Topics

- Default arguments
- Keyword arguments
- `*args`, `**kwargs`
- Local vs global scope
- `lambda` + `map`/`filter` (light)
- Avoid mutable default args

---

## Learn by typing

```bash
vim day09_demo.py
```

```python
def power(base, exp=2):
    return base ** exp

print(power(3))        # 9
print(power(2, 5))     # 32
print(power(exp=3, base=2))

def total(*nums):
    return sum(nums)

print(total(1, 2, 3, 4))

def profile(**info):
    for k, v in info.items():
        print(k, ":", v)

profile(name="Nitish", city="Canada")

# scope
x = 10
def demo():
    x = 99          # local
    print("inside", x)

demo()
print("outside", x)

# lambda
square = lambda n: n * n
print(square(6))

nums = [1, 2, 3, 4, 5]
print(list(map(lambda n: n * 2, nums)))
print(list(filter(lambda n: n % 2 == 0, nums)))
```

---

## Practice questions

1. Function with default city `"Toronto"`.
2. `average(*nums)` using `*args`.
3. `show_user(**kwargs)` prints all key-values.
4. Explain what happens if you assign to a variable name inside a function that also exists outside.
5. Write `apply_op(a, b, op)` where `op` is a function.
6. Sort list of tuples by second value using `lambda`.
7. Filter names longer than 4 characters with `filter` + lambda.
8. Why is `def f(items=[])` dangerous? Demo the bug.
9. Rewrite a tiny lambda as a normal `def` (same behavior).
10. Function that accepts required `name` and optional `title="Mr"`.

---

## Mini task — `report.py`

```python
def build_report(title, *lines, **meta):
    ...
```

Print title, each line, then metadata key-values.

---

## Checklist

- [ ] Defaults + keyword args
- [ ] `*args` / `**kwargs` used
- [ ] Understand local scope

**Next:** [[Day-10-Modules-Stdlib]]
