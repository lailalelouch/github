This command is used to add files to be tracked in our git repo.

In the coloring book example, the add would be like adding the picture we're coloring right now to be tracked by git.

Let's try adding the file we just created

```
$ git add hello.txt
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   hello.txt

```

I added the file `hello.txt` to be tracked for any changes. So, if you look under `Changes to be committed:` in the message `git status` gave us you'll see that the change now is that there is a `new file` called `hello.txt`.

Now create a new file in your `hakuna_matata` folder. I added an image called `data.png`. Now check the status of your repo....Before you try it, can you guess what the status of each file is....you can have some dancing potato thinking time...

![dancing potato](https://media1.tenor.com/images/61497871ab091f01703a3f1a624fb3c4/tenor.gif?itemid=11684043)

Terminal/gitbash

```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   hello.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	data.png

```

You'll notice that the new file created is in the `untracked files` section. What if we wanted git to track this file, do you remember what we had to do....Do you need another dancing potato thinking time?....no?...okay.

The answer is to add this file.

```
$ git add data.png
```

Take your time...create new files, delete them, edit them and check the status to see how git is tracking them.

One last thing beofre we move on. What if we had 10 files that we wannted to `add`, it wouldn't be practical to `git add <FILE_NAME>` for each file. Fortunately, we have a command to add `all` the files.

```
$ git add .
```

Note: all of these commands needs to be done while you're in the repo folder which in this case is `hakuna_matata`. To check if you're in the right place, the ls/dir command should give you the files that are in the repo folder. If you're not familiar with these commands, the last chapter about command lines should help.
