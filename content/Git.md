---
title: Git
---
Status: 
Tags: 
Links: [Coding MOC](out/coding-moc.md)
___
# Git
> [Guide](https://git-scm.com/book/en/v2/)
- [Updating a local clone with new branch name](out/updating-a-local-clone-with-new-branch-name.md)
## Commands
Keep credentials: `git config --global credential.helper store`
Show credentials: `cat  ~/.git-credentials`

`git rebase {branch}`
- Introduce changes from main to feature branch
- edit commit history using `git rebase -i {branch}`

Merge conflicts
- `git merge {branch}`
- `git rebase {branch}`

Revert
- `git revert {commit hash}`
- 

Merging vs rebasing
- Merging pros
	- Easier, simpler to resolve
	- Extra commit
- Rebase pros
	- More control over history
	- Cleaner history
### Groupwork
**![](https://lh5.googleusercontent.com/p3ZQ1kscAlg1X-Ok5iFOT3HU_bUZy3Bh1xc4lV5YZshEyS1uBrOlYn_IArZTSED5Pr4yDnPvONXsD2g2waBctOaTbTCcB5TEGnnJoFuut1IVfvQTI4n7FqokiMu5jzI_pNCpBF4xIpXS)**
___
# Backlinks
```dataview
list from [Git](out/git.md)
```
___
References: 

Created:: 2021-07-15 23:07
