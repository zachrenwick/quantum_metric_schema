# Quantum Metric Schema Tree

Interactive collapsible tree visualization of the BigQuery schema for `quantummetrics_prd.sessions_archive`.

## Usage

Open `quantum_metric_schema.html` directly in a browser (`file://` or served via HTTP). No build step required.

- **Click** a node to expand/collapse
- **Scroll** to zoom
- **Drag** to pan
- **Right-click** to reset view

## Details

- 297 fields, max nesting depth 4
- Built with [ECharts](https://echarts.apache.org/) (CDN)
- Self-contained — schema data is embedded in the HTML

## Refreshing the Schema

1. Query BigQuery table metadata using the MCP BigQuery tool (`get_table_info`) or `bq show`.
2. Transform fields into `{ name: "field_name (TYPE)", children: [...] }` format.
3. Replace the `SCHEMA_DATA` constant in the HTML file.
