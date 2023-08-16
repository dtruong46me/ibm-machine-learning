## SQL Databases
**Structure Query Language** (SQL) represents a set of relational databases with fixed schemas.

There are many types of SQL databases, which function similarly (with some subtle differences in syntax)

Examples of SQL databases:
- Microsoft SQL Server
- Postgres
- MySQL
- AWS Redshift
- Oracle DB
- Db2 Family

**Reading SQL Data**
```
# SQL Data Imports
import sqlite3 as sq3
import pandas as pd

# Initialize path to SQLite database
path = 'data/clasic_rock.db'

# Create connection SQL database
conn = sq3.Connection(path)

# Write query
query = '''
    SELECT * FROM rock_songs;
'''

# Execute query
data = pd.read_sql(query, conn)
```

## NoSQL Databases
**Not-only SQL** (NoSQL) databases are not relational, vary more in structure.

Depending on application, may perform more quickly or reduce technical overhead

Most NoSQL databases store data in **JSON format**

Examples of NoSQL databases:
- **Document databases:** mongoDB, couchDB
- **Key-value stores:** Riak, Voldemort, Redis
- **Graph databases:** Neo4j, HyperGraph
- **Wide-column stores**: Cassandra, HBase

**Reading NoSQL Data**
```
# SQL Data Imports
from pymongo import MongoClient

# Create a Mongo Connection
conn = MongoClient()

# Choose database (conn.list_database_name() will display available database)
db = conn.database_name

# Create a cursor object using a query
cursor = db.collection_name.find(query)

# Expand cursor and construct DataFrame
df = pd.DataFrame(list(cursor))
```

**Explanation**
- This example uses the **pymongo** module to read files stored in **MongoDB**, although there are several other packages available.
- We first make a connection with the database (MongoDB needs to be running).
- Data is read into pandas by combining a query with this connection.
- Here, query should be replaced with a MongoDB query string (or {} to be select all).

## APIs and Cloud Data Access

```
# UCI Cars dataset - url location
data_url = 'http://archive.ics.uci.edu/ml/machine-learning-databases/author/imports-85.data'

# Read data into Pandas
df = pd.read_csv(data_url, header = None)
```