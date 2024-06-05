---
layout: default
title: Software Management Plan
nav_order: 4
has_children: true
has_toc: true
---

# Software Management Plan (SMP)

A Software Management Plan (SMP) is a formal document that defines what you will develop, who the software is for, how it will be delivered and how it will be supported over time. The plan addresses management during the active phases of development and sustainability once the project is completed.  

An SMP typically includes the following contents:  

- Assets Used & Produced
- Software Documentation & Version Control Protocol
- Preservation & Sustainability
- Roles & Responsibilities
- Software Dissemination & Sharing
- Ethics, Licensing & Legal Compliance

Hyper Articles en Ligne (HAL) provides a basic [research software management plan template](https://hal.science/hal-01802565) that you may follow. The Netherlands eScience Center and NWO, the Dutch Research Council, have also taken the initiative to develop a [practical guidelines for software management plans](https://zenodo.org/records/7185371).  

Utilizing a software management plan is highly recommended to ensure the desired level of reproducibility in your project. Achieving absolute reproducibility is challenging given the growing complexity of statistical and computational techniques, such as multi-threading and pseudo-randomness. However, by clearly defining reproducibility goals and implementing a comprehensive SMP, you can employ targeted best practices to reduce computational uncertainty and enhance research reproducibility.  

## Why you may need a Software Management Plan?

Here are several benefits to having a well-documented plan to manage and share your research software as the [Software Sustainability Institute](https://www.software.ac.uk/guide/writing-and-using-software-management-plan) points out:  

- Better understanding of roles and responsibilities in the project and potentially minimize the organizational and logistical damage if members of the project team change.  
- Reduce the efforts for other researchers to make use of, reuse and cite the research software.  
- More research funders start requiring software management to be addressed as part of the mandatory research data management plan.  

## Reproducibility Goal

There are many best practices to software project management. However, only few of them are best to all project scenarios. Defining reproducibility your project wants to achieve by categorical levels simplifies targeting best practices and resources to meet the specific needs of each level.  

Here is an article about different levels of reproducibility in research software, [_How reproducible should research software be?_](https://zenodo.org/record/4761867). In this article, it introduces four levels of research software reproducibiltiy, which can be applied to identify how reproducible the software should be and the best practices to achieve the different levels of reproducibility .  

- Level 0 - The script you downloaded that one time from the internet
    > Share code snippets, functions, single operations from the internet. Simple code that is intended for single or occasional use.

- Level 1 - Research software for pulication
    > Code that directly support the research conclusion, e.g. data processing, analysis and visualization scripts specific to the project or data.

- Level 2 - Research software as a tool
    > Code that is intended to be applied to different inputs or scenarios over a modest period of time, e.g. scientific software packages, development framworks.

- Level 3 - Research software as infrastructure
    > Software that is used by a broader community, e.g. data archiving systems, laboratory information management systems.
