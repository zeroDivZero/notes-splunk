# `count`

number of events matching search criteria

`as`-clause changes count column name.
`by`-clause returns count for each value of named field(s).

```
index=sales sourcetype=vendor_sales
| stats count as "Total Sells by Vendors"
by product_name, categoryId, sale_price
```

Pass field name to `count` as arg to count only events that have that field:

```
index=web sourcetype=access_combined
| stats count(action) as "Action Events", count as "Total Events"
```
