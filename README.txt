SS13 40.76 rebuilt source (June 2004, BYOND 339). Compiles with 0 errors to a .dmb that is BYTE-IDENTICAL to the original
cellautomata.dmb (md5 6c87fbb98897a03a73f754a2e8edb0c7, 532232 bytes; checked with md5, cmp and the audit, 3 compiles).

Compiler: BYOND 339 (C:\s40\byond339\x), header "world bin v339 / min compatibility v338" as in the original.
  sh C:/sp76/work/cmp.sh <folder>        (compiles <folder>/cellautomata.dme, prints md5 + audit against the original)
From scratch: sh C:/sp76/work/rebuild.sh <new folder>  (40.70 source from C:\misc\dev\space4070 + work\port4076.patch
  + map written from the 40.76 .dmb + icons from the 40.76 .rsc; tested: same .dmb md5 as the original).
The .rsc is rebuilt from the original icons; a compiled .rsc never matches byte for byte (dates, slack), its files do.

How it was made: the bit-perfect 40.70 source with every 40.70 -> 40.76 change put in: 22 changed procs (3-way merge),
11 new procs, 4 new types (reinforced wall, reinforced metal sheet, yellow jumpsuit, technician wardrobe), 2 new vars,
the new changelog text, and 4 changed icons (items, mob, stationobjs, wall). Where 40.93.0 has the same code its
spelling was used (C:\misc\dev\space40930).

Not the author's text: comments are gone (the .dmb does not store them); blank lines stand in for lines whose content
is unknown. Choices that the bytes cannot decide are listed in C:\sp76\NOTES.md - for example the one-line
`/obj/machinery/computer/med_data{var/printing = null}` after med_data's Topic in cryo.dm: the bytes prove that some
declaration with a value sits there, not that it was written exactly this way.
