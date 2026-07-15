# Day 25 — Pandas Intro
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-24-APIs-Requests]] · **Next:** [[Day-26-Matplotlib]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day25_pandas`

```bash
mkdir -p ~/python-practice/day25_pandas && cd ~/python-practice/day25_pandas
python3 -m venv .venv
source .venv/bin/activate
python -m pip install pandas
```

---

## Topics

- DataFrame / Series
- Read CSV
- `head`, `info`, `describe`
- Filter rows, select columns
- `groupby` basics
- Export CSV

---

## Sample data

```bash
vim sales.csv
```

```csv
date,product,qty,price
2026-01-02,Diaper,100,12.5
2026-01-02,Wipe,50,5.0
2026-01-03,Diaper,80,12.5
2026-01-03,Pant,40,14.0
2026-01-04,Wipe,70,5.0
2026-01-04,Diaper,120,12.5
```

---

## Learn by typing

```bash
vim day25_demo.py
```

```python
import pandas as pd

df = pd.read_csv("sales.csv")
print(df.head())
print(df.info())
print(df.describe())

print(df["product"])
print(df[["product", "qty"]])

# filter
print(df[df["qty"] >= 80])
print(df[df["product"] == "Diaper"])

# new column
df["revenue"] = df["qty"] * df["price"]
print(df)

# groupby
print(df.groupby("product")["revenue"].sum())

df.to_csv("sales_with_revenue.csv", index=False)
print("saved")
```

```bash
python day25_demo.py
```

---

## Practice questions

1. Load CSV and print first 3 rows.
2. How many rows/columns? (`df.shape`)
3. Unique products (`df["product"].unique()`).
4. Total qty sold.
5. Average price.
6. Filter rows where product is Wipe.
7. Create revenue column.
8. Revenue by product with groupby.
9. Sort by revenue descending.
10. Save filtered Diaper rows to `diaper_only.csv`.

---

## Mini task — `ipc_audit_fake.py`

Make `audits.csv` with columns: `audit,location,pass,fail` (6+ rows).

Pandas script prints:
- fail rate column
- average pass by audit type
- worst location by fail count

---

## Checklist

- [ ] pandas installed in venv
- [ ] read/filter/groupby worked
- [ ] Mini audit analysis done

**Next:** [[Day-26-Matplotlib]]
