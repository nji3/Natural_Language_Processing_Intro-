# Movie Genres

## Data Preparation

A sample of 2500 movies is selected from the original dataset. It seems that each movie could have more than one genres. We would want to check out the genres we have and reorganize them to be the target variable we could use for the prediction.

There are two ways  to select the genres we want to use for the prediction task. The first one is to check the correlation of the occurency among the genres assigned for these movies. And then, we could combine the genres with high occurence correlations into a new genre. However, here to save the time, I would just use the Top genres provided here for the prediction task.

We could take a look at a heat map for the occurence of each genres (Some genres would appear together for one movie).

## Text to Numerical Vector

Now it is the time to modify the predict variable, whcih is the summary of the movie. The summary of the movie contains short sentences. We need to transfer these sentences into numerical vectors of wrods.

To make the texts usable and meaningful, we need to do three steps. The first step is to transfer all the texts into a frequency matrix. Here I just use the naive way, which is the bag of words tech that count the appearing fequency for each word in all the summary sentences. Use the package 'CountVectorizer', we could easily do that.

However, not every word is meaningful. So the second step is that we would want get rid of the words that appear too often in all the sentences and the words that appear too seldom (Too unique for each movie, might not be general when we try to train a prediction model).

The third step is to give a weight indicating the importance of the word. For the meaningful words, the word appears too often would still be less important, such as 'about', 'for'. They would have a smaller weight. But in the low-frequent words, the word appears more times would be relatively important (indicate some features). We would simply apply 'TfidfTransformer' package to help us assign all the weightage.

<div align="center">
        <img src="https://github.com/nji3/Natural_Language_Processing_Intro-/blob/master/Movie%20Genres/readme_img/genre_corr.png" width="400px"</img> 
</div>

## Statistics Model Training

### Multinomial Naive Bayes

### SVM

### Boosting

## Deep Nueral Network Model

### Simple Fully-Connect NN

### Pretrained Model from the TensorHub
