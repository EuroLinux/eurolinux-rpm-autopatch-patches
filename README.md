# EuroLinux autopatches

This repository contains patches used by the
[https://github.com/EuroLinux/python-rpmpatch](https://github.com/EuroLinux/python-rpmpatch).


The repository structure is as follows:

Root level for each version of the EuroLinux
```
├── el6
├── el7
├── el8
├── el9
```

Then each branded/changed package has its directory in which there are files,
patches and '.ini' file for the package. For example firefox for EuroLinux 9:
```
├── el9
│   └── firefox
│       ├── distribution.ini
│       ├── firefox-eurolinux-default-prefs.js
│       └── firefox.ini
```


## How to use

- Clone repository wherever You want. In the example below repository was cloned
  into the `/tmp/` directory
- set `--config` in for the `./rpmpatch/patchsrpm.py` to the one that you want
  to use. Example:
  ```bash
  ./rpmpatch/patchsrpm.py --config=/tmp/eurolinux-rpm-autopatch-patches/el9/ /PATH/TO/SRPM --keep_dist 
  ```
