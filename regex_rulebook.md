
# 📘 Regular Expression (RegEx) Rule Book

## 📌 What is RegEx?
Regular expressions (RegEx) are patterns used to match character combinations in strings. Commonly used in data cleaning, validation, and text processing.

---

## 🔤 Basic Syntax

| Pattern | Meaning |
|--------|---------|
| `.` | Any character except newline |
| `\d` | Digit (0–9) |
| `\D` | Not a digit |
| `\w` | Word character (a-z, A-Z, 0–9, _) |
| `\W` | Not a word character |
| `\s` | Whitespace (space, tab, newline) |
| `\S` | Not whitespace |
| `^` | Start of string |
| `$` | End of string |
| `[...]` | Matches any one character inside brackets |
| `[^...]` | Matches any one character NOT inside brackets |
| `|` | OR operator |

---

## 🔁 Quantifiers

| Pattern | Meaning |
|--------|---------|
| `*` | 0 or more times |
| `+` | 1 or more times |
| `?` | 0 or 1 time |
| `{n}` | Exactly n times |
| `{n,}` | n or more times |
| `{n,m}` | Between n and m times |

---

## 🔗 Grouping and Capturing

| Pattern | Meaning |
|--------|---------|
| `(...)` | Capturing group |
| `(?:...)` | Non-capturing group |
| `(?P<name>...)` | Named capturing group |
| `\1`, `\2`... | Backreference to group 1, 2, etc. |

---

## 📱 Common Patterns

| Use Case | Pattern | Example |
|----------|---------|---------|
| **Phone Number** | `\(\d{3}\)-\d{3}-\d{4}|\d{10}` | Matches `(123)-456-7890` or `1234567890` |
| **Email Address** | `[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+` | Matches `email@domain.com` |
| **URL** | `https?://[^\s]+` | Matches `http://example.com` |
| **Date (dd-mm-yyyy)** | `\d{2}-\d{2}-\d{4}` | Matches `01-07-2025` |
| **Time (HH:MM)** | `\d{2}:\d{2}` | Matches `23:45` |
| **Only Digits** | `^\d+$` | Matches whole string of digits |
| **Only Alphabets** | `^[a-zA-Z]+$` | Matches only letters |
| **Alphanumeric** | `^[a-zA-Z0-9]+$` | Letters and numbers |

---

## ✅ Useful Functions in Python (`re` module)

```python
import re

# Find all matches
matches = re.findall(pattern, text)

# Search (first match)
match = re.search(pattern, text)

# Match (from start)
match = re.match(pattern, text)

# Replace
re.sub(pattern, replacement, text)

# Compile pattern
regex = re.compile(pattern)
regex.findall(text)
```

---

## 💡 Tips

- Use **raw strings** in Python: `r"\d{3}"` instead of `"\\d{3}"`
- Always test patterns with real examples
- Use tools like [regex101.com](https://regex101.com) to debug patterns
- Try not to overcomplicate patterns—break them down

---

## 📚 Resources

- [Regex101](https://regex101.com) (Interactive RegEx editor)
- Python `re` documentation: https://docs.python.org/3/library/re.html
- Cheatsheets:
  - https://www.debuggex.com/cheatsheet/regex/python
  - https://www.rexegg.com/regex-quickstart.html
