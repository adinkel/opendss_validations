## Overview

Circuit model field validations for OpenDSS

## Dependencies

* <a href="https://greatexpectations.io/" target="_blank"><code>Great Expectations</code></a> for api and docs

## Usage (running locally):

Add database connection string to `./gx/uncommitted/config_variables.yml`
```yml
POSTGRESQL_CONNECTION_STRING: "postgresql+psycopg2://PGUSER:PGPASSWORD@localhost:5432/postgres"
```
Run example
```python
import great_expectations as gx
from datetime import datetime

# File Context
context = gx.get_context(mode="file")

# Run Checkpoints
checkpoint = context.checkpoints.get('circuit_model_validation')
validation_results = checkpoint.run()
checkpoint = context.checkpoints.get('circuit_result_validation')
validation_results = checkpoint.run()

# Build docs
context.build_data_docs(site_names='local_site')
context.open_data_docs()
```
## Example
![Alt text](images/Screenshot_Transformer_Expectations.png)

![Alt text](images/Screenshot_Validation_Results.png)

![Alt text](images/Screenshot_Transformer_Validation_Results.png)




