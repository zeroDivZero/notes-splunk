# `dedup`

Removes events with duplicated values.

```
index=security sourcetype=history* Address_Description="San Francisco"
| dedup Username
| table Username, First_Name, Last_Name
```

_Or_ combination of fields:

`| dedup First_Name Last_Name`
