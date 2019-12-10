# SPL (SPLUNK SEARCH LANGUAGE)

Each search consists of 5 parts:

1. Search terms
2. Commands - what to do with search results (charts, stats, formatting, etc.)
3. Functions - how to chart, compute, eval results
4. Arguments - variables to apply to functions
5. Clauses - how results are grouped or defined

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
