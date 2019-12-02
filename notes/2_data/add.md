# ADD DATA

Before searching, need to add data. Only admin allowed. Use **Add Data** icon in Home app, or use **Settings** menu.

## Source

Choose one of popular data sources at top of page. Or, for custom data, go to bottom of page and choose to upload files, monitor, or use forwarder.

### Upload

Upload files from local computer. Only indexed once. Good for testing, or data that never gets updated.

### Monitor

Monitor files & directories, http events, network ports, or data-gathering scripts. Can continuously monitor, or just once.

### Forward

Receive data from external forwarder.

## Source Type

If Splunk recognizes data, will assign pretrained source type. Can create custom ones. Can adjust settings like timestamp and delimiter.

When saving custom type, need to select App context, which tells Splunk which app to apply source type to. Choose `system` for system-wide availability.

## Input Settings

### Host

Specify **Host field value** as constant, regex, or segment.

### Index

Choose index (timestamped directories) to store data. Tendency is to use default **Main Index**. Advantages of using separate indexes:

1. Search is more efficient (limits search space).
2. Easier to control who can see what data.
3. Each index can have own retention policy (how long to keep data).
