# Import necessary library -- pandas to read file
import pandas as pd

#Read data from tsv file
def load_tsvdata(tsvFileName):

#Read data from csv file
def load_csvdata(csvFileName):

#Drop useless columns in FEATURES
def preprocess_features(featureStream):
    
#Drop useless columns in LABLES  
def preprocess_labels(labelStream):

Then load 5 files and name variables, drop useless columns

# Import necessary library -- TfidfVectorizer
from sklearn.feature_extraction.text import TfidfVectorizer


""" 
funtion: finish TFIDF process
input: column: name of column. eg: 'title', 'tag'
       dfmin: int or float. Ignore terms that have a document frequency strictly lower than the given threshold
                            If float in range of [0.0, 1.0], the parameter represents a proportion of documents. 
       dfmax: int or float. similar with dfmin.
return: TFIDF for train, valid and test. The features must process same opeartion 

"""
def TFIDF(column, dfmin = 1, dfmax = 0.5):

#merge the original data, TFIDF for title and TFIDF for tag to train.
def final_input(data, title_TFIDF, tag_TFIDF):


#normaliztion each columns.
def normalization():

get the TFIDF results for "title" and "tag"
merge and normalization

this part define 7 models. I tried all of them. But I only detailed writed Naive Bayes and SVM(SVC) in report.






==============================================================================================
==============================================================================================
This file describes the data provided as part of 
COMP90049: Introduction to Machine Learning
Project 2: Romance or Thriller? Movie Genre Prediction from Audio, Visual, and Text Features!

The features and class labels are derived from the following published data sets

Deldjoo,  Yashar  and  Constantin,  Mihai  Gabriel  and  Schedl,  Markus  and  Ionescu,  Bogdan 
andCremonesi, Paolo. MMTF-14K: A Multifaceted Movie Trailer Feature Dataset for Recommendation and 
Retrieval. Proceedings of the 9th ACM Multimedia Systems Conference, MMSys 2018,Amsterdam, 
The Netherlands, June 12-15, 2018F. 

Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM 
Transactions on Interactive Intelligent Systems (TiiS) 5, 4, Article 19 (December 2015
==============================================================================================
==============================================================================================

======================
Data splits and format
======================

The data set consists of audio, visual and metadata features for 5840 movies, as well as their
genre labels. The movies are split into a training set (5241 movies), development set (299 movies)
and test set (298 movies).

For each data split, we provide a features.tsv file, labels_single.tsv file. Each file is in tsv format 
(tab-separated values). 

========
Features
========

The feature files (train_features.tsv, valid_features.tsv and test_features.tsv) contains the 
following columns:

* movieID: unique identifier for each movie (to be used for mapping movies to their labels)
* movieTitle: title of the movie. Type: text.
* year: The year in which the movie was released. Type: integer.
* Tag: A comma-separated list of tags assigned to the movie by human annotators. Type: text / categorical.
* avg1 ... avg107: 107 columns containing pre-computed visual features of the movie. These 
  features were pre-extracted from the movie trailer, and capture asthetic aspects of the 
  video. Each feature takes a continuous value. Type: float / continuous.
* ivec1 ... ivec20: 20 columns containing pre-computed audio features of the movie. These
  features were pre-extracted from the movie trailer, and capture a variety of sound features
  of the specific movie. Type: float / continuous
* YTID: Youtube link to the movie trailer on youtube. You may use this linke for qualitative 
  analysis. You are not required to use the links in your project. We do not guarantee that all 
  links are functional.

=======
Labels
=======
  
The single-label files (train_labels_single.tsv, valid_labels_single.tsv and test_labels_single.tsv)
contain the following columns:

* movieID: unique identifier for each movie (to be used for mapping movies to their labels)
* genres: the genre label


All genre labels are taken from the following set of 18 genres:
1. Action 
2 .Adventure 
3. Animation 
4. Children 
5. Comedy 
6. Crime 
7. Documentary 
8. Drama 
9. Fantasy 
10. Film_Noir 
11. Horror 
12. Musical 
13. Mystery 
14. Romance 
15. Scifi 
16. Thriller 
17. War 
18. Western

