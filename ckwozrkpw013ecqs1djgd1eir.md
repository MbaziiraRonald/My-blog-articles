# Git basics: The simple commands to begin with

Hooray! We are back. Let's look at the second and last of the series. In the first article, we looked at 8 major commands and the subcommands we can use under them.

In this second and last part of the series, we are going to look at 5 major commands and their subcommands.

If you haven't looked at the first article of the series, I encourage you to do so in order to follow along well. For those who have already done with the first article, let's roll this thing.

### Git modify command  

The modify command allows you to change your latest commit message, change your latest commit and leave the message the same or change the repo’s remote URL.

Let’s take a look at its implementation in detail.

```plaintext
  git commit --amend
```

This command allows you to change your latest commit message.

```plaintext
  git add .
  git commit --amend --no-edit
```

This allows you to change your latest commit but leave the commit message the same.

```plaintext
  git remote set-url <alias> <URL>
```

This command allows you to modify your remote repo’s URL.

### Viewing commands/status  

This command allows you to do quite a number of tasks. Here are the subcommands that fall under it:

```plaintext
  git status
```

This command allows you to view the status of your project i.e unstaged, staged, and untracked files.

```plaintext
  git log
```

This command allows you to view all commits logs or history.

```plaintext
  git diff
```

This command allows you to view uncommitted changes in your repo.

```plaintext
  git diff --staged
```

This command shows you staged changes in your repo.

```plaintext
   git remote -v
```

This command shows you your remote repo’s remote URL.

```plaintext
    git branch
```

This command allows you to view the branches on your repo.

```plaintext
     git tag
```

This command allows you to view the tags in your repo.

### Git clone command  

This command allows replicating ( making the same exact copy ) of a specific repo into a specified directory.

```plaintext
     git clone <repo-url> <directory>
```

This command allows you to clone an existing repo into a specified directory.

```plaintext
     git clone <repo-url> .
```

This command allows you to clone an existing repo into the current working directory.

```plaintext
     git clone --recurse-submodules <repo-url>
```

This command allows you to replicate the existing repo along with its submodules into the current working directory.

```plaintext
     git submodule update --init --recursive
```

This command allows you to replicate submodules after cloning the existing repo.

### Git delete command  

This command allows you to delete files, branches, tags, etc. Let’s look at what it can do in detail.

```plaintext
    git branch -D <branch name>
```

This command allows you to delete a specified branch.

```plaintext
    git branch -D <branch name> <branch name>
```

This command allows you to delete multiple branches by going on listing their names. There is also an option of deleting them with a regex pattern but that is out of the scope of this article.

```plaintext
    git tag -d  v<tag version>
```

This command allows you to delete a tag.

```plaintext
    git remote rm <remote>
```

This command allows you to delete a remote repo.

```plaintext
    git clean -<flag>
```

This command allows you to delete untracked files.

```plaintext
    git remote prune <remote-name>
```

This command allows you to delete local branches that don’t exist at the remote repo.

### Git revert command  

This command allows you to undo a specific command or action. Here is how it works:

```plaintext
    git revert <commit-hash>
```

This command allows you to reset a specific commit by using their hashes alongside them.

```plaintext
    git checkout <repo>/<branch>  <filename>
```

This command allows you to reset a specific file.

```plaintext
    git reset --hard
```

This command allows you to revert or go back to the latest commit.

```plaintext
    git reset --hard <repo>/<branch>
```

This command allows you to go back to the last commit on the remote branch.

## Conclusion

This is the end of part 2 of this series my friends. Thank you for reaching the end. 🙏

## Before you go

Thank you for reading the article and I hope you found it helpful. Please consider sharing it with your friends. ❤️

If you liked this article, feel free to visit me on [Twitter](https://twitter.com/mbaziiraronn), I regularly post content there. It is basically the platform where you will find my content first before it lands on my blog or somewhere else.

%%[buy-me-a-coffee]