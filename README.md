# aethel-public
Repository containing the public subset of the [AETHEL dataset](http://www.lrec-conf.org/proceedings/lrec2020/pdf/2020.lrec-1.647.pdf).


The repository contains 8,569 linear logic theorems, each corresponding to a parse of a written Dutch sentence or phrase.
Included in the LEXICON directory are also files containing lexical type assignments for 81,730 words 
(obtained from the aggregation of the full dataset). 

---

#### Binary Version
You can download a binary version of the data in the form of a python pickle from 
[here](https://surfdrive.surf.nl/files/index.php/s/jIpWUphW7RSQJ5V).
To be able to access the data you will need to clone the 
[extraction code](https://github.com/konstantinosKokos/Lassy-TLG-Extraction/tree/master) (follow the instructions there).
The data are represented as a list of tuples, the first element containing a graph corresponding to the dependency
parse including type assignments for words, and the second element containing a proofnet, encoded as a bijection between
atomic types.

---
 
If you would like to access the full dataset, require a representation format not available in the repo, or encounter any issues, do not hesitate to get in touch.
