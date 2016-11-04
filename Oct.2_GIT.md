# [**Git**](https://git-scm.com/blog)
```
git stash
```
[stash](https://www.atlassian.com/git/tutorials/git-stash/#re-applying-your-stashed-chang): temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on.
```
git clean
```

```
git pull --rebase origin master
```
1. —-rebase: avoid to use;
2. git pull --> git merge (handle conflict) --> git push
```
	(my_branch) $ git add .
	(my_branch) $ git commit -m "..."
	(my_branch) $ git checkout devel
	(devel) $ git pull origin devel
	(devel) $ git merge my_branch
	(devel) $ git push origin devel
```

```
git reset --hard HEAD
```
1. HEAD: pointer to last commit snapshot
2. --hard: resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded.
3. [Read...](http://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit)
