# wikiwords
Parsing wikipedia into usable form for NLP / skipgram training

Usable Form: Paragraphs as a unit of data that will be storeed in a database. Training module will pull paragraphs to be broken down into sentences which define the groups for the skipgram. Goal is extract all large paragraphs of text by removing all formatting, editing comments, tables, charts, and lists. Any information that cant be interpreted as text will also be removed (links, other languages).


Processing Steps:

  - Remove all subsections for sources and references
    From the first 100k lines of the xml the most common subsections were
       23 ===citations===
       24 ===1601–1900===
       24 ===1901–present===
       24 ===pre-1600===
       34 ==bibliography==
       39 ==etymology==
       71 ==notes==
       73 ==history==
       89 ==furtherreading==
      175 ==seealso==
      199 ==externallinks==
      219 ==references==


  - Remove all editor comments and notations

  - Remove xml headers and footers. Preserving the title as an additional data field

  - Preserve quotes by extracting them from formatting

  - Remove inline citations

  - Extract information from curly and square brackets

  - Remove lists/charts/tables/info boxes

  - Remove all file names and links

  - Convert all xml control characters into regular text form

  - LaTeX
