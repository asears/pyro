# Uplift Notes

## .github

- actions upgrades
- Split workflow templates
- markdown lint
- main not master branch
- dependabot
- secuity
- uv / ruff
- uv replaces setuptools build

## Issue Template

- bug telemetry

## docker

- Upgrade ubuntu
- scan dockerfile
- Add codespaces
- Replace conda with uv venv
- security scan
- shellcheck sh file
- makefile uses python 3.6
- install could use dependencies from file/lockfile uv.lock or piptools/pipenv

## Makefile

- Make could be replaced by tox, invoke, other options for python projects

## Docs

requirements.txt - dependency updates, stale project dependencies api, funsor, unmaintained library observations

## Examples

- docstrings, annotations

Warnings for improvements.

```shell
ruff check --select "ALL" examples --ignore S101,ANN101,ANN002,ANN003,T201,ANN,D,COM,RET,ERA,N,FBT,UP,PLR,C,G001
```

## Security

- Warnings outside use of assert.
- Examples have security warnings
- profiler/hmm has security warnings

```shell
ruff check --select "S" --ignore S101
```

## argparse

- uplift to click, typer, other cli tool helper

## licensing

- Apache however BSD-3 with no date.
- Uber to 2019

## codecov.yml

- move to pyproject.toml

## coveragerc

- move to pyproject.toml

## .gitattributes

- review ipynb, other extensions

## .gitignore

- comment the ignores

## .readthedocs.yml

- move to pyproject, sphinx config?

## CONTRIBUTING.md

- ruff check --select "I" --fix instead of isort?
- auto-add license header with vscode workspace?
- auto-format with vscode workspace?
- activating venv

## pyproject.toml

- linter for toml/pyproject
- centralize config
- properties for python versioning, packaging
- uv properties
- ruff checks

## setup.cfg/setup.py

- replace with pyproject.toml
- dependencies externally or in pyproject.toml / extended pyproject.toml

## hyperlinks

- dead link checker
- safe link checker

```shell
grep -i "http" *.* -s -r --exclude-dir=.ruff* --exclude-dir=.venv* --exclude-dir=_static --exclude=bayesian_regression_ii.ipynb --exclude=gmm.ipynb --exclude=gp.ipynb --exclude=intro_long.ipynb --exclude model_rendering.ipynb --exclude=normalizing_flows_intro.ipynb --exclude=scanvi.ipynb
```

- index links for LLM/RAG
