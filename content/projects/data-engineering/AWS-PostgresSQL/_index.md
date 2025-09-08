---
title: "AWS(RDS) + PostgreSQL"
draft: false
summary: "Crowdfunding Data Pipeline"
---
The goal of this project is to take raw crowdfunding campaign data and build an analytics-ready database. The workflow includes:

### Data Cleaning & Transformation
![Data Cleaning](/static/images/data-clean.png)
- Load raw CSV data using Pandas.
- Convert timestamp fields to datetime objects.
- Convert boolean fields (staff_pick, spotlight) to proper boolean type.
- Split the category column into category and sub_category.

### Dimension & Fact Tables
![Dimension & Fact Tables](/static/images/dim-tables.png)
Created dimension tables:
- dim_time — stores unique dates with year, month, day, weekday.
- dim_category — stores categories and subcategories.
- dim_country — stores country and currency information.
- dim_campaign — stores campaign metadata (name, blurb, staff_pick, spotlight).
Created fact table:
- fact_campaign — stores campaign metrics (goal, pledged, backers_count, outcome) and foreign keys referencing dimension tables.

### Database Schema
{{< video src="/static/videos/schema.mp4" width="600" autoplay="true" loop="true" >}}
- Star schema design for easy analytics.
- Enforced foreign key relationships between fact and dimension tables.

### Cloud Integration
![Cloud Integration](/static/images/cloud-deploy.png)
- PostgreSQL database hosted on AWS RDS.
- Data loaded programmatically using Python and SQLAlchemy.
- Scripts include functionality to connect to RDS, create tables, and import cleaned data.

---
You can find the code for this project on my
[Github Repo](https://github.com/Chan-McLaren/crowdfunding_data_engineering_ISI)

---
[Back to Data Engineering]({{< relref "../_index.md" >}})