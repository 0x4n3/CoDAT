# Introduction

## Why Document Code? 

* Code is notoriously difficult to understand
* Huge "semantic gap" between what the code looks like and what it actually does at runtime. This gap is responsible for:
    * Bugs, including security bugs which lead to exploits
    * Failures in deployed systems
    * Cost overruns/missed deadlines/project cancellation

## The Traditional Code Review
 
According to the landmark study, "Comparing the Effectiveness of Software Testing Strategies" by Basili and Selby:

> With the professional programmers, code reading detected more software faults and had a higher fault detection rate than did functional or structural testing.”

Thus, code reviews themselves serve an important role in secure software development. However, the implementation can severely impact the effectiveness of a code review. 

## How Documentation Supports Code Reviews

Based on the paper, "Comments on Comments: Where Code Review and Documentation Meet" by Rao, et. al. We observe the following: 

* There is a parallel between documentation and code reviews. 
* Oftentimes, it's been found that strong documentation aids in a strong code review.

In addition, according to "Code Reviews Do Not Find Bugs" by Czerwonka, et. al. There are two key factors in where current code reviews fall short: 

* Current code reviews are informal and asynchronous
* Commenting and documentation standards are loosely defined and heavily influenced by reviewer’s experience

There exists a need to approach the intersection of Code Reviews and Documentation in both a strategic and measured way. 

# CoDAT: Code Comprehension and Maintenance via Effective Documentation

## The Code Review Vision

1. We need a way to formalize small-scale code reviews that support a larger base of code. 
2. Frequent and dynamic is better than formal and static.
3. Model behavior based off of source control systems such as Git or Subversion. 

## The Components of CoDAT

Code Comprehension and Maintenance via Effective Documentation, or CoDAT, creates a narrative framework to engage developers in sustainable code documentation practices. CoDAT implements this vision by 

* **Change flagging**: The developer is alerted when a change occurs in code that needs to be reflected in its documentation.
* **Consistency Checking**: CoDAT has built in integrations to allow a 3rd party LLM to perform a "soft" check on if the code functionality matches the document's specifications.
* **Completeness Sieve**: CoDAT serves as a documentation sieve by allowing developers the ability to pinpoint syntax changes at a code sketch level.

## How CoDAT Supports the Code Review Vision

1. *We need a way to formalize frequent small-scale code reviews that support a larger base of code.*

CoDAT tracks both design and code changes, allowing developers the ability to monitor not only the code’s performance but also its expectations. 

For example, if the program specifications change but the code is not updated, the outdated function may provide incorrect parameters to a callee. This can cause severe problems that may be hard to detect without CoDAT. 

2. *Frequent and dynamic is better than formal and static.*

CoDAT allows for developers to asynchronously sign areas whose documentation and code are invariant. 

If areas of signed code change, CoDAT can then alert the user of the design or code change. Allowing developers the ability to solely focus on actively changing code or documentation.

If changed code or documentation impacts other areas, CoDAT can implement signature detection to determine the area and scope of impact within a program.

3. *Model behavior based off of source control systems such as Git or Subversion.*

CoDAT integrates existing Source Control Systems to provide extensive tracking with both an individual developer and an asynchronous team.

This allows CoDAT to be scaled to match the need within an arbitrary program or development environment.

# Applications of CoDAT

## Cybersecurity

* Provides the ability for cybersecurity professionals to track what code changes frequently versus what code is stable. 
* Based on the stability, the code can then be designated as needing frequent or periodic reviews.

## Mitigating Company Liability

* Code reviews may only focus on if the code works and not necessarily if the documentation is accurate.
* As with cybersecurity, CoDAT can provide a stability verification to allow companies to have a way of externally validating their code.

## Reverse Engineering

* CoDAT can be refactored to monitor basic blocks and pseudocode similar to how IDA syncs function prototype signatures with disassembled opcodes.

# Installation

## Step 1: Access the Plugin Repository

1. Open Web Browser:
    * Launch your web browser and navigate to the GitLab project repostiory with [https://gitlab.com/nathanieloh2/AU-CSCI-7130-Project/-/tree/main/Intellij-Plugin](https://gitlab.com/nathanieloh2/AU-CSCI-7130-Project/-/tree/main/Intellij-Plugin)

2. Download the Plugin JAR:
    * Within the `Intellij-Plugin` directory, locate the file `AU-CSCI-7130-Project-Intellij-Plugin-1.0-SNAPSHOT.jar` or the relevant JAR file for your plugin.
    * Click on the file to open its details page and then click the "Download" button to save the JAR file to your computer.

## Step 2: Install the Plugin in Intellij IDEA

    1. Launch Intellij IDEA

    2. Install the Plugin
        * Navigate to `File > Settings` on Windows/Linux or `IntelliJ IDEA > Preferences` on macOS.
Select Plugins from the sidebar.
        * Click on the gear icon (⚙️), then choose `Install Plugin from Disk....`
        * Browse to the location where you downloaded the `.jar` file, select it, and click `OK`.

    3. Restart IntelliJ IDEA

## Step 3: Verify the Plugin Installation

    1. Check Plugin Status
        * After restarting IntelliJ IDEA, open the `Settings` or `Preferences` again.
        * Go to the `Plugins` section and verify that your plugin is listed and enabled.

    2. Test Plugin Functionality
        * Activate the plugin features within IntelliJ IDEA to confirm that everything is working as expected.
        * Evaluate the plugin's functionality, such as code suggestion or comment tracking, to ensure it meets project specifications.
