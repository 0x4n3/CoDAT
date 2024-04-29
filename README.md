# CoDAT: Code Comprehension and Maintenance via Effective Documentation

Code Comprehension and Maintenance via Effective Documentation, or CoDAT, creates a narrative framework to engage developers in sustainable code documentation practices. CoDAT implements this vision by 

* **Change flagging**: The developer is alerted when a change occurs in code that needs to be reflected in its documentation.
* **Consistency Checking**: CoDAT has built in integrations to allow a 3rd party LLM to perform a "soft" check on if the code functionality matches the document's specifications.
* **Completeness Sieve**: CoDAT serves as a documentation sieve by allowing developers the ability to pinpoint syntax changes at a code sketch level.

## Implementation

CoDAT is currently implemented as an Intellij IDEA plugin. 

## Benefits in Cybersecurity

* Provides the ability for cybersecurity professionals to track what code changes frequently versus what code is stable. 
* Based on the stability, the code can then be designated as needing frequent or periodic reviews.

## Benefits in Company Liability

* Code reviews may only focus on if the code works and not necessarily if the documentation is accurate.
* As with cybersecurity, CoDAT can provide a stability verification to allow companies to have a way of externally validating their code.

# Biographies

## Dr. Paul Attie

Paul Attie is a Professor of Computer Science at Augusta University. He received a Ph.D. in Computer Science from the University of Texas at Austin in 1995.

Paul's research is in software engineering, formal methods, and distributed computing. He is currently interested in methods for the effective documentation and analysis of code.  He also works on devising efficient methods for specifying, designing, and reasoning about the behavior of large distributed and concurrent software systems. In particular, he showed that the safety, liveness, and deadlock-freedom of large concurrent programs can be established by reasoning about small sets (2 or 3) of component processes at a time, thereby avoiding state-explosion.

Paul has previously held faculty positions at Florida International University, Northeastern University, and the American University of Beirut.  He was also a Visiting Scientist and Research Affiliate at the MIT Computer Science and Artificial Intelligence Laboratory (CSAIL).

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
