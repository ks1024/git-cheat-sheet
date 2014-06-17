<p align="center">
	<img alt="Git" src="./img/git-icon.png">
</p>
<p align="center">Hi, this is a quick tour to using Git.</p>

## Creating repositories

Create a new local repository with the specified name

```
$ git init [project-name]
```

Clone a remote repository to your local machine

```
$ git clone [url]
```

## Making changes

Once you've made changes to your files, you can list all new or modified files waiting to be commited

```
$ git status 
$ git status -s	 
# -s : short format
```

Add changes (new or modified files) to the **Index**

```
$ git add [file-name]
# add a specified file
$ git add *			
# add all changed files
```

Commit changes to **HEAD**

```
$ git commit -m "commit message"
```

Now that your changes are in the **HEAD** of your local working directory, which means they are ready to be pushed to your remote repository in Github, then push your changes 

```
$ git push [alias] [branch-name]
$ git push origin master
# push commits to your remote repository (master branch) stored on github 
```

## Branching

For creating a new branch

```
$ git branch [branch-name]
```

For switching to the specified branch 

```
$ git checkout [branch-name]
```

Or you can directly switch to the new branch after creating it

```
$ git checkout -b [branch-name]
```

You can list all local branches in your current working directory.
The current branch will be highlighted with an asterisk (`*`)

```
$ git branch
  develop
* master
```

You can use `-a` to shows all local and remote branches

```
$ git branch -a
  develop
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/develop
  remotes/origin/master
  remotes/upstream/master
```

Or use `-r` to show only remote branches

```
$ git branch -r
  origin/HEAD -> origin/master
  origin/develop
  origin/master
  upstream/master
```

You can delete a specified branch

```
$ git branch -d [branch-name]
```

## Adding a remote

To add a new remote, use the `git remote add` command in your working directory

```
$ git remote add [alias] [url]
```

For an original repo that you've forked

```
$ git remote upstream https://github.com/username/repo.git
# When a repo is cloned, it has a default remote called origin that points to 
your fork on GitHub, not the original repo it was forked from. To keep track of 
the original repo, you need to add another remote named upstream
```

For your own repo on Github

```
$ git remote origin https://github.com/yourname/repo.git
```

Then you can list your remote aliases

```
$ git remote
origin
master
$ git remote -v
origin	https://github.com/yourname/repo.git (fetch)
origin	https://github.com/yourname/repo.git (push)
upstream	https://github.com/username/repo.git (fetch)
upstream	https://github.com/username/repo.git (push)
```

## Synchronize changes

If the original repo you forked gets updated, you can fetch any new changes from the original repository by running

```
$ git fetch upstream [branch-name]
```

Combines any changes fetched into current local branch

```
$ git merge [alias]/[branch-name]
$ git merge upstream/master
# merges changes fetched into your working files
```

Uploads all local branch commits to Github

```
$ git push [alias] [branch-name]
```

You can also use `git pull` to get commits from a remote repository

```
$ git pull 
# when you use git pull, git will merge any pulled commits into the branch 
you are currently working in which may run into frequent conflicts
```







