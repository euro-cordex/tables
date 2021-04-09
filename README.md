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

Contains tables with cordex domains and definitions in rotated coordinates.

## ESGF

[![pipeline status](http://git.gerics.de/Lars.Buntemeyer/schedule-test/badges/master/pipeline.svg)](http://git.gerics.de/Lars.Buntemeyer/schedule-test/commits/master)

A table of Cordex Simulations currently available in the ESGF. This table is now updated
nightly! You can convert this table into a more convenient (humand readable) format using, e.g.


```python
import pandas as pd

url = "https://raw.githubusercontent.com/euro-cordex/tables/master/esgf/euro-cordex-esgf.csv"
df = pd.read_csv(url)

# group the data to have a more readable layout.
cordex_table = df.groupby(['institute', 'model_id', 'driving_model_id', 'experiment_id', 'member', 'frequency', 'domain'])['variable'].apply(list)

# write the table to excel
cordex_table.to_excel('cordex.xlsx')
```

A formatted table in `xlsx` format is also updated nightly [here](https://raw.githubusercontent.com/euro-cordex/tables/master/esgf/euro-cordex-esgf.xlsx)
