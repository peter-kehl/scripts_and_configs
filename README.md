# Various scripts & configs

Clone with submodules: `git clone --recurse-submodules`.

# Config files
Use by creating symlinks. Suppose you cloned it as `~/GIT/scripts_and_configs`. Then
```
cd
ln -s GIT/scripts_and_configs/.gitconfig
ln -s GIT/scripts_and_configs/.spacemacs
cd .mozilla/firefox
cd *-default
ln -s ../../GIT/scripts_and_configs/mozillaChrome chrome
```

## Make Firefox profile ytd9zooq use tmpfs
The profile and its cache are stored under inactive folders (ignored by Firefox). They're copied
from and to /tmp and symlinked to those /tmp subfolders when used by Firefox. It risks that if the
machine is turned off abruptly, the profile & the cache will be as before Firefox was started.
However, if only Firefox itself exits abruptly, this does update the profile & the cache.

Once only:
```
cd ~/.mozilla/firefox
ln -s /tmp/firefox-ytd9zooq.light-67-pkehl

cd ~/.cache/mozilla/firefox
ln -s /tmp/firefox-cache-ytd9zooq.light-67-pkehl
```

Once per reboot (before using this Firefox profile):
```
~/GIT/scripts_and_configs/firefox-sh/firefox-sync-ytd9zooq.light-67
~/GIT/scripts_and_configs/firefox-sh/firefox-sync-cache-ytd9zooq.light-67
```

Start Firefox (which copies the modified files to the "static" storage afterwards):
```
~/GIT/scripts_and_configs/firefox-sh/firefox.sh
```

