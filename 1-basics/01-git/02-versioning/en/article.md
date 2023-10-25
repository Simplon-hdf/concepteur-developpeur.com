# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Versioning](#versioning)
  - [What is it?](#what-is-it)
  - [What's it for?](#whats-it-for)
  - [How does it work with Git?](#how-does-it-work-with-git)
- [Summary](#summary)

# Versioning

## What is it?

Versioning (or versionnage in French) is a concept that involves cataloging versions of a work, software, a document... in fact, all kinds of things that are meant to evolve over time.

To put it simply: different versions of a resource are preserved for various purposes.

That's what versioning is all about.

## What's it for?

Versioning is very useful for various reasons.

Have you ever gone back to read the code of a project you worked on a few years ago? Or have you ever realized that your perspective on a subject has changed?

In fact, you've encountered versioning long before reading any articles on the subject. In the first question, if the answer is "Yes", then we can say that the version of you today is much better than the one from several years ago. In this case, you become aware of the progress made. It may sound a bit abstract for now, so let's take a more concrete example:

```
Imagine you're working on a project that you worked on
a few years ago, and you need to code a function that still
gives you nightmares because of its complex behavior. It's
more than likely that you would like to have this function to
simply copy and paste it rather than spending a week doing
fruitless research and tests, isn't it?
You go to the class that contains this famous function, but you
remember that you deleted it and stopped this project. You have
no way to recover this function, and you realize that you will
have to go through an intense thought process again.
```

If you had used a versioning tool like Git, you could have gone back to a version of this class prior to the version in which the function was deleted.

To put it simply:

Not using a versioning tool is like working with a single version of an application.
Using a versioning tool is like creating multiple versions of your application's code.

## How does it work with Git?

Versioning is the core aspect of Git. In fact, everything revolves around the concept of versioning with Git, and we'll discuss it in more detail in the [article](../../03-git-functions/en/article.md) on how Git functions.

The versions of files in a Git repository are stored in a "commit" history. With Git, you can save different versions of any type of file whenever you want. Taking the example above, once your function was functional, you could have decided to save that version of your class. Then, you could have retrieved your function because even if it no longer existed in the latest version of your code, there would have been a version of your class containing your function in the "commit" history of your Git repository.

# Summary

- Versioning is a concept that involves keeping a record of different versions of a resource.
- A versioning tool allows saving different versions of a resource for various purposes.
- Git is a software that heavily relies on versioning, although it's not the only aspect that characterizes it.
- Git allows storing different versions of a resource in a history using a mechanism called "commit."