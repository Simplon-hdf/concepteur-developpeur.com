# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Basic Commands](#basic-commands)
  - [Initializing Git in a Project](#initializing-git-in-a-project)
  - [Stage Changes for Commit](#stage-changes-for-commit)
  - [Unstage a File](#unstage-a-file)
  - [Commit Changes](#commit-changes)
  - [Conclusion](#conclusion)
  - [Summary](#summary)

# Basic Commands

Git commands are how you interact with Git. They allow you to tell Git to perform specific actions. These commands are entered in your terminal (shell). This article covers the most basic commands. If you haven't read the [article](../../03-git-functions/en/article.md) on how Git works, please do so before reading this one.

## Initializing Git in a Project

To initialize Git in a project, use the following command:

```sh
git init
```

This command will create a `.git` directory in the directory where you run it. For example, if you are in `/my_git_project/`, a `.git` directory will be created in that folder, and you can access it by going to `/my_git_project/.git`. You might not see the `.git` directory in a regular `ls` listing because the `.` before `git` makes it a hidden directory. You can use the `ls -al` command to see hidden directories.

Now, Git is initialized in your project.

## Stage Changes for Commit

To stage files that have been modified, use the following command:

```sh
git add [file_name]
```

This command will place your file in the staging area.

For example:

```sh
git add index.js
```

Will stage `index.js`, and you'll can include this file in your next commit.

You can also stage an entire directory:

```sh
git add my_directory/
```

This command stages all files that have been modified in the specified directory.

However, it's possible that you want to add all your modified files to a commit. In this case, you can use:

```sh
git add .
```

This command stages all modified files from the directory where you run it. For example, if you run this command in `/my_git_project/articles/`, it stages all files in `/my_git_project/articles/` and its subdirectories recursively.

It's best to avoid this approach unless you are only modifying one file at a time and committing changes in real-time.

## Unstage a File

It's possible to make a mistake when staging files. For example, you realize that you included a file that shouldn't be part of the commit you intended to make. In such cases, you can use the command:

```sh
git restore --staged [file_name_to_unstage/directory]
```

You can also use:

```sh
git restore --staged .
```

This command will unstage all files. 

**However, use this command with caution. Without the `--staged` option, this command will reset the specified file or directory to its last known state (the state in your local repository).**

## Commit Changes

If you have files in your stage area, you probably want to make a commit. To do this, enter the following command:

```sh
git commit
```

This will open a text editor like Vi or Nano, depending on which one you have. This method can be a bit lengthy, which is why there is an option that streamlines the process:

```sh
git commit -m "commit message"
```

By adding this option, you can specify the commit message directly and you don't have to do anything else. For example:

```sh
git commit -m "Implementation of my super useful function"
```

There you have it, your commit is done, and the version of the file that was in the stage area has been copied to your local repository. The files that were previously in the stage area are no longer there since they have been committed.

## Conclusion

You should now be able to use Git at a basic level. The upcoming articles will focus on more advanced and concrete concepts.

## Summary

- Commands are a way to interact with Git to perform actions.
- The `git init` command tells Git to initialize itself in a directory.
- The `git add [file/directory name]` command is used to stage files for a commit.
  - The `git restore --staged [file/directory name]` command is used to "unstage" files.
    - This command, without the `--staged` option, restores the last known version of the specified file/directory (the version from the latest commit related to that file in the local repository).
- The `git commit` command is used to confirm the changes made to the staged files.
  - The `-m` option allows specifying a commit message directly.