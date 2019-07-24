# Mueller Report and Analytics

[Damir Cavar], July 2019

Created: 04/18/2019

Last Change: 07/24/2019


Please cite this repo and acknowledge the work by the team. Like it, if you use it, etc. Let us know what to correct by raising an issue.


This is the entire Mueller Report converted to raw ASCII/Unicode text format.


This repo contains the data and results of our NLP-based Mueller Report Analysis, Knowledge Graphs, entitites, relations.

Results will be published incrementaly as we identify them.

This is a collaborative effort between:

- [The NLP-Lab](https://nlp-lab.org/) (Damir Cavar's Research Lab at Indiana University in Bloomington)
- [Semiring Inc.]


Numerous volunteers have helped preparing this cleaned up and annotated text collection:

- [Damir Cavar]
- Stefan Geissler
- Maanvitha Gongala
- Joshua Herring
- Mureli Kammili
- Chaitanya Patil
- S Panicker
- Umang Mehta

and many other.


## Log

### 04/18/2019

In the pre-rocessing phase I prepared the two Mueller report volumes to be able to run corpus analyses on them. This is what we did after the document was published on the 18th of April.

We converted the PDF to an editable raw text format:

- The raw text has been generated in two ways:
  - We used various free and commercial OCR systems to process the PDF and export the raw Unicode encoded text.
- A paragraph is one line of text preceded and followed by an empty line.
- Footnotes are tagged in the text and a footnote text is a paragraph that starts with a footnote tag <FN#>, where # is an integer as used in the original document. A footnote is a line (paragraph) that starts with the <FN#> mark. A reference to a footnote will be in running text and not starting a line.
- Section titles are paragrpahs that start with a <SECTION> tag.
- Redacted portions of text are tagged with a <REDACTED> tag.
- We removed words and characters that were surrounded by square brackets (e.g. [T]he...).

We annotated the footnotes in the text (a lot of footnotes) using a tag in the text:

  <FN#>

where # is the number of the footnote, eg. <FN1011>. The footnote text itself is a paragraph that starts with a <FN...> tag. We left the footnotes in the text where they appeared, but we merged broken paragraphs to be continuous, if a footnote appeared within a paragraph.

The <SECTION> and <FN#> tags allow us to filter these paragraphs when running analyses over the corpus.



[Damir Cavar]: http://damir.cavar.me/ "Damir Cavar"
[Semiring Inc.]: https://semiring.com "Semiring Inc."
[The NLP-Lab]: https://nlp-lab.org/ "The NLP-Lab"
