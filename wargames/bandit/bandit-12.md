# Level 12

## Level Goal

The password for the next level is stored in the file `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

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

Check out [ROT13 on Wikipedia](https://en.wikipedia.org/wiki/ROT13).

ROT13 is a simple substitution cipher that replaces a letter with the character 13 places ahead.

You may recognise it as a Caesar cipher, but with a specific shift of 13 places.

Unix command `tr` will **translate** from one character set to another.


## Walkthrough

Look at the directory's contents for some context.

`$ ls`

-> `data.txt

Read the file.

`$ cat data.txt`

-> `Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh`

We can use `tr` in order to decode this. We'll split the alphabet 13 places along (i.e. swap A-M with N-Z).

Instead of stating every literal character, we can use `-` to use the full range.

`$ tr 'A-Ma-mN-Zn-z' 'N-Zn-zA-Ma-m' < data.txt`

-> `The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`

Simple enough!

## Notes

None.
