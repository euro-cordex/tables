# Tables
This repository contains machine readable cordex tables with data and meta information.
To read one of the tables, e.g., into python, you can simply use the public raw adress, e.g.:

```python
import pandas as pd
url = "https://raw.githubusercontent.com/euro-cordex/tables/master/domains/cordex.csv"
table = pd.read_csv(url)
```

## Data Request

A table with some meta information about the Cordex data request.


## Domains

Contains tables with cordex domains and definitions in rotated coordinates.

## ESGF

A table of Cordex Simulations currently available in the ESGF. This table should be updated
regularly soon.
