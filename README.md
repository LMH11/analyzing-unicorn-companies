# Analyzing Unicorn Companies

## Overview

A SQL-based analysis of unicorn companies (privately held startups valued at over $1 billion) to identify industry trends and high-growth sectors. The project supports an investment firm in understanding which industries produce the highest valuations and how rapidly new unicorns are emerging, helping inform portfolio strategy.

## Objective

Identify the three top-performing industries based on the number of new unicorns created between 2019 and 2021, and analyze their year-over-year trends in unicorn count and average valuation.

## Database Schema

The analysis uses four related tables in the `unicorns` database:

**companies** — Company details including name, city, country, and continent.

**dates** — Tracks when each company became a unicorn and when it was founded.

**funding** — Valuation, funding raised, and key investors.

**industries** — The industry each company operates in.

## Approach

1. **Rank industries** — Use a CTE with `RANK()` window function to identify the top 3 industries by total unicorn count (2019–2021).
2. **Aggregate by year** — For those top industries, calculate the number of unicorns and average valuation per year.
3. **Compare trends** — Analyze how each industry's unicorn growth and valuations changed across the three-year period.

## Key Findings

- **Fintech**, **Internet software & services**, and **E-commerce & direct-to-consumer** are the three top-performing industries by unicorn count.
- 2021 saw the highest volume of new unicorns across all three industries, but with lower average valuations compared to prior years.
- Earlier unicorns (2019) tended to have higher average valuations — for example, Fintech unicorns averaged $6.80B in 2019 versus $2.75B in 2021 — suggesting that as more companies reach unicorn status, the average valuation moderates.

## Tools Used

- SQL (PostgreSQL — CTEs, window functions, aggregations)
- Jupyter Notebook
