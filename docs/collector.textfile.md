# textfile collector

The textfile collector exposes metrics from files written by other processes.

Metric name prefix | `textfile`
Classes             | None
Enabled by default? | Yes

## Flags

### `--collector.textfile.directory`

The directory containing the files to be ingested.

Default value: `C:\Program Files\wmi_exporter\textfile_inputs`

Required: No

Only files with the suffix .prom will be ingested.

Example:

```
C:\Program Files\wmi_exporter\textfile_inputs\my_metricfile.prom
```

## Metrics

Metrics will primarily come from the files on disk. The below listed metrics
are collected to give information about the reading of the metrics themselves.

Name | Description | Type | Labels
-----|-------------|------|-------
`wmi_textfile_scrape_error` | 1 if there was an error opening or reading a file, 0 otherwise | gauge | None
`wmi_textfile_mtime_seconds` | Unix epoch-formatted mtime (modified time) of textfiles successfully read | gauge | file

### Example metric

You can put your own metrics into a .prom file, and use the normal metric convention as seen in http://<servername>:9182/metrics.

```
my_own_metric 55
my_own_other_metric{my_number="0",mode="mode1"} 123
```

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
