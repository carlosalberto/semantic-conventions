<!--- Hugo front matter used to generate the website version of this page:
linkTitle: SDK
--->

# Semantic Conventions for SDK Metrics

**Status**: [Experimental][DocumentStatus]

This document describes instruments and attributes for common SDK level
metrics in OpenTelemetry. Consider the [general metric semantic
conventions](README.md#general-metric-semantic-conventions) when creating
instruments not explicitly defined in the specification.

<!-- Re-generate TOC with `markdown-toc --no-first-h1 -i` -->

<!-- semconv metric.otel.exporter.spans(metric_table) -->
| Name     | Instrument Type | Unit (UCUM) | Description    |
| -------- | --------------- | ----------- | -------------- |
| `otel.exporter.spans` | Counter | `{span}` | Measures the number of exported Spans. |
<!-- endsemconv -->

<!-- semconv metric.otel.exporter.spans(full) -->
| Attribute  | Type | Description  | Examples  | Requirement Level |
|---|---|---|---|---|
| `exporter.dropped` | boolean | Whether the Span was dropped or not. [1] |  | Required |
| `exporter.type` | string | Type of exporter being used. | `OtlpGrpcSpanExporter` | Recommended |

**[1]:** Spans may be dropped in case of failed ingestion, e.g. network problem or the exported endpoint being down.
<!-- endsemconv -->
