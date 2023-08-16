---
title: "git cheat sheet"
date: 2022-10-27
draft: false
summary: 自己整理的git cheat sheet
---

### 配置:

$ git config --global user.name "[name]"
Sets the name you want attached to your commit transactions

$ git config --global user.email "[email address]"
Sets the email you want attached to your commit transactions



## Create repositories

When starting out with a new repository, you only need to do it 
once; either locally, then push to GitHub, or by cloning an 
existing repository.

$ git init

 git clone [url]
 $ git clone [url]
Clone (download) a repository that already exists on 
GitHub, including all of the files, branches, and commits

## The .gitignore file

Sometimes it may be a good idea to exclude files from being 
tracked with Git. This is typically done in a special file named
 .gitignore . You can find helpful templates for .gitignore
files at github.com/github/gitignore.


## Make changes

Browse and inspect the evolution of project files

$ git add [file]
Snapshots the file in preparation for versioning

$ git commit -m "[descriptive message]"
Records file snapshots permanently in version history
  
## remote

 $ git fetch
Downloads all history from the remote tracking branches
$ git merge
Combines remote tracking branch into current local branch
 $ git push
Uploads all local branch commits to GitHub
  $ git pull
Updates your current local working branch with all new 
commits from the corresponding remote branch on GitHub. 
 git pull is a combination of git fetch and git merge 


 ## branch

 $ git branch [branch-name]
Creates a new branch

$ git checkout [branch-name]
Switches to the specified branch and updates the 
working directory

$ git merge [branch]
Combines the specified branch’s history into the 
current branch. This is usually done in pull requests, 
but is an important Git operation.


$ git branch -d [branch-name]
Deletes the specified branch


## Redo commits

Erase mistakes and craft replacement history

$ git reset [commit]
Undoes all commits after [commit], preserving changes locally

$ git reset --hard [commit]
Discards all history and changes back to the specified commit

## Glossary
git: an open source, distributed version-control system
GitHub: a platform for hosting and collaborating on Git repositories
commit: a Git object, a snapshot of your entire repository compressed into a SHA
branch: a lightweight movable pointer to a commit
clone: a local version of a repository, including all commits and branches
remote: a common repository on GitHub that all team member use to exchange their changes
fork: a copy of a repository on GitHub owned by a different user
pull request: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated 
tests, and more
HEAD: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits 
when using git checkout


repository

    A collection of refs together with an object database containing all objects which are reachable from the refs, possibly accompanied by meta data from one or more porcelains. A repository can share an object database with other repositories via alternates mechanism.


master

    The default development branch. Whenever you create a Git repository, a branch named "master" is created, and becomes the active branch. In most cases, this contains the local development, though that is purely by convention and is not required.

origin

    The default upstream repository. Most projects have at least one upstream project which they track. By default origin is used for that purpose. New upstream updates will be fetched into remote-tracking branches named origin/name-of-upstream-branch, which you can see using git branch -r.

  submodule

    A repository that holds the history of a separate project inside another repository (the latter of which is called superproject).

tag

    A ref under refs/tags/ namespace that points to an object of an arbitrary type (typically a tag points to either a tag or a commit object). In contrast to a head, a tag is not updated by the commit command. A Git tag has nothing to do with a Lisp tag (which would be called an object type in Git’s context). A tag is most typically used to mark a particular point in the commit ancestry chain.

   
branch

    A "branch" is a line of development. The most recent commit on a branch is referred to as the tip of that branch. The tip of the branch is referenced by a branch head, which moves forward as additional development is done on the branch. A single Git repository can track an arbitrary number of branches, but your working tree is associated with just one of them (the "current" or "checked out" branch), and HEAD points to that branch.

checkout

    The action of updating all or part of the working tree with a tree object or blob from the object database, and updating the index and HEAD if the whole working tree has been pointed at a new branch.

commit

    As a noun: A single point in the Git history; the entire history of a project is represented as a set of interrelated commits. The word "commit" is often used by Git in the same places other revision control systems use the words "revision" or "version". Also used as a short hand for commit object.

    As a verb: The action of storing a new snapshot of the project’s state in the Git history, by creating a new commit representing the current state of the index and advancing HEAD to point at the new commit.

fetch

    Fetching a branch means to get the branch’s head ref from a remote repository, to find out which objects are missing from the local object database, and to get them, too. See also git-fetch[1].

HEAD

    The current branch. In more detail: Your working tree is normally derived from the state of the tree referred to by HEAD. HEAD is a reference to one of the heads in your repository, except when using a detached HEAD, in which case it directly references an arbitrary commit.

merge

    As a verb: To bring the contents of another branch (possibly from an external repository) into the current branch. In the case where the merged-in branch is from a different repository, this is done by first fetching the remote branch and then merging the result into the current branch. This combination of fetch and merge operations is called a pull. Merging is performed by an automatic process that identifies changes made since the branches diverged, and then applies all those changes together. In cases where changes conflict, manual intervention may be required to complete the merge.

    As a noun: unless it is a fast-forward, a successful merge results in the creation of a new commit representing the result of the merge, and having as parents the tips of the merged branches. This commit is referred to as a "merge commit", or sometimes just a "merge".

pull

    Pulling a branch means to fetch it and merge it. See also git-pull[1].
push

    Pushing a branch means to get the branch’s head ref from a remote repository, find out if it is an ancestor to the branch’s local head ref, and in that case, putting all objects, which are reachable from the local head ref, and which are missing from the remote repository, into the remote object database, and updating the remote head ref. If the remote head is not an ancestor to the local head, the push fails.

gitfile

    A plain file .git at the root of a working tree that points at the directory that is the real repository.
