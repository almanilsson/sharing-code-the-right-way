# DDLS Annual Conference 2025

**Workshop 2: Open Source Software for Research – Sharing Code and Software the Right Way**
*By Alma Nilsson, Open Science Team, SciLifeLab Data Centre*

Most of us know open source as "a good thing we should be participating in", and might recognise high level ideas like making research software *findable, accessible, interoperable,* and *reusable*. But what does that actually mean in practice, especially for research code? Research software can be anything from a short CWL workflow used only once to large, long-running projects like [Percolator](https://github.com/percolator/percolator), used for peptide identification in proteomics for years. When code is part of the research method, sharing it is essential for transparency. Without it we simply can not review or verify whether the work was done correctly.

What’s less clear is *how* to apply these principles. How to go beyond simply uploading code to GitHub and actually make it understandable and even reusable. In other words, how to share code *the right way*.

This tutorial will take you through how to apply the [Open Software Checklist](https://github.com/ScilifelabDataCentre/open-science-checklists), developed by the SciLifeLab Open Science Team.

## The Messy Repository

We’ll be working with a deliberately “messy” example repository for **[insert repo name/function here]**. But this tutorial is probably more useful if you apply it to your own repository (not saying yours is messy).

Our example repository shows what many real world research repositories look like, even those linked to fancy publications. Currently, the state of open research software does not look great. **TODO: add reference to how many are made available** 

Many researchers hesitate to share their code because they feel it’s “not good enough”, or because it seems like too much work. We’re here to improve and build confidence in sharing. Your code is good enough to be shared, and any small improvement is progress. Today we hope to make that process as easy as possible.


## Task 1: Identify problems

Please note that any imporvement towards openness is great. In this tutorial we want you to start working on the openness of your repository, that might involve implementing two or three of the checklist points, but we do not by any means expect you to do it all. In fact, not every checklist point will apply to your repository. For example, modular code might not be relevant if you’re only sharing a few workflows, and software testing isn’t crucial if you’ve only got a single preprocessing script. So don’t worry if many boxes stay unchecked.

Start by looking through your repository and going over the [Open Software Checklist](https://github.com/ScilifelabDataCentre/open-science-checklists/blob/main/open_software_checklist.md) point by point. Note which items are fully, partially, or not at all fulfilled. Based on what we’ve discussed ([Presentation PDF](OBS_ADD_LINK!!)) about *why* and *how* to do open source, identify the areas that could affect the openness or FAIRness of your code. Write them down! 
TODO:Alma, link the presentation here - should also live in this repo.

## Task 2: Solve Problems
Now let’s solve the checklist points one by one, in order of priority (according to me), and fix them. Please note that the provided solutions are not the only options, but have been made simple and direct so you can get them done quickly.

Since the checklist can be a little too general and hard to understand, we’ll break each point down using the following format:

#### Title prompt (what should be done)

> Checklist point from the open software checklist
 
**What needs to be addressed** 
**What issue it causes** 
**How to solve it**


### 2.1 Highest priority points

#### 2.1.1 Host Code in a Public Version-Controlled Repository/ The code isnt public or version controlled 

> **Host Code in a Public Version-Controlled Repository:** Host your code on platforms like GitHub, GitLab, or CodeBerg to track development history, enable tagged versioned releases, improve reusability, and support collaboration.

If your code is already on GitHub, great! You can mentally (or literally) tick this one off.

**What needs to be addressed**
The code isn’t stored in a public repository that keeps track of changes over time. Version control lets you see what has been done and makes the code easier to review and improve.

**What issue it causes**
If your code isn’t in a public repository that records version history, you can’t see how it developed or which version produced certain results. It also makes it harder for others, or even your own team, to follow the process and work on the code together

**How to solve it**
Upload your code to a public version-controlled platform like GitHub.


#### 2.1.2 Choose an Open-Source Licence 
> **Choose an Open-Source Licence:** Select an appropriate licence ([MIT License](https://choosealicense.com/licenses/mit/), [Apache License](https://choosealicense.com/licenses/apache-2.0/), or [GPL License](https://choosealicense.com/licenses/gpl-3.0/)), e.g., using [Choose a License](https://choosealicense.com/). If your repository also contains non-software content (e.g., website text or documentation), consider adding a separate licence for that, such as [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Note that code or content without a licence can not legally be reused, even if it is publicly available.

**What needs to be addressed**
The repository has no licence file that states how the code can be used, shared, or modified.

**What issue it causes**
If your code has no licence, it’s not legally reusable, even if it is accessible. 

**How to solve it**
Add a `LICENSE` file to your repository. Use a permissive licence such as the MIT Licence (SciLifeLab’s standard) by either selecting **“Add file → Choose a license template”** on GitHub or copying the official licence text from its website and pasting it into your `LICENSE` file.

If your repo includes other materials like text or figures, add a separate licence for those, for example, *CC BY 4.0*. If you mix different types (code, data, text), list each licence clearly in your `README` and specify what applies to what.

#### 2.1.3 Write a Structured README

> **Write a Structured README:** Create a machine-readable `README.md` (e.g. using [readme.so](https://readme.so/)) with installation instructions, usage examples, required prerequisites, contribution guidelines, and licence information. Machine-readable means structured in a way that allows automated tools to identify and extract information, for the README for example by using plain text Markdown section titles.

**What needs to be addressed**
The repository has no `README.md` file, or the existing one lacks clear sections such as repository description, usage and licence information.

**What issue it causes**
Without a structured README, it is hard to understand what the code does, how to install or use it, or how to contribute. 

**How to solve it**
Add a `README.md` file to the repository. Include at least a title and description, and the sections "Installation", "Licence" and "Citing this resource". 
You can create the file by clicking pre-made sections in [readme.so](https://readme.so/) and filling in the relevant information.


### 2.2 Additional points

#### Archive and Assign a Persistent Identifier

> **Archive and Assign a Persistent Identifier:**  Ensure long-term preservation by depositing a snapshot of a specific software release (e.g., v1.0.0) in repositories that assign a PID such as [Zenodo](https://zenodo.org/), [Software Heritage](https://www.softwareheritage.org/), or your local institutional repository (e.g., [SciLifeLab Data Repository](https://figshare.scilifelab.se/)). This complements hosting code in a public repository by providing a fixed reference that can be cited in publications and matched to data and results.

This is a high priority item since it ensures your code can be persistently linked and cited. However, it does not need to be done during the tutorial. It is best completed once todays openness updates are done.

**What needs to be addressed**
The software has not been archived or assigned a persistent identifier for longterm access.

**What issue it causes**
Without a persistent identifier, references/links to the code may change or break over time. This makes citations unreliable and can prevent others from finding the code ( or correct version). Especially if the code is updated, renamed or moved.

**How to solve it**
Upload your code to Zenodo (by integrating Zenodo with your GitHub repository or by uploading manually) or another archive that gives it a DOI.
Follow the steps to upload your code here: https://help.zenodo.org/docs/github/

#### Provide Descriptive Metadata

> **Provide Descriptive Metadata:** Include essential details such as title, authors, version, licence, DOI and keywords. This can be done in a `CITATION.cff` file. For more extensive metadata, you can also create a `codemeta.json` file using tools like the [CodeMeta generator](https://codemeta.github.io/codemeta-generator/), which can then be added to public and preservation repositories (e.g. GitHub, Zenodo). One such file can be seen [here](https://github.com/cboettig/codemeta/blob/master/codemeta.json). Optionally, include a contributors table in your `README.md` (e.g., [The Turing Way's Contributors Table](https://book.the-turing-way.org/community-handbook/acknowledgement/acknowledgement-record)), or frameworks like [All Contributors](https://allcontributors.org/) to make roles and credit visible.

**What needs to be addressed**
The repository does not include structured metadata describing key information.

**What issue it causes**
Without clear metadata, the code is harder to find, cite and connect to related research outputs. Missing author or licence information can also make attribution unclear.

**How to solve it**
Add a `CITATION.cff` file including title, authors, version, licence, (DOI, if available) and keywords.

#### Use Package Managers (and Manage Them Wisely): 

> **Use Package Managers:** Specify dependencies via [package managers](https://en.wikipedia.org/wiki/List_of_software_package_management_systems) (e.g., pip, npm, mamba) for better compatibility and reproducibility. Include a dependency file (e.g. `requirements.txt`, `environment.yml`, or `package.json`) to allow others to easily install the necessary packages. Consider adding a lock file to ensure exact versions are used across environments.

> **Manage Dependencies Wisely:** Use well-maintained libraries and avoid obsolete and redundant dependencies  so the software continues to work as intended over time.

Note that these two points are combined since both relate to dependency , though the main focus is on the first one. As you review and collect your dependencies, check if they are trustworthy and actively maintained so your software continues to work as intended.

**What needs to be addressed**
Dependencies are not specified.

**What issue it causes**
Without a defined dependencies others can not easily use your code (and outdated packages may break the software or create security risks).

**How to solve it**
List all required dependencies in a file such as `requirements.txt` or `environment.yml`. Preferably also specify version ranges (e.g. `wordfreq>=3.0,<4.0`).

#### Use Descriptive Names 

> **Use Descriptive Names:** Choose consistent and descriptive names for variables, functions to make code easy to read and understand. See [The Turing Way Guidelines for Code Styling](https://book.the-turing-way.org/project-design/info-management/code-styling/code-styling-guidelines) 

**What needs to be addressed**
Variable and function names are unclear, inconsistent, or too short to describe their purpose.

**What issue it causes**
Unclear naming makes the code harder to read, understand, and maintain. Both for you and for new users.

**How to solve it**
Use short but descriptive names that reflect what the variable or function does. Follow a consistent naming style (for example, `snake_case` in Python or `camelCase` in JavaScript) throughout the code.


#### Write Clear Documentation 

> **Write Clear Documentation:** Provide concise instructions, usage examples, and inline comments to help others understand and use the code. See [CodeRefinerys Modular Code Development lesson](https://cicero.xyz/v3/remark/0.14.0/github.com/coderefinery/modular-code-development/master/talk.md/#1) for more information.

**What needs to be addressed**
The documentation is incomplete or does not exist, and the code lacks comments showing how it should be used.

**What issue it causes**
Others may be unable to understand or built upon the code. It also makes it harder for you and collaborators to maintain it later.

**How to solve it**
Add concise instructions and usage examples in your `README.md`, or for larger projects, create full documentation (e.g. a GitHub Pages or ReadTheDocs site). Write short, but informative, inline comments explaining what each part of the code does.


#### Include Example Use Cases 

>  **Include Example Use Cases:** Provide example use cases via sample scripts or [Jupyter notebooks](https://jupyter.org/) (see [notebook guidance](https://zenodo.org/records/5651648) on documenting your workflow). Include small example datasets with your software to ensure others can test and reproduce your results. If including data in the repository is not feasible (e.g. due to size limits or policies), share it via platforms like [Zenodo](https://zenodo.org/) or reuse existing publicly available datasets.

**What needs to be addressed**
The repository does not include example use cases or sample data showing how the software can be applied.

**What issue it causes**
Without clear examples others may not understand how to runthe code, or what format the data needs to be in if applied to another dataset.

**How to solve it**
Add a small example dataset, and a short script, description in the README or a Jupyter notebook that demonstrates how to use the code, and on what type of data. Include expected results for the user to compare to.

#### Follow Code Formatting Standards 

> **Follow Code Formatting Standards:** Use recognised open standards, style guides, linters, and formatters to keep code clean and consistent. Common examples include Black and Pylint (Python). See the [Netherlands eScience Center Guide](https://guide.esciencecenter.nl/#/) for language-specific examples and [The Turing Way’s overview of static analysis tools](https://book.the-turing-way.org/reproducible-research/code-quality) for formatter options.


**What needs to be addressed**
The code does not follow consistent formatting standards, such as indentation, spacing, line length, or naming conventions, and no automated tools are in place to check or enforce them.

**What issue it causes**
Inconsistent formatting makes the code harder to read, and increases the chance of small avoidable errors.

**How to solve it**
Look up and follow the standard formatting guide for your programming language, or install a linter to apply it automatically (for example, using the guide linked above).

#### Use Issue Tracking & Discussionss 

> **Use Issue Tracking & Discussions:** Enable GitHub Issues, forums, or mailing lists to gather community feedback and improve software. Consider building a backlog with clearly identified “Starter Issues” to help new contributors find small, manageable issues to start on.

**What needs to be addressed**


**What issue it causes**


**How to solve it**

#### Set Up Contributing Guidelines 

> **Set Up Contributing Guidelines:** Create a `CONTRIBUTING.md` file to guide community contributions. Credit them according to “Ensure Proper Credit” above.

**What needs to be addressed**
The repository does not include a `CONTRIBUTING.md` file describing how others can report issues, suggest changes, or contribute code.

**What issue it causes**
People who want to report an issue or contribute may not know how to do so which could, for example, lead to bugs being unnoticed.

**How to solve it**
Add a `CONTRIBUTING.md` file that covers how to suggest changes, open issues, and submit pull requests (and if you want that at all). It can also include information on coding style, the review process and how (if) contributors will be credited.


#### Write Modular Code 

> **Write Modular Code:** Logically break up code into functions and modules to make it easier to read, avoid repetition, simplify testing, and improve long-term maintainability. Avoid hardcoding details like file paths or settings by passing them as inputs instead. See [The Turing Ways Detailed Recommendations for Code Reuse](https://book.the-turing-way.org/reproducible-research/code-reuse/code-reuse-details#re-runnable-recommendations) for more information.

**What needs to be addressed**
The code is written without functions or separate modules.

**What issue it causes**
Long and unstructured code blocks are hard to read, test and rework. They may be repetitive and run less efficiently, and changing one part can easily break others.

**How to solve it**
Split the code into smaller, non-repetative, parts and call them as functions. Pass (and define well) inputs like file paths or settings as arguments instead of hardcoding them.

#### Define Input/Output Schemas 

> **Define Input/Output Schemas:** Use formats like [JSON Schema](https://json-schema.org/) to clearly describe the structure of your software’s inputs and outputs.

**What needs to be addressed**
The software does not clearly define what inputs it expects or what outputs it produces. There is no structured description of their type, use or content.

**What issue it causes**
It becomes unclear what the code expects, returns and how to adapt it to new data.

**How to solve it**
Define expected inputs and outputs (the type, what it is used for and what it contains) in each functions docstring and describe their structure in your documentation. Formally describe input and output data, for example using JSON schema. 

#### Implement and Automate Software Testing 

> **Implement and Automate Software Testing:** Include unit tests and integration tests so the software continues to work as intended over time, using frameworks like [PyTest](https://docs.pytest.org/en/stable/), [Jest](https://jestjs.io/), or [Mocha](https://mochajs.org/). Use CI/CD tools like GitHub Actions and GitLab CI to streamline testing and deployment.

**What needs to be addressed**
The software does not include tests to check that it works correctly (or they are not automated).

**What issue it causes**
When changes are made, new errors can go unnoticed and it is hard to confirm that the full software still works as expected.

**How to solve it**
Add simple unit tests for key functions using a testing framework such as PyTest. Preferably, set up automated testing with GitHub Actions so tests run automatically when the code is updated and notifies you if something is wrong.

#### Define Governance for Long-Term Maintenance 

> **Define Governance for Long-Term Maintenance:** Outline roles, responsibilities, and decision-making processes for sustaining your software project over time.

**What needs to be addressed**
It is not clear who, how and if the code will be maintained (updated over time).

**What issue it causes**
Users may assume the software is actively maintained and safe to build upon or include in their workflows, but without maintenance unpatched bugs or security issues can arise and create risks for those who reuse it.

**How to solve it**
Decide and communicate (for example, in the `README.md`) whether the code will be maintained. If it will be, specify who is responsible and how maintenance will be handled.

#### Structure Your Code for Reuse (Bonus BETA point)

TODO: perhaps not include?
> **Structure Your Code for Reuse:** Organise your software in a logical, modular way with well-defined user interaction (for example, a CLI), so it can be easily reused or extended, for example in a pipeline. This can be done by creating a package, module, or library depending on your programming language.

**What needs to be addressed**
The software is not organised in a way that supports reuse, and lacks a clear interface for how users should interact with it.

**What issue it causes**
The software may be harder to integrate into other workflows or pipelines. Users may not know how to run or reuse it safely.

**How to solve it**
Organise the code into logical modules or functions and define a clear way for users to interact with it, such as a command line interface or callable functions.

#### Use a Clear Versioning Scheme 

> **Use a Clear Versioning Scheme:** Label official releases of software using a consistent versioning system, such as [Semantic Versioning (SemVer)](https://semver.org/) (`major.minor.patch`), tagging the exact commit related to each release. This makes each version unambiguously citable and reusable.

**What needs to be addressed**
The software does not use a consistent versioning system or clearly label official releases.

**What issue it causes**
Users can not tell which version of the software they are using or citing. This can make it harder to track changes, reproduce results, or identify when updates introduce issues.

**How to solve it**
Use a clear versioning system such as Semantic Versioning (major.minor.patch). Tag each release (via command line or the GitHub interface) in your repository.


#### Establish a Code of Conduct 

> **Establish a Code of Conduct:** Define expectations for community interactions using a `CODE_OF_CONDUCT.md` file (e.g., [Contributor Covenant](https://www.contributor-covenant.org/)), and include a contact method for reporting violations.

**What needs to be addressed**
The repository does not include a `CODE_OF_CONDUCT.md` file describing how contributors and users are expected to interact.

**What issue it causes**
Misunderstandings or conflicts may arise, and contributors may feel unsure how to, or if they should, report issues.

**How to solve it**
Add a `CODE_OF_CONDUCT.md` file using a standard template such as the [Contributor Covenant](https://www.contributor-covenant.org/). Include a contact email or form for reporting violations or concerns.

#### Add Repository Badges 

>  **Add Repository Badges:** Include badges for citation (e.g., Zenodo DOI), licence, build status, and community standards. You can create and customise badges via [shields.io](https://shields.io/).

**What needs to be addressed**
The repository does not include badges showing for example citation, licence or build information.

**What issue it causes**
Users can not see key information quickly which might lead to, for example, less accurate citation.

**How to solve it**
Create and customise badges using shields.io or get them from the platforms they represent (GitHub Actions, Zenodo, or licence metadata). Add them as linked images to your `README.md`.

#### Containerise Your Software 

> **Containerise Your Software:** Provide instructions to create consistent, portable environments using [Docker](https://www.docker.com/) or [Singularity](https://github.com/apptainer/singularity), by including a Dockerfile or equivalent build instructions. This improves transparency and ensures your software runs reliably across different systems, thus enhancing reproducibility and simplifying deployment.

**What needs to be addressed**
The software does not include a container or build instructions to reproduce its runtime environment.

**What issue it causes**
Without a container, the software may behave differently on other systems due to differences in things like dependencies or operating systems.

**How to solve it**


### Points not addressed

- Develop a Software Management Plan (SMP)
- Cite Your Software in Publications
- Declare Software Availability in Publications

These points are outside the scope of this tutorial but should be considered when starting a new project. Some researchers include software in their Data Management Plan (DMP), while others create a separate Software Management Plan (SMP). In any case, software should be covered by some form of management plan, and as we’ve emphasised throughout, **code is part of the research method and should therefore be linked and cited in publications**.
