---
title: 'Tutorial on how to remove blank lines from multiple files'
author: G. E. Saretto
date: July 2018
---

- After having prepared the files for training, we noted that `ketos` had produced `.txt` files containing blank lines, which slowed down and possibly interfered with the training process. This is something of a temporary solution; there are probably some more elegant ones.

1. Move into the folder where your files are.

2. Type this command:

> `for i in $(ls 0*.gt.txt); do cat $i | awk NF > 2_$i; done`

3. This will create a copy of each file with the blank lines removed; the new files will have a `2_` prefix. To rename them type this command:

> `for i in 2_*.txt; do mv -i "${i}" "${i/2_0/0}"; done`
