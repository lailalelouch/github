Let's start with the basics. `git` is a version control system that keeps track of our files and the changes that are made to them.

Let's go back to the coloring book example. Imagine you have a coloring book and you're coloring a picture of a flower. You just finished coloring the leaves in green. Next, you start coloring the petals in red. However, after you finished, you thought the petals looked horrible. With git, you can revert your choice of red and go back to the point where you just finished the leaves and start again from that point.

How does git know which coloring book to track its changes or which page in the book to track and save those chnages?

The first thing is to tell git that you need to track any changes that happen in this book, through this command

    git init

Now with this command all pages inside of this coloring book will be tracked.

Let's see this from a computers point of view. The book is a folder and the pages are all the files inside of this folder.

Let's create a folder called `hakuna_matata` in the desktop. You can just leave the folder empty for now.

Next, open your terminal/gitbash and go inside of a the newly created folder/directory.

note: in case you don't know how to move through directories in the command line. you can check the command line chapter at the end of this workshop.

```
 $ cd hakuna_matata
 $ git init
```

Now this folder is your `git repository`. A `git repository`(repo for short) is a folder that git tracks for changes.

Right now the folder is empty. But we'll add things to it later on to see how git tracks them.
