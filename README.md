# standardizeUtils
A Python package for standardizing SMILES and InChI strings with PubChem's Standardization Service.
Standardization requests are called through [PubChem's PUG service](https://pubchem.ncbi.nlm.nih.gov/docs/power-user-gateway).

### Installation via pip:
```bash
pip install -e 'git+https://github.com/boecker-lab/standardizeUtils/#egg=standardizeUtils'
```
### Examples:
To standardize a single SMILES string using PubChem, use:
```python
from standardizeUtils.standardizeUtils import standardize_structure_with_pubchem
standardize_structure_with_pubchem('OCO', 'smiles')
```

To standardize multiple SMILES strings with PubChem, use:
```python
from standardizeUtils.standardizeUtils import standardize_structure_list_with_pubchem
smiles_strings = ['OCO', 'CC']
standardize_structure_list_with_pubchem(smiles_strings, 'smiles')
```
