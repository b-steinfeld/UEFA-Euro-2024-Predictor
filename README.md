# 2024-Euros-Predictor
Goal: Trying to predict the 2024 Euros using webscrapping and machine learning.

Webscrapping: Extracted match data from the last five years of international soccer through FBref. However, within those five years, did not extract any data from friendly matches. Why? Friendly matches don't track signficant statistics, while also being considered to be less competitive games.

Model Predictor: The train data included matches prior to the 2022 World Cup, while the test data included the 2022 World Cup till matches prior to the 2024 Euros. However, my model (currently) does not predict draws. 

No Draws vs. With Draws: When games that involve draws are a part of the test data, the algorithm has a precision of about 70%; just enough to be classifed as a useful model. On the other hand, when games that involve draws are NOT a part of the test data, the algorithm has a precision of about 88%; very much can be considered to be a useful model. 

As my model (currently) does not predict draws, I decided not to try to predict the group stages as draws are possible. Furthermore, because the round of 16, quarter-finals, semi-finals, and finals, must all end with a win or loss for each team, in this scenario it is fair to say the model has a precision closer to 88% than that of 70%. 

Future Predictor: The train data included matches prior to the 2024 Euros, while the test data would be each round of the tournament (besides the group stages). As these are future matches, we cannot webscrape. Therefore, each CSV file (for each round) was manually created based on the outcome predicted for the prior round. (See the "Train+Test Data for Future Predictions" folder).

My Predicted Winner: Spain

This is my first ever major ML project. I'm proud of what I've done and learned along the way, and hope to continue learning and creating more!

For the future, I do want to come back to this project in order to:
1. remodel my algorithm in order to predict draws (which would allow me to try to predict the group stages and potentially gain better precision in my model).
2. not have to manually create CSV files for each part of the tournament I'm predicting (so, build code that automatically does this process).
3. did not predict both sides (team becomes opponent, opponent becomes team); possible conflicting results?
4. finishing adding notes to each part of the code in order to convey each lines/blocks purpose.
5. potentially figure out other ways to grow precision (more data, different reference, new model, etc)?
6. when the tournament is over, compare results.

Note: "matchesplusgroupstage.csv" was not used in the prediction process. Rather, just here if I decide to utilize it in anyway in the future.
