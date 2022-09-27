# awk for create unique data file in linux


Example:

    awk 'BEGIN {OFS=","} {print $0,NR-1FILENAME}' dm_transaction.txt > dm_transaction_unique.txt

* {OFS=","} = "delimiter"
* dm_transaction.txt = "data file before changing"
* dm_transaction_unique.txt = "data file after changing"
* print $0 = "print unique from the beginning"
