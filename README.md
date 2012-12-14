mevalonate
==========

Mevalontae and non-Mevalonate pathway in dinos

Directory layout
----------------

DOXP\_HMMs: Mavelonate pathway domain HMMs

TODO: document generation of HMMs
---------------------------------

In order to extract the abbreviated domain name, the ID of the contig,
and the reading frame I used the follwing pipe. In esseence, I used awk
to print the 1st and 3rd column of the tabular output file (DOXP.tbl),
and piped that into the stream editor sed to replace part of the contig
name with a tab. The output should have 3 columns.

```bash
awk '{ print $1"\t"$3 }' Pglacialis/DOXP.tbl | sed 's/v3_/v3\t/g' > Pglacialis/DOXP.contigs
```
