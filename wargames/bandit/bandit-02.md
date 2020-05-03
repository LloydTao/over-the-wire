# Level 2

## Level Goal

The password for the next level is stored in a file called `-` located in the home directory.

## Useful Commands

- `$ ls`
- `$ cd`
- `$ cat`
- `$ file`
- `$ du`
- `$ find`

## Walkthrough

Same as last level. Read the file.

`$ cat ./-`

-> `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`

Connect to the server with the new username and password.

## Notes

The dash (`-`) is a special character. We can't use `$ cat -`.

There's a few approaches, but stating the explicit path is recommended.
