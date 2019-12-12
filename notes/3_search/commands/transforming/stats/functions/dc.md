# `dc`

Distinct (unique) count of values in search results. Clauses same as those of `count`.

```
index=sales sourcetype=vendor_sales
| stats distinct_count(product_name) as "Number of games for sale by vendors" by sale_price
```

`distinct_count` and `dc` are interchangeable.
