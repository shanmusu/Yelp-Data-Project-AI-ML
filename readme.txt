System requirements:
Jupyter notebook
Python version 2.7
Packages needed: Pattern, NLTK

Steps for running the code:
1) Download Yelp Academic Dataset from the Internet. Feed files yelp_academic_dataset_business.json and yelp_academic_dataset_review.json to filter_data.ipynb.
 Filter data file is used to extract restaurants in a particular city and reviews related to that restaurant. The output of this code is Phoenix_restaurants.json and Phoenix_restaurant_reviews.json.

2) The next step is to summarize all the reviews to meaningful phrases, determine the polarity of filtered phrases and give a score to each of the words in the phrases.
 We feed the file Phoenix_restaurant_reviews.json to review_summarization.ipnyb for this purpose and output file Phoenix_restaurant_review_Results.csv is generated. 
The output file contains extracted phrases and their respective polarities.

3) We now have the phrases extracted and the polarity calculated from the reviews, hence using Phoenix_restaurant_review_Results.csv from step2,
 we can now execute the jupyter notebook 'yelp_project_classify.ipynb' step by step to verify the following:
- correlation
- classification
- phrase categorization
- visualization
- restaurant evaluation. 

4) For restaurant evaluation, we changed the categories to 'Pizza' in filter_data.py() and reran the same code to generate restaurant_reviews_Pizza.json. 
This json file was used by review_summarization.py to generate the phrases only for Pizza restaurants.The following lines of code were modified in filter_data.py to extract Pizza only restaurants:
'Pizza' in each_business['categories']
fileName=city + '_restaurant_reviews_Pizza.json'

The following csv files are included in the zip folder to perform the above tasks:
Phoenix_restaurant_review_Results.csv 
yelp_restaurants_business_data.csv
yelp_reviews_pizza.csv
CategorizingPhrases_Visualization.csv
Phrase_visualization_stackedbar.csv
Phoenix_restaurant_reviews_Pizza_Results.csv