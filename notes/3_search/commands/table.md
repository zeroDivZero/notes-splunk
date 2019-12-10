# `table`

Similar to `fields`, keeps specified fields in results, but shows them in tabulated format (each row is event).

```
index=web sourcetype=access* status=200 product_name=*
| table JSESSONID product_name price
```

Order of args is order of columns.
