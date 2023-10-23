# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Introduction to Git](#introduction-to-git)
- [A Bit of History](#a-bit-of-history)
- [What's the Use?](#whats-the-use)
- [Summary](#summary)

# Introduction to Git

This article is dedicated to introducing the software Git. Here, you will find useful information about what Git is, and you will learn about its history.

# A Bit of History

Git is a free software invented by Linus Torvalds in 2005 and is distributed under the GNU2 license, making it open-source software. It allows for the decentralization of code versions, or in other words, it enables the creation of versions of code files (and more) to ultimately access different versions of the same file.

# What's the Use?

Git is absolutely essential software for any serious developer in our modern age. You'll understand why as you read this section.

The primary idea behind Git is to be able to track the changes that a file has received, whether it contains code or not. Git was created with the aim of allowing file sharing among developers.

Let's take a concrete example to help you understand what Git is used for:

```
Imagine you're working on a JavaScript project, and you make changes to your code.
Then you realize that the changes you've made create a bug in your project.
Unfortunately, you need to find the cause of the bug and
remove everything you've done for the past two hours.
```

It's more than likely that you've found yourself in this situation before. Git makes it very easy to manage such situations.

Let's take this example again, but this time, we'll use Git to help you figure out how it's used.

```
You're working on a JavaScript project, and after each significant code change,
you make a "commit" (we'll discuss this term later).
Your changes have created a bug in your project.
You use Git to trace back to when you made your changes and
directly compare code versions.
You can remove only the problematic change.
```

In essence, when you use Git to make a "commit", it's like taking a snapshot of your code, except with Git, you can go back to a previous point in time.

So, that's what Git is used for. We'll revisit this in the next [article](../../02-versioning/fr/article.md).

# Summary

- Git is free and open-source software created by Linus Torvalds in 2005.
- Git is used to maintain multiple versions of the same file.
- Git facilitates code sharing (and more) among developers.
- Git is considered mandatory for developers.