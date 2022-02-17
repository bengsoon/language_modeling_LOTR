# Language Modeling for the Lord of The Rings trilogy corpus
Language Models trained with LSTM using the Lord of The Rings trilogy corpus.

### Character Level modeling
- Two methods were explored:
    1. **`sparse_categorical_crossentropy` model** where the input sentences were vectorized using `TextVectorization` from Keras, yielding input shape of (`MAX_SEQ_LEN`,) where `MAX_SEQ_LEN` is the maximum sequence of the input sentences (Tx). Each individual sequence in the `MAX_SEQ_LEN` would correspond to the vectorized integer number for the corresponding `N_UNIQUE_CHARS` of the corpus (where `N_UNIQUE_CHARS` is the unique characters found in the corpus)
    
    2. **`categorical_crossentropy` model or One-Hot Encoding model** where the input sentences were vectorized into one-hot encoded arrays, yielding input shape of (`MAX_SEQ_LEN`, `N_UNIQUE_CHARS`), where `MAX_SEQ_LEN` is the maximum sequence of the input sentences (Tx). For each of the individual sequence in the `MAX_SEQ_LEN` there would be corresponding one-hot-encoded vector of length `N_UNIQUE_CHARS` where N_UNIQUE_CHARS` is the unique characters found in the corpus.
