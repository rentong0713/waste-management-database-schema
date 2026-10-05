# Waste Management Database Schema — Clear Away

This repository contains the complete relational database design and SQL schema for **Clear Away**, a municipal waste collection and logistics management system.

The project demonstrates the full database development lifecycle, progressing from **conceptual entity-relationship modeling** to the generation of **Oracle 12c Data Definition Language (DDL)** scripts.

## Technologies Used

* **Modeling Tool:** Oracle SQL Developer Data Modeler
* **Database Management System:** Oracle Database 12c
* **Language:** SQL (DDL)

## Technical Highlights & Methodology

### Data Normalization

Systematically normalized data structures from **Unnormalized Form (UNF) to Third Normal Form (3NF)**, identifying and eliminating partial and transitive dependencies to ensure data integrity.

### Entity-Relationship Modeling

Engineered comprehensive conceptual and logical models using **Information Engineering (Crow's Foot) notation**, explicitly defining minimum and maximum cardinalities and distinguishing between identifying and non-identifying relationships.

### Strategic Key Management

Implemented **surrogate keys**, such as:

* `global_street_id`
* `property_id`
* `ctwaste_id`

These keys prevent composite key bloat in child tables and help resolve diamond inheritance conflicts.

Original composite business keys were preserved using **UNIQUE constraints** to enforce business rules without compromising referential efficiency.

### Schema Generation & Constraint Enforcement

Generated robust DDL SQL scripts defining:

* Tables
* Primary keys
* Foreign keys
* `CHECK` constraints
* Attribute-level business rules

For example, `CHECK` constraints are used to:

* Restrict bin overweight status to `'Y'` / `'N'`
* Limit local authority types to classifications such as `'City'` or `'Shire'`

## Repository Contents

| File                   | Description                                                                                                                                 |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `ca_schema.sql`        | Finalized Oracle 12c DDL script containing table creation, constraints, and commenting statements.                                          |
| `ca_conceptual.pdf`    | Conceptual entity-relationship diagram covering local authorities, properties, bins, waste types, collection runs, and other core entities. |
| `ca_logical.pdf`       | Detailed logical schema showing attributes, data types, primary/foreign keys, and relational mappings.                                      |
| `ca_normalisation.pdf` | Step_                                                                                                                                       |
