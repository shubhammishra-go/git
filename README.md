# Git

Git is a `distributed version control system`. that tracks changes in any set of computer files, usually used for coordinating work among programmers who are collaboratively developing source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows (thousands of parallel branches running on different computers).

Git was originally authored by `Linus Torvalds` in 2005 for development of the `Linux kernel`, with other kernel developers contributing to its initial development.


![alt text](Git-logo.svg.png)


# About Version Control

Version control (also known as `revision control`, `source control`, or `source code management`) is a `class of systems` responsible for managing changes to computer programs, documents, large web sites, or other collections of information. Version control is a component of software configuration management.

![alt text](image.png)


# Why Version Control Systems Needed ?

Version control systems [VCS] also helps developers move faster and allows software teams to preserve efficiency and agility as the team scales to include more developers.

Some most common benefits of using VCS :::

1. A complete `long-term change history of every file`. This means every change made by many individuals over the years. Changes include the creation and deletion of files as well as edits to their contents. Different VCS tools differ on how well they handle renaming and moving of files. This history should also include the author, date and written notes on the purpose of each change. Having the complete history enables going back to previous versions to help in root cause analysis for bugs and it is crucial when needing to fix problems in older versions of software. If the software is being actively worked on, almost everything can be considered an "older version" of the software.


2. `Branching and merging`. Having team members work `concurrently` is a no-brainer, but even individuals working on their own can benefit from the ability to work on independent streams of changes. Creating a "branch" in VCS tools keeps multiple streams of work independent from each other while also providing the facility to merge that work back together, enabling developers to verify that the changes on each branch do not conflict. Many software teams adopt a practice of branching for each feature or perhaps branching for each release, or both. There are many different workflows that teams can choose from when they decide how to make use of branching and merging facilities in VCS.


3. `Traceability`. Being able to trace each change made to the software and connect it to project management and bug tracking software such as Jira, and being able to annotate each change with a message describing the purpose and intent of the change can help not only with root cause analysis and other forensics. Having the annotated history of the code at your fingertips when you are reading the code, trying to understand what it is doing and why it is so designed can enable developers to make correct and harmonious changes that are in accord with the intended long-term design of the system. This can be especially important for working effectively with legacy code and is crucial in enabling developers to estimate future work with any accuracy.


# Examples of Version Control Systems

![alt text](<1 _1IWN_hxJcf6yLR3j-xejQ.png>)

Github , Gitlab , Beanstalk , Apache Subversion , Mercurial etc...


# Types of Version Control Systems

There are two types of version control: `centralized` and `distributed`.


## Centralized version control system

A centralized version control system offers software development teams a way to collaborate using `a central server`.

![alt text](<1 GgaGcwh5L246YcU5NVDA5A.png>)

In centralized version control system a server acts as the main centralized repository which stores every version of
code. Using centralized source control, every user commits directly to the
main branch, so this type of version control often works well for small teams,
because team members have the ability to communicate quickly so that no two
developers want to work on the same piece of code simultaneously. Strong
communication and collaboration are important to ensure a centralized workflow
is successful.


### Examples of centralized version control system

Examples of centralized version control system such as `Concurrent Versions System (CVS)`, `Perforce`, and `Subversion (SVN)` that require users to pull the latest version from the server to download a local copy on their machine. Contributors then push commits to the server and resolve any merge conflicts on the main repository.


### Advantages of centralized version control system

`Works well with binary files` ::: Binary files, such as graphic assets and text files, require a large amount of space, so software developers turn to centralized version control systems to store this data. With a centralized server, teams can pull a few lines of code without saving the entire history on their local machine. Users of distributed systems have to download the entire project, which takes up time and space and prevents them from doing diffs. If a team works with binary files regularly, a centralized system offers the most efficient approach to code development.

`Offers full visibility` ::: With a centralized location, every team member has full visibility into what code is currently worked on and what changes are made. This knowledge helps software development teams understand the state of a project and provides a foundation for collaboration, since developers share work in the central server. A centralized version control system only has two data repositories that users have to monitor: the local copy and the central server.


`Decreases the learning curve ` ::: Centralized version control is easy to understand and use, so developers of any skill level can push changes and start contributing to the code base quickly. Setting up the system and the workflow is also simple and doesn't require a significant amount of time investment to establish how the software development team should use the tool. When developers can `navigate a workflow quickly and easily`, they're able to focus on feature development rather than memorizing a series of complicated steps to merge versioned changes. Decreasing the learning curve also helps new developers make an impact as soon as possible.


### Disadvantages of centralized version control system

`A single point of failure risks data ` ::: The biggest disadvantage is the single point of failure embedded within the centralized server. If the remote server goes down, then `no one can work` on the code or push changes. The lack of offline access means that any disruption can significantly impact code development and even result in code loss. The entire project and team comes to a standstill during an outage. In the event of hard disk corruption, software development teams must rely on backups to retrieve the running history of a project. If backups haven't been kept properly, then the team loses everything. When storing all versions on a central server, teams risk losing their source code at any time. Only the snapshots on local machines are retrievable, but that is a small amount of code compared to the entire history of a project.

Unlike a centralized VCS, a distributed version control system enables every user to have a local copy of the running history on their machine, so if there's an outage, every local copy becomes a backup copy and team members can continue to development offline.


`Slow speed delays development` ::: Centralized version control system users often have a difficult time branching quickly, because users must communicate with the remote server for every command, which slows down code development.

Branching becomes a time-consuming task and allows merge conflicts to appear, because developers can't push their changes to the central repository fast enough for others to view. If team members have slow network connections, the code development process becomes even more tedious when trying to connect with the remote server.

The speed at which software development teams operate has a direct impact on how quickly they can ship features and deliver business value. If teams are slow to develop, iteration and innovation stall and developers can become frustrated with how long it takes to see their changes in the application. Missed releases are possible if the remote server or networks are down, and team members won't be able to make up for lost time and quickly push changes.


`Few stable moments to push changes` ::: A centralized workflow is easy for small teams to utilize, but there are limitations when `larger teams` try to collaborate. When multiple developers want to work on the same piece of code, `it becomes difficult to find a stable moment to push changes.` Unstable changes cannot be pushed to the main central repository so developers have to keep them local until they're ready for release.

Because users delay pushing changes, software development projects can be delayed, and merge conflicts can arise, because the rest of the team doesn't have visibility into changes that exist only on a user's machine. Once changes are finally pushed to the central repository — after dealing with stability and speed issues — users will have to resolve conflicts quickly when merging to ensure the rest of the team can contribute to the code. The lack of stability is what leads many teams to migrate to a different version control system, such as Git.


## Distributed version control system

A distributed version control system (DVCS) brings a local copy of the complete repository to `every team member’s computer`, so they can commit, branch, and merge locally. The server doesn’t have to store a physical file for each branch — it just needs the differences between each commit.

![alt text](Git-a-Distributed-Version-Control-System.png)


Distributed version control systems help software development teams create strong workflows and hierarchies, with each developer pushing code changes to their own repository and maintainers setting a code review process to ensure only quality code merges into the main repository.


### Examples of distributed version control system

examples of distributed version control system such as `Git`, `Mercurial`, and `Bazaar`, mirror the repository and its entire history as a local copy on individual hard drives.


### Advantages of distributed version control system

`Reliable backup copies` ::: An interesting way to think about distribution version control is to visualize a collection of backups. When a team member clones a repository, she essentially creates an offsite backup, so if something catastrophic happens, like a server crash, every team member’s local copy becomes a backup. Unlike a centralized version control system, a distributed version control removes the reliance on a single backup, making development more reliable. A common misconception is that multiple copies could be a waste of space, but most development includes plain text files and many systems compress files, so the impact on hard drive storage is minimal.


`Fast merging and flexible branching ` ::: Because systems don’t require remote server communication, code can be quickly merged. A distributed version control also allows software development teams to use different branching strategies, a feature that isn’t possible with a centralized system. Distributed version control systems accelerate delivery and business value by helping team members focus on innovation rather than become bogged down with slow builds.


`Rapid feedback and fewer merge conflicts` ::: A  distributed version control system makes branching easy, because having an entire repository’s history on their local workstation ensures that they can quickly experiment and request a code review. Developers benefit from fast feedback loops and can share changes with team members before merging the changeset. Merge conflicts are less likely, because contributors focus on their own piece of code. Furthermore, having easy access to the full local history helps developers identify bugs, track changes, and revert to previous versions.

`Flexibility to work offline` ::: A distributed version control system doesn’t require an internet connection, so most development, except pushing and pulling, can be done while traveling or away from home or an office. Contributors can view the running history on their hard drive, so any changes will be made in their own repository. This increased flexibility enables team members to fix bugs as a single changeset. Increased developer productivity.

With a local copy, developers can complete common development activities rapidly. A DVCS means that developers no longer have to wait on a server run through routine tasks, which can slow down delivery and cause frustration.


### Disadvantages of distributed version control system

`Initial checkout of a repository is slower` as compared to checkout in a centralized version control system, because all branches and revision history are copied to the local machine by default.


`The lack of locking mechanisms` that is part of most centralized VCS and still plays an important role when it comes to non-mergeable binary files such as graphic assets or too complex single file binary or XML packages (e.g. office documents, PowerBI files, SQL Server Data Tools BI packages, etc.).[citation needed]


`Additional storage` required for every user to have a complete copy of the complete codebase history.


Increased exposure of the code base since every participant has a locally `vulnerable` copy.



## GitHub Authentication


First we need to configure username and email

`git config --global user.name shubhammishra-go`

`git config --global user.email shubham.....@gmail.com`

Than Create An access token goto Settings >>> Developer Settings 

Create an Auth URL

`git remote set-url origin https://<accessToken>@github.com/<githubUsername>/<repository>`


execute it on terminal , Done!





...



