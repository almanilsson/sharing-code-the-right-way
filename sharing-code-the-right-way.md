# DDLS Annual Conference 2025

**Workshop 2: Open Source Software for Research – Sharing Code and Software the Right Way**
*By Alma Nilsson, Open Science Team, SciLifeLab Data Centre*

Most of us know open source as "a good thing we should be participating in", and might recognise high level ideas like making research software *findable, accessible, interoperable,* and *reusable*. But what does that actually mean in practice, especially for research code? Research software can be anything from a short CWL workflow used only once to large, long-running projects like [Percolator](https://github.com/percolator/percolator), used for peptide identification in proteomics for years. When code is part of the research method, sharing it is essential for transparency. Without it we simply can not review or verify whether the work was done correctly.

What’s less clear is *how* to apply these principles. How to go beyond simply uploading code to GitHub and actually make it understandable and even reusable. In other words, how to share code *the right way*.

This tutorial will take you through how to apply the [Open Software Checklist](https://github.com/ScilifelabDataCentre/open-science-checklists), developed by the SciLifeLab Open Science Team.

## The Messy Repository

We’ll be working with a deliberately “messy” example repository for **[insert repo name/function here]**. But this tutorial is probably more useful if you apply it to your own repository (not saying yours is messy).

Our example repository shows what many real world research repositories look like, even those linked to fancy publications. In fact, I got through my university journal clubs mostly by critiquing the state of development repos linked to papers - how accessible or reusable they were - and the state of open research software did not look great. **add reference to how many are made available**

Many researchers hesitate to share their code because they feel it’s “not good enough”, or because it seems like too much work. We’re here to improve and build confidence in sharing. Your code is good enough to be shared, adn any small improvement is progress. Today we hope to make that process as easy as possible.


## Task 1: Identify problems

Start by looking through your repository and going over the [Open Software Checklist](https://github.com/ScilifelabDataCentre/open-science-checklists/blob/main/open_software_checklist.md) point by point. Note which items are fully, partially, or not at all fulfilled. Based on what we’ve discussed ([Presentation PDF](OBS_ADD_LINK!!)) about *why* and *how* to do open source, identify the areas that could affect the openness or FAIRness of your code.
TODO:Alma, link the presentation here - should also live in this repo.

Write them down! And remember that not every checklist point will apply to your repository. For example, modular code might not be relevant if you’re only sharing a few workflows, and software testing isn’t crucial if you’ve only got a single preprocessing script. So don’t worry if many boxes stay unchecked.

## Task 2: Solve Problems

These notes will form the basis of what we’ll be working on. Since the checklist can be a little too general and hard to understand, we’ll break each point down into:
**what needs to be addressed | what issue it causes | how to solve it.**

Now let’s go through the checklist points one by one, in order of priority (according to me), and fix them. Please note that the provided solutions are not the only options, but have been made simple and direct so you can just get them done.

### Host Code in a Public Version-Controlled Repository/ The code isnt public or version controlled 

> **Host Code in a Public Version-Controlled Repository:** Host your code on platforms like GitHub, GitLab, or CodeBerg to track development history, enable tagged versioned releases, improve reusability, and support collaboration.

If your code is already on GitHub, great! You can mentally (or literally) tick this one off.

**What needs to be addressed**
The code isn’t stored in a public repository that keeps track of changes over time. Version control lets you see what has been done and makes the code easier to review and improve.

**What issue it causes**
If your code isn’t in a public repository that records version history, you can’t see how it developed or which version produced certain results. It also makes it harder for others, or even your own team, to follow the process and work on the code together

**How to solve it**
Upload your code to a public version-controlled platform like GitHub.


### Choose an Open-Source Licence 
> **Choose an Open-Source Licence:** Select an appropriate licence ([MIT License](https://choosealicense.com/licenses/mit/), [Apache License](https://choosealicense.com/licenses/apache-2.0/), or [GPL License](https://choosealicense.com/licenses/gpl-3.0/)), e.g., using [Choose a License](https://choosealicense.com/). If your repository also contains non-software content (e.g., website text or documentation), consider adding a separate licence for that, such as [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Note that code or content without a licence can not legally be reused, even if it is publicly available.

**What needs to be addressed**
The repository has no licence file that states how the code can be used, shared, or modified.

**What issue it causes**
If your code has no licence, it’s not legally reusable, even if it is accessible. 

**How to solve it**
Add a `LICENSE` file to your repository. Use a permissive licence such as the MIT Licence (SciLifeLab’s standard) by either selecting **“Add file → Choose a license template”** on GitHub or copying the official licence text from its website and pasting it into your `LICENSE` file.

If your repo includes other materials like text or figures, add a separate licence for those, for example, *CC BY 4.0*. If you mix different types (code, data, text), list each licence clearly in your `README` and specify what applies to what.

### Write a Structured README

> **Write a Structured README:** Create a machine-readable `README.md` (e.g. using [readme.so](https://readme.so/)) with installation instructions, usage examples, required prerequisites, contribution guidelines, and licence information. Machine-readable means structured in a way that allows automated tools to identify and extract information, for the README for example by using plain text Markdown section titles.

**What needs to be addressed**
The repository has no `README.md` file, or the existing one lacks clear sections such as repository description, usage and licence information.

**What issue it causes**
Without a structured README, it is hard to understand what the code does, how to install or use it, or how to contribute. 

**How to solve it**
Add a `README.md` file to the repository. Include at least a title and description, and the sections "Installation", "Licence" and "Citing this resource". 
You can create the file by clicking pre-made sections in [readme.so](https://readme.so/) and filling in the relevant information.
