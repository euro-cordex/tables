# Tables
This repository contains machine readable cordex tables with data and meta information.
To read one of the tables, e.g., into python, you can simply use the public raw adress, e.g.:

```python
import pandas as pd
url = "https://raw.githubusercontent.com/euro-cordex/tables/master/domains/cordex.csv"
table = pd.read_csv(url)
```

## Data Request

A table with some meta information about the Cordex data request. It's an attempt to clean up and convert the [variable list](https://github.com/IS-ENES-Data/cordex/blob/master/CORDEX_standard_output.xls) into a machine readable format.


## Domains

Contains tables with cordex domains and definitions in rotated coordinates. The data is mostly based on the [Cordex archive specifications](https://is-enes-data.github.io/cordex_archive_specifications.pdf).
