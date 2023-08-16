## Learning Goals
- Why data cleaning is important for Machine Learning
- Issues that arise with messy data
- How to identify duplicate or unnecessary data
- Policies for dealing with outliers

## Why is Data Cleaning is so important?
Decisions and analytics are increasingly driven by data and models.

Key aspects of Machine Learning Workflow depend on cleaned data:

- **Observations:** An instance of the data (usually a point or row in a dataset)
- **Labels:** Output variable(s) being predicted
- **Algorithms:** Computer programs that estimate models based on available data
- **Features:** Information we have for each observation (variables)
- **Model:** Hypothesized relationship between observations and data

Messy data can lead to "garbage-in, garbage-out" effect, and unreliable outcomes.

**The main data problem companies face:**
- Lack of data
- Too much data
- Bad data

Having data ready for ML and AI ensures you are ready to infuse AI across your organization.

## How can data be messy?

- Duplicate or unnecessary data
- Inconsistent text and typos
- Missing data
- Outliers
- Data sourcing issues:
    - Multiple systems
    - Different database types
    - On premises, in cloud
- ... and more.

## Duplicate or Unnecessary Data
Pay attention to **duplicate data** and research why there are multiple values.

It is a good idea to look at the features you're bringing in and **filter** the data as neccessary (be careful not to filter too much if you may use features later).