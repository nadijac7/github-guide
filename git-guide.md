# Quick Guide to making git repositories on the command line

There's three parts in this process:

1. make a repository on your local machine (command line)
2. set up a place on Github to store your repository (internet browser)
3. tell your local repository about the Github spot, and push your work to Github (command line)

This guide assumes you are using `Git Bash` (or other `*nix` shell) as your command line.

---

## List of Commands, and a brief explanation of them

- `mkdir`
makes a directory

- `pwd`
what directory am I in

- `ls`
List the stuff in the current directory

    - `ls -l`
List things in long form. This can be easier to read.

    - `ls -la`
Long form, and show hidden files and folders.

- `cd`
change directory

    - `cd Documents`
if there is a directory called `Documents` in the current directory,
you will move into the `Documents` directory

    - `cd ..`
move up one directory (ex: from `C:/Users/Jonathon/` to `C:/Users/`)

- `touch file.txt`
makes an empty file called `file.txt`


- `git init`
make a new git repo, in the current directory

- `git status`
what is the status of the git repo/directory I'm in. It is good practice to use this command frequently so that you can fully understand the state of the repo.

- `git add .`
add all the files to git's tracking system. In git-speak, this is called `staging` your files.

- `git commit -m "commit message"`
commit (save) the changes to git's tracking system (the `-m` means messages).

- `git remote add origin https://github.com/username/repository_name.git`
You'll get the URL from Github's "New Repository" process. This command tells git that github has a backup for this repository. To avoid typos, you should copy and paste (with right click, not Ctrl-V) the URL.

- `git push -u origin master`
the standard command to push to your Github repo (the Github repo added with `git remote add origin url`). This will probably ask you for your Github username and password. After it finishes, your work will be backed up on the Github servers

## Guide - New Repository

In Git Bash, navigate (`pwd`, `cd`, `mkdir`) into a new directory.

`git init`

to make a new git repository in the new folder.

Go to the Github website, and click on the + sign (top right) and then click "New Repository"

Give this repository the same name that you gave the folder on your computer.

Github will provide you a link (looks like https://github.com/username/repository.git). Copy this link.

Back in Git Bash, make sure you are in your git repository (`git status`, `pwd`). Type the following

`git remote add origin <your url>`

ex: `git remote add origin https://github.com/username/repository.git`

You should Right Click > Paste the URL in order to avoid typos. In the terminal, Ctrl-V doesn't usually work, so you should use right click.

Now your repository and Github know about each other.

Add files to the directory, and then track them with Git using

`git add .`

Make Git permanently remember your files with

`git commit -m "commit message"`

Push your changes to Github with

`git push -u origin master`

Now your files should be on the Github site.

