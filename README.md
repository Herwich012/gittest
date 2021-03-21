# How to branch, add/edit code and merge
- **Always** check wether your local repository is up-to-date with the remote repository!
```
$ git fetch
```
- If your local repository is not up to date, merge these fetched changes with your local repository:
```console
$ git pull
```
### Making a new branch
- Add a new branch:
```console
$ git branch my_branch
```

- Switch to the new brach:
```console
$ git checkout my_branch
```

- Check on what branch you are:
```console
$ git branch -v
```

It will returns something like
```console
* my_branch
  default_branch
```
### Working with your branch
This means that you are on the newly created branch! (in our case the default_branch is the `mavlabCourse2021` branch)
Now you can add features/fix bugs on the part of the code you are working on without altering the default branch. Along the way, you can update your branch by carrying out the following procedure:

- List new or modified files not yet committed:
```console
$ git status
```

Here you see the changes made to exsiting files (tracked) and newly created files (untracked). 

- Stage all these files, ready for commit:
```console
$ git add .
```

or 
```console
$ git add [file]
```

to stage a specific file for commit.

- Commit the changes to your local repository:
```console
$ git commit -m "commit messsage"
```

- Push the local changes to the remote repository so that others can pull them again
```
$ git push OurGroupRemote my_branch
```

Note: when pushing for the first time, the branch has been added to the remote repository for everyone to see, otherwise they would not have been aware of a newly created branch!

### Merging branches
When done implementing your changes to the code, the branch is ready to be merged to the default branch. This is done by first moving back to the default branch, and from there you merge my_branch to it. For best pracises concerning merging, [check this article](https://dev.to/neshaz/how-to-use-git-merge-the-correctway-25pd).

- 'Move' to the main branch again:
```
$ git chechout default_branch
```

- Merge your branch with the main/default:
```
$ git merge my_branch
```

### Deleting branches (after merging!)
After merging, my_branch has pretty much fulfilled it's purpose. It is thefore best practise to delete it in order to keep the project clean. For more info [check this article](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/).

- Delete the branch locally:
```
$ git branch -d my_branch
```

- Delete the branch on the remote:
```
$ git push OurGroupRemote --delete my_branch
```

## All done! you can now collab using git like a pro! :)

### Further reading:
- [Merging and managing conflicts](https://dev.to/neshaz/how-to-use-git-merge-the-correctway-25pd)
- [Deleting a branch](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/)
