# Documentary

## Install

### Mac 

```
brew install python
pip install pdm
pdm install
```
### Windows

Install Python https://www.python.org/downloads/windows/

```
pip install pdm
pdm install
```

## Usage

```
pdm run python -m bin.cli
```

Then input the path to your project to analyze. 
For large project it can take couple of minutes

## Use cases

### Parallel entities

Different kinds of entities (see function collect_code_items) which appear at the same level. We assume they belong to one class of entities and should be documented
files/folders in a folder
yaml, json sections of the same level
env vars from one file

### Common

Trying to scan files structure in order to find common markers (see categories) If it's not documented, it will be recommended.
* CI/CD
* Infrastructure as Code
* Configuration
* Installation process
* Deployment process
* Tests

### Endpoints

Endpoints are modules which are not imported by any other module. Assuming that such files are entry points of services, or scripts, which should be documented. Only Python supported. If they are not yet, to recommend
Python only for now

### Validation

Looks for validation of variables against some strings, assuming such cases should be documented
“==” "startswith", "endswith", "find", "index"


# License 
Business Source License 1.1