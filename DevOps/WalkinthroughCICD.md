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


## Basics of CI/CD
### What is a pipeline within CI/CD?
pipeline is basically a series of steps that we want to have executed. 
Theoretically speaking, it can be summarized as below: 
Prepare -> Test -> Push -> TAG
for each of the septs of need a *runner*, we do have these steps defined in them .yaml, we use an image to execute each step.
we use an image to execute the steps.
![Screenshot](https://github.com/farnoosh27/NLP/blob/main/DevOps/Screenshot%202023-08-01%20at%2011.56.36%20AM.png)

And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.

## What is gemfury?
