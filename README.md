# Recommender-System-2020-Challenge---Polimi
Recommender system course accademid challenge

This is the repository for the Recommender system challenge 2020-2021 of the "Recommender systems" course at Politecnico di Milano

# Goal
The application domain is book recommendation. The datasets we provide contains both interactions between users and books, and tokens (words) extracted from the book text. The main goal of the competition is to discover which item (book) a user will interact with.

# Description

The datasets includes around 135k interactions, 7947 users, 25975 items and 20000 tokens. The training-test split is done via random holdout (85% training, 15% test). The goal is to recommend a list of 10 potentially relevant items for each user. MAP@10 is used for evaluation. You can use any kind of recommender algorithm you wish (e.g., collaborative-filtering, content-based, hybrid, etc.) written in Python.






# Evaluation
The evaluation metric for this competition is MAP@10.

# MAP@10
The average precision at 10, for a user is defined as:

where P(k) is the precision at cut-off k, rel(i) is 1 if item in position k is relevant, 0 otherwise, and m is the number of relevant items in the test set.

The mean average precision for N users at position 10 is the average of the average precision of each user, i.e.,






# Dataset Description
IMPORTANT: All files are comma-separated (columns are separated with ',' ) - including the submission file.

# Interactions files
data_train.csv
This file contains the training set, describing implicit preferences expressed by the users.
The file contains the following 3 columns:

row : identifier of the user
col : identifier of the item
data : value of the preference

# Item content file
data_ICM_title_abstract.csv
This file contains additional information about the items. The file contains, for each row, the id of the item, the id of the attribute (feature) and the value of the non-zero cells of the sparse item-content-matrix that represent the relative importance of each token for each item. The values refer to weighted text tokens extracted from the book.
Note that the tokens are anonymized and represented only by a numerical identifier.
The file is composed by 3 columns:

row : identifier of the item
col : identifier of the feature
data : value of the cell
data_target_users_test.csv
This file contains the ids of the users that should appear in your submission file. The submission file should only contain these users and not all those present in the train data.

sample_submission.csv
A sample submission file in the correct format: [user_id],[ordered list of recommended items]. Be careful with the spaces and be sure to recommend the correct number of items to every user.
