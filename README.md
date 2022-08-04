# Topic-Modelling---Gensim-LDA
Modelling Topics for the 20Newsgroups dataset using Gensim's LDA model


For this project, I have used Gensim's LDA model for topic modelling on the 20Newsgroups Dataset

The purpose of this assignment is to demonstrate training an LDA model and obtaining good results.

In the notebook available at <https://github.com/sandeepsethu/Topic-Modelling---Gensim-LDA/blob/main/Topic%20Modelling%20Assignment(1).ipynb> I have:

    Loaded the data.
    Pre-processed the data.
    Transformed documents to a vectorized form.
    Found the optimal topic number.
    Trained an LDA model.
    Visualized the results.

Data used -The 20Newsgroups Dataset

I have made use of the 20-Newsgroups dataset for this topic modelling assignment. This version of the dataset contains about 11,000 newsgroups posts from 20 different topics and is available in the json format.

The link for the dataset was obtained from https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/. The code for reading the json file was also borrowed from the same website.

Qualitatively evaluating the output of an LDA model is challenging and can require you to understand the subject matter of your corpus (depending on your goal with the model). I believe that with the 20Newsgroups dataset with its vastly different topics, it would be easier to understand the topics learnt by the LDA model and to better evaluate its "accuracy".

.. Important:: The corpus contains 11314 documents, and not particularly long ones.


![image](https://user-images.githubusercontent.com/29595951/182833388-b99fa56b-a1ff-45c8-828b-d6fb9f3bb5a8.png)



As can be seen from the image, the ideal topic number was found to be 20.

Using the same, the LDA model was trained and keywords found from which the topics were examined.


Refer to the diagram below for a quick look at the different topics identified:


![Untitled Diagram drawio](https://user-images.githubusercontent.com/29595951/182833730-e12f4ae3-ab42-47fa-bfa7-5d9b3d0fc287.png)


A topic coherance score of 0.5618 was obtained with this model.


The dataset we chose has some overlap with topics, such as christianity, misc religion and atheism which has not been accurately captured by the model.

Similarly topics like mac hardware, pc hardware, graphics, windows misc and windows x have not been properly demarcated by the model on the basis of the keywords.

There were also some topics with incoherant/random keywords which could not be interpreted as any topic. 

On the other hand, we can also see that there are some topics which were not part of the original dataset and are instead subtopics which has been captured by the LDA model.

With more parameter tuning and given more time, I could possibly fine tune the model to better capture these cases and have more coherant topics.

Things to experiment with to further examine the model:
-------------------------

* When building the dictionary, change ``no_above`` and ``no_below`` parameters in ``filter_extremes`` method.
* Add trigrams and see if it makes a difference.
* Remove bigrams and see if it makes a difference.
* Do not remove stopwords and see if it makes a difference
* Try visualizing with fewer topics to see if that helps to reduce the number of incoherent topics even with the possibility of merging two or more topics into one.
* Try different chunksizes, alpha, eta, values etc while training the model.




References
----------

1. LDA Tutorial. https://radimrehurek.com/gensim/auto_examples/tutorials/run_lda.html
2. Gensim Topic Modelling. https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/



