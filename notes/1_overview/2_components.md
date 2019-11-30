# COMPONENTS

## Indexer

Processes incoming machine data and stores results in indexes as events. Saves files in directories organized by age. Need timeframe to search.

## Search Head

Allows user to use search language to search indexed data. Distributes query request to indexers, which perform actual search. Then consolidates and enriches results to present to user. Also provides tools like dashboards, reports, and visualizations.

## Forwarder

Enterprise instance that consumes data and forwards to indexer for processing. Requires minimal resources, has limited impact on performance. Usually resides on machines where data originates. E.g., install forwarder on web server to forward data to indexer.

In most Splunk deployments, serves as primary way to supply data for indexing.
