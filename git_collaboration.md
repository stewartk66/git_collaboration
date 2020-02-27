# git collaboration
# GET NOTES FROM `chendaniely` REPOS
## Clone a repository from github (non-SSH)
```

stewa@LAPTOP-58OP9CKK MINGW64 ~
$ cd /c/users/stewa/MyStuff/git/

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git
$ git clone https://github.com/stewartk66/git_collaboration.git
Cloning into 'git_collaboration'...
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (5/5), 2.25 KiB | 5.00 KiB/s, done.

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git
$ ls
git_basics/  git_collaboration/

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git
$ cd git_collaboration/

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ nano README.md

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git add .

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git commit -m "first commit update to readme"
[master 351e6cc] first commit update to readme
 2 files changed, 2 insertions(+)
 create mode 100644 Annotation 2020-02-26 181839.png

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git remote -v
origin  https://github.com/stewartk66/git_collaboration.git (fetch)
origin  https://github.com/stewartk66/git_collaboration.git (push)

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --decorate --all
* 351e6cc (HEAD -> master) first commit update to readme
* d6f5672 (origin/master, origin/HEAD) Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 71.20 KiB | 1.15 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To https://github.com/stewartk66/git_collaboration.git
   d6f5672..351e6cc  master -> master

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$
```
## Command History #1
```
  141  git --version
  142  cd  cd /c/Users/stewa/MyStuff/git/
  143   cd /c/Users/stewa/MyStuff/git/
  144  ls
  145  ls
  146  cd /c/users/stewa/MyStuff/git/
  147  git clone https://github.com/stewartk66/git_collaboration.git
  148  ls
  149  cd git_collaboration/
  150  nano README.md
  151  git add .
  152  git commit -m "first commit update to readme"
  153  git remote -v
  154  git log --oneline --graph --decorate --all
  155  git push origin master
  156  history

```
## Create branch and switch/checkout commands
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch my_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch
* master
  my_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git checkout my_branch
Switched to branch 'my_branch'
D       Annotation 2020-02-26 181839.png

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git switch my_branch
Already on 'my_branch'
D       Annotation 2020-02-26 181839.png

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git branch -a
  master
* my_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
```
## Command History #2
```
  158  git status
  159  git branch my_branch
  160  git branch -a
  161  git branch
  162  git checkout my_branch
  163  git switch my_branch
  164  git branch -a
  165  hostory
  166  history
```
## Using `checkout`
* Use checkout to move HEAD to a different branch or commit  
* More recent versions of git have `restore` and `switch` commands instead of more complex `checkout` commands 

##
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ nano readme.md

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git status
On branch my_branch
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    Annotation 2020-02-26 181839.png
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git add .

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git commit -m "branch and switch"
[my_branch c5f23c9] branch and switch
 2 files changed, 2 insertions(+)
 delete mode 100644 Annotation 2020-02-26 181839.png

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git log --oneline --graph --decorate --all
* c5f23c9 (HEAD -> my_branch) branch and switch
* 351e6cc (origin/master, origin/HEAD, master) first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git push origin my_branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 379 bytes | 13.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'my_branch' on GitHub by visiting:
remote:      https://github.com/stewartk66/git_collaboration/pull/new/my_branch
remote:
To https://github.com/stewartk66/git_collaboration.git
 * [new branch]      my_branch -> my_branch

```
## Switch branches and check readme.md file content
Switch branches and checking content of the README.md file will show that the files are being updated as part of the switch 
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ cat README.md
# git_collaboration
Git Collaboration Live Training

git clone as a one time copy repo from remote

create branch & checkout/switch to move HEAD to that branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ cat README.md
# git_collaboration
Git Collaboration Live Training

git clone as a one time copy repo from remote

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$

```
## Command History #3
```
  167  nano readme.md
  168  git status
  169  git add .
  170  git commit -m "branch and switch"
  171  git log --oneline --graph --decorate --all
  172  git push origin my_branch
  173  cat README.md
  174  git switch master
  175  cat README.md
  176  history
```
## Check current position
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --decorate --all
* c5f23c9 (origin/my_branch, my_branch) branch and switch
* 351e6cc (HEAD -> master, origin/master, origin/HEAD) first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$
```
## Basic process to add changes to remote repo
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git switch my_branch
Switched to branch 'my_branch'

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ nano README.md

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git status
On branch my_branch
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git add .

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git status
On branch my_branch
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md


stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git commit -m "further changes"
[my_branch 5b03a76] further changes
 1 file changed, 2 insertions(+)

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git push origin my_branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 316 bytes | 10.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/stewartk66/git_collaboration.git
   c5f23c9..5b03a76  my_branch -> my_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$

```
## github `Pull Request` and `Issues`
Use github to create a `pull request`. Similar to gitlab `Merge request`.
Use github to add an `Issue` or `Project` which can then be associated with the `pull request`

github has `checks` and `actions` to 'run' for example unit tests before allowing merge 

git pull = git fetch + git merge

## Local Branchs left with no Remote
After accepting  Pull Request the branch should be deleted in github. _However_, this will leave `local` with references to the deleted branch

```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_branch
```

Although my_branch was deleted in github
 it is still local so need to tidy up

 ```
 stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_branch)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git pull origin master
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 622 bytes | 2.00 KiB/s, done.
From https://github.com/stewartk66/git_collaboration
 * branch            master     -> FETCH_HEAD
   351e6cc..972a4f4  master     -> origin/master
Updating 351e6cc..972a4f4
Fast-forward
 Annotation 2020-02-26 181839.png | Bin 73507 -> 0 bytes
 README.md                        |   4 ++++
 2 files changed, 4 insertions(+)
 delete mode 100644 Annotation 2020-02-26 181839.png

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   972a4f4 (HEAD -> master, origin/master, origin/HEAD) Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 (origin/my_branch, my_branch) further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit
```

## Use `--prune` to remove local ref to deleted remote branch

```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git fetch --prune --all
Fetching origin
From https://github.com/stewartk66/git_collaboration
 - [deleted]         (none)     -> origin/my_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```
 Reference to the origin/my_branch has gone but still has ref to my_branch.
 ## Remove local branch
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -d my_branch
Deleted branch my_branch (was 5b03a76).

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   972a4f4 (HEAD -> master, origin/master, origin/HEAD) Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

```

## Command History #4
```
  177  git log --oneline --graph --decorate --all
  178  git switch my_branch
  179  nano README.md
  180  git status
  181  git add .
  182  git status
  183  git commit -m "further changes"
  184  git push origin my_branch
  185  git checkout master
  186  git pull origin master
  187  git branch -a
  188  git log --oneline --graph --all
  189  git fetch --prune --all
  190  git status
  191  git branch -a
  192  git branch -d my_branch
  193  git log --oneline --graph --all
  194  git branch -a
  195  git status
  196  history

```

## Exercise to create a second branch, work with it & delete it
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch my_second_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git switch my_second_branch
Switched to branch 'my_second_branch'

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ nano readme.md

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git add .
git
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git commit -m "more changes"
[my_second_branch d4cd8df] more changes
 1 file changed, 3 insertions(+)

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git push origin my_second_branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 310 bytes | 310.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'my_second_branch' on GitHub by visiting:
remote:      https://github.com/stewartk66/git_collaboration/pull/new/my_second_branch
remote:
To https://github.com/stewartk66/git_collaboration.git
 * [new branch]      my_second_branch -> my_second_branch
```
Should have switched to master at this point but didn't 
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git pull origin master
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 631 bytes | 9.00 KiB/s, done.
From https://github.com/stewartk66/git_collaboration
 * branch            master     -> FETCH_HEAD
   972a4f4..ac2651f  master     -> origin/master
Updating d4cd8df..ac2651f
Fast-forward

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git branch -a
  master
* my_second_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_second_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git log --oneline --graph --all
*   ac2651f (HEAD -> my_second_branch, origin/master, origin/HEAD) Merge pull request #2 from stewartk66/my_second_branch
|\
| * d4cd8df (origin/my_second_branch) more changes
|/
*   972a4f4 (master) Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git fetch --prune --all
Fetching origin

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git status
On branch my_second_branch
nothing to commit, working tree clean

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git branch -a
  master
* my_second_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_second_branch
```
... now to do it properly, start by switching to master

### Update master
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (my_second_branch)
$ git switch master
Switched to branch 'master'
Your branch is behind 'origin/master' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git pull origin master
From https://github.com/stewartk66/git_collaboration
 * branch            master     -> FETCH_HEAD
Updating 972a4f4..ac2651f
Fast-forward
 README.md | 3 +++
 1 file changed, 3 insertions(+)

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_second_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_second_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   ac2651f (HEAD -> master, origin/master, origin/HEAD, my_second_branch) Merge pull request #2 from stewartk66/my_second_branch
|\
| * d4cd8df (origin/my_second_branch) more changes
|/
*   972a4f4 Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit
```
### Prune master 
Hadn't removed remote branch at this point so didn't 'prune' local 
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git fetch --prune --all
Fetching origin

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  my_second_branch
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/my_second_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -d my_second_branch
Deleted branch my_second_branch (was ac2651f).

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   ac2651f (HEAD -> master, origin/master, origin/HEAD) Merge pull request #2 from stewartk66/my_second_branch
|\
| * d4cd8df (origin/my_second_branch) more changes
|/
*   972a4f4 Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git pull origin master
From https://github.com/stewartk66/git_collaboration
 * branch            master     -> FETCH_HEAD
Already up to date.

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   ac2651f (HEAD -> master, origin/master, origin/HEAD) Merge pull request #2 from stewartk66/my_second_branch
|\
| * d4cd8df (origin/my_second_branch) more changes
|/
*   972a4f4 Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit
```
Deleted local branch at this point but hadn't deleted the remote so remote still being referred to  
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git fetch --prune --all
Fetching origin
From https://github.com/stewartk66/git_collaboration
 - [deleted]         (none)     -> origin/my_second_branch

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```
Reference to remote has now been removed
```
stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git log --oneline --graph --all
*   ac2651f (HEAD -> master, origin/master, origin/HEAD) Merge pull request #2 from stewartk66/my_second_branch
|\
| * d4cd8df more changes
|/
*   972a4f4 Merge pull request #1 from stewartk66/my_branch
|\
| * 5b03a76 further changes
| * c5f23c9 branch and switch
|/
* 351e6cc first commit update to readme
* d6f5672 Initial commit

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

stewa@LAPTOP-58OP9CKK MINGW64 /c/users/stewa/MyStuff/git/git_collaboration (master)
$
```
The branches are now reported as expected  
The git fetch ... `--prune` tidies up local refs to deleted branches
## Command History #5
```
  197  git branch my_second_branch
  198  git switch my_second_branch
  199  nano readme.md
  200  git add .
  201  git commit -m "more changes"
  202  git push origin my_second_branch
  203  git pull origin master
  204  git branch -a
  205  git log --oneline --graph --all
  206  git fetch --prune --all
  207  git status
  208  git branch -a
  209  git switch master
  210  git pull origin master
  211  git branch -a
  212  git log --oneline --graph --all
  213  git fetch --prune --all
  214  git status
  215  git branch -a
  216  git branch -d my_second_branch
  217  git log --oneline --graph --all
  218  git pull origin master
  219  git log --oneline --graph --all
  220  git fetch --prune --all
  221  git status
  222  git branch -a
  223  git log --oneline --graph --all
  224  git branch -a
  225  git status
  226  history
```

## reset / restore
```
git reset --hard <hash> to reset to hash 
```

## merge, rebase, cherrypick

### merge
seems a bit dodgy,  merged branch onto local master!!!

### rebase
1 rewind your branch commits back to common master
2 apply master branch commits to bring it up to date
3 replay your branch commits 

`review video at this point about merge conflict`

search for `atlassian git workflow` for more informatio n on feature branch workflow 
- also include other types of workflow