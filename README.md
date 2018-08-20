# BIKER-ASE2018
The dataset and source code for paper "API Method Recommendation without Worrying About the Task-API Knowledge Gap"

The code is based on Python 2.7.12. The required packages are listed below:

numpy 1.13.3
gensim 3.2.0
nltk 3.2.5

In the main package, running test.py will output the evaluation result of BIKER (method-level recommendation) with our dataset. Running test_api_class.py will output the result of class-level recommendation.

The online.py file allows you to input any query online, and output the recommended top-5 API methods, along with the API summary. This file may take 30~60 seconds to preprocess the data (just once) before receiving your queries.
