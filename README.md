# SteamAnalysis

## Introduction 

In the entertainment industry, the gaming sector has established itself as a prominent player (Newzoo, 2023). As game development and releases grow, it has become increasingly crucial for developers and publishers to comprehend the factors and decisions that contribute to a game's triumph. The present study endeavors to explore the feasibility of classifying games into distinct success levels based on their number of owners, positive ratings, and average playtime as features. These factors are believed to be strong indicators of a game's popularity and overall success. Other than quantifying measurements of success, the dataset contains several potential features that may contribute to high ownership which will be explored.

## Dataset

The dataset selected is from Kaggle's [Nik Davis Steam Store Games](https://www.kaggle.com/datasets/nikdavis/steam-store-games).
Collected in May 2019, any game releases or additional data past this mark is not reflected in the dataset.

| appid        | name           | release_date  | english | developer | publisher | platforms | required_age | categories | genres | steamspy_tags | achievements | positive_ratings | negative_ratings | average_playtime | median_playtime | owners | price |
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Unique ID for each app      | Title of app (game) | Release date in format YYYY-MM-DD | Language support: 1 if is in English | Name (or names) of developer(s). Semicolon delimited if multiple | Name (or names) of publisher(s). Semicolon delimited if multiple | Semicolon delimited list of supported platforms. At most includes: windows;mac;linux | Minimum required age according to PEGI UK standards. Many with 0 are unrated or unsupplied. | Semicolon delimited list of game categories, e.g. single-player;multi-player | Semicolon delimited list of game genres, e.g. action;adventure | Semicolon delimited list of top steamspy game tags, similar to genres but community voted, e.g. action;adventure | Number of in-games achievements, if any | Number of positive ratings, from SteamSpy | Number of negative ratings, from SteamSpy | Average user playtime, from SteamSpy | Median user playtime, from SteamSpy | Estimated number of owners. Contains lower and upper bound e.g. 20000-50000.| Current full price of title in GBP, (pounds sterling) |
