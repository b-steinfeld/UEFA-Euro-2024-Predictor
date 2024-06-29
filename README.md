# 2024-Euros-Predictor
Goal: Trying to predict the 2024 Euros using webscrapping and machine learning.

Webscrapping: Extracted match data from the last five years of international soccer through FBref. However, within those five years, did not extract any data from friendly matches. Why? Friendly matches don't track signficant statistics, while also being considered to be less competitive games.

Model Predictor: The train data included matches prior to the 2022 World Cup, while the test data included the 2022 World Cup till matches prior to the 2024 Euros. However, my model (currently) does not predict draws. 

No Draws vs. With Draws: When games that involve draws are a part of the test data, the algorithm has a precision of about 70%; just enough to be classifed as a useful model. On the other hand, when games that involve draws are NOT a part of the test data, the algorithm has a precision of about 88%; very much can be considered to be a useful model. 

As my model (currently) does not predict draws, I decided not to try to predict the group stages as draws are possible. Furthermore, because the round of 16, quarter-finals, semi-finals, and finals, must all end with a win or loss for each team, in this scenario it is fair to say the model has a precision closer to 88% than that of 70%. 

Then, a future predictor was created; in which, the test data would be each part of the tournament (round of 16, quarterfinals, semifinals, and the final). As these are future matches, each of these csv(s) were manually created based on the outcome predicted for each part.

My Predicted Winner: Spain

For the future, I do want to come back to this project in order to:
1. remodel my algorithm in order to predict draws.
2. not having to manually create csv(s) for each part of the torunament I'm are predicing.
3. did not predict both sides (team becomes opponent, opponent becomes team); conflicting results?

Note: "matchesplusgroupstage.csv" was not used in the prediction process. Rather, just here if I decide to utilize it in anyway in the future.
