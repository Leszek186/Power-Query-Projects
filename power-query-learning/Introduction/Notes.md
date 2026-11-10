# Power Query: Introduction (notes)

> Sections 1-3 and 5 are prompts for my own notes. Section 4 is a worked example based on an audit of `sales.csv`.

## 1. What is Power Query?

- Definition in my own words:
- Where it lives: Excel (Data tab), Power BI Desktop (Transform data):

## 2. The ETL idea

- Extract:
- Transform:
- Load:

## 3. Power Query Editor

- Applied Steps pane:
- Formula bar and M language:
- Most used transformations I learned:

## 4. Example from this repo: checking `sales.csv` before analysis

Dataset: [`../dataset/sales.csv`](../dataset/sales.csv)

What a quick data-quality check showed:

| Check | Result |
|---|---|
| Rows / columns | 10,000 rows, 6 columns, no empty fields |
| Delimiter and dates | Semicolon; dates as `dd.mm.yyyy`, so set the locale to Polish when typing the date column |
| Date range | 2024-01-01 to 2024-12-31 |
| Value ranges | `quantity_sold` 1-4, `total_price` 120-1,200 |
| Unit price | Each of the 365 `shoe_id` values has one fixed unit price |
| `sale_id` | Not unique (41 IDs shared by different transactions) by design, so use an index column if a key is needed |
| Header problem | A hidden character in the `quantity_sold` header made the column name differ from what is displayed; it is fixed in this repository |

Lessons:

- Always check column names for invisible characters after import.
- Verify whether an ID column is really unique before removing duplicates.
- Set the locale when converting text to dates.

## 5. Questions to revisit

-
