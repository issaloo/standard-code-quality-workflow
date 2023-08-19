# Standard Code Quality Workflow

## Contributing

### General Guidelines
Please take a look at the following guides on writing code:
- [PEP 8 Style Guide](https://www.python.org/dev/peps/pep-0008/) for Python

### Set Up Development Environment
1. If you haven't already, clone the repository
```shell
cd ~/GitHub/issaloo
git clone git@github.com:issaloo/standard-code-quality-workflow.git
cd standard-code-quality-workflow
```

2. Create the virtual environment (to keep dependencies separate between projects)
```shell
python -m venv .venv
```
:memo: **Note:** Virtual environment will use the same python version as the system 

Navigate to your 


 
**To install development packages & general packages**, run
```shell
pip install '.[dev]'
```

**If you only want to install the general packages**, run
```shell
pip install .
```

### Set Up Templated Git Commits

Check if you have `npm` installed on your machine first before continuing.
```shell
npm --version
```

**If you don't have `npm`**, run
```shell
brew install node
```

And then, run
```shell
npm install
```

Now you should be able to use the `cz` command line tool to structure git messages.

### Set Up Linting

