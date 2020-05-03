# Level 5

## Level Goal

The password for the next level is stored in the only human-readable file in the `inhere` directory. 

Tip: if your terminal is messed up, try the `reset` command.

## Useful Commands

- `$ ls`
- `$ cd`
- `$ cat`
- `$ file`
- `$ du`
- `$ find`

## Walkthrough

Navigate to the directory.

`$ cd inhere`

Look at the directory's contents for some context.

`$ ls -a`

-> `.   -file00  -file02  -file04  -file06  -file08`
-> `..  -file01  -file03  -file05  -file07  -file09`

Look at the file type of each file.

`$ file ./*`

-> `./-file00: data`
-> `./-file01: data`
-> `./-file02: data`
-> `./-file03: data`
-> `./-file04: data`
-> `./-file05: data`
-> `./-file06: data`
-> `./-file07: ASCII text`
-> `./-file08: data`
-> `./-file09: data`

Read file 7.

`$ cat ./-file07`

-> `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`

## Notes

We're using the explicit path due to the dashes, as in Level 2.
