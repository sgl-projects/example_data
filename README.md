# example_data

A dbt project that builds example datasets into a DuckDB database for use across [sgl-projects](https://github.com/sgl-projects) repos.

## Datasets

- **diamonds** — `ggplot2::diamonds` (53,940 round-cut diamonds with price, carat, cut, color, clarity, and dimensions)

## Using the database

The latest DuckDB database is published as a GitHub Release asset and can be downloaded directly:

```
https://github.com/sgl-projects/example_data/releases/latest/download/example_data.duckdb
```

### R

```r
download.file(
  "https://github.com/sgl-projects/example_data/releases/latest/download/example_data.duckdb",
  "example_data.duckdb"
)
con <- DBI::dbConnect(duckdb::duckdb(), "example_data.duckdb")
```

## Documentation

Browse the dbt docs at [sgl-projects.github.io/example_data](https://sgl-projects.github.io/example_data/).
