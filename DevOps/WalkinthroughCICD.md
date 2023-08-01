## Packaging packages
## Definition of pipeline
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
For pipeline to exist, we need to do it through the codefresh
