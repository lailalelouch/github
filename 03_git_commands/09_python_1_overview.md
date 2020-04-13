Let's just wrap things up here.

There are two kinds of repos: local and remote.

Local are just a folder in your computer.

Remote is a repo in github or any other website that uses git.

The remote repo will stay empty until it is connected to a local one.

Now let's get into how we create a repo at all.

Any folder that you have on your computer could be a git repo but you'd have to get into it using your terminal/gitbash and writing the `git init` command.

Any file that you make changes too and would like to commit/add in a checkpoint. You need to add and commit it.

```
git add .
git commit -m "message that represents this checkpoint"
```

Final step is to upload and push these changes to the remote repo. If your local repo is not connected to the remote repo you'll need to follow the steps the remote repo is giving you and connect them. Otherwise you can go ahead and `git push`.

Most of the projects in codeunicorn that do not start from scratch will ask you to fork a preexisting repo and then clone it to continue building on it.
