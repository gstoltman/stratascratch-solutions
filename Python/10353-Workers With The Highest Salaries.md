## Find the titles of workers that earn the highest salary. Output the highest-paid title or multiple titles that share the highest salary.

```
# Import your libraries
import pandas as pd

# Start writing code
top = worker['salary'].sort_values(ascending=False).reset_index(drop=True)[0]

merged = worker.merge(title, left_on='worker_id', right_on='worker_ref_id')

merged['worker_title'][merged['salary'] == top]
```
