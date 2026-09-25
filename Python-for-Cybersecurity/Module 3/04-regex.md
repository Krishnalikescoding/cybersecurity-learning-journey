# Python Regular Expressions (Regex) 

## What is Regex?
- **Regular expression (regex)**: a sequence of characters forming a search pattern.
- Used to find complex patterns (IP addresses, emails, device IDs) within strings.

## Using the `re` Module
```python
import re
```
- **`re.findall(pattern, string)`**: returns a list of all matches to a pattern.
  - Param 1: regex pattern (as a string)
  - Param 2: string to search through

```python
import re
re.findall("ts", "tsnow, tshah, bmoreno")
# ['ts', 'ts']
```

## Character Type Symbols

| Symbol | Matches | Example |
|--------|---------|---------|
| `\w` | any alphanumeric character or underscore | matches I,D,_,A,1,7 in "ID_A17" |
| `\d` | any single digit | matches 1,7 in "ID_A17" |
| `\s` | any whitespace (space, tab, newline) | matches the space in "user 1" |
| `.` | any character except newline | — |
| `\.` | literal period (escaped) | — |

```python
re.findall("\w", "h32rb17")   # 7 matches — every char is alphanumeric
re.findall("\d", "h32rb17")   # 4 matches — only digits: 3,2,1,7
```

## Quantifier Symbols

| Symbol | Meaning | Example |
|--------|---------|---------|
| `+` | one or more occurrences | `\d+` matches 1, 12, 12345 |
| `*` | zero, one, or more occurrences | — |
| `{n}` | exactly n occurrences | `\d{4}` matches 1234 |
| `{n,m}` | between n (min) and m (max) occurrences | `\d{1,3}` matches 1, 12, or 123 |

```python
re.findall("\d+", "h32rb17")     # ['32', '17'] — consecutive digit groups
re.findall("\d*", "h32rb17")     # includes empty strings for non-digit spots
re.findall("\d{2}", "h32rb17 k825t0m c2994eh")   # exact pairs of digits
re.findall("\d{1,3}", "h32rb17 k825t0m c2994eh") # 1-3 digit groups
```

- **Note**: Python scans left-to-right; once a match is found, it continues matching from right after that match ends.

## Constructing a Pattern
- Break the target pattern into smaller components, then combine matching symbols.


- Components needed: username (`\w+`) + colon (`:`) + space (`\s`) + digits (`\d+`)

```python
import re
pattern = "\w+:\s\d+"
employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
print(re.findall(pattern, employee_logins_string))
```

- **Tip**: test regex patterns carefully — they can return unwanted matches or miss intended ones.

## Key Takeaways
- Regex lets you search strings for complex patterns using the `re` module.
- **`re.findall()`** returns all matches as a list.
- Character symbols (`\w`, `\d`, `\s`, `.`) define character types.
- Quantifiers (`+`, `*`, `{n}`, `{n,m}`) define how many repetitions to match.
- Complex patterns are built by combining these symbols piece by piece.