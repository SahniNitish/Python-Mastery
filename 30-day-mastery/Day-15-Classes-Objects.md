# Day 15 — Classes & Objects
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-14-Week2-Project]] · **Next:** [[Day-16-Methods-Init]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day15_classes`

```bash
mkdir -p ~/python-practice/day15_classes && cd ~/python-practice/day15_classes
```

---

## Topics

- Class = blueprint; object = instance
- Attributes
- Why OOP helps structure bigger programs
- Creating multiple objects from one class

---

## Learn by typing

```bash
vim day15_demo.py
```

```python
class Dog:
    species = "Canine"   # class attribute

    def bark(self):
        print("Woof!")

# create objects
d1 = Dog()
d2 = Dog()
d1.name = "Rex"          # instance attribute
d2.name = "Bella"

print(d1.name, d2.name)
print(d1.species)
d1.bark()
```

Better style uses `__init__` (tomorrow in depth) — peek:

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says woof!")

Dog("Rex").bark()
```

---

## Mental model

```text
Class Dog          → design of a dog
Object Dog("Rex")  → one real dog
self               → "this object"
```

---

## Practice questions

1. Create class `Book` with attributes title/author set after creation; print them.
2. Create 3 `Book` objects.
3. Class `Car` with method `honk()` printing `"beep"`.
4. What is the difference between class and object?
5. Add instance attributes `brand` and `year` to a car.
6. Create class `Student` with method `introduce()` using `self.name`.
7. Make a list of 3 Student objects; loop and introduce each.
8. Class attribute vs instance attribute — give one example each.
9. What is `self`?
10. Why would a bank app use a `BankAccount` class instead of only dicts?

---

## Mini task — `library.py`

Class `Book(title, author, pages)` with method `summary()` printing a one-liner. Create 3 books and print summaries.

---

## Checklist

- [ ] Created a class and objects
- [ ] Called a method with `self`
- [ ] Mini library done

**Next:** [[Day-16-Methods-Init]]
