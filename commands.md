## Add a file

`git add <filename>`

## Add some files by name

`git add <list of file>`

## Add all .txt files (same extension files)

`git add *.txt`

## Add all .txt files in docs directory

`git add docs/*.txt`

## Add all files in docs directory

`git add docs/`

## Add all .txt files in the whole project

`git add "*.txt"`

## Add all files

`git add --all`
OR
`git add .`

## Get back from staged area

`git rm --cached <filename>`
OR
`git reset HEAD <filename>`

## Diffrence between last commit and present version(Before stage)/Unstage diffrences

`git diff`

## Diffrence between staged version and last commmit

`git diff --staged`

## commit changes

`git commit`
`git commit -m "<your message>"`

## to add and commit in one command

`git commit -a -m "<your message>"`

## Amend last commmit and override commit message

`git add --all`
`git commit --amend -m "<your message>"`

## Move to the stage area from last commit

`git reset --soft HEAD^`

## totally delete the last commit

`git reset --hard HEAD^`

## Totally delete the last two commit

`git reset --hard HEAD^^`

## To watch all remote branches

`git branch -r`

## To switch into branches

`git checkout <branch name>`

## To create branch

`git branch <branch name>`

## To create brach and switch

`git branch -b <branch name>`

## Delete only remote branch

`git push origin :<branch name>`

## Delete branch locally

`git branch -d <branch name>`

## Delete branch forcefully

`git branch -D <branch name>`

## To watch remote log

`git remote show origin`

## Delete all remote branch refrences

`git remote prune origin`

## List all the tag

`git tag`

## Go to tag

`git checkout <tagname>`

## Add a tag

`git tag -a v1.0.0 -m "<commit message>"`

## Push all tags

`git push --tags`

## List of all remote branches

`git branch -r`

## Watch all remote branches

`git remote show <remote name>`

## Delete all deleted remote branch refrences

`git remote prune`

## Push branch into Heroko which is not master

`git push <Heroko branch name> <branch name>:master`

## Set configuration for local branch

`git config user.name <username>`
`git config user.email <email>`

## Set username password for local/paticular branch

`git config credential.helper store`
`git pull`

<!-- #### then provide the username and password for once, it won't ask you for password anymore -->

## To untrack a single file that has already been added/initialized to repository

`git rm --cached <filename>`

## To untrack every file that is now in `.gitignore`

`git rm -r --cached .`
