## Learning Goals
- Retrieving data from multiple data sources
    - SQL databases
    - NoSQL databases
    - APIs
    - Cloud data sources
- Understand common issues that arise with importing data

## Reading CSV Files
**Comma-separated values** (CSV) files consists of rows of data, separated by commas.

In Pandas, CSV files can typically be read using just a few lines of code:

```
import pandas as pd
filepath = 'data/iris_data.csv'

# Import the data
data = pd.read_csv(filepath)

# Print a few rows
print(data.iloc[:5])
```

**Output**

| | sepal_length | sepal_width | petal_length | petal_width | species |
| --- | --- | --- | --- | --- | --- |
| 0 | 5.1 | 3.5 | 1.4 | 0.2 | lrish-setosa |
| 1 | 4.9 | 3.0 | 1.4 | 0.2 | lrish-setosa |
| 2 | 4.7 | 3.2 | 1.3 | 0.2 | lrish-setosa |
| 3 | 4.6 | 3.1 | 1.5 | 0.2 | lrish-setosa |
| 4 | 5.0 | 3.6 | 1.4 | 0.2 | lrish-setosa |

**Reading CSV Files: Useful Arguments**

```
# Different delimiters - tab-separated file (.tsv)
data = pd.read_csv(filepath, sep='\t')

# Different delimiters - space-separated file:
data = pd.read_csv(filepath, delim_whitespace = True)

# Don't use first row for column names
data = pd.read_csv(filepath, header = None)

# Specify column names
data = pd.read_csv(filepath, names=['Name1', 'Name2'])

# Custom mising values
data = pd.read_csv(filepath, na_values=['NA', 99])
```

## JSON Files
**JavaScript Object Notation** (JSON) files are a standard way to store data across platforms.

JSON files are very similar in structure to Python dictionaries.

Reading JSON files into Python:

```
# Read JSON file are dataframe
data = pd.read_json(filepath)

# Write dataframe file to JSON
data.to_json('outputfile.json')
```

**Example**
```
[
    {
        "id": 7267,
        "name": "10pin Bowling Lounge",
        "address": 330 N State Street",
        "city": "Chicago / Illinois",
        "postal_code": "60610",
        "country": "US",
        "phone": 3126440300x",
        "lat": 41.888624,
        "lng": -87.628091,
        "price" 4
    }
]
```