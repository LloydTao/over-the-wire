# Level 3

## Level Goal

The password for the next level is stored in a file called `spaces in this filename` located in the home directory.

## Useful Commands

- `$ ls`
- `$ cd`
- `$ cat`
- `$ file`
- `$ du`
- `$ find`

## Walkthrough

Same as last level. Read the file.

`$ cat 'spaces in this filename'`

-> `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`

Connect to the server with the new username and password.

## Notes

Using backslashes to escape the spaces can work too.

`$ cat spaces\ in\ this\ filename`
