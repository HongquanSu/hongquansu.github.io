---                                                                                                                                                                         
layout: default
title: "Useful tools for Astronomy"
tagline: 
---

## Git

### Basic 

Clone a git repo :
```
git clone [repo_url]
```

Add a file to the repo :
```
git add [file_name]
```

Save changes locally :
```
git commit
```

Caching your GitHub password in Git :
```
git config --global credential.helper cache
```

Save the committed changes to the remote :
```
git push
```

### Branch

See all branches :
```
git branch
```

Change working branch :
```
git checkout [branch_name]
```

Create a branch and switch in this branch :
```
git checkout -b [branch_name]
```

Push a branch on github (be sure to be in this branch) :
```
git push origin [branch_name]
```

Delete a local branch :
```
git branch -d [branch_name]
```

To force the deletion of local branch :
```
$ git branch -D [branch_name]
```

Delete the branch on github :
```
git push origin :[branch_name]
```

Remove multiple files that have already been deleted from disk :
- To stage your whole working tree:
```
git add -u :/
```
- To stage just the current path:
```
git add -u .
```




