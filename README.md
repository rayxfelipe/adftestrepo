# adftestrepo

## Fiscal paginated report export

`pl_export_paginated_report_csv` exports the Power BI paginated report
`Fiscal Transactions Sample` as CSV and writes the rendered output to:

`acctdatalakedemo001/fiscal/paginated-reports/fiscal-transactions/`

The pipeline is stored in the ADF folder `FisCAL`. It retrieves the dedicated
Power BI automation application's client ID and secret from
`kv-pbi-exp-rayf-001`, starts and polls the asynchronous Power BI export, and
copies the completed CSV to ADLS Gen2 without transforming it.

The Power BI tenant must allow service principals to use Power BI APIs, and the
application `adf-pbi-paginated-export-demo` must have access to the `Fiscal`
workspace before the pipeline can run successfully.
