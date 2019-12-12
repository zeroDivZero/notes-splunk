# `sum`

Sum of numeric values in field.

```
index=sales sourcetype=vendor_sales
| stats sum(price) as "Gross Sales" by product_name
```

`stats` can have multiple functions, but should be in same pipe:

```
| stats count as "Unit Sold"
sum(price) as "Gross Sales"
by product_name
```
