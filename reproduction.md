# Reproduction in Roundup

## From data_exploration.ipynb

This script has a simple joining, combining data from two tables: `awards_by_school_16_clean.csv` and `amount_by_school_16_clean.csv`. The former contains the number of vouchers awarded to each school in 2016, while the latter contains the total amount of money awarded to each school in 2016. By joining these two tables on the school number, we can create a new table that shows both the number of vouchers and the total amount awarded to each school in 2016. In the original specification, the user does an outer join, but in Roundup we see that the set of unique values in both join keys is equal.

### In Roundup

1. Load tables `awards_by_school_16_clean.csv` and `amount_by_school_16_clean.csv` into Roundup.
2. Create a pack operation with these two tables: join on `School No` and `School No.`, on equality.
3. Export the intersection of these tables as `awards_and_amount_by_school_16.csv` for further visualization and analysis.
