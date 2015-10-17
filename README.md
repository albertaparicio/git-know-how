# Git Know-How

## Git initial setup

### Setup username and e-mail

To set your username and e-mail up, run these two commands in the Terminal, 
inside the project's folder:

`git config --global user.name "Your user name"`

`git config --global user.email "your@email.direction"`

### Repository initialization

There are two possible ways to start a repository.

#### Creating a local repository and uploading it to the remote server

In this case, the initialization goes from local to remote.

`mkdir repo_folder`

`cd repo_folder`

`git init`

`git remote add origin git@remote.server:server_username/project-name.git`

The remote direction can be obtained at the project's page at the remote server. This direction can be obtained to connect through **HTTPS** (Requires user and password at every `push` and `pull`) or through **SSH** (*__Recommended__* Does not require user and pass, but needs an SSH key to be created and uploaded)

`git add .`

`git commit`

`git push -u origin master`

This is the recommended command, although `git push` usually works well, too.

#### Cloning an already created repository

`git clone git@remote.server:server_username/project-name.git`

`cd project_folder`

`touch README.md`

`git add README.md`

These two README.md commands are an example of making any changes in the project.

`git commit -m "add README"`

The commit message serves as a way to rapidly identify what has been changed in the project.

`git push -u origin master`

## Git workflow

The command `git status` can be used at any moment to check if there are commits to push, changes to commit, etc. The typical workflow using a Git repository is as follows:

1. `git pull` in order to download anything new that has been done to the project.
2. Work on the project.
3. `git add files_to_commit`. All files that you want to be reflected on this commit must be added here. Not necessarily all changed files must be uploaded in a single commit.
4. `git commit` or `git commit -m "commit_message`. The difference between them is that the first command opens a Terminal text editor (By default, `nano` in Linux, `vi` in Mac OS systems) and the second one gets the message written directly at the command-line.

    This default editor can be changed with `git config --global core.editor "chosen_editor"`.
5. If you want to continue working on the project, do so and `git commit` any other changes. If you have finished, now it is the time to `git push` all these new commits to the remote server.
    It is advisable to push all commits at once, so the remote server is less stressed.

### Pushing and pulling

Remote Git servers like GitHub or GitLab allow two ways of connecting to them. One is via HTTPS, the other is SSH.

The HTTPS method is the most simple to set up. It just asks for your server username and password, and sends the data through port 443 (HTTPS default). It is advisable if your connection does not allow you to use port 22 (SSH default).

The SSH method requires a slightly more complex setup, but when pushing and pulling data, there is no user or pass to be input. It is not always available, as your connection may have blocked port 22. (Not usual in domestic connections)

#### Setting up an SSH connection

1. First of all, the local repository must have an SSH remote direction set up.
    To obtain your project's SSH direction, check its main page, select the SSH option and copy it:
    
    ![Alt text](/path/to/img.jpg "Optional title")


how to create and upload an SSH key 
