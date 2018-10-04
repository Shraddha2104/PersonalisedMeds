### Overview
The host, Memorial Sloan Kettering Cancer Center (MSKCC), has been maintaining the database OncoKB for the purpose of knowledge sharing of mutation effects among oncologist. Currently this interpretation of genetic mutations is being done manually. This is a very time-consuming task where a clinical pathologist has to manually review and classify every single genetic mutation based on evidence from text-based clinical literature. And due to my combined interest in biology and data science, I am interested in using my expertise to develop a machine learning algorithm that, using an expert-annotated knowledge base as a baseline, automatically classifies genetic variations.

### Software and Libararies
- [Python 2.7](https://www.python.org/download/releases/2.7/)
- [NumPy](http://www.numpy.org/)
- [pandas](http://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [matplotlib](http://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org)
- [Gensim (word2vec)](https://radimrehurek.com/gensim/)
- [XGBOOST](https://xgboost.readthedocs.io/en/latest/)


**Note:**
- The mentioned kaggle competition is [here](https://www.kaggle.com/c/msk-redefining-cancer-treatment).



### Project Overview

A lot has been said during the past several years about how precision
medicine and, more concretely, how genetic testing is going to disrupt
the way diseases like cancer are treated. But this is only partially
happening due to the huge amount of manual work still required. Once
sequenced, a cancer tumor can have thousands of genetic mutations. But
the challenge is distinguishing the mutations that contribute to tumor
growth (drivers) from the neutral mutations (passengers). The host,
Memorial Sloan Kettering Cancer Center (MSKCC) has been maintaining the database OncoKB \[1\] for the purpose of
knowledge sharing of mutation effects among oncologist. Currently this
interpretation of genetic mutations is being done manually. This is a
very time-consuming task where a clinical pathologist has to manually
review and classify every single genetic mutation based on evidence from
text-based clinical literature.  Therefore, the task is to develop a
Machine Learning algorithm that, using an expert-annotated knowledge
base as a baseline, automatically classifies genetic variations.


**Details of input datasets: **

-   training\_variants - a comma separated file containing the
    description of the genetic mutations used for training. Fields
    are ID (the id of the row used to link the mutation to the clinical
    evidence), Gene (the gene where this genetic mutation is
    located), Variation (the aminoacid change for this
    mutations), Class (1-9 the class this genetic mutation has been
    classified on)

-   training\_text - a double pipe (||) delimited file that contains the
    clinical evidence (text) used to classify genetic mutations. Fields
    are ID (the id of the row used to link the clinical evidence to the
    genetic mutation), Text (the clinical evidence used to classify the
    genetic mutation)

-   test\_variants - a comma separated file containing the description
    of the genetic mutations used for training. Fields are ID (the id of
    the row used to link the mutation to the clinical
    evidence), Gene (the gene where this genetic mutation is
    located), Variation (the aminoacid change for this mutations)

-   test\_text - a double pipe (||) delimited file that contains the
    clinical evidence (text) used to classify genetic mutations. Fields
    are ID (the id of the row used to link the clinical evidence to the
    genetic mutation), Text (the clinical evidence used to classify the
    genetic mutation)
