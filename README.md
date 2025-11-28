
# Simple bubblewrap script for running opencode in it's own namespace.

## Prerequsites
 
### Bubblewrap
Install 'bubblewrap' package on your system. This should most probably be available via your package manager.

### Install 'opencode'
This may differ and may need tweaks to the opencode script in this repo.

On ArchLinux:
```
$ yay opencode
```

On other distributions you need to check what folders things get installed in and update the opencode script with more read-only bind's.


## Setup

* Add the script to : ~/.local/my_scripts/

* Add ~/.local/my_scripts/ to PATH
```
export PATH=~/.local/my_scripts/:${PATH} >>~/.profile

```
* After logout/login, or "source ~/.profile" you should see:
```
$ which opencode
<your homefolder>/.local/my_scripts/opencode
```
Now you are setup to use opencode as you would normally do. Arguments are parsed and forwarded to the actual opencode binary.
```
$ cd <project folder>
$ opencode --whatever
```

## Notes
- If opencode is located anywhere else than /usr/bin/opencode you need to update the hardcoded path
- This has been tested on ArchLinux so required path's may be different for /usr/lib etc.
