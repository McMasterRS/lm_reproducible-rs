---
layout: default
title: General Practices
parent: Reproducible Computer Code
nav_order: 1
---

## General Practices

### Version Control Audit

One might be interested in seeing the details of the code for an analysis when a researcher is curious about how a specific design processing reach to a particular result. This curiosity is often raised out of the suspicion of error in the analysis or sometimes due to a desire to learn the details of new methodologies. Generating and providing an audit trail of work allows others follow or retrace the thought process in designing the code. And this can be easily achieved by publicly maintaining your source code with a version control system (git e.g.).  

![GitHub Blame](assets/img/github-blame.png)

### Documentation in Source Code

Publishing every step (computer code) and the underlying logic executed in the process. This is not just simply publishing the code. The goal is to publish *well-documented*, *well-commented* code. Code commenting is the practice of adding short notes throughout your code. These notes are called comments. They explain how your program works, and your intentions behind it. Consider the following code snippet,  

```python
poly = PolynomialFeatures(degree=2, include_bias=False)
```

How will the variable `poly` behave if the number of `degrees` is set to 4 instead of 2 or `include_bias` is set to true? This information is the underlying logic executed to reach to the analysis result. One might be interested in the reasoning of the decision made during the analysis such as why choosing a specific value for the parameter of a function. Code commenting can help illustrating the logics side by side with the code step executed in the analysis process. Code commenting is often done manually, and it is a long and time-consuming process. There are also AI tools that help speeding up the code commenting process, such as [GitHub Copilot](https://github.com/features/copilot).  

### Interoperable Software Design

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

### Use of Non-proprietary Formats

In addition, the use of non-proprietary file formats for assets sharing is encouraged in reproducibility improvement.  

For documentation, formats like `.md` and `.txt` are preferable over `.docx` and `.pages`. And for software data, formats like `.csv`, `.xml` and `.json` are preferable over `.xls`.  

If files are stored using proprietary software and when the software is no longer available or not available other users, information within those files will be lost. If proprietary files are needed for sharing, consider providing open files in addition to this.  
