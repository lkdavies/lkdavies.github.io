---
title: Process automation - Single-sourced code examples
date: 2026-03-06 00:00:00 -0800
#categories: [code_examples, example]
#tags: [code examples, automation]     # TAG names should always be lowercase
---

**Use case:**

JavaScript code examples for network edge functions lacked a single source, resulting in discrepancies between the code in a GitHub repo and the code examples in a developer guide on a different domain. It also took a long time to add new code examples across both locations: four hours per example. 

The solution was to automate publication from the GitHub repo to the developer guide, which required modifying an existing publication process and creating a template to capture metadata and proper content formatting across content sites.


**Skills I used:** 
- Systems thinking
- Cross-functional technical collaboration
- Process analysis and root cause diagnosis
- Information architecture 
- Template and governance design
- Metadata design and content modeling
- Automation and docs-as-code
- Technical scoping and project management

**What I did:**

- From my previous work with SDK engineers, I knew about a pipeline for **data plane** code examples that automatically published GitHub repo examples to the developer guide website. However, my examples were **control plane** examples that didn't fit the technical criteria. I consulted with the SDK engineers to confirm if it was possible to adapt my use case to use the existing pipeline. 
- I added a new category for the control plane code examples in YAML. The SDK team modified their existing architecture to override the default metadata and text for my category so I could add appropriate titles and descriptions for my examples. 
- I created metadata and text templates in YAML and Markdown, respectively. The templates ensured that code examples added to the GitHub repo would contain the correct metadata and text needed for the developer guide website.
- I identified a need to categorize the code examples by JavaScript runtime version, and collaborated with an SDK developer to add functionality that would publish this information, too. 
- I cleaned up and synced the existing code examples and tested the auto-publication functionality.
- I evangelized the new automated process with the network edge functions team.

**Result:**

With the templates and single-source publication functionality, adding a new code example now takes one hour instead of four, a time savings of 75%. When a developer or writer adds the example to the GitHub repo, it publishes to the developer guide site automatically.

[See a code example as published in the developer guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/example_cloudfront_functions_add_security_headers_section.html)

[See the source repo](https://github.com/aws-samples/amazon-cloudfront-functions/tree/main)
