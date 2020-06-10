# Level 7

## Level Goal

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Useful Commands

- `$ ls`
- `$ cd`
- `$ cat`
- `$ file`
- `$ du`
- `$ find`
- `$ grep`

## Walkthrough

Search for all files owned by group `bandit6` and user `bandit7`.

`$ find /* -size 33c -group bandit6 -user bandit7`

That's an annoying amount of errors.

Let's use `grep` to filter these results.

`$ find /* -group bandit6 -user bandit7 2>&1 | grep -v "Permission denied"`

-> `/dev/pts/29`
-> `/dev/pts/26`
-> `/etc/bandit_pass/bandit7`
-> `...`
-> `/run/screen/S-bandit7`
-> `/var/lib/dpkg/info/bandit7.password`

Read the file.

`$ cat /var/lib/dpkg/info/bandit7.password`

-> `HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs`

## Notes

None.
