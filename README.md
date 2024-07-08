# LSC-in-Polish-using-XL-Lexeme

This is a repository for storing the code used for Lexcial Semantic Change (LSC) detection task in the Polish language.

**CreateLwsfListC1.ipynb** and **CreateLwsfListC2.ipynb** scan through the *ann_morphosyntax.xml* files and create a list of tuples: (lemma, word form, segment number, file path) for C1 and C2, respectively.

**CreateLwsfDiction.ipynb** creates a dictionary with lemmas as keys and a list of tuples of (word form, segment number, file path) as values.

**CreateClearedList.ipynb** creates a list of lemmas to be examined by the model. This is done by cutting 2000 most common lemmas in both time periods and removing all lemmas with less than 25 occurences in either of the time periods.

**CreateRandomSentences** chooses 25 random sentences for each of the saved lemmas.

**CreateJSONLFiles.ipynb** searches through *text_structure.xml* files to find the randomly chosen sentences. For each lemma, it creates a JSONL file with dictionaries containing the sentence, the first index of the target word, the last index of the target word and the lemma.

**model.ipynb** iterates through the JSONL files and passes them through XL-Lexeme, creating an embedding matrix for each lemma.

**CreatePRT.ipynb** passes the lemma matrices through the PRT algorithm, creating single vectors for each lemma in both time periods.

**CalculateCosineDistance.ipynb** calculates the cosine distances between the vectors made by PRT.

**CreateAPD.ipynb** passess the lemma matrices through the APD algorithm.
