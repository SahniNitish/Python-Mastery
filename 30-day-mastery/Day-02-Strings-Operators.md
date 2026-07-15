# Day 2 — Strings & Operators
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-01-Hello-Variables]] · **Next:** [[Day-03-Conditionals]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day02_strings`

```bash
mkdir -p ~/python-practice/day02_strings && cd ~/python-practice/day02_strings
```

---

## Topics

- String indexing & slicing
- String methods: `upper`, `lower`, `strip`, `replace`, `split`, `join`
- f-strings
- Arithmetic, comparison, logical operators
- `//`, `%`, `**`

---

## Learn by typing

```bash
vim day02_demo.py
```

```python
msg = "  Python Mastery  "
print(msg.strip())
print(msg.upper())
print(msg.lower())
print(msg.replace("Mastery", "Power"))

word = "Python"
print(word[0])       # P
print(word[-1])      # n
print(word[0:3])     # Pyt
print(word[::-1])    # nohtyP

name = "Nitish"
days = 30
print(f"{name} will master Python in {days} days")

# Operators
print(10 + 3, 10 - 3, 10 * 3, 10 / 3)
print(10 // 3)   # floor division → 3
print(10 % 3)    # remainder → 1
print(2 ** 3)    # power → 8

print(5 > 3 and 2 < 4)   # True
print(5 > 3 or 2 > 4)    # True
print(not False)         # True
```

```bash
python3 day02_demo.py
```

---

## Practice questions

1. Given `s = "irving personal care"`, print it title-cased (`.title()`).
2. Count how many times letter `"a"` appears in a sentence (`.count("a")`).
3. Check if a string starts with `"Py"` and ends with `"on"`.
4. Split `"apple,banana,mango"` into a list.
5. Join `["I", "love", "Python"]` into one string with spaces.
6. Ask for first and last name; print `LAST, First` using f-string.
7. Compute BMI formula: `weight_kg / (height_m ** 2)` (inputs from user).
8. Extract the domain from `"user@gmail.com"` (use `.split("@")`).
9. Remove all spaces from a string.
10. Write expression: number is even if `n % 2 == 0`. Test with 7 and 8.

---

## Mini task — `string_lab.py`

Build a program that:
1. Takes a sentence from user
2. Prints length, uppercase, lowercase, reversed
3. Prints word count (`len(sentence.split())`)

---

## Checklist

- [ ] Used slicing and f-strings
- [ ] Practiced `// % **`
- [ ] 10 questions done
- [ ] `string_lab.py` works

**Next:** [[Day-03-Conditionals]]
