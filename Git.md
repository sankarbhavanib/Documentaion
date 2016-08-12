### To set up alias for git commands 
https://github.com/robbyrussell/oh-my-zsh/blob/7fabc8bca4/plugins/git/git.plugin.zsh


### To config the configurations
```
vim .git/config   

```
##new repo creation …or create a new repository on the command line
```
echo "# Caliculator-Andriod" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/sankarbhavanib/Caliculator-Andriod.git
git remote set-url origin git@github.com:sankarbhavanib/Caliculator-Andriod.git
git push -u origin master
```

### Software to down load  and install to resolve merge issue
```
http://www.sourcegear.com/diffmerge/downloaded.php 
git mergetool
```

###To merger (force merge commits) 
```
step1 : git rebase -i HEAD~2
step2 : add “s” infant of coming you want to squash and save 
step3 : add # informant of commit message you want to keep and save the file 
step4 : git push -f origin gh-pages
```
### To Rebase 
```
git fetch upstream
git rebase upstream/master
git tag v0.0.1   to create tags 
git push —tag   to push tags 
git tag -d v0.0.1   to delete tag 
git push origin :refs/tags/v0.0.1   update the master with deleted tag   
git remote set-url origin git@github.XX.git
git log  ( gives list of commits )
git reset --hard 82335f6f1ed38acddf045c42aaa4cc761ff99604    #you can reset it to commit id
```

##For intarative rebase 
https://www.youtube.com/watch?v=mBCJCuU3p7I

##To build sub module project
```
step1   : close sub project inside the main project 
step 2  : establish connection   
$git submodule update --init
step3   : mvn clen install ( submodule to rebuild )   and mvn clean deploy to deploy submodule to nexas 
step 4  : go to main module folder and do mvn clean install -U to get latest changes 
```

## FQA
1. How to delete Local/remore branch?
2. How to rename branch local /remore?
3. How to Undo last commit ?
4. How to update commit message ?
5.how to checkout remore repo?  
6. what is the difference between Pull Vs fetch?  git pull does a git fetch followed by a git merge. You can do a git fetch at any time to update your remote-tracking branches under refs/remotes/<remote>/. This operation never changes any of your own local branches under refs/heads, and is safe to do without changing your working copy
7. http://career.guru99.com/top-40-interview-questions-on-git/

```
git branch -m old_branch new_branch         # Rename branch locally    
git push origin :old_branch                 # Delete the old branch    
git push --set-upstream origin new_branch   # Push the new branch, set local branch to track the new remote
git reset --soft HEAD~1                     # How to Undo last commit you can use --hard to stash chages 
git commit -amend                           # will allow you to edit last comit 
git rebase -i HEAD~3                        # will open the commit history in editor will allow your o modify multiple commit messages 
git stash                                   # to save current changes 
git stash pop                               # to retrieve stashed chages
git branch -a                               # will give you both local and remove branches    
git branch -r                               # will give you remove branches
git branch                                  # will give you local branches 
git remote set-url origin git@github.com:XXX.git  #  to set origin
git remote set-url public git@github.com:XXX.git  #  to set origin to public repo 
git submodule update --init --recursive    # update all submodules 
```

