# AGENTS.md

## Snowflake Environment

- **Database:** `DEMO_DB`
- **Schema:** `TPCH_TRANSFORMED`
- **Warehouse:** `DEMO_WH`

## Source Data

Source data lives in `SNOWFLAKE_SAMPLE_DATA.TPCH_SF1`. All raw tables must be referenced through `_sources.yml` — never query source tables directly in models.

## dbt

Build all models:

```sh
dbt build --project-dir dbt/
```

Build a single model:

```sh
dbt build --select <model_name> --project-dir dbt/
```

## Naming Conventions

- Model files use **snake_case** (e.g., `orders_summary.sql`, `customer_lifetime_value.sql`).

## Git Workflow

- Feature branches follow the pattern: `feature/<description>`
- PRs are required before merging to `main`

## Tooling

This project uses **CoCo Desktop**. Do not use the `cortex` CLI command.
