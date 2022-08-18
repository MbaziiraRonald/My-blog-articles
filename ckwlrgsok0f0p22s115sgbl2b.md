## Git basics: The simple commands to begin with

In this series, we are going to look at the most basic, simple commands you can start with while just kick-starting your journey with Git (the most popular open-source Version Control System in use currently).

Keeping track of the changes in our code as developers can be quite a headache. But it does not have to be because Git has got you covered.

As a heads up, we assume you have already kick-started your journey with Git, but you are trying to get started with the basic commands, and you are having a bit of a migraine about it. That's where we've come in to help. We are going to assume that you also have some basic knowledge about the terminal since are your Git commands will be executed using the terminal.

Let's explore and learn these simple Git commands so that you can even explain them to your 5-year-old brother. 

Let's roll this thing. 


### Git config command <br>
This command is used to configure settings accompanying your use of git on your local machine/computer. Here are the major settings and configurations executed with this command. You can configure these settings on a global or local level.

**NB:** <br>
Your username and email should be the same as those on your GitHub or any service provider you use to store your code for example Bitbucket. 

- 
Name (username) <br>
***git config --global user.name  "username"*** <br>
This command is used to create a username for the computer on a global level.


- 
Email (email address) <br>
**git config --global user.email  "email address"** <br>
This command is used to create an email address on the computer for the global user.


- 
Default Editor (Code Editor) <br>
**git config --global core.editor  "code"** <br>
This command sets the specified code editor as your default editor.



### Initializing a repository <br>
**git init** <br>
This command is used to initialize a new repository on your machine/computer in the current folder or any other folder you may want


 ### Git add command  <br>
This command is used to do quite several tasks with flags attached to it at the end.  Let’s look at the major 3 tasks this command executes in detail. 

**Adding a new branch to the repo.** <br>
This task itself has 3 simple major commands that can help reach your goal depending on the direction you want to take. Here they are.


- 
**git branch < new name >** <br>
This command creates a new branch in the repository but keeps you at the current branch. 


- 
**git checkout -b < new name >** <br>
This command creates a new branch in the repository and takes you to the newly created branch.


- 
**git checkout -b < new name > < another name >** <br>
This command creates a new branch in the repository from another branch.

**Adding new changes (staging the changes)** <br>

- 
**git add < file.ext >** <br>
This command adds changes to the specified file to the staging area in the repository.


- 
**git add .** <br>
This command adds changes of all files in the repository to the staging area.
You can also add a directory to a repo by using the command "git add < directory name >" 

**Adding a remote repo <br>**

- 
**git remote add < alias name > < URL >** <br>
This command is primarily used to add a remote repo.


### Git commit command <br>
The commit command enables you to commit (or submit, if you will) all changes to the repo. It has two main implementations, which are:


- 
**git commit -m < message > ** <br>
This command commits all staged changes to the repository. Keep in mind that the message should be a short description of what the snapshot represents.


- 
**git commit -a**  <br>
This command commits all the local changes in tracked files.


### Ignoring files <br>
You can also ignore tracking certain files in certain directories like log files.


- 
**< dir name >/*** <br>
This command enables you to ignore all files in a specified directory. Where there is <dir name>, you replace it with the name of the directory whose files you want to ignore. 


- 
***.< file extension > ** <br>
This command enables the .gitignore file to ignore all files with a specified extension. This must be added to the .gitignore file. 


- 
For example, * .css tells git ignore to ignore all CSS files. <br>
* .jxt tells git ignore to ignore all files in the JavaScript XML format.


### Cherry pick command <br>
**git cherry pick < commit-hash > < commit-hash >**<br>
This command enables you to apply one or commits from other branches to the current working branch. This can come in handy when time is not on your side while working on a project.


### Git rename command <br> 
This command enables you to rename branches, files, and URLs with flags attached to them at the end. 


- 
**git branch -m < new name of branch >** <br>
This command allows you to rename the current working branch you are in.


- 
**git branch -m < old name of branch > < new name to give branch >** <br>
This command allows renaming any branch that exits in the repo even though you may not at the moment, be working in that branch.


- 
**git mv file_from file_to** <br>
This command allows renaming a file from its old name to the one you want to give it.


- 
**git remote rename < old name > < new name >** <br> 
This command allows you to rename the remote repo from its old name to the new one you want.


### Git merge command <br>
The merge command allows merging two or more branches or files to keep track of the changes in either branch or files.


- 
**git merge < branch name >** <br>
This command allows you to merge another branch to the current branch.


- 
**git checkout < branch name > < path to file > --patch** <br>
This command allows you to merge a single file from one branch to another.


### Conclusion
This is the end of part 1 of this series my friends, I will be publishing part 2 soon. So be sure to check out my blog so you do not miss it. 


## Before you go
Thank you for reading the article and I hope you found it helpful. Consider sharing it with your friends. ❤️

If you liked this article, feel free to visit me on [Twitter](https://twitter.com/mbaziiraronn). I regularly post content there. It is basically the platform where you will find my content first before it lands on my blog or somewhere else.
