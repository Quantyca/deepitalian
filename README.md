# Italian Language Model for Fast.ai ULMFiT
This is the repo for the pre-trained Italian Language Model for fast.ai (see ULMFiT models at http://nlp.fast.ai/) , based on Italian wikipedia dump.

Resources available:
* Two parametric workbooks (tested with fastai v1 rev. 51) to tokenize the dataset and to train the model (in this repo).
* The basic CSVs with the data derived from wikipedia and created using the official fast.ai process with 400M tokens (https://github.com/fastai/fastai/tree/master/courses/dl2/imdb_scripts step 0): [train csv](https://drive.google.com/file/d/1Eoipisg2-nGewt-96BJVY8SPweTTf_yG/view?usp=sharing) and [val csv](https://drive.google.com/file/d/1gG4FlqOYs0PmYKMK4aHlPnPyjJWW_Fr0/view?usp=sharing)
* The merged CSV for language model training: [merged csv](https://drive.google.com/file/d/1pzTOT1trQLfj0F1fabC-dsDfwQwLKmeh/view?usp=sharing)
* A serialized loader with a corpus of 100M tokens and a vocab size of 60.000 words (we downsample the above file using  `.use_partial_data(p_in_partial_data_pct, seed=42)` with a pct of .25 in the datablock api: [corpus](https://drive.google.com/file/d/1e9hLetLb64pB6eIzgpX7O0-twJhrMWrV/view?usp=sharing)
* The corresponding itos file (to be used on step 2 and 3 of ULMFiT approach): [itos](https://drive.google.com/file/d/1-HubZtd6oY62S1Z5oR1_aLm4dFoNwTpq/view?usp=sharing)
* The trained model (47.5 perplexity): [model](https://drive.google.com/file/d/18IGx8RHHKUsIC7xQ-1d_2ZzHRr6_B4hO/view?usp=sharing). With this model we achieved 96.5% accuracy on classifications of sentiment in restaurant reviews.

Work is heavily inspired by https://github.com/tchambon/deepfrench and made with :heart: by Quantyca Analytics Team
