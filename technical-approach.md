---
layout: default
title: Technical Approach
parent: Reproducible Computer Code
nav_order: 2
---

## Technical Approach

Updates to libraries can lead to subtly different behaviours across versions. Hence, generating code dependency is the first objective in creating reproducible research. In most packages/libraries managers, there exists a function to export packages/libraries installed for running the software you wrote. For example, in `pip`, a package installer for Python, you may run,  

```bash
pip freeze > requirements.txt
```

The resulting `requirements.txt` files would include the list of all packages you have installed for running the software with the same versions. Other researchers may follow this file and install the same packages/libraries used to run the software, by running,  

```bash
pip install -r requirements.txt
```

Aside from using version control management tools to store source code, dependencies and documentation in repositories, one should consider generating DOI for snapshots in the repository using tools like [Zenodo](https://zenodo.org/). Some software also can be built and shared as container images. Docker offers a service called [Docker Hub](https://hub.docker.com/), which is an open-source registry to [store](https://docs.docker.com/engine/reference/commandline/push/) container images and allows others to download and run your container images.  

Testing should be carried out in different levels of research software. Consider implementing a formal test plan, including unit testing, regression and integration testing, with the help of a continuous integration workflow ([GitHub Actions](https://github.com/features/actions), [Travis CI](https://www.travis-ci.com/) e.g.). Like the software source code, the test plan should be well-documented, well-commented and open-source to increase the legitimacy and transparency of the projects.  
