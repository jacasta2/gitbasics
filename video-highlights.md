# Git

The video by [Fazt](https://www.youtube.com/c/FaztTech) can be watched [here](https://www.youtube.com/watch?v=HiXLkL42tMU). It is in Spanish. If you don't understand Spanish, try to configure the video with auto-generated English subtitles.  

<span style="color:blue">2:50</span> --> What is Git  
- Repository (repo)
- Multiple developers can alter code
- But all have a local copy of code
- Registry of all code (like a time machine)
- Revert changes

<span style="color:blue">5:30</span> --> Basic concepts  
- Track changes through snapshots
- Keep changes with 'commits'

<span style="color:blue">6:35</span> --> Basic commands  
- `git init`: Start using **Git**  
- `git add [path-to-file]`: Move files to staging  
- `git status`: Check status  
- `git commit`: Keep the changes (create the snapshots)  
- `git push`: Move files to a remote repo  
- `git pull`: Bring changes from other developers  
- `git clone`: Copy code from server where it's stored to your machine  

<span style="color:blue">7:15</span> --> The 3 states  
1. Working directory (work with files)
2. Staging (start tracking changes)
3. Repo (keep changes)

<span style="color:blue">9:30</span> --> Installing **Git**  

<span style="color:blue">13:35</span> --> Start working with **Git**  
Create a project directory and add some files.  
Following the video, I worked with **Atom**.  

<span style="color:blue">16:40</span> --> `git init`  

<span style="color:blue">17:30</span> --> `git status`  

<span style="color:blue">18:15</span> --> `git add [path-to-file]`  

<span style="color:blue">19:50</span> --> `git commit`  
It shows an error since we haven't configured and user.  

<span style="color:blue">20:30</span> --> `git config [...]`  

<span style="color:blue">21:40</span> --> `git commit`  
Write an informative message about the version!!!

<span style="color:blue">23:00</span> --> `git log`  
Running `git status` shows there's nothing to commit, the environment is clean.  

Modify index.html  

<span style="color:blue">24:35</span> --> `git status`  
It shows index.html was modified.  
Note the messages (not staged for commit) and colors (red).  

<span style="color:blue">24:45</span> --> `git checkout -- index.html`  
It discards changes in index.html, showing the previous version.  
Running `git status` shows there are no changes.  

Modify index.html  

<span style="color:blue">25:45</span> --> `git diff index.html`  
It indicates what lines changed in index.html.  
Note the signs (- and +) and colors (red and green)!!!  

<span style="color:blue">26:20</span> --> `git status`  
It shows index.html was modified.  
Note the messages (not staged for commit) and colors (red).  

<span style="color:blue">26:25</span> --> `git add index.html`  
It shows new changes can be committed.  
Running `git status` shows there are no changes.  
Note the messages (to be committed) and colors (green).  

<span style="color:blue">26:45</span> --> `git commit`  
Write an informative message about the version.  
After saving the commit, a message appears summarizing the changes.  

<span style="color:blue">27:40</span> --> `git log`  
It shows the different code snapshots (2 versions so far).  

Create a folder with test files that we don't want to be tracked by **Git**.  

<span style="color:blue">29:20</span> --> `git status`  
It shows the test folder as untracked (in red).  

<span style="color:blue">29:35</span> --> Create file `.gitignore` so that **Git** ignores specific stuff  
Write the name of the test folder in this file.  

<span style="color:blue">30:00</span> --> `git status`  
It doesn't show the test folder anymore, but it shows the `.gitignore` file (in red) as untracked.  

<span style="color:blue">30:15</span> --> `git add .gitignore`  
It adds `.gitignore` to the project.  
Running `git status` shows `.gitignore` (in green) can be commited.  

Add another test folder, include it in `.gitignore` and run `git status`.  
The folder shouldn't appear, but a message shows `.gitignore` was modified.  
Repeat the process with a test file.  

<span style="color:blue">31:25</span> --> `git add .gitignore`  

<span style="color:blue">31:40</span> --> `git commit -m "I added .gitignore"`  
The option `-m` plus the message prevents the commit editor from launching.  

<span style="color:blue">33:10</span> --> `git branch`  
It shows a (the) **master** version.  

What if we want an alternative version with, for example, a login screen?

<span style="color:blue">33:35</span> --> `git branch login`  
Running `git branch` shows there are two branches or versions: **master** and **login**.  
It also shows we are working with **master** (it's in green).  

<span style="color:blue">34:00</span> --> `git checkout login`  
Running `git branch` shows we are working with **login**.  

Add a couple of folders (login, authentication) with files inside and a file (indexlogin.js).  

<span style="color:blue">35:05</span> --> `git add .`  
It moves all files to staging.  

<span style="color:blue">35:40</span> --> `git commit -m "Alternative version with login"`  

<span style="color:blue">36:00</span> --> `git log`  
It shows the different code snapshots (4 versions so far).  

<span style="color:blue">36:20</span> --> `git checkout master`  
It moves back to **master**.  
Note the recently created folders and files aren't showed in the project directory since they belong to **login**.  

<span style="color:blue">36:45</span> --> `git log`  
Note the **login** commit isn't showed since it doesn't belong to **master**.  

# GitHub

Go to your **GitHub** profile. If you don't have one, please create it.  

<span style="color:blue">40:10</span> --> Create repo in **GitHub**  

<span style="color:blue">43:00</span> --> `git remote add origin https://github.com/jacasta2/gitbasics.git`  
It links our project (the **master** branch) with the repo.  

<span style="color:blue">44:00</span> --> `git push -u origin master`  
It uploads the files from **master** to the **GitHub** repo.  
Note the password authentication method doesn't work.  
Follow the **GitHub** documentation in [Creating a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) to create a token that replaces your password and run the `git push [...]` command again, pasting the token in the password field.  

<span style="color:blue">46:15</span> --> Create a README file  

Delete the project folder from your computer.  
Before doing so, make sure to create a copy and paste it in a folder different from the one where the `git clone [...]` command is going to be run since the clone doesn't have the **login** branch.  

<span style="color:blue">47:35</span> --> `git clone https://github.com/jacasta2/gitbasics.git`  
It downloads the repo to your computer.    
Run `git status` and `git log` to check the work.  

# Other stuff (not in the video)

## Undo the last commit

`git reset [...]` undoes the last commit:  

`git reset --soft HEAD~1`  

Note this command undoes the last commit but not the changes made to the files.  

More details can be found in [How to undo last Git commit](https://devconnected.com/how-to-undo-last-git-commit/) by [SCHKN](https://devconnected.com/author/schkn/).  

## Revert a single file

If you want to retrieve an older version of a particular file and keep it, first you have to load the older version. This is done through a `git checkout`:  

`git checkout [commit ID] -- [path-to-file]`  

Commit IDs can be found by running:  

`git log --oneline`

You can also use a HEAD pointer to load some particular versions:

`git checkout HEAD [path-to-file]`: last commit.  
`git checkout HEAD^ [path-to-file]`: last commit - 1.  
`git checkout HEAD^^ [path-to-file]`: last commit - 2.  
`git checkout HEAD~10 [path-to-file]`: 10 commits behind of HEAD.  

After the older file is loaded, running `git status` indicates the file has changes to be committed.

Then, if you want to keep this older version, it should be committed using `git commit [...]`.  

If for some reason you load the older file and don't want to revert it, you have to load the latest version, i.e., the file from the last commit. Once this is done, running `git status` no longer indicates the file has changes to be committed.  

More details can be found in [Git and GitHub: How to revert a single file](https://dev.to/lofiandcode/git-and-github-how-to-revert-a-single-file-dha) by [Joseph Trettevik](https://dev.to/lofiandcode) and [Retrieve single file from old commit on GIT](https://coderwall.com/p/dvdrzg/retrieve-single-file-from-old-commit-on-git) by [Willy Barro](https://coderwall.com/willybarro).  

## Create a pull request

Up to this point, you should have a **GitHub** repo and know how to push stuff to it. But how can you contribute to other people's GitHub projects?  

[How to create a pull request in GitHub](https://opensource.com/article/19/7/create-pull-request-github) by [Kedar Vijay Kulkarni](https://opensource.com/article/19/7/create-pull-request-github) shows an easy-to-follow guide for creating a pull request using **Git** and **GitHub**.  

The only thing that wasn't working for me was the line `git commit -S -m "your-commit-message"`. I removed the `-S` option and voilà!

## 'Accidentally' deleting files in GitHub...

In a recent project I 'accidentally' deleted a file from **GitHub** (not locally) and found myself having issues pushing more stuff to that project's repo. I had to integrate such change (the deletion of the file) locally through the `git pull` command. Be careful when doing so since the command also deletes the local copy of the file.

When you delete a file locally and want to push that change to **GitHub**, do the following:

`git rm [path-to-file]`

Then commit the change and push it to the repo.