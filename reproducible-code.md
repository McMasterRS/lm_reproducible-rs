---
layout: default
title: Reproducible Computer Code
nav_order: 5
has_toc: true
---

# Reproducible Computer Code

Having developed a Research Software Management Plan, it's time to delve into your project. In the upcoming sections, we will explore technical and coding strategies aimed at enhancing the reproducibility of your software.  

# General & Technical Practices

## Documentation in Source Code

Publishing every step (computer code) and the underlying logic executed in the process. This is not just simply publishing the code. The goal is to publish *well-documented*, *well-commented* code. Code commenting is the practice of adding short notes throughout your code. These notes are called comments. They explain how your program works, and your intentions behind it. Consider the following code snippet,  

```python
poly = PolynomialFeatures(degree=2, include_bias=False)
```

How will the variable `poly` behave if the number of `degrees` is set to 4 instead of 2 or `include_bias` is set to true? This information is the underlying logic executed to reach to the analysis result. One might be interested in the reasoning of the decision made during the analysis such as why choosing a specific value for the parameter of a function. Code commenting can help illustrating the logics side by side with the code step executed in the analysis process. Code commenting is often done manually, and it is a long and time-consuming process. There are also AI tools that help speeding up the code commenting process, such as [GitHub Copilot](https://github.com/features/copilot).  

## Version Control Audit

One might be interested in seeing the details of the code for an analysis when a researcher is curious about how a specific design processing reach to a particular result. This curiosity is often raised out of the suspicion of error in the analysis or sometimes due to a desire to learn the details of new methodologies. Generating and providing an audit trail of work allows others follow or retrace the thought process in designing the code.  

![GitHub Blame](assets/img/github-blame.png)  

And this can be easily achieved by publicly maintaining your source code with a version control system (git e.g.) and including adequate and meaningful commit messages with each changes.  

Commit messages serve as a form of communication between team members working on a project. Clear and descriptive messages provide valuable context about the changes made in a commit, making it easier for others to understand and collaborate on the codebase. It allows team members to track the progress of specific features or bug fixes, review changes, and provide feedback effectively.  

## Interoperable Software Design

Interoperable software is designed to enabling integration with other software components via a standard programming interface. Consider the following two functions,  

```python
def foo():
    x = 1
    y = 2
    return x + y

def bar(x=1, y=2):
    return x + y
```

Which function can be reused and integrated with other software components easily? `foo()` or `bar()`? When other developers use the function in their software, `bar()` allows developers to utilize the underlying logic in the method without modifying its source code.  

```python
def baz(z=42):
    return bar(z, 916)
```

Aside from the software design perspective, employing middleware or integration platforms (Apache Kafka e.g.) that provide standardized interfaces and tools for connecting disparate software systems helps achieving software interoperability. These platforms act as intermediaries, enabling communication, data transformation, and message routing between different applications.  

## Use of Non-proprietary and Lossless Formats

In addition, the use of non-proprietary and lossless file formats for assets sharing is encouraged in reproducibility improvement.  

For documentation, formats like `.md` and `.txt` are preferable over `.docx` and `.pages`. And for software data, formats like `.csv`, `.xml` and `.json` are preferable over `.xls`. And for imagery assets, vector file formats like `.svg` and `.eps` are preferable over bitmap file formats like `.jpg` and `.gif`. When compiling software binary, avoid using proprietary code compilers (i.e. building software for platforms, like Windows and MacOS). As platform and OS dependencies are potential barriers to other users or developers.

If files are stored using proprietary software and when the software is no longer available or not available other users, information within those files will be lost. If proprietary files are needed for sharing, consider providing open files in addition to this.  

## Dependency Preservation

Updates to libraries can lead to subtly different behaviours across versions. Hence, generating code dependency is the first objective in creating reproducible research. In most packages/libraries managers, there exists a function to export packages/libraries installed for running the software you wrote. For example, in `pip`, a package installer for Python, you may run,  

```bash
pip freeze > requirements.txt
```

The resulting `requirements.txt` files would include the list of all packages you have installed for running the software with the same versions. Other researchers may follow this file and install the same packages/libraries used to run the software, by running,  

```bash
pip install -r requirements.txt
```

## More Formats to Preserve

A source code repository management service provides a centralized location for storing, managing, and versioning source code files and related assets. It offers a set of tools and features to facilitate collaboration, code sharing, version control, and project management for software development teams. Aside from using version control management tools to store source code, dependencies and documentation in repositories, one should consider generating DOI for snapshots in the repository using tools like [Zenodo](https://zenodo.org/).  

Some software also can be built and shared as container images. Docker offers a service called [Docker Hub](https://hub.docker.com/), which is an open-source registry to [store](https://docs.docker.com/engine/reference/commandline/push/) container images and allows others to download and run your container images. A container image repository is a centralized location or service that stores and manages container images. Container images are self-contained, lightweight packages that encapsulate an application along with its dependencies and configuration settings. They are used in containerization technologies like Docker to create and run containers consistently across different environments.  

A software package registry is a centralized repository or database that hosts and manages software packages. It serves as a platform for developers and users to discover, download, install, and manage software libraries, frameworks, tools, or applications. Software package registries provide a standardized way to distribute and share software components across different programming languages and platforms. The package installer for Python mentioned above, `pip`, download packages from a software package registry called [PyPI (Python Package Index)](https://pypi.org/).  

You may also consider adding your software to the [Research Software Directory](https://research-software-directory.org/). The Netherlands eScience Center developed the open-source research software directory to promote visibility, findability, impact and reuse of research software.  

Why do you need all these preservation methods? One may ask. Each of these methods/tools help promote the reproducibility of research software in different aspects. Here is the general rule of thumb, use...  

- **GitHub or other source code repository management services**, for storing software source code files and related assets and collaboration.  
- **Zenodo or other records repository**, for generating a persistent object identifier for your software and using it for citations in publications.  
- **Research Software Directory**, for making your research software discoverable and findable in the research software community.  

## Software Testing

Research software often relies on external libraries, frameworks, or tools. Testing aids in managing dependencies by verifying that the software works correctly with specific versions of those dependencies. This information is crucial for reproducibility because it allows others to recreate the software environment accurately, ensuring that the same results can be obtained.  

Testing enables collaboration among researchers by providing a shared understanding of the software's behaviour. By testing and documenting the software thoroughly, researchers can verify each other's work, reproduce experiments, and validate research outcomes. This collaborative approach fosters transparency, trust, and confidence in the research and open source community.  

Testing should be carried out in different levels of research software. Consider implementing a formal test plan, including unit testing, regression and integration testing, with the help of a continuous integration workflow ([GitHub Actions](https://github.com/features/actions), [Travis CI](https://www.travis-ci.com/) e.g.). Like the software source code, the test plan should be well-documented, well-commented and open-source to increase the legitimacy and transparency of the projects.  
