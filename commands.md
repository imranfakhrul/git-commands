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

## totally delete the last two commit 
`git reset --hard HEAD^^`