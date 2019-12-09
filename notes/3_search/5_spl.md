# SPL (SPLUNK SEARCH LANGUAGE)

Each search consists of 5 parts:

1. Search terms
2. Commands - what to do with search results (charts, stats, formatting, etc.)
3. Functions - how to chart, computer, eval results
4. Arguments - variables to apply to functions
5. Clauses - how results grouped or defined

Example:

`sourcetype=acc* status=200 | stats list(product_name) as "Games Sold" | top "Games`

* `sourcetype=acc* status=200` is search terms.
* `stats` is command.
* `list` is function.
* `product_name` is argument.
* `as` is clause.

Components are separated by pipes (`|`), which passes current result to next.

`Cmd+\` to move each pipe to new line, for easier reading.

In Splunk bar select **user name > Preferences > SPL Editor** to change SPL editing tool settings.

Piping can further limit search results. Hence, not all results available to next (right) component.

## Command `fields`

Includes/excludes fields from results, can make search faster.

### Include

```
index=web sourcetype=access_combined
| fields status clientip
```

### Exclude

```
index=web sourcetype=access_combined
| fields - status clientip
```

Field extraction is one of most costly operations. Field inclusion occurs before extraction and can improve performance. Exclusion happens after, so no perf benefit (only affects display results).

## Command `table`

Similar to `fields`, keeps specified fields in results, but shows them in tabulated format (each row is event).

```
index=web sourcetype=access* status=200 product_name=*
| table JSESSONID product_name price
```

Order of args is order of columns.

## Command `rename`

Renames field.

```
index=web sourcetype=access* status=200 product_name=*
| table JSESSONID, product_name, price
| rename JSESSONID as "User Session" product_name as "Purchased Game" price as "Purchase Price"
```

If renamed, original name no longer available to subsequent commands.

## Command `dedup`

Removes events with duplicated values.

```
index=security sourcetype=history* Address_Description="San Francisco"
| dedup Username
| table Username, First_Name, Last_Name
```

_Or_ combination of fields:

`| dedup First_Name Last_Name`

## Command `sort`

Displays results in ascending or descending order.

```
sourcetype=vendor_sales
| table Vendor product_name sale_price
| sort Vendor product_name
```

Default is ascending order. `sort price` is same as `sort + price`. Use `sort -price` for descending order. If there's space between `-` and first field, descending order applied to all fields. Remove space to apply only to that field.

To limit number of results:

`| sort -sale_price Vendor limit=20`
