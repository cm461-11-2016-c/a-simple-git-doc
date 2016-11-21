Git Commit
=============

git-commit - Record changes to the repository

DESCRIPTION
=============

Stores the current contents of the index in a new commit along with a log message from the user describing the changes.

The content to be added can be specified in several ways:

1. by using git add to incrementally "add" changes to the index before using the commit command (Note: even modified files must be "added");

2. by using git rm to remove files from the working tree and the index, again before using the commit command;

3. by listing files as arguments to the commit command (without --interactive or --patch switch), in which case the commit will ignore changes staged in the index, and instead record the current content of the listed files (which must already be known to Git);

4. by using the `-a` switch with the commit command to automatically "add" changes from all known files (i.e. all files that are already listed in the index) and to automatically "rm" files in the index that have been removed from the working tree, and then perform the actual commit;

5 by using the `--interactive` or `--patch` switches with the commit command to decide one by one which files or hunks should be part of the commit in addition to contents in the index, before finalizing the operation. See the “Interactive Mode” section of git-add[1] to learn how to operate these modes.

OPTIONS
=======

**-a**

**--all**

Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.


EXAMPLES
========

When recording your own work, the contents of modified files in your working tree are temporarily stored to a staging area called the "index" with git add. A file can be reverted back, only in the index but not in the working tree, to that of the last commit with git reset HEAD -- <file>, which effectively reverts git add and prevents the changes to this file from participating in the next commit. After building the state to be committed incrementally with these commands, git commit (without any pathname parameter) is used to record what has been staged so far. This is the most basic form of the command. An example:

	$ edit hello.c
	$ git rm goodbye.c
	$ git add hello.c
	$ git commit

