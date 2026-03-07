---
title: AI assisted content - Developer tutorials at scale
date: 2026-03-06 00:00:00 -0800
categories: [tutorials, example]
tags: [tutorials, ai]     # TAG names should always be lowercase
---

**Use case:**

Developers asked for more comprehensive AWS command-line interface (CLI) tutorials. There were fewer CLI tutorials than web interface tutorials because of the labor and testing involved, and leadership moved up the date for completing the CLI tutorials. My team and I used generative AI and human-in-the-loop testing to develop prompt templates for creating the tutorials and testing them on actual AWS resources.

**Skills I used:** 
- Process design and standardization
- Prompt engineering and human-in-the-loop AI validation 
- Command line LLM testing and scripting
- Technical subject matter expertise (AWS CLI, AWS services)
- Error analysis and iterative improvement 
- Knowledge sharing and team collaboration 
- High-volume delivery under constraints 
- Open source contribution

**What I did:**

- Baseline testing with Amazon Q Developer CLI and Claude at the command line. Minimal prompting to create an Amazon CloudFront CLI tutorial based on an existing web interface tutorial. 
- Applied subject matter expertise and manually tested CLI commands and JSON inputs to identify and debug errors. Iterative prompting to address errors in output. 
- Shared test case notes with team. Feedback used to draft initial prompt templates. 
- Retested tutorial creation with prompt templates, continuing to test manually, re-prompt, and log errors for prompt template improvements.
- Ran prompt templates with test script that team created to address source of several errors (LLM not testing CLI commands against real AWS resources). Identified errors to improve in script.
- Tested Amazon CloudFront CLI tutorial manually. Used Amazon Q Developer to create a script that converted the Markdown output to XML for developer guide publication, with unique rules for our ZonBook-flavored schema.
- Using the refined prompt templates and test script, my team and I created additional CLI tutorials at scale. 

**Result:**

The prompt templates we developed were standardized so developers could use them with an LLM to generate their own tutorials for any AWS CLI scenario. We released the prompt templates into a public GitHub repo along with the Markdown CLI tutorials and Bash scripts we created. 

Ultimately, we delivered ~70 new CLI tutorials and Bash scripts in 60 days.

[See a tutorial example as published in a developer guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/get-started-cli-tutorial.html)

[See Markdown tutorials and Bash script examples in the public repo](https://github.com/aws-samples/sample-developer-tutorials/pull/1/changes/892db67fdac71444f80ceb2ca3a00ac0a86f01b5)
