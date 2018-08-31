# gitNotes
Personal helper about Git

### Setting Up Workspace

[Udacity lesson](https://classroom.udacity.com/courses/ud775/lessons/2980038599/concepts/33417185870923)

### Commit

#### Message

"A good commit message is composed of two parts: a short message, less than 72 characters long, which briefly states (in active voice) the change being made; and a much longer, optional description, which is separated from the brief description by a newline."
https://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html

Android Studio >> Commit Changes dialog >> Commit message text box

You can separate short message and optional description with new line.

#### Amend

Change last commit or message with the change that you forgot.

Add the change

`git add .`

Commit with amend

(use -m argument to change commit message or you'll be prompted with previous commit message)

`git commit --amend`

or If you don't want to change commit message but add the forgotten change

`git commit --amend --no-edit`

If you pushed the commit that you amended, you need to use -f attribute to change the commit in remote.

`git push -f origin your-branch`

If not, just push it normally.

https://nathanhoad.net/git-amend-your-last-commit

https://help.github.com/articles/changing-a-commit-message/

https://medium.com/@igor_marques/git-basics-adding-more-changes-to-your-last-commit-1629344cb9a8

#### Move changes to another branch and revert master

Move all uncommitted changes to a new branch and revert the existing branch to HEAD.
https://gist.github.com/tonylukasavage/5672490


### Changing a remote's url

`git remote set-url origin https://github.com/USERNAME/REPOSITORY.git`

https://help.github.com/articles/changing-a-remote-s-url/

### Removing unstaged changes

For all

`git checkout --` 

Or the name of the file

`git checkout <insert-file-name-here>` 

### After sending file to repo, let git do not track any changes to file

Example: api_key file with empty string api key in it and then you stop
tracking changes in the file with the following command and then
update empty string with your api key.

`git update-index --skip-worktree path/to/file`

https://stackoverflow.com/a/50826529/1463542

### Removing files from staging area

remove all files:

`git reset HEAD .`

http://clubmate.fi/git-removing-files-from-the-staging-area-and-the-tree/


### Git Config: Setup your name and email address

`git config --global user.name "Firstname Lastname"`
`git config --global user.email "your_email@youremail.com"`
