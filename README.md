# Retail Data Analysis

This project shows how make decisions using limited history. Retail data is one of them. Holidays and select major events which come once a year changes the way people shop. To keep up with the customer needs, retail store also need to make some decision. The aim of this project is to visualize the retail data and learn from the data. Systematically present visuals of the data by plotting various graphs and chart which is useful for the store to understand their past product trends and make decision based on that knowledge.


The Stanford Question Answering Dataset `SQuAD2.0` is used to train the model. <br />
download link : https://rajpurkar.github.io/SQuAD-explorer

`glove.6B.100d` is Stanford's unsupervised learning algorithm to get word embeddings is used for obtaining vector representations for words. <br />
download link : https://nlp.stanford.edu/projects/glove/

## Walkthrough

>The code starts with preprocessing raw data.

>It takes the preprocessed data and tokenizes. Further, it pads the input to make a standard size for all the input data.

>`glove.6B.100d` word embeddings are loaded and applied to the padded and tokenized data to get vector representation.

>Model architecture is build using encoder and decoder system. In encoder, two LSTM layers; one for the context and other for it's corresponding question are created. Further, the output encodings from both the LSTM layers are concatenated and passed to the decoder. Decoder consists of LSTM layers which outputs the encoding with fixed output shape. Finally, a dense layer with `Softwmax` activation function is used to output the predictions.

>Model is trained with a batch size of 64, 5 epochs and validation split of 0.3

