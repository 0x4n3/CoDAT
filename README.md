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

# Biographies

## Dr. Paul Attie

Paul Attie is a Professor of Computer Science at Augusta University. He received a Ph.D. in Computer Science from the University of Texas at Austin in 1995.

Paul's research is in software engineering, formal methods, and distributed computing. He is currently interested in methods for the effective documentation and analysis of code.  He also works on devising efficient methods for specifying, designing, and reasoning about the behavior of large distributed and concurrent software systems. In particular, he showed that the safety, liveness, and deadlock-freedom of large concurrent programs can be established by reasoning about small sets (2 or 3) of component processes at a time, thereby avoiding state-explosion.

Paul has previously held faculty positions at Florida International University, Northeastern University, and the American University of Beirut.  He was also a Visiting Scientist and Research Affiliate at the MIT Computer Science and Artificial Intelligence Laboratory (CSAIL).

## Mr. Anas Obeidat

Anas Obeidat is a seasoned software engineer with over 13 years of experience specializing in Java tools and technologies. He currently serves as a Senior Developer at Avanos Medical, focusing on the EtQ Reliance framework since March 2020. Anas has a strong background in both front and backend development, expertly handling Java, Python, JavaScript, HTML, CSS, and various databases such as Oracle, DB2, SQL Server, and MySQL.

His educational background includes a Master’s Degree in Computer Science from MUM University, obtained between 2010 and 2013, and earlier studies at Jami'at Al-Balqa Al-Tatbiqiyya, where he earned both his BSc and another Master's in Computer Science by 2009. Currently, Anas is pursuing his PhD in Computer and Cyber Sciences at Augusta University.

Previously, Anas has demonstrated significant impact in roles such as a Web Developer at Excellence through Quality (EtQ), where he improved the EtQ Reliance system, and a Senior Developer at United Airlines, where he developed solutions for merging applications in the Safety and Security department using the EtQ Reliance framework.

His technical expertise is complemented by strong problem-solving skills, evident from his successful development and deployment of a CRM system for telemarketing companies, which led to a notable increase in lead conversion rates from 20% to 60%. Anas is also proficient in Agile and Scrum methodologies, ensuring timely and effective project delivery.

Anas is certified as a Sun Certified Web Component Developer (SCWCD) and a Sun Certified Programmer for the Java 2 Platform (SCJP), underscoring his deep knowledge and expertise in the field. His professional journey reflects a commitment to excellence and a deep understanding of technological solutions that enhance business operations and user experiences.

## Mr. Nathaniel Oh

Mr. Oh has over 10 of experience working in cybersecurity in both industry and academia settings. Mr. Oh currently is pursuing his PhD in Computer and Cyber Sciences at Augusta University while working as a Vulnerability Research SETA for ARPA-H. Prior to pursuing his doctorate, Mr. Oh worked as a Senior Cybersecurity Professional at Tyler Technologies where he assisted clients in securing their network and assessed their production binaries and environments. Mr. Oh has given technical talks and has taught advanced computer science and cyber security concepts to both industry professionals and academic peers. 

Mr. Oh has earned over 115 certifications in fields ranging from computer science, cybersecurity, and machine learning. He holds certifications from several industry leaders such as Microsoft, Cisco, IBM, CompTIA and OffSec. His certifications include the OSCE3, CASP+, CCNA, and many more. 

Mr. Oh holds a Bachelor of Science degree in Applied Mathematics from American Military University and an Associate of Science degree in Mathematics from Anne Arundel Community College.

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
