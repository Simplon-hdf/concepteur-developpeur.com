Renaming a file using the command line :

You can use the command line to rename any file in your repository.

Many files can be renamed directly on GitHub, but some files, such as images, require that you rename them from the command line.

This procedure assumes you've already:

    Created a repository on GitHub, or have an existing repository owned by someone else you'd like to contribute to
    Cloned the repository locally on your computer

    Open Terminal.
    Change the current working directory to your local repository.
    Rename the file, specifying the old file name and the new name you'd like to give the file. This will stage your change for commit.

    $ git mv OLD-FILENAME NEW-FILENAME

    Use git status to check the old and new file names.

    $ git status
    > # On branch YOUR-BRANCH
    > # Changes to be committed:
    > #   (use "git reset HEAD ..." to unstage)
    > #
    > #     renamed: OLD-FILENAME -> NEW-FILENAME
    > #

    Commit the file that you've staged in your local repository.

    $ git commit -m "Rename file"
    # Commits the tracked changes and prepares them to be pushed to a remote repository.
    # To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.

    Push the changes in your local repository to GitHub.com.

    $ git push origin YOUR_BRANCH
    # Pushes the changes in your local repository up to the remote repository you specified as the origin

