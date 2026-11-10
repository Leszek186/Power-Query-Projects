# Power Query Learning

Practice material for learning Power Query: notes and a dataset to work on.

## Structure

- [`Introduction/Notes.md`](Introduction/Notes.md): learning notes (basic concepts, Power Query Editor, M language).
- [`dataset/`](dataset/): the practice dataset `sales.csv` with its description.

## Suggested exercises (using `sales.csv`)

1. Import the file with the correct delimiter and date locale, then set column types.
2. Check that `sale_id` is not unique (41 IDs are shared by different transactions) and, if you need a key, add an index column instead of removing rows.
3. Add a calculated column with the unit price (`total_price / quantity_sold`).
4. Group sales by `branch_id` and by month.
