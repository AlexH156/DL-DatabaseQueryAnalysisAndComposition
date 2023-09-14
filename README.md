# Deep Learning For Database Query Analysis And Composition
GitHub repository for the code of my Master Thesis 'Deep Learning for Database Query Analysis and Composition' at the University Münster in Information Systems. The thesis explores the capabilities of deeper Convolutional Neural Networks (CNNs) for the task of prediction the runtime and cardinality of database queries. It continues the exploration of [Zolaktaf et al. (2020)](https://dl.acm.org/doi/10.1145/3318464.3380602) who evaluated that a shallow, character-level CNN performed best of the tested models. [Conneau et al. (2016)](https://arxiv.org/abs/1606.01781) found deeper CNNs do perform better on the related task of text classification than shallow CNNs. Therefore, the thesis explores the idea of very deep CNN for predicting runtime and cardinality.

## Files
The dataset is [SDSS](https://www.sdss.org/). Preprocessing.ipynb encompasses all steps taken to preprocess the data, such as data cleaning as well as reducing the load of 150 million obtained queries to around 240 thousand. hyperparameter-tuning.ipynb explored the best hyperparameters for the models with GreadSearch. baseline.ipynb evaluated two baseline models Median and TFIDF for the task of predicting runtime and cardinality. fit.ipynb is used to train and evaluate all CNNs.

All trained models are contained in the models folder, splitted by runtime, cardinality and full prediction. All models were trained three times in total. Once for only runtime, once for only cardinality and once for a combined prediction of both.

The used dataset is contained in the data folder, splitted by training and test data. 
