# Day 1 — Hello World, Variables & Types
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-00-Terminal-and-Vim]] · **Next:** [[Day-02-Strings-Operators]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day01_hello`

```bash
mkdir -p ~/python-practice/day01_hello
cd ~/python-practice/day01_hello
```

---

## Topics

- `print()`
- Variables and assignment
- Basic types: `int`, `float`, `str`, `bool`
- `type()`, `input()`
- Comments `#`

---

## Learn by typing

```bash
vim day01_basics.py
```

```python
# This is a comment — Python ignores it

print("Hello, Python!")

# Variables store values
name = "Nitish"
age = 25
height = 5.9
is_student = True

print(name)
print(age)
print(type(name))      # <class 'str'>
print(type(age))       # <class 'int'>
print(type(height))    # <class 'float'>
print(type(is_student))# <class 'bool'>

# input always returns a string
user = input("What is your name? ")
print("Nice to meet you,", user)
```

```bash
python3 day01_basics.py
```

---

## Key rules

| Rule | Example |
|------|---------|
| Names are case-sensitive | `Age` ≠ `age` |
| No spaces in names | use `first_name` not `first name` |
| Can reassign | `x = 1` then `x = 2` |
| `input()` → always `str` | cast with `int(input(...))` |

```python
age_text = input("Age: ")
age = int(age_text)          # convert string → int
print("In 10 years:", age + 10)
```

---

## Practice questions

Create `day01_questions.py` and solve:

1. Print your full name and city on two lines.
2. Store `a = 10`, `b = 3`. Print their sum, difference, product.
3. Ask user for favorite color with `input()`, then print `"Your color is: ..."`.
4. Create variables for: integer, float, string, boolean. Print each with `type()`.
5. Convert the string `"42"` to an integer and add 8. Print result.
6. What happens if you do `int("hello")`? Try it, read the error.
7. Swap two variables `x` and `y` (hint: `x, y = y, x`).
8. Ask for birth year, compute approximate age for year 2026.
9. Print `True` if `10 > 5`, else `False` (use a comparison expression).
10. Write 3 useful comments above a short program explaining what it does.

---

## Mini task — `intro.py`

```bash
vim intro.py
```

Program should:
1. Ask name, age, city
2. Print a short intro paragraph using those values
3. Print the type of each variable

---

## Checklist

- [ ] Ran `print` and `input`
- [ ] Used `int`, `float`, `str`, `bool`
- [ ] Converted string input to int
- [ ] Solved questions 1–10
- [ ] Built `intro.py`

**Next:** [[Day-02-Strings-Operators]]
