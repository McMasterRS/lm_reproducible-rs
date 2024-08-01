---
layout: default
title: Preservation & Sustainability
parent: Software Management Plan
nav_order: 3
---

# Preservation & Sustainability

Preservation and sustainability in research software management refer to practices and strategies aimed at ensuring the long-term availability, usability and maintenance of research software beyond the duration of a specific project. These practices and strategies involve measures to address technological, organizational, and environmental factors that may impact the software's accessibility and usability over time. Research software preservation has four major aspects.  

1. Storage

    Code of actively developed or maintained software can be stored in public cloud version control management services (e.g. GitHub) where it can be maintained to prevent degredation or obselescence, and new versions can be released and found. These public services allow interested parties to find the latest code and documentation of any changes.  

   Long term storage, especially for references to the software that will live long after the project (e.g. in publications), require more persistent storage (e.g. Zenodo). Associating this long term storage with a persistent identifier (e.g. a Digital Object Identifier - DOI) will greatly assist reproducibility through operation of the exact version used to generate the research results. Findability of the software by the research community is improved as these DOIs are indexed and can be used to persistently and reliably point to this storage.  

3. Retrieval

    A preserved software package as well as its dependencies need to be clearly labeled and identified with a suitable meta-data to be included in catalogs to improve findability. Where possible and appropriate, dependencies should be bundled with the software package. Including these dependencies helps ensure accurate reproducibility by ensuring the exact version of the dependencies are used when validating results. In addition, this bundling helps prevent the preserved software from being unusable if the dependencies cannot be retrieved in the future, thereby improving the overall software accessibility. See the [`left-pad` debacle](https://qz.com/646467/how-one-programmer-broke-the-internet-by-deleting-a-tiny-piece-of-code) for an example of how the deletion of a simple, minor dependency crippled web development across the globe.  

5. Construction

    To ensure the software can be rebuilt using the preserved software source code and reinstalled within a replica of the environment so that it will execute exactly as expected, adequate descriptive documentation of the compilation and operation environment is required.  

6. Replay

    Document test cases and include test data that demonstrate the preserved software and to help verify the executing software is producing the the correct, expected results. This replay relates to the construction and documentation aspect above. The software documentation should include detailed instructions on how to install, configure, use and test the software. Replay future users and maintainers understand the software's functionality, dependencies and assumptions, ensuring its continued consistency and usability.  

Preserved research software should include everything needed to reproduce the environment, execution and results for longevity of the same.  

Continuously improved research software requires ongoing maintenance and updates to address bugs, security vulnerabilities, and changing dependencies, environments and requirements. Establishing plans to support this development helps ensure that the software remains functional and up to date. In addition, encouraging and supporting a community around the software contributes to its sustainability. Researchers can engage with users, contributors, and stakeholders by fostering communication channels, providing support, and encouraging collaboration. A vibrant community can help maintain and enhance the software over time. This would require a proper transfer of knowledge about the research software from researchers to the community through adequate documentation.  

Addressing these aspects in a research software management plan helps support both preserved and continuously improved research software long into the future.  
