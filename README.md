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

#### Cloning an already created repository

Pushing and pulling

how to create and upload an SSH key 
