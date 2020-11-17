# ChemTextMining
## Short description of repository
##### This repository contains code and additional resources for experimenting on disease entities extraction using conditional random fields. Structure is as follows:<br>
0. webmd_corpus.json is a full corpus.
1. classification_pipe.py - entry point of program.
2. vocabularies - directory with used vocabularies in txt format, each line contains one vocabulary entity.
3. clustered words - directory with words clustered using brown clustering algorithm.
4. corpus_json - directory with datasets used in experiments.
5. word2vec - directory with word embeddings
6. remaining is utility code

## Usage:
0. How to load vectors(to use them in your application):

            w2v = KeyedVectors.load_word2vec_model('patht/to/vectors', binary=True)                       
1. Install all the requirements.

            pip install -r requirements.txt
   Also perl is need to be installed

2. Specify in "features" dictionary current token features from list of available features. Also it's necessary to define context size by setting k_prev(tokens to look before) and k_next(tokens to look forward) and features for each context token(in prev_features and next_features).
3. Run code:

          python classificaton_pipe.py

4. Output is in format:

        ...
        Average exact score:
          precision	recall	fscore

        Average weak score:
          precision	recall	fscore


#### Note: To use different word embedding vectors need to specify it in crf/features.py in load_w2v_model function.
#### Citing:
#####   Sh, Miftahutdinov Z., Tutubalina EV, and Tropsha AE. "Identifying disease-related expressions in reviews using conditional random fields." Computational Linguistics and Intellectual Technologies (2017): 155-166.
  http://www.dialog-21.ru/media/3932/miftahutdinovzshetal.pdf
##### BibTex:
    @inproceedings{miftahutdinov2017,
                  title={Identifying Disease-related Expressions in Reviews using Conditional Random Fields},
                  author={Miftahutdinov, Zulfat and Tutubalina, Elena and Tropsha, Alexander},
                  booktitle={Computational Linguistics and Intellectual Technologies: Proceedings of International Conference Dialogue},
                  volume={1},
                  pages={155-166},
                  year={2017}
    }
##### Tutubalina, E. V., Miftahutdinov, Z. S., Nugmanov, R. I., Madzhidov, T. I., Nikolenko, S. I., Alimova, I. S., & Tropsha, A. E. (2017). Using semantic analysis of texts for the identification of drugs with similar therapeutic effects. Russian Chemical Bulletin, 66(11), 2180-2189.
   [link to paper](https://www.researchgate.net/profile/Elena_Tutubalina/publication/323751823_Using_semantic_analysis_of_texts_for_the_identification_of_drugs_with_similar_therapeutic_effects/links/5bf7cfc3299bf1a0202cbc1f/Using-semantic-analysis-of-texts-for-the-identification-of-drugs-with-similar-therapeutic-effects.pdf)
##### BibTex
    @article{tutubalina2017using,
            title={Using semantic analysis of texts for the identification of drugs with similar therapeutic effects},
            author={Tutubalina, EV and Miftahutdinov, Z Sh and Nugmanov, RI and Madzhidov, TI and Nikolenko, SI and Alimova, IS and Tropsha, AE},
            journal={Russian Chemical Bulletin},
            volume={66},
            number={11},
            pages={2180--2189},
            year={2017},
            publisher={Springer}}
