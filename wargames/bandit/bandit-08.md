# Level 8

## Level Goal

The password for the next level is stored in the file `data.txt` next to the word **millionth**.

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

## Walkthrough

Look at the directory's contents for some context.

`$ ls`

-> `data.txt

Read the file.

`$ cat data.txt`

-> ...
-> `virtuosi        YlvLcmh6tAAXdkZb5NGu9yCjxHZeoha7`
-> `guarantors      ooq4uTy7isEPgn2rl9QEUriB5TMfOO90`
-> `proposed        liECD7g8oaQD9vnVckcUU22UAJedY5jZ`
-> `outburst        0nJl6agx4kjs08jIdCgwpqFreShql376`
-> `aquamarine      xgXPmIo5ZbPqjem7WHChxwOhORoczyoG`
-> ...

Yikes. Let's filter the results.

`$ cat data.txt | grep "millionth"`

-> `millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV`

Awesome.

## Notes

None.
