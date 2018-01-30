---
title: 2-Setup
nav: true
---

# Getting Started

First, let's take a look at an example on GitHub and then get Git configured on your local computer.

## GitHub Web Interface

Log in to GitHub and go to our [git-example repository](https://github.com/uidaholib/git-example).
The main page of a repository is the "Code" tab, which has a representation of the files, and displays the `README`.

Demo the basic features of the interface:

1. Click the "Fork" button in the upper right--you now have your own version of the repo! Forking is a GitHub concept that allows you to create a new copy of a repository, yet maintain a connection so that changes can be sent back to the original via "Pull Requests" (PR). It is a common workflow for collaborating on bigger projects.
2. On your `git-example`, click the "Commits" button below the description. The Commits page allows you to review and navigate the entire history of the repo.
3. Click back on the "Code" tab, then click on one of the file names. This will display the file's contents on the page. 
4. Click the edit pencil on the upper right side of the document to open the web editor. 
5. Make some changes or add some new text, then scroll down to the "Commit Changes" box. Enter a commit message and click the green button to save your edits to the history. You just used Git--you made your first commit!
6. Click back to the "Code" tab and "Commits" to view your updated history.

> Note: GitHub allows [Markdown](https://guides.github.com/features/mastering-markdown/) formating for READMEs and comments through out the site.

## Create a New Repository

The most common way to work with Git is to create or fork a repository on GitHub, then `clone` it to your local machine.
To create a new "remote" repository:

1. Click the plus sign on the upper right and select "New repository" from the drop down
2. Give it a nice name
3. Check "Initialize this repository with a README"
4. Click "Create repository"

> Every GitHub repo has handy project management features builtin. 
> Check the Issues, Projects, and Wiki tabs to start organizing your work!

## Git Config

To start learning Git we will use it on the command line.
Although there are GUI clients to manage Git repositories, being familiar with the command line version will help you better understand the basic workflow.
If you need a command line refresher, check out this [mini-lesson](https://evanwill.github.io/_drafts/notes/commandline.html).
So fire up your favorite shell, terminal, or Git Bash to get started!

Some initial setup is necessary the first time you use Git on a computer.
You will use these commands only once, unless you want to change something.

Set your name and email:

```
git config --global user.name "Evan Will"
git config --global user.email "myemail@gmail.com"
```

> Your email and user name is recorded with every commit.
> This helps ensure integrity and authenticity of the history.
> Most people keep their email public, but if you are concerned about privacy, check GitHub's tips to [hide your email](https://help.github.com/articles/keeping-your-email-address-private/).

Set your default text editor (Windows "notepad" or nano on Git Bash, Mac "edit -w", Linux "nano -w"):

```
git config --global core.editor "notepad"
```

> Git opens the default editor to ask for commit messages. 
> You are most likely to encounter it when merging.
> If you don't set a default editor, Git will use the default default--which might be surprising if you are not used to terminal-based editors such as [VIM](http://www.vim.org/). 
> If you are stuck in VIM and can't figure out how to escape, type `:wq` to save and quit ([VIM quick ref](https://w3.cs.jmu.edu/bernstdh/Web/common/help/vim.php), and don't worry, you are [not alone in confusion](https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/)).

With our test repository ready and Git configured, we can move on to the basic [Git workflow]({{ '/3-workflow.html' | absolute_url }})!

## Create Repository Locally

P.s. If you really want to you can create a local repository:

```
mkdir test
cd test
git init
```

If you want to connect this repository to GitHub, you have to `git remote add`.
Generally, it is easier to create the repo on GitHub first and `clone`, rather than using `init`.