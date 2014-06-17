<p align="center">
	<img alt="Git" src="./img/git-icon.png">
</p>
<p align="center">Hi, this is a quick tour to using Git.</p>

## Create repositories

Create a new local repository with the specified name

```
$ git init [project-name]
```

Clone a remote repository to your local machine

```
$ git clone /path/to/repository
```

## Make changes

Once you've made changes to your files, you can list all new or modified files waiting to be commited

```
$ git status 
$ git status -s	// -s : short format
```

Add changes (new or modified files) to the **Index**

```
$ git add [file-name]	// for a file with the specified name
$ git add *			// all files changed
```

Commit changes to **HEAD**

```
$ git commit -m "descriptive message"
```

Now that your changes are in the **HEAD** of your local working directory, which means they are ready to be pushed to your remote repository in Github, then push your changes 

```
$ git push origin [branch-name]
```

## Branching

You can list all local branches in your current working directory.
The current branch will be highlited with an asterisk (`*`)

```
$ git branch
*gh-pages
```

For creating a new branch

```
$ git branch [branch-name]
```

For switching to the specified branch 

```
$ git checkout [branch-name]
```

or you can switch to it just after creating a new branch

```
$ git checkout -b [branch-name]
```

