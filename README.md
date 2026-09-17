# An Unsupervised Natural Language Processing Pipeline for Assessing Referral Appropriateness
Code for the paper "An Unsupervised Natural Language Processing Pipeline for Assessing Referral Appropriateness" https://arxiv.org/abs/2501.14701 

`Referral_Appropriateness_NLP.ipynb` contains the full pipeline, organized into sections that
mirror the paper and its supplementary material:
1. Setup
2. Data loading and description
3. Pre-processing (cleaning, abbreviation expansion, typo correction)
4. Manual annotations and guideline-based appropriateness mapping
5. Text embedding (UmBERTo-E3C)
6. Clustering, summarisation and guideline mapping
7. Evaluation methodology
8. Hyperparameter selection and comparative baselines (TF-IDF, Word2Vec, UmBERTo-Base, LDA, direct embedding match)
9. Results: validation against manual annotations
10. Population-scale analysis
11. Regional, physician and temporal stratification
12. Embedding space visualisation

### Running it
The notebook is not runnable end-to-end out of the box: it needs the referral datasets, the
manual annotations, the abbreviation and guideline-item tables, and the UmBERTo-E3C checkpoint,
none of which are redistributed here (see below). Section 1.2 ("Required external resources")
lists every one of these with what it is and where it comes from, and centralizes them in a
single `RESOURCES` dict — fill that in with your own copies and the rest of the notebook runs
as is, on CPU or GPU.

The data that support the findings of the study are available from Regione Lombardia but restrictions apply to the availability of these data, which were used under license for the current study, and so are not publicly available.
