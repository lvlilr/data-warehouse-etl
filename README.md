# Data Warehouse and ETL Implementation

Collaborative academic Oracle SQL/PLSQL source: OE orders/customers → staging and transformations → four dimensions → order fact table → analytical queries. Includes uppercasing order modes, handling missing IDs, customer turnover tiers and date dimensions.

## Structure and execution
`original/CODE_SQL.sql` contains the historical source. Requires Oracle SQL/PLSQL and permitted OE source tables in a disposable, isolated schema. No OE export, customer records, credentials or database is included. Review the DROP statements and run reviewed blocks only after preparing that schema. Do not run this historical script against an existing shared or production schema.

## Results and verification
Historical report screenshots describe 105 order rows, 319 customer classifications, total order amount 3,668,054.7, 80 orders above 5,000 and 51.9% direct-channel share of sales amount. They are not independently reproduced Oracle results. No Oracle service or original source export was available for a rerun.

## Limitations
Historical source contains unguarded DROP statements, lacks fact foreign keys and has locale-sensitive date semantics. The reported currency conversion is not fully represented in the supplied code. The 51.9% measure is amount share, not order share. The repository preserves these limitations rather than presenting a production-ready warehouse.

## Attribution and publication status
This is collaborative academic work. Teammate publication permission is candidate-confirmed; team authorship is retained. Any `codex_improvements/` implementation is a later Codex-assisted reproduction or improvement. Repository preparation and README editing are also Codex-assisted. Original outcomes are not presented as newly executed tests.

## Rights and dependencies
No project license is assigned. Rights remain with the respective authors; no permission to reuse is granted by this README. Dependency licenses remain separate. No datasets, private reports, credentials or original Git history are included. Install dependencies from their declared files rather than uploading dependency bundles.
