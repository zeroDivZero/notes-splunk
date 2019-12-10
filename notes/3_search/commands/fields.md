# `fields`

Includes/excludes fields from results, can make search faster.

## Include

```
index=web sourcetype=access_combined
| fields status clientip
```

## Exclude

```
index=web sourcetype=access_combined
| fields - status clientip
```

Field extraction is one of most costly operations. Field inclusion occurs before extraction and can improve performance. Exclusion happens after, so no perf benefit (only affects display results).
