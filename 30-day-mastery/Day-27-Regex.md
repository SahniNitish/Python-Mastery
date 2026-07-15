# Day 27 — Regular Expressions (regex)
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-26-Matplotlib]] · **Next:** [[Day-28-Mini-Project]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day27_regex`

```bash
mkdir -p ~/python-practice/day27_regex && cd ~/python-practice/day27_regex
```

---

## Topics

- `re` module
- `search`, `findall`, `sub`, `match`
- Common patterns: digits, email-like, word boundaries
- Raw strings `r"..."`

---

## Learn by typing

```bash
vim day27_demo.py
```

```python
import re

text = "Call me at 506-555-1234 or 506-555-9999 on day 30."

print(re.findall(r"\d+", text))
print(re.findall(r"\d{3}-\d{3}-\d{4}", text))

m = re.search(r"day (\d+)", text)
if m:
    print("day number:", m.group(1))

email_text = "email sahni.nitish@irvingpersonalcare.com please"
print(re.findall(r"[\w.+-]+@[\w-]+\.[\w.-]+", email_text))

dirty = "Python   is   fun"
print(re.sub(r"\s+", " ", dirty).strip())

# validate simple employee id: E12345
for code in ["E12345", "X99", "E00001"]:
    ok = bool(re.fullmatch(r"E\d{5}", code))
    print(code, ok)
```

```bash
python3 day27_demo.py
```

### Pattern cheatsheet

| Pattern | Meaning |
|---------|---------|
| `\d` | digit |
| `\w` | word char |
| `\s` | whitespace |
| `+` | one or more |
| `*` | zero or more |
| `{3}` | exactly 3 |
| `^` `$` | start / end |
| `[]` | character set |
| `()` | capture group |

---

## Practice questions

1. Extract all integers from a sentence.
2. Find all emails in a paragraph.
3. Replace multiple spaces with one space.
4. Check if string is a Canadian-ish postal pattern `A1A 1A1` (basic).
5. Extract hashtags from `"Loving #python and #data"`.
6. Mask a phone number center digits with `re.sub`.
7. Split a log line on commas/spaces carefully.
8. Count how many times word `"error"` appears case-insensitive.
9. Validate password: at least 8 chars, one digit (basic).
10. When is normal `.split()` better than regex?

---

## Mini task — `log_cleaner.py`

Given `app.log`:
```text
INFO user login
ERROR disk full code=503
INFO ok
ERROR timeout code=504
```

Extract all ERROR lines and all `code=###` values.

```bash
vim app.log
vim log_cleaner.py
python3 log_cleaner.py
```

---

## Checklist

- [ ] findall/search/sub used
- [ ] Read a pattern and explain it
- [ ] Log cleaner works

**Next:** [[Day-28-Mini-Project]]
