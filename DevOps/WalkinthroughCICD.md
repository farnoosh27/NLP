# Packaging/Hatchling/CI/CD/Codefresh
### PEP 660 
[Editable installs for pyproject.toml based builds (wheel based)](https://peps.python.org/pep-0660/)
### PEP 621 
[PEP 621 – Storing project metadata in pyproject.toml](https://peps.python.org/pep-0621/)

## What is Hatch?
[Hatch](https://hatch.pypa.io/latest/) is a modern, extensible Python project manager.

### Why pyproject.toml rather than setup.py?
* pyroject.toml is basically formerly setup.py
benefits:
1) extendable
2) some information related to tools like .bandit -> [tool.bandit]
## What is [gemfury](https://gemfury.com/)?
Our private python artifactory.

Also, when using hatch, we can do a pretty cool thing with testing: 
1) you can make a test.matrix
2) python = [39]
3) a bit more project-agnostic compared with poetry
4) 
## .fake8
does code style check
## scripts/build.sh
in the build stage, we want to build a **wheel** from our Python package, so here are the hatch commands.
```
#!/bin/sh
set -e

python3 -m pip install --upgrade pip hatch
python3 -m hatch build
```

## How to create the pipeline?
For the pipeline to exist, we need to do it through the Codefresh
### Codefresh
* CI
  * Prepare
  * Test: static code analysis/unit testing
* CD
  * Push: push to Gemfury ( basically, we are pushing the wheel at this stage not the TAG) 
  * Tag: creating a release tag
  
We want to have the CD action only after the code review on the **main branch**. In our case, in the yaml file, We run this pipeline on every push to every branch, and if it is the main branch, we do something. 


## Basics of CI/CD
### What is a pipeline within CI/CD?
pipeline is basically a series of steps that we want to have executed. 
Theoretically speaking, it can be summarized as below: 

Prepare -> Test -> Push -> TAG

for each of the septs that need a *runner*, we do have these steps defined in them .yaml, we use an image to execute each step.
we use an image to execute the steps.

![Screenshot](https://github.com/farnoosh27/NLP/blob/main/DevOps/Screenshot%202023-08-01%20at%2011.56.36%20AM.png)

And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.
## What to do on codefresh? 
1) choose a pipleline template, in this case it can be app-CICDtemplate and choose project to be agility, and ADD GIT CLONE STEP TO PIPLELINE choose the name of your project
2) check for yaml from the repository, and choose Branch to be main, It will find our codefresh.yaml, make sure we are in the repository that we should be.
3) more importantly, we need to add variables from shared configurations.
4) When pushing on the gemfury, check that in the scripts/release.sh --> PACKAGE_NAME=${3:-"expl_oem_parsing"}

## What happens, after creating pipeline?
