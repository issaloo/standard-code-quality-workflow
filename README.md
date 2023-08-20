# Standard Code Quality Workflow (Python)

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
[!IMPORTANT]
Virtual environment will use the same python version as the system

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
[!NOTE]
This will install packages [pre-commit](https://pre-commit.com/), [commitizen](https://commitizen-tools.github.io/commitizen/), and [gitlint](https://jorisroovers.com/gitlint/latest/)

(Optional) Install only the general packages
```shell
pip install .
```

### Set Up Standardized Version Control

1. Automate scripts (i.e., linting, formatting) at commit with pre-commit
```shell
pre-commit install
```

2. Enforce commit message template at commit with gitlint
```shell
gitlint install
```

### Test It Out

**Check if `Commitizen` is working**

:mag_right: Try using `cz commit` or `cz c` in command line
:white_check_mark: You should get structured commits

[!NOTE]
Ctrl-C to exit commit template

**Check if `gitlint` is working**
:mag_right: Write a bad commit (e.g., `git commit -m 'bad commit'` in command line
:white_check_mark: You should get a question on whether to continue the commit.

**Check if `pre-commit` is working**
:mag_right: Change test/main.py lightly (e.g., adding a space), run `git add test/main.py`, run `cz commit`
:white_check_mark: You should get automatic fixes to the main.py file and some errors
