# `top`

Finds most common values of given field.

Ex: Find vendors with most sales:

```
index=sales sourcetype=vendor_sales
| top Vendor
```

Displays top 10 by default. Add `limit=X` to change. `limit=0` to get all.

Can use over multiple fields:

```
| top Vendor product_name
```

Besides `limit`, there are other useful clauses.

Change names of count and percent column headers:

```
countfield=string
percentfield=string
```

Show count or percent:

```
showcount=true/false
showperc=true/false
```

Show all others not in limit as single row at bottom:

```
useother=true/false
otherstr=string
```

Ex:

```
| top Vendor limit=5 showperc=False countfield="Number of Sales" useother=true
```

Show top 3 products by each vendor:

```
| top product_name by Vendor limit=3
```
