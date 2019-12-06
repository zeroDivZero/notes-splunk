# BEST PRACTICES

Filter by time is most effective.

After that, filter by `index`, `source`, `host`, `sourcetype`.

Apply filtering commands as early as possible in search to limit events for future manipulation.

## Time

Use abbreviations to specify time range to search. `30s`, `30m`, `30h`, `30d`, `30w`, `30mon`, `30y`.

`@` to round down to nearest unit. `-30m@h: 9:37 -> 9:00`.

In search string, to specify range: `earliest=-2h latest=-1h`. Can also use absolute values (`01/08/2109:12:00:00`).

## Index

`index=web`, `index=web OR index=security`, `index=ma*`.
