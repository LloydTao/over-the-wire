# Level 6

## Level Goal

The password for the next level is stored in a file somewhere under the `inhere` directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

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

We're able to list files recursively using `$ find`.

This command can take a flag `-size 1033c` to find files with 1033 bytes.

`$ find -size 1033c`

-> `./maybehere07/.file2`

Read the file.

`$ cat ./maybehere07/.file2`

-> `DXjZPULLxYr17uwoI01bNLQbtFemEgo7`

## Notes

We only needed one of the criteria to succeed, but for fun:

- To find the type of each file: `$ find -exec file {} \;`.

- To actually filter our results: `$ find -exec file {} \; | grep "ASCII text"`.

- To find non-executable files, we can use the negated flag `! -executable`.

- Our final command: `$ find -size 1033c ! -executable -exec file {} \; | grep "ASCII text"`.
