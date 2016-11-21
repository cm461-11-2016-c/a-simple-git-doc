12. Git Merge

#git merge
Git merge is used for merging the current branch into the other branch.
When we merge 2 branches the has a different commits history, the result is a recursive merge.
When we merge branches that is in the same timeline, the result is a fast-forward merge.

#git merge with --no-ff
When we merge development branch into stable branch, we may choose to git
merge with option --no-ff . This means even the stable branch can be fast
forward, we still want a new commit to create. In such case, when we git log the
graph, we can always see that that is a merge with 2 parents node.

#git merge and git pull
Git pull is git fetch and git merge combined.
Git pull will automatically merge the remotely changed code
into your local branch.
You can git fetch first, exam the changed. If no issues found, you may merge it.

#git merge and conflicts
When we try to merge 2 branches which edit the same line of
source file, conflicts happen.
Conflicts need to be solved by human.

#undoing merge
The git-scm has a blog post that talk about undoing merges.
http://git-scm.com/blog/2010/03/02/undoing-merges.html
