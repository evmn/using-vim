# Add Chapter Number Before Titles in Table of Contents

`toc.ncx` is the origin file, `toc.txt` is the updated file.

Use the following command to add chapter number before titles between line 64 and 485

```
:let i = 1 | 64,485g/<text>/s/>/\=printf(">Chap %02d: ", i)/ | let i = i+1
```

Compare two files with vimdiff:

```
vimdiff toc.txt toc.ncx
```
