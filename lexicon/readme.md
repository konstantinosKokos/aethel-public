# Lexicon

The files in this folder provide various views of the lexicon and relevant utilities.

---  

## word_lexicon.lex
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
 
 where `TYPE` the string representation of a dependency-decorated linear type
 
 and `COUNT` an integer representing the number of occurrences of that particular type under the context of the 
 corresponding word and pos tag.
 
 
## type_lexicon.lex
 TYPE_LEXICON.lex contains a mapping from types to sequences of pairs of words and their corresponding counts. 
 The keys are (types) are arranged by their cumulative occurrence counts (descending), and the values (word and count 
 pairs) are arranged by counts (descending).
 
 The grammar of the file is:

 `LEX ::= LINE | LINE "\n" LEX`
 
 where 
 
 `LINE ::= TYPE "\t" WORD_SEQUENCE`
 
 where 
 
 `TYPE` the string representation of a dependency-decorated linear type,
 
  and 
  
 `WORD_SEQUENCE ::= WORD_COUNT | WORD_COUNT " | " WORD_SEQUENCE`
 
 with 
 
 `WORD_COUNT ::= TEXT " #= " COUNT ` 
 
 where `TEXT` a string representing either a word or (in the case of multi-word phrases) a contiguous phrase,
 
 and `COUNT` an integer representing the number of occurrences of that particular word under the context of the 
 corresponding type.
    
 
## word_map.map
 WORD_MAP.map contains a mapping from tuples of words, part-of-speech tags and lemmata to pairs of types and 
 their respective occurrence counts. 
 Unlike the *.lex files, this mapping is non-unique (i.e. there are multiple assignments to each tuple of the domain).
 
 The grammar of the file is:
 
 `MAP := LINE | LINE "\n" MAP`
 
 where 
 
 `LINE := TEXT "\t" POS "\t" LEMMA "\t" TYPE " #= " COUNT`
 
 with `TEXT` being a corpus word or multi-word phrase,
 
 `POS` the string representation of an element of the POS-tags in LASSY,
 
 `LEMMA` either the lemma information provided by LASSY (in case of a word) or the original text (in case of a 
 multi-word phrase),
 
 `TYPE` the string representation of a dependency-decorated linear type,
 
 and `COUNT` the occurrence count of that type.
 
 
## type_frequencies.freq
 TYPE_FREQUENCIES.freq contains a mapping from types to integers, counting the sum of occurrences of each unique type 
 within the corpus.
 
 The grammar of the file is:
 
  `FREQ ::= LINE | LINE "\n" FREQ`
  
  where 
  
  `LINE ::= TYPE "\t" COUNT`,
  
  with `TYPE` being the string representation of a dependency-decorated linear type,
  
  and `COUNT` the integer representing its cumulative occurrence count.
  
  
## pos_frequencies.freq
 Ditto, for the part of speech tags present in the corpus.
 
 
  `FREQ ::= LINE | LINE "\n" FREQ`
  
  where 
  
  `LINE ::= POS "\t" COUNT`,
  
  with `POS` being the part-of-speech tag,
  
  and `COUNT` the integer representing its cumulative occurrence count.
  