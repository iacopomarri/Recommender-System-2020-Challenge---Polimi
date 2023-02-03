# Recommender-System-2020-Challenge---Polimi
Recommender system course accademid challenge

This is the repository for the Recommender system challenge 2020-2021 of the "Recommender systems" course at Politecnico di Milano

Goal
The application domain is book recommendation. The datasets we provide contains both interactions between users and books, and tokens (words) extracted from the book text. The main goal of the competition is to discover which item (book) a user will interact with.

Description

The datasets includes around 135k interactions, 7947 users, 25975 items and 20000 tokens. The training-test split is done via random holdout (85% training, 15% test). The goal is to recommend a list of 10 potentially relevant items for each user. MAP@10 is used for evaluation. You can use any kind of recommender algorithm you wish (e.g., collaborative-filtering, content-based, hybrid, etc.) written in Python.
