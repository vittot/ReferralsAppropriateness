# An Unsupervised Natural Language Processing Pipeline for Assessing Referral Appropriateness

![arXiv](https://img.shields.io/badge/arXiv-2501.14701-b31b1b.svg)
![Python](https://img.shields.io/badge/python-3.10%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Code for the paper "An Unsupervised Natural Language Processing Pipeline for Assessing Referral Appropriateness" https://arxiv.org/abs/2501.14701 

`Referral_Appropriateness_NLP.ipynb` contains the full pipeline:
1. Setup
2. Data loading and description
3. Pre-processing (cleaning, abbreviation expansion, typo correction)
4. Guideline-based appropriateness mapping
5. Text embedding (UmBERTo-E3C)
6. Clustering, summarisation and guideline mapping
7. Evaluation methodology
8. Hyperparameter selection and baselines comparison (TF-IDF, Word2Vec, UmBERTo-Base, LDA, direct embedding match)
9. Results: performance against the annotated validation set, pre-processing ablation, and a stratified bias check by physician type and year
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

Python dependencies are listed in `requirements.txt` (`pip install -r requirements.txt`).

The data that support the findings of the study were provided from Regione Lombardia but restrictions apply to the availability of these data, which were used under license for the current study, and so are not publicly available.

### How to cite
```bibtex
@article{torri2025referral,
  title={An Unsupervised Natural Language Processing Pipeline for Assessing Referral Appropriateness},
  author={Torri, Vittorio and Bottelli, Annamaria and Ercolanoni, Michele and Leoni, Olivia and Ieva, Francesca},
  journal={arXiv preprint arXiv:2501.14701},
  year={2025}
}
```
