# Revisions and the cloud

## Version Control

A system that allows you to view previous versions of recorded files. This Version Control System (VCS) allows the user to revert, track, modify, and compare files.

### Local Version Control

A LVCS stores the file changes to a database on a local drive.

### Centralized Version Control

A CVCS stores the changes on a server that can be accessed by multiple clients. This system removed the involvement of multiple local databases and streamlined the process of many individuals collaborating on a team.

### Distributed Version Control

A DVCS also stores the changes on a server, but also allows individuals to mirror the repositories within their local storage. This creates many data backups and, in the case of server failure, prevents the loss of valuable data.

## Git

Git is a DVCS that snapshots file changes, called commits, and stores references to them. 

### Cloning in Git

The act of creating a copy of an existing Git repository. 

Cloning copies all versions of all files for a project.

### Tracking and Staging

Tracked files are working copies of files that can be modified, unmodified, or staged. Staged files are modified files that are prepped for commiting.

- To track and stage a single new file:

  > git add filename

- Multiple files:

  > git add *

### Snapshotting

Git snapshots the changes made to the files once you commit them.

- To commit a file:

  > git commit -m "comment on what changed"

- To commit all changes:

  > git commit -a

### Pushing

In order to send the changes to the remote repository in Github, you will have to use the push command.

- To push changes from local to remote:

  > git push origin master
