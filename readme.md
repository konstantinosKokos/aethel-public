# aethel
Repository containing the **full** ÆThel dataset, as described in the 
paper "ÆThel: Automatically Extracted Typelogical Derivations for Dutch" 
([link](http://www.lrec-conf.org/proceedings/lrec2020/pdf/2020.lrec-1.647.pdf)).


The repository contains 72,192 linear logic theorems, each corresponding to a parse of a written Dutch sentence 
or phrase.
The dataset is split into training, development and test sets, enumerating 57,753, 7,219 and 7,220 theorems
respectively.
Included in the `lexicon` directory are also files containing lexical type assignments for 81,730 words, as 
obtained by dataset aggregation. 

---

#### Binary Version
You can download a binary version of the data in the form of a python pickle from 
[here](https://surfdrive.surf.nl/files/index.php/s/2ZnYupSI7nwkFrZ).
The pickle contains three lists of analyses, corresponding to the training, development and test subsets.
Analyses are provided in the form of tuples `(DAG, PN)`, where `DAG` a dependency graph originating from the 
original Lassy annotation, with a type assigned to each lexical/phrasal node, and `PN` the associated type-logical
derivation in the form of a proof net, represented as a bijection between atomic types.
To be able to access the data, you will need to clone the 
[extraction code](https://github.com/konstantinosKokos/Lassy-TLG-Extraction/tree/master) 
(basic instructions can be found there).


---
 
If you require a representation format not available in the repo, encounter any issues or find any inconsistencies,
 do not hesitate to [get in touch](mailto:k.kogkalidis@uu.nl).
