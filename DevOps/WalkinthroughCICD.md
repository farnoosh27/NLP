## Packaging packages
## Definition of pipeline
### PEP 660 
[Editable installs for pyproject.toml based builds (wheel based)](https://peps.python.org/pep-0660/)
### PEP 621 
[PEP 621 – Storing project metadata in pyproject.toml](https://peps.python.org/pep-0621/)
* pyroject.toml is basically formerly setup.py
benefits:
1) extendable
2) some information related to tools like .bandit -> [tool.bandit]


Also, when using hatch, we can do a pretty cool thing with testing: 
1) you can make a test.matrix
2) python = [39]
3) a bit more project-agnostic compared with poetry 

## build.sh
in the build stage, we want to build a wheel from our Python package

## How to create the pipeline?
For the pipeline to exist, we need to do it through the Codefresh


PEP 660 – Editable installs for pyproject.toml based builds (wheel based)

