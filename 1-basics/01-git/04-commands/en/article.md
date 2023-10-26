# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Basic Commands](#basic-commands)
  - [Initializing Git in a Project](#initializing-git-in-a-project)
  - [Stage Changes for Commit](#stage-changes-for-commit)

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