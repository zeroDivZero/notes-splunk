# SEARCH UI

**Search & Reporting** app provides default UI for searching and analyzing data. Can create knowledge objs, reports, dashboards, etc.

7 main parts:

1. Top is **Splunk bar**. Used to switch apps, edit account, settings, etc. Appears on every page.
2. Followed by **App bar** for navigating app. Tap **Search** to clear current search.
3. **Search bar** for searches. As text entered, **search assistant** automatically shows contexual matches and syntax docs.
4. To right of search bar is **time picker** to choose time period for search. Limiting search by time is key to faster results.
5. **How to Search** panel has links to docs and tutorial.
6. **What to Search** gives summary of indexed (searchable) data.
7. **Search History** menu allows browsing and rerunning past searches.

## After Search

UI now contains **Save As** menu, result tabs (events, stats, etc.), (job) action buttons, mode selector, and timeline. Events matching query are displayed as list with extracted fields in side bar.

### Save As

Save as knowledge objs.

### Tabs

If query contains stats or visualization commands (called _transforming commands_, since they transform events into tables, charts, etc.), results can be viewed in stats or visualization tab. Otherwise they show instant **Pivot** and doc links.

### Event Sampling

Next to total events display is menu for **Event Sampling**, which returns random set of events.

### Action Buttons

**Job** menu -> **Edit Job Settings:** Save search as job. Can set read permissions and lifetime before save. Access saved jobs in top Splunk bar **Activity** menu.

**Share** button: Share search with others or to bookmark. By default search job remains active for 10 min, but shared job lasts 7 days (others will see exact same results).

### Modes

1. **Fast:** Cuts down info returned. **Field discovery** disabled, only returns default fields or those fulfilling search.
2. **Verbose:** Returns as much data as possible.
3. **Smart (default):** Togggles between other 2 based on search type.

### Timeline

Tap or drag-select interval to investigate only events selected. Or use zoom buttons to zoom in/out. Zooming in uses original job, zooming out triggers new search.

## Event List

Displayed in reverse chronological order, highlighting matching texts.

**Selected fields** (**host**, **source**, **sourcetype**, etc.) displayed underneath each event. Use info button (left of event) to see selected fields, and event and field actions.

Timestamp displayed in user account's timezone.

Hover over text in event to highlight, tap to do contextual search (add, exclude, or new search).

By default events displayed as **List**. Can change to **Raw** or **Table**.
