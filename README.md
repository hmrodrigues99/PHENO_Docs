# PHENO_Docs
[User documentation](https://pheno-docs.readthedocs.io/en/latest/) for the [PHENO platform](https://brapi.biodata.pt/) & the OntoBrAPI metadata submission tool, hosted by Read the Docs.
Generated with sphinx (v8.1.3) and the sphinx-rtd-theme (v3.0.2).

## Generate PHENO documentation
```python
# Clone the repository
git clone git@github.com:hmrodrigues99/PHENO_Docs.git
cd PHENO_Docs
# Create and activate a python virtual environment
python3 -m venv venv_docs
source venv_docs/bin/activate # (Linux, MacOS)
source venv_docs/Scripts/activate # (Windows)
# Install dependencies
python3 -m pip install -r requirements.txt
# Make documentation
cd docs
make html
```

The index.html will be generated within the builds/html folder.
