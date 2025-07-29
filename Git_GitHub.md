# Git and GitHub

[Git](https://git-scm.com/) is a version control system used to track changes in files and coordinate work on those files among multiple people. [GitHub](https://github.com/) is an hosting service for Git repositories.

To synchronise our first repository we can follow one of the many useful [tutorial](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository?platform=linux&tool=webui) that GitHub developers have written during these years. Using the 'ssh URL' instead of makes things easier, to correctly set our origin.

usefult commands:

```bash
git add <file> #add file to the stagin area
git commit -m "commit message" #creates a new a commit 
git push #push any new commit
git pull #pull any changes from online repositories
git rm <file> #remove any file automatically adding this change to the staging area
git mv <file> #mv any file automatically adding this change to the staging area
git status #display the current state of the git repository
```

## SSH keys

We need to give permission to our local repository to contact the online one and exchange information. To so so, we can follow this [tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) creating a pair of ssh-keys that can allow the correct autentication between local and origin repositories. When you will be asked to choose a password, take into consideration the possibility to not choose one. It seems counterintuitive, but it lets you have more room for automatisation. For example, in this way you can write a script that automatically can update and synchronise your entire repository every day, even if you forget to do it. This is possible using the tool `crontab`, which is designed to launch periodical background commands. To do so, follow instruction present [here](./time_scheduled_commands.md).

## Gitignore

A very useful file is [.gitignore](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files). This file allows to list all files that we do not want to synchronise with out online repository, because to big or not useful. As always, it is only a common text file which containes extensions and file to ignore. a good starting point is to ignore all fasta and logs file. If in any way they become important, it is only possible to force those we want.

## How Git works

![git staging area working](../99_Figures/git_staging_area.jpeg)

![git tree](../99_Figures/git_tree.png)
