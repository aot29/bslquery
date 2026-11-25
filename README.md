# bslquery

[![tests](https://github.com/MfN-Berlin/bslquery/actions/workflows/tests.yml/badge.svg)](https://github.com/MfN-Berlin/bslquery/actions/workflows/tests.yml)

Python package for querying the [biosoundslab](https://github.com/MfN-Berlin/biosoundslab) database.

Query results are returned as Darwin Core JSON or as Excel files (depending on the query, see examples).

## Installation
```
conda create -n biosoundslab python=3.12
conda activate biosoundslab
python -m pip install -r requirements.txt
```

Copy the `.env.examples ` file to `.env`. 
Open `.env` and set the required variables (this file will not be committed).

## Running the tests
```
conda activate biosoundslab
pip install -e .
python -m pytest
```

## Running the examples
Start the Jupyter notebooks server

```
conda activate biosoundslab
pip install -e .
jupyter lab
```

Open the `examples/00_Setup_DB_Connection` notebook and follow the instructions in the notebook to finish the setup.

See the notebooks in the `examples` directory for more examples.


## Generating the API documentation
The classes in `src/bslquery` are documented with [pdoc](https://pdoc.dev), which reads the docstrings automatically.

```
conda activate biosoundslab
pip install -e ".[dev]"
# static HTML into docs/
pdoc bslquery -o docs
# or serve locally at http://localhost:8080
pdoc -p 8080 bslquery
```

Open `docs/index.html` in a browser to browse the generated docs.

