# Day 18 — Encapsulation & Dunder Methods
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-17-Inheritance]] · **Next:** [[Day-19-Venv-Pip]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day18_encapsulation`

```bash
mkdir -p ~/python-practice/day18_encapsulation && cd ~/python-practice/day18_encapsulation
```

---

## Topics

- Public vs "private" (`_name`, `__name`)
- `@property` getters/setters
- Dunder methods: `__str__`, `__repr__`, `__len__`, `__eq__`
- Composition (has-a) vs inheritance (is-a)

---

## Learn by typing

```bash
vim day18_demo.py
```

```python
class Temperature:
    def __init__(self, celsius):
        self._celsius = celsius

    @property
    def celsius(self):
        return self._celsius

    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("Below absolute zero")
        self._celsius = value

    @property
    def fahrenheit(self):
        return self._celsius * 9 / 5 + 32

    def __str__(self):
        return f"{self._celsius}°C ({self.fahrenheit:.1f}°F)"

    def __eq__(self, other):
        return self._celsius == other._celsius

t = Temperature(25)
print(t)
t.celsius = 30
print(t.fahrenheit)

class Team:
    def __init__(self, members):
        self.members = members

    def __len__(self):
        return len(self.members)

print(len(Team(["A", "B", "C"])))
```

---

## Practice questions

1. Make `BankAccount.balance` readable via property, settable with validation (≥ 0).
2. Implement `__str__` and `__repr__` for a `Point(x,y)`.
3. Implement `__eq__` so two Points with same x,y are equal.
4. Class `Deck` with `__len__` = number of cards.
5. What does a single underscore `_balance` signal to other developers?
6. Composition demo: `Laptop` has a `Battery` object.
7. Prevent setting invalid email on a `User` via setter.
8. Why prefer properties over public attributes for important fields?
9. Compare two Temperature objects with `==`.
10. Write one sentence: encapsulation means ___.

---

## Mini task — `product.py`

`Product(name, price, qty)`:
- validate price > 0, qty ≥ 0
- property `value` = price * qty
- `__str__` nice inventory line

---

## Checklist

- [ ] Used `@property`
- [ ] Implemented at least 2 dunder methods
- [ ] Product class works

**Next:** [[Day-19-Venv-Pip]]
