# `list`

Lists all values of field.

Ex: List all company assets given to each employee.

```
index=bcgassets sourcetype=asset_list
| stats list(Asset) as "company assets" by Employee
```
