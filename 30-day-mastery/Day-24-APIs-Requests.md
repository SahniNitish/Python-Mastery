# Day 24 — APIs with requests
> **Plan:** [[Python_30_Day_Mastery]] · **Prev:** [[Day-23-CSV-JSON]] · **Next:** [[Day-25-Pandas-Intro]]

**Time:** 60–90 min  
**Folder:** `~/python-practice/day24_apis`

```bash
mkdir -p ~/python-practice/day24_apis && cd ~/python-practice/day24_apis
python3 -m venv .venv
source .venv/bin/activate
python -m pip install requests
```

---

## Topics

- What is an API / HTTP GET
- `requests.get`
- Status codes
- JSON responses
- Query parameters
- Saving API data to file

---

## Learn by typing

```bash
vim day24_demo.py
```

```python
import requests
import json

url = "https://api.github.com"
r = requests.get(url, timeout=10)
print("status:", r.status_code)
print("ok?", r.ok)

data = r.json()
print(type(data))
print(data.get("current_user_url"))

# public API example — JSONPlaceholder
r2 = requests.get(
    "https://jsonplaceholder.typicode.com/todos/1",
    timeout=10,
)
todo = r2.json()
print(todo)

# list with params
r3 = requests.get(
    "https://jsonplaceholder.typicode.com/posts",
    params={"userId": 1},
    timeout=10,
)
posts = r3.json()
print("posts for user 1:", len(posts))
print("first title:", posts[0]["title"])

with open("posts_user1.json", "w", encoding="utf-8") as f:
    json.dump(posts, f, indent=2)
```

```bash
python day24_demo.py
```

---

## Practice questions

1. GET a URL and print status code.
2. If status != 200, print error message.
3. Fetch todo #5 and print `title` + `completed`.
4. Fetch posts for `userId=2`, count them.
5. Save response JSON to a file.
6. What does timeout protect you from?
7. Headers: print `Content-Type` from response headers.
8. Write a function `fetch_json(url)` that returns dict/list or None on failure.
9. Explain GET vs POST in one sentence each.
10. Why shouldn't you hardcode secret API keys in code?

---

## Mini task — `weather_or_public_api.py`

Use any free public API (JSONPlaceholder is fine if weather needs a key):

```text
Fetch 5 posts → print id and title → save to data.json
```

Or with Open-Meteo (no key):
```text
https://api.open-meteo.com/v1/forecast?latitude=45.27&longitude=-66.06&current_weather=true
```

Print temperature for Saint John area coords (example).

---

## Checklist

- [ ] venv + requests installed
- [ ] Successful GET + JSON parse
- [ ] Saved data to file
- [ ] Error handling for bad status

**Next:** [[Day-25-Pandas-Intro]]
