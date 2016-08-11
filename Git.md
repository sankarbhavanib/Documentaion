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
```
$ git branch -a     will give you both local and remove branches    
$ git branch -r     will give you remove branches
$ git branch        will give you local branches 

git commit --amend   ( to update the commit message )
to merger (force merge commits) 
————
step1 : git rebase -i HEAD~2
step2 : add “s” infant of coming you want to squash and save 
step3 : add # informant of commit message you want to keep and save the file 
step4 : git push -f origin gh-pages

git remote set-url origin git@github.com:username/repo.git
git remote set-url public git@github.com:paypal/PayPal-Android-SDK.git
git submodule update --init --recursive
public static final String BRAINTREE_DEMO_APP = "braintree-demo-app";——
git@github.paypal.com:bbheemanadham/developerspartaweb.git
cd /developer/developerspartaweb
git remote add upstream git@github.paypal.com:AppPlatform/developerspartaweb.git
git fetch upstream
git rebase upstream/master
git tag v0.0.1   to create tags 
git push —tag   to push tags 
git tag -d v0.0.1   to delete tag 
git push origin :refs/tags/v0.0.1   update the master with deleted tag   
git remote set-url origin git@github.XX.git
git log  ( gives list of commits )
git reset --hard 82335f6f1ed38acddf045c42aaa4cc761ff99604    ( you can reset it to commit id)
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

