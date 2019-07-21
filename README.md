Various configs

Clone with submodules: `git clone --recurse-submodules`.

Use by creating symlinks. Suppose you cloned it as `~/GIT/configs`. Then
```
cd
ln -s GIT/configs/.gitconfig
ln -s GIT/configs/.spacemacs
cd .mozilla/firefox
cd *-default
ln -s ../../GIT/configs/mozillaChrome chrome
```

