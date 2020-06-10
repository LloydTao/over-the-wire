# Level 9

## Level Goal

The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

## Useful Commands

- `$ grep`
- `$ sort` 
- `$ uniq` 
- `$ strings` 
- `$ base64` 
- `$ tr` 
- `$ tar` 
- `$ gzip` 
- `$ bzip2` 
- `$ xxd`

## Helpful Reading Material

Check out [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php).

Every command has three data streams (STDIN, STDOUT, STDERR), and we can manipulate those data streams in useful ways:

### Redirecting STDOUT and STDIN

- We can redirect STDOUT to write to a file by using `>` (e.g. `ls > output.txt`).
- We can append STDOUT to a file similarly by using `>>` instead of `>`.
- We can redirect a file into STDIN by using `<` (e.g. `wc -l < output.txt`).
- We can combine these operators (e.g. `wc -l < input.txt > output.txt`).

### Redirecting STDERR

- We can refer to a stream by value (`1>` is STDOUT, `2>` is STDERR).
- We can direct both streams using `&` (e.g. `ls > output.txt 2>&1`).

### Piping

- We can send data from one program to another by using `|` (e.g. `cat input.txt | head`).
- We can use many pipes in a row (e.g. `cat input.txt | head | tail`).
- Piping and redirection can be combined (e.g. `cat input.txt | head | tail > output.txt`).


## Walkthrough

Look at the directory's contents for some context.

`$ ls`

-> `data.txt

Read the file.

`$ cat data.txt`

-> ...
-> `U0NYdD3wHZKpfEg9qGQOLJimAJy6qxhS`
-> `flyKxCbHB8uLTaIB5LXqQNuJj3yj00eh`
-> `TThRArdF2ZEXMO47TIYkyPPLtvzzLcDf`
-> `cIPbot7oYveUPNxDMhv1hiri50CqpkTG`
-> `kJTBMD8k9OHyXwZ2aJMQkV23u0gyuoIO`
-> ...

We have many lines of junk, and need to find the unique occurrence. 

We can use `uniq -u` to print only the unique lines. We do need to sort it first.

`$ sort data.txt | uniq -u`

-> `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`

Awesome.

## Notes

None.
