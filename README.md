# gitrick
Comandos git, aliases, pipelines de execução e truques.

### usage
1. git clone https://github.com/viniciusknob/gitrick.git
2. Make sure git files are executable (otherwise user chmod +x)
3. Add local repository path for gitrick to PATH variable

### aliases
go = checkout  
find = !git branch -r | grep  
st = status -sb  
lg = log --pretty='%C(yellow)%h%Creset %Cblue%an%Creset %Cgreen%cr%Creset%Cred%d%Creset %s'  
lgmh = !git lg origin/master..HEAD  
lgmu = !git lg origin/master..@{u}  
lguh = !git lg @{u}..HEAD  
merges = !git lgmh --merges  
allmerges = !git lg --merges  
sno = show --name-only  
rim = rebase -i origin/master  
poh = push origin HEAD  
pfwloh = push --force-with-lease origin HEAD  
undo = reset --mixed HEAD^  
rhu = reset --hard @{u}  
fixup = commit --fixup  
ccsne = commit --cleanup=scissors --no-edit  
cane = !git add -N . && git commit -a --amend --no-edit  
save = !git add -N . && git commit -am 'SAVEPOINT'  
aliases = !git config --list | grep 'alias'  
upstream = rev-parse --abbrev-ref --symbolic-full-name @{u}  
rerere-clear = !rm -rf .git/rr-cache  
