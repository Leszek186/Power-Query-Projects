# Dataset: `sales.csv`

Sales records of a shoe retailer with three branches, covering 2024-01-01 to 2024-12-31.

## Format

- 10,000 data rows, 6 columns
- Delimiter: semicolon (`;`)
- Dates: `dd.mm.yyyy` (use the Polish locale or set the date type "Using Locale" when importing)

## Columns

| Column | Meaning | Notes |
|---|---|---|
| `sale_id` | Sale identifier | Not unique, see the note below |
| `branch_id` | Branch (1, 2 or 3) | Roughly 3,300 rows per branch |
| `shoe_id` | Product code | 365 distinct products |
| `sale_date` | Date of sale | `dd.mm.yyyy` |
| `quantity_sold` | Units sold | Integer from 1 to 4 |
| `total_price` | Total value of the sale | From 120 to 1,200; each `shoe_id` has one fixed unit price |

> **Note:** `sale_id` is not a unique identifier; multiple transactions can share the same ID.
> This is intentional: it simulates several transactions belonging to the same customer or order.
> In the data, 41 IDs occur twice with different branch, product, date and price.
> Do not remove "duplicates" by `sale_id`, as that would delete real sales.

## Importing into Power Query

1. **Data**, then **Get Data**, then **From Text/CSV**.
2. Set the delimiter to **Semicolon**.
3. Change the type of `sale_date` to **Date** using the Polish locale.
4. Check that the column names match the table above exactly.
