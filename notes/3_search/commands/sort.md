# `sort`

Displays results in ascending or descending order.

```
sourcetype=vendor_sales
| table Vendor product_name sale_price
| sort Vendor product_name
```

Default is ascending order. `sort price` is same as `sort + price`. Use `sort -price` for descending order. If there's space between `-` and first field, descending order applied to all fields. Remove space to apply only to that field.

To limit number of results:

`| sort -sale_price Vendor limit=20`
