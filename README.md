# LSC-in-Polish-using-XL-Lexeme

This is a repository for storing the code used for LSC detection task in Polish language.

**CreateLwsfListC1.ipynb** and **CreateLwsfListC2.ipynb** scan through the *ann_morphosyntax.xml* files and create a list of tuples: (lemma, word form, segment number, file path) for C1 and C2, respectively.

**CreateLwsfDiction.ipynb** creates a dictionary with lemmas as keys and a list of tuples of (word form, segment number, file path) as values.

