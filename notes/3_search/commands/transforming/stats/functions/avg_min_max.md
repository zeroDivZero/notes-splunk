# `avg`, `min`, `max`

Average, minimum, and maximum. Only work if field has numeric value.

```
index=sales sourcetype=vendor_sales
| stats avg(sale_price) as "Average Price",
min(sale_price) as "Min Price",
max(sale_price) as "Max Price" by categoryId
```

Missing or misformatted values not added to calculation.
