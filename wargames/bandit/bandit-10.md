# Level 10

## Level Goal

The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `‘=’` characters.

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
-> `▒I▒▒▒Y▒i▒3_▒▒6z▒▒;▒▒G▒GJ▒▒;Y▒ä▒?▒▒▒˕▒.▒▒▒k7B▒L▒▒N▒▒▒%|▒▒䑌▒▒▒`
-> `pu▒▒OMd▒H`
-> `6m▒▒▒ӂ▒)▒I(n▒`
-> `▒z▒▒>▒5▒G▒▒▒▒▒▒▒▒C▒▒▒▒3CA▒󛬑t▒▒9▒▒▒hCx䫶n*ȴY▒▒ྶ▒▒`
-> `▒J޶#֩▒▒cq    ▒u5▒X▒▒sG▒&7▒$Q▒▒r\P▒▒▒0Z▒▒`
-> ...

Looks like a bunch of binary junk.

We need to use `strings` in order to get the human-readable text content of this file.

`$ strings data.txt`

-> ...
-> `WB|{`
-> `GhG$`
-> `========== the*2i"4`
-> `DUJmU`
-> `ux.j`
-> ...

Lots of lines. Let's filter it down by "several `‘=’` characters", like it said.

`$ strings data.txt | grep '==='`

-> `========== the*2i"4`
-> `========== password`
-> `Z)========== is`
-> `&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`

Well, that looks like our answer!

## Notes

None.
