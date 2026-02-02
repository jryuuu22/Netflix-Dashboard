# Netflix Content Strategy Dashboard

## Overview
This project is an interactive **Power BI dashboard** designed to support **content strategy and catalog analysis** for a Netflix-style streaming platform. The dashboard enables users to evaluate catalog composition, audience targeting, geographic availability, and individual title metadata through a clean, relational, and highly interactive BI experience.
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

## Design Approach 

Key design principles:
- Metrics are derived using **implicit measures** (counts, distinct counts, sums) where appropriate
- Relationships handle cross-filtering between genres, countries, cast, and titles
- Visual interactions and slicers are used to drive analytical context
- Business logic is embedded in the **data model**, not hard-coded into calculations

This approach demonstrates how many real-world BI dashboards are built:
- Faster development
- Easier maintenance
- Lower risk of logic errors
- Clearer analytical intent

Custom DAX can be added if advanced calculations or scenario modeling are required, but was intentionally excluded to keep the model transparent and scalable.

---

## Tools & Technologies
- **Power BI Desktop**
- Relational data modeling
- Interactive visuals, slicers, and cross-filtering
- Map visualizations for geographic analysis

---

## Example Use Cases
- Evaluate overall content catalog composition
- Identify dominant genres and audience ratings
- Analyze geographic availability of titles
- Explore individual movies or TV shows in detail
- Support strategic discussions around content distribution

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

## Notes
This project is intended for **portfolio and interview demonstration purposes** and is not affiliated with Netflix.

---

## Author
Created by **jryuu22**
