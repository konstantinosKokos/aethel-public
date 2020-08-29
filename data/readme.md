## data/
The directory contains different views of the dataset.
 
##### Currently available presentations
 * **natural deduction** (`data/natural_deduction/`) 
 * **sequent calculus** (`data/sequent_calculus/`) 
 * **dependency-decorated λ-terms** (`data/lambda_terms/`)

The first two presentations are conversions of the extracted data, as produced by 
[LinearOne](https://github.com/RichardMoot/LinearOne). 
They come in the form of xml files, with each file containing a single data sample/theorem.

The last one is the yield of traversal algorithm applied directly on the extracted proof nets.
It comes in the form of a single file per dataset split containing many samples. 

---

Note that a small portion of samples containing disjoint multi-word units are not included in the 
natural deduction and sequent style folders due to incompatibilities with the conversion tool.

