<p align="center">
	<img alt="Git" src="./img/git-icon.png">
</p>
<p align="center">A simple guide to using Git.</p>

## Install Git

[Github for Windows](https://windows.github.com)

[Github for Mac](https://mac.github.com)

[Github for Linux](http://git-scm.com/book/en/Getting-Started-Installing-Git)


## Create repositories

Create a new local repository with the specified name

```
git init [project-name]
```

Create a working copy of a local repository

```
git clone /path/to/repository
```

## Make changes

Lists all new or modified files waiting to be commited

```
git status
```

Add changes (new or modified files) to the **Index**

add a file with the specified name

```
git add [filename]
```

add all files

```
git add *
```

Commit changes

```
git commit -m "descriptive message"
```

