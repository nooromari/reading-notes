# GitHub

##### In order to explain Git, we have to first explain various aspects of Version Control.

## Version Control

is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. 

### Local Version Control

A Local VCS entails one database on your hard disk that stores changes to files.


### Centralized Version Control (CVCS)

This system entails a single server storing all changes and file versions, which can be accessed by various clients. allowed programmers to have more knowledge of team members’ activities with certain files by eliminating the need to involve all local databases. But the server as a single point if it has a failure the collaborators cannot work with each other on a file or save changes and new versions.


### Distributed Version Control (DVCS)

Addresses the major vulnerability of the a CVCS by allows clients to create mirrored repositories. These data backups can be easily by placed on the server to replace any lost information.


 ![](https://s26500.pcdn.co/wp-content/uploads/2019/09/VCS_Diff.png)
 
 
 
## So, what is Git?

Git is a DVCS that stores data in a file system made up of **snapshots** . Each time you save (commit) a changed version of your project Git creates a snapshot of the file and stores a reference to it. Also, Git mostly relies on local operations because most necessary information can be found in **local resources** . This allows for process expediency because a project’s history resides on the local disk and allowing one to continue work on a project even when not online or on a VPN.
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.
In addition, It is set up to greatly minimize the possibility of irreversible damage to files. That makes it extremely difficult to lose committed files. In the last, Files in Git can reside in three main states: committed, modified and staged.


![](https://static.javatpoint.com/tutorial/git/images/git-index.png)


### Download Git  

In order to use Git, your computer must have it available. If you already have Git on your computer, you should make sure you have the latest version.

For Git install you can see more [here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#4_1)

*After making sure Git has been installed, you should perform some steps.*

You can follow it from the image below or from link [here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#4_3)

![](https://rubygarage.s3.amazonaws.com/uploads/article_image/file/599/git-cheatsheet-5.jpg)



## Workflow

### Local Repository Structure

The local Git repository has three components:

1. Working Directory: The actual files reside here.
2. Index: The area used for staging
3. Head: Points to the most recent commit


### Saving Changes

All files in a checked out (or working) copy of a project file are either in a tracked or untracked state.

- Tracked : unmodified, or staged; they were part of the most recent file snapshot.

- Untracked : not in the last snapshot and do not currently reside in the staging area.


### The Life Cycle of File Status

After you edit a file, Git flags it as modified because of changes made after the previous commit and stage the modified file.Then, you commit staged changes.

![](https://git-scm.com/figures/18333fig0201-tn.png)


And for more detales you can press [here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#5)

##### Go back from [here](https://nooromari.github.io/reading-notes/summarize)








