# DevcamPortfolio
- rails generate scaffold Blog Title:string body:text

rake routes


### Initiating git inside application
> `git init`

 add particular file
> `git add <file_name>`
	
 adding everything 
> `git add .` or `git add --all` or `git add -A`
	
to see status
> `git status` and `git log`
	
 **USING gitignore file**
> gitignore is the way by which we can tell git that which file we don't want to checked into version control.

> Let suppose we don't out secrets file to not get checked into version control and we mention that in the gitignore file 
/config/secrets.yml  which currently i don't have in my application maybe because of different versions of rails.

>Therotically any changes that we make to the file should not be seen in the git status command but it shows 
also to remove any changes from specified file
 `git checkout /config/secrests.yml`

>Anyway

>git shows the ignored file because of git cached we have to clear out all of the cached
`git rm . -r --cached`
Now we should make commit of this tasks by mentioning that we have cleared cached and push the commit.
Now we can make changes in the file that we need it to be ignored and it will not be added into the repo.
it's going to remove all the cached now ignored file will not get seen as jordan said so but it didn't work for me i was trying this blogs_controller.rb file.


# Git Cheat Sheet

## Basic commands

> `git init` **Creates a new git repository in the directory**

> `git add <file name>` **Adds a specific file to staging**

> `git add .` or `git add -A` **Adds the full directory and its contents to staging**

> `git commit -m 'Commit message here'` **Commits the file changes in staging and provides a description for the commit**

> `git diff` **Analyze the differences between old files and ones that have been added to staging **


## Branching

> `git branch` **View all local branches**

> `git checkout -b <branch name>` **Create a new branch and check into it**

> `git branch -av` **View all branches local and remote**

> `git checkout <branch name>` **Switch into the specified branch**

> `git branch -d <branch name>` **Delete a specific branch**

> `git push origin <branch name>` **Push a branch to a remote repository**

> `git merge <branch name>` **Merge branch into master branch (ensure that you're inside the master branch)**


## Stashing

> `git stash` **Stashes changes in the .git file for temporaily hiding changed elements (make sure to run `git add` prior to stashing**

> `git stash apply` **Returns the stashed items**



## View History

> `git log` **View previous commits, their messages, and ids**

> `git log <file name>` **View who changed a specific file**

> `git blame <file name>` **View who changed a specific file**


## Reverting

> `git reset --hard HEAD` **Remove all changes and revert to the previous commit**

> `git checkout <file name>` **Remove changes made to a specific file, reverting it back to the previous commit**


## Merge Conflicts

> When you encounter a merge conflict, first... don't freak out. This just means you're being given the ability to choose which code you want to choose to go with.

### Sample Conflict

- You run `git pull` on a repo that has changes that conflict with your local copy.
- You're presented with the following error message:

```
error: The following untracked working tree files would be overwritten by merge:
README.md
Please move or remove them before you merge.
Aborting
```

### Natural Response

![large](https://s3.amazonaws.com/devcamp-static/images/cagey.jpg)


### How to Fix a Merge Conflict

> It's actually not that hard to fix merge conflicts, simply run `git status` and it will show you where the conflict exists. An example conflict might look like this:

```ruby
<<<<<<< HEAD
# Git Homepage
=======
# git-guide

> A guide for working with git
>>>>>>> a1dfac148fb86311a453a9de338e4d7b9389ade5
```

The `<<<<<<< HEAD`, `=======`, and `>>>>>>>` symbols are simply showing you where the conflict is. You have the choice to pick what you want to keep, what you want to remove, etc. After picking out the implementation that you want you can run:

- `git add .`
- `git commit -m 'some commit message'`
- `git push`

And you will be good to go.


## Cloning

> `git clone <link to repo>` **Clone a repository from a remote source, such as GitHub**


## Rebase

> `git rebase master` **While working on a branch you can bring in committed changes from another branch. This is helpful for ensuring that your feature branch can be cleanly merged with the master branch**



