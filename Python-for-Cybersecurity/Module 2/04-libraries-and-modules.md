# Python Libraries & Modules 

## Recap: Modules vs. Libraries
- **Module**: a Python file containing functions, variables, classes, and other runnable code.
- **Library**: a collection of modules providing reusable code.

## The Python Standard Library
- Extensive collection of pre-built Python code, usually packaged with Python itself.
- Previously covered modules:
  - **re** – searching for patterns in log files
  - **csv** – working with `.csv` files
  - **glob** and **os** – interacting with the command line
  - **time** and **datetime** – working with timestamps

### New Module: `statistics`
- Provides functions for calculating statistics on numeric data.
- **`mean()`** – calculates the average.
- **`median()`** – calculates the middle value.

## Importing Modules

### Importing an Entire Module
- Use the **`import`** keyword followed by the module name.
- Must prefix function calls with the module name + a period (`.`).

```python
import statistics

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]

mean_failed_attempts = statistics.mean(monthly_failed_attempts)
print("mean:", mean_failed_attempts)   # 35.25

median_failed_attempts = statistics.median(monthly_failed_attempts)
print("median:", median_failed_attempts)   # 20.5
```

### Importing Specific Functions
- Use **`from module import function`** syntax.
- Multiple functions can be imported by separating with commas.
- No need to prefix the module name when calling the function.

```python
from statistics import mean, median

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]

mean_failed_attempts = mean(monthly_failed_attempts)
print("mean:", mean_failed_attempts)

median_failed_attempts = median(monthly_failed_attempts)
print("median:", median_failed_attempts)
```

## External Libraries
- Libraries outside the Python Standard Library must be **installed** before use.
- Examples: **Beautiful Soup (bs4)** – parsing HTML; **NumPy (numpy)** – arrays and math computations.

### Installing a Library (in Jupyter Notebook / Google Colab)
```python
%pip install numpy
```

### Importing After Installation
```python
import numpy
```

## Key Takeaways
- Python Standard Library modules (`re`, `csv`, `os`, `glob`, `time`, `datetime`, `statistics`) are imported using `import`.
- Two import styles:
  - **Full module import** → must prefix functions with module name (`statistics.mean()`)
  - **Specific function import** → no prefix needed (`mean()`)
- External libraries need installation (e.g., `%pip install`) before importing.