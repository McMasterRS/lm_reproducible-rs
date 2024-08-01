---
layout: default
title: Ethics, Licensing & Legal Compliance
parent: Software Management Plan
nav_order: 4
---

# Ethics

Research software often deals with sensitive data, such as personal information or proprietary data. Ethical considerations ensure that software developers implement appropriate security measures and adhere to data protection regulations. Researchers must also obtain informed consent from participants and handle data in a way that respects privacy rights, maintains confidentiality and informs uses.  

If your software collects and stores any data from your users, ideally you will want to host your software and data from a Canadian location. Data hosted exclusively in Canada have some protection through federal and provincial laws. Data hosted outside Canada may be subject to foreign laws and may be open to data seizure or surveillance by foreign entities or international security agencies. For more details, please refer to the [Summary of Privacy Laws in Canada by the Office of the Privacy Commissioner of Canada](https://www.priv.gc.ca/en/privacy-topics/privacy-laws-in-canada/02_05_d_15) and [Government of Canada White Paper: Data Sovereignty and Public Cloud](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/cloud-services/gc-white-paper-data-sovereignty-public-cloud.html).  

When considering where data may be stored, also consider where your software operates as it may require data to be transmitted to that location as well. Also consider where any third party software or services are hosted. Third parties may have secondary services, servers or backup storage outside of their declared country. Third parties may also have partner agreements with other companies with similar foreign country hosting and transmission scenarios or external data sharing agreements. All of these data hosting and transmission locations are relevant when evaluating data security, privacy and use.  

Some tools and services may use data to further train their systems, such as, but not limited to, generative artificial intelligence tools and large language models. This data retention and use must also be considered.  

Research software should be developed and used in a way that promotes inclusivity and minimizes biases, such as machine learning models. Ethical considerations involve ensuring software tools do not discriminate against certain groups, provide equal opportunities for participation and consider diverse perspectives. At the very least, these biases need to be documented and declared. Developers need to be aware of biases that may be present in algorithms or data, and work to address them.  

# Licensing & Legal Compliance

> **DISCLAIMER**: The following content is intended to highlight resources which may be useful to those developing open source research software. This content is for informational purposes only. It is **NOT** legal advice. McMaster University and McMaster Research Software Development Team are not responsible for the content referenced in this guide, nor any and all costs, claims, losses, damages, expenses which may result through the application of this information. Be sure to contact a professional for legal advice.

It is encouraged to assign an appropriate license for your research software project. When choosing a license, consider the following:  

- Are modifications/distributions of the software possible with/without reference to your name, organization and the license you have chosen?
- Is the software available for commercial use?
- Do you or your organization own/use any patents in the research software project?
- Do the tools or libraries used to develop the software require you to reference the source? Are there restrictions or requirements that are carried forward to your software?

Where possible, use existing licenses, such as GNU General Public License or MIT License, rather than creating custom terms of use. These are some resources for comparing different licenses:  

- [Open Source Licenses (OSI)](https://opensource.org/licenses/)
- [choosealicense.com](https://choosealicense.com/licenses/)

Where possible, try to use the same licenses for all software components. Software license restrictions and requirements are transitive, i.e. are carried forward to any software that uses them, unless the license states explicitly otherwise. Software use is greatly simplified if there is only one license to review, thereby improving the FAIR accessibility and reusability of the software.  

Should I share my research data and software source code using the same Creative Commons license? Normally it is recommended to use the same licenses wherever possible. Unfortunately, in the case of Creative Commons licenses, and similar, this practice should be avoided. The Creative Commons Organization strongly recommends against using Creative Commons licenses for software in its [Frequently Ask Questions](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software):  

> Unlike software-specific licenses, CC [Creative Commons] licenses do not contain specific terms about the distribution of source code, which is often important to ensuring the free reuse and modifiability of software. Many software licenses also address patent rights, which are important to software but may not be applicable to other copyrightable works. Additionally, our licenses are currently not compatible with the major software licenses, so it would be difficult to integrate CC [Creative Commons] -licensed work with other free software. Existing software licenses were designed specifically for use with software and offer a similar set of rights to the Creative Commons licenses.

Ethical considerations extend to intellectual property and licensing in research software development. Developers should respect copyright, properly attribute existing software components, and consider open source licensing when appropriate. These practices help ensure the fair, responsible and legal use of intellectual property.  
