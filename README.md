# Farm Sustainability SQL Database

A relational SQL database project for modelling farm sustainability, crop production, soil health, resource applications, and environmental impact.

The project uses a normalised relational schema with primary keys, foreign keys, constraints, indexes, joins, aggregate queries, and a reusable view for analysing sustainability-related farm records.

## Project Overview

The database separates the main business concepts into related tables:

- farms
- crops
- soil health records
- resource types
- sustainability initiatives
- farm-crop production records
- resource applications

The central table is `FarmCrop`, which represents a crop grown on a farm during a specific planting and harvest period. Resource applications are linked to this table so that water, fertilizer, and energy use can be analysed in context.

## Repository Contents

- `farm_sustainability.sql` - SQL implementation for the relational database.
- `farm-sustainability-database-report.pdf` - design report covering the schema, normalisation decisions, SQL implementation, and design trade-offs.

## Main Features

- Normalised relational database design
- Entity-relationship modelling
- Primary key and foreign key constraints
- Named constraints and referential actions
- Data validation using `CHECK` constraints
- Indexes for common relationship and lookup paths
- Reusable SQL view for joined sustainability profiles
- Aggregate queries for energy use and environmental scoring
- Relational vs document-based design comparison

## How to Run

Open `farm_sustainability.sql` in MySQL or a compatible SQL environment, then run the script from top to bottom.

The script creates the database, defines the schema, inserts sample data, creates the view, and runs validation and analysis queries.

## Example Analysis Areas

The SQL queries can be used to inspect:

- total energy use by farm
- average environmental impact score by farm
- resource applications after harvest dates
- joined farm, crop, soil, resource, and initiative records
- expected row counts across the schema

## Design Focus

The design keeps repeated information out of the main transaction table and avoids storing resource applications directly against farms or crops without context. This makes the schema easier to validate, query, and extend.
