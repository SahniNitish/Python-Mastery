# Day 26 — Matplotlib Basics
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-25-Pandas-Intro]] · **Next:** [[Day-27-Regex]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day26_matplotlib`

```bash
mkdir -p ~/python-practice/day26_matplotlib && cd ~/python-practice/day26_matplotlib
python3 -m venv .venv
source .venv/bin/activate
python -m pip install matplotlib pandas
```

---

## Topics

- Line chart, bar chart
- Labels, title, legend
- Save figure to PNG
- Quick plot from pandas

---

## Learn by typing

```bash
vim day26_demo.py
```

```python
import matplotlib.pyplot as plt
import pandas as pd

# simple line
days = [1, 2, 3, 4, 5]
scores = [70, 75, 72, 80, 88]

plt.figure()
plt.plot(days, scores, marker="o")
plt.title("Practice Scores")
plt.xlabel("Day")
plt.ylabel("Score")
plt.grid(True)
plt.savefig("scores_line.png")
plt.close()

# bar chart
products = ["Diaper", "Wipe", "Pant"]
revenue = [2500, 900, 1200]

plt.figure()
plt.bar(products, revenue)
plt.title("Revenue by Product")
plt.ylabel("Revenue")
plt.savefig("revenue_bar.png")
plt.close()

# from pandas
df = pd.DataFrame({"product": products, "revenue": revenue})
ax = df.plot(kind="bar", x="product", y="revenue", legend=False, title="Pandas Bar")
ax.set_ylabel("Revenue")
plt.tight_layout()
plt.savefig("revenue_pandas.png")
plt.close()

print("charts saved")
```

```bash
python day26_demo.py
ls *.png
# open: open scores_line.png
```

---

## Practice questions

1. Line chart of 7 study minutes per day.
2. Add title + axis labels.
3. Bar chart of 4 categories.
4. Save chart as PNG.
5. Two lines on one chart (e.g., plan vs actual) with legend.
6. Plot from a small DataFrame.
7. What does `plt.close()` help with?
8. Change marker/style on line plot.
9. Horizontal bar chart (`plt.barh`).
10. Create a chart that would help in your IPC audit dashboard story.

---

## Mini task — `audit_chart.py`

CSV of audit fail counts by type → bar chart → `audit_fails.png`.

---

## Checklist

- [ ] Created line + bar charts
- [ ] Saved PNG from terminal workflow
- [ ] Mini audit chart done

**Next:** [[Day-27-Regex]]
