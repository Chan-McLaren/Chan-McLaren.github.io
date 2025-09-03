---
title: "PostgreSQL"
draft: false
summary: "Database Design for a Movie Rental Company"
---
PostgreSQL Database Design - Movie Rental Company

Leveraging Python and SQLAlchemy to automate a complete data pipeline for a movie rental company. The database is designed to efficiently manage films, inventory, rentals, customers, stores, and payments, with a focus on relational integrity and scalability.

Below is the Entity-Relationship Diagram (ERD) illustrating table relationships, followed by the table schema. The schema demonstrates advanced PostgreSQL concepts including:

- Primary keys and foreign keys to enforce relationships between tables.
- Array types (special_features) and full-text search (tsvector) for flexible data storage and querying.
- Default values and constraints to maintain data consistency.
- Timestamps for tracking updates (last_update) and data creation (create_date).

The database supports queries and analyses across multiple entities, allowing operations such as:
- Tracking film inventory across stores and rentals.
- Calculating rental statistics and payment totals.
- Associating customers with stores and addresses for targeted operations.
- Performing complex queries involving full-text search and aggregation.

![Movie Rental ERD](../static/images/MovieRentalERD.png)
{{<video src="../static/videos/MovieRentalSchema.mp4" autoplay="true" loop="true" >}}

[Back to Data Engineering]({{< relref "../_index.md" >}})
