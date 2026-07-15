# Day 0 — Terminal + vim (Create, Edit, Run Files)
> **Plan:** [[Python_30_Day_Mastery]] · **Next:** [[Day-01-Hello-Variables]]

**Time:** 30–45 minutes  
**Goal:** Be comfortable creating a Python file in the terminal, editing it with **vim**, saving it, and running it with `python3`.

This is your **Day 0** — no big Python theory yet. Only the workflow you will use for the next 30 days.

---

## Topics

1. What is the terminal?
2. Moving around folders (`pwd`, `ls`, `cd`, `mkdir`)
3. Creating & editing files with **vim**
4. Running Python files with `python3`
5. Fixing common mistakes

---

## 1) Open the terminal (macOS)

- Spotlight: `Cmd + Space` → type **Terminal** → Enter  
- Or: Applications → Utilities → Terminal

You should see a prompt like:
```text
yourname@MacBook ~ %
```

`~` means your **home folder**.

---

## 2) Essential navigation commands

Type these one by one. Press Enter after each.

```bash
pwd
# print working directory — where am I?

ls
# list files/folders in current directory

ls -la
# detailed list (includes hidden files)

cd ~
# go to home folder

mkdir -p ~/python-practice/day00_terminal
# create practice folders (-p = create parents if needed)

cd ~/python-practice/day00_terminal
# enter the folder

pwd
# confirm you are inside day00_terminal

ls
# should be empty (or almost empty)
```

### `cd` cheat sheet

```bash
cd folder_name     # go into a folder
cd ..              # go up one level
cd ~               # go home
cd /Users/YourName # absolute path
cd -               # go back to previous folder
```

---

## 3) Create a file with vim

Still inside `~/python-practice/day00_terminal`:

```bash
vim hello.py
```

### Modes (the only thing you must understand)

Vim has **modes**. Beginners get stuck when they forget which mode they are in.

| Mode | How you enter it | What you do there |
|------|------------------|-------------------|
| **Normal** | default when vim opens; press `Esc` | move cursor, run commands (`:w`, `:q`) |
| **Insert** | press `i` | type code like a normal editor |
| **Command-line** | press `:` from Normal | save, quit, search (`:w`, `:q`, `:wq`) |

**Golden rule:** when confused → hit **`Esc`** a few times → you are back in Normal mode.

### Type this program

1. Open: `vim hello.py`
2. Press **`i`** (bottom-left may show `-- INSERT --`)
3. Type:

```python
print("Hello from Day 0!")
print("I created this file with vim.")
```

### Save and exit (do this every time)

1. Press **`Esc`** (leave Insert mode)
2. Type **`:wq`** then **Enter**
   - `:w` = write (save)
   - `:q` = quit
   - `:wq` = save + quit

You are back at the normal terminal prompt.

### Other ways to leave vim

| Command | Meaning |
|---------|---------|
| `:w` | save only (stay in vim) |
| `:q` | quit (fails if unsaved changes) |
| `:wq` or `:x` | save and quit |
| `:q!` | quit **without** saving (discard changes) |
| `ZZ` | save and quit (Normal mode, no `:`) |

### Verify the file exists

```bash
ls
# you should see: hello.py

cat hello.py
# print file contents without opening editor
```

---

## 4) Run the Python file

```bash
python3 hello.py
```

**Expected output:**
```text
Hello from Day 0!
I created this file with vim.
```

### If `python3` is not found

```bash
python --version
which python3
```

On macOS, if missing:

```bash
brew install python
```

---

## 5) Edit an existing file

```bash
vim hello.py
```

1. `i` → Insert mode  
2. Change the first line to:

```python
print("Hello from Day 0 — edited!")
```

3. `Esc` → `:wq` → Enter  
4. Run again:

```bash
python3 hello.py
```

You just did the full loop: **open → edit → save → run**.

---

## 6) Second file — name + math

```bash
vim greeter.py
```

```python
name = "Nitish"
age = 25

print("Name:", name)
print("Age:", age)
print("Next year I will be", age + 1)
```

`Esc` → `:wq` → run:

```bash
python3 greeter.py
```

---

## 7) Interactive Python (REPL) — quick tests

```bash
python3
```

You will see `>>>`. Try:

```python
2 + 2
print("hi")
exit()
```

Or press `Ctrl + D` to leave.

Use REPL for tiny experiments. Use **vim + .py files** for real practice.

---

## 8) Useful file commands (not vim)

```bash
# create empty file without vim
touch notes.txt

# copy a file
cp hello.py hello_backup.py

# rename / move
mv greeter.py day00_greeter.py

# delete a file (careful!)
rm hello_backup.py

# view file with less (q to quit)
less day00_greeter.py
```

---

## vim keys — memorize these first

### Essential (Day 0)

| Keys | Mode | Action |
|------|------|--------|
| `i` | Normal → Insert | insert before cursor |
| `a` | Normal → Insert | insert after cursor |
| `o` | Normal → Insert | new line below + insert |
| `Esc` | any → Normal | leave Insert mode |
| `:w` | Normal | save |
| `:q` | Normal | quit |
| `:wq` | Normal | save + quit |
| `:q!` | Normal | quit without saving |

### Movement (Normal mode) — learn this week

| Key | Move |
|-----|------|
| `h` `j` `k` `l` | left / down / up / right |
| `w` / `b` | next / previous word |
| `0` / `$` | start / end of line |
| `gg` / `G` | top / bottom of file |
| `dd` | delete (cut) current line |
| `yy` | yank (copy) current line |
| `p` | paste below |
| `u` | undo |
| `Ctrl + r` | redo |
| `/text` | search forward (`n` = next) |
| `x` | delete character under cursor |

### Optional quality-of-life

```bash
# show line numbers every time (optional config)
echo "set number" >> ~/.vimrc
echo "syntax on" >> ~/.vimrc
echo "set tabstop=4 shiftwidth=4 expandtab" >> ~/.vimrc
```

Then reopen vim — line numbers + Python-ish tabs.

---

## Practice questions (answer in your own words)

Write answers in a notes file:

```bash
vim day00_answers.md
```

1. What does `pwd` show you?
2. What is the difference between `ls` and `ls -la`?
3. What does `cd ..` do?
4. How do you create a new folder called `practice`?
5. How do you create a new Python file with vim?
6. After typing code in vim, what keys save and quit?
7. How do you run `hello.py`?
8. What is the difference between `python3 hello.py` and just typing `python3`?
9. What does `Esc` do in vim? Why is it important?
10. How do you quit vim **without** saving?

---

## Mini tasks (must complete)

### Task A — Create folder structure

```bash
cd ~/python-practice
mkdir -p day01_hello day02_strings projects
ls
```

### Task B — Make `about_me.py`

```bash
cd ~/python-practice/day00_terminal
vim about_me.py
```

```python
print("=== About Me ===")
print("Name: Your Name Here")
print("Goal: Master Python in 30 days")
print("Editor: vim")
print("Runner: python3")
```

```bash
python3 about_me.py
```

### Task C — Break it on purpose, then fix it

1. Open `about_me.py` in vim.
2. Delete one closing quote on purpose.
3. Save and run — read the error message.
4. Fix it in vim and run again successfully.

**Learning:** Errors are normal. Read the last line of the traceback.

### Task D — Vim recovery drill

1. Open a file, type junk, then exit with `:q!` (discard).
2. Open again, type something good, save with `:wq`.
3. Confirm you know the difference.

---

## Common mistakes & fixes

| Problem | Fix |
|---------|-----|
| `command not found: python3` | Install Python, or try `python` |
| `No such file or directory` | `pwd` + `ls` — wrong folder? |
| Typed code but nothing appears | You are in **Normal** mode — press `i` first |
| Pressed keys and weird stuff happens | Hit **`Esc`**, then try again |
| Stuck and can't quit | `Esc`, then `:q!` Enter |
| "No write since last change" | `:wq` to save+quit, or `:q!` to discard |
| Code runs but old output | Did you `:w` save before running? |
| `SyntaxError: EOL while scanning string` | Missing closing quote `"` |

---

## Day 0 checklist

- [ ] I can open Terminal
- [ ] I can use `pwd`, `ls`, `cd`, `mkdir`
- [ ] I created `~/python-practice/day00_terminal`
- [ ] I created a file with `vim hello.py`
- [ ] I enter Insert with `i` and leave with `Esc`
- [ ] I save/quit with `:wq`
- [ ] I ran code with `python3 hello.py`
- [ ] I edited a file and re-ran it
- [ ] I know `:q!` to force quit without saving
- [ ] I completed Task A–D
- [ ] I answered the 10 practice questions

---

## End of Day 0 — what you unlocked

You now have the **full coding loop**:

```text
terminal → vim file.py → i → type → Esc → :wq → python3 file.py → fix → repeat
```

Tomorrow you start real Python.

**Next day:** [[Day-01-Hello-Variables]]

---

## Quick command card (pin this)

```bash
cd ~/python-practice/day00_terminal
vim hello.py           # open
# i  → type code
# Esc → :wq → Enter
python3 hello.py       # run
```

```text
STUCK IN VIM?  →  Esc   Esc   :q!   Enter
```
