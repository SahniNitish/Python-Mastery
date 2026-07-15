# Day 17 — Inheritance & Polymorphism
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-16-Methods-Init]] · **Next:** [[Day-18-Encapsulation]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day17_inheritance`

```bash
mkdir -p ~/python-practice/day17_inheritance && cd ~/python-practice/day17_inheritance
```

---

## Topics

- Parent / child classes
- `super()`
- Method overriding
- Polymorphism (same method name, different behavior)

---

## Learn by typing

```bash
vim day17_demo.py
```

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "..."

class Dog(Animal):
    def speak(self):
        return f"{self.name}: Woof"

class Cat(Animal):
    def speak(self):
        return f"{self.name}: Meow"

class Puppy(Dog):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

animals = [Dog("Rex"), Cat("Mimi"), Puppy("Max", 1)]
for a in animals:
    print(a.speak())   # polymorphism
```

---

## Practice questions

1. `Vehicle` → `Car` and `Bike` subclasses.
2. Override a `describe()` method in each subclass.
3. `Employee` base; `Manager` adds `department`.
4. Use `super().__init__` in child.
5. Function `make_speak(animal)` that calls `.speak()` — works for Dog/Cat.
6. What is method overriding?
7. Create `ElectricCar(Car)` with battery attribute.
8. `isinstance(obj, Class)` checks — try them.
9. Multi-level inheritance example (A→B→C).
10. When is inheritance a bad fit? (prefer composition note)

---

## Mini task — `shapes.py`

```text
Shape
 ├── Rectangle → area()
 └── Circle → area()
```

Put shapes in a list; print each area.

---

## Checklist

- [ ] Built parent + child classes
- [ ] Used `super()`
- [ ] Polymorphism demo works

**Next:** [[Day-18-Encapsulation]]
