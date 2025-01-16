### Gaming Success

**Julia Ryan**

#### Executive summary


#### Rationale
Millions of dollars are spent on computer games with thousands of games releasing each year. What should a gaming company do to ensure their product receives the right attention? What metrics are important to focus on?

#### Research Question
What makes a computer game successful?

#### Data Sources
Data set used is from Kraggle: https://www.kaggle.com/datasets/arnabchaki/popular-video-games-1980-2023/

#### Methodology
Successful games are generally defined by high consumer ratings.  Per ReviewTrackers (1), Western conducted a study showing purchasers are most influenced by reviews with an average rating of 4.2 to 4.5 stars, while Womply research showed that reviews between 4.0 - 4.5 earned 28% more revenue. Yogi (2) completed a study defining ideal star ratings per product.  For Toys and games, they found the ranges 4.0 - 4.5 or higher had the greatest impact.

In this dataset, we do not have the star rating overtime so focused on a range of 3.8 to 5 assuming that these numbers indicated the product was within the "good range" for a significant period of time. 

(1) https://www.reviewtrackers.com/blog/5-star-rating/#:~:text=Most%20people%20think%20it's%20too,star%20rating%20for%20purchase%20probability.
(2) https://www.meetyogi.com/post/what-makes-a-good-star-rating-for-products-in-different-industries

Models were trained on the training set and validated with the test set. Additionally, RandomizedSearchCV was used to evaluate models using accuracy score, and fine tuned each model's hyperparameters to maximize this metric.  Accuracy is suitable because we have a balanced dataset and measures the proportion of correctly predicted observations out of total observations. It is calculated as (True Positive count + True Negative count) / (Total count), or

$$
\frac{TP + TN}{TP + TN + FP + FN}
$$


Four models were trained, fine-tuned, and compared to find the best model for this task.


#### Results
The best model was the LogisticRegression with C=0.6. This resulted in an accuracy score of .968 with the training score of .955. 

Using the data collected for 1512 games, we isolated 8 key metrics that were identified as common for games with product reviews in the "good range". These metrics are as follows: Count of entries in wishlist, Active players, Positive review count, Number of players who reviewed the game or listed it in some manner, Negative review count, Number of players who list the game in their backlog of games to play, and Number of players who used to play the game.

As expected negative and positive reviews were consistently high indicators of the game's success as was the number of current players. Nearly as important were the number of people who listed the game on their account and how many players reviewed the game. 

Interestingly as the count of players who used to play the game increased, the games success rate drops. This seems to indicate while many players started to play the game, they did not continue causing the played volume to be significantly greater than the playing volume.

In no model, did the genre of the game play a significant impact on the game rating. We assume this is due to the players knowing which genres are most interesting to them and avoiding genres that are not interesting. Some genre groups did have some impact in a few models. More data would be required to find the most popular genre. 


#### Next steps
This model indicates focus should be on encouraging two aspects: 1) Encouraging players to add to wishlist, and 2) Achieving a high review volume with both negative and positive reviews. More marketing research should be pulled to determine how best to achieve this with the company's primary audiences.

Currently this data was pulled from a single review source: [Backloggd](https://www.backloggd.com/games/lib/popular/) and should be expanded to include more sites like Steam or Microsoft Game Store which track actual game play rates as well as ratings.  With a larger dataset, additional analysis could be done on specific genres to determine if there are tighter links to time played, how frequently played, and impact of game updates.     

#### Outline of project

- [Gaming Analysis]()


##### Contact and Further Information
Julia Ryan
