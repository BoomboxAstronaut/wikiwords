# wikiwords
Parsing wikipedia into usable form for NLP / skipgram training

Usable Form: Paragraphs as a unit of data that will be storeed in a database. Training module will pull paragraphs to be broken down into sentences which define the groups for the skipgram. Goal is extract all large paragraphs of text by removing all formatting, editing comments, tables, charts, and lists. Any information that cant be interpreted as text will also be removed (links, other languages).


Processing Steps:

  - Remove all subsections for sources and references

  - Remove all editor comments and notations

  - Remove xml headers and footers. Preserving the title as an additional data field

  - Preserve quotes by extracting them from formatting

  - Remove inline citations

  - Extract information from curly and square brackets

  - Remove lists/charts/tables/info boxes

  - Remove all file names and links

  - Convert all xml control characters into regular text form

  - LaTeX
