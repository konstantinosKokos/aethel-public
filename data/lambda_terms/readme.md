## data/lambda_terms/

This directory contains terms of the linear lambda-calculus with dependency and type annotations for each of the
72,192 samples split into three files for the training, development and test splits.

---  

## *.lam
The grammar of the file is:

 `LMD ::= LMD | LMD "\n" SAMPLE`
 
 where 
 
 `SAMPLE ::= SAMPLE_ID ":-\n\t" WORD_SEQUENCE "\n\t" TERM`
 
 where 
 
 `SAMPLE_ID` a unique identifier specifying the filename of the original LassySmall file postfixed by a mark `_i` to 
 determine which subpart of the original file is analyzed (in the case of a split during processing)
 
 `WORD_SEQUENCE ::= WORD_SEQUENCE, WORD` a list of comma-separated words (or phrases, in the case of multi-word 
 expressions) corresponding to the analyzed sentence/phrase
 
 and
 
 `TERM` the derived lambda term.

 ---
 
 The `TERM` grammar:
 
 A term is an expression `w_i::t` where `w_i` denotes the `i`-th word of the sentence and `t` denotes the type assigned 
 to that word (implication-only intuitionistic linear), or `x_j` for a hypothetical lambda-variable.
 
 If `t1` is a term and `t2` is a term, then `(t1^d t2)` and `(t1 t2^d)` are also terms, denoting the _application_ of
 term `t1` to `t2`, where `d` assigns a dependency role to either the functor or its argument.

 Decorations `d` apply to the argument `t2` if it is a phrasal _complement_ to phrasal head `t1`,
 or to the functor `t1` if it is a dependant of phrasal head `t2`.
 Phrasal heads assume no dependency role.
 
 Finally, if `t` is a term, `λx_j.t` is also a term denoting the λ-abstraction over `x_j` of `t`.
 
 Linearity constraints apply as usual (no vacuous abstractions, no copying). 
 
 
