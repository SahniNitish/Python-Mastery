# Day 16 — Methods, `__init__`, self
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-15-Classes-Objects]] · **Next:** [[Day-17-Inheritance]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day16_init`

```bash
mkdir -p ~/python-practice/day16_init && cd ~/python-practice/day16_init
```

---

## Topics

- `__init__` constructor
- Instance methods
- Updating object state
- `__str__` intro (nice printing)

---

## Learn by typing

```bash
vim day16_demo.py
```

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        if amount <= 0:
            print("Amount must be positive")
            return
        self.balance += amount

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient funds")
            return
        self.balance -= amount

    def __str__(self):
        return f"{self.owner}: ${self.balance:.2f}"

acc = BankAccount("Nitish", 100)
acc.deposit(50)
acc.withdraw(30)
print(acc)
```

---

## Practice questions

1. Class `Rectangle(w, h)` with `area()` and `perimeter()`.
2. Class `Counter` with `increment`, `decrement`, `value`.
3. Class `Playlist` storing song list; methods `add`, `show`.
4. Prevent negative deposit with a check.
5. Add method `transfer(other_account, amount)`.
6. What runs automatically when you do `BankAccount("A")`?
7. Why is first parameter named `self` by convention?
8. Create two accounts and transfer between them.
9. Implement `__str__` for `Rectangle`.
10. Store a list of accounts; print all.

---

## Mini task — `bank_cli.py`

Menu:
1. Create account
2. Deposit
3. Withdraw
4. Show balance
5. Quit

(One account in memory is fine.)

---

## Checklist

- [ ] Solid with `__init__`
- [ ] Methods change object state
- [ ] Bank CLI works

**Next:** [[Day-17-Inheritance]]
