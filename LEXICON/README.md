# Lexicon

The files in this folder provide various views of the lexicon and relevant utilities.  

## WORD_LEXICON.lex
WORD_LEXICON.lex contains a mapping from word and part-of-speech tag pairs into sequences of pairs of types and their 
corresponding counts.
The keys (words and pos tags) are arranged in alphanumeric order, whereas their values (types and counts) are arranged 
by count (descending).

The grammar of the file is:

 `LEX ::= LINE | LINE "\n" LEX`
 
 where 
 
 `LINE ::= TEXT "\t" POS "\t" TYPE_SEQUENCE`
 
 where 
 
 `TEXT` a string representing either a word or (in the case of multi-word phrases) a contiguous phrase,
 
 `POS` a string representing an element of the set of POS-tags employed by LASSY
 
 and 
 
 `TYPE_SEQUENCE ::= TYPE_COUNT | TYPE_COUNT " | " TYPE_SEQUENCE`,
 
 with 
 
 `TYPE_COUNT ::= TYPE " #= " COUNT ` 
 
 where
 
 `TYPE` the string representation of a dependency-decorated linear type
 
 and 
 
 `COUNT` an integer representing the number of occurrences of that particular type under the context of the 
 corresponding word and pos tag.
 
 
 ## TYPE_FREQUENCIES.freq
 TYPE_FREQUENCIES.freq contains a mapping from types to integers, counting the sum of occurrences of each unique type 
 within the corpus.
 
 The grammar of the file is:
 
  `FREQ ::= LINE | LINE "\n" FREQ`
  
  where 
  
  `LINE ::= TYPE "\t" COUNT`,
  
  with `TYPE` being the string representation of a dependency-decorated linear type,
  
  and `COUNT` the integer representing its cumulative occurrence count.
  
  
 ## POS_FREQUENCIES.freq
 Ditto, for the part of speech tags present in the corpus.
 
 
  `FREQ ::= LINE | LINE "\n" FREQ`
  
  where 
  
  `LINE ::= POS "\t" COUNT`,
  
  with `POS` being the part-of-speech tag,
  
  and `COUNT` the integer representing its cumulative occurrence count.
  