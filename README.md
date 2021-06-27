# Project 3: API and Classification of Reddit posts

---

## Background:

Dota 2 and League of legends are 2 of the most popular Multiplayer online battle arena (MOBA) games in the world. The competition for these games have a total prize pool of over USD 40 million and USD 6 million respectively. The game is played with 2 teams consisting of 5 players each going against each other. Each player will be controlling a single game character that will be able to cast spells and attack. The objective of the game is to destroy the opponent's 'Headquarter building'. The game is very popular worldwide and requires mechanical skills and good teamwork. 

---

## Problem Statement

Razor wants to market their products to the gaming community and wants to know what are the areas to target for 2 of the most popular MOBA games Dota2 and Leage of Legends. Razor only has budget to sponsor 1 of the gaming community and wants to target areas that best differentiates the 2 communities. 

To build a model that is able to differentiate reddit posts with high accuracy and provide the strongest features that differentiates the posts. To select one gaming community to promote their products and provide recommendations.

---

## Contents:
- [Data Cleaning / EDA](#data_cleaning)
- [Train-test-split](#train_test_split)
- [Logistic Regression](#logistic_regression)
- [Naive Bayes](#naive_bayes)
- [Random Forest](#random_forest)
- [Ada Boost](#ada_boost)
- [Support Vector Machine](#support_vector_machine)
- [Comparing models](#compare_model)
- [Conclusion and Recommendations](#conclusion_recommendations)

---

## Data Dictionary

| Columns   | Data type | Description                                                              |
|-----------|-----------|--------------------------------------------------------------------------|
| subreddit | object    | Subreddit the posts belong to. Dota2 and League of Legends respectively. |
| selftext  | object    | The content of the reddit post.                                          |
| title     | object    | Title of the reddit post.                                                |

---

## Conclusions and Recommendations

Stakeholders should use the Naive Bayes (TF-IDF) model as it has the highest accuracy in classifying the posts correctly. The features from the model is also easy to interpret. We also beat the baseline score of 56% with an accuracy score of 87%. To further improve the Naive Bayes model, we can try to collect more data, spend more time tuning the hyperparameters and remove frequently occuring words that are not differentiable between the 2 subreddits. One thing to note is the Naive Bayes model assumes that all the features are independent of each other. However this is rarely the case in real life as can be seen from our features (e.g. Evil Geniuses and the team players). This model will also not be able to differentiate other subreddit topics other than Dota 2 and LoL.

Dota 2 would be the better choice to focus their marketing on as they will be able to target areas with large audience exposure such as Competitions, professional players and teams. Instead of LoL where the target areas is within the game itself. The model is also better at predicting true Dota 2 posts than true LoL posts.

Some competitions to sponsor would be The International 10 (TI) which is next upcoming competition with a prize pool over 40 million USD. With a prize pool this large, viewership will most likely be very high.

Players and teams to sponsor would be Evil Geniuses and players from it such as iceciceice, Abed and Arteezy. Razor being a Singapore grown company will definitely resonate with iceiceice being a Singaporean professional Dota 2 player.
