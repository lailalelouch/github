This command is used to create a checkpoint that we can go back to later.

In the coloring book example, we had to make a `commit`(checkpoint) after coloring the leaves. That's why we were able to go back to that `commit`(checkpoint).

A `commit` creates a checkpoint for all the files that have been `added`. At the same time a `commit` should have a short descriptive message describing what this checkpoint represents.

Let's take a look at what our repo has

Terminal/gutbash

```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   apples.txt
	new file:   data.png
	new file:   flamingo.txt
	new file:   hello.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	watermelon.txt
```

If I decide to create a checkpoint/commit now. Which files do you think will be commited or added to this checkpoint?

Take some time to figure out the answer...one dancing potato coming up

![dancing potato](https://media1.tenor.com/images/61497871ab091f01703a3f1a624fb3c4/tenor.gif?itemid=11684043)

The answer is these files will be added to the checkpoint.

- apples.txt
- data.png
- flamingo.txt
- hello.txt

Let's move on to creating the checkpoint

Terminal/gitbash

```
$ git commit -m "created new files with the data image"

[master (root-commit) 28dcb9f] created new files with the data image
 4 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 apples.txt
 create mode 100644 data.png
 create mode 100644 flamingo.txt
 create mode 100644 hello.txt
```

With this command I created a checkpoint which is my folder having those three text files which are currently empty and an image.

Notice that the message has to be descriptive to what this checkpoint has because checkpoints are for you in case you changed your mind and wanted to go back to them. But if the checkponts are labeled randomly, how would you know which checkpoint has what you want.

So far we only have one checkpoint so it isn't that difficult. But, let's create more.

Let's check the status of our repo first

```
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	watermelon.txt

nothing added to commit but untracked files present (use "git add" to track)
```

Now, I'm going to write something in `hello.txt`

Let's see how this would affect the status

```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   hello.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	watermelon.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

Now, it says that the file `hello.txt` was modified.

Let's try to create a checkpoint for this. To create a checkpoint we need to commit

Terminal/gitbash

```
$ git commit -m "added my name in hello file"
On branch master
Changes not staged for commit:
	modified:   hello.txt

Untracked files:
	watermelon.txt

no changes added to commit
```

I wasn't able to create a checkpoint and got this back `no changes added to commit`. That means git creates a checkpoint for files that are added. So, remember this whenever you make changes to files that you want to commit/make a checkpoint for you need to add them first. So, let's add all the files that have changes in them and then commit them.

terminal/gitbash:

```
$ git add .
$ git commit -m "added my name in hello file"
[master bda29ae] added my name in hello file
 2 files changed, 2 insertions(+)
 create mode 100644 watermelon.txt
```

Now we have two checkpoint. at any point if you decide that you want to go back to a point where you created a checkpoint, you can just look through your commits...read the labels/messages you added for each commit and you'll easily know which one you'd want to go back to.

This might not sound very useful for normal files. But if you're working on a programming project and at some point your program crashed and isn't working anymore and you can't fix it. The best thing to do is go back to the last working version which would be your last commit/checkpoint instaed of starting from scratch.
