# swc-conda-recipes
Conda meta-packages for helping with workshop installation

Core concepts:
  * environment.yml should be downloaded by end-users into a folder by itself, followed by

```
conda env create
```

in that folder.  This creates an env named like the folder containing environment.yml.  Please keep the "name" field in environment.yml consistent with the folder name.

  * environment.yml files do not support specifying different packages based on platform (selectors).  Conda recipes do.  We create metapackages that behave differently on different platforms, and have the environment.yml install those packages.  To change the environment people get, change these metapackages (currently here, as swc-[topic])
