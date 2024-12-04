FROM quay.io/astronomer/astro-runtime:12.5.0

RUN python -m venv soda_venv
RUN . soda_venv/bin/activate && pip install --no-cache-dir soda-core-bigquery==3.0.45 && deactivate
# RUN . soda_venv/bin/activate && pip install --no-cache-dir soda-core-scientific==3.0.45
# install dbt into a virtual environment
RUN python -m venv dbt_venv && source dbt_venv/bin/activate && \
    pip install --no-cache-dir dbt-bigquery==1.5.3 && \
    pip install --no-cache-dir setuptools