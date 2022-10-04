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

### Make Windows Terminal look amazing!
https://www.youtube.com/watch?v=AK2JE2YsKto
https://github.com/xcad2k/dotfiles/blob/main/.config/starship.toml

* Install new fonts: https://www.nerdfonts.com/font-downloads
Use right button of mouse on font and select "Install for all users".
To remove a font, access Control Panel, Appearence, Fonts, choose a font and press delete.

* Install chocolatey: https://chocolatey.org/install#individual
* Install starship: https://community.chocolatey.org/packages/starship

#### Ubuntu on Windows with WSL2 config
Install on Ubuntu using Terminal:
```
curl -sS https://starship.rs/install.sh | sh
```
Create a symbolic link to starship.toml:
```
mkdir ~/.config
ln -s /mnt/c/Users/<username>/.config/starship.toml ~/.config/starship.toml
```
