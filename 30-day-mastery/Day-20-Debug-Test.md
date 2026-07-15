# Day 20 — Debugging & Basic Tests
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-19-Venv-Pip]] · **Next:** [[Day-21-Week3-Project]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day20_debug`

```bash
mkdir -p ~/python-practice/day20_debug && cd ~/python-practice/day20_debug
```

---

## Topics

- Reading tracebacks
- `print` debugging strategically
- `assert`
- `unittest` or simple test functions
- Rubber-duck debugging mindset

---

## Learn by typing

### 1) Read a traceback

```bash
vim buggy.py
```

```python
def average(nums):
    return sum(nums) / len(nums)

data = []
print(average(data))
```

```bash
python3 buggy.py
```

Read bottom line first: `ZeroDivisionError`. Fix:

```python
def average(nums):
    if not nums:
        return 0
    return sum(nums) / len(nums)
```

### 2) assert

```bash
vim test_math_utils.py
```

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0
    assert add(0, 0) == 0
    print("all tests passed")

if __name__ == "__main__":
    test_add()
```

```bash
python3 test_math_utils.py
```

### 3) unittest style (optional)

```bash
vim test_unittest_demo.py
```

```python
import unittest

def is_even(n):
    return n % 2 == 0

class TestEven(unittest.TestCase):
    def test_even(self):
        self.assertTrue(is_even(2))

    def test_odd(self):
        self.assertFalse(is_even(3))

if __name__ == "__main__":
    unittest.main()
```

```bash
python3 test_unittest_demo.py
```

---

## Debugging checklist

1. Read **last line** of traceback
2. Open the **file + line number** shown
3. Print intermediate values
4. Reproduce with smallest input
5. Fix → re-run tests

---

## Practice questions

1. Fix a function that fails on empty list.
2. Write 3 asserts for a `max_of_two(a,b)` function.
3. What does `AssertionError` mean?
4. Intentionally break a test; watch it fail; fix it.
5. Explain stack traceback top vs bottom.
6. Add a guard clause to avoid crash.
7. Write tests for `is_palindrome`.
8. Why are tests useful when you refactor?
9. Print-debug a loop that "skips" a value.
10. Name 2 bugs you fixed this week and the error type.

---

## Mini task — `buggy_stats.py` → fixed + tests

Create a buggy mean/min/max script, fix it, write `test_stats.py` with asserts.

---

## Checklist

- [ ] Comfortable reading tracebacks
- [ ] Wrote assert tests
- [ ] Fixed at least one deliberate bug

**Next:** [[Day-21-Week3-Project]]
