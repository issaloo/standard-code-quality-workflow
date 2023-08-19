# Standard Code Quality Workflow

## Contributing

### General Guidelines
Please take a look at the following guides on writing code:
- [PEP 8 Style Guide](https://www.python.org/dev/peps/pep-0008/) for Python

### Set Up Development Environment
1. Clone and navigate to the repository
```shell
cd ~/GitHub/issaloo
git clone git@github.com:issaloo/standard-code-quality-workflow.git
cd standard-code-quality-workflow
```

2. Create the virtual environment to keep dependencies separate between projects
```shell
python -m venv .venv
```
:memo: **Note:** Virtual environment will use the same python version as the system

3. Activate the virtual environment
```shell
source .venv/bin/activate
```
(Optional) Deactivate the virtual environment
```shell
deactivate
```

4. Install general & development packages
```shell
pip install '.[dev]'
```

(Optional) Install only the general packages
```shell
pip install .
```

5. Set Up Templated Git Commits

Now you should be able to use the `cz` command line tool to structure git messages.


6. Set Up Lintin and Autoformatting

