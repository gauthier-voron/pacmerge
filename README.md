Pacmerge
========

Merge or remove .pacnew files in your system.

Just another convenience script to find .pacnew files and merge them with their
original files. The user can preview and modify the changes before to apply
them.

```
pacmerge
:: /etc/pacman.d/mirrorlist [a,e,v,o,r,s,j,q,?] ?
 a apply patch and remove pacnew file
 e edit pacnew patch
 v view result of pacnew patch
 o view original file
 r remove pacnew file
 s skip this file and let unchanged
 j jump to next file and come back later
 q quit this program
 ? print help
:: /etc/pacman.d/mirrorlist [a,e,v,o,r,s,j,q,?] 
```

Use can control how the original file is modified with option 'e'. Pacmerge
genrates a patch from the diff between the original and the pacnew file and let
the user edit it.


Dependencies
------------

Pacmerge is a perl script calling a few external commands to work. The
essential ones are `diff` and `patch`. The `locate` or the `find` command is
used to locate pacnew files but user can specify a custom command. Finally an
editor is required to edit patches.

  * perl
  * diff
  * patch
  * locate (optional)
  * find (optional)

The script also uses a non core perl module.

  * File::Which
