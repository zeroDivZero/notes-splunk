# `rename`

Renames field.

```
index=web sourcetype=access* status=200 product_name=*
| table JSESSONID product_name price
| rename JSESSONID as "User Session" product_name as "Purchased Game" price as "Purchase Price"
```

If renamed, original name no longer available to subsequent commands.
