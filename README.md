Various scripts & configs

Clone with submodules: `git clone --recurse-submodules`.

Use by creating symlinks. Suppose you cloned it as `~/GIT/scripts_and_configs`. Then
```
cd
ln -s GIT/scripts_and_configs/.gitconfig
ln -s GIT/scripts_and_configs/.spacemacs
cd .mozilla/firefox
cd *-default
ln -s ../../GIT/scripts_and_configs/mozillaChrome chrome
```

