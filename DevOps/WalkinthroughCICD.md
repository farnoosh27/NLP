## Packaging packages
* pyroject.toml is basically formerly setup.py
benefits:
1) extendable
2) some information related to tools like .bandit -> [tool.bandit]


Also, when using hatch, we can do a pretty cool thing with testing: 
1) you can make a test.matrix
2) python = [39]
3) a bit more project-agnostic compared with poetry 

## build.sh
in the build stage, we want to build wheel from our python package
