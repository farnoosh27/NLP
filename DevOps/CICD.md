## What is CI/CD?

Continuous Integration (CI) is the practice of regularly integrating code changes into a shared repository, triggering automated build processes and tests to detect issues early in the development process.


[Video: IBM Continuous Integration](https://www.youtube.com/watch?v=1er2cjUq1UI)

![Screenshot](https://github.com/farnoosh27/NLP/blob/28e6cdc567ca7d47c54139c552707fd5da0c43c2/DevOps/Screenshot%202023-07-31%20at%203.54.34%20PM.png)
(the image is extracted from the LinkedIn learning [course](https://www.linkedin.com/learning/devops-with-aws/cicd-overview) taught by Dipali Kulshrestha)
Dipali Kulshrestha

[Video: IBM Continuous Integration](https://www.youtube.com/watch?v=1er2cjUq1UI)


Continuous Delivery (CD) is similar to CD, but with the distinction that in Continuous Delivery, code changes are automatically deployed to a staging environment after passing CI, and the deployment to the production environment is typically triggered manually, allowing for human verification and approval before going live.


[Video: IBM Continuous Delivery](https://www.youtube.com/watch?v=2TTU5BB-k9U)



![Screenshot](https://github.com/farnoosh27/NLP/blob/main/DevOps/Screenshot%202023-07-31%20at%204.39.43%20PM.png)
(the image is extracted from the LinkedIn learning [course](https://www.linkedin.com/learning/devops-with-aws/cicd-overview) taught by Dipali Kulshrestha)


## Codefresh & CI/CD
Codefresh is a cloud-native continuous integration and delivery (CI/CD) platform designed to facilitate the rapid development, deployment, and management of cloud-native applications. It supports various cloud platforms, including Kubernetes, Docker, and AWS. The platform offers an intuitive user interface to streamline the development process.

Codefresh provides a comprehensive CI/CD solution covering the entire software lifecycle. It allows users to view releases in the Kubernetes dashboard, access Docker images, and trace builds from a single interface. The platform is versatile, working with all major Git platforms and cloud providers, offering freedom from vendor lock-in.

While Codefresh has a strong focus on containers and Kubernetes, it can also handle traditional applications running on virtual machines or physical data centers.

## Basics of CI/CD
### What is a pipeline within CI/CD?
pipeline is basically a series of steps that we want to have executed. 
Theoretically speaking, it can be summarized as below: 
Prepare -> Test -> Push -> TAG
for each of the septs of need a *runner*, we do have these steps defined in them .yaml, we use an image to execute each step.
we use an image to execute the steps.
![Screenshot](https://github.com/farnoosh27/NLP/blob/main/DevOps/Screenshot%202023-08-01%20at%2011.56.36%20AM.png)

And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.And then we we define the steps and put under those stages and for each step we define an image on which we want the step to run and we define what we want to happen that step.


## Python Package Index (PyPI)

## What are package managers?
probably a useful article can be found here: https://www.activestate.com/blog/which-python-dependency-manager-should-i-choose/

both a Python packaging tool and a dependency management tool
### Setuptools
### PIP
## pyproject.toml vs setup.py 
pyproject.toml is formerly setup.py as it contains all the metadata of the projects and dependencies. What is cool about it is thata is's extendible and we can put other tools such as [tool.bandit]

[Python Enhancement Proposal (PEP) 518](https://peps.python.org/pep-0518/#:~:text=This%20PEP%20specifies%20how%20Python,execute%20their%20chosen%20build%20system.), which describes a mechanism for specifying minimum and maximum version requirements for Python packages. PEP 518 introduces the use of a new file called pyproject.toml for specifying build system requirements and build backend configuration.
