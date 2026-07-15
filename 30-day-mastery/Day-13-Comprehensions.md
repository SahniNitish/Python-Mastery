# Day 13 — Comprehensions
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-12-Exceptions]] · **Next:** [[Day-14-Week2-Project]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day13_comprehensions`

```bash
mkdir -p ~/python-practice/day13_comprehensions && cd ~/python-practice/day13_comprehensions
```

---

## Topics

- List comprehensions
- Dict / set comprehensions
- Conditional comprehensions
- Readability rule: if it's hard to read, use a normal loop

---

## Learn by typing

```bash
vim day13_demo.py
```

```python
# list comprehension
squares = [n * n for n in range(1, 11)]
print(squares)

evens = [n for n in range(20) if n % 2 == 0]
print(evens)

words = ["python", "java", "go", "rust"]
upper = [w.upper() for w in words]
long = [w for w in words if len(w) > 3]

# dict comprehension
lengths = {w: len(w) for w in words}
print(lengths)

# set comprehension
letters = {ch for ch in "banana"}
print(letters)

# nested-ish
pairs = [(x, y) for x in range(3) for y in range(2)]
print(pairs)
```

---

## Practice questions

1. Squares of 1..15.
2. From a list of temps in C, make F list: `f = c*9/5+32`.
3. Extract only positive numbers from a mixed list.
4. Dict: number → `"even"`/`"odd"` for 1..10.
5. Flatten `[[1,2],[3,4]]` with comprehension.
6. Lengths of each word in a sentence.
7. Set of first letters from a list of names.
8. Filter scores ≥ 50 from `[40, 55, 70, 30, 90]`.
9. Rewrite a 5-line loop as a comprehension (your choice).
10. When should you NOT use a comprehension?

---

## Mini task — `clean_data.py`

Given:
```python
raw = ["  alice ", "BOB", "", "Charlie", "bob", "  "]
```

Produce cleaned unique lowercase names (no empties), sorted. Use comprehensions + set.

---

## Checklist

- [ ] List + dict comprehension written
- [ ] Filter with `if` in comprehension
- [ ] Mini data-clean task done

**Next:** [[Day-14-Week2-Project]]
