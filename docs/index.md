---
title: tds-csv — User Guide
author: Kasim Dhilawala
date: 2026-05-10
---

# tds-csv

**tds-csv** is a tiny CLI for quickly exploring CSV files. Built for the
*Tools in Data Science* course at IIT Madras, May 2026.

## Installation

```bash
uvx tds-csv-kasim --help
```

Or install globally:

```bash
uv tool install tds-csv-kasim
tds-csv --help
```

## Usage

### Show the top 10 rows

```bash
tds-csv sample.csv
```

### Sort by a specific column

```bash
tds-csv sample.csv --by population --top 5
```

## How It Works

The tool:

1. Reads the CSV with `pandas.read_csv`.
2. Sorts by the chosen column (defaulting to the first column).
3. Takes the top N rows.
4. Renders them with `rich` as a Unicode table.

## Architecture

The formula for text-to-digital transformation in our case is:

```
output = Render(SortBy_col(Read(csv))[:N])
```

## License

MIT — see the [LICENSE](https://github.com/KASIM-S-DHILA/tds-csv-kasim/blob/main/LICENSE) file.
