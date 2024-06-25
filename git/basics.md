# GIT Basics

Git is a distributed version control system that allows you to track changes in your project and collaborate with other developers. This document contains some of the basic commands and configurations you need to know to start using git.

## Getting Started

### Configuring git

To be able to use [git](https://git-scm.com/downloads), make sure you have it installed on your machine. Most Linux distributions come with git pre-installed. To check if you have git installed, run the command:

```bash
git --version
```

### Initializing a git repository

To initialize a git repository in your project, navigate to the project's directory and run the command:

```bash
git init
```

This command will create a hidden directory `.git` in your project's directory. This directory contains all the information about your project's history and configurations.

In your project's directory, you can create a file named `.gitignore` to specify the files and directories you want git to ignore. For example, you can add the following lines to ignore the `build` and `.vscode` directories:

```bash
build
.vscode
```

The next step would be to add your files to the staging area. To add all the files in your project to the staging area, run the command:

```bash
git add .
```

To add a specific file, run the command:

```bash
git add <file_name>
```

To commit the changes in the staging area, run the command:

```bash
git commit -m "Your commit message"
```

If you want to see the changes you have made in your project, run the command:

```bash
git status
```

To see the history of your commits, run the command:

```bash
git log
```

If you have a remote repository on say `GitHub`, you can add it as a remote to your local repository by running the command:

```bash
git remote add origin <remote_repository_url>
```

To push your changes to the remote repository, run the command:

```bash
git push -u origin master
```

If you have changes in the remote repository and you want to get them to your local repository, run the command:

```bash
git pull origin master
```

### Cloning a git repository

To clone a git repository from a remote repository, run the command:

```bash
git clone <remote_repository_url>
# or
git clone <remote_repository_url> <directory_name> # to clone the repository to a specific directory
```

This command will create a directory with the name of the repository and download all the files in the repository to that directory.

You can also clone a specific branch of the repository by running the command:

```bash
git clone -b <branch_name> <remote_repository_url>
```

Some repositories might have submodules. To clone the repository with its submodules, run the command:

```bash
git clone --recurse-submodules <remote_repository_url>
```
