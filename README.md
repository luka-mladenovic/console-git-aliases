# console-git-aliases

e.=explorer .
history=cat %CMDER_ROOT%\config\.history
unalias=alias /d $1

ls=ls --show-control-chars -F --color $*
pwd=cd
clear=cls
touch=echo $null >> $*

phpmig=php artisan migrate
phpref=php artisan migrate:refresh
phpreset=php artisan migrate:reset
phproll=php artisan migrate:rollback
phprollx=php artisan migrate:rollback $*

phpseed=php artisan db:seed
phpseedx=php artisan db:seed --class=$*

makemod=php artisan make:model $* -m -c && composer dump-autoload
makemig=php artisan make:migration $* && composer dump-autoload

cdump=composer dump-autoload

glt=gulp test
glw=gulp watch
unit=phpunit
univ=phpunit --verbose
unid=phpunit --debug
unig=phpunit --group $*
unif=phpunit --filter $*

tinker=php artisan tinker

g=git $*
gs=git status
gss=git status -s
ga=git add $*
gaa=git add -A
gc=git commit
gca=git commit --amend
gcaa=git commit -A --amend

addcom=git add -A && git commit -m $*
save=git add -A && git commit -m 'Work in progress'

gist=git stash
gisl=git stash list
gisa=git stash apply
gisp=git stash pop
gisb=git stash branch $*
giss=git stash show -p stash@{$*}

gdev=git checkout develop
gmas=git checkout master
gica=git checkout $*
gicb=git checkout -b $*
gmer=git merge --no-ff $*

gres=git reset
gresh=git reset HEAD --hard
grev=git revert
gcln=git clean -fdx

branchcd=git branch --sort=-committerdate
branchcdr=git for-each-ref --sort=-committerdate refs/heads/

gl=git log --oneline --all --graph --decorate  $*
gll=log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat
dog=git log --all --decorate --oneline --graph
wdiff=git diff --color-words
gfl=gitlog -u
