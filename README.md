# notes-splunk

Notes on Splunk, a web platform for searching, monitoring, and analyzing machine-generated big data.

## Overview

1. [Functions](./notes/1_overview/1_functions.md)
2. [Components](./notes/1_overview/2_components.md)
3. [Deployment](./notes/1_overview/3_deployment.md)
4. [App](./notes/1_overview/4_app.md)
5. [Roles](./notes/1_overview/5_roles.md)

## Data

1. [Add](./notes/2_data/1_add.md)

## Search

1. [UI](./notes/3_search/1_ui.md)
2. [Basics](./notes/3_search/2_basics.md)
3. [Fields](./notes/3_search/3_fields.md)
4. [Best Practices](./notes/3_search/4_best_practices.md)
5. [SPL](./notes/3_search/5_spl.md)

### Commands

* [`fields`](./notes/3_search/commands/fields.md)
* [`table`](./notes/3_search/commands/table.md)
* [`sort`](./notes/3_search/commands/sort.md)
* [`dedup`](./notes/3_search/commands/dedup.md)
* [`rename`](./notes/3_search/commands/rename.md)

#### Transforming

[Basics](./notes/3_search/commands/transforming/1_basics.md)

* [`top`](./notes/3_search/commands/transforming/top.md)
* [`rare`](./notes/3_search/commands/transforming/rare.md)
* [`stats`](./notes/3_search/commands/transforming/stats/stats.md)
  * Functions
  * [`count`](./notes/3_search/commands/transforming/stats/functions/count.md)
  * [`dc` (`distinct_count`)](./notes/3_search/commands/transforming/stats/functions/dc.md)
  * [`sum`](./notes/3_search/commands/transforming/stats/functions/sum.md)
  * [`avg`, `min`, `max`](./notes/3_search/commands/transforming/stats/functions/avg_min_max.md)
  * [`list`](./notes/3_search/commands/transforming/stats/functions/list.md)
  * [`values`](./notes/3_search/commands/transforming/stats/functions/values.md)
