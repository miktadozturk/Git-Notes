# Git

Git is a tool that we use for version control. When you're in a git repository (which is just a directory with a ```.git``` directory in it), git tracks all changes for you and lets you package and label them. This is immensely useful when you want to retrace how and why a piece of software was written. And it is equally useful for undoing changes and getting back to earlier versions of your work. There is a lot to know about git, but to get started, let's get acquainted with the basic git workflow you'll be using every day at Spiced.

# Check the status
Check what changes you have in your repository. Is everything as it should be?

```git status```

# Adding.
Commit the files in your directory that you have worked on and that you want to be included in the next commit. For example:

```git add index.html style.css```

OR, if you just want to add all the changes there are:

```git add .```

The add command adds your changes to the staging area. This means they are ready to be committed.

# Check the status (again)
Check what changes you have in your repository. Is everything as it should be?

```git status```

# Committing
```git commit -m "added new JS modules, need styling"```

Committing makes a commit with your specified message. These changes have now been packaged and labelled but the commit is still just on your local computer.

# Check the status (are you seeing a pattern?)

Check what changes you have in your repository. Is everything as it should be?

```git status```

# Pushing
By pushing, you can send your commits to a remote repository on a different server. In our case, that is Github. ```git push origin master```

**origin** is name of the remote repository.

**master** is the branch. More on branches later....

You can use ```git push -u <remote_name> <local_branch_name>``` to set the default upstream. See the documentation for git push for more details.

When you git push take care to check the terminal output for any errors.

# Pulling
```git pull origin master```

This pulls commits from the remote repo that is located at origin.

# Branches
One of the most powerful and useful parts of git is its branches. By branching off, you can start to work on different versions of your code. So you can work on one branch, and not affect the other branch. Branches are typically used so members of a team can work on different features. But you can also easily create a branch to start an experiment when you're not yet sure if it's taking you in the right direction.

To make a new branch:
```git checkout -b <my_new_branch>```

To switch between branches
```git checkout <branch_i_want>```

To check your branches, and to see which one you are on:
```git branch```

To delete a local branch:
```git branch -D <branch_to_delete>```

You may also need the ```-f``` flag if you have unmerged changes. It may also prompt you to use the ```-D```.

```git checkout -b <my_new_branch> origin/master``` --> will create the new branch and automatically have it set to pull from master

# Bash programs you will use often
The list of the small programs that come with Bash is long. Here are the ones you will probably use most often.

- ```pwd``` - print working directory - this will show you your current location in the directory structure
- ```ls``` - list - lists all files and directories. when used with ```-a``` it will also show you hidden files ("dotfiles")
- ```cat``` - concatenate - print the content of a file to the terminal, i.e. ```cat hello.txt```
- ```cd```- change directory - used to switch to a different directory. for example ```cd dev/myproject```, ```cd ..``` or ```cd ~```
- ```touch``` - will create an empty file with the name you specify. for example, ```touch index.html```
- ```mkdir``` - make directory - creates a directory with the name you specify, for example ```mkdir images```
- ```rm``` - remove - removes a file or directory (when used with -r). for example ```rm index.html```
- ```mv``` - move - used to move or rename files. first specify the file, then the place you want to move it to or its new name.
- ```man``` - manual - when used with a command, shows you a help file. try ```man ls```
- ```ps``` - process status - get a list of all running programs/processes
- ```sudo``` - super user do - executes a command as the super user. i.e. ```sudo rm very-important-file.txt```

# Other Useful commands
```git remote -v``` --> check where the remote for your git repo is.

```git push origin :<branch_name>``` --> delete a REMOTE branch

```git clone <remote_repo>``` --> clone a remote branch to your local computer. This is what you use if you want to copy code from github onto your computer.
