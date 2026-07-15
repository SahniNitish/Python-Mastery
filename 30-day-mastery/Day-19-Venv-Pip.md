# Day 19 — Virtual Environments & pip
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-18-Encapsulation]] · **Next:** [[Day-20-Debug-Test]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day19_venv`

```bash
mkdir -p ~/python-practice/day19_venv && cd ~/python-practice/day19_venv
```

---

## Topics

- Why venv exists (isolated project packages)
- Create / activate / deactivate
- `pip install`, `pip list`, `requirements.txt`
- `python -m pip` (safer)

---

## Do this in terminal (macOS/zsh)

```bash
cd ~/python-practice/day19_venv

# create virtual environment named .venv
python3 -m venv .venv

# activate (macOS/Linux zsh/bash)
source .venv/bin/activate

# your prompt should show (.venv)
which python
python --version

# upgrade pip
python -m pip install --upgrade pip

# install a package
python -m pip install requests

# list packages
python -m pip list

# freeze to requirements
python -m pip freeze > requirements.txt
cat requirements.txt

# deactivate when done
deactivate
```

### Reactivate later

```bash
cd ~/python-practice/day19_venv
source .venv/bin/activate
```

### Install from requirements

```bash
python -m pip install -r requirements.txt
```

---

## Tiny test with requests

With venv activated:

```bash
vim fetch_demo.py
```

```python
import requests

r = requests.get("https://api.github.com")
print("status", r.status_code)
print("server", r.headers.get("server"))
```

```bash
python fetch_demo.py
```

---

## Practice questions

1. What problem does a virtual environment solve?
2. Commands to create and activate a venv on your Mac.
3. Why prefer `python -m pip` over plain `pip`?
4. What is PyPI?
5. What does `pip freeze` do?
6. Should you commit `.venv/` to git? Why/why not?
7. Install `rich`, print a colored hello (optional).
8. Difference between global install and venv install.
9. How do you recreate an environment on another machine?
10. Add `.venv/` to a mental `.gitignore` list.

---

## Mini task

1. Create venv
2. Install `requests`
3. Write `requirements.txt`
4. Run `fetch_demo.py`
5. Deactivate

---

## Checklist

- [ ] Created `.venv`
- [ ] Activated / deactivated
- [ ] Installed package with pip
- [ ] Generated requirements.txt

**Next:** [[Day-20-Debug-Test]]
