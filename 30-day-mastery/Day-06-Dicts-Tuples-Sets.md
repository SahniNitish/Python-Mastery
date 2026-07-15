# Day 6 — Dictionaries, Tuples & Sets
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-05-Lists]] · **Next:** [[Day-07-Week1-Project]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day06_collections`

```bash
mkdir -p ~/python-practice/day06_collections && cd ~/python-practice/day06_collections
```

---

## Topics

- Dict: keys/values, `.get()`, `.items()`
- Tuple: immutable sequence
- Set: unique items, union/intersection
- When to use list vs dict vs set vs tuple

---

## Learn by typing

```bash
vim day06_demo.py
```

```python
# Dictionary
person = {
    "name": "Nitish",
    "role": "Data Analyst",
    "city": "Canada"
}
print(person["name"])
print(person.get("age", "unknown"))
person["age"] = 25

for key, value in person.items():
    print(key, "→", value)

# Tuple
point = (10, 20)
x, y = point
print(x, y)

# Set
a = {1, 2, 3, 3, 2}
b = {3, 4, 5}
print(a)              # {1, 2, 3}
print(a | b)          # union
print(a & b)          # intersection
print(a - b)          # difference
```

### When to use what

| Type | Use when |
|------|----------|
| **list** | Ordered collection, can change |
| **tuple** | Fixed pair/record, safer as key |
| **dict** | Lookup by name/key |
| **set** | Unique items, membership tests |

---

## Practice questions

1. Create a dict of 3 students → marks; print each.
2. Add a new student; update one mark.
3. Safe get: print value or `"N/A"` if key missing.
4. Count letter frequency in `"banana"` using a dict.
5. Convert two lists `keys=["a","b"]`, `vals=[1,2]` into a dict.
6. Unpack tuple `(name, age, city)`.
7. Why can't you do `t[0] = 5` on a tuple? Try and explain.
8. From list with duplicates, make a set and print unique count.
9. Find common items between two lists using sets.
10. Phonebook: store 3 contacts; lookup by name.

---

## Mini task — `contact_book.py`

Menu:
1. Add contact (name → phone)
2. Search contact
3. Show all
4. Quit

Use a dictionary.

---

## Checklist

- [ ] Dict loop with `.items()`
- [ ] Set operations tried
- [ ] Contact book works

**Next:** [[Day-07-Week1-Project]]
