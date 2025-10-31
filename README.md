# relational_modeling_sql
Designed a normalized relational schema for companies, places, and CEOs with PostgreSQL
Relational Modeling & SQL Analytics (PostgreSQL)

Overview:
I designed a normalized relational schema for companies, places, and CEOs; loaded data with referential integrity; and wrote analytical SQL to answer business-style questions (ages of companies, CEO tenure filters, HQ rollups). This demonstrates schema design, join reasoning, and window-free analytical querying in PostgreSQL. 

Process:
-Schema design: Created 5 tables—countries, states, cities, ceos, companies—with foreign keys and constraints (e.g., year checks).
-Data load with subqueries: Inserted geographic and entity data using SELECT-based foreign-key lookups to guarantee integrity.
-Analytical queries:
Company age given a CEO’s birth state (e.g., Tennessee) using joins across CEO→birth city→state.
CEOs of companies founded in the USA before 1965.
CEOs younger than 60 (on a reference year).
HQ city/state/country of the company whose CEO was born in India (LEFT JOIN on HQ state for global cities).
Companies with CEOs starting after 2014.
Ergonomics & correctness: Applied COALESCE for global HQs without states; kept query output tidy for downstream reporting.
-Skills: PostgreSQL DDL/constraints, relational modeling, multi-table joins, analytical SQL patterns.
