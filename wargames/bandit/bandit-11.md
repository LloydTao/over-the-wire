# Level 11

## Level Goal

The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

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

Check out [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64).

Base64 is a binary-to-text encoding scheme used to represent binary data as an ASCII string.

A Base64 digit represents 6 bits of data, as 64 is equal to 2^6.

The Base64 digits are `A-Z` (0-25), `a-z` (26-51), `0-9` (52-61), `+` (62) and `/` (63).


## Walkthrough

Look at the directory's contents for some context.

`$ ls`

-> `data.txt

Read the file.

`$ cat data.txt`

-> `VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==`

Looks like it's composed of the Base64 alphabet we looked at earlier.

We can use the 'decode' flag for 'base64' in order to decode this.

`$ base64 -d data.txt`

-> `The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`

Simple enough!

## Notes

None.
