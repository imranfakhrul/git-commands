# Git commands

Daily used git commands archive (**PRs welcome**)

- **Initialize git repository**

  `git init`

- **Add files/folder into `.gitignore`**

  - Create a `.gitignore` file
  - Add file name or folder name into there

    Example:

    ![image](/assets/gitignore.png)

- **Add a file**

  `git add <filename>`

- **Add some files by name**

  `git add <list of file>`

- **Add all .txt files (same extension files)**

  `git add *.txt`

- **Add all .txt files in docs directory**

  `git add docs/*.txt`

- **Add all files in docs directory**

  `git add docs/`

- **Add all .txt files in the whole project**

  `git add "*.txt"`

- **Add all files**

  `git add --all`

  OR

  `git add .`

- **Add only part of a file**
- `git add --patch <filename>`

- **Get back from staged area**

  `git rm --cached <filename>`

  OR

  `git reset HEAD <filename>`

- **Difference between last commit and present version(Before stage)/Unstage differences**

  `git diff`

- **Difference between staged version and last commit**

  `git diff --staged`

- **Commit changes**

  `git commit`
  `git commit -m "<your message>"`

- **To add and commit in one command**

  `git commit -a -m "<your message>"`

- **Amend last commit and override commit message**

  `git add --all`
  `git commit --amend -m "<your message>"`

- **Pick specific commit from same or another branch to targeted branch**

  `git cherry-pick <commit_id>`

- **Pick file from another branch to targeted branch**

  `git checkout <branch_name> <file_name>`

- **Move to the stage area from last commit**

  `git reset --soft HEAD^`

- **totally delete the last commit**

  `git reset --hard HEAD^`

- **Totally delete the last two commit**

  `git reset --hard HEAD^^`

- **To watch all remote branches**

  `git branch -r`

- **To switch into branches**

  `git checkout <branch name>`

- **To create branch**

  `git branch <branch name>`

- **To create brach and switch**

  `git branch -b <branch name>`

- **Delete only remote branch**

  `git push origin :<branch name>`

- **Delete branch locally**

  `git branch -d <branch name>`

- **Delete branch forcefully**

  `git branch -D <branch name>`

- **To watch remote log**

  `git remote show origin`

- **Delete all remote branch references**

  `git remote prune origin`

- **List all the tag**

  `git tag`

- **Go to tag**

  `git checkout <tagname>`

- **Add a tag**

  `git tag -a v1.0.0 -m "<commit message>"`

- **Push all tags**

  `git push --tags`

- **List of all remote branches**

  `git branch -r`

- **Watch all remote branches**

  `git remote show <remote name>`

- **Delete all deleted remote branch references**

  `git remote prune`

- **Push branch into Heroko which is not master**

  `git push <Heroko branch name> <branch name>:master`

- **Set configuration for local branch**

  - Username

    `git config user.name <username>`

  - Email

    `git config user.email <email>`

- **Set username password for local/particular branch**

  - Run this command

    `git config credential.helper store`

  - Then pull the repository

    `git pull`

- **Remove cached password**

  `git config --global --unset credential.helper`

- **To untrack a single file that has already been added/initialized to repository**

  `git rm --cached <filename>`

- **To untrack every file that is now in `.gitignore`**

  `git rm -r --cached .`

- **Rename a local and remote git repository**

  - Checkout to old repository

    `git checkout <old name>`

  - Rename the repository

    `git branch -m <new name>`

  - Delete origin repository

    `git push origin --delete <old name>`

  - Push repository with new name

    `git push origin -u <new name>`

  - List the changed files before staging
    `git diff --name-only`

  - List the changed files in staging
    `git diff --name-only --cached`

  - List the changed files of current commit
    `git diff --name-only HEAD^ HEAD`

- **Batch search and delete local branches when there are too many**

  > **NOTE:** Beaware of `grep`, `egrep`, `xargs` in **Windows**
  >
  > > You can check out below link if you are facing any issue with these commands
  > >
  > > > [git grep and xargs in Windows Batch file?](https://stackoverflow.com/questions/38672888/git-grep-and-xargs-in-windows-batch-file)

  - Delete all branches matching keyword, e.g: dev<some-suffix> or <some-prefix>dev

    - Delete all branches suffixing `dev`

      `git branch --list "*dev" | xargs git branch -D`

    - Delete all branches prefixing `dev`

      `git branch --list "dev*" | xargs git branch -D`

    - Delete all branches prefixing `dev` and ends only with a number (e.g: task number)

      `git branch --list "dev*[0-9]" | xargs git branch -D`

  - Delete all _except_ given branches, e.g: except develop and master branchs

    `git branch | egrep -v "master|develop" | xargs git branch -D`

    _here `-v` means "invert the match"_

## For Mac users only

- **Often for Mac users, using bash terminal, you do not find git autocomplete in bash**

  > **STEP 1:** From [git-completion](https://github.com/git/git/tree/master/contrib/completion)
  >
  > > Get git-completion script
  >
  > > `curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash`

  > **STEP 2:** Update .bash_profile
  >
  > > Add the following code to your .bash_profile (~/.bash_profile).

  ```
  if [ -f ~/.git-completion.bash ]; then
    . ~/.git-completion.bash
  fi
  ```

  > **STEP 3:** Apply the changes
  >
  > > `source ~/.bash_profile`

  Now you should be able to use git autocomplete in your bash terminal.

- **Delete all `.DS_Store` files from `git` `—cached`**

  `find . -name '.DS_Store' -type f | xargs git rm -r --cached`

  _You can use similar command for other file names_

  _You can use regex in the search string parameter_
