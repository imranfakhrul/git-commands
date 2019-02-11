## Add a file 
`git add <filename>`

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

## Move to the stage area from last commit 
`git reset --soft HEAD^`