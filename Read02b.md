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
