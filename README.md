# vim-HowTo
All about VIm

# Bash comment/uncomment
[source](https://stackoverflow.com/questions/1676632/whats-a-quick-way-to-comment-uncomment-lines-in-vim/1676659#1676659)

Dans le fichier .vimrc ou /etc/vim/vimrc, à la fin ajouter le code suivant :
```
"insert and remove comments in visual and normal mode
vmap ,ic :s/^/#/g<CR>:let @/ = ""<CR>
map  ,ic :s/^/#/g<CR>:let @/ = ""<CR>
vmap ,rc :s/^#//g<CR>:let @/ = ""<CR>
map  ,rc :s/^#//g<CR>:let @/ = ""<CR>
```

Désormais, en visuel ('v') pour commenter en bash, il faut utiliser la séquence : 
- ',' 'i' 'c' pour commenter (iNSERT cOMMENT)
- ',' 'r' 'c' pour décommenter (rEMOVE cOMMENT)
