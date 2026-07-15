# Day 5 — Lists
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-04-Loops]] · **Next:** [[Day-06-Dicts-Tuples-Sets]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day05_lists`

```bash
mkdir -p ~/python-practice/day05_lists && cd ~/python-practice/day05_lists
```

---

## Topics

- Create lists, index, slice
- `append`, `insert`, `remove`, `pop`, `extend`
- `len`, `min`, `max`, `sum`, `sorted`
- `in` membership
- Nested lists
- Loop with `enumerate`

---

## Learn by typing

```bash
vim day05_demo.py
```

```python
nums = [10, 20, 30, 40]
print(nums[0], nums[-1])
print(nums[1:3])

nums.append(50)
nums.insert(1, 15)
nums.remove(20)
last = nums.pop()
print(nums, "popped", last)

scores = [88, 92, 70, 95]
print(len(scores), min(scores), max(scores), sum(scores)/len(scores))
print(sorted(scores))          # new list
scores.sort()                  # in place
print(scores)

print(92 in scores)

# enumerate
fruits = ["apple", "banana", "mango"]
for i, fruit in enumerate(fruits, start=1):
    print(i, fruit)

# nested
matrix = [[1, 2], [3, 4]]
print(matrix[1][0])  # 3
```

---

## Practice questions

1. Create a list of 5 cities; print first and last.
2. Add two more cities; remove one.
3. Given numbers, print only values greater than 50.
4. Find second largest number in a list (no fancy tricks required).
5. Reverse a list with a loop (and also with slicing).
6. Remove duplicates from a list (order can change).
7. Merge two lists into one.
8. Count how many times `"pass"` appears in `["pass","fail","pass"]`.
9. Ask user for 5 numbers (loop + append), print average.
10. Flatten `[[1,2],[3,4],[5]]` into `[1,2,3,4,5]`.

---

## Mini task — `todo_list.py`

CLI todo list in memory:
- add item
- view items
- remove by number
- quit

Store tasks in a list.

---

## Checklist

- [ ] Mutating methods practiced
- [ ] `enumerate` used
- [ ] Todo mini app works

**Next:** [[Day-06-Dicts-Tuples-Sets]]
