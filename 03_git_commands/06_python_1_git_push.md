This command is used to upload your git repo online with all your files and checkpoints.

This is where github the website you signed up in in the beggining comes in. All your local repos(folders that you initialized as a git repo using the `git init` command) are just folders on your computers. Github gives you the option to upload those files with their checkpoints. Now that they're uploaded you can share them with people and if something happened to your computer, you still have your work online and can just download it again(that's the next chapter).

However, if it is the first time pushing(uploading) your files to an online git repo, you need to specify where you're uploading them.

So, if you try to push/ upload your repo now, you'll get this:

```
$ git push
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>
```

It says `No configured push destination.` which means that you need to specify where to upload it.

So, to push a local repo for the first time, you need to do the following:

- Create an online repo in [GitHub](https://www.github.com).
- Connect your local repo to the online repo.
- Push it.

Let's start from step 1: Create an online repo in [GitHub](https://www.github.com).

Open the website, login and try to find a `New` button. Or you'll find a plus sign in the right hand corner click it then click `new repository`.

Then just fill out the `Repository name` with whatever you want your repo to be called and click `create repository`. And now you have an online repo....congratulations.

Now to step 2: Connect your local repo to the online repo.

After you created your online repo, it's going to give you steps to push your code, go to the part that says `…or push an existing repository from the command line`

It gave me these two commands where `lailalelouch` is my github username and `test` is what I named my online repo. So these two will be different for you.

```
git remote add origin https://github.com/lailalelouch/test.git
git push -u origin master
```

Now, go back to your terminal/gitbash and connect your local repo with the online one.

```
$ git remote add origin https://github.com/lailalelouch/test.git
```

Step 3: Push it.

terminal/gitbash

```
git push -u origin master
```

Now go back to your online repo in github and refresh the page, and you'll see your files. How cool is that!!!

Now everytime you change your files and create a few checkopoints, you can simply upload/push them by writing this command in your terminal/gitbash. Only the first push requires the above steps. Any other time you would just push your changes like this.

```
$ git push
```

Note: Only changes to files that have been commited/added to a checkpoint will be pushed to your github repo.

You can think of the whole `add`, `commit`, `push` cycle as a shipment company and you have boxes to fill:

- `add`: you add files to the currently open box.
- `commit`: you close and seal the box and add a message on it describing what's inside the box.
  The above two actions can be repeated as many times as you want where each time you commit a new box is closed.
- `push`: all the closed boxes are shipped off to their destination (uploaded to your remote repo).
