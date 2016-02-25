## Linux commands

### List only directories in a folder.
```shell
ls -d */
```


### List contents of a folder sorted by date.
Command which shows contents of a folder in `human readable`, `show hidden`, `print details`, `sort by date`, `reverse` [most recent at the bottom].
```shell
ls -haltr
```


### List files and sub-folders of a folder with absolute path -- useful for easy copy + pasting.
> Note this command does not recursively list sub-folders; only top level folder.
```shell
ls -1d $PWD/*
```
