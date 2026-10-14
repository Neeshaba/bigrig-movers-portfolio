# BigRig Movers — Database Development

An Oracle SQL coursework project modelling the operations of a transport and removals business. The project covers relational schema design, sample data, data manipulation, schema evolution, business reporting, and the generation of nested JSON documents.

This README provides a high-level overview of Tasks 1–6 without reproducing assessment answers or personal identifiers. Descriptions are based on the SQL files reviewed in the separate private project repository.

## Business context

The database represents customer quotes, transport jobs, employees, truck–trailer combinations, and vehicle maintenance. Quotes connect customers with dispatchers; jobs connect quotes with scheduling employees, drivers, and vehicle combinations. Maintenance records link trucks, service events, task types, and employees.

## Technology

- **Oracle SQL:** table definitions, constraints, sequences, inserts, updates, deletes, and reporting queries.
- **Oracle SQL/JSON:** `JSON_OBJECT` and `JSON_ARRAYAGG` for customer-oriented documents.
- **SQL client commands:** output settings and table descriptions used alongside SQL statements.

The reviewed source demonstrates JSON generation in Oracle. No MongoDB import or query script was available for verification.

## Tasks 1–6

| Task | Focus | Work represented in the project files |
| --- | --- | --- |
| **1** | Relational schema and integrity | Defines employee, quote, and job tables with column documentation, primary keys, required fields, role and payment checks, and foreign keys. Includes an employee-to-manager relationship and a composite reference to a truck–trailer combination. |
| **2** | Sample data | Populates employee, quote, and job records with sample operational scenarios, including employee roles, reporting relationships, repeat customer quotes, vehicle assignments, payment states, and quoted versus actual costs. |
| **3** | Data manipulation | Creates sequences for record identifiers; adds an employee and related quote/job records using lookup subqueries; changes scheduling and cost information; and removes related records in an order that respects foreign keys. |
| **4** | Schema extensions | Adds quote assignment status and a reason field, initialises status from existing jobs, and introduces service task types, truck service events, and individual service tasks. |
| **5** | Business reporting | Reports on customers with multiple quotes and above-average quoted costs, employee roles and management relationships, dispatcher workload, and truck–trailer utilisation. Uses joins, subqueries, aggregation, conditional expressions, and formatted output. |
| **6** | Relational data to JSON | Generates a document per customer containing customer information, quote and job counts, paid and unpaid cost totals, and a nested quote history. Handles absent jobs and falls back to quoted cost when an actual job cost is not supplied. |

## Skills demonstrated

- Translating operational relationships into a relational data model.
- Applying primary, foreign, composite, and self-referencing keys.
- Managing related records with sequences and lookup queries.
- Extending a schema as business requirements evolve.
- Turning reporting requirements into SQL queries.
- Representing relational records as nested JSON documents.

## Project context

Developed as university coursework. This documentation summarises the project scope and techniques; it does not establish authorship of every source component or permission to redistribute assessment material. Publication of source code and any third-party contributions remains subject to the applicable permissions.

## Publication scope

This repository contains documentation only. Assessment solutions, credentials, personal identifiers, and full project files are excluded.
