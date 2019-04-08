#Test_sample  

Testing multiple machine learning NLP models on conduct risk related communications within a financial services domain.
Models vary from neural network nlp models to more traditional TF-IDF based models.  

There were multiple different upstream conversions of text-to-numeric. Some models used word embedding vectors with minimal preprocessing, others followed a more traditional atomic based bag of words approach with typical preprocessing for that format e.g lower casing, lemmatization and punctuation plus stopword removal.

Downstream there was also a lot of variance in the models. Neural net structures varied considerably and for one of the TF-IDF models hyperparameter optimization was undertaken via a five fold cross val grid search.

In the real world models need to detect target content that might represent just a tiny fraction of the total electronic communications passing through a server any any given point in time. 

In this test classes are deliberately balanced. Tokenizers are trained on as much data as is available in the test. This will aid the models ahead of classification task but not reflect the real world possibility of out-of-vocab words being shown to the models during testing. F1 scores are compared and the goal is to find the most efficient, least complex and least computationally expensive model.  

Footnote:
No novelty detection algorithms. No pretained vectors imported. Balanced classes. Shallow nets. Left-to-right LSTM's.
