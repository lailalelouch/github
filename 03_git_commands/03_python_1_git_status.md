This command is used to let you know about the status of the files inside your repo(the folder that you git init in). It let's you know if a file was modified or deleted or added and so on.

If you try this command in your terminal/gitbash while in your empty folder, this is what you'll get:

```
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

This basically says that there are no changes because you didn't change anything inside your repo.

Now go ahead and add something in your folder. An image, a text file, anything you want. I'll be adding a text file called `hello.txt`. Now, when I do `git stattus` this is what I get:

```
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	hello.txt

nothing added to commit but untracked files present (use "git add" to track)
```

It now says that I have this new file called `hello.txt`.

If you notice the message `git status` is giving us, it says `Untracked files:` and then gives us the new file/s we added. Go into the next section to figure out what this means.
