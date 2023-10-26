# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Basic Commands](#basic-commands)
  - [Initializing Git in a Project](#initializing-git-in-a-project)

# Basic Commands

Git commands are how you interact with Git. They allow you to tell Git to perform specific actions. These commands are entered in your terminal (shell). This article covers the most basic commands. If you haven't read the [article](../../03-git-functions/en/article.md) on how Git works, please do so before reading this one.

## Initializing Git in a Project

To initialize Git in a project, use the following command:

```sh
git init
```

This command will create a `.git` directory in the directory where you run it. For example, if you are in `/my_git_project/`, a `.git` directory will be created in that folder, and you can access it by going to `/my_git_project/.git`. You might not see the `.git` directory in a regular `ls` listing because the `.` before `git` makes it a hidden directory. You can use the `ls -al` command to see hidden directories.

Now, Git is initialized in your project.