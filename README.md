## Overview

Powerflow Service. Back end service for running powerflow simulations and studies

## Features:

* **Circuit Model Valdation**
* **Power Flow Result Validation**

## Dependencies

* <a href="https://greatexpectations.io/" target="_blank"><code>Great Expectations</code></a> for api and docs

## Usage (running locally):

Add database connection string to `./gx/uncommitted/config_variables.yml`
```yml
POSTGRESQL_CONNECTION_STRING: "postgresql+psycopg2://PGUSER:PGPASSWORD@localhost:5432/postgres"
```

![Alt text](images/screenshot.png)

## Example


