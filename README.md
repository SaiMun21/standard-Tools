# standard-Tools

This is a set of scripts and notebooks intented to introduce people to the use of ROOT in data analysis.

## How to install

### Git installation

In order to learn how to use GitHub, installation will be done by manual git initiallization. Git will allow to control the different versions of the code. In the following: Remote repository will refer to the code that you have in GitHub, and local repository will refer to the code that you have in your working area e.g. your remote machine, lxplus, uaf... etc.

### Create a forked repo: This will be the repo where you will work

1. First, make sure that you have a GitHub account
2. Fork this repository into your GitHub profile. A fork will create an exact copy of the repository that can be managed by you. Additionally, it can be synchronized with the original repository repo.
3. For this example, your remote repository will be the new repository that you just have forked in your profile

### Create your local repository in your working area

Since we want to work with SWAN, you will need to create the local repo in your eos. For that, you to the following path:
```
cd /eos/user/[first letter of username]/[username]/
```
and then install the repository from GitHub:
1. Go to your forked repo
2. Get the .git direction: Code -> ssh -> Copy url to clickboard
3. In you eos, create the ```SWAN_projects```folder if you don't have one. Then open it:
```
mkdir SWAN_projects
cd SWAN_projects
```
4. And then:
```
git clone [the url that you just have copied]
```

### Git in a nutshel

Whenever a new repository is created, the main branch is created as well. This is, as the name indicates, the main branch.

1. In order to have more control and freedom tu update the repository, it is strongly adviced to create a new so-called branch that will track all the modifications that you will do:
```
git checkout -b my_branch
```
2. You can see the branches that you have by doing:
```
git branch
```
3. And switch again to other existing branches by doing
```
git checkout [name of the existing branch]
```

### Accessing your repository in SWAN

Once done, if you access your SWAN space, you will see the new folder with the repository, that can now be run.

### Comitting changes and share the code

1. You can check which files have been modified since a change was committed to the code:
```
git status
```
2. After a file is modified, you can commit the change by doing:
```
git add [modified file]
git commit -m "Message explaining what you just have done"
```
3. If you want to have this change committed to your remote repository too (in GitHub), you have to push the changes:
```
git push origin my_branch
```
(origin is an idenfier for the remote repository, and you have to specify which branch is the one you want to push)
4. If you create new files, these will appear as untracked i.e. if you just push the branch, they won't be included. If you want to include them and let them be part of the repo, just do:
```
git add [new file]
git status (The new file will have appeared in green!)
git commit -m "Add new file"
git push origin my_branch
```
Changes between branches can be compared in GitHub.

## Muons: Z to $\mu\mu$ exercises

Files in the Basic-ZToMuMu gives and introduction to file reading and histogram handling:

- Tutorial-ReadFiles
- Tutorial-Histograms
- Planned: Tutorial-Fitting
