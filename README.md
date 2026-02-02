# Netflix Content Strategy Dashboard

## Overview
This project is an interactive **Power BI dashboard** designed to support **content strategy and catalog analysis** for a Netflix-style streaming platform. The dashboard enables users to evaluate catalog composition, audience targeting, geographic availability, and individual title metadata through a clean, relational, and highly interactive BI experience.

The project emphasizes **data modeling, relationship-driven analysis, and UX design**, intentionally minimizing custom DAX to demonstrate effective use of Power BI’s semantic model and filter context.

---

## Data Preparation & Cleaning

The dataset was cleaned and structured using **Microsoft Excel** prior to loading into Power BI.

Key steps included:
- Cleaning and standardizing column values (e.g., removing extra whitespace, handling inconsistent text formatting)
- Splitting multi-value fields (such as genres, cast members, and countries) into separate rows to support relational modeling
- Creating new tables to normalize the data (e.g., genre, cast, director, and country tables)
- Establishing a consistent primary key (`show_id`) across all tables
- Reordering and organizing fields to improve readability and usability within Power BI

This preprocessing step enabled a **clean relational data model**, improved filtering performance, and reduced the need for complex calculations within the dashboard.

## Dashboard Preview

### Executive Overview & Single Title View
![Netflix Dashboard](https://github.com/jryuuu22/Netflix-Dashboard/blob/9c2f1e1ef760c43278d7400ae489f02a856fdb7f/dashboard/Netflix%20Dashboard%20page%201.png)
![Netflix Dashboard](https://github.com/jryuuu22/Netflix-Dashboard/blob/9c2f1e1ef760c43278d7400ae489f02a856fdb7f/dashboard/Netflix%20Dashboard%20Page%202.png)


> *The dashboard is structured with an executive overview for portfolio-level insights and a single-title view for detailed exploration of individual movies or TV shows.*

---

## Relational Data Model

![Relational Model](https://github.com/jryuuu22/Netflix-Dashboard/blob/546dc2c24c16eaba5d3dc8bd45605ad4964bf04b/dashboard/relational_table.png)

> *The data model uses `show_id` as the primary key and relies on normalized dimension tables to drive filtering, aggregation, and interactivity across visuals.*

---

## Dashboard Pages

### 1. Executive Overview
This page provides a high-level summary of the content catalog for strategic decision-making.

Key elements include:
- Total titles, movies, and TV shows
- Distinct genre count
- Movie vs TV show composition
- Ratings distribution
- Top genres
- Content growth over time
- Global country availability map

The layout is designed to be **executive-facing**, with all key insights visible without scrolling.

---

### 2. Single Title View
This page allows users to explore detailed information for an individual movie or TV show.

Features include:
- Title metadata (release year, date added, rating, type)
- Description and genre classification
- Country availability map
- Cast and director information
- Interactive filtering via title selection

This view supports **operational analysis and content discovery** by enabling drill-down from portfolio-level insights to individual titles.

---

## Data Model & Architecture
The dashboard uses a **normalized, relational data model** with `show_id` as the primary key.

### Core Tables
- `netflix_titles` – Central fact table containing title metadata
- `netflix_listed_in` – Genre/category mapping
- `netflix_cast` – Cast members per title
- `netflix_directors` – Directors per title
- `countries_released` – Country availability per title

Relationships between tables drive filtering and aggregation across visuals.

---

## Design Approach (No DAX by Design)
This dashboard intentionally avoids custom DAX measures to highlight **Power BI’s built-in aggregation engine and filter propagation capabilities**.

Key design principles:
- Metrics are derived using **implicit measures** where appropriate
- Relationships handle cross-filtering between genres, countries, cast, and titles
- Visual interactions and slicers define analytical context
- Business logic is embedded in the **data model**, not hard-coded into calculations

This approach reflects many real-world BI implementations where:
- Simplicity improves maintainability
- Logic transparency reduces risk
- Models scale more easily across teams

Custom DAX can be added for advanced calculations if required.

---

## Files in This Repository

| File | Description |
|------|-------------|
| `Netflix Dashboard.pbix` | Power BI dashboard file |
| `Netflix Dashboard.pdf` | Static export of the dashboard |
| `Netflix_relational_table.pdf` | Data model and relationship diagram |
| `netflix_titles.csv` | Source dataset |
| `README.md` | Project documentation |

---

## Tools & Technologies
- **Power BI Desktop**
- **Excel** for data cleaning
- Relational data modeling
- Interactive visuals and slicers
- Geographic mapping for content availability analysis

---

## Notes
This project is intended for **portfolio and interview demonstration purposes** and is not affiliated with Netflix.

---

## Author
Created by **jryuuu22**
