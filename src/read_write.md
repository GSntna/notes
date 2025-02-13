# Reading and writing files

## Index

* [Navigating through system](#navigating-through-system)
    * [pathlib](#path-library)
    * [os](#os-library)
    * [Navigation functions summary](#navigation-functions-summary)

## Navigating through system

### Path library

The `Path` module from the `pathlib` library allows to manipulate file paths and
navigate through the system. These are some functions in the `Path` module:

```py
>>> from pathlib import Path
>>> Path('folder', 'subfolder', 'file.txt')  # returns path (adapted to os)
PosixPath('folder/subfolder/file.txt')
>>> Path.home()                              # returns home directory
PosixPath('/home/user')
>>> Path.cwd()                               # get current working directory
PosixPath('/home/user/current/working/directory')

# Getting ancestor folder of a path
>>> Path.cwd().parents[0]
PosixPath('/home/user/current/working')
>>> Path.cwd().parents[1]
PosixPath('/home/user/current/')
>>> Path.cwd().parents[5]
PosixPath('/home')

# get the attributes of a path
>>> p = Path('/home/user/current/file.txt')
>>> p.anchor
'/'
>>> p.parent
PosixPath('/home/user/current/file.txt')
>>> p.name
'file.txt'
>>> p.stem
'file'
>>> p.suffix
'.txt'
>>> p.drive  # what's before the anchor ('C:' in Windows)
''
```

### os library

Another library used for navigation and manipulation of files and directories is
`os`. This library is older than `pathlib`, so it can do most of the things that
`pathlib` does. Here are some useful functions not covered by the latter:

```py
>>> import os
>>> os.makedirs('/home/user/new/folder/paths')  # create one or multiple folders
>>> os.path.abspath('.')  # returns the absolute path
>>> os.path.isabs('.')  # boolean if path is absolute
False
>>> os.sep  # gets the separator for the OS
'/'  # '\\' for Windows
```

### Navigation functions summary

| Function | Description |
| -------- | ----------- |
