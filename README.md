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
regularly soon. You can convert this table into a more convenient (humand readable) format using, e.g.


```python
import pandas as pd

url = "https://raw.githubusercontent.com/euro-cordex/tables/master/esgf/euro-cordex-esgf.csv"
df = pd.read_csv(url)

# group the data to have a more readable layout.
cordex_table = df.groupby(['institute', 'model_id', 'driving_model_id', 'experiment_id', 'member', 'frequency', 'domain'])['variable'].apply(list)

# write the table to excel
cordex_list.to_excel('cordex.xlsx')
```
