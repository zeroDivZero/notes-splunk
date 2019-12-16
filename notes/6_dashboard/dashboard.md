# DASHBOARD

Collection of reports.

Start with search. Create chart panel. **Save As > Dashboard Panel**. Fill out options and save.

Continue to create panels, but to add to previously created dashboard, instead of creating new, choose existing one.

All dashboards accessible from **Dashboards** menu. When viewing dashboard, can **Edit** to drag top bars of panels around for better layout. Can also edit XML src, add panel, add input (such as time range picker), select dark theme, etc.

Can change settings per panel.

## Time Range Picker

**Edit > Add Input > Time**. Can enable **Search on Change**. Provide token to connect to panel. Only works on panel with inline search.

**Inline search:** Instead of referencing saved search with search ref, SPL search string is imbedded inside dashboard XML.

If panel does not have inline search, can only **View report** and not **Edit search**. Tap **View report** button and choose **Clone to inline**. To tie time range picker to panel's search, tap **Edit search** and for **Time Range** select picker (look for token entered earlier). Repeat for all panels to be driven by picker.
