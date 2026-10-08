# Third-party notices: Market-Ready Data

## What Data Meaning supplies

The deployment runs one container image, `datameaning.azurecr.io/market-ready-data`, from a registry operated
by Data Meaning Services Group, Inc. The image contains:

1. **Data Meaning's own code** (the assessment engine and its catalogs), licensed to you under the terms of
   the Marketplace offer.
2. **The `python:3.12-slim` base image**, published by the Docker Official Images program. It contains the
   Python interpreter (Python Software Foundation License) and packages from Debian GNU/Linux, some under the
   GNU General Public License. The corresponding source for those packages is published by Debian at
   https://sources.debian.org and by the Python Software Foundation at https://www.python.org/downloads/source/.
   On written request to legal@datameaning.com, Data Meaning will provide a copy of that source for three years
   from the date you received the image.
3. **A public sample** of 39,741 records from the City of Chicago's "Crimes - 2001 to Present" dataset, used
   only when you choose Sample data. Published by the City of Chicago on its Data Portal
   (https://data.cityofchicago.org) and subject to the City's terms of use.

## What your deployment downloads itself

When the assessment job starts, it installs the libraries below from the Python Package Index (pypi.org),
directly from their publishers. Data Meaning does not distribute, mirror or republish them; each is licensed to
you by its publisher under the license named here.

Always installed:

| Package | Version | License |
|---|---|---|
| duckdb | 1.5.6 | MIT |
| sqlglot | 30.21.0 | MIT |
| pyarrow | 25.0.1 | Apache License 2.0 |
| numpy | 2.5.3 | BSD 3-Clause (its wheels bundle further libraries under their own permissive or GPL-with-runtime-exception terms, listed in the package) |
| pytz | 2026.5 | MIT |
| PyYAML | 6.0.3 | MIT |
| openpyxl | 3.1.5 | MIT |
| azure-identity | 1.26.0 | MIT |
| azure-keyvault-secrets | 4.11.3 | MIT |

Installed only for the database you choose:

| Database | Package | Version | License |
|---|---|---|---|
| Azure SQL Database, SQL Server | mssql-python | 1.15.0 | MIT; it installs Microsoft ODBC Driver 18 for SQL Server, under Microsoft's license for that driver |
| PostgreSQL | psycopg[binary] | 3.3.6 | GNU Lesser General Public License v3 (bundles libpq, PostgreSQL License) |
| Oracle Database | oracledb | 26.0.1 | Apache License 2.0 or Universal Permissive License 1.0 |
| Snowflake | snowflake-connector-python | 4.8.0 | Apache License 2.0 |
| Google BigQuery | google-cloud-bigquery | 3.46.1 | Apache License 2.0 |

Those packages may install their own dependencies from PyPI, each under its own license as published there.

## Contact

legal@datameaning.com
