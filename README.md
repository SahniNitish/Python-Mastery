# Python 30-Day Mastery Plan
> **Related:** [[Python_Roadmap]] · [[Python_Foundations_Checklist]] · [[python-50-question-easy]] · [[PythonProjects]] · [[Study & Career — MOC]]

**Goal:** Go from zero → confident Python coder in 30 days, coding **in the terminal** with `vim` + `python3`.

**Time:** 60–90 minutes/day (Day 0 may take 30–45 min)

**How you will code every day:**
```bash
cd ~/python-practice          # your practice folder
vim day01_hello.py           # create/edit file
python3 day01_hello.py        # run it
```

**Folder layout (create on Day 0):**
```
~/python-practice/
├── day00_terminal/
├── day01_...
├── day02_...
└── projects/
```

---

## How to use this plan

1. Open the day note for today (links below).
2. Read **Topics** → type every example in vim → run it.
3. Solve all **Practice Questions** yourself first.
4. Do the **Mini Task** before you stop.
5. Check off the day on this page.

**Rule:** Do not copy-paste blindly. Type. Break things. Fix them.

---

## Progress tracker

| Day | Topic | Done |
|-----|--------|------|
| [[Day-00-Terminal-and-Vim\|0]] | Terminal + vim (create/edit/run files) |✅|
| [[Day-01-Hello-Variables\|1]] | Hello world, variables, types |✅|
| [[Day-02-Strings-Operators\|2]] | Strings & operators | ☐ |
| [[Day-03-Conditionals\|3]] | if / elif / else | ☐ |
| [[Day-04-Loops\|4]] | for & while loops | ☐ |
| [[Day-05-Lists\|5]] | Lists | ☐ |
| [[Day-06-Dicts-Tuples-Sets\|6]] | Dicts, tuples, sets | ☐ |
| [[Day-07-Week1-Project\|7]] | Week 1 project + review | ☐ |
| [[Day-08-Functions\|8]] | Functions | ☐ |
| [[Day-09-Args-Scope-Lambda\|9]] | args, scope, lambda | ☐ |
| [[Day-10-Modules-Stdlib\|10]] | Modules & stdlib | ☐ |
| [[Day-11-File-IO\|11]] | File read/write | ☐ |
| [[Day-12-Exceptions\|12]] | try / except | ☐ |
| [[Day-13-Comprehensions\|13]] | List/dict comprehensions | ☐ |
| [[Day-14-Week2-Project\|14]] | Week 2 project | ☐ |
| [[Day-15-Classes-Objects\|15]] | Classes & objects | ☐ |
| [[Day-16-Methods-Init\|16]] | methods, `__init__`, self | ☐ |
| [[Day-17-Inheritance\|17]] | Inheritance & polymorphism | ☐ |
| [[Day-18-Encapsulation\|18]] | Encapsulation & dunder methods | ☐ |
| [[Day-19-Venv-Pip\|19]] | venv + pip | ☐ |
| [[Day-20-Debug-Test\|20]] | Debugging & basic tests | ☐ |
| [[Day-21-Week3-Project\|21]] | Week 3 project | ☐ |
| [[Day-22-Pathlib-OS\|22]] | pathlib & OS automation | ☐ |
| [[Day-23-CSV-JSON\|23]] | CSV & JSON | ☐ |
| [[Day-24-APIs-Requests\|24]] | APIs with requests | ☐ |
| [[Day-25-Pandas-Intro\|25]] | Pandas intro | ☐ |
| [[Day-26-Matplotlib\|26]] | Matplotlib basics | ☐ |
| [[Day-27-Regex\|27]] | Regular expressions | ☐ |
| [[Day-28-Mini-Project\|28]] | Build a mini tool | ☐ |
| [[Day-29-Portfolio-Polish\|29]] | Polish + README + Git | ☐ |
| [[Day-30-Final-Project\|30]] | Final project + next steps | ☐ |

---

## 4-week overview

| Week | Theme | Outcome |
|------|--------|---------|
| **0** | Terminal setup | Create, edit, run `.py` files in terminal |
| **1** (Days 1–7) | Fundamentals | Variables, strings, logic, loops, collections |
| **2** (Days 8–14) | Reusable code | Functions, files, errors, modules |
| **3** (Days 15–21) | OOP + tools | Classes, venv, pip, testing |
| **4** (Days 22–30) | Real work | Data files, APIs, pandas, projects |

---

## Daily rhythm (use every day)

```
1. Open terminal
2. cd ~/python-practice/dayXX_...
3. vim exercise.py
4. i → type code → Esc → :wq → Enter
5. python3 exercise.py
6. Fix errors → repeat
7. Answer questions in the day note
```

### vim cheat sheet (pin this)

| Key | Action |
|-----|--------|
| `i` | Insert mode (type code) |
| `Esc` | Back to Normal mode |
| `:w` | Save |
| `:q` | Quit |
| `:wq` | Save + quit |
| `:q!` | Quit without saving |
| `dd` | Delete line |
| `yy` / `p` | Copy line / paste |
| `u` | Undo |
| `/text` | Search |

**Stuck in vim?** → `Esc` `Esc` → `:q!` → Enter

### python3 essentials

```bash
python3 --version          # check install
python3 script.py          # run a file
python3 -i script.py       # run then stay in interactive shell
python3                    # interactive REPL (quit with exit() or Ctrl+D)
```

---

## Practice folder setup (do once on Day 0)

```bash
mkdir -p ~/python-practice
cd ~/python-practice
mkdir -p day00_terminal projects
```

---

## Extra practice banks

- Easy drills: [[python-50-question-easy]]
- Foundations checklist: [[Python_Foundations_Checklist]]
- Bigger project ideas: [[PythonProjects]]
- Long-term roadmap: [[Python_Roadmap]]

---

## After Day 30

You will be ready for:
- Automation scripts at work
- Data analysis with Pandas
- Coding interviews (easy–medium)
- Building small tools + portfolio projects

**Next:** Open → [[Day-00-Terminal-and-Vim]]
