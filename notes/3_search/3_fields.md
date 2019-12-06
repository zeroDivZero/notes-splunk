# FIELDS

To left of event list (search results) are selected and interesting fields (have values in >= 20% of events).

Letter `a` next to field name means string value. `#` denotes numeral.

Click on field to see more details, like values and distributions. Can add to selected fields list. Click on one of quick reports to perform transforming search and display results as stats.

## Search

Use this format to limit search by field value:

`<field name>=<value>`

E.g., `sourcetype=linux_secure`. Field name is case-sensitive, value is not.

Operators `=`, `!=` apply to string and numerical values. `>`, `>=`, `<`, `<=` apply only to numerical values. Can also use wildcard and boolean operators.

Can add to search directly by clicking on value in field details window.

Instead of chaining multiple boolean operators, can use `IN` operator. E.g., instead of `status=500 OR status=503 OR status=505`, do `status IN (500, 503, 505)`.
