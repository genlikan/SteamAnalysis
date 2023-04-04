# SteamAnalysis

## Introduction 

In the entertainment industry, the gaming sector has established itself as a prominent player (Newzoo, 2023). As game development and releases grow, it has become increasingly crucial for developers and publishers to comprehend the factors and decisions that contribute to a game's triumph. The present study endeavors to explore the feasibility of classifying games into distinct success levels based on their number of owners, positive ratings, and average playtime as features. These factors are believed to be strong indicators of a game's popularity and overall success. Other than quantifying measurements of success, the dataset contains several potential features that may contribute to high ownership which will be explored. Steam is the eminent online software distribution platform. Created by Valve, Steam has become synonymous with PC gaming, which is where the main dataset used is collected.

## Dataset

The dataset selected is from Kaggle's [Nik Davis Steam Store Games](https://www.kaggle.com/datasets/nikdavis/steam-store-games).
Collected in May 2019, any game releases or additional data past this date is not reflected in the dataset.
The following table describes the features within steam.csv.
| appid        | name           | release_date  | english | developer | publisher | platforms | required_age | categories | genres | steamspy_tags | achievements | positive_ratings | negative_ratings | average_playtime | median_playtime | owners | price |
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Unique ID for each app      | Title of app (game) | Release date in format YYYY-MM-DD | Language support: 1 if is in English | Name (or names) of developer(s). Semicolon delimited if multiple | Name (or names) of publisher(s). Semicolon delimited if multiple | Semicolon delimited list of supported platforms. At most includes: windows;mac;linux | Minimum required age according to PEGI UK standards. Many with 0 are unrated or unsupplied. | Semicolon delimited list of game categories, e.g. single-player;multi-player | Semicolon delimited list of game genres, e.g. action;adventure | Semicolon delimited list of top steamspy game tags, similar to genres but community voted, e.g. action;adventure | Number of in-games achievements, if any | Number of positive ratings, from SteamSpy | Number of negative ratings, from SteamSpy | Average user playtime, from SteamSpy | Median user playtime, from SteamSpy | Estimated number of owners. Contains lower and upper bound e.g. 20000-50000.| Current full price of title in GBP, (pounds sterling) |

From initial assumptions, features such as 'appid', 'name' or 'achievements' may not have high (or any) feature importance.
The main target variable will be 'owners', and since it given as a range, the midpoint of this value will be used.

After some preliminary exploratory data analysis, here are some quick infographs.

The number of native English games (98.11%) to non-English (1.89%)

![newplot](https://user-images.githubusercontent.com/54910000/229918221-f2954e9d-d9bf-4651-b1c8-d749b84aedd2.png)

About 9.46% are free games, 90.54% are paid games.

![newplot (1)](https://user-images.githubusercontent.com/54910000/229919070-d11d4564-fbdc-4867-b8f8-b3e4783f9eb7.png)

The number of games released on Steam has exploded since 2014. (Mind the cut off for 2019 limited to the dataset collection)

![newplot (2)](https://user-images.githubusercontent.com/54910000/229919772-00895fbc-2ddc-4fae-b585-e485b60744c1.png)

Most certainly, there are correlations between 'positive_ratings', 'negative_ratings', 'average_playtime', 'median_playtime', and 'owners'. However the more curious finding will be what features that might correlate with success, will a type of category, platform, genre or tag succeed more than others.

There are an abundance of games released on the Steam platform, and as a side effect, great games with a lot of press that receives the most attention will shoot some games right out of the waters.
Games such as Dota2, Team Fortress 2, Counter-Strike:Global Offensive are (or have since become) free-to-play, accessible on Mac and Linux, and have dominant Esports presence, notably Dota2 having one of the hiest overall prize pools in Esports history at $40 million dollars (The International 2021, Dota 2 International Esports Tournament), it won't come as a surprise the amount of attention glued to these games are likely to be popular and to have high ownership, resulting in an over successful game that is likely to be considered an outlier.

Since the initial features like 'categories' and 'steamspy_tags' are semicolon delimited, feature engineering techniques like OneHotEncoder and LabelEncoder has been applied to allow some algorithms to be applied.

## Models Used
Linear Regression

XGBRegressor

RandomForestRegressor

KNeighborsRegressor

KMeans

NearestNeighbors

Decision Tree
